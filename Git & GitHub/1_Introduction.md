### **What is Version Control?**

Version control is a system that helps you **track changes to files** over time. It lets you:

- Save different versions of your project.

- Go back to previous versions if something breaks.

- Work with teammates without overwriting each other’s changes.

👉 Think of it like the **“Undo” button** for your entire project.

### **Types of Version Control Systems**

Local Version Control
	- Stores versions on your computer only.
	- Limitation: Only one person can work at a time.
Centralized Version Control (CVCS)
	- A single central server stores project history.
	- Developers pull and push changes to this central server.
	- Limitation: If the server goes down, nobody can work.
Distributed Version Control (DVCS)
	 - Every developer has a **full copy** of the project history.
	 - Even without the internet, you can commit and browse history.
	 - Example: Git, Mercurial.
	 - Stronger, faster, and safer for collaboration.

### **Why Git?**

Git is the **most popular DVCS**, created by Linus Torvalds (the creator of Linux).  
Advantages of Git:

- **Fast**: Optimized for performance.
- **Distributed**: Every copy is a full backup.
- **Branching**: Easy to create and merge feature branches.
- **Popular**: Used by millions of developers and big companies.
- **Free & Open Source**.

### **Git vs GitHub (and Others)**

- **Git**: A version control _tool_ installed on your computer.
    
    - Works offline.   
    - Manages code history and versions.
    
- **GitHub**: A _cloud platform_ that hosts Git repositories.
    
    - Makes collaboration easier.   
    - Provides Pull Requests, Issues, Wikis, Project boards, Actions (CI/CD).
       
- **Alternatives**: GitLab, Bitbucket, SourceForge.
	   - Similar purpose, different ecosystems.

👉 **Think of Git as the engine, and GitHub as the garage where you keep, share, and showcase your projects.**

### **Use Cases**

- **Solo developers**: Track your personal projects.
- **Teams**: Multiple devs can work together without overwriting work.
- **Open Source**: Contribute to global projects (Linux, React, TensorFlow, etc.).
- **Companies**: Manage large-scale enterprise projects.
- **DevOps & Deployment**: GitHub Actions automate testing and deployment.

# Installing & Setting Up Git

### **1. Installing Git**

Git needs to be installed on your system before use.

### **Configuring Git (Identity & Settings)**

After installation, configure your **name** and **email** (important for commit history).

```shell
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

`--global`: applies to all repos on your computer.
### **Check your settings:**

```shell
git config --list
```

### **Setting the Default Branch**

Traditionally, Git used `master` as the default branch, but now many platforms (like GitHub) use `main`.

Set `main` as default:

```shell 
git config --global init.defaultBranch main
```

### **Git Configuration Levels:**

- **System** (`C:\Program Files\Git\etc\gitconfig`): applies to all users.
    
- **Global** (`C:\Users\<YourName>\.gitconfig`): applies to your user account.
	-  This is the most commonly used level.
    
- **Local** (`.git/config` inside each repo): applies only to that repo.
