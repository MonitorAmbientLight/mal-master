# Introduction to Monitor Ambient Light (MAL)

The Monitor Ambient Light system (MAL) is a simple and inexpensive open source solution that enhances the immersion while playing games and watching movies and series on a monitor.

This solution is based on the open source product Hyperion and is intended to provide a quick and easy way to deploy ambient lights for monitors that anyone can use, with pre-built 3D models, instructions, parts list and pre-built images.

The MAL system is interposed between the source and the output device via HDMI. The HDMI signal is analyzed by a Raspberry Pi via a capture card. The colors in the image signal indicate the colors of the LEDs, which light up according to the signal.

Below you will find everything that is necessary to 3D print the case, assemble the MAL system and getting started with the software.

# Preparations / Requirements
In order to assemble the system and get started, you still need some hardware components and software. To ensure compatibility, you should use the listed hardware and software. If you have advanced knowledge you can of course use other parts and modify them as you like.
## Hardware list

## Software download

## Printing the MAL case

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

# Hardware assembly
## Assembling the MAL
### Step 1

Have the white breadboard and the oblong microcontroller ready.
![01](/pictures/01.jpeg)

Now put the microcontroller in the horizontal center of the white breadboard, so that the nose or cutout (yellow marker) on the controller points to the center of the breadboard.
![02](/pictures/02.jpeg)

Now pull off the cover foil of the adhesive pad on the bottom side of the breadboard. Now glue the breadboard into the MAL case so that it rests against the wall (yellow marker) and the horizontal edge is about 1.5 centimeters away from the lower wall (orange marker).
![03](/pictures/03.jpeg)

### Step 2

Now take the 4-core cable with the black plug and push it through the rectangular hole where the two side-by-side glands are located, so that the exposed wire ends protrude about 2 centimeters behind the gland and screw down the strain relief with two hex screws (Part no. X) (yellow marker).
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
1x white
1x red
1x green

Male on both ends:
1x white
1x blue

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
Plug on end in the very next vertical position after the last plugged in black cable.
![14](/pictures/14.jpeg)

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

### Step 5

Have three of the Wago clamps ready.
![15](/pictures/15.jpeg)

Use one Wago clamp for the red and one Wago clamp for the white cable which you installed an secured in Step 2. Clamp the ends of the cables in the Wago clamp.
![16](/pictures/16.jpeg)

For the green and blue cables use only one Wago clamp and clamp the ends together.
![17](/pictures/17.jpeg)

Now take the red cable coming from the hollow plug and clamp it in the Wago clamp which is connected to the other red cable. Also take the white cable from Step 4 with both male ends and clamp in together with the other white cable. The blue cable from Step 4 will no be clamped together with the other blue and green cable.
![18](/pictures/18.jpeg)

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

### Step 6

Have the Raspberry Pi and three hex screws (Part No. Y) ready.
![19](/pictures/19.jpeg)

Place the Raspberry Pi on the intended place in the MAL case.
![20](/pictures/20.jpeg)

Secure the Raspberry Pi with the three screws.
![21](/pictures/21.jpeg)

Now connect the red, white and green cable from Step 4 with the female end to the Raspberry Pi als shown:
![22](/pictures/22.jpeg)

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

### Step 7

Have the black capture card the the corresponding USB A 3.0 to USB A 3.0 cable as well as the capture card holder with one hex screw (Part no. X) ready.
![23](/pictures/23.jpeg)
![24](/pictures/24.jpeg)

Place the capture card in the intended place. Be sure that the orientation is correct. The two HDMI ports must be fully accessible from the outside of the MAL case.
Now secure the capture card with the capture card holder and the screw.
![25](/pictures/25.jpeg)

Finally connect the capture card with the Raspberry Pi with the USB cable.
Be sure to use the upper middle USB port of the Raspberry Pi.
![26](/pictures/26.jpeg)

### Step 8

The very last step of the assembly of the MAL is to screw down the top cover on the case.
Take the top cover and four hex screws (Part no. X).
![27](/pictures/27.jpeg)

The final result should look like this:
![28](/pictures/28.jpeg)

## Assembling the LEDs to a monitor

## Connecting MAL to HDMI devices

Any device which you want to use with the MAL needs to be connected through the MAL to your monitor.

> **For example:** If you want to use a XBOX Series One with your TV and MAL, the XBOXs HDMI output needs to be connected to the input of the MAL. The output of the MAL needs to be connected with your TV.

Left: Input HDMI
Right: Output HDMI

![29](/pictures/29.jpeg)

As an input device you can use any HDMI capable device with a maximum resolution of 3680x2160 and a refresh rate of 60 Hz.

Use the left connector as the input.

# Software preparation
## 

