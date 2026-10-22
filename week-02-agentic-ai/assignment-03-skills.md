# Assignment 3 — Building Your Command Center

Part of the DevOps Micro Internship (DMI) Cohort 3 with Agentic AI

---

## Purpose

In this assignment, you will build a local Claude Skills system by creating the `.claude/skills/` folder structure, adding predefined skill files, and executing a real agentic command (`/scaffold-terraform`) to generate infrastructure code. You will also observe how skills enforce tool restrictions and enable controlled automation.

---

# Task 1 — Create the Skill Folder Structure

## Goal

Create the required `.claude/skills/` directory structure for all skills.

### Evidence

#### Screenshot 1 — VS Code sidebar showing `.claude/skills/` folder with all 4 subfolders visible

![Screenshot 1 — .claude/skills/ with all 4 skill folders](screenshots/a3-ss1-skills-folders.png)

---

# Task 2 — Add the Skill Files

## Goal

Place all required skill files into their correct directories and verify their configuration.

### Evidence

#### Screenshot 2 — `.claude/skills/scaffold-terraform/` open in VS Code showing both `SKILL.md` and `template-spec.md`

![Screenshot 2 — scaffold-terraform/ showing SKILL.md and template-spec.md](screenshots/a3-ss2-scaffold-terraform-files.png)

---

#### Screenshot 3 — Screenshot 3 — `tf-plan/SKILL.md` frontmatter showing `allowed-tools: Bash, Read, Grep` (no Write) and `disable-model-invocation: true`

![Screenshot 3 — tf-plan/SKILL.md frontmatter with allowed-tools and disable-model-invocation](screenshots/a3-ss3-tf-plan-frontmatter.png)

---

# Task 3 — Run /scaffold-terraform

## Goal

Execute the `/scaffold-terraform` skill to generate a full Terraform infrastructure setup.

### Evidence

#### Screenshot 4 — Claude's response showing the scaffold complete with the file list

![Screenshot 4 — /scaffold-terraform complete with the 5-file list](screenshots/a3-ss4-scaffold-complete.png)

---

#### Screenshot 5 — VS Code sidebar showing the `terraform/` folder with all generated files inside

![Screenshot 5 — terraform/ folder with all 5 generated files](screenshots/a3-ss5-terraform-folder.png)

---

# Task 4 — Run terraform init and /tf-plan

## Goal

Initialize Terraform and execute the `/tf-plan` skill to observe plan execution and output analysis.

### Evidence

#### Screenshot 6 — Claude's `/tf-plan` response showing it ran the command and analyzed the result (pass or auth error both count)

![Screenshot 6 — Claude analysing the /tf-plan result (AWS credentials error)](screenshots/a3-ss6-tf-plan-analysis.png)

---

# Submission Instructions

- Ensure `.claude/skills/` folder and all skill files are committed to your GitHub repository
- Run all commands successfully and capture required screenshots
- Push final changes to your forked repository

---

## GitHub Repository URL

Paste your forked repository URL here:

`https://github.com/faiyaadmahabub-hash/Ultimate-Agentic-DevOps-with-Claude-Code`

## LinkedIn post URL

Paste your forked repository URL here:

`Add your URL here`

---

# Completion Checklist

- [x] `.claude/skills/` folder created with all 4 skill folders
- [x] All skill files placed correctly
- [x] `tf-plan/SKILL.md` shows correct `allowed-tools` restrictions
- [x] `/scaffold-terraform` executed successfully
- [x] Terraform files generated inside `terraform/` folder
- [x] `terraform init` executed successfully
- [x] `/tf-plan` executed and output analyzed by Claude
- [x] All required screenshots added
- [x] GitHub repository URL included
- [ ] LinkedIn post URL included

---

## 📌 About DMI & CloudAdvisory

DevOps Micro Internship (DMI) is a project-based DevOps program run by Pravin Mishra (The CloudAdvisory) focused on real-world execution, systems thinking, and career readiness.

It helps learners build strong DevOps foundations with hands-on experience.

---

## 📌 Resources

- 🌐 DMI Official Website: https://dmi.pravinmishra.com?utm_source=github&utm_medium=readme  
- 🎓 University: https://university.pravinmishra.com?utm_source=github&utm_medium=readme  
- 💬 Discord Community: https://discord.pravinmishra.com?utm_source=github&utm_medium=readme  
- 📝 Blog: https://dmi.pravinmishra.com/blog?utm_source=github&utm_medium=readme  
- ▶️ YouTube Playlist: https://www.youtube.com/playlist?list=PLFeSNDtI4Cho  
- 🔗 Pravin Mishra (LinkedIn): https://www.linkedin.com/in/pravin-mishra-aws-trainer/  
- 🏢 CloudAdvisory (LinkedIn): https://www.linkedin.com/company/thecloudadvisory/

---

*This submission is part of DevOps Micro Internship (DMI) Cohort 3 — Agentic AI Track.*
