You should learn Git like this:

> **Folder → Git → Save → GitHub**

Here's a much simpler version.

# Git & GitHub — Super Easy Beginner Guide

Imagine you have a **school notebook**.

You write something today.

Tomorrow you change it.

You want to remember what you wrote yesterday.

**Git does this for your computer files.**

**GitHub is like an online cupboard where you keep your Git project.**

---

# 1. Git vs GitHub

Think:

```text
Git      = Notebook history 📓
GitHub   = Online cupboard ☁️
```

Git is on your computer.

GitHub is on the internet.

```text
YOUR COMPUTER
     │
     │ Git
     ↓
YOUR PROJECT
     │
     │ git push
     ↓
GITHUB
```

---

# 2. First: Check Git

Open **Git Bash**.

Run:

```bash
git --version
```

If you get something like:

```text
git version 2.x.x
```

Git is installed.

---

# 3. Tell Git Your Name

Do this only once:

```bash
git config --global user.name "Gowtham"
```

Tell Git your email:

```bash
git config --global user.email "your-email@example.com"
```

Check:

```bash
git config --global user.name
git config --global user.email
```

---

# 4. Create a Project

Suppose you want a project called:

```text
my-project
```

Create it:

```bash
mkdir my-project
```

Go inside:

```bash
cd my-project
```

---

# 5. Tell Git: "Watch This Folder"

Run:

```bash
git init
```

Now Git starts watching your project.

Think:

```text
Before:

my-project
   ↓
Normal folder


After:

my-project
   ↓
Git is watching 👀
```

---

# 6. Create a File

Create:

```bash
touch index.html
```

Check:

```bash
ls
```

You should see:

```text
index.html
```

---

# 7. Check What Git Sees

Run:

```bash
git status
```

Git may say:

```text
Untracked files:
    index.html
```

What does **untracked** mean?

Simple:

> "Gowtham, I can see this file, but I am not tracking it yet."

---

# 8. Tell Git to Track the File

Run:

```bash
git add index.html
```

Now Git says:

> "Okay, I will include this file in my next save."

Check:

```bash
git status
```

You should see:

```text
Changes to be committed:
    new file: index.html
```

---

# 9. Save the File in Git

Now create a Git save point:

```bash
git commit -m "Add index page"
```

Think:

```text
git add
   ↓
"Get this ready"


git commit
   ↓
"Save this version"
```

---

# 10. Very Important: Add vs Commit

Don't confuse these.

```text
git add
    =
"Prepare this file"


git commit
    =
"Save this version"
```

Like school homework:

```text
Homework
   ↓
Put homework in bag
   ↓
git add
   ↓
Submit homework
   ↓
git commit
```

---

# 11. Create GitHub Repository

Go to GitHub.

Create a new repository.

For example:

```text
my-project
```

GitHub gives you a repository address like:

```text
https://github.com/YOURNAME/my-project.git
```

---

# 12. Connect Your Computer to GitHub

Inside your project:

```bash
git remote add origin https://github.com/YOURNAME/my-project.git
```

`origin` simply means:

> "This is my GitHub repository."

Check:

```bash
git remote -v
```

---

# 13. Send Your Project to GitHub

First make sure your branch is called `main`:

```bash
git branch -M main
```

Then:

```bash
git push -u origin main
```

Now your project goes:

```text
YOUR COMPUTER
     │
     │ git push
     ↓
   GITHUB
```

---

# 14. Your First Complete Git → GitHub Flow

Memorize this:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin GITHUB_URL
git push -u origin main
```

That's it.

---

# 15. What Does `git add .` Mean?

You will frequently see:

```bash
git add .
```

The `.` means:

> "Add everything in this folder."

Instead of:

```bash
git add index.html
git add style.css
```

you can do:

```bash
git add .
```

---

# 16. After Your First Push

This is the important part.

Tomorrow you change your project.

For example:

```text
index.html
style.css
script.js
```

You modify something.

Then use:

```bash
git status
```

See what changed.

Then:

```bash
git add .
```

Prepare everything.

Then:

```bash
git commit -m "Update website"
```

Save the new version.

Then:

```bash
git push
```

Send it to GitHub.

So your normal daily workflow is:

```text
CHANGE
  ↓
git status
  ↓
git add .
  ↓
git commit -m "message"
  ↓
git push
```

**Memorize this.**

---

# 17. GitHub → Computer

Now imagine your project is already on GitHub.

You want to download it to your computer.

Use:

```bash
git clone https://github.com/YOURNAME/my-project.git
```

Git downloads the project.

Then enter the folder:

```bash
cd my-project
```

Check:

```bash
git status
```

That's it.

---

# 18. What is `git clone`?

Think:

```text
GITHUB
   │
   │ git clone
   ↓
YOUR COMPUTER
```

It means:

> "Give me a copy of this GitHub project."

Example:

```bash
git clone https://github.com/gowthamRCG/zepto-sql-analysis.git
```

Then:

```bash
cd zepto-sql-analysis
```

---

# 19. After Clone

Suppose you cloned:

```text
zepto-sql-analysis
```

Go inside:

```bash
cd zepto-sql-analysis
```

Check files:

```bash
ls
```

Check Git:

```bash
git status
```

Now you can edit the project.

After editing:

```bash
git add .
git commit -m "Update SQL analysis"
git push
```

---

# 20. What is `git pull`?

Imagine your friend changed the GitHub project.

Your computer still has the old version.

Run:

```bash
git pull
```

It brings the latest changes from GitHub to your computer.

Think:

```text
GITHUB
   │
   │ git pull
   ↓
YOUR COMPUTER
```

---

# 21. Push vs Pull

This is extremely important.

```text
git push
    ↓
Computer → GitHub
```

```text
git pull
    ↓
GitHub → Computer
```

Remember:

```text
PUSH = Send ↑

PULL = Get ↓
```

---

# 22. Clone vs Pull

Don't confuse these.

### `git clone`

Used when you **don't have the project yet**.

```text
GitHub
   ↓
git clone
   ↓
Computer
```

Usually done once.

### `git pull`

Used when you **already have the project**.

```text
GitHub
   ↓
git pull
   ↓
Existing project
```

Used whenever you need the latest changes.

---

# 23. What is `git status`?

This is your **best friend**.

Whenever you don't know what is happening:

```bash
git status
```

It tells you:

```text
Which branch?
Which files changed?
Which files are new?
Which files are ready to commit?
```

When confused:

> **Run `git status` first.**

Don't randomly run `reset`, `restore`, `checkout`, etc.

---

# 24. What is `git log`?

It shows your saved history.

```bash
git log --oneline
```

Example:

```text
a82f123 Update CSS
4bc912a Add HTML
1c82f91 Initial project
```

Think:

```text
Today      → Update CSS
Yesterday  → Add HTML
Monday     → Initial project
```

Git remembers these versions.

---

# 25. What is a Branch?

Imagine your main project is:

```text
main
```

You want to experiment without disturbing it.

Create:

```bash
git switch -c test
```

Now you're on:

```text
test
```

You can experiment there.

When finished, you can merge it into `main`.

For now, don't worry too much about branches. Learn the basic workflow first.

---

# 26. Basic Commands You Need First

Don't memorize 50 commands.

Learn these first:

```bash
git --version
git init
git status
git add .
git commit -m "message"
git push
git pull
git clone URL
git log --oneline
git remote -v
```

That's enough to start working with Git.

---

# 27. The Complete Picture

## Computer → GitHub

```text
Create/Edit File
      ↓
git status
      ↓
git add .
      ↓
git commit -m "message"
      ↓
git push
      ↓
GitHub
```

## GitHub → Computer

```text
GitHub
   ↓
git clone       ← First time
   ↓
Computer
```

Later:

```text
GitHub
   ↓
git pull
   ↓
Computer
```

---

# 28. One-Line Meaning of Each Command

```text
git init
→ Start Git in this folder

git status
→ What is happening?

git add .
→ Prepare my changes

git commit
→ Save my changes in Git

git push
→ Send my commits to GitHub

git pull
→ Get latest changes from GitHub

git clone
→ Download a GitHub project

git log
→ Show my Git history

git remote -v
→ Show my GitHub connection

git branch
→ Show branches
```

---

# 29. The One Workflow to Memorize

### New project

```text
git init
   ↓
git add .
   ↓
git commit
   ↓
git push
```

### Existing GitHub project

```text
git clone
   ↓
cd project
   ↓
git pull
   ↓
Edit
   ↓
git add .
   ↓
git commit
   ↓
git push
```

---

# 30. DON'T Learn These Yet

If you're still learning the basics, don't jump into these immediately:

```text
git rebase
git cherry-pick
git reflog
git reset --hard
git revert
git stash
git bisect
```

They are useful, but learning them now will just create confusion.

First become comfortable with:

```text
clone
status
add
commit
push
pull
log
branch
switch
merge
```

---

# FINAL MEMORY TRICK

Remember this:

```text
                 GITHUB
                ↕      ↕
             PUSH ↑    ↓ PULL
                ↕      ↕
          LOCAL GIT REPOSITORY
                  ↑
               COMMIT
                  ↑
                 ADD
                  ↑
              YOUR FILES
```

Or even simpler:

```text
I CHANGE
   ↓
I CHECK
   ↓
I ADD
   ↓
I COMMIT
   ↓
I PUSH
   ↓
GITHUB
```

And:

```text
I WANT GITHUB PROJECT
        ↓
      CLONE
        ↓
     COMPUTER
```

**If you remember only 7 commands, remember these:**

```bash
git clone
git status
git add .
git commit -m "message"
git push
git pull
git log --oneline
```

Master these before touching advanced Git commands.
