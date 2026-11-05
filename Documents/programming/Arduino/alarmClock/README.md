# Arduino + GitHub: Quick Beginner Guide

Use Git to save versions of your Arduino code and GitHub to store them online. This guide assumes your project is already connected to a GitHub repository.

## Everyday workflow

### 1. Open your project folder

Save your sketch in Arduino IDE, then open a terminal in its folder:

```bash
cd ~/Arduino/AlarmClock
```

Replace this example path with your actual project folder. Keep the main sketch and its folder names matching, such as `AlarmClock/AlarmClock.ino`.

### 2. Check your changes

```bash
git status
git diff
```

- `git status` lists changed and new files.
- `git diff` shows unstaged changes to tracked files. `-` marks removed lines; `+` marks added lines. Press `q` to exit if a viewer opens.

### 3. Stage, commit, and push

```bash
git add .
git commit -m "Add snooze button"
git push
```

- **Stage (`add`):** select changes for the next commit. `.` includes changes under the current folder, except ignored files. Review `git status` before committing.
- **Commit:** save a snapshot locally. Use a short message describing your changes.
- **Push:** upload your commits to GitHub.

To stage just one file instead:

```bash
git add AlarmClock.ino
```

Saving in Arduino IDE does not automatically commit or push. Pushing to GitHub does not upload code to your Arduino board.

## First push only

If your branch is named `main` and the remote is already configured:

```bash
git push -u origin main
```

| Term | Meaning |
| --- | --- |
| `origin` | WHERE: the nickname for your GitHub repository URL |
| `main` | WHICH branch: your primary line of development |
| `-u` | Remember the remote branch for future pushes and pulls |

After this, use `git push` while on `main`. You do not need to repeat `git init`, `git remote add`, or login for every update.

## Working on multiple computers or with others

Before making local edits, get the latest committed changes:

```bash
git pull --ff-only
```

If pulling fails or pushing is rejected, read the error before continuing. Do not force-push to bypass it; ask for help if you are unsure.

## Useful checks

```bash
git status          # Current branch and file changes
git diff --staged   # Changes selected for the next commit
git log --oneline   # Commit history
git remote -v      # Remote names and URLs
git branch         # Local branches; * marks the current one
```

If Git says `nothing to commit`, save your file and check that you are in the correct folder. If it says `Everything up-to-date`, there are no new commits to upload.

Never commit passwords, access tokens, or Wi-Fi credentials. Keep secrets in an ignored file.
