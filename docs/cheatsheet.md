---
layout: default
title: Cheat Sheet
---
# Java Cheat Sheet
[Java Cheat Sheet](https://quickref.me/java)

# WPILIB Cheat Sheet
## Commands
Commands can be created in multiple ways. 
- As a class in a dedicated file ([example](https://github.com/roboblazers7617/2024Robot/blob/main/src/main/java/frc/robot/commands/drivetrain/LockWheelsState.java))
- They can also be created from within a subsystem with `this.run()` or `this.run_once()` ([example](https://github.com/roboblazers7617/2024Robot/blob/f5001c29fe566a391c225b51ecd9b3a94f114b5d/src/main/java/frc/robot/subsystems/Arm.java#L224))
- This can also be run from outside of a subsystem with `Commands.run()` or `Commands.run_once()`
- By creating a new `InstantCommand()`
- additional instructions can be added on with `andThen()`
Commands created in their own class can be used by creating an instance of that class. Commands created with `this.run()` in a subsystem can be returned in a function ([example](https://github.com/roboblazers7617/2023Robot/blob/c20cb360442556252a7e746540ee881309c408a3/src/main/java/frc/robot/subsystems/Arm.java#L233-L235))
