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

### MAL Remote App

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

## Installation of the MAL Remote App

