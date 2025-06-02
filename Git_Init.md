# Initializing a Git Repository

## 1. How to Start Tracking a Project with Git

To start using Git in your project, **initialize a repository**:

```
git init
```

This creates a hidden folder called `.git` in your project directory.  

**Diagram: Project Structure After `git init`**
```
Your Project Folder
├── xyz.txt
└── .git   (hidden folder created by git init)
```

---

## 2. Adding Files to Your Project

To add a file (e.g., `xyz.txt`) to your project and start tracking it:

```
git add xyz.txt
```

---

## 3. Checking the Status of Files

To see which files are being tracked or untracked, use:

```
git status
```

- **Untracked:** Files that are not yet being tracked by Git (e.g., `xyz.txt` before adding).
- **Staging Area:** Where files go after `git add`, ready to be committed.

---

## 4. Staging and Committing Changes

- **Stage a file:**  
  `git add xyz.txt`
- **Commit staged files:**  
  `git commit -m "Added xyz content to file"`

---

## 5. Configuring User Information

Before making commits, it's important to set your user information so Git can record who made each change.

- **Set your name and email for the current repository:**
  ```
  git config user.name "vipin"
  git config user.email vipin@example.com
  ```

- **Set your name and email globally (for all repositories on your system):**
  ```
  git config --global user.name "vipin"
  git config --global user.email vipin@example.com
  ```

- **Check your current configuration:**
  ```
  git config --list
  ```

- **Edit the configuration file directly (optional):**
  ```
  git config --global --edit
  ```

> Setting your user information globally is recommended if you use the same identity for all your projects.  
> You can override it per repository if needed.

---

## 6. Ignoring Files

If you have files you **do not want Git to track** (e.g., `notes.txt`), use a `.gitignore` file.

- Create a `.gitignore` file:
  ```
  touch .gitignore
  ```
- Add the filename (e.g., `notes.txt`) to `.gitignore`.

After this, `notes.txt` will not appear in `git status` output.

---

## 7. Should You Track `.gitignore`?

**Yes!**  
You should commit the `.gitignore` file to your repository so everyone working on the project ignores the same files.

---

## Visual Diagram: Git File Lifecycle

```
+----------------+      git add      +-------------+      git commit      +---------------------+
|   Untracked    | --------------->  |   Staged    |  --------------->   | Tracked in Repo     |
|   (new file)   |                   | (index)     |                     | (committed history) |
+----------------+                   +-------------+                     +---------------------+
        |                                 ^                                        ^
        |                                 |                                        |
        |                                 |                                        |
        |      (in .gitignore)            |                                        |
        +-----------------------------> [Ignored] <--------------------------------+
```

---

*These steps help you start a new Git project, track files, ignore unwanted files, and understand the basic workflow!*
