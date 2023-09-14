+++
author = "Vladimir Likhanov"
title = "Installing Visual Studio Code on Ubuntu"
date = "2022-04-12"
description = "Working with Linux"
featured = true
tags = [
    "Ubuntu"
]
categories = [
    "Linux",
]
thumbnail = "images/blog/linux/ubuntu-logo.png"
+++

> This post deals with installing the Visual Studio Code (VSC) application on Ubuntu (versions 16.04 and higher).

Visual Studio Code (VSC) is a modern and very convenient IDE from Microsoft. It has a built-in code debugger,
version control support, syntax highlighting, and many other features.

You can install the VSC application on Ubuntu in one of the following ways:

* Using the *.deb/.rpm* packages from the [official Microsoft repository](https://code.visualstudio.com/download)

![Official Microsoft repository for Visual Studio Code](/images/blog/linux/ubuntu-vsc-microsoft-repository.png)

* Using the Ubuntu Software center on your local laptop / Pc

![Visual Studio Code in the Ubuntu Software center](/images/blog/linux/ubuntu-vsc-software-center.png)

* Using a [Snap package](https://snapcraft.io/code)

![Snap package for Ubuntu](/images/blog/linux/ubuntu-vsc-snap-package.png)

In our article, we’ll use the Snap package to set up VSC on your laptop or PC. VSC is distributed as a Snap
package and can be downloaded from the Snap Store.

> A snap is a bundle of an app and its dependencies that works without modification across many different Linux
distributions. Snaps are discoverable and installable from the Snap Store, an app store with an audience of millions.</br></br>
**Work Cited** </br>
https://snapcraft.io/docs/getting-started

Do the following:

1. Make sure that **snap** is installed on your machine (it should normally be the case starting from Ubuntu 16.04):

        $ snap version
        snap    2.54.4
        snapd   2.54.4
        series  16
        ubuntu  20.04
        kernel  5.13.0-39-generic

2. Find the VSC package in the Snap store:

        $ snap find vscode
        Name                        Version   Publisher   Notes    Summary
        code                        8dfae7a5  vscode✓     classic  Code editing. Redefined.
        code-insiders               fcaeb69e  vscode✓     classic  Code editing. Redefined.
        vscode-json-languageserver  1.3.4     alexmurray  -        JSON Language Server
        karuta                      0.6.7     nekoaddict  -        Karuta is a scripting language for FPGA design (so called HLS).
        awdur                       0.0.7     alcarney    -        Simple Screenwriting Application
        code-tray                   1.0.0     devcass     -        Code Tray

2. Look for the **code** entry in the **Name** column. This package contains all the files necessary for setting up VSC.

3. Run the following command to download and install the application:

        $ sudo snap install --classic code
        [sudo] password for docsmatter:
        code 8dfae7a5 from Visual Studio Code (vscode✓) installed

Snaps are rather big in size. So, it may take some time to download and install the VSC package, depending on your internet speed.

Once VSC is installed, you can use the VSC editor to create and manage text files on your system. For example, to open a file in VSC
from the terminal, run this command:

        $ code *path_to_file*

After launching VSC for the first time, you may wish to configure some of its settings (like choosing another theme) or install some
additional components for working with your code.

## Removing VSC

If you decide that you don't need the VSC editor anymore, you can easily remove it from your Ubuntu system by running this command:

        $ sudo snap remove code
