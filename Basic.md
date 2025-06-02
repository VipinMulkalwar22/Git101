# Git Basics and Installation Guide

## 1. Git History

**What is Git?**  
Git is a tool that helps you track changes in your files and collaborate with others. It is widely used for managing source code and project files.

**Why use Git?**  
- To keep a history of changes
- To collaborate with others without conflicts
- To restore previous versions if needed

---

## 2. Installing Git

**Step 1:** Identify your operating system (Windows, macOS, or Linux).

**Step 2:** Follow the official installation guide:  
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

**Tip:** On Linux, use `sudo` to get the necessary permissions for installation.

---

## 3. Checking Your Git Installation

After installing, check the version of Git to confirm it is installed correctly:

```
git --version
```

---

## 4. Getting Help in Git

You can get help for any Git command by typing:

```
git help
```

Or for a specific command, use:

```
git help <command>
```

For example, to get help about the `init` command:

```
git help init
```

This will show you the manual page for that command, including usage, options, and examples.

To access detailed manual pages, you may need to install them first:

```
sudo apt-get install git-man
```

---

## 5. Common Git Commands Used in Various Situations

Below is a quick reference for common Git commands, similar to what you might see in a `man` page:

| Command                        | Description                                      |
|--------------------------------|--------------------------------------------------|
| `git clone <repository-url>`   | Clone a repository into a new directory          |
| `git init`                     | Create a new Git repository                      |
| `git add <file>`               | Add file contents to the index                   |
| `git mv <old> <new>`           | Move or rename a file, directory, or symlink     |
| `git restore <file>`           | Restore working tree files                       |
| `git rm <file>`                | Remove files from the working tree and index     |
| `git log`                      | Show commit logs                                 |
| `git diff`                     | Show changes between commits, or working tree    |
| `git status`                   | Show the working tree status                     |
| `git show`                     | Show various types of objects                    |
| `git branch`                   | List, create, or delete branches                 |
| `git commit -m "message"`      | Record changes to the repository                 |
| `git merge <branch>`           | Join two or more development histories together  |
| `git rebase <branch>`          | Reapply commits on top of another base tip       |
| `git reset --hard <commit>`    | Reset current HEAD to the specified state        |
| `git switch <branch>`          | Switch branches                                  |
| `git tag`                      | Create, list, delete or verify tags              |
| `git fetch`                    | Download objects and refs from another repository|
| `git pull`                     | Fetch from and integrate with another repository |
| `git push`                     | Update remote refs along with associated objects |

---

## 6. Bare vs Normal Git Repository

- **Normal Repository:**  
  Created with `git init`. Contains both your files and the Git history. Used for day-to-day work.

- **Bare Repository:**  
  Created with `git init --bare`. Contains only the Git history, not your working files. Used as a central repository for sharing (for example, on a server).

**Difference:**  
A normal repo is for working and editing files. A bare repo is for sharing and collaboration, not for editing files directly.

---

*This guide covers the basics of Git history, installation, checking your setup, getting help, and understanding the difference between normal and bare repositories.*