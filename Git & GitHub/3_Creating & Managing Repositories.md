### **1. Initializing a Repository**

A repository (repo) is where Git stores your project history.

**Steps to create one:**

```shell
mkdir myproject # create a folder
cd myproject    # move inside 
git init        # initialize git repo
```

Output:

`Initialized empty Git repository in .../myproject/.git/`
👉 Now your folder has a hidden `.git` directory that stores Git data.  
Check it with:
`ls -a`

---
### **2. Cloning an Existing Repository**

Instead of starting from scratch, you can copy a repo from GitHub (or another server).

`git clone https://github.com/username/repo.git`

- Creates a new folder with all files and history.  
- Useful when you join a project or contribute to open source.

---
### **3. Repository Structure**

Inside a Git repo, the key components are:

- `.git/` → hidden folder with all history, branches, commits.
- `working directory` → your actual project files.
- `.gitignore` → tells Git which files/folders to ignore (e.g., `node_modules/`, `.env`).

---
### **4. Using `.gitignore`**

Sometimes you don’t want certain files in Git (like passwords, logs, or system files).  
You create a `.gitignore` file at the repo root.

**Example `.gitignore`:**

```shell
# Ignore system files 
.DS_Store 
Thumbs.db
# Ignore logs 
*.log  
# Ignore environment configs
.env  
# Ignore dependencies 
node_modules/
```

👉 Add `.gitignore` before committing your files.

---

### **5. Best Practices When Creating a Repo**

- Always create a `README.md` → explains your project.
- Add a `.gitignore` early.
- Use clear folder structure.
- Commit small, meaningful changes.