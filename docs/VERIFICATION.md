# Content/configuration verification — 17 October 2026

This repository is a Markdown coursework journal based on an upstream program template. No application runtime, infrastructure provisioning, deployment, account login or external service request was required for this review.

## Local checks and results

From the repository root, Windows/Python 3.10.9:

```powershell
rg --files -g '!*.png' -g '!*.jpg' -g '!*.jpeg' -g '!*.svg' -g '!*.pdf'
git log --format="%h %an %s" -- week-00-internet-and-networking week-01-success-mindset
```

Result: 14 week directories; 77 root-level assignment Markdown files; 101 Markdown files overall before these documentation edits; 14 badge SVGs and 432 PNGs including upstream onboarding/solution images. The Week 00 submission screenshot folder contains five files. Counts are content inventory, not completion metrics. Reviewed actual written answers in Weeks 00 and 01 and the unchecked completion list in the root-level Week 02 first assignment. The history distinguishes personal changes by `takif0` from course-author/template updates.

The following Python checks were executed locally with existing PyYAML; use `BaseLoader` so the GitHub Actions `on` key is not coerced by YAML 1.1 boolean parsing:

```python
from pathlib import Path
import json
import yaml
root = Path('.')
workflow = yaml.load(
    (root / '.github/workflows/block-external-prs.yml').read_text(encoding='utf-8'),
    Loader=yaml.BaseLoader,
)
assert workflow['on']['pull_request_target']['types'] == ['opened', 'reopened']
assert workflow['permissions'] == {'pull-requests': 'write'}
steps = workflow['jobs']['block-non-collaborator-prs']['steps']
assert all('run' not in step for step in steps)
assert all('checkout' not in str(step) for step in steps)
json.loads((root / '.vscode/settings.json').read_text(encoding='utf-8'))
for item in ['INSTRUCTIONS.md', 'dmi_resources.md', 'onboarding',
             'week-00-internet-and-networking/assignment-01-internet-and-networking.md',
             'week-01-success-mindset/assignment-01-mindset-os.md']:
    assert (root / item).exists()
```

Result: passed. The workflow uses `pull_request_target` and write permission to comment on and close external PRs via `actions/github-script`; it does not check out or execute pull-request code. This was a configuration inspection, not a workflow run or a broader security certification. No root `package.json`, `Dockerfile` or `main.tf` exists, so application build/test/deploy commands do not apply.

## Provenance and limits

Week 02 worked examples under `assignment-solutions/`, course screenshots, badges and curriculum are upstream educational material, not newly authored deployment evidence. Instructions explicitly require personal answers in the week root. The original README's Weeks 00/01 completion entries were not independently graded or externally verified.

No screenshot was generated for this review: existing images remain historical artifacts in place. No certificate, award, cloud deployment, later assignment completion, external link availability or production result is asserted. The corrected overview points to the actual `dmi_resources.md` rather than the old missing `dmi_cohort3_resources.md` name. Other upstream materials and automation remain unchanged.
