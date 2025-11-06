# 🧘‍♀️ Serenity Yoga Studio Website

## 🧠 Git & GitHub Collaboration Workshop

### Duration: 2.5 hours

### Scenario: *Collaborating on the “Serenity Yoga Studio” Project*

---

## 🌟 Learning Goals

By the end of this workshop, you will be able to:

1. Initialize and clone repositories.
2. Push and pull changes using GitHub.
3. Create and work on branches.
4. Open, review, and merge Pull Requests (PRs).
5. Resolve merge conflicts.
6. Use Issues and Project Boards for teamwork.
7. Tag and release a final version.

---

## 🧬 Project Setup

### Step 1 – Form Teams

* Create **teams of 2 or 3 students**.
* Decide one **Team Lead**.

### Step 2 – Create the Repository (handled by GitHub Classroom)

Each team will automatically receive a repository named similar to:

```
serenity-yoga-studio-teamX
```

(X = your assigned group number)

Your repository already includes starter files representing Serenity Yoga Studio’s website and booking system.

### Step 3 – Clone the Repo

Each teammate runs:

```bash
git clone https://github.com/<org-name>/serenity-yoga-studio-teamX.git
cd serenity-yoga-studio-teamX
```

---

## 🪜 Phase 1 – Chaos on Main (15–20 min)

**Goal:** Experience what happens when everyone edits the same branch.

1. Everyone opens `contributors.md` (create one if it doesn’t exist).
2. Add your name under a list:

   ```
   - Priya
   - Jordan
   - Amir
   ```
3. Stage, commit, and push:

   ```bash
   git add .
   git commit -m "Added my name to contributors"
   git push origin main
   ```
4. The first person’s push will succeed.
   Others will see:

   ```
   ! [rejected] main -> main (fetch first)
   ```
5. Fix by pulling and merging:

   ```bash
   git pull origin main
   # Resolve merge markers if they appear
   git add .
   git commit -m "Resolved merge conflict in contributors.md"
   git push origin main
   ```

💬 **Discussion Prompt:**
Why did we face errors? How does Git prevent accidental overwrites?

---

## 🌱 Phase 2 – Branching and Pull Requests (60 min)

**Goal:** Collaborate safely using feature branches.

### Step 1 – Create Branches

Each member makes a new branch for their assigned task:

```bash
git switch -c feature/<your-task>
```

Examples:

* `feature/add-class-schedule`
* `bugfix/fix-booking-form`
* `docs/update-readme`

### Step 2 – Make Changes

Edit different parts of the Serenity Yoga Studio website:

* Add a new class schedule section in HTML.
* Fix the “Book Now” button in JavaScript.
* Update instructor bios in README.

Commit and push:

```bash
git add .
git commit -m "Implemented class schedule section"
git push -u origin feature/add-class-schedule
```

### Step 3 – Open a Pull Request

1. Go to your repo on GitHub.
2. You’ll see a banner: **“Compare & Pull Request”** → click it.
3. Add a descriptive PR title and comment (e.g., “Added yoga class schedule section”).
4. Choose **main** as the base branch.
5. **Assign a teammate as reviewer.**

### Step 4 – Review and Merge

* Reviewer checks code, leaves comments, and **Approves**.
* Maintainer merges PR → main.
* Everyone updates their local main:

  ```bash
  git checkout main
  git pull origin main
  ```

💬 **Reflection:**
How did branching make teamwork easier?
What are good commit messages?

---

## ⚔️ Phase 3 – Merge Conflict Simulation (30 min)

**Goal:** Learn to detect and fix merge conflicts.

### Step 1 – Create the Conflict

* Everyone edits the **same line** in `index.html`.
  Example:

  ```html
  <h2>Welcome to Serenity Yoga Studio</h2>
  ```

  → each person changes the line differently.

### Step 2 – Push and Merge

* Each person commits and pushes their branch.
* When creating the PR, GitHub will show **“This branch has conflicts.”**

### Step 3 – Resolve the Conflict

In VS Code:

1. Click **Resolve Conflicts** or open the conflicted file.
2. You’ll see:

   ```
   <<<<<<< HEAD
   <h2>Welcome to Serenity Yoga Studio</h2>
   =======
   <h2>Serenity Yoga – Flow, Breathe, and Balance</h2>
   >>>>>>> feature/add-class-schedule
   ```
3. Keep the desired line (or combine both).
4. Save → stage → commit → push:

   ```bash
   git add .
   git commit -m "Resolved merge conflict in index.html"
   git push
   ```

### Step 4 – Merge and Pull

* After resolving, merge the PR.
* Everyone updates local main again.

💬 **Discussion:**
What caused the conflict?
How can teams minimize them?

---

## 🧱 Phase 4 – Issues & Project Board (20–25 min)

**Goal:** Track work visually.

### Step 1 – Create Issues

In GitHub:

1. Go to **Issues → New Issue**.
2. Write a clear title, e.g., “Fix class booking confirmation alert.”
3. Add labels (`bug`, `enhancement`, `documentation`).
4. Assign to a teammate.

### Step 2 – Create Project Board

1. Click **Projects → New Project**.
2. Choose **Board view** (To Do / In Progress / Done).
3. Add your issues to the board.
4. Move cards as you work.

💬 **Reflection:**
How do Issues and Boards help track work in real teams?

---

## 🎉 Phase 5 – Release and Wrap-Up (15 min)

1. Ensure all PRs are merged into main.
2. Tag a release:

   ```bash
   git tag -a v1.0.0 -m "Team 1 final Serenity Yoga release"
   git push origin v1.0.0
   ```
3. Update README:

   * Team members
   * What each person did
   * Lessons learned

---

## 📊 Bonus Explorations (if time)

| Topic               | Command / Location                     |
| ------------------- | -------------------------------------- |
| View commit graph   | `git log --oneline --graph --decorate` |
| Undo a bad commit   | `git revert <commit-hash>`             |
| Create .gitignore   | Add files/folders to ignore            |
| Protect main branch | Repo → Settings → Branches → Rules     |
| Add badges          | [shields.io](https://shields.io)       |
| Add CI workflow     | `.github/workflows/ci.yml`             |

---

## 🦯 Summary of Key Commands

| Action         | Command                          |
| -------------- | -------------------------------- |
| Clone a repo   | `git clone <url>`                |
| Check status   | `git status`                     |
| Stage changes  | `git add .`                      |
| Commit changes | `git commit -m "message"`        |
| Push to remote | `git push origin <branch>`       |
| Create branch  | `git switch -c <branch>`         |
| Switch branch  | `git switch <branch>`            |
| Pull latest    | `git pull origin <branch>`       |
| Merge branch   | `git merge <branch>`             |
| View branches  | `git branch -a`                  |
| Tag release    | `git tag -a v1.0.0 -m "message"` |
| Push tag       | `git push origin v1.0.0`         |

---

## 🧠 Team Roles and Responsibilities

| Role            | Description                               |
| --------------- | ----------------------------------------- |
| **Team Lead**   | Manages merges and oversees project flow. |
| **Feature Dev** | Adds new feature on a branch.             |
| **Bug Fixer**   | Fixes issues in booking or layout.        |
| **Doc Writer**  | Updates README and contributors.          |

---

## 📘 Reflection Questions (for Submission or Discussion)

1. What went wrong when everyone pushed to main?
2. How did branches and PRs solve the problem?
3. What’s the difference between `merge` and `rebase`?
4. How can conflicts be prevented in large teams?
5. Which commands did you use most often?
6. How does GitHub help track ownership and accountability?

---

## 🎥 Additional Resources

* [Video: How to Tag and Release in GitHub](https://www.youtube.com/watch?v=Ob9llA_QhQY)
* [Video: Understanding Git Tags and Releases (alternative guide)](https://www.youtube.com/watch?v=6EQN0gJL7y8)

---

## 🤏 Deliverables (to Instructor)

Each team must submit:

* GitHub repository URL
* Screenshot of merged PRs (≥ 2)
* Screenshot of one conflict resolution
* Screenshot of Issues board
* Final README with team names and Serenity Yoga release tag

