# ⏳ PulseCountDown in Android

This Android app demonstrates how to use the **PulseCountDown** library — a visually animated alternative to `CountDownTimer`.  
It can be used in **quiz apps, games, or timed challenges** to show a countdown with smooth pulse animations.

> ⚠️ **Note:** This library is no longer updated and may not work in the latest Android Studio versions.

---

## 📱 Features
- Simple pulse-style countdown animation  
- Easy to integrate with just one line of code  
- Fully customizable start and end values  
- Perfect for quizzes or timed tasks  

---

## 🧩 Step 1: Add Dependency

Open your `build.gradle (Module: app)` file and add:

```gradle
implementation ("com.gusakov:pulse-countdown:1.1.0-rc2")
```

## 🖼️ Step 2: activity_main.xml
```kt
<androidx.constraintlayout.widget.ConstraintLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/white"
    tools:context=".MainActivity">

    <com.gusakov.library.PulseCountDown
        android:id="@+id/pulseCountDown"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="5"
        android:textSize="100sp"
        app:pc_startValue="5"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"/> 

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="188dp"
        android:text="Start Countdown"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" /> 

</androidx.constraintlayout.widget.ConstraintLayout>
```
## 🧠 Step 3: MainActivity.kt
```
package org.geeksforgeeks.demo

import android.os.Bundle
import android.view.View
import android.widget.Toast
import androidx.appcompat.app.AppCompatActivity
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        // Start the countdown when button is clicked
        button.setOnClickListener(View.OnClickListener {
            pulseCountDown.start {
                // Show toast message when countdown ends
                Toast.makeText(this, "Course Alert!", Toast.LENGTH_LONG).show()
            }
        })
    }
}

```
## 👨‍💻 Developed by
<p style="color:blue; font-weight:bold;">Developer: Ishan Walia</p>

## 🏷️ Tags

Android PulseCountDown Kotlin Timer Animation QuizApp CountDownTimer
