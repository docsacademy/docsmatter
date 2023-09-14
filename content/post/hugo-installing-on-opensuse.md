+++
author = "Vladimir Likhanov"
title = "Installing Hugo on openSUSE"
date = "2021-05-10"
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

> In this post, you'll learn how to set up Hugo on a system running openSUSE Leap 15.2.
If you are using another version of openSUSE, the installation procedure may slightly
differ.

At the moment of this writing, there is no official Hugo package available for openSUSE 15.2.
However, you can still set up the Hugo static site generator on a machine with openSUSE 15.2
using alternative methods. The procedure below describes how to do this with the help of the
Snap package manager.

1. If the *snappy* repository is not available on your system, add it by running this command:

        ~> sudo zypper addrepo --refresh https://download.opensuse.org/repositories/system:/snappy/openSUSE_Leap_15.2 snappy
        Adding repository 'snappy' ........................................................................[done]
        Repository 'snappy' successfully added
        ...

> NOTE: If you are using another version of openSUSE, replace *15.2* in the command above with your own version.

2. Import the GPG key for the snappy repository:

        ~> sudo zypper --gpg-auto-import-keys refresh
        ...

3. Upgrade the package cache to include the *snappy* repository:

        ~> sudo zypper dup --from snappy

4. Install Snap on your local machine:

        ~> sudo sudo zypper install snapd
        ...
        Additional rpm output:
        Please reboot, logout/login or source /etc/profile to have /snap/bin added to PATH.
        On a Tumbleweed system you need to run: systemctl enable snapd.apparmor.service

5. Restart your system to add Snap to the **PATH** environment variable. After restart,
proceed with the next step.

6. Enable and start the *snapd* service:

        ~> sudo systemctl enable --now snapd
        Created symlink /etc/systemd/system/multi-user.target.wants/snapd.service → /usr/lib/systemd/system/snapd.service.

7. Install the Hugo package:

        ~> sudo snap install hugo
        ...
        hugo 0.80.0 from Hugo Authors installed

> NOTE: To install the extended Hugo version, use this command instead:

        ~> sudo snap install hugo --channel=extended

That's it! Now you can create your first Hugo site on openSUSE.