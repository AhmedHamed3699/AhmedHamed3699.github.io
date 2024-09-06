---
title: "Final Report - GSoC'24"
date: 2024-09-09
permalink: /posts/gsoc/libreoffice/final-report-2024
tags:
  - gsoc
  - libreoffice
  - open-source
---

## Hello everybody :)

LibreOffice Calc has a nice functions deck on the sidebar allowing to pick one of the many functions,
and this functions panel has some room for improvements. 
The project aims to improve this functions deck to enhance usability and functionality 
to create a better user experience.  

The project was about making these general improvements to the function deck,
but we find it better to make the enancements apply to both function deck (FD) and function wizard (FW). 
It was not always an easy thing to do it in both places, as they are in different modules and created with different code structrures.

It was really challenging working with such complex code base,
I did spend most of the time trying to find where to put what, with dozens of hours debugging. 
Actully my debugging skills has been enhanced alot with the use of debuggers like rr which is built on top of gdb.

***Project Goals:***
  - List all functions in collapsible sections (rather the current filtering per dropdown)
  - Add a help button to open the respective documentation page
  - Improve searching techniques

***Abandoned Goals:***
  - Save custom made formulas, to be used anywhere
  - Add an editor area that provides structure of the function, with:
    - Syntax highlighting and formatting – with connection to referenced cells
    - Ability to drill down for better debugging process

[Link to The meta-bug ticket on Bugzilla](https://bugs.documentfoundation.org/show_bug.cgi?id=92416)

My Work & Progress
==================
My work was splitted into seperate tasks conserning every proposed enhancement.

> Note: you can go to the bug ticket on Bugzilla by clicking on tdf#***** at the begining of the commit message.

***Converting functions list into collapsible sections*** -->
[Patch link](https://gerrit.libreoffice.org/c/core/+/169639)  

***Adding a help button to open respective help documentation*** ->
[Patch link](https://gerrit.libreoffice.org/c/core/+/170181) - 
[Bug fix](https://gerrit.libreoffice.org/c/core/+/171929)

***Enhancing searching functionality - adding similarity search*** ->
[Patch link](https://gerrit.libreoffice.org/c/core/+/170073)

***Adding a category to store favorite functions*** ->
[Patch link](https://gerrit.libreoffice.org/c/core/+/171828)

***Making Initial focus to be in the document when creating a new sheet*** ->
[Patch link](https://gerrit.libreoffice.org/c/core/+/171709)

Futrue Work
-----------

- *Cycling between absolute and relative references everywhere using F4 Key* ->
[Bug Link](https://bugs.documentfoundation.org/show_bug.cgi?id=162287)

- *Adding typical keyboard shortcuts*

Screenshots of the enhancements
-------------------------------
### The Function Deck
![FD](../../../images/Functions-Deck.png)

### The Function Wizard
![FW](../../../images/Function-Wizard.png)

------------------------------------------------------

I really enjoyed working on this project, it was a great and challenging experience. I am willing to continue contributing to LibreOffice and open-source in general.
I would like to show my gratitude to the community for their help, and speciall thanks to my mentors (Andreas Heinisch, Heiko Tietze) for their guidance and support throughout the project.