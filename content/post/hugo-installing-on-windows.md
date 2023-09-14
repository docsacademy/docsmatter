+++
author = "Vladimir Likhanov"
title = "Installing and updating Hugo on Windows"
date = "2021-08-03"
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

> This post walks you through the process of installing the Hugo static site
generator on a Windows system and updating it once a new generator version
is released.

## Installing Hugo on Windows

In this example, I assume that you will use the following folders for Hugo:

* C:\Hugo. This folder will store all Hugo-related files.
* C:\Hugo\bin. This folder will contain the Hugo executable files.
* C:\Hugo\sites. This folder will store your Hugo sites.

If some of these folders are missing on your system, create them before proceeding with
the installation.

Follow these steps to install Hugo on a Windows system:

1. Open the [Hugo releases](https://github.com/gohugoio/hugo/releases) page.

2. Navigate to the section with the installation files for different operating systems.
The Hugo installation files for Windows are usually located at the bottom of this section.

![Hugo installation files](/images/blog/hugo-windows-installation-files.png)

3. Click on the required ZIP file to download it to your computer. Please notice that your theme
may require the extended Hugo version to function correctly. In this case, you should look for
the file containing **extended** in its name.

4. Extract the content of the downloaded ZIP file to the **C:\Hugo\bin** folder. As a rule, the
extracted content contains the **hugo.exe** executable file and some additional files.

5. Add the **hugo.exe** executable file to your **PATH** variable. In this way, Windows will know
where to look for this file when you run Hugo-related commands in the command prompt. The
easiest way to update your PATH variable is run the following command in Windows PowerShell:

        set PATH=%PATH%;C:\Hugo\bin

6. Open the command line and execute this command:

        hugo version
        hugo v0.87.0-B0C541E4+extended windows/amd64 BuildDate=2021-08-03T10:57:28Z VendorInfo=gohugoio

If your command output looks like the one above, you have successfully set up Hugo on your computer
and can now proceed with creating your first static website.

## Updating Hugo

Once a new Hugo version is released, you may want to update your existing installation to benefit from
new features or fixed bugs. In this case, follow the steps below:

1. Follow steps 1 to 3 above to download the new Hugo version.

2. Extract the downloaded file to some folder on your computer.

3. Copy the extracted files to the **C:\Hugo\bin** folder. This should replace your existing Hugo files
with the new ones.

4. Execute this command in the command prompt to make sure that you are now using the updated version
of Hugo.

        hugo version