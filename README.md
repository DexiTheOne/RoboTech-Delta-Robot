With the advent of high density distribution and fulfillment centers. Chaos storage has proven to be the most effective method of organization, or lack thereof. Items may be stowed at any place inside the warehouse, lowering labor and bookkeeping requirements. However, smart indexing systems must be leveraged to recall and retrieve items efficiently, regardless of how many different items are grouped together. 

This project is a demonstration of a simple yet clever kinematic system, the delta robot. Compared to a traditional robotic arm, the delta robot combines all 3 axes into one end effector, providing higher efficiency and greater agility. 

The video demos here show the robot moving between different positions at a high speed. The second demo shows a practical use of the high speed movement for picking up and sorting packages and boxes, even food! As you can see, such a delta robot is very practical for automating warehouse indexing and sorting. 

Now let’s look at the design: 

The system is first modeled in CAD. With specific calculations applied to determine the most efficient lengths and arrangements.  

The KR26 FPGA also contains an arm processor capable of running standard linux operating systems. Here lies an application that calculates the reverse kinematics to operate the Delta Robot. 

Movement commands are then sent to a dedicated real time control board capable of generating time synchronized pulses between all 3 stepper motors, this is critical to ensuring accuracy and safety. 

A clever sensorless homing solution was implemented, the arms will go to their 0 degree position and hit hard stops. The stepper driver then detects resistance in the motors, signaling that the arm position has returned to zero. This solution requires no mechanical switches that may wear down over time. 

The open loop nature of the system requires that the stepper motors find their home position at the beginning of every run. As you remote power from the system, all motors free up and the arm drops down. 

Design files and open source credits are all listed in the Github that I've prepared. 

Problems that were encountered: 

Nothing is ever as easy as it seems, especially when dealing with the kinematics of a Delta Robot. Any misalignment in the construction greatly skews dimensional accuracy and therefore causes very unexpected behaviors. Some manual calibration was needed.  

The overall mechanical system has proven to be functional, but could certainly improve in ways that increase reliability and rigidity.  Of course with a 36 hour time limit and 4 hours of 3D printing, this is the best that I could come up with. 

Thank you for your interest! 

Built with open source Ubuntu Linux operating system and Klipper Kinematics firmware. 
