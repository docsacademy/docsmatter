+++
author = "Vladimir Likhanov"
title = "Translation memory and terminology databases"
date = "2021-06-14"
description = "Powerful translation tools"
featured = false
tags = [
    "SDL Trados Studio"
]
categories = [
    "Translation Management",
]
series = ["Working with SDL Trados Studio"]
thumbnail = "images/blog/sdl-translation-memory-example.png"
+++

> In this post, we'll take a look at two main components of any CAT system - *translation memory* and *terminology database*.

[**PREVIOUS POST**](/post/sdl-trados-cat-vs-machine-translation/) **< || >** [**NEXT POST**](/post/sdl-trados-autosuggest/)
## Translation memory

A translation memory is a special database that stores the source text and its translated equivalent. When new texts are translated, the translation memory is checked for identical or similar fragments:

* If the CAT system finds such fragments, it suggests them for reuse. You can apply the fragments without any changes or correct them as needed. The corrected fragment is also saved in the translation memory and can be used later when translating new texts.
* If the CAT system does not find similar fragments, you can enter the translation for the new fragment manually. Once the fragment is translated, it is also saved in the translation memory and the system moves on to the next fragment.

As a rule, translation memories are stored as separate files that can be connected to CAT systems. Some systems allow you to work with several files simultaneously (for example, SDL Trados Studio). In this case, one memory acts as the main one and the rest are used for reference.

The advantage of using a CAT system is most clearly seen when you update already translated documents. All fragments which have not changed since the last translation are translated automatically, and the translation of similar, previously translated sentences is displayed for the changed fragments (see also the picture above).

Texts are stored in the translation memory in the form of so-called *segments*. A segment can be any piece of text: a whole sentence, a header, a list item, etc. Along with translated segments, the translation memory usually stores additional information about the segments: creation and modification date and time, translator's name and so on.

![Additional information about segments](/images/blog/additional-info-on-segments.png)

1 - segments <br/>
2 - additional information

## Terminology database

Usually, a CAT system works in conjunction with other applications and, first of all, with terminology management systems. These systems allow you to create *terminology databases* (also referred to as *termbases*), bilingual dictionaries that contain translations of words or small phrases. During the translation process, the CAT system checks the connected terminology database and shows the translation of those terms that appear in the current segment.

In addition to the terms themselves, termbases contain various linguistic information (gender, part of speech, case, number, etc.) and meta-information (scope, source, etc.). For some terms, synonyms and examples of use in a certain context can also be provided.

![Additional information about segments](/images/blog/multiterm-example.png)

Listed below are some of the benefits of using terminology databases:

* Improved translation quality
* Reduced translation costs
* Recognition of forbidden terms
* Better perception of translated texts and, as a result, greater customer satisfaction

[**PREVIOUS POST**](/post/sdl-trados-cat-vs-machine-translation/) **< || >** [**NEXT POST**](/post/sdl-trados-autosuggest/)