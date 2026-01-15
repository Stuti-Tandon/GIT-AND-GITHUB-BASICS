# Git Workflow – Commands & Definitions

## 1. Creating a Local Repository

### Commands
a. Create project directory:
```bash
mkdir devops
```

b. Move into directory:
```bash
cd devops
```

c. Initialize git repository:
```bash
git init
```

### Definition
**git init** creates a new blank repository or makes an existing project a git project. It creates a `.git` folder storing metadata and HEAD.

---

## 2. Configure Username & Email

### Commands
a. Set username:
```bash
git config user.name "full_name"
```

b. Set email:
```bash
git config user.email "email_id"
```

---

## 3. Create & Edit a File

### Commands
a. Create empty file:
```bash
touch helloworld.py
```

b. Add text into file:
```bash
echo 'print("Hello World")' > helloworld.py
```

c. Display file contents:
```bash
cat helloworld.py
```

d. Edit using nano:
```bash
nano helloworld.py
```

e. Edit using vi:
```bash
vi helloworld.py
```

### Definitions
- **touch** creates an empty file.
- **echo** outputs text; using `>` writes text into a file.
- **nano / vi** are text editors to modify file contents.

### vi Usage Notes
Inside vi:
```
i      # insert mode
Esc    # exit insert
:wq    # save and quit
```

---

## 4. Commit Changes

### Commands
a. Add file to staging:
```bash
git add helloworld.py
```

b. Commit staged changes:
```bash
git commit -m "First commit"
```

### Definitions
- **Add** moves modified files to staging using `git add`.
- **Commit** snapshots changes to repository using `git commit -m <msg>`.

---

## 5. Branching

### Commands
a. Create branch:
```bash
git branch feature_a
```

b. Switch to branch:
```bash
git checkout feature_a
```

c. Create and switch combined:
```bash
git checkout -b feature_a
```

### Definition
A **branch** isolates development so work doesn’t affect main code.  
`checkout` switches between branches.

---

## 6. Modify File in Branch

### Commands
a. Edit file again:
```bash
vi helloworld.py
```
(add data → `Esc` → `:wq`)

b. Check file state:
```bash
git status
```

---

## 7. Merging Branches

### Commands
a. Switch to master/main:
```bash
git checkout master
```

b. Merge feature branch:
```bash
git merge feature_a
```

### Definition
**merge** integrates changes from one branch into another. Conflicts may require manual resolution.

---

## 8. Add Remote Repository (SSH)

### Commands
a. Add remote origin:
```bash
git remote add origin git@github.com:<your-github-username>/<repository-name>.git
```

### Definition
A **remote** connects local repo to a repository hosted externally (e.g., GitHub).  
SSH URL enables push without HTTPS credentials.

---

## 9. Clone Remote Repository

### Commands
a. Clone public repo:
```bash
git clone https://github.com/singh-ashok25/webserver.git
```

---

## 10. Additional Terminology

1. **.git Directory**  
Hidden directory storing repository metadata and history.

2. **Working Directory**  
Project files currently being modified.

3. **Staging Area**  
Intermediate layer between working directory and commit.

---

End of Notes.
