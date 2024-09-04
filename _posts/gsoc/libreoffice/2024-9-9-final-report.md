---
title: 'Final Report - GSoC'24'
date: 2024-09-09
permalink: /posts/gsoc/libreoffice/final-report-2024
tags:
  - gsoc
  - libreoffice
  - open-source
---

Abstract
========
- Thanks to my mentors
- Really fun and challenging experience
- Hard codebase
- I loved open-source and I want to continue to contribute

About The Project
=============
My project was about making general improvements to the function deck in Calc,
but we made theses enancements apply to botth function deck (FD) and function wizard (FW).

- [ ] A short description of the goals of the project.
- [ ] Any challenges or important things you learned during the project.

***Project Goals:***
  - List all functions in collapsible sections (rather the current filtering per dropdown)
  - Add a help button to open the respective documentation page
  - Consider direct editing capabilities

The meta-bug ticket on Bugzilla: https://bugs.documentfoundation.org/show_bug.cgi?id=92416

My Work & Progress
==================
My work was splitted into seperate tasks.

> Note: you can go to the bug ticket on Bugzilla by clicking on tdf#***** at the begining of the commit message.

### *Converting functions list into collapsible sections*
Patch link: https://gerrit.libreoffice.org/c/core/+/169639  

### *Adding a help button to open respective help documentation*
Patch link: https://gerrit.libreoffice.org/c/core/+/170181  
Some minor bug fix: https://gerrit.libreoffice.org/c/core/+/171929  

### *Enhancing searching functionality*
Patch link: https://gerrit.libreoffice.org/c/core/+/170073  

### *Adding a category to store favorite functions*
Patch link: https://gerrit.libreoffice.org/c/core/+/171828  

### *Making Initial focus to be in the document when creating a new sheet*
Patch link: https://gerrit.libreoffice.org/c/core/+/171709  

Futrue Work
-----------

### *Cycling between absolute and relative cell/range references everywhere using F4 Key*
Bug Link: https://bugs.documentfoundation.org/show_bug.cgi?id=162287  

### *Adding typical keyboard shortcuts*

================
