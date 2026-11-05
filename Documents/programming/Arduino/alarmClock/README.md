
## 1. Install and sign in
1. Download [GitHub Desktop for Windows](https://desktop.github.com/).
2. Install and open it.
3. Click **Sign in to GitHub.com** and complete the browser login.
4. Confirm the name and email Git will attach to your commits.

## 2. Clone the repository
1. In GitHub Desktop, click **File → Clone repository**.
2. Select the **URL** tab.
3. Enter your repository address:

   ```text
   https://github.com/minchaumc/AlarmClock.git
   ```

4. Under **Local path**, choose where to store it on your computer.
5. Click **Clone**.
6. Select **Repository → Show in Explorer** to open the downloaded folder.

## 3. Pull updates before editing

When other users commit a change to the repository, you can update their changes by "pulling" said change

1. Select your project under **Current repository**.
2. Check that **Current branch** is `main`, unless your team uses another branch.
3. Click **Fetch origin**.
4. If the button changes to **Pull origin**, click it.
5. Wait for it to finish before editing.

## 4. Commit your changes

A commit saves a version of your selected changes **on your computer**.

1. Open the **Changes** tab.
2. Click each changed file to review it. **Red** shows removed lines; **green** shows added lines.
3. Check the files you want included.
4. In **Summary**, describe what you changed, such as:

   ```text
   Add snooze button
   ```

6. Click **Commit to main** (or the name of your current branch).

Your changes are now committed locally (in your computer), but **they are not uploaded yet to for other users to see**.

## 7. Push your commits

A push uploads your commits to GitHub.

1. Click **Push origin** at the top.
2. Wait for the upload to finish.
3. Select **Repository → View on GitHub** to check the online version.

If your push is rejected because someone else uploaded changes, fetch and pull first. If a conflict appears, resolve it with your teammate before pushing again.

## Summary

1. **Fetch → Pull** if updates are available.
2. **Edit → Save** in Arduino IDE.
3. **Review → Commit** in GitHub Desktop.
4. **Push origin** to upload.

Saving, committing, and pushing are separate steps. Uploading the program to your Arduino board is also separate—you still do that through Arduino IDE.
