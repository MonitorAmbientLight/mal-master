# Introduction to Monitor Ambient Light (MAL)

![mal_logo](/pictures/mal_logo.png)

The Monitor Ambient Light system (MAL) is a simple and inexpensive open source solution that enhances the immersion while playing games and watching movies and series on a monitor.  

This solution is based on the open source product [Hyperion](https://github.com/hyperion-project) and is intended to provide a quick and easy way to deploy ambient lights for monitors that anyone can use, with pre-built 3D models, instructions, parts list and pre-built images.  

The MAL system is interposed between the source and the output device via HDMI. The HDMI signal is analyzed by a Raspberry Pi via a capture card. The colors in the image signal indicate the colors of the LEDs, which light up according to the signal.  

Below you will find everything that is necessary to 3D print the case, assemble the MAL system and getting started with the software.  

![mal-case](/pictures/mal-case.jpeg)

## Table of content
**[Preparations / Requirements](https://github.com/MonitorAmbientLight/mal-master#preparations--requirements)**  

* [Hardware list](https://github.com/MonitorAmbientLight/mal-master#hardware-list)  
* [Software download](https://github.com/MonitorAmbientLight/mal-master#software-download)  
* [Printing the MAL case](https://github.com/MonitorAmbientLight/mal-master#printing-the-mal-case)  

**[Hardware assembly](https://github.com/MonitorAmbientLight/mal-master#hardware-assembly)**  

* [Assembling the MAL](https://github.com/MonitorAmbientLight/mal-master#assembling-the-mal)  
* [Assembling the LEDs to a monitor](https://github.com/MonitorAmbientLight/mal-master#assembling-the-leds-to-a-monitor)  
* [Connecting MAL to HDMI devices and the LED strips](https://github.com/MonitorAmbientLight/mal-master#connecting-mal-to-hdmi-devices-and-the-led-strips)  

**[Software deployment](https://github.com/MonitorAmbientLight/mal-master#software-deployment)**  
* [Deployment of the Raspberry Pi image](https://github.com/MonitorAmbientLight/mal-master#deployment-of-the-raspberry-pi-image)  
* [Installation of the MAL Remote app](https://github.com/MonitorAmbientLight/mal-master#installation-of-the-mal-remote-app)  

**[Quick Start Guide: Starting the MAL and MAL Remote App](https://github.com/MonitorAmbientLight/mal-master/blob/main/README.md#quick-start-guide-starting-the-mal-and-mal-remote-app)**  

# Preparations / Requirements
In order to assemble the system and get started, you need some hardware components and software.  
To ensure compatibility, you should use the listed hardware and software.  
If you have advanced knowledge you can of course use other parts and modify them as you like.

> You are not bound to use the MAL case. You can either design your own case, use ours or use all parts in an open setup. **The last solution is only suitable for a first test.**

## Hardware list

Use the provided MAL Hardware list in the [parts folder](/parts) to get every needed part together for this project.  
We can not guarantee the availability of each part in your region.  
You might have to find equivilant substitutes.  

## Software download

### Image for Raspberry Pi

Please download the MAL image that fits for you needs from the [mal-images](/mal-images) folder.  
The image will be used to install it onto a SD card.  
The naming scheme is as follows:  

mal-image_[TV-SIZE]-inch.exe  

> **For example:** If you have a display with a diagonal size of 40 inch you will need the image with the name **mal-image_40-inch.exe**

### MAL Remote App

**WORK IN PROGRESS**  

## Printing the MAL case

You can either print the case by yourself or use an 3D printing service.  
The corresponding files are in the [3dmodels folder](/3dmodels):  
  
- mal-base.stl
- mal-cable-strain-relief.stl
- mal-capture-card-mount.stl
- mal-top-cover.stl
  
As we can only use FDM printers by now we can only advice you to use the following print settings:  
  
Resolution: 0.2 mm  
Supports: no  
Infill: 15 %  
Print speed: 70 mm/s  

You can either use PETG or PLA in any desired color as your printing material. Any other material like ABS should be also no problem.  
> Don't use a soft plastic like TPU or conductive material.  

# Hardware assembly
The following sections will guide you through the process to get the hardware assembled and ready so that we can then deploy the software.
You can also watch the assembling video here: [Assembling the MAL system](https://youtu.be/FyggdWm1GQ4)

## Assembling the MAL
### Step 1

Have the breadboard and the oblong microcontroller ready.  
![01](/pictures/01.jpeg)

Now put the microcontroller in the horizontal center of the white breadboard, so that the nose or cutout (yellow marker) on the controller points to the center of the breadboard.  
![02](/pictures/02.jpeg)

Now pull off the cover foil of the adhesive pad on the bottom side of the breadboard. Glue the breadboard into the MAL case (3D Model: mal-base) so that it rests against the wall (yellow marker) and the horizontal edge is about 1.5 centimeters away from the lower wall (orange marker).  
![03](/pictures/03.jpeg)

### Step 2

Now take the 4-core cable with the black plug and push it through the rectangular hole where the two side-by-side glands are located, so that the exposed wire ends protrude about 2 centimeters behind the gland and screw down the strain relief (3D model: mal-cable-strain-relief) with two 2,5 mm screws (yellow marker).  
![04](/pictures/04.jpeg)

The intermediate result should now look like this:  
![05](/pictures/05.jpeg)

### Step 3

Have the round hollow plug with the black and red cable, the corresponding nut and a plier or a suitable wrench ready.  
![06](/pictures/06.jpeg)

Now take the hollow plug and insert it with the cables first from the outside of the MAL case through the round hole near the breadboard, so that the black plastic of the hollow plug is flush with the wall of the MAL case.  
Now use the nut to hand-tighten the hollow connector from the other side.  
![07](/pictures/07.jpeg)

### Step 4

Have the following plug cables ready:  
  
One male and one female end:  
- 1x white
- 1x red
- 1x green
  
Male on both ends:  
- 1x white
- 1x blue

![08](/pictures/08.jpeg)

Now plug the blue cable into the last row of the breadboard at the height of the third pin of the microcontroller (seen from the direction of the nose or cutout of the microcontroller).  
![09](/pictures/09.jpeg)

Then take the green cable and plug with the male end at the next left position right after the blue cable. The green cable should now at the height of the second pin of the microcontroller.  
![10](/pictures/10.jpeg)

The next cable is the white cable with one male and one female end.  
Plug the male side on the next left position right after the green cable so that the white cable is now on the horizontal height of the very last pin of the microcontroller (on the side of the nose or cutout of the microcontroller).  
![11](/pictures/11.jpeg)

Now we need the red cable (be sure to use the plug cable not the red cable from the hollow plug). Plug this on the mirrored position of the white cable which we just plugged in.  
![12](/pictures/12.jpeg)

Take the black cable from the hollow plug and plug it into the very last position on the right hand side of the breadboard (on the row of the other 3 plugged in cables).  
![13](/pictures/13.jpeg)

The last cable is the white cable with both male ends.  
Plug the end in the very next vertical position after the last plugged in black cable.  
![14](/pictures/14.jpeg)

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

### Step 5

Have three of the Wago clamps ready.  
![15](/pictures/15.jpeg)

Use one Wago clamp for the red and one Wago clamp for the white cable which you installed in Step 2. Clamp the ends of the cables in the Wago clamp.  
![16](/pictures/16.jpeg)

For the green and blue cables use only one Wago clamp and clamp the ends together.  
![17](/pictures/17.jpeg)

Now take the red cable coming from the hollow plug and clamp it in the Wago clamp which is connected to the other red cable. Also take the white cable from Step 4 with both male ends and clamp in together with the other white cable. The blue cable from Step 4 will now be clamped together with the other blue and green cable.  
![18](/pictures/18.jpeg)

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

### Step 6

Have the Raspberry Pi and three 2,2 mm screws ready.  
![19](/pictures/19.jpeg)

Place the Raspberry Pi on the intended place in the MAL case.  
![20](/pictures/20.jpeg)

Secure the Raspberry Pi with the three 2,2 mm screws.
![21](/pictures/21.jpeg)

Now connect the red, white and green cable from Step 4 with the female end to the Raspberry Pi as shown:
![22](/pictures/22.jpeg)

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

### Step 7

Have the black capture card and the corresponding USB A 3.0 to USB A 3.0 cable as well as the capture card mount (3D Model: mal-capture-card-mount) with one 2,5 mm screw ready.
![23](/pictures/23.jpeg)
![24](/pictures/24.jpeg)

Place the capture card in the intended place. Be sure that the orientation is correct. The two HDMI ports must be fully accessible from the outside of the MAL case.  
Now secure the capture card with the capture card mount and the screw.
![25](/pictures/25.jpeg)

Finally connect the capture card with the Raspberry Pi with the USB cable.  
Be sure to use the upper middle USB port of the Raspberry Pi.  
![26](/pictures/26.jpeg)

### Step 8

The very last step of the assembly of the MAL is to screw down the top cover on the case.  
Take the top cover (3D model: mal-top-cover) and four 2,5 mm screws.  
![27](/pictures/27.jpeg)

The final result should look like this:
![28](/pictures/28.jpeg)

## Assembling the LEDs to a monitor
### Cutting the LED strip

Each LED strip has segments. The segments are separated by four solder / connector points (copper plates between the LEDs).
You will have to cut the LED strip at the right length with a scissor so that you can then apply these to your monitor or TV.

> **Attention:** Be sure that these LED strip have a fixed direction. You will find arrows printed on the strips. The direction is important when you cut the LED strip and apply these to your display. Make sure the arrows show in the same direction starting from the feed point to the end of the strip.

![35](/pictures/35.jpeg)

As we only supports fixed display sizes we advice you to use our **MAL LED strip cheat sheet** in the [instructions folder](/instructions). This document
will tell you after how many LEDs you will have to do each cut. The cheat sheet will be updated in the future to support more display sizes.

> **For example:** You have a display with a diagonal size of 40 inch. You will need two vertical and two horizontal LED strips. According to our cheat sheet you will need two LED strips for the vertical part with a length of 29 LEDs and two LED strips for the horizontal part of your display with a length of 51 LEDs.

Search for the feed point where the LED strip will be connected to the 4 pin cable that sticks out of the MAL case.
The feed point is the same cable as the 4 pin cable of the MAL case. It has 4 pins at the end.

![36](/pictures/36.jpeg)

The feed point will start at the lower right point of your display (seen from the back of the display) and will then go upwards to the horizontal line.
Now take the MAL LED strip cheat sheet and search for you the column **Display size in inch** and search for the row with the display size of your monitor / TV. The next column shows you the **Vertical LED count**. This is the measure you need to now count starting from the 4 pin connector until you reach the LED count shown in the according cell.  
Then take the scissor and carefully cut the strip at the copper plated segments.  
  
Repeat the step for the other vertical LED strip. As a help you can now take the first LED strip at hold it side by side.  
You can then just cut at the right count as you already have the right length.  

You now have both LED strips for the vertical part of your display.  
Repeat the process for the horizontal LED strips. Have a look in the MAL LED strip cheat sheet and search for the column **Horizontal LED count**.  

At the end you will have a total of four LED strips. Two shorter (with one having the 4 pin connector at the start) and two longer strips.  

### Applying the LED strips to the display

After you cut all the LED strips you can now apply the strips to your display.  
Begin with the vertical (shorter) LED strip with the 4 pin connector at the start.  
This LED strip will be glued to the right side of the display. The connector must be at the bottom.  

You can then take the longer strip which is indended to be placed at the top of the display.
Next glue the last shorter LED strip on the left side of the display.  
Finally you can take the last longer strip and apply it to the bottom side of the display.  

> **Attention:** Be sure that these LED strip have a fixed direction. You will find arrows printed on the strips. The direction is important when you cut the LED strip and apply these to your display. Make sure the arrows show in the same direction starting from the feed point to the end of the strip.

The final result will look like this:  

![37](/pictures/37.jpeg)

### Connect each LED strip

To finalize your work at your display you will now connect every LED strip with the 4 pin corner LED strip connectors.

![31](/pictures/31.jpeg)

## Connecting MAL to HDMI devices and the LED strips
### HDMI
Any device which you want to use with the MAL needs to be connected through the MAL to your monitor.  
As an input device you can use any HDMI capable device with a maximum resolution of 3840x2160 and a refresh rate of 60 Hz.  
If the audio needs to be send through HDMI this is no problem with the MAL as the audio will be passed through.  

> **For example:** If you want to use a XBOX Series One console with your TV and MAL, the XBOXs HDMI output needs to be connected to the input of the MAL. The output of the MAL needs to be connected with your TV.

- Left: HDMI output
- Right: HDMI input

![29](/pictures/29.jpeg)
![32](/pictures/32.jpeg)

### LED strips
Connect both ends of the 4 pin cables of the MAL with the LED strip.

![33](/pictures/33.jpeg)

### Power the LEDs and the Raspberry Pi

To power the LEDs and the Raspberry Pi you will now have to take the DC 12 V power supply with the hollow plug and the USB-C power supply ready.
Connect the USB-C power supply with the left USB-C port at the MAL case and the DC 12 V power supply with the hollow plug on the right side.

![34](/pictures/34.jpeg)

You MAL system is now ready to be deployed with the MAL software.

# Software deployment
## Deployment of the Raspberry Pi image

1. To deploy an IMG File from one of our preconfigured [MAL-Images](/mal-images), you need to have the Raspberry Pi Imager installed. It is available for download [here](https://www.raspberrypi.com/software/).
2. To deploy the IMG File to a SD card, start the Raspberry Pi Imager and select the downloaded IMG File as OS-Image. Now select your injected SD card and additionaly click on the settings wheel located at the bottom right corner.
3. Set the hostname to "raspberrypi", select an individual username and unique password (you do not need it, unless you want to make changes within the OS itself). Set the WiFi-SSID to your local WiFi Name and enter the according password. You may also set your local timezone and keyboard layout.
4. After installing the image on the SD card, your MAL Application is ready to run once you inject it into the Raspbery Pi.

## Installation of the MAL Remote App

### How to Install MAL-APK file on ANY Android

**Introduction:**
APK files are Android application packages used to install apps on Android devices. This guide will walk you through the process of installing MAL-APK file on your Android device.

**Requirements:**
- An Android smartphone or tablet

### Instructions:

1. **Download the APK file:**
   - Using your Android device, download the MAL.apk file from the [apk-file folder](/apk-file).

2. **Access the file directory:**
   - Open the "My Files" or "Files" app on your Android device. The name may vary depending on your device.

3. **Locate the downloaded APK file:**
   - Navigate to the "Downloads" folder or directly to the "APKs" folder, depending on your device's file organization.

4. **Select the APK file:**
   - Tap on the downloaded MAL.apk file.

5. **Enable installation from unknown sources:**
   - A notification will appear, stating, "For your security, your phone isn't allowed to install unknown apps from this          source. You can change this in Settings."
   - Tap on the notification to open Settings.
   - Toggle on the "Allow from this source" option.

6. **Confirm the installation:**
   - The installation prompt will reappear.
   - Press the "Install" button to begin the installation process.

7. **Complete the installation:**
   - Wait for the installation process to finish. This may take a few moments.

8. **Choose the next step:**
   - Once the installation is complete, you can either press "Done" to exit the installer or "Open" to launch the newly           installed app.

**Congratulations!** You have successfully installed the MAL app on your Android device. You can now use the app and explore its features.

## Quick Start Guide: Getting Started with the MAL App

The MAL App provides a user-friendly interface for controlling your MAL-Hardware. This Quick Start Guide will help you navigate through the app and make the most of its features.

### 1. Connecting to the MAL-Hardware

- On the home page, you'll find an input field where you can enter the Hyperion IP address associated with your MAL-Hardware. Alternatively, you can simply click on the 'Detect MAL-Hardware' button to automatically connect to the corresponding hardware.

<img src="/pictures/Page1.png" alt="Page1" style="width:228px;"/>

### 2. Exploring the Pages

The main page of the MAL App consists of three buttons, each providing access to different settings:
- Color Adjustment
- Colors/Effects
- Settings

<img src="/pictures/Page2.png" alt="Page2" style="width:228px;"/>

- **Color Adjustment:** This page allows you to adjust the brightness, light colors and gamma values according to your personal preferences. You'll find various buttons to save changes, reset values to default, or return to the main page.

![Page3](/pictures/Page3.png)

- **Colors/Effects:** On this page, you can set the light to a specific color or enable different effects. Additionally, you'll find buttons to save changes, reset values to default, or return to the main page.

![Page4](/pictures/Page4.png)

- **Settings:** The settings page offers several toggle buttons, including effects, smoothing and LED lights. There is also a timer input field where you can specify the minutes after which the lights should automatically turn off. Save your changes or return to the main page using the provided buttons. Additionally, there is a "Clear" button that allows you to clear your app storage.

![Page5](/pictures/Page5.png)

We hope this Quick Start Guide helps you navigate through the MAL App and control your MAL-Hardware effortlessly. 
<br>**Enjoy your lighting experience!**
