### **Repository (Repo)**

- A **repository** is like a **project folder** that Git tracks.
- It contains all your files, plus a hidden `.git` folder where Git keeps history.
- Repositories can be:
    - **Local** → on your computer.
        
    - **Remote** → hosted on platforms like GitHub.
👉 Example:

```shell
git init   # creates a new local repo in the current folder
```

---

### **2. The Three Git Areas**

Git manages your project in **three main areas**:

1. **Working Directory**
	- The actual files/folders you see and edit.
	- Example: `index.html`, `style.css` on your computer.

1. **Staging Area (Index)**
	- A “waiting room” for changes you want to commit.
	- You add files here using :
```shell
git add
```

3. **Commit History (Repository)**
	- A permanent record of your project’s changes.
	- You save changes here using `git commit`.


👉 Flow: **Working Directory → Staging Area → Commit History**

---

### **4. File States in Git**

Every file in a Git repo is always in one of these states:

1. **Untracked** → New files not tracked by Git yet.
- Example: You just created `notes.txt`.
- Command to track it:
- `git add notes.txt`

2. **Modified** → File changed in working directory but not staged yet.

- Example: You edited `index.html`.
- Command to stage it:
```shell
git add index.html
```

3. **Staged** → File is marked for the next commit.

- Example: After running `git add`.  
- Command to commit: 
```shell
git commit -m "Add index.html"
```

4. **Committed** → File is safely stored in history.
- It’s now part of the permanent repo.

👉 Command to check file states:

```shell
git status
```

---

### **5. Key Terms

- **Repo** = Project folder + Git history.
- **Working Directory** = Your live files.
- **Staging Area** = Pre-commit “waiting list.”
- **Commit** = Snapshot of your project at a point in time.
- **Untracked/Modified/Staged/Committed** = File states in Git.