---
title: "Final Report - GSoC'25"
date: 2025-09-01
permalink: /posts/gsoc/vlc/final-report-2025
tags:
  - gsoc
  - open-source
  - vlc
  - ndi
---

## GSoC'25 with VLC 🎉

Hello everyone 👋

This year marked my second time participating in Google Summer of Code (GSoC), and it felt both familiar and completely new at the same time. Having gone through GSoC before, I was able to approach the program with more confidence and perspective, but the challenges were on a whole different scale.

I had the privilege of working with **VLC**, one of the most widely used open-source media players and one of my favorite FOSS projects. My project focused on **Network Device Interface (NDI)**, a protocol designed for high-quality, low-latency video transmission over networks.

Until now, there was no open-source, cross-platform implementation of NDI. There was an early prototype library, `libNDI`, had been started 5 years ago by Jean-Baptiste Kempf, but was incomplete and difficult to maintain. My task was to **revive and expand this library**, then integrate it into VLC so the player could discover and play NDI streams out of the box.

### Why this matters

_To begin with, NDI is fun :)_  
Adding NDI support addresses a noticeable gap in the open-source ecosystem. Since many broadcasters, streamers, and production setups rely on NDI for real-time workflows, extending VLC with the ability to handle NDI streams makes the protocol more accessible to a wider community, including both professionals and hobbyists.

## Project Goals

The original goals outlined in my proposal included:

1. **Expand Protocol Support**

   - Implement support for NDI-HX2
   - Develop a UDP-based NDI variant

2. **Reduce Dependencies & Improve Performance**

   - Remove dependency on libavutil
   - Optimize memory and buffer handling

3. **Strengthen Security & Stability**

   - Add fuzzing-based testing
   - Improve error handling and robustness

4. **Implement Stream Sending**

5. **Integrate `libNDI` into VLC**

## My Work & Progress

The project began with a major **refactoring of `libNDI`** to make it efficient, modular, and maintainable. From there, I worked on extending its functionality and integrating it into VLC.

Some highlights include:

- **Library improvements**

  - Large-scale code refactoring for clarity and maintainability
  - Enhanced receiving functionality with **non-blocking support**
  - Reduced reliance on external libraries

- **VLC integration**

  - VLC can now discover and playback NDI streams directly

- **Ongoing development**

  - Continuing work on full support for all HX variants, which requires deep analysis of sender behavior

Key merge requests:

- [Import Tobias’ work & Refactor Code](https://code.videolan.org/jbk/libndi/-/merge_requests/12) (Merged)
- [Integrate libNDI into VLC](https://code.videolan.org/videolan/vlc/-/merge_requests/7371) (In Progress)
- [Add NDI Input Module](https://code.videolan.org/videolan/vlc/-/merge_requests/7396) (In Progress)

Repository: [libNDI](https://code.videolan.org/AhmedHamed3699/libndi)

## Future Work

There is still plenty of room for growth, including:

- Implementing a **stream sending pipeline**
- Adding a **UDP-based variant** (with QUIC support)
- Integrating **fuzzing-based testing** to strengthen security against malformed packets

## Reflections

This project has been one of the most exciting experiences of my open-source journey so far. Unlike my first GSoC, which was about enhancing usability within an existing application, this year I worked on a standalone library and its integration into a larger system, a very different challenge that taught me a lot about networking, packet analysis, and multimedia streaming.

The work was both enjoyable and challenging, especially given the limited documentation available for NDI. Moving forward often meant experimenting, carefully observing different behaviors, and analyzing network traffic to piece together how everything worked. This process was not always straightforward, but it was incredibly rewarding.

I am deeply grateful to my mentors, **Steve Lhomme** and **Jean-Baptiste Kempf**, as well as the VLC community, for their constant support, feedback, and guidance. The review process was one of the most engaging and insightful experiences I’ve had, and their mentorship pushed me to think critically and tackle problems from multiple angles.

I’m proud of what we’ve achieved, and even more excited about the potential of where this project will go. I look forward to continuing this collaboration, improving `libNDI`, and contributing to VLC and the open-source ecosystem.
