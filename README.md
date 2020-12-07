# PCB Design Competition Guide

## Objective
The goal of the PCB Design Competition is to design a Buzzcard sized printed circuit board (PCB) using EAGLE to do anything you want! The competition has two categories, beginner and advanced. The beginner category is for 1st and 2nd years and those with limited electronics experience. The advanced category is for 3rd years and older and those with significant electronics experience.
##Constraints

###Technical
Our goal is to create as few technical restrictions as possible. However, to keep the competition fair and to ensure that the designs are within RoboJackets manufacturing capabilities, all submissions must follow these rules.
- PCB Size must not exceed 85.6 by 54 mm (standard credit card size). A template of the appropriate size will be provided. The board size and shape can be freely edited given that a bounding box around the PCB does not exceed the aforementioned size.
- Cost of design must be < $50. This includes the individual cost of one PCB + the cost of components for one PCB.
- Options for manufacturers are JLC PCB and OshPark. Please specify your desired manufacturer in the documentation. The circuit board must pass the design rules check (DRC) given by the specified manufacturer (the DRCs for both OshPark and JLC are in #eagle-libraries). OshPark costs more than JLC so keep that in mind when considering overall cost.

###Teams
For the Beginner category, teams will be allowed of **up to 2 members**. For the Advanced category, teams are **not allowed**.

##Anonymity
In order to preserve the integrity of the competition, judges have agreed to leave or mute the #electrical-ama channel. This will be the only channel for technical communication related to the competition. Please do not share your designs with your division’s judges until all designs have been judged. At the time of submission, a submission link will be provided. In addition, please do not put personally identifying information on your PCB design. If you wish to consult with someone on your design, please use the #electrical-ama channel.
##Submission Materials
All files for submission should be on GitHub. Details on GitHub setup and submission is the Getting Started section. 

The following submission materials are required:
- EAGLE Schematic (.sch) and Board (.brd) files
- EAGLE Library (.lbr) for any custom parts not included in the [RoboJackets Standard Library](https://github.com/RoboJackets/eagle-libraries)
- Bill of Materials and PCB cost (For one unit) as a CSV file
	- Columns
		- Part RefDes
		- Description (incl. value and tolerance as necessary)
		- Vendor
		- Vendor Part Num
		- Unit Cost
		- Num per board
		- Total cost
- EAGLE Manufacturing view screenshots
	- Optional 3D render screenshot
		- While not required, 3D renders are also appreciated. This is a feature within EAGLE that uses Fusion 360 which incorporates 3D models for parts.
		- If you have questions, feel free to reach out on #electrical-ama for an explanation of this process.
- Documentation as a README.md
	- The explanation should include any explanations for any significant circuits in your design. This can be formatted with screenshots of parts of your schematic/board with explanation. This is also the section to include any design choices or calculations you made while designing your PCB.

##Judging Criteria
The Advanced category will be judged by RoboJackets alumni Ryo Osawa, Jonathan Jones, and Matthew White. 

The Beginner category will be judged by current RoboJackets members Joseph Spall, Asha Bhandarkar, and Arthur Siqueira.

Submissions for both categories will be judged based on the following criteria:

###Design Efficiency - 9 Points
This will be judged based on your bill of materials. Judges will evaluate whether your choice of components and PCB specifications is efficient, i.e. do all components and circuits meet the desired function, without exceeding it unnecessarily (in cost, complexity, or otherwise)?


###Creativity - 14 Points
The judges will look at all materials to determine whether the designer put in significant effort to create something interesting and cool.


###Effectiveness - 14 Points
The judges will look at the PCB files and explanation to determine whether most of the design would work and that the circuits designed achieve their intended goal.


###Style Guide - 4 Points
The judges will look to ensure that the PCB schematic, layout, and parts match the specifications in the [RoboJackets Style Guide](https://wiki.robojackets.org/EAGLE_Style_Guide). Overall, the schematic should be organized and readable, and the board layout should be functional with an appropriate silkscreen.


###Documentation - 9 Points
The judges will look at the screenshots and markdown summary to determine if they are accurate, sufficient, and understandable. The markdown summary can be supplemented with additional renders, 3D CAD, calculations, diagrams, simulations, etc. If firmware is a critical part of your design, please provide an explanation of its aspects as well. Strong documentation which helps judges to better understand your design can improve scores in the other categories.


##Prizes
RoboJackets will manufacture the PCB and buy related components for the winner(s) of each category. Alternatively, the winner(s) can receive a $35 giftcard to Adafruit or Sparkfun.


##Getting Started

###Github

###EAGLE
To install EAGLE, go to the AutoDesk education software [website](https://www.autodesk.com/education/edu-software/overview?sorting=featured&page=1), create an account, and install the education version of EAGLE. 

If you are new to EAGLE and PCB design, we encourage you to look at the various RoboJackets resources. A good starting point is to watch the EAGLE tutorial videos and go through the comprehensive EAGLE Guide while doing so. As you begin using the tool, the EAGLE Cheat Sheet will be a useful resource to remember various EAGLE commands and tools.


###Design Brainstorming
If you are having trouble coming up with a design idea, a good resource is Adafruit and Sparkfun. Both have tutorials for various projects for inspiration. In addition, all of their designs are open source. Sometimes it is also useful to think at a component level, so we have listed some components that you might consider using. By no means is the list below comprehensive, and there’s not a requirement for including any of these in your design.

- Inputs
	- Switches
	- Buttons
	- Touch Sensors
	- Dial
- Sensors
	- Ultrasonics
	- IMUs (Gyro, Accel, Compass)
	- Temperature
	- Biometrics
	- Hall Effect
- Visuals
	- Neopixels
	- DotStar
	- 7 Segment Display
	- LCD
	- LEDs
- Useful ICs
	- Voltage Regulators
	- 555 Timer
	- Audio Amplifiers
- Microcontrollers
	- Breakout Boards (Watch out for cost)
		- Arduino (Uno, Nano, etc.)
		- mBed
		- STM32 Nucleo
		- Teensy
	- STM32
	- Atmel/Microchip
		- AVR/Arduino: ATMega328, ATMega32u4, ATTiny
		- ARM: ATSamd

##Resources

###People
- Organizer: Varun Madabushi
- Beginner Judges: Joseph Spall, Asha Bhandarkar, Arthur Siquerira
- Advanced Judges: Jonathan Jones, Ryo Osawa, Matthew White
Remember that you cannot consult or share designs with judges from your division.

###Github

###RoboJackets EAGLE Resources
[EAGLE Tutorial Series](https://www.youtube.com/watch?list=PL1R5gSylLha2iQ7e9mwiXJDY2RXoM8HxK&v=2VtJ9Y4NA2E)
[Electrical Training Fall 2020](https://www.youtube.com/watch?list=PL1R5gSylLha1r1cdYd3TEnzhL_FxiWyOD&v=gtxdOOxpT5U)
[Electrical Training GitHub](https://github.com/RoboJackets/electrical-training)

###Other EAGLE Resources
[EAGLE Layers Explained](https://www.autodesk.com/products/eagle/blog/every-layer-explained-autodesk-eagle/)

###Design Resources
[Electronics Stack Exchange](https://electronics.stackexchange.com)
[Hackaday](https://hackaday.com)
[Adafruit](https://blog.adafruit.com)
[Sparkfun](https://www.sparkfun.com/news)

##FAQ
This section will be updated throughout as common questions arise. The question and answer will be noted here for future use.



