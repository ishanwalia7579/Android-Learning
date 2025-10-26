# Android Camera App

This Android application demonstrates how to **open the device camera using an Intent**, capture an image, and display it inside the app.  

The app uses the `ACTION_IMAGE_CAPTURE` Intent of the `MediaStore` class and `FileProvider` to securely handle image files. Glide library is used to display images in an `ImageView`.  

---

## Features

- Open the camera from inside the app  
- Capture an image and store it temporarily  
- Display the captured image inside the app  
- Uses `FileProvider` for secure file sharing  
- Glide library for efficient image loading  

---

## Screenshots

![App Screenshot](screenshot.png) <!-- Replace with your actual screenshot -->

---

## Prerequisites

- Android Studio installed  
- Minimum Android SDK: 21 (Lollipop)  
- Kotlin support  

---

## Setup & Installation

1. **Clone the repository**  

```bash
git clone https://github.com/YourUsername/AndroidCameraApp.git
```
<ol type=1>
<li>Open the project in Android Studio</li>

<li>Add dependencies in build.gradle (Module: app)</li>

```kt
dependencies {
    implementation("com.github.bumptech.glide:glide:4.16.0")
}
```
<li>Update AndroidManifest.xml</li>

```xml
<provider
    android:name="androidx.core.content.FileProvider"
    android:authorities="${applicationId}.fileprovider"
    android:exported="false"
    android:grantUriPermissions="true">
    <meta-data
        android:name="android.support.FILE_PROVIDER_PATHS"
        android:resource="@xml/file_paths" />
</provider>
```
<li>Create file_paths.xml in res/xml</li>

```xml
<?xml version="1.0" encoding="utf-8"?>
<paths xmlns:android="http://schemas.android.com/apk/res/android">
    <cache-path name="images" path="images/" />
</paths>
```

<li>Run the app on a device or emulator with a camera</li>
</ol>

##  Usage
<ol type=1>
<li>Open the app.</li>
<li>Tap the “Open Camera” button.</li>
<li>Capture an image.</li>
<li>The captured image will appear in the <b>ImageView.</b></li>
</ol>


# Code Snippet

## Opening Camera and displaying image using Glide:
```kt
val cameraIntent = Intent(MediaStore.ACTION_IMAGE_CAPTURE).apply {
    putExtra(MediaStore.EXTRA_OUTPUT, photoUri)
    addFlags(Intent.FLAG_GRANT_WRITE_URI_PERMISSION)
}
startActivityForResult(cameraIntent, CAMERA_REQUEST_CODE)

```

## Load image in ImageView:
```kt
Glide.with(this).load(photoUri).into(clickedImage)

```

## License

This project is licensed under the MIT License.


```yaml

If you want, I can also make a **super short, GitHub-ready version with badges, 3-4 lines of features, and screenshot**, perfect for a clean repo look.  

Do you want me to make that too?

```
<p><strong><span style="color:red;">Developer Ishan Walia</span></strong></p>
