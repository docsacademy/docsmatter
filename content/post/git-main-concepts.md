+++
author = "Vladimir Likhanov"
title = "Working with Git - basics"
date = "2022-04-18"
description = "Git"
featured = true
draft = false
tags = [
    "Git"
]
categories = [
    "Git"
]
thumbnail = "images/blog/git/git-logo.png"
+++

> This post introduces the basic operations you usually perform when working with Git: initializing a Git repository,
adding a new file to it, staging the file, and committing your changes to your local repository.

Listed below are the main steps you usually perform when working with Git:

1. You [create a new file](#creating-file) or modify an existing one in the Git working directory.

2. You [add the new or modified file](#staging-file) to the Git staging area. The staging area is where you prepare your files
for committing to the local repository.

3. You [commit the new / modified file](#committing-file) to the Git local repository. By performing a commit to your local
repository, you save the current state of your files.

4. You [push your local changes](#pushing-changes) to a remote repository. For example, this can be a GitHub, GitLab, or BitBucket
repository.

## Checking prerequisites

Before we get started, let's quickly discuss what you'll need to follow along with the steps described in this article. We
assume the following:

* You've just started working on your new website.

* You've decided to use Git for tracking your website content.

* You've created a new folder - **my-website** - that will store all website-related files.

* You've installed and configured Git on your local computer. If you have not, refer to [Setting up Git](/post/git-introduction)
to learn how you can set up Git on your local machine.

* If you are on a Windows computer, you use Git Bash to work with Git and perform Git-related commands. Git Bash allows you to
interact with Git like you would on a Linux or Mac terminal.

## <a name="creating-file"></a>Adding a file to the Git local repository

We'll start with creating (initializing) a new Git repository on our computer and adding a new file to it.

1. Change to the **my-website** folder. This folder will be our Git working directory and contain the
files you'll be working on.

        ~> cd 'C:\my-website'

2. Initialize the repository:

        ~> git init
        Initialized empty Git repository in C:/my-website/.git/

Now you can create your first file - **index.html** - and add it to your local repository.

1. Open your favorite text editor (e.g., [Visual Studio Code](/post/ubuntu-installing-visual-studio-code/)).

2. Create a new file.

3. Add the following text to it:

        <!DOCTYPE html>
        <html lang="en">
                <head>
                        <meta charset="UTF-8">
                        <meta http-equiv="X-UA-Compatible" content="IE=edge">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <title>Start page</title>
                        <link href="./resources/css/main.css" rel="stylesheet" type="text/css">
                </head>
                <body>
                        <p>My start page</p>
                </body>
        </html>

4. Save the file as **index.html**.

## <a name="staging-file"></a>Staging files

First, let’s check the status of our Git project:

        ~ git status
        On branch main

        No commits yet

        Untracked files:
        (use "git add <file>..." to include in what will be committed)
                index.html

        nothing added to commit but untracked files present (use "git add" to track)

You can see that the **Untracked files** section contains the information about the **index.html** file.
That means that Git sees the file, but it has not started tracking changes yet.

Let's change this situation and make Git start tracking your **index.html** file. To do this, we need to add this file to the
Git staging area:

        ~ git add index.html

> If you are adding several files, separate them by spaces. To add all untracked files at once, use the **--all** option
(**git add --all**).

The **git add** command produces no output. So, to make sure that the file has been successfully added to the staging area, check the
repository status again:

        ~ git status
        On branch main

        No commits yet

        Changes to be committed:
        (use "git rm --cached <file>..." to unstage)
                new file:   index.html

You should see that Git has added our file to the staging area and that this file can now be committed to your Git repository.

## <a name="committing-file"></a>Committing files

A commit is the next step in our Git workflow. The commit saves the changes from the staging area to your local repository.

When making a commit, you need to specify the commit message using the **-m** option. As a rule, the commit message contains a brief
description of your changes.

Now let’s make our first commit:

        ~ git commit -m “Add index.html to our website”
        [main (root-commit) e2ffec2] Add index.html to our website
        1 file changed, 13 insertions(+)
        create mode 100644 index.html

## <a name="pushing-changes"></a>Pushing changes to a remote repository

Once you've added the **index.html** file to your local Git repository, you may wish to place this repository in a shared location,
like GitHub, BitBucket, or GitLab. This remote repository can then serve as both a backup and a place where you can collaborate with
others on your website.

The process of setting up a remote repository depends on the chosen platform (GitHub, BitBucket, GitLab, etc.). After configuring
your remote repository, you can use the **git push** command to update the remote repository with your local commit.