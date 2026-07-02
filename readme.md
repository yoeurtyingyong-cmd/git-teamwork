# Git Teamwork Guide

This project is a simple static website with these main areas:

- `index.html` - home page
- `client/product.html` - client product page
- `admin/dashboard.html` - admin dashboard page

Use this guide when working together as a team with Git and GitHub.

## 1. Clone the Project

Each team member should copy the project to their own computer first.

```bash
git clone <repository-url>
cd git-teamwork
```

Example:

```bash
git clone https://github.com/your-team/git-teamwork.git
cd git-teamwork
```

## 2. Check the Current Status

Before making changes, check your Git status.

```bash
git status
```

If there are no changes, Git will show that your working tree is clean.

## 3. Get the Latest Code

Always update your local project before starting new work.

```bash
git pull origin main
```

This helps prevent conflicts with your teammates' work.

## 4. Create Your Own Branch

Do not work directly on `main`. Create a branch for your task.

```bash
git checkout -b <branch-name>
```

Good branch name examples:

```bash
git checkout -b feature-homepage
git checkout -b feature-product-page
git checkout -b feature-admin-dashboard
git checkout -b fix-navbar-link
```

## 5. Work on Your Assigned File

Team members can divide the work like this:

- Homepage member: edit `index.html`
- Client page member: edit `client/product.html`
- Admin page member: edit `admin/dashboard.html`
- Documentation member: edit `readme.md`

Open the HTML file in your browser to test your changes.

## 6. Check What You Changed

After editing files, check your changes.

```bash
git status
git diff
```

Use `git status` to see changed files.
Use `git diff` to review the exact code changes.

## 7. Save Your Work with a Commit

Add your changed files.

```bash
git add .
```

Commit your changes with a clear message.

```bash
git commit -m "Add product page layout"
```

Good commit message examples:

```bash
git commit -m "Update homepage title"
git commit -m "Add dashboard cards"
git commit -m "Style product list"
git commit -m "Fix broken client page link"
```

## 8. Push Your Branch to GitHub

Upload your branch.

```bash
git push origin <branch-name>
```

Example:

```bash
git push origin feature-product-page
```

## 9. Create a Pull Request

On GitHub:

1. Open the repository page.
2. Click **Compare & pull request**.
3. Write a short title and description.
4. Explain what files you changed.
5. Ask a teammate to review your work.

Example pull request description:

```text
Added product cards to client/product.html.
Tested the page in the browser.
```

## 10. Review Teammate Changes

Before merging, another team member should review the pull request.

Check these things:

- The page opens correctly in the browser.
- The code is easy to read.
- The change does not break other pages.
- The commit message is clear.

If something needs to be fixed, leave a comment on the pull request.

## 11. Merge the Pull Request

After review, merge the pull request into `main`.

On GitHub:

1. Open the pull request.
2. Click **Merge pull request**.
3. Confirm the merge.

## 12. Update Your Local Main Branch

After a teammate merges changes, everyone should update their local project.

```bash
git checkout main
git pull origin main
```

Then create a new branch for the next task.

```bash
git checkout -b <new-branch-name>
```

## 13. If There Is a Merge Conflict

A merge conflict happens when two people edit the same part of the same file.

To reduce conflicts:

- Pull the latest code before starting work.
- Work on separate files when possible.
- Commit small changes often.
- Tell teammates which file you are editing.

If Git shows a conflict:

```bash
git status
```

Open the conflicted file and look for lines like this:

```text
<<<<<<< HEAD
Your code
=======
Teammate code
>>>>>>> branch-name
```

Choose the correct code, delete the conflict markers, then commit the fix.

```bash
git add .
git commit -m "Resolve merge conflict"
```

## Team Rules

- Always pull before starting work.
- Always create a branch for your task.
- Do not commit directly to `main`.
- Use clear commit messages.
- Test your page in the browser before pushing.
- Review pull requests before merging.
- Communicate with teammates about which files you are editing.

## Common Commands

```bash
git status
git pull origin main
git checkout -b feature-name
git add .
git commit -m "Describe your change"
git push origin feature-name
git checkout main
git pull origin main
```
