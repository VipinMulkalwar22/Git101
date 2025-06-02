# Understanding Git Logs

## What is `git log`?

The `git log` command shows the history of commits in your repository. It helps you see what changes were made, when, and by whom.

---

## 1. Checking Git Log Output

If you run `git log` in a new repository **before making any commits**, you will see an error:

```
fatal: your current branch 'master' does not have any commits yet
```

This means there is no history to show yet.

---

## 2. Viewing Commit History

Once you have committed files, running `git log` will display a list of commits. Each commit shows details like:

- Commit hash (unique ID)
- Author
- Date
- Commit message

**Example output:**
```
commit 1a2b3c4d5e6f7g8h9i0j
Author: vipin <vipin@example.com>
Date:   Mon Jun 10 10:00:00 2024 +0000

    Added xyz content to file
```

---

## 3. What Information is NOT Displayed by Default?

By default, `git log` **does not show the list of files changed** in each commit.

---

## 4. How to See Changed Files in Each Commit

You can use the `--name-only` option to display the names of files changed in each commit:

```
git log --name-only
```

---

## 5. Which Branch Has the Changes?

The branch information is shown in the first line of the `git log` output, where you might see something like:

```
commit 1a2b3c4d (HEAD -> main)
```
Here, `main` is the branch where the commit was made.

---

## 6. Compact Log Output

To see the log in a compact, one-line-per-commit format, use:

```
git log --oneline
```

---

## 7. Limiting the Number of Commits Shown

If your repository has many commits and you want to see only the last 3, use:

```
git log -n 3
```

You can also combine this with `--name-only` to see the files changed in the last 3 commits:

```
git log -n 3 --name-only
```

---

## 8. Customizing Log Output

You can format the log output to show specific details, for example:

```
git log --pretty=format:"%h - %an, %ar : %s"
```
- `%h`: abbreviated commit hash
- `%an`: author name
- `%ar`: relative date
- `%s`: subject (commit message)

---

## 9. Searching Commit Messages

To find commits with a specific keyword (e.g., "fix bug") in the message:

```
git log --grep="fix bug"
```

---

## Diagram: How `git log` Fits in the Workflow

```
+-------------------+      git add      +-------------------+      git commit      +-------------------+
| Working Directory | --------------->  |   Staging Area    |  --------------->   |   Repository      |
|  (edit files)     |                   |   (index)         |                     | (commit history)  |
+-------------------+                   +-------------------+                     +-------------------+
                                                                                           |
                                                                                           |
                                                                                     git log shows
                                                                                     commit history
```

---

*Use these commands to explore your project's history and understand what has changed over time!*