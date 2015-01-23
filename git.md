# Git Protocols

## Creating a new repository

- What assignment or project is this repository for? If you don't know the answer, you're not ready to create a repository yet.
- Where on your machine is this project going to live?
- What is your current working directory?

Answers to the above questions are necessary before you can move on.

The below protocol contains re-usable steps for making a new Git repository. The actual commands can be copy/pasted without much difficulty (and with minor adjustments for your task's particulars).

For the purposes of the protocol, we're using a make-believe project called "My Blog".

1. Change the working directory to **~/Code**.
  - `cd ~/Code`
    - At this point, check your command-line prompt. You should **not** be in a Git repository already. Running `git status` should return something like, "Not a git repository". If your working directory is somehow a repository already, a couple things might be the cause:
      - Maybe the current working directory isn't actually **~/Code**. Use `pwd` to verify the current path.
      - Maybe you accidentally made **~/Code** a Git repository. You need to remove the repository (There's a protocol for this).
2. Make a new folder for your project.
  - `mkdir my-blog`
3. Change the working directory to your new project's folder.
  - `cd my-blog`
4. Add a README file.
  - `echo "# My Blog" >> README.md`
5. Stage the README file and add it to the repository as its first commit.
  1. `git add README.md`
  2. `git commit -m "First commit."`
6. Now you can open the project's directory in TextMate and get to work.
  - `mate .`
  
## Making a new commit

- What assignment or project are you working on right now?
- Where on your maching does this project live?
- What is your current working directory?

There's always a chance you think you're working on "My Blog", which is in **~/Code/my-blog**; but your current working directory in Terminal is **~/Code/final-project** (or something). Validate your assumptions with `pwd` before moving on.

1. Check the status of your repository.
  - `git status`
    - Are there any surprises? **Don't move on until you understand each line of your repository's status.**
2. Stage the files containing changes (and/or any new files that relate to this commit).
  - `git add file_path_1 file_path_2`
3. Add the staged files to a commit and write a message explaining the commit.
  - `git commit`
  - In TextMate, you'll now be prompted for the commit message. Remember, a short (< 80 characters) title followed by an empty newline and then a longer description if needed. Remember that your commit messages should be such that anyone who reads them can figure out very quickly what's been done, what's in progress, and what still needs to be finished before you can say that you're done.
    - Save the file when you're finished (It's a temporary file, so you just need to do `CMD + S`. You don't need to choose where on your machine to save it to.)
    - Close that file's window. (Don't quit TextMate entirely.)
4. Verify that the commit took.
  - `git status`
    - Is the status what you're expecting?
  - `git log`
    - Do you see your latest commit message in the log?
