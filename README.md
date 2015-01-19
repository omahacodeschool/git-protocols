# Git Protocols

## Creating a new repository

- What assignment or project is this repository for? If you don't know the answer, you're not ready to create a repository yet.
- Where on your machine is this project going to live?
- Where is your current working directory?

Answers to the above questions are necessary before you can move on.

The below protocol contains re-usable steps for making a new Git repository. The actual commands can be copy/pasted without much difficulty (and with minor adjustments for your task's particulars).

For the purposes of the protocol, we're using a make-believe project called "My Blog".

1. Change the working directory to **~/Code**.
  - `cd ~/Code`
    - At this point, check your command-line prompt. You should **not** be in a Git repository already. Running `git status` should return something like, "Not a git repository". If your working directory is somehow a repository already, a couple things might be the cause:
      - Maybe the current working directory isn't actually **~/Code**.
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