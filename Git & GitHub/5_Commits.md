### **What is a Commit?**

- A **commit** is like a **snapshot** of your project at a given time.
- Each commit has:
    - A unique **hash ID** (like a fingerprint).
    - A **message** describing the change.
    - Metadata (author, date, time).
👉 Commits build the history of your project.

### **2. Staging Files (`git add`)**

Before committing, you need to move files into the **staging area**.

**Examples:**

```shell
git add index.html        # stage one file 
git add .                 # stage everything in the folder 
git add *.css             # stage all CSS files
```

👉 Files must be staged **before** they can be committed.


### **3. Making a Commit (`git commit`)**

Once staged, you can save a snapshot with a commit.
**Example:**

```shell
git commit -m "Add homepage with index.html"
```

- `-m` lets you write a message inline.
- Messages should be **short and clear**.

### **4. Writing Good Commit Messages**

Bad commit:
`git commit -m "fixed stuff"`

Good commit:
`git commit -m "Fix navbar alignment issue on homepage"`

👉 Best practice:
- Use present tense: “Add feature” (not “Added feature”).
- Keep messages short (50 chars max in summary).
- Optionally add a longer description if needed.

### **5. Viewing History (`git log`)**

To see all past commits:
`git log`
Shows commit hash, author, date, and message.

👉 Short version:
`git log --oneline`
Example output:
`a1c2d3e Add navbar f4g5h6i Initial commit`

### **6. Amending a Commit**

If you forgot something in your last commit:
`git commit --amend`
- Lets you add staged changes to the previous commit.
- Or edit the commit message.

### **7. Undoing Changes**

Sometimes mistakes happen!
- **Unstage a file** (remove from staging area):
`git restore --staged file.txt`

- **Discard changes in working directory**:
`git restore file.txt`

- **Go back to a previous commit (dangerous)**:
`git reset --hard <commit_hash>`

👉 Use carefully, especially if working with others.

### **8. Checking What Changed**

See line-by-line changes:

```
git diff  # unstaged changes 
git diff --staged  # staged changes
```
