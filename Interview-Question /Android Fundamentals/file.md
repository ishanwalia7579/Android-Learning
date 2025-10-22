# 📱 Android Fundamentals

## 🧩 Q1. Explain Android Architecture and its Main Components

### 🧠 **Answer:**

Android Architecture is the basic design or structure of the Android operating system.  
It defines how different parts of the system — like hardware, applications, and system processes — work together so the device runs smoothly.  
It is built on **Linux**, which provides **security**, **memory management**, and **hardware control**.

Android Architecture is a layered structure that helps Android devices run efficiently. It connects the hardware (like camera or memory) with software (apps and system services) using layers such as Kernel, Libraries, Runtime, Framework, and Applications.

### 🏗️ **Main Layers of Android Architecture**

---

### 1️⃣ **Linux Kernel (Bottom Layer)**
- The foundation of Android OS.  
- Controls device hardware like **CPU, camera, memory, and sensors**.  
- Manages **security**, **memory**, and **processes** using built-in features like **SELinux**.  
- **Example:** When you take a photo, the kernel connects the software to the camera hardware.

---

### 2️⃣ **Hardware Abstraction Layer (HAL)**
- Acts as a **middleman** between hardware and software.  
- Ensures Android can run on different devices by using **standard interfaces** for components such as **Bluetooth, camera, and speakers**.  
- **Example:** The camera app doesn’t need to know the camera’s internal details — HAL handles it.

---

### 3️⃣ **Native Libraries**
- A set of **pre-built C/C++ code libraries** that perform complex tasks efficiently.  
- **Examples include:**  
  - `OpenGL` → Handles graphics  
  - `SQLite` → Stores data  
  - `WebKit` → Web browser engine  
- These libraries help apps perform heavy operations faster.

---

### 4️⃣ **Android Runtime (ART)**
- Converts app code into **machine code** using **AOT (Ahead-of-Time)** and **JIT (Just-in-Time)** compilation.  
- Improves **speed** and **performance** compared to the older Dalvik system.  
- Handles **Garbage Collection** to free unused memory automatically.

---

### 5️⃣ **Application Framework**
- Provides **tools and APIs** for developers to build Android apps.  
- Helps manage **app components**, **notifications**, and **background tasks**.  
- Key Managers:
  - `ActivityManager` → Controls app life cycle  
  - `NotificationManager` → Shows notifications  
  - `PackageManager` → Tracks installed apps  
  - `ContentResolver` → Shares data across apps

---

### 6️⃣ **Applications (Top Layer)**
- The layer users **see and interact with**.  
- Includes **built-in apps** like Contacts, Messages, Settings, and **user-installed apps**.  
- Every app runs in a **sandbox**, meaning it cannot access another app’s data unless given permission.

---

### 📊 **Android Architecture Overview**

