+++
author = "Vladimir Likhanov"
title = "Installing Ubuntu - the easy way"
date = "2022-05-15"
description = "Installing Ubuntu on your laptop / PC"
featured = true
tags = [
    "Ubuntu"
]
categories = [
    "Linux",
]
thumbnail = "images/blog/linux/ubuntu-logo.png"
+++

> This post covers how to install Ubuntu (LTS) on your laptop or PC, including different options you can choose during the installation process.

## Prerequisites

We assume the following:

* You’ve checked the hardware requirements for installing Ubuntu. If you have not, visit the [Ubuntu download page](https://ubuntu.com/download/desktop).

* You’ve downloaded the ISO image of Ubuntu. In our example, we’ll use the Desktop version of [Ubuntu 20.04.4 LTS](https://ubuntu.com/download/desktop).

* You’ve created a bootable Ubuntu USB stick containing the downloaded ISO image. For example, you can use the [Rufus utility](https://rufus.ie/downloads/) to create a bootable USB stick on Windows. And the default Disk Utility helps you to write the ISO image to your USB stick on Mac.

> You can also use another installation media (e.g., DVD) to install Ubuntu following the instructions below.

* You’ll have a single partition for storing all your files.

* Your BIOS is configured to boot from a USB drive.

* You don’t mind erasing your hard drive.

## Installation

1. Insert the Ubuntu USB stick (or another installation media) into your drive and reboot your laptop / PC.

* After a while, the initial installation screen is displayed. On this screen, you can choose the language you want
to use during installation.

![Installing Ubuntu - choosing the language](/images/blog/linux/ubuntu-installation-choosing-language.png)

2. Select the English entry and click the **Install Ubuntu** button on the right part of the screen.

* The **Keyboard layout** window opens.

![Installing Ubuntu - choosing the keyboard layout](/images/blog/linux/ubuntu-installation-keyboard-layout.png)

3. Choose the keyboard layout you want to use and click **Continue**. This setting also determines some language-related elements of your system (e.g., the language used by spell checkers).

* The **Updates and other software** window opens.

![Installing Ubuntu - choosing the initial installation set](/images/blog/linux/ubuntu-installation-choosing-software.png)

4. Choose the initial software installation set - either normal or minimal. <br/>
-- If your storage capacity is limited, go with the minimal installation set. Otherwise, leave the **Normal installation option** activated.<br/>
-- Decide whether you want to download updates during the installation. This can save you time later.<br/>
Once you are done, click **Continue**.

* The **Installation type** window opens.

![Installing Ubuntu - choosing the installation type](/images/blog/linux/ubuntu-installation-choosing-type.png)

5. Choose the installation type. If you are installing Ubuntu on new hardware (what we assume in this article and what is recommended if you are new to Linux), leave the **Erase disk and install Ubuntu** option activated. If you want to divide your drive into smaller partitions, see, for example, https://help.ubuntu.com/community/HowtoPartition/ResizingPartition for more detail.

6. Click **Install now** and then in the confirmation window that opens, click **Continue**.

* The **Where are you?** window opens.

![Installing Ubuntu - choosing the location / zone](/images/blog/linux/ubuntu-installation-choosing-zone.png)

7. Make sure that your current location / zone is selected in the drop-down list and click **Continue**. As a rule, this information is detected automatically if you have an active Internet connection.

* The **Who are you?** window opens.

![Installing Ubuntu - entering the login information](/images/blog/linux/ubuntu-installation-entering-credentials.png)

8. Enter the information for logging in to your system (username, password, etc.) and click **Continue**.

* Ubuntu is installed on your laptop / PC.

* The installation progress is shown in the Install window.

![Installing Ubuntu - entering the login information](/images/blog/linux/ubuntu-installation-progress.png)

9. Click **Restart Now**.

10. If asked, remove your USB stick from the laptop / PC and press Enter.