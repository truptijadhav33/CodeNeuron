### **1. Stashing Changes (`git stash`)**

- Sometimes you’re in the middle of editing, but need to switch branches quickly.
- `git stash` saves your changes temporarily and cleans your working directory.


**Example:**

```shell
git stash         # save changes
git stash list    # see saved stashes
git stash apply   # reapply last stash 
git stash drop    # delete a stash
```

👉 Think of it as a **clipboard for unfinished work**.

---

### **2. Tagging Releases (`git tag`)**

- Tags mark important points in history (like versions).
- Used for releases: `v1.0`, `v2.1`.

**Examples:**

```shell
git tag v1.0              # lightweight tag 
git tag -a v1.0 -m "Release version 1.0"   # annotated tag 
git show v1.0             # see details 
git push origin v1.0      # push a tag to GitHub
```

---

### **3. Viewing Differences (`git diff`)**

- Shows what has changed between commits or in the working directory.

**Examples:**

```shell
git diff            # changes not staged 
git diff --staged   # changes staged for commit 
git diff commit1 commit2   # compare two commits
```


---

### **4. Rebasing (`git rebase`)**

- **Rebasing** = moving or combining commits onto a new base branch.
- It’s an alternative to **merge**.
- Goal: keep history **linear and clean** instead of messy with merge commits.

## Example Scenario

You and your teammate are working on a project:

- `main` branch has 3 commits:

```shell 
A -- B -- C (main)
```

- You create a feature branch and add commits:

```shell
A -- B -- C (main)           
		   \   
		    D -- E (feature)
```

- Meanwhile, teammate adds more commits to `main`:

```shell
A -- B -- C -- F -- G (main)           
		   \           
		    D -- E (feature)
```

---

### **Option 1: Merge**

If you merge `main` into your branch:

```shell
A -- B -- C -- F -- G (main)           
		  \           \            
		   D -- E ----- H (feature)
```

👉 History shows a **merge commit (H)**. It works, but history looks messy.

---

### **Option 2: Rebase**

If you rebase your branch onto `main`:

```shell
git checkout feature
git rebase main
```

**`git checkout feature`**

- Switches you to the `feature` branch.
- Now your HEAD pointer is on `feature`.

`git rebase main` while on:

1. Git sees that `A -- B -- C` are already in `main`.
2. It doesn’t duplicate them — they remain part of both branches.
3. Commits `D` and `E` get **removed from feature temporarily**.
4. Git moves `feature` to the tip of `main` (after `G`).
5. Git re-applies (`replays`) `D` and `E` as **new commits** (`D'`, `E'`).
Your commits `D` and `E` are **replayed** on top of `main`:

```shell
A -- B -- C -- F -- G -- D' -- E' (feature)
```

👉 Cleaner history: looks like you built your feature after `F` and `G`.

### ⚠️ Golden Rule of Rebase

👉 **Never rebase public/shared branches.**
- Rewriting history can confuse teammates.
- Only use rebase on your **own local feature branches** before pushing.
## Merge vs Rebase

|Feature|Merge|Rebase|
|---|---|---|
|History|Shows full branching & merging|Linear, looks like one straight timeline|
|Commit IDs|Original commits preserved|New commit IDs created|
|Safe to use?|Always safe|Can be dangerous if used on **shared branches**|
|Use case|Team collaboration|Cleaning up your own local commits|
#### **In short:**
- **Merge** keeps full history,
- **Rebase** rewrites history to look cleaner,
- Use **rebase only on your own local branches**, not shared ones.
---

### **5. Cherry-Picking (`git cherry-pick`)**

- Apply a specific commit from one branch onto another.

**Example:**

`git checkout main git cherry-pick <commit_hash>`

👉 Useful if you only need one fix, not the whole branch.

---

### **6. Reset vs Revert**

- **Reset** → moves branch pointer backwards (can erase history).
    `git reset --hard <commit_hash>`

- **Revert** → creates a new commit that undoes previous changes (safe for shared repos).
    
    `git revert <commit_hash>`

👉 Rule of thumb:

- Use **reset** for local work.
- Use **revert** for published/shared work.

---

### **7. Aliases for Faster Workflow**

Typing long commands often? Create shortcuts with aliases.

**Examples:**

```shell
git config --global alias.st status 
git config --global alias.ci commit 
git config --global alias.co checkout 
git config --global alias.br branch
```

Now run:

`git st   # instead of git status git ci -m "message"`