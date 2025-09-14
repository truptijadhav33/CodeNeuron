### **1. What is a Remote Repository?**

- A **remote repository** is a version of your project hosted on the internet (e.g., GitHub).
- Benefits:
    - Backup in the cloud.
    - Share with teammates.
    - Collaborate with open source.

👉 A Git project can have **multiple remotes**, but usually `origin` is the default.

### **2. Creating a New Repo on GitHub**

1. Log in to [GitHub](https://github.com).
2. Click **New Repository**.
3. Choose:
    - Repo name.
    - Public or private.
    - Add README (optional).
4. Click **Create repository**.

### **3. Connecting Local Repo with GitHub**

Suppose you created a local repo already. Link it to GitHub:

`git remote add origin https://github.com/username/repo.git`

- `origin` = nickname for your remote.
- Verify remotes:

`git remote -v`

### **4. Pushing Changes to GitHub**

- Push local commits to GitHub:
`git push -u origin main`

- The first push uses `-u` (sets upstream), so next time you can just do:

`git push`

### **5. Pulling Updates from GitHub**

If teammates updated the repo, you need to fetch their changes.

`git pull`

- Downloads and merges updates from GitHub into your local branch.

### **6. Fetch**

- Downloads new data (commits, branches, tags) from a remote repository **without changing your working files or current branch**.

#### **Fetch vs. Pull**

- `git fetch` → Downloads changes from GitHub, but doesn’t apply them.
- `git pull` → Does `fetch` + then automatically merges (or rebases) into your current branch.

👉 Think of `git fetch` as _“Check what’s new on GitHub”_ and `git pull` as _“Bring the new stuff into my branch right now.”_
### **7. Cloning a Repo from GitHub**

Instead of starting locally, you can copy a project from GitHub.

`git clone https://github.com/username/repo.git`

- Creates a folder with all files + commit history.
- Automatically sets `origin` to that GitHub repo.

### **8. Working with Multiple Remotes**

Sometimes, you may want to connect to more than one remote (e.g., GitHub + GitLab).

`git remote add upstream https://github.com/original/repo.git git fetch upstream`

- `origin` = your fork.
- `upstream` = the original project.