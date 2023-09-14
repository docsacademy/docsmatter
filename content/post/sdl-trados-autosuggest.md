+++
author = "Vladimir Likhanov"
title = "AutoSuggest"
date = "2021-06-24"
description = "Powerful translation tools"
featured = false
tags = [
    "SDL Trados Studio"
]
categories = [
    "Translation Management",
]
series = ["Working with SDL Trados Studio"]
thumbnail = "images/blog/sdl-trados-autosuggest.png"
+++

> This post deals with AutoSuggest in SDL Trados Studio - a special technology that monitors what
you are typing and presenting you with a list of suggested words and phrases you can use in your
translation.

[**PREVIOUS POST**](/post/sdl-trados-tm-tb/) **< || >** [**NEXT POST**](/post/sdl-trados-editions/)

Unlike the translation memory, which stores entire segments, AutoSuggest is based on incomplete
segments - words or phrases. The principle of AutoSuggest is similar to that of AutoComplete in
Microsoft Word - that is, appropriate words and phrases are suggested automatically when you
translate text in SDL Trados Studio.

For example, if you type the *C* letter, the system (depending on the context of the source text)
tries to guess which word or phrase you are trying to translate and suggests the **Create object**
segment as a translation option. If the AutoSuggest dictionary contains several matching segments,
all segments are shown. By clicking on the corresponding entry, you can copy it into your translation.

![AutoSuggest in SDL Trados Studio - Example 1](/images/blog/sdl-autosuggest-example-01.png)

Fragments from the AutoSuggest dictionary can be recognized by the blue book icon in front of the
fragment. The green icon is used for terms found in the terminology database.

As you enter the following letters, the list of fragments is updated accordingly and offers only
suitable fragments.

![AutoSuggest in SDL Trados Studio - Example 2](/images/blog/sdl-autosuggest-example-02.png)

Words and phrases in AutoSuggest can be taken from several sources:

* **Lists with auto-text**. You can create your own lists containing specific words and phrases. These
words and phrases are automatically suggested when you translate texts.

* **AutoSuggest Dictionaries**. AutoSuggest dictionaries contain words and phrases retrieved from
the translation memory. A special module in SDL Trados Studio analyzes the translation memory, finds
the appropriate words and phrases, and adds them to the AutoSuggest dictionary. See also the
information about the SDL AutoSuggest Creator module below.

* Instances of translation memories and machine translation systems configured for use with your
project.

* SDL MultiTerm terminology databases.

* Fragment matches from translation memory instances that support *fragment alignment*.

## SDL AutoSuggest Creator

If you are using SDL Trados Studio Freelance or SDL Trados Studio Freelance Plus version, you need to
purchase an additional module - SDL AutoSuggest Creator - to generate AutoSuggest dictionaries.
SDL Trados Studio Professional Edition owners do not need an additional module - the AutoSuggest dictionary
creation feature is built into this version. You can call the dictionary creation function by clicking
the **Create AutoSuggest Dictionary** button on the **Home** tab of the **Welcome** section.

![AutoSuggest in SDL Trados Studio - calling the function](/images/blog/sdl-autosuggest-calling-function.png)

[**PREVIOUS POST**](/post/sdl-trados-tm-tb/) **< || >** [**NEXT POST**](/post/sdl-trados-editions/)