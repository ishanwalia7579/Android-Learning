## How to Run the Android App on a Real Device?
The time comes when the Android Studio project is ready and you want to test that application. One can test the application by running the application which can be done in two ways.
<ol>
<li>By running the app on an Android Virtual Device(AVD), and</li>
<li>By running the app on a real device</li>
</ol>
So in this article, we are going to discuss how to run the Android app on a real device. So before running the app on a real device we have to set up the real device first. Set up your device as follows:

## Steps for Running the Android App on a Real Device
### Step 1: In the physical android device goto Settings -> About phone and then find the Build Number Option.
<img src="">

#### Step 2: Then one needs to tap the Build Number option fast until it shows, "No need, you are already a developer" as a Toast message.
<img src="">

#### Step 3: Go back to the Settings menu and search for the USB Debugging. And open the USB Debugging option.
<img src="">

#### Step 4: Then find the USB Debugging option and enable it. One alert dialogue pops up and you need to click "OK" and make sure that the developer option should be kept "on".
<img src="">

#### Step 5: Now open the android studio project and then connect the device to the PC using a suitable USB cable and if there are no USB drivers installed in your PC of your android device then you can google search and download and install the USB driver of the specific device model number.

#### Step 6: As soon as you connect the device, in the physical device, it asks to allow USB debugging for the PC you connected. Then you need to check "Always allow this computer", and hit the "Allow" button

<img src="">


### Step 7: Now you can see the device name under the Running devices list in Android Studio IDE. Select your device and then click on the Run Button, and the application you developed in Android Studio will be up and running. Following is the symbol of the Run button.
