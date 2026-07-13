# GitHub Issues & Workflow Guide for AI Agents

Welcome, AI Agent! When assisting with the `apex-theraphy-website` project, it is critical to maintain discipline in our work tracking. We use GitHub Issues and Milestones as our single source of truth for all tasks, bugs, and feature development.

**Every time you begin working on a request, you must follow these rules.**

## 🎯 Core Principles
1. **No Ghost Code:** Every piece of work (feature, bugfix, refactor) MUST be tracked by a GitHub Issue.
2. **Transparent Progress:** Keep issues updated with comments about your progress, blockers, or design decisions.
3. **Milestone Tracking:** Every issue should belong to an active Milestone to track our overall project timeline.

---

## 📋 Standard Workflow

### 1. Discovery (Before writing code)
- **Check Existing Issues:** Before creating a new issue, use GitHub search tools (`search_issues` or `list_issues`) to check if an issue already exists for the task.
- **Read Context:** If an issue exists, use `issue_read` to understand its requirements, constraints, and current status.

### 2. Issue Creation (If no issue exists)
- **Create Issue:** Use `issue_write` to create a new issue for the work requested by the user.
- **Structure:**
  - **Title:** Clear and descriptive (e.g., `Feature: Add Hero Section to Homepage`, `Bug: Mobile navigation menu not closing`).
  - **Body:** Provide a clear description of what needs to be done, including acceptance criteria.
  - **Labels:** Apply relevant labels (`enhancement`, `bug`, `documentation`, etc.).
  - **Milestone:** Assign it to the current active milestone (check with the user or use milestone APIs if available).

### 3. Execution & Updates
- **Document Decisions:** If you make a significant architectural or design decision, add an issue comment documenting your thought process.
- **Track Progress:** If a task takes multiple steps or spans across multiple chat sessions, leave a status update comment on the issue.

### 4. Completion & PRs
- **Linking:** When creating Pull Requests (or commits), reference the issue number using closing keywords (e.g., `Closes #12`, `Fixes #45`) so the issue closes automatically upon merge.
- **Manual Closing:** If no PR is needed (e.g., direct commits or non-code tasks), ensure you explicitly close the issue when the task is fully verified and completed.

---

## 🛠️ GitHub MCP Tools Reference
To accomplish these tasks, you have access to the `github-mcp-server`. Please utilize tools like:
- `search_issues` / `list_issues`: Find existing work.
- `issue_read`: Get details on a specific task.
- `issue_write`: Create new tasks or update existing ones.
- `add_issue_comment`: Leave progress updates.

**By strictly adhering to this guide, you will help us maintain a perfectly synchronized and well-documented repository. Thank you!**
