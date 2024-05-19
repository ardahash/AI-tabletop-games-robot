# chess-robot  
  
For the Android/GUI version see the instructions in the versiongui directory.
    
3D printed chess robot, Python code for Raspberry Pi, other Linux or Windows PC. New users should use version 2.

Install Stockfish engine, Python 3, python-pip, espeak

pip install pyserial  
pip install psutil  
pip install numpy  
pip install opencv-python  
pip install stockfish  
pip install pyttsx3  

Run CBint.py from Thonny or elsewhere.

The camera should be positioned directly over the centre of the chess board and lined up pretty well. Then camera calibration asks you to click on the four corners of the playing area of the chessboard (on the image), and you are shown the result. Click them in the order requested. (The robot arm should not be in the way, and all the pieces must be in their correct starting positions). By "playing area" we mean the chessboard squares, NOT including any external margin).

The calibration is remembered even if all systems are shut down, so if the robot, board and camera have not been moved, recalibration can optionally be avoided when a new game is started

The camera should be at least 56 cm above the board. Square size 3.4 cm. Tallest piece: 5.5 cm. The image of a piece should not fall across an adjacent square.

Calibrating the Cartesian robot arm: The lower strut must be vertical and the upper strut horizontal and coming out straight over the board.

Code configuration: You will need to check squaresize, axistorow8, etc. in robotmove.py. Check the declarations in CBstate.py.

Axistorow8 is the distance in mm horizontally along the y coordinate, between the robot’s vertical axis and the centre of row 8. 


The RPi or PC is connected to the Arduino by a USB A/B cable (printer cable). Or alternatively via Bluetooth (not BLE), using an HC-05 Bluetooth module.

Both USB and IP cameras are supported. Calibration for fish-eye distortion is provided, and is more likely to be needed for IP cameras. USB cameras are often OK without it.

Things used in this project
Hardware components

Arduino Mega 2560 ×	1	
Raspberry Pi 3 Model B Or a later version ×	1	
Ramps 1.4 ×	1	
Stepper motor driver board A4988	
SparkFun Stepper motor driver board A4988 ×	3	
NEMA 17 stepper motor ×	3	
USB Speaker Or similar ×	1	
HP Webcam HD 2300 Or similar ×	1	
USB Light Or similar ×	2	
SG90 Micro-servo motor	×	1	
AMS1117 ×	1	
Software apps and online services
Raspbian	
Raspberry Pi Raspbian
Python 3, pyserial, psutil, aplay, numpy, pillow, espeak, python stockfish class, Thonny
Stockfish chess engine
Hand tools and fabrication machines
3D Printer (generic)	

The Hardware Build
The 3D printer files for the robot are freely available as specified as specified by F Tobler here. There you will find a parts list, an animation and a video and many other things. Tobler gives a great description of hardware, Arduino software and robot assembly.

The Tobler arm is modified with the longer arm components as specified here. This is required in order to reach the far corners of the chess board.

We replace the Tobler gripper with a mini-gripper as specified here.

Tobler also refers to a Community and there are some great diagrams there (linked to here under "Schematics") - but be aware that the hardware build is for a slightly different robot arm with a belt drive.

So, we have a Raspberry Pi connected to an Arduino via a printer cable. The Arduino has a Ramps 1.4 board sitting on it to drive the motors via A4988 motor driver boards.

The stepper motors give very high precision and repeatability.

As an alternative to the USB connection from the Raspberry Pi, other Linux or Windows, the code supports Bluetooth (not BLE), using an HC-05.






===  
Version1-old only:  
pip install pillow
pip install psutil  
On RPi install fswebcam, aplay

