# TimePicker
<p>The Android TimePicker is a user interface component that allows users to select a specific time in either a 24-hour format or an AM/PM format. It ensures users input valid times within an application. TimePicker provides two display modes:
</p>
<ol type="1">
<li><b>Clock Mode:</b> Displays an analog clock-style interface for time selection.</li>
<li><b>Spinner Mode:</b> Presents hour and minute values in a scrollable spinner format.</li>
</ol>
Ways to Implement TimePicker in Android

<ol type="1">
<li><b>XML Layout: Define the TimePicker directly in the layout file.</li>
<li><b>Programmatically: </b>Dynamically create and configure the TimePicker in a Kotlin file.</li>
</ol>

## Important Attributes of TimePicker

| XML Attribute           | Description |
|-------------------------|-------------|
| `android:timePickerMode` | Used to specify the mode of TimePicker (`spinner` or `clock`) |
| `android:background`     | Used to set the background color of the view |


## Step 1: Create a new project in Android Studio
Below are the steps to be followed:
<ol>
<li>Click on File, then New => New Project.</li>
<li>After that include the Kotlin support and click on next.</li>
<li>Select the minimum SDK as per convenience and click next button.</li>
<li>Then select the Empty activity => next => finish.</li>
</ol>

## Step 2: Adding TimePicker widget in Layout file
We can use android:timePickerMode to choose which the mode for the TimePicker. The possible values are "clock" and "spinner". This article demonstrate how to implement both type of modes.

## activity_main.xml:
# Spinner Mode
```xml
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/white"
    tools:context=".MainActivity">

    <TimePicker
        android:id="@+id/timePicker"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:padding="24dp"
        android:timePickerMode="spinner"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="24dp"
        android:textSize="18sp"
        android:text="Time is: "
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/timePicker" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
# Clock mode
```xml
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/white"
    tools:context=".MainActivity">

    <TimePicker
        android:id="@+id/timePicker"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:padding="24dp"
        android:timePickerMode="clock"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="24dp"
        android:textSize="18sp"
        android:text="Time is: "
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/timePicker" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
<img src="TimePicke.png">

# Step 3: Access the TimePicker in MainActivity.kt file
First of all, we declare two variables textView and timePicker to access the widgets from the XML layout using their id's.
```
val textView = findViewById(R.id.textView)
val timePicker = findViewById(R.id.timePicker)
```

Then, we set the setOnTimeChangedListener(), to detect when the time is changed
```
timePicker.setOnTimeChangedListener { view, hourOfDay, minute ->
    // your code here
}
```
# MainActivity.kt:
```kt
package org.geeksforgeeks.demo

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.view.ViewGroup
import android.widget.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val textView: TextView = findViewById(R.id.textView)
        val timePicker: TimePicker = findViewById(R.id.timePicker)

        timePicker.setOnTimeChangedListener { _, hour, minute ->
            var hour1 = hour
            var amPm = ""
            // AM_PM decider logic
            when {hour1 == 0 -> { hour1 += 12
                amPm = "AM"
            }
                hour1 == 12 -> amPm = "PM"
                hour1 > 12 -> { hour1 -= 12
                    amPm = "PM"
                }
                else -> amPm = "AM"
            }

            val hour2 = if (hour1 < 10) "0$hour1" else hour1
            val min = if (minute < 10) "0$minute" else minute
            // display format of time
            val msg = "Time is: $hour2 : $min $amPm"
            textView.text = msg
            textView.visibility = ViewGroup.VISIBLE
        }
    }
}
```
