<p>Android architecture contains a different number of components to support any Android device's needs. Android software contains an open-source Linux Kernel having a collection of a number of C/C++ libraries which are exposed through application framework services. Among all the components Linux Kernel provides the main functionality of operating system functions to smartphones and Dalvik Virtual Machine (DVM) provide a platform for running an Android application.
</p>

## Components of Android Architecture
The main components of Android architecture are the following:-

<ol>
<li>Applications</li>
<li>Application Framework</li>
<li>Android Runtime</li>
<li>Platform Libraries</li>
<li>Linux Kernel</li>
</ol>

Pictorial representation of Android architecture with several main components and their sub-components
<img src="Android_Architecture.webp">
<p>Understanding Android's architecture is essential for building efficient applications. For those looking to master this structure and move from beginner to advanced skills in Kotlin, the Android Mastery with Kotlin: Beginner to Advanced course offers a comprehensive guide</p>

1. Applications
Applications is the top layer of android architecture. The pre-installed applications like home, contacts, camera, gallery etc and third party applications downloaded from the play store like chat applications, games etc. will be installed on this layer only. It runs within the Android run time with the help of the classes and services provided by the application framework.
<img src="">
2. Application framework
The Application Framework is a core part of Android that gives developers the tools and services they need to build apps. It provides access to device features like hardware, screen display, and system resources. It includes several important services that make it easier to build powerful and consistent Android apps without having to create everything from scratch. The services are as follows:

Activity Manager - Manages the app’s activities and their life cycle (like opening, pausing, or closing screens).
Notification Manager - Allows apps to show alerts or updates to the user.
Package Manager - Keeps track of all the apps installed on the device.
<img src="">

3. Application runtime
Android Runtime environment is one of the most important part of Android. It contains components like core libraries and the Dalvik virtual machine(DVM). Mainly, it provides the base for the application framework and powers our application with the help of the core libraries. Like Java Virtual Machine (JVM), Dalvik Virtual Machine (DVM) is a register-based virtual machine and specially designed and optimized for android to ensure that a device can run multiple instances efficiently. It depends on the layer Linux kernel for threading and low-level memory management. The core libraries enable us to implement android applications using the standard JAVA or Kotlin programming languages.
<img src="">

4. Platform libraries
The Platform Libraries includes various C/C++ core libraries and Java based libraries such as Media, Graphics, Surface Manager, OpenGL etc. to provide a support for android development.

<b>Media </b>library provides support to play and record an audio and video formats.
<b>Surface manager</b> responsible for managing access to the display subsystem.
<b>SGL</b> and <b>OpenGL </b>both cross-language, cross-platform application program interface (API) are used for 2D and 3D computer graphics.
SQLite provides database support and FreeType provides font support.
Web-Kit This open source web browser engine provides all the functionality to display web content and to simplify page loading.
SSL (Secure Sockets Layer) is security technology to establish an encrypted link between a web server and a web browser.
Window Manager - Handles the placement and appearance of windows on the screen.
Content Providers - Help apps share data with other apps (like contacts or photos).
View System - Controls how things (like buttons or text) appear on the scree
