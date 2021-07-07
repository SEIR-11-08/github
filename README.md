<img src="https://i.imgur.com/ce7PitU.png">

# Intro to Git

## Learning Objectives

| Student will be able to: |
|---|
| Describe what a Version Control System is |
| Describe the difference between Git and GitHub |
| Distinguish between local and remote repositories |
| Fork & clone repos to your computer |
| Use basic git commands to save work to the fork of a repo | 

## What is version control, and why should you care?

A Version Control System (VCS) records changes to files over time so that you can recall specific versions later.

It also makes working in teams easier, because it enables developers to submit changes to be merged into the codebase.

More specifically, a VCS allows you to:

- Revert files back to a previous state
- Review changes made over time
- Collaborate on a set of files with others
- Create separate "branches" of the codebase to develop new features on without impacting the "master", or production, branch.

In SEI, we'll be using the world's most popular version control system - [git](https://git-scm.com/).

Git was created by [Linus Torvolds](https://en.wikipedia.org/wiki/Linus_Torvalds) in 2005 to help with the development of his main project at the time - developing Linux.

## Git vs. GitHub

GitHub is not the same as git. **GitHub** is a social network built around git. It has completely changed the way we, as programmers, share and work on code. GitHub is now the largest online storage space of collaborative works, and it works with git in order to keep track of versions, issues, and requests for changes.

GitHub also plays the important role of a cloud-based backup system - a safe place for all your work!  Your code, and the time you spent writing it, is valuable, therefore, you don't want to risk losing it to hardware failure, etc. So we "connect" our local git repo to a "remote" repo on GitHub where we can then "push" code to, and "pull" code from - on demand.

In summary:

- Git provides us with local repositories on our computers
- GitHub provides us with remote repositories stored in the cloud
- A local repository is "linked" to a remote repository by adding a "remote" with this command `$ git remote add <name of remote> <URL of repo on GitHub>`

## Saving Your Work on Exercises, Labs, etc.

You will want to save work that you've completed during code alongs, labs, etc.

In fact, you may not be able to pull changes added to the class repo by your instructors until you save your work/changes by committing them like we saw earlier:

```sh
$ git add -A
$ git commit -m "Add amazing work..."
```

## Fork & Clone the Daily Code Challenges Repo

Let's now get some practice with how we will be submitting our deliverable assignments.

This guide will walk you through the steps of forking, cloning, and making a pull request to submit your work.
https://github.com/SEIR-7-06/deliverable-submissions

We'll use the Daily Js Code Challenges repo to practice the deliverable submission process. Go ahead and follow the above guide to make a pull request for the [Daily JS Code Challenge repo](https://github.com/SEIR-7-06/daily-js-code-challenges).

## Summary of Common Git Commands

By following along today and having done the pre-work, you should now be familiar with basic git commands.

In SEI, you'll get plenty of practice using git, especially during project week because each of your projects will be stored in its own directory and will be made a git repository in that directory tracking the changes.

> IMPORTANT: At some point, you will lose access to the class repo that's hosted on GA's GitHub Enterprise account. Not to worry.  You will of course have all of the materials and your work stored locally. Additionally, at the end of the cohort, you can simply add a new remote that links a repo on your personal GitHub account and push to it - that remote repo will then contain all materials and commits for your labs, practice exercises, code challenges, etc.

For your convenience, there is a git command cheatsheet located in the `resources` section of the class repo. However the following summary of commands will "git" you far:

| Command | Purpose |
|---------------------------------|---|
| `git init` | Initializes a local repository and adds a hidden `.git` directory responsible for holding repo-related data. If you've cloned your repo down from github you will already have a `.git` directory in your project and do not need to run `git init`. |
| `git status` | Checks and reports on the status of your repo. It will inform you what changes to tracked (staged) files will be included in next commit, if there are any untracked files that have been added to the project or have changes, etc. |
| `git add -A`| Adds all changes within the repo to the staging are for next commit. |
| `git commit -m "<message>"`| Commits all staged changes to the local repo. The message should be in worded such that it describes what the commit **does**, not what it **did**. For example, "Style nav bar" instead of "Styled nav bar".|
| `git remote add origin <git-url>` | Connects your local repo to a repo you've created in Github. This will add a remote called origin that you can push your code to with the next command. |
| `git push origin <branch-name>` | Pushes code in your local repo to your origin romote. Often your main branch will be called master or main. |

This following diagrams the flow of making changes to a repo:
 
<img src="https://i.imgur.com/MGQoFYo.png">

This is the basic git/GH workflow.  Things get a bit more complex when you start sharing code and manage larger codebases.

> IMPORTANT: Do not create a repo within an existing repo!  If you find your computer very sluggish, it might be because you have "nested" repos. It's not uncommon for students to accidentally make their home folder (`~`) a repo - so start there if you suspect something is wrong.



