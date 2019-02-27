# DTWSpells_Eric

Eric Minor

The goal is to transform my backscratcher into a magical wand.

This was accomplished by rubber banding a microbit to my backscratcher and making that microbit transmit
its x,y,z accelerations with radio signals to another microbit which then fed the signals to a python script.
The Python script in turn sends the accelerations as OSC messages to wekinator in order to build a dynamic time
warping model.

I initially tried the gestures of moving the wand up and down. Although the model was able to successfully identify
the gestures, it was difficult to move down without needing to also move up. This caused up to be identified
between down gestures, and vice versa.

I then realized the best gesture to use with my magic wand was a scratching gesture. Scratching one's back and 
scratching one's belly are two very unique gestures, with movement patterns that don't overlap much.
Using these two gestures, along with a  third 'motionless' gesture, I found the model was able to successfully
identify whether I was scratching my belly, my back, or not at all with little to no error.

Others might improve my work by adding more scratching locations

My spell names are:
back scratch
belly scratch

video: https://youtu.be/6LCYH_EzBP4

Usage:

Open the wekinator model backScratch and run it.
Open and run the processing script Processing_TriggerText_1DTW.pde
It is not the default processing script by that name, but a modified version.
Changing the name caused it to fail to display images for reasons unknown
microbit-transmitter (10).hex onto a microbit and attach the battery and microbit to magical wand
load microbit-Receiver (9).hex onto a microbit and keep the microbit plugged in via usb
run the python script wand_to_osc.py

The processing script should now output an image relating to what you are scratching.