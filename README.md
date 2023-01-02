# Overview

The MonitorAmbientLight system (MAL) is a simple and inexpensive open source solution that enhances the immersion while playing games and watching movies and series on a monitor.

This solution is based on the open source product Hyperion and is intended to provide a quick and easy way to deploy ambient lights for monitors that anyone can use, with pre-built 3D models, instructions, parts list and pre-built images.

Below you will find everything that is necessary for this.

# Preparations / Requirements
In order to assemble the system and get started, you still need some hardware components and software. To ensure compatibility, you should use the listed hardware and software. If you have advanced knowledge you can of course use other parts and modify them as you like.
## Hardware list

## Software download

## Printing the MAL case

StackEdit stores your files in your browser, which means all your files are automatically saved locally and are accessible **offline!**

# Hardware assembly
## Assembling the MAL
 **Step 1**
Have the white breadboard and the oblong microcontroller ready.
![alt text](://github.com/MonitorAmbientLight/mal-master/blob/main/pictures/01.jpg?raw=true)

Now put the microcontroller in the horizontal center of the white breadboard, so that the nose or cutout (yellow marker) on the controller points to the center of the breadboard.
02

Now pull off the cover foil of the adhesive pad on the bottom side of the breadboard. Now glue the breadboard into the MAL case so that it rests against the wall (yellow marker) and the horizontal edge is about 1.5 centimeters away from the lower wall (orange marker).
03

**Step 2**
Now take the 4-core cable with the black plug and push it through the rectangular hole where the two side-by-side glands are located, so that the exposed wire ends protrude about 2 centimeters behind the gland and screw down the strain relief with two hex screws (Part no. X) (yellow marker).
04

The intermediate result should now look like this:
05

**Step 3**
Have the round hollow plug with the black and red cable, the corresponding nut and a plier or a suitable wrench ready.
06

Now take the hollow plug and insert it with the cables first from the outside of the MAL case through the round hole near the breadboard, so that the black plastic of the hollow plug is flush with the wall of the MAL case.
Now use the nut to hand-tighten the hollow connector from the other side.
07

**Step 4**
Have the following plug cables ready:

One male and one female end:
1x white
1x red
1x green

Male on both ends:
1x white
1x blue

08

Now plug the blue cable into the last row of the breadboard at the height of the third pin of the microcontroller (seen from the direction of the nose or cutout of the microcontroller).
09

Then take the green cable and plug with the male end at the next left position right after the blue cable. The green cable should now at the height of the second pin of the microcontroller.
10

The next cable is the white cable with one male and one female end.
Plug the male side on the next left position right after the green cable so that the white cable is now on the horizontal height of the very last pin of the microcontroller (on the side of the nose or cutout of the microcontroller).
11

Now we need the red cable (be sure to use the plug cable not the red cable from the hollow plug). Plug this on the mirrored position of the white cable which we just plugged in.
12

Take the black cable from the hollow plug and plug it into the very last position on the right hand side of the breadboard (on the row of the other 3 plugged in cables).
13

The last cable is the white cable with both male ends.
Plug on end in the very next vertical position after the last plugged in black cable.
14

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

**Step 5**
Have three of the Wago clamps ready.
15

Use one Wago clamp for the red and one Wago clamp for the white cable which you installed an secured in Step 2. Clamp the ends of the cables in the Wago clamp.
16

For the green and blue cables use only one Wago clamp and clamp the ends together.
17

Now take the red cable coming from the hollow plug and clamp it in the Wago clamp which is connected to the other red cable. Also take the white cable from Step 4 with both male ends and clamp in together with the other white cable. The blue cable from Step 4 will no be clamped together with the other blue and green cable.
18

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

**Step 6**
Have the Raspberry Pi and three hex screws (Part No. Y) ready.
19

Place the Raspberry Pi on the intended place in the MAL case.
20

Secure the Raspberry Pi with the three screws.
21

Now connect the red, white and green cable from Step 4 with the female end to the Raspberry Pi als shown:
22

Be sure to review your work and compare it with the pictures as this step is necessary for a functional MAL solution. **A wrong cabling may destroy parts or the whole solution.**

**Step 7**
Have the black capture card the the corresponding USB A 3.0 to USB A 3.0 cable as well as the capture card holder with one hex screw (Part no. X) ready.
23
24

Place the capture card in the intended place. Be sure that the orientation is correct. The two HDMI ports must be fully accessible from the outside of the MAL case.
Now secure the capture card with the capture card holder and the screw.
25

Finally connect the capture card with the Raspberry Pi with the USB cable.
Be sure to use the upper middle USB port of the Raspberry Pi.
26

**Step 8**
The very last step of the assembly of the MAL is to screw down the top cover on the case.
Take the top cover and four hex screws (Part no. X).
27

The final result should look like this:
28

## Assembling the LEDs to a monitor

## Connecting MAL to HDMI devices

# Software preparation
## 
The file explorer is accessible using the button in left corner of the navigation bar. You can create a new file by clicking the **New file** button in the file explorer. You can also create folders by clicking the **New folder** button.

## Switch to another file

All your files and folders are presented as a tree in the file explorer. You can switch from one to another by clicking a file in the tree.

## Rename a file

You can rename the current file by clicking the file name in the navigation bar or by clicking the **Rename** button in the file explorer.

## Delete a file

You can delete the current file by clicking the **Remove** button in the file explorer. The file will be moved into the **Trash** folder and automatically deleted after 7 days of inactivity.

## Export a file

You can export the current file by clicking **Export to disk** in the menu. You can choose to export the file as plain Markdown, as HTML using a Handlebars template or as a PDF.


# Synchronization

Synchronization is one of the biggest features of StackEdit. It enables you to synchronize any file in your workspace with other files stored in your **Google Drive**, your **Dropbox** and your **GitHub** accounts. This allows you to keep writing on other devices, collaborate with people you share the file with, integrate easily into your workflow... The synchronization mechanism takes place every minute in the background, downloading, merging, and uploading file modifications.

There are two types of synchronization and they can complement each other:

- The workspace synchronization will sync all your files, folders and settings automatically. This will allow you to fetch your workspace on any other device.
	> To start syncing your workspace, just sign in with Google in the menu.

- The file synchronization will keep one file of the workspace synced with one or multiple files in **Google Drive**, **Dropbox** or **GitHub**.
	> Before starting to sync files, you must link an account in the **Synchronize** sub-menu.

## Open a file

You can open a file from **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Open from**. Once opened in the workspace, any modification in the file will be automatically synced.

## Save a file

You can save any file of the workspace to **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Save on**. Even if a file in the workspace is already synced, you can save it to another location. StackEdit can sync one file with multiple locations and accounts.

## Synchronize a file

Once your file is linked to a synchronized location, StackEdit will periodically synchronize it by downloading/uploading any modification. A merge will be performed if necessary and conflicts will be resolved.

If you just have modified your file and you want to force syncing, click the **Synchronize now** button in the navigation bar.

> **Note:** The **Synchronize now** button is disabled if you have no file to synchronize.
