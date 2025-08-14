## When does .git get created in our project folder?
- This .git directory contains all the metadata, history, configuration, and objects that Git needs to track your project.
- The .git directory is created in your project folder when you initialize a Git repository locally.
  This happens in one of the following two ways:
  1. Using git init **git init**
     Git creates a .git directory inside that folder. Immediately in current folder
  2. Cloning an existing repository **git clone https://github.com/user/repo.git**. Immediately in the cloned folder
- You can see the .git directory using command: **ls -a**
