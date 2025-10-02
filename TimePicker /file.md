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
<img src="TimePicker.png">
