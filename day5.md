Great question! Here's a clear explanation of the **`git restore`** and **`git switch`** commands, and how to **get the version of a file from a particular commit** using them — perfect for interviews and real-world Git use.

---

## ✅ **1. `git switch` – For Branch Management**

### 🔹 Purpose:

`git switch` is a simpler, safer alternative to `git checkout` when changing branches.

### 📌 Common Uses:

* **Switch to a branch**:

  ```bash
  git switch main
  ```

* **Create and switch to a new branch**:

  ```bash
  git switch -c feature/new-login
  ```

> 🧠 Interview Tip:
> "`git switch` focuses only on branches — it's more intuitive and less risky than `checkout`."

---

## ✅ **2. `git restore` – For File & Content Restoration**

### 🔹 Purpose:

`git restore` restores file contents from commits, the index (staging area), or discards changes.

---

### 📌 To Get the Version of a File from a Particular Commit:

Use this command:

```bash
git restore --source=<commit-hash> <file-name>
```

🔧 **Example:**

```bash
git restore --source=abc123 src/app.js
```

> This restores the version of `src/app.js` from commit `abc123` into your working directory **without switching branches**.

---

### 📌 Other Useful `git restore` Options:

* **Discard uncommitted changes to a file**:

  ```bash
  git restore <file>
  ```

* **Unstage a file (keep changes in working dir)**:

  ```bash
  git restore --staged <file>
  ```

---

## ✅ Summary Table

| Task                                | Command                              |
| ----------------------------------- | ------------------------------------ |
| Switch to a branch                  | `git switch branch-name`             |
| Create and switch to a new branch   | `git switch -c new-branch`           |
| Restore file from a specific commit | `git restore --source=commit <file>` |
| Discard file changes                | `git restore <file>`                 |
| Unstage file                        | `git restore --staged <file>`        |

---

## 🧠 Interview Summary:

> "`git switch` is used to manage branches safely. `git restore` lets me recover files from previous commits or undo changes. I use `git restore --source=<commit>` to get the exact version of a file from any past commit without changing branches."

---

Would you like to see how this differs from `git checkout <commit> -- <file>`?
==================
