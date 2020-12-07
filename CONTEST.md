# PCB Design Competition Guide

## Objective
The goal of the PCB Design Competition is to design a Buzzcard sized printed circuit board (PCB) using [Autodesk EAGLE](https://www.autodesk.com/products/eagle/overview) to do anything you want! The competition has two categories: **Beginner** and **Advanced**. The Beginner category is for 1st and 2nd years and those with limited electronics experience. The Advanced category is for 3rd years and older and those with significant electronics experience.


## Logistics

### Teams
For the Beginner category, teams will be allowed of **up to 2 members**. For the Advanced category, teams are **not allowed**.

### Timeline
The competition will run from **December 14th 2020 to January 14th 2021**! While you are allowed to think of ideas and form teams until then, please only start working on the 14th.

### Technical Contraints
Our goal is to create as few technical restrictions as possible. However, to keep the competition fair and to ensure that the designs are within RoboJackets manufacturing capabilities, all submissions must follow these rules:
- PCB size must not exceed **85.6 mm by 54 mm** (standard credit card size).
	- The board size and shape can be freely edited given that a bounding box around the PCB does not exceed this size.
- Cost of design must be **less than $50**. This includes the individual pre-tax cost of one PCB + the cost of components for one PCB.
	- The BOM must include everything necessary for your design to operate (i.e. AC wall power adapters) with the exception of small guauge (greater than 18 AWG) wire.
- Options for manufacturers are **JLCPCB** or **OshPark**.
	- Please specify manufacturing-related information as explained in [Submission Materials](#submission-materials).
	- The circuit board must pass the design rules check (DRC) for the specified manufacturer (the DRC files for both OshPark and JLCPCB are in [RoboJackets Standard Library](https://github.com/RoboJackets/eagle-libraries)).

### Anonymity
In order to preserve the integrity of the competition, please do not put any personally identifying information on your PCB design. The judges have agreed to leave or mute the #electrical-ama Slack channel. Please do not share your designs with your division’s judges until all designs have been judged.

### Design Help
If you wish to consult with someone on your design, please use the #electrical-ama Slack channel. This will be the place for all technical questions during the competition.

### Questions
Please direct any competition logistics or other non-technical questions to the competition organizer, **Varun Madabushi** on Slack. The [FAQ](#faq) below will be updated with clarifying information throughout the competition.

## Submission Materials

### GitHub Repository
All files for submission should be on GitHub in your own reposistory. A link to this reposistory will be submitted at the end of contest using a Google form. Details on the GitHub setup is in [Getting Started](#getting-started).

### Required Files
- EAGLE Schematic (.sch) file
- EAGLE Board (.brd) file
- EAGLE Library (.lbr) file for any custom parts not included in the [RoboJackets Standard Library](https://github.com/RoboJackets/eagle-libraries)
- Bill of Materials (for one unit including the PCB and other componenets) as a CSV file with the following columns:
	- Quantity
	- Part RefDes
	- Description (including value and tolerance as necessary)
	- Vendor
	- Vendor Part Number
	- Unit Cost
	- Unit Total
	- Total Cost
- EAGLE Schematic screenshots
- EAGLE Manufacturing View screenshots
- **Optional** 3D Render screenshots
	- While not required, 3D renders are also appreciated. This is using a feature within EAGLE that uses Fusion 360 to incorporate 3D models for parts.
	- If you have questions, feel free to reach out on the #electrical-ama Slack channel for an explanation of this process.
- Documentation as a README.md
	- This file should be a [Markdown](https://www.markdownguide.org/getting-started/) file so that it is easy to view formatted online.
	- The explanation should include any explanations for any significant circuits in your design.
	- This can be formatted with screenshots of parts of your schematic/board with explanation.
	- This is also the section to include any design choices or calculations you made while designing your PCB.
	- If necessary to understand your design, explain any major firmware features that would be necessary here.
	- Finally, be sure to mention any important manufacturing information here, including but not limited to:
		- PCB manufacturer
		- Layer count
		- Soldermask color
		- Surface finish (HASL, ENIG, etc.)
		- PCB type (regular, flex, etc)


## Judging

### Judges
The Advanced category will be judged by RoboJackets alumni Jonathan Jones, Ryo Osawa, and Matthew White.

The Beginner category will be judged by current RoboJackets members Asha Bhandarkar, Arthur Siqueira, and Joseph Spall.

### Criteria
Submissions for both categories will be judged based on the following criteria (out of 50 points):

#### Creativity - 14 Points
The judges will look at all materials to determine whether the designer put in significant effort to create something interesting and cool.

#### Effectiveness - 14 Points
The judges will look at the PCB files and explanation to determine whether most of the design would work and that the circuits designed achieve their intended goal.

#### Design Efficiency - 9 Points
This will be judged based on your bill of materials. Judges will evaluate whether your choice of components and PCB specifications is efficient, i.e. do all components and circuits meet the desired function, without exceeding it unnecessarily (in cost, complexity, or otherwise).

#### Documentation - 9 Points
The judges will look at the screenshots and markdown summary to determine if they are accurate, sufficient, and understandable. The markdown summary can be supplemented with additional renders, 3D CAD, calculations, diagrams, simulations, etc. If firmware was a critical part of your design, judges will look at those aspects as well. Strong documentation which helps judges to better understand your design can improve scores in the other categories.

#### Style Guide - 4 Points
The judges will look to ensure that the PCB schematic, layout, and parts match the specifications in the [RoboJackets EAGLE Style Guide](https://wiki.robojackets.org/EAGLE_Style_Guide). Overall, the schematic should be organized and readable, and the board layout should be functional with an appropriate silkscreen.


## Prizes
RoboJackets will manufacture the PCB and buy related components for the winner(s) of each category. Alternatively, the winner(s) can receive a $35 giftcard to [Adafruit](https://www.adafruit.com) or [Sparkfun](https://www.sparkfun.com).


## Getting Started

### GitHub
To use Git to version your project, you can either install the graphical tool [GitHub Desktop](https://desktop.github.com) or use the command line tool [git](https://git-scm.com/downloads). To get started with this contest, you will create your own copy of this reposistory to work with. Start by navigating back to the top of this [reposistory](https://github.com/RoboJackets/pcb-contest) and click the green **Use this template** button. Then give your repository a name and make it **public**. You are now ready to start working!

### EAGLE
To install EAGLE, go to the [Autodesk education software website](https://www.autodesk.com/education/edu-software/overview?sorting=featured&page=1), create an account, and install the education version of EAGLE.

If you are new to EAGLE and PCB design, we encourage you to look at the various [RoboJackets EAGLE resources](#robojackets-eagle-resources) before you continue further.

### Design Brainstorming
If you are having trouble coming up with a design idea, a good resource is [Adafruit](https://www.adafruit.com) or [Sparkfun](https://www.sparkfun.com). Both have tutorials for various projects for inspiration. In addition, all of their designs are open source. Sometimes it is also useful to think of your design at a component level, so we have listed some components that you might consider using. By no means is the list below comprehensive, and there’s not a requirement for including any of these in your design.
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
	- Class D Audio Amplifiers
- Microcontrollers
	- Breakout Boards
		- Arduino (Uno, Nano, etc.)
		- mBed
		- STM32 Nucleo
		- Teensy
	- STM32
	- Atmel/Microchip
		- AVR (ATMega328, ATMega32u4, ATTiny)
		- ARM (ATSamd)

## Resources

### People
- Organizer: Varun Madabushi
- Beginner Judges: Asha Bhandarkar, Arthur Siqueira, and Joseph Spall
- Advanced Judges: Jonathan Jones, Ryo Osawa, and Matthew White

Remember that you cannot consult or share designs with judges from your division.

### Git and GitHub
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet.pdf)
- [GitHub Tutorial](https://guides.github.com/activities/hello-world/)

### Markdown
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [Markdown Tutorial](https://guides.github.com/features/mastering-markdown/)

### RoboJackets EAGLE Resources
- [RoboJackets Standard Library](https://github.com/RoboJackets/eagle-libraries)
- [EAGLE Style Guide](https://wiki.robojackets.org/EAGLE_Style_Guide)
- [EAGLE Video Tutorial Series](https://www.youtube.com/watch?list=PL1R5gSylLha2iQ7e9mwiXJDY2RXoM8HxK&v=2VtJ9Y4NA2E)
- [Electrical Training Fall 2020](https://www.youtube.com/watch?list=PL1R5gSylLha1r1cdYd3TEnzhL_FxiWyOD&v=gtxdOOxpT5U)
- [Electrical Training GitHub](https://github.com/RoboJackets/electrical-training)
- [EAGLE Cheat Sheet](https://github.com/RoboJackets/electrical-training/blob/master/references/eagle_cheat_sheet/eagle_cheat_sheet.pdf)
- [EAGLE Guide](https://github.com/RoboJackets/electrical-training/blob/master/references/eagle_training_guide/eagle_guide.pdf)

### Other EAGLE Resources
- [EAGLE Layers Explained](https://www.autodesk.com/products/eagle/blog/every-layer-explained-autodesk-eagle/)

### Design Resources
- [Electronics Stack Exchange](https://electronics.stackexchange.com)
- [Hackaday](https://hackaday.com)
- [Adafruit Blog](https://blog.adafruit.com)
- [Sparkfun Blog](https://www.sparkfun.com/news)

## FAQ
This section will be updated as common questions arise.

- Can we have multiple of the same PCB being assembled and connected together as part of our submission?
	- The end product can be made of multiple PCBs assembled together, but all PCBs must be able to panelize within the originally specified area (85.6 mm by 54 mm).
- Can we have flex PCBs?
	- Yes, as long as it is indicated in the doucmentation and the appropriate PCB manufactuer is chosen.
