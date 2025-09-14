### **Collaboration**

- Collaboration in GitHub means **working together on the same repository**.
- Usually, you’re **added as a collaborator** (via repo settings) or part of an **organization/team**.
- You have **direct access** to the repository:
    - Can clone it.
    - Create branches.
    - Push commits directly.
    - Open and merge Pull Requests inside the same repo.

👉 Common in **private/team projects** where all members are trusted.

---
### **1. Forking a Repository**

- **Fork** = make a copy of someone else’s GitHub repo under your account.
- Purpose:
    - Experiment without affecting the original.
    - Contribute to open source projects.
- Steps:
    1. Go to the repo on GitHub.
    2. Click **Fork**.
    3. A copy appears in your GitHub account.

---

### **2. Creating Pull Requests (PRs)**

When you make changes in your fork and want them in the original repo:

1. Create a new branch in your fork:
	
    `git checkout -b feature-xyz`
    
2. Make changes, commit, and push:
    
    `git push origin feature-xyz`
    
3. On GitHub, click **Compare & pull request**.
    
4. Add description, explain what you changed, and submit.

---

### **3. GitHub Issues & Discussions**

- **Issues**: Used for bug reports, feature requests, or tasks.
    - Can be assigned to team members.
    - Can have labels (`bug`, `enhancement`, etc.).
- **Discussions**: Used for open-ended conversations (not tied to code).

---

### **4. Merging Pull Requests**

Once approved:
- Maintainer can merge via GitHub UI.
- Merge options:
    - **Merge commit** → keeps full history.
    - **Squash & merge** → combines all commits into one.
    - **Rebase & merge** → replays commits on top of main.

---

### **8. Collaboration Workflow Example**

1. Alice forks repo, clones it, creates `feature-branch`.
2. Alice commits changes and pushes to her fork.
3. Alice opens a Pull Request to the original repo.
4. Bob (maintainer) reviews, requests a small fix.
5. Alice updates her branch, pushes again → PR auto-updates.
6. Bob approves & merges the PR (PULL Request).

## Difference Between Collaboration and Forking

| **Aspect**         | **Collaboration**                               | **Forking**                              |
| ------------------ | ----------------------------------------------- | ---------------------------------------- |
| **Access**         | Direct access to repo                           | No direct access to original repo        |
| **Use Case**       | Team projects, private repos                    | Open-source contributions, experimenting |
| **Where you push** | Directly to the repo (shared)                   | To your own fork (copy)                  |
| **Pull Requests**  | Open PRs within the same repo                   | Open PRs from your fork → original repo  |
| **Setup**          | Owner must add you as collaborator              | Anyone can fork without permission       |
| **Example**        | You & friends build an app together in one repo | You fork React repo to suggest a bugfix  |

- **Collaboration** = Working together in the same Google Doc.

- **Forking** = Making a copy of someone’s Google Doc, editing your copy, and then suggesting your changes back.