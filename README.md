# Learning GIT and GitHub

## What is a Repository?

A **GitHub repository (repo)** is a storage space on **GitHub** where you can keep your project's files, including code, documentation, images, and more. It also tracks all changes made to those files over time, using **Git version control**.

---

## Key Points about a GitHub Repository

### 📁 Project Storage
A repository is like a folder where all your project's code and files are kept.

### 🕒 Version Control
Every change you or others make is tracked. You can view the history, revert to previous versions, or collaborate without overwriting others' work.

### 🤝 Collaboration
Multiple people can work on the same project, suggest changes (**Pull Requests**), and review code together.

### 🔒 Public or Private
Repositories can be **public** (anyone can see) or **private** (only selected people have access).

### 🔄 Clone & Fork
- **Clone**: Download the repository to your local machine to work on it.
- **Fork**: Create your own copy of someone else's repository for experimentation or personal use.

### 📝 README.md
Most repositories include a **README.md** file that explains:
- What the project is about
- How to use it
- How to contribute to it

---

# Git Configuration Levels

Git allows you to configure settings at three different levels: **System**, **Global**, and **Local**. These levels determine how settings are applied across different repositories and users on your machine.

---

## Configuration Levels Explained

### 1. System Level
- **Scope**: Applies to all users and all repositories on the system.
- **Config File**: `/etc/gitconfig`
- **Permissions**: Requires administrator/root access.

#### Example Command:
```bash
git config --system user.name "Your Name"
git config --system user.email "your.email@example.com"
```

---

### 2. Global Level
- **Scope**: Applies to your user account across all repositories.
- **Config File**: `~/.gitconfig` (Linux/macOS) or `C:\\Users\\YourName\\.gitconfig` (Windows)

#### Example Command:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

### 3. Local Level
- **Scope**: Applies only to the specific repository.
- **Config File**: `.git/config` inside the repository directory.
- **Precedence**: Overrides global and system configurations for that repository.

#### Example Command:
```bash
cd /path/to/your/repository
git config user.name "Repo Specific Name"
git config user.email "repo.specific@example.com"
```

---

## Viewing Configuration Settings

- View all configurations (in order of precedence):
```bash
git config --list
```

- View configuration at a specific level:
```bash
git config --system --list
git config --global --list
git config --local --list
```

---

## Configuration Precedence Order
When Git needs a configuration value, it looks in the following order:
1. **Local** (specific repository)
2. **Global** (user-wide)
3. **System** (machine-wide)

The closer the configuration is to the repository, the higher its priority.

---

## Example Scenario
- **System Level**: Organization-wide settings, like preferred diff/merge tools.
- **Global Level**: Your personal identity (user.name, user.email).
- **Local Level**: Repository-specific identity for work projects or open-source contributions.

---

## Summary
| Level   | Scope                             | Config File Location              |
|---------|-----------------------------------|-----------------------------------|
| System  | All users, all repositories       | `/etc/gitconfig`                  |
| Global  | Current user, all repositories    | `~/.gitconfig`                    |
| Local   | Specific repository only          | `.git/config` inside repo folder  |

---

## Helpful Commands
```bash
# View Effective Configurations
git config --list

# Edit Global Configuration File
git config --global --edit

# Edit Local Configuration File
git config --local --edit
```

---



