# Create a Moving Virtual Donut in Python 🍩
With Python, you can create a cool moving donut that appears on your screen! This guide uses the vpython library to make the donut move in a natural, circular pattern.

Requirements
Install Python on your system.
Install the vpython library for 3D graphics.
Run the following command in your terminal to install vpython:

pip install vpython
Step 1: Python Code
Here’s the Python code to create a moving donut:

from vpython import *

Set up the scene with a purple background
scene.background = vector(0.5, 0, 0.5)

Create the donut (inner part)
donut = ring(radius=0.5, thickness=0.25, color=vector(400, 100, 1))

Create the chocolate outer layer
chocolate = ring(radius=0.55, thickness=0.25, color=vector(0.4, 0.2, 0))

Initialize angle for rotation
rad = 0

Animate the donut
while True:
    rate(10)  # Control the speed of the animation
    
    # Move the donut and chocolate in a circular path
    donut.pos = vector(3*cos(rad), sin(rad), 0)
    chocolate.pos = vector(3*cos(rad), sin(rad), 0)
    
    # Update the angle to create continuous movement
    rad = rad + 0.03
Step 2: Running Your Virtual Donut
Save the script as virtual_donut.py.
Run the script in your Python environment (e.g., PyCharm or the terminal).
When you run the program, a new window will pop up, showing a donut moving in a circular motion.

How It Works
Scene Setup: We set the background to purple using scene.background.
Donut Creation: We create the donut shape (ring) with a radius of 0.5 and thickness of 0.25.
Chocolate Layer: A chocolate-colored ring (chocolate) is created with a slightly larger radius.
Circular Movement: The donut’s position (donut.pos) and chocolate's position (chocolate.pos) are updated continuously in a circular path using cos(rad) and sin(rad).
Animation: The while True: loop keeps the donut moving, with rate(10) controlling the speed of the movement.

Customization Ideas
Color Variations: Change the color attribute to customize the donut's color.
Speed Adjustment: Adjust the rate(10) value to change the speed of the donut’s movement.
Rotation: You can add more rotations or effects to the donut for an even more dynamic look!

Enjoy your moving virtual donut! 🍩
