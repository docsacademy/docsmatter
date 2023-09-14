+++
author = "Vladimir Likhanov"
title = "Setting up pandoc on Windows"
date = "2022-10-23"
description = "Setting up pandoc on a Windows operating system"
featured = true
draft = true
tags = [
    "pandoc"
]
categories = [
    "Markup formats",
]
thumbnail = "images/blog/lightweight-markup-languages/pandoc-logo.png"
+++

> In this post, we'll see how to set up the **pandoc** utility on a Windows operating system. You can then use this utility
to convert files from one markup format into another (Word to Markdown, Markdown to HTML, and so on).

Pandoc is a universal utility for working with different text formats. It's mainly used to format mathematical and technical
texts. [pandoc](https://pandoc.org/) can be installed on different operating systems, e.g.:

* Linux
* macOS
* Windows

In this article, we'll install **pandoc** on a Windows computer:

1. Go to the [pandoc installation page](https://pandoc.org/installing.html) and click on **Download the latest release for Windows**
button.

* The installation file is downloaded.

2. Double-click on the installation file.

* The **Pandoc Setup** window opens.

![Pandoc - license agreement](/images/blog/lightweight-markup-languages/pandoc-license-agreement.png)

3. Activate the **I accept the terms in the License Agreement** option and click **Install**.

* The **pandoc** utility is installed on your laptop.
* The progress is displayed in the **Installing Pandoc** window.
* Once the installation is complete, the **Complete Pandoc Setup Wizard** window is shown.

![Pandoc - installation complete](/images/blog/lightweight-markup-languages/pandoc-installation-complete.png)

4. Click on the **Finish** button.

* The wizard is closed.

## Pandoc in Action

Let us check that the **pandoc** utility has been successfully installed on your laptop and is ready for use:

1. Open the Windows command prompt (**Start** - **Terminal**).

2. Type the following command and press Enter:

        C:\>pandoc --version
        Compiled with pandoc-types 1.22.2.1, texmath 0.12.5.2, skylighting 0.13,
        citeproc 0.8.0.1, ipynb 0.2, hslua 2.2.1
        Scripting engine: Lua 5.4
        User data directory: C:\Users\vl-sc\AppData\Roaming\pandoc
        Copyright (C) 2006-2022 John MacFarlane. Web:  https://pandoc.org
        This is free software; see the source for copying conditions. There is no
        warranty, not even for merchantability or fitness for a particular purpose.

If your output looks similar to the one above, you've successfully installed the **pandoc** utility and can
now use it for converting different markup formats.

Now try the following to see **pandoc** in action:

1. In the command prompt, run this command:

        C:\>pandoc

* The cursor is moved to the next line and is blinking waiting for your input.

2. Type the following text:

         Use **pandoc** to convert

         * Markdown to HTML
         * HTML to Markdown

3. Press Ctrl+Z and then Enter.

You should now see the following output in the command prompt:

    <p>Use <strong>pandoc</strong> to convert</p>
    <ul>
    <li>Markdown to HTML</li>
    <li>HTML to Markdown</li>
    </ul>

What happened? Pandoc has interpreted your entered text as Markdown and converted it to the HTML output. This
is the default behavior when you run **pandoc** without any options and arguments.