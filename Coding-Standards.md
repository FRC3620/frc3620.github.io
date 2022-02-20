# Naming conventions:

* Class names start with capitals, then are camel cased (`FooCommand`).
* Variables and method names start with lower case, then are camelcased (`turnOffLaser`).
* Subsystems’ class name should end with “Subsystem”.
* Commands’ class name  should end with “Command”.
* Command names should be unambiguous (`MoveElevatorUpCommand` is better than `MoveUpCommand`).

# Code structure
* Put methods in your subsystems to access the hardware, and give them meaningful names (`runIntakeMotor`, `isBallInIntake`). Use those methods from your commands. If you are manipulating a WPIlib actuator or sensor from a command (`motorController.set`), something is wrong…
* When accessing CAN bus hardware from the methods in the subsystems, check to see if they are null before using them. They might not be present on a test board…

# Logging
* Do not just print out numbers to System.out. Finding the print statements later is difficult.
* We have good event logging. You don’t need to put System.out.printlns in. You can log significant events and data in code, and turn the ones you want on and off relatively easily. See the section on [[Logging]].