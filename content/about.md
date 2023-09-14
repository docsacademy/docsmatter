+++
title = "About"
description = "About me, this website and used technologies"
date = "2021-04-28"
aliases = ["about-us", "about-hugo", "contact"]
author = "Vladimir Likhanov"
+++

![](/images/avatar.png)

My name is Vladimir Likhanov. I'm a translation manager, CCMS (Component Content Management Systems) administrator, and technical writer with over 18 years of professional experience in creating software documentation. I love researching new technologies, finding their best use cases, and turning them into useful information sources for end users and developers.

In my current position at a German software company, I work with the developers and QA engineers to plan and write various documentation for complex IT projects in English and German.
I’m responsible for creating and maintaining the company's online help, user and administrator manuals as well as installation guides, system requirements, release notes, and API documentation.

[Dowload Resume](/pdfs/resume.pdf)

## About DocsMatter

The DocsMatter website provides useful resources that can help you create good technical documentation.

Here, you can find information about modern technical writing tools and approaches, including

* docs like code
* Markdown
* AsciiDoc
* Git and GitHub
* static site generators (Hugo, Sphinx, and Gatsby)
* documentation standards (e.g. XML and DITA)
* and so on

You will also learn about other technical documentation-related topics like translation management and video editing.

## About technologies behind this website

This website was built using the Hugo static site generator. For storing and delivering the site’s static content, Amazon Simple Storage Service (S3) and Amazon CloudFront (CDN) are used.

The source content is created in Markdown, a lightweight markup language that can be written with any plain-text editor. As an editor, Visual Studio Code is used providing support for Markdown out of the box.

All source files are stored in a local Git repository. At regular intervals, the content is pushed to a remote repository on GitHub. The repository on GitHub is integrated with Travis CI that takes care of continuous integration and delivery (CI / CD).