+++
author = "Vladimir Likhanov"
title = "Switching a Hugo theme"
date = "2021-08-06"
description = "Static site generators"
featured = false
tags = [
    "Hugo"
]
categories = [
    "Static Site Generators",
]
thumbnail = "images/blog/hugo-bg.png"
+++

> In this post, we'll take a look at how to switch Hugo themes to give your website
a new look and feel.

Hugo uses a special mechanism to control the look and feel of your websites—themes. You can
check the full list of available themes at https://themes.gohugo.io/.

Let's assume that you have installed a Hugo theme and used it for some time. But now you
want to try something new, maybe a theme providing additional features and functions. In this
case, you can follow the steps below to switch your website to another theme:

1. Decide which theme meets your demands best of all. In our example, we'll make a switch to the
[Clarity](https://themes.gohugo.io/themes/hugo-clarity/) theme.

2. Change to your website directory (as a rule, **/home/my-user/hugo/site-name/**) and add the
Clarity theme.

        $ git submodule add https://github.com/chipzoller/hugo-clarity themes/hugo-clarity
        Cloning into 'C:/Hugo/docsmatter.org/themes/hugo-clarity'...
        remote: Enumerating objects: 3179, done.
        remote: Counting objects: 100% (338/338), done.
        remote: Compressing objects: 100% (158/158), done.
        remote: Total 3179 (delta 182), reused 276 (delta 153), pack-reused 2841
        Receiving objects: 100% (3179/3179), 5.16 MiB | 3.11 MiB/s, done.
        Resolving deltas: 100% (1841/1841), done.
        warning: LF will be replaced by CRLF in .gitmodules.
        The file will have its original line endings in your working directory

3. Open the **config.toml** file in your favorite editor. This file is located in the Hugo
main directory (**/home/my-user/hugo/**).

4. Navigate to the **theme** property in this file and change its value to the name of your
new theme, for example:

        theme = "hugo-clarity"

5. Save the **config.toml** file. This will activate your new theme.

6. Run the following command to start the local Hugo server:

        $ hugo server

7. Open your browser, type http://localhost:1313/, and press Enter.

8. Make sure that the new layout has been successfully applied to your website.

> **Customizing existing content** <br />
As the structure and functions provided by your existing theme sometimes differ from those
in your new theme, you may need to perform some additional operations to make your website
fully functional or look the way you want.