# Splash Screen (Definition & Details)

## ✅ 1. What is a Splash Screen?
A **splash screen** is the first screen that appears when a mobile app, game, or software is launched.  
It usually displays the **app logo, name, or an animation** for a few seconds before opening the main screen.

---

## ✅ 2. Why is a Splash Screen Used?

###  1. Branding  
Shows the app’s **logo, name, and identity** to create a strong first impression.

###  2. Hides Loading Time  
Covers the time while the app **loads resources, data, or initializes components**.

###  3. Improves User Experience  
Prevents **blank screens or lag** and provides a smooth opening.

###  4. Professional Presentation  
Gives the app a **clean, polished, and premium look**.

---

## ✅ 3. Where is a Splash Screen Used?

- Mobile Apps (Android/iOS)  
- Games  
- Desktop Software  
- Websites / Web Apps

---

## ✅ 4. How Long Does It Stay?
A splash screen generally shows for **1 to 3 seconds**, then redirects to the **Home Screen or Login Page**.

---

## ✅ 5. Examples of Splash Screens

- **YouTube** → Red/white logo screen  
- **WhatsApp** → Green background with logo  
- **Instagram** → Logo before feed  
- **Paytm / Flipkart / Facebook** apps

---

## ✅ 6. Benefits of a Splash Screen

- Builds **brand awareness**  
- Provides a **smooth app start**  
- Covers **loading delays**  
- Makes the app look **professional**

---

## ✅ 7. When Should You Use a Splash Screen?

Use it when:

- You want to show branding first  
- The app needs time to load data  
- You want to avoid blank screens  
- You want a clean startup experience

---

## ✅ 8. What Should a Good Splash Screen Include?

<li> App Logo</li>  
<li>App Name / Tagline</li>  
<li>Optional animation or loader </li> 
<li>Simple and clean design </li> 
<li>Short display duration</li>

---

##  ✅ 9. Code Example

###  `activity_splash.xml`
```xml
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:background="@color/white">

    <ImageView
        android:id="@+id/imgLogo"
        android:layout_width="150dp"
        android:layout_height="150dp"
        android:layout_centerInParent="true"
        android:src="@drawable/ic_app_logo"
        android:contentDescription="App Logo" />

    <TextView
        android:id="@+id/tvTag"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/imgLogo"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="12dp"
        android:text="Welcome to My App!"
        android:textSize="16sp" />
</RelativeLayout>
```
###  `SplashActivity.kt`
```kt
package com.example.myapp

import android.content.Intent
import android.os.Bundle
import android.os.Handler
import android.os.Looper
import androidx.appcompat.app.AppCompatActivity

class SplashActivity : AppCompatActivity() {

    private val SPLASH_TIME: Long = 2000 // 2 seconds

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_splash)

        supportActionBar?.hide() 

        Handler(Looper.getMainLooper()).postDelayed({
            startActivity(Intent(this, MainActivity::class.java))
            finish()
        }, SPLASH_TIME)
    }
}
```

### ✅ MainActivity.kt
```kt
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
    }
}
```

### ✅ AndroidManifest.xml
```xml
<application
    android:theme="@style/Theme.AppCompat.Light.NoActionBar">

    <activity
        android:name=".SplashActivity"
        android:exported="true">
        <intent-filter>
            <action android:name="android.intent.action.MAIN" />
            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>
    </activity>

    <activity android:name=".MainActivity" />
</application>
```
