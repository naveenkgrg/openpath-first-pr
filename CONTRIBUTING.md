# Contributing

Welcome. This guide helps you make your first pull request in a safe, friendly repo.

## Quick steps

1. Fork the repository.
2. Clone your fork to your computer:
   ```bash
   git clone https://github.com/<your-username>/openpath-first-pr.git
   cd openpath-first-pr
   ```
3. Create a new branch for your change:
   ```bash
   git checkout -b add-your-name
   ```
4. Add one line to `participants.md`.
5. Commit your change:
   ```bash
   git add participants.md
   git commit -m "Add my name"
   ```
6. Push your branch:
   ```bash
   git push -u origin add-your-name
   ```
7. Open a pull request on GitHub.

## How to Avoid and Resolve Pull Request Conflicts

Working with others means the repo can change while you work. This section shows how to keep your fork up to date and what to do if conflicts happen.

### Scenario 1: Syncing a Fork (Recommended First Step)

**What it means:** Syncing a fork means copying the latest changes from the original repo into your fork so you start from the newest version.

**When to sync:**
- Before starting work
- When the repo has new changes
- Before opening a PR

**GitHub UI (Sync fork → Update branch):**
- Go to your fork on GitHub.
- Click `Sync fork`.
- Click `Update branch`.
- Your fork now has the latest changes.

**Git CLI (fetch upstream, merge, push):**
1. Add the original repo as `upstream` (one-time setup):
   ```bash
   git remote add upstream https://github.com/openpath/openpath-first-pr.git
   ```
2. Get the latest changes:
   ```bash
   git fetch upstream
   ```
3. Move your local main branch to the newest version:
   ```bash
   git checkout main
   git merge upstream/main
   ```
4. Update your fork on GitHub:
   ```bash
   git push origin main
   ```

**Reminder:** Syncing early helps prevent conflicts later.

### Scenario 2: Resolving a Merge Conflict

**What it is:** A merge conflict happens when two people change the same lines and Git needs you to choose what to keep.

Conflicts are normal in open source and are easy to fix with a few steps.

**Resolve conflicts using GitHub UI:**
- Open your pull request on GitHub.
- If GitHub shows “This branch has conflicts,” click `Resolve conflicts`.
- Edit the file in the browser to keep the correct lines.
- Click `Mark as resolved`, then `Commit merge`.

**Resolve conflicts locally using Git:**
1. Get the latest changes:
   ```bash
   git fetch upstream
   ```
2. Merge them into your branch:
   ```bash
   git checkout add-your-name
   git merge upstream/main
   ```
3. Open the conflicted file and edit it by hand.
4. Save the file, then finish the merge:
   ```bash
   git add participants.md
   git commit
   ```
5. Push your updated branch:
   ```bash
   git push
   ```

**Tips to avoid conflicts:**
- Sync your fork before you start.
- Make small changes and open your PR soon.
- Avoid editing the same line as someone else if you can.

## Branching and commits

- Use a short branch name like `add-your-name`.
- Keep your commit message simple, such as "Add my name".
- Only include one line change in `participants.md`.

## What reviewers look for

- You followed the one-PR rule.
- You added only one line in the correct format.
- You did not include private or sensitive information.

## Learning from feedback

If a reviewer requests changes, update your branch and push again. Feedback is normal in open-source projects and helps you grow as a contributor.
