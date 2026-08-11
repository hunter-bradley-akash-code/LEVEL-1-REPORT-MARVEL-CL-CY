# TASK 1: Working with Git and GitHub
- - -

In this task I learned the basics of **Git and GitHub** and how they are used to track changes, manage different versions of a project and collaborate with other developers.

I started with a simple Python calculator and used Git to maintain its development history. I created separate commits while adding operations such as modulus and power and learned how each change is recorded in Git.

## Git Basics

I practiced commonly used Git commands for managing a project.

| Command | Purpose |
|---|---|
| `git init` | Creates a new Git repository |
| `git add` | Stages changes |
| `git commit` | Saves changes to Git history |
| `git status` | Shows the current repository status |
| `git log` | Displays commit history |
| `git branch` | Creates or lists branches |
| `git checkout` | Switches between branches |
| `git push` | Uploads changes to GitHub |
| `git clone` | Downloads a repository |

## Images

![Git commit history](git_log.jpg)

- - -

## Git Revert and Cherry-Pick

I learned how to undo and restore specific changes using `git revert` and `git cherry-pick`.

First, I used `git revert` to undo the **power operation** that had been added to the calculator. Git created a new commit to reverse the previous changes instead of deleting the original commit.

After that, I used `git cherry-pick` to bring the original power-operation commit back into the current branch.

```bash
git revert <commit-id>
git cherry-pick e9e546c
