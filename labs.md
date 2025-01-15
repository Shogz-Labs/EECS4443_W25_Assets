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

### Lab 1 (Demo_Android)
1. I keep getting errors when importing **Demo_Android**! The app won't event run.... 

    **TA Response:** Firstly, please make sure that you have downloaded the lab from [here](https://github.com/yorku-ease/EECS4443-Demos). The older source is known to have problems with newer versions of Android Studio.

    If the bugs persist, please do the following and let me know if you are still facing difficulties:

    - Upgrade Gradle to the recommended version
    - Upgrade the dependencies as suggested by the Android SDK Update Assistant
    - Sync Project with Gradle Files 
    - Rebuild the Project 

2. I see that Task 5 asks for source-code comments. To what extent should I be documenting my code?

    **TA Response:** You should use **in-line** comments for any small modifications that you make to the existing Java code (e.g., New Variables, Connecting an Event Listener). 
    If you are adding new methods (e.g., implementing an interface and overriding method(s)), then you should use **Javadoc**. 

    Any modifications that you make to the layout or resources (e.g., String) should be documented using in-line style. 
    XML uses the same commenting style as HTML. See below:
    
    ```xml
        <!-- This is how we add comments in XML :) -->
    ```

    It would also be appreciated if you include a brief summary of what you implemented and how you did it in the header block comment which includes your name, student id, etc., 

3. Should I submit my Lab once it is checked off or is it okay to submit it prematurely?

    **TA Response:** If the application passes the demo and you have sufficiently documented your code, feel free to submit it before talking to me!
    However, some students in the past have had to make changes to their work in the lab sessions and forgot to re-submit the zip file. In such cases, you will lose marks for this. I recommend submitting your work once we have gone through it together to avoid this.

4. I'm completely lost. I've spent hours trying to do this lab and nothing is working...

    **TA Response:** Please reach out to the teaching team over Slack ASAP. You should post your questions in the general chat section so that everyone benefits! I'm sure other people are feeling the same way as you and have similar questions. **Please let us know what you have tried first.**

    Lastly, you can refer to [Demo_Elections.zip](https://github.com/Shogz-Labs/EECS4443_W25_Assets/blob/main/ta_recitations/demos/DemoElections.zip). Look at what I've done and use the documentation to understand how the code and xml work together.

### Lab 2 (Demo_Buttons)
1. I imported Demo_Buttons into Android Studio. Everything worked fine until I refactored the package and class names. I keep getting **java.lang.ClassNotFoundException**! Please help, what should I do!?

    **TA Response:** Please go to AndroidManifest.xml and ensure that **android:name** is properly defined in your activity tag. It should be, **".DemoButtons99999Activity"**.

2. My Views are being cropped when the Activity changes orientation. What should I do? Help!
    
    **TA Response:** You will either need to re-arrange the views in your defined horizontal layout (layout-land) or use a ScrollView as the top-most parent. 

3. What exactly do I need to save and restore?

    **TA Response:** Run the application and investigate what happens when you tap the widgets and change the screen orientation. You will find that certain View properties are natively managed by the Android OS. Don't save and restore states that are already supported.

4. I'm confused by Task 4 part 1. Can you please give me some clarification?

    **TA Response:** The window background colour of the activity should be changed to **#ff123456** without modifying the layout width or height of the LinearLayout. 
    
    To do this, please read the [documentation](https://developer.android.com/develop/ui/views/theming/themes) on applying **styles** to your Android application.   

5. Can you please elaborate on how complex my original feature should be?

    **TA Response:** Well.. You can't go wrong with adding a new image button... I tend to like creative and unique features!

    Please don't just change a property in the layout (XML) that does not add any substantial contributions to UI/UX.

6. I've spent hours trying to finish this lab... I'm at a complete loss of how to proceed.  What should I do?

    **TA Response:** Please take a ready through the [Demo_Layout](https://yorku-ease.github.io/EECS4443-Demos/Demo_Layout/index.html) and [Demo_Buttons](https://yorku-ease.github.io/EECS4443-Demos/Demo_Buttons/index.html) documentation. You can also benefit from reading about the [activity lifecycle](https://developer.android.com/guide/components/activities/activity-lifecycle). Pay special attention to **onSaveInstanceState(@NonNull Bundle savedInstanceState)** and **onRestoreInstanceState(@NonNull Bundle savedInstanceState)**.

### Lab 3 

1. TBD 

    **TA Response:** TBD

<hr> 