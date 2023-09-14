+++
author = "Vladimir Likhanov"
title = "Generating documents with the Asciidoctor Docker image"
date = "2021-08-10"
description = "Lightweight Markup Languages"
featured = true
tags = [
    "AsciiDoc",
    "openSUSE",
    "Docker"
]
categories = [
    "Lightweight Markup Languages",
]
thumbnail = "images/blog/asciidoc-bg.png"
+++

> This post explains how to convert AsciiDoc files using a Docker image. 

## Why use the Asciidoctor Docker image

Instead of installing all the necessary packages by yourself, you can use a Docker image.
The Asciidoctor Docker image includes everything you need to generate your documentation in
different formats:

* PDF
* EPUB
* HTML
* etc.

The benefit of this approach is that you can bypass setting up the Asciidoctor processor
and get right down to generating your documentation.

## Preparation steps

First, you need to install Docker on your machine. In our example, we will set up Docker on
a machine running openSUSE Leap 15.2. If you are using another Linux distribution, see the
instructions at https://docs.docker.com/engine/install. Here you also find information about
installing Docker on macOS and Windows.

Do the following:

1. Install the **docker** and **docker-compose** packages:

        ~> zypper install docker python3-docker-compose

2. Join the currently logged-in user to the Docker group to allow him to use the Docker daemon:

        ~> sudo usermod -G docker -a $USER

3. Restart the Docker daemon:

        ~> sudo systemctl restart docker

4. Make sure that Docker is running:

        ~> docker version
        Client:
        Version:           19.03.15
        API version:       1.40
        Go version:        go1.13.15
        ...

5. Search for an image providing the Asciidoctor environment:

        ~> sudo docker search asciidoctor
        NAME                                 DESCRIPTION                                     STARS
        asciidoctor/docker-asciidoctor       A Docker image for using the Asciidoctor …      56  
        softwarecraftsmen/asciidoctor-node   FROM asciidoctor/docker-asciidoctor, adding …   0
        ...

> NOTE: You should be interested in the line containing the folllowing entry in the **NAME**
column - **asciidoctor/docker-asciidoctor**. It should also contain the **OK** value
in the **OFFICIAL** column. That means that this image is hosted by the Docker organization.

6. Download the image to your local machine:

        ~> sudo docker pull asciidoctor/docker-asciidoctor

7. Wait until the download is complete and run this command to check if the image is now
available on your local machine:

        ~> docker images
        REPOSITORY                       TAG                 IMAGE ID            CREATED             SIZE
        asciidoctor/docker-asciidoctor   latest              db948d49c744        2 weeks ago         452MB

Now you are ready to create the documentation from your AsciiDoc files.

## Creating documentation from AsciiDoc files

You need to perform the steps above only once. After that, you can generate documentation from
AsciiDoc files at any time by doing the following:

1. Starting the Docker container and mapping the directory where you store the AsciiDoc files to
the **/documents** directory in the container, for example:

        ~> docker run -it -v /home/user/directory-with-asciidoc-files:/documents/ asciidoctor/docker-asciidoctor
        bash-5.1# 

This command assumes that your AsciiDoc files are located in the **/home/user/directory-with-asciidoc-files**
directory. Now you are inside the running Docker container and can publish your documentation.

2. Using Asciidoctor commands to create the output in different formats. For example, to create the HTML and PDF
documents from the **my-asciidoc-file.adoc** file, execute these commands:

        ~> asciidoctor my-asciidoc-file.adoc
        ~> asciidoctor-pdf my-asciidoc-file.adoc

