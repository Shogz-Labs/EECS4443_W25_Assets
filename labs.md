---
layout: page
title: Labs (FAQ)
description: Commonly asked questions + Hints about the lab
---

# Labs (FAQ)

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## General

1. I have installed Android Studio. How can I run my applications to ensure that they work properly?

    **TA Response:** There are two ways to run and debug your Android Applications:

    - **Android Emulator:** You can run and deploy your Android applications on a virtual device. Please consult the [comprehensive documentation](https://developer.android.com/studio/run/emulator) and ensure that your desktop or laptop meets the minimum system requirements.   
    - **Physical Device:** You will need to enable USB Debugging in order for your phone to be recognized by Android Studio. Again, please refer to the [documentation](https://developer.android.com/studio/run/device) first and let us know if you run into any other problems.

2. I have followed the Emulator setup instructions. It still doesn't work. Why?

    **TA Response:** This has been a commonly reported problem. Please ensure that your desktop/laptop has [virtualization](https://support.microsoft.com/en-us/windows/enable-virtualization-on-windows-c5578302-6e43-4b4b-a449-8ced115f58e1) enabled.
 
3. I'm really lost with Android Studio... Do you have a textbook reference for the course?

    **TA Response:** Please speak with the teaching team as soon as possible. We are here to help you and wish to see you succeed. I highly recommend the textbook, [Android Programming: The Big Nerd Ranch Guide (3rd)](https://www.amazon.ca/Android-Programming-Nerd-Ranch-Guide/dp/0134706056). It has comprehensive case-studies and all of the demos are written in Java.

4. It has been quite some time since I wrote Java... Do you have any references that could be helpful?

    **TA Response:** I found the textbook, [Introduction to Java Programming and Data Structures, Comprehensive Version (11th)](https://www.amazon.ca/Introduction-Programming-Structures-Comprehensive-Version/dp/0134670949) to be very helpful. Furthermore, this [YouTube playlist](https://www.youtube.com/playlist?list=PLFE2CE09D83EE3E28) by  [thenewboston](https://www.youtube.com/@thenewboston) is a great resource. I highly recommend it. 

5. I can't submit my lab as the zipped file size exceeds eClass limits! What should I do!?

    **TA Response:** Firstly, prior to zipping the file, please ensure that you have cleaned the project. This will reduce the file size significantly as your cached files are deleted. If you have done so already and the error still persists, please reach out to the teaching team.

6. My code appears to be correct, however, Android Studio is still throwing errors! What should I do!?

    **TA Response:** There are typically some problems that occur and persist when you add or delete resources. Synchronization problems can be traced to the R class, Manifest, or gradle changes. With that being said, you can generally solve most of these problems by:

    - **Build > Rebuild Project:** Cached files are deleted and the project is rebuilt from scratch. This often solves many problems.
    - **Sync Project with Gradle Files:** Click the elephant icon located in the top right corner. Problems occur here when you change build.gradle as everything goes out-of-sync.
    - **File > Invalidate Caches...:** Make sure to select all of the optional parameters and restart the IDE. Caches and indexes are deleted and the project is rebuilt reducing the likelihood of propagated errors.
    - If all else fails, then you need to use Android Lint, the debugger (e.g., breakpoints), and ensure that your XML files (e.g., layouts) are correct.   
<hr>

## Lab Questions & Hints

<hr>

### Lab 1 
1. TBD 

    **TA Response:** TBD

<hr> 