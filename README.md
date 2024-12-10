Hovercraft Control System
This project demonstrates the construction and programming of a remote-controlled hovercraft using BLDC motors and a servo motor. The hovercraft is designed to lift off, move forward, and turn left or right by controlling the thrust and aerodynamic pressure dynamically.

Working Explanation
Hardware Setup
Motors:

Three BLDC motors:
Two lift motors at the hull corners to generate thrust for hovering.
One propulsion motor at the back to push the craft forward.
One servo motor:
Controls the aerodynamic angle of the main sail to guide direction.
Motor Placement:

The two BLDC motors for lift are placed with a calculated gap to avoid propeller contact.
The third BLDC motor is mounted at the topmast for propulsion.
The servo motor is connected to the sail at the quarter deck.
Thrust Mechanism:

Lift Motors: Rotate in opposite directions to generate maximum lift.
If they rotate in the same direction, their thrust cancels, and hovering is not achieved.
Propulsion Motor: Pushes the craft forward.
Servo Motor: Angles the sail to create aerodynamic pressure, enabling turns.
Control Mechanism
The hovercraft is controlled via a mobile app that sends specific commands to the microcontroller.

Command Functions
Command	Description	Action
0	Start Hovercraft	Activates lift motors to full throttle, lifting the hovercraft.
1	Move Forward	Propulsion motor at full throttle, sail angle at 0° (perpendicular to airflow).
2	Turn Right	Sail angled to +60°; air pressure guided to push craft to the right.
3	Turn Left	Sail angled to -60°; air pressure guided to push craft to the left.
4	Stop Hovercraft	All motors stop; hovercraft descends back to the surface.
Program Explanation
The program uses an Arduino microcontroller to interpret commands and control the motors accordingly. Below is an overview of how the program executes each command:

Start Hovercraft:

Test(): Sets BLDC motors 1 and 2 to maximum throttle to achieve lift.
Move Forward:

Test1(): Keeps lift motors at full throttle and engages the propulsion motor with the sail at a 0° angle.
Turn Right:

Test2(): Sets sail to +60°, redirecting airflow to turn the craft right.
Turn Left:

Test3(): Sets sail to -60°, redirecting airflow to turn the craft left.
Stop Hovercraft:

Test4(): Stops all motors, bringing the craft back to the surface.
Features
Dynamic Control: Real-time adjustments for lift, propulsion, and direction using a mobile app.
Aerodynamic Efficiency: Utilizes servo-controlled sails to guide airflow effectively.
Multi-Motor Coordination: Seamless interaction between motors to achieve desired actions.
Output Explanation
Example Outputs:
Command: 0
Output: Hovercraft lifts off the surface.
Command: 1
Output: Hovercraft moves forward.
Command: 2
Output: Hovercraft turns right.
Command: 3
Output: Hovercraft turns left.
Command: 4
Output: Hovercraft stops and descends.
Future Enhancements
Integrating obstacle detection sensors for autonomous navigation.
Adding additional controls for more complex maneuvers.
Using more energy-efficient motors and lightweight materials for enhanced performance.
