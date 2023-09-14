+++
author = "Vladimir Likhanov"
title = "Setting up Hugo"
date = "2022-09-27"
description = "Static site generators"
featured = true
tags = [
    "Hugo"
]
categories = [
    "Static Site Generators",
]
thumbnail = "images/blog/hugo-bg.png"
+++

> This post describes the procedure of setting up Hugo, one of the most popular open-source static site generators, on Ubuntu. You will learn how to install Hugo on your local machine, create a new Hugo site, store this site in a Git local repository, and finally put it up on GitHub.

*UPD: 27 September, 2022*

## Installing Hugo

The easiest way to install Hugo on Ubuntu is to use the *snap* package manager.

1. First, check the availability of the **Hugo** installation package in the Snap Store.

        $ snap find hugo
        Name            Version  Publisher     Notes  Summary
        hugo            0.80.0   hugo-authors  -      A Fast and Flexible Static Site Generator...
        bissetii        1.8.0    zoralab       -      This package bissetii provides a way to inst...
        gotham          v0.13.0  gothamhq      -      An awesome and super fast Static Site Generator.
        demo-hugo-site  0.1      ryanjyoder    -      Demo Hugo Site - Snap a hugo site

2. Install the Hugo package.

        $ sudo snap install hugo

        hugo version
        Hugo Static Site Generator v0.80.0 linux/amd64 BuildDate: 2020-12-31T20:00:21Z

## Setting up a new Hugo site

Once you've installed Hugo, you can create a new site:

1. Navigate to the directory where you want to store your project. In our example, it will be stored in the */home/my-user/hugo/* directory. Make sure the directory exists or create it, if necessary.

        $ cd /home/my-user/hugo

2. Create a new site. Our site will be called *docsmatter*:

        $ hugo new site docsmatter

        Just a few more steps and you're ready to go:

        1. Download a theme into the same-named folder.
        Choose a theme from https://themes.gohugo.io/ or
        create your own with the "hugo new theme <THEMENAME>" command.
        2. Perhaps you want to add some content. You can add single files
        with "hugo new <SECTIONNAME>\<FILENAME>.<FORMAT>".
        3. Start the built-in live server via "hugo server".

        Visit https://gohugo.io/ for quickstart guide and full documentation.


## Setting up Git

To perform the next steps, we'll need Git. Git is likely already installed on your Ubuntu machine. You can confirm this by running the following command:

    $ git --version
    git version 2.25.1

If this is not the case - that is, the output does now show any Git version number - you can install it with the *apt* package manager.

1. Run this command to update the local database of available packages:

        $ sudo apt update

2. Install the Git package:

        $ sudo apt install git

## Creating a Git repository

Now we need to create a local Git repository to be able to add a theme to our Hugo site in the next step:

1. Open the terminal and go to the *docsmatter* directory.

2. Run the following command:

        $ git init

        Initialized empty Git repository in /home/my-user/hugo/docsmatter/.git/

3. Check the repository status.

        $ git status
        On branch master

        No commits yet

        Untracked files:
        (use "git add <file>..." to include in what will be committed)
                archetypes/
                config.toml

        nothing added to commit but untracked files present (use "git add" to track)

## Adding a theme to the site

The Hugo website we created before has the following structure:

    └── docsmatter
        ├── archetypes
        │   └── default.md
        ├── config.toml
        ├── content
        ├── data
        ├── layouts
        ├── static
        └── themes

But none of the directories has currently any content. The easiest way to add content to your site is to download a Hugo theme and change it to meet your needs.

In our example, we'll use the [Bigspring Light](https://github.com/gethugothemes/bigspring-light) theme. You can use this theme or visit [https://themes.gohugo.io/](https://themes.gohugo.io/) and choose another one.

> **_NOTE:_**  Depending on the chosen theme, you may need to install some additional components on your system to make the theme work.

1. In the terminal, make sure that your working directory is *docsmatter*.

2. Run the following command to download the Bigspring Light theme from GitHub to the */docsmatter/themes/bigspring* directory on your local computer:

        $ git clone https://github.com/gethugothemes/bigspring-light.git themes/bigspring-light

3. Change to the */docsmatter/themes/bigspring/exampleSite* directory:

        $ cd /docsmatter/themes/bigspring/exampleSite

4. Start the Hugo webserver to build and serve the example site shipped with the Bigspring theme:

        $ hugo server --themesDir ../..
        Start building sites …
        ...

5. Open your favourite browser, enter [http://localhost:1313/bigspring-light/examplesite/](http://localhost:1313/bigspring-light/examplesite/), and click Enter. You should see the Bigspring example site in your browser.

![Hugo example website](/images/blog/hugo-example-site.png)

<br />If your browser window looks like the one above, you have successfully set up Hugo on your local computer. You can now customize the downloaded theme to meet
your needs and release it to the public.