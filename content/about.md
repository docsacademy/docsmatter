+++
title = "About"
description = "About me, this website and used technologies"
date = "2023-04-28"
aliases = ["about-us", "about-hugo", "contact"]
author = "Vladimir Likhanov"
+++

![](/images/avatar.png)

My name is Vladimir Likhanov. I'm a translation manager, CCMS (Component Content Management Systems) administrator, and technical writer with over 18 years of professional experience in creating software documentation. I love researching new technologies, finding their best use cases, and turning them into useful information sources for end users and developers.

In my current position at a German software company, I work with the developers and QA engineers to plan and write various documentation for complex IT projects in English and German.
I’m responsible for creating and maintaining the company's online help, user and administrator manuals as well as installation guides, system requirements, release notes, and API documentation.

## About DocsMatter

The DocsMatter website provides useful resources that can help you create good technical documentation.

Here, you can find information about modern technical writing tools and approaches, including

* docs like code
* Markdown and AsciiDoc
* Git and GitHub
* Static site generators (Hugo, Gatsby, etc.)
* Documentation standards (e.g. XML and DITA)
* and so on

You will also learn about other technical documentation-related topics like translation management, localization, and video editing.

## About technologies behind this website

The Hugo static site creator is used to make this website, and Azure Static Web Apps technology is used to make it live.

The source content is created in Markdown, a lightweight markup language that can be written with any plain-text editor. As an editor, Visual Studio Code is used providing support for Markdown out of the box.

All source files are stored in a local Git repository. At regular intervals, the content is pushed to a remote repository on GitHub. To monitor the changes in the repository, Azure Static Web Apps connects with GitHub directly. GitHub Actions starts an automatic build and release process whenever commits are pushed or pull requests are accepted into this repository. 

The website includes picture assets, HTML, CSS, and JavaScript and does not need server-side rendering. This should provide good performance, quick deploymennt, seamless integration, and lower maintenance overhead.