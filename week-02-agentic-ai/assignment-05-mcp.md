# Assignment 5 — Connecting Claude to the Outside World

Part of the DevOps Micro Internship (DMI) with Agentic AI

---

## Purpose

In this assignment, you will connect Claude Code to external systems using MCP (Model Context Protocol). You will configure the GitHub MCP server, securely store credentials, verify the connection, and run a live query that proves Claude is accessing real-time GitHub data.

---

# Task 1 — Create a GitHub Personal Access Token

## Goal

Generate a GitHub Personal Access Token (PAT) that will be used for MCP authentication.

### Evidence

#### Screenshot 1 — GitHub token creation page showing the selected scopes (`repo`, `read:user`) — token value must NOT be visible

![Screenshot 1 — Token name and 30-day expiry](screenshots/a5-ss1-token-scopes-1.png)

![Screenshot 1 — repo scope selected](screenshots/a5-ss1-token-scopes-2.png)

![Screenshot 1 — read:user scope selected](screenshots/a5-ss1-token-scopes-3.png)

---

# Task 2 — Create .mcp.json at the Project Root

## Goal

Create and configure the `.mcp.json` file to define the GitHub MCP server.

### Evidence

#### Screenshot 2 — `.mcp.json` open in VS Code showing the full configuration

![Screenshot 2 — .mcp.json with the GitHub MCP server configuration](screenshots/a5-ss2-mcp-json.png)

---

# Task 3 — Add Your Token to settings.local.json

## Goal

Store your GitHub token securely in `.claude/settings.local.json` and ensure it is not committed to version control.

### Evidence

#### Screenshot 3 — `settings.local.json` open in VS Code showing the `env` section — **blur or cover the actual GitHub token value**

![Screenshot 3 — settings.local.json env section (token hidden)](screenshots/a5-ss3-settings-local.png)

---

# Task 4 — Verify the Connection with /mcp

## Goal

Confirm that the GitHub MCP server is successfully connected inside Claude Code.

### Evidence

#### Screenshot 4 — `/mcp` output showing `github: connected`

![Screenshot 4 — /mcp showing the GitHub MCP server connected](screenshots/a5-ss4-mcp-connected.png)

---

# Task 5 — Run a Live GitHub Query

## Goal

Verify MCP functionality by retrieving real-time data from your GitHub account using Claude Code.

### Evidence

#### Screenshot 5 — Claude's response showing the GitHub MCP tool call and the retrieved README.md content.

![Screenshot 5 — Claude calling the GitHub MCP tool and returning README.md](screenshots/a5-ss5-github-readme-query.png)

![Screenshot 5 — README.md content retrieved from GitHub](screenshots/a5-ss5-github-readme-query-2.png)

---

# Task 6 — Share Your MCP Achievement

## Goal

Share your MCP achievement on Facebook or WhatsApp Status and provide evidence of the published post/status.

### Evidence

#### Screenshot 6 — Published Facebook post or WhatsApp Status showing your MCP achievement message and leaderboard progress link visible

Add your screenshot here.

---

# Submission Instructions

- Ensure `.mcp.json` is committed to your GitHub repository
- Ensure `.claude/settings.local.json` is NOT committed (must be gitignored)
- Confirm token value is hidden in all screenshots
- Add all required screenshots to your submission
- Push final changes to your forked repository

---

## GitHub Repository URL

Paste your forked repository URL here:

`https://github.com/faiyaadmahabub-hash/Ultimate-Agentic-DevOps-with-Claude-Code`

---

## Security Confirmation

Confirm below:

- [x] `settings.local.json` is added to `.gitignore`
- [ ] GitHub token is NOT exposed in repository or screenshots

---

# Completion Checklist

- [x] GitHub PAT created with correct scopes (`repo`, `read:user`)
- [x] `.mcp.json` created at project root
- [x] `.claude/settings.local.json` contains token (hidden in screenshot)
- [ ] `.claude/settings.local.json` is NOT committed
- [x] `/mcp` shows GitHub connection as active
- [x] Live GitHub query returns real repository data
- [ ] All required screenshots added
- [x] GitHub repository URL included
- [ ] MCP achievement shared on Facebook or WhatsApp Status
- [ ] Screenshot 6 added showing the published post/status

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

*This submission is part of DevOps Micro Internship (DMI) — Agentic AI Track.*