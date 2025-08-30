---
title: "Final Report - GSoC'25"
date: 2025-09-01
permalink: /posts/gsoc/vlc/final-report-2025
tags:
  - gsoc
  - open-source
---

## GSoC'25 is Over 🎉

Hello everyone 👋

This year was my second time participating in the Google Summer of Code (GSoC), and the experience turned out to be quite different from my first. Having gone through the program before, I was able to approach it with more perspective, while also exploring new challenges and areas of contribution. This time, I had the opportunity to work with VLC, one of my favorite FOSS projects, and the journey has been both rewarding and a valuable step forward in my open-source involvement.

Network Device Interface (NDI) is a software specification that enables
high-definition video transmission over a computer network with low
latency and high quality.

There was an open-source cross-platform library called libNDI started by Jean-Baptiste Kempf 5 years ago, but it was in its very early stages with everything nearly in one file. It only supported receiving NDI streams and lacked support for the newer NDI-HX variants. My project aimed to enhance this library overall structure and improved performance and security and expand NDI versions supportby adding support for sending NDI streams. So, The improved implementation was then integrated into VLC, enabling seamless NDI-based discovery and playback within the media player.

This was an incredible opportunity, as there was no existing open-source, cross-platform implementation of the NDI protocol. I believe this project will bring significant value to the community. The experience was both enjoyable and challenging, especially since there was little to no clear documentation available. To move forward, I had to experiment extensively, investigate different behaviors, and analyze the network to truly understand how everything worked.

**_Project Goals:_**

These are the goals that were orignially mentioned in the proposal:

1. Expand Protocol Support
   a. Implement support for NDI-HX2.
   b. Develop a UDP-based NDI variant.
2. Implement NDI Stream Sending
3. Reduce Dependencies to Improve Performance
   a. Remove dependency on libavutil (av_fifo functions).
   b. Optimize memory management and buffer handling.
4. Strengthen Security & Stability
   a. Integrate fuzzing-based security testing.
   b. Improve error handling and robustness.
5. Integrating libNDI into VLC.

## My Work & Progress

This is a link to libndi project repository: [libndi](https://code.videolan.org/AhmedHamed3699/libndi)

We found that the library needs a lot of refactoring so it can be more efficient and easier to maintain and add new features. So that was our main focus, besides integrating libNDI into VLC.

- Improve libNDI library
  - A great amount of code refactoring to improve maintainability.
  - Improved receiving functionality.
  - Add non-blocking support for receiving NDI streams.
  - Reduced Dependencies on external libraries
- Integrate libNDI into VLC successfully, and now it can discover and playback NDI streams.

Currently working on adding support for all HX variants, it is taking more time than expected due to the complexity of analyzing the behaviour of the sender.

Project was split into some MRs, you can find them here:

[Import Tobias Work & Refactor Code](https://code.videolan.org/jbk/libndi/-/merge_requests/12) (Merged)  
[Integrate libNDI into VLC](https://code.videolan.org/videolan/vlc/-/merge_requests/7371) (In Progress)  
[Add NDI input module ](https://code.videolan.org/videolan/vlc/-/merge_requests/7396) (In Progress)  

## Future Work

- Implement NDI Stream Sending Pipeline
- Expand Protocol Support with a UDP-based NDI variant and implement QUIC support
- Strengthen Security & Stability through integrating fuzzing-based security testing to identify and fix
   vulnerabilities in packet parsing and stream handling.

---

I want to highlight that this has been one of the most exciting projects I have ever worked on. I am deeply grateful to my mentors, Steve Lhomme and Jean-Baptiste Kempf, as well as the entire VLC community, for their continuous support and guidance throughout this journey. I learned a great deal from them, and I look forward to continuing this collaboration on this project and on VLC more broadly.
