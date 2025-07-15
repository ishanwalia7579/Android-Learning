### 1. What is Android ?
Android is a mobile operating system developed by Google, based on the Linux kernel, designed mainly for touchscreen devices like smartphones and tablets.
It provides a user-friendly interface and supports millions of mobile apps available through the Google Play Store.

### 2. How Android Works ?
Android works using a layered architecture, where each layer has a specific role — starting from controlling hardware to running user-facing apps.

 <ul><b>1. Linux Kernel (Lowest Layer)</b><ul>
<li>Acts as the heart of Android OS.</li>
<li>Controls hardware like camera, battery, Bluetooth, memory, Wi-Fi, etc.</li>
<li>Ensures security, process management, and driver communication.</li></ul></ul>

<ul><b>2. Android Runtime (ART)</b>
Responsible for executing your app's code.<ul>
<li>It includes the core libraries (like Java SDK).</li>
<li>Converts your Java/Kotlin code into machine-readable format using Ahead-Of-Time (AOT) compilation.</li>
<li>Replaced the older Dalvik VM for better performance.</li>
</ul>
</ul>
<ul>
 <b> 3. Native Libraries</b>
<ul>Collection of C/C++ libraries built on top of the Linux kernel.
Examples:
<li>SQLite – Database</li>
<li>WebKit – Browser engine</li>
<li>Media – Audio/video playback</li>
<li>OpenGL – Graphics rendering</li>
These libraries help Android apps use complex features easily.
</ul>
</ul>
<ul><b>
4. Application Framework</b><ul>
<li>This is the layer developers interact with.</li>
<li>Provides ready-to-use APIs to access phone features like:</li>
<li>Activity Manager – app lifecycle</li>
<li>Notification Manager – push notifications</li>
<li>View System – UI design</li>
<li>Location Manager – GPS-based services</li>
</ul>
</ul>

<ul><b>5. Applications Layer (Top Layer)</b><ul>
<li>This is where all the user-installed apps live.</li>
<li>Apps like WhatsApp, Instagram, YouTube, Calculator, etc.</li>
<li>These apps are built on top of all the lower layers and interact with them using the Application Framework.</li>
</ul>
</ul>

### 3. How to Install Android Studio
<ul>
<li>1. Visit: https://developer.android.com/studio</li>
<li>2. Download Android Studio </li>
<li>3. Install Java JDK if required</li>
<li>4. Install and launch Android Studio</li>
<li>5. Create a new project with “Empty Activity”</li>
<li>6. Start coding in Java or Kotlin</li>
</ul>

### 4. Basic Structure of an Android App

<ul><b>1. java/ or kotlin/ folder</b><ul>
<li>Stores your app’s source code files.</li>
<li>Contains all Activities, Fragments, and business logic.</li>
<li>Example: MainActivity.java or MainActivity.kt</li>
</ul>
</ul>

<ul><b>2. res/layout/</b><ul>
<li>Stores all your XML UI design files.</li>
<li>Example: activity_main.xml → designs buttons, text, layouts.</li>
<li>These files define how the app looks on screen.</li>
</ul>
</ul>


<ul><b>3. res/drawable/</b><ul>
<li>Stores images, icons, logos, shapes, etc.</li>
<li>You can use PNG, JPG, SVG, or XML </li>
<li>drawable files here.</li>
</ul>
</ul>

<ul><b>4. res/values/</b><ul>
<li>Stores reusable data like:</li>
<li>strings.xml → app texts (good for localization)</li>
<li>colors.xml → theme colors</li>
<li>styles.xml → app themes</li>
<li>Helps in managing app design consistently.</li>
</ul>
</ul>

<ul><b>5. AndroidManifest.xml</b><ul>
<li>The main configuration file of the app.</li>
<li>Declares:</li>
<li>App name, icon</li>
<li>All Activities</li>
<li>Permissions (camera, location, etc.)</li>
<li>App launcher info</li>
</ul>
</ul>

<ul><b>6. build.gradle</b><ul>
<li>This file tells Android Studio:</li>
<li>Which SDK version to use</li>
<li>Which libraries to include (e.g., Firebase, Glide)</li>
<li>Helps to build and run the app properly.</li>
</ul>
</ul>
