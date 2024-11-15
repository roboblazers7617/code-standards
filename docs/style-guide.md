---
layout: default
title: Style Guide
---

# Class and interface names

* SHOULD be a noun
* MUST use pascal case
* SHOULD use full words instead of acronyms

```java
class Robot
class Drivetrain
class Launcher extends SubsystemBase
```

# Method names

* SHOULD either be a verb or verb-noun combination
* MUST use camel case

```java
public void periodic()
public void setVelocity(double velocity)
```

### Boolean methods

* SHOULD use `is` or `has` as a prefix before the function name
* MUST NOT be negated (an example of a negated name would be `isNotSpinning`)
* SHOULD ask a question that can be answered `true` or `false`

``` java
boolean isIntakeLowered() {...};
boolean isFlywheelAtTarget() {...};
```

# Command names

* SHOULD either be a verb or verb-noun combination
* MUST use pascal case

```java
public static Command Shoot()
public static Command RaiseArm()
```

# Variable names

## Variables

* MUST be a noun
* MUST use camel case
* SHOULD accurately describe the function of the variable without any other context

```java
Motor motor;
double speed;
int velocityRPM;
```

### Boolean variables

* SHOULD use `is` or `has` as a prefix before the variable name
* MUST NOT be negated (an example of a negated name would be `isNotSpinning`)
* SHOULD ask a question that can be answered `true` or `false`

``` java
boolean isIntakeLowered;
boolean isFlywheelAtTarget;
```

## Constants

* MUST be a noun
* MUST use uppercase snake case
* MUST accurately describe the function of the constant without any other context
* SHOULD be declared with `public` `static` and `final` modifiers

```java
public static final double MIN_BATTERY_VOLTAGE;
public static final int CLIMBER_ID;
```

# Importing classes
The following rules will be follwed by classes imported by VSCode. 
* MUST be listed explicitly

```java
import frc.robot.commands.ResetGyro;
import frc.robot.commands.swerve.TurnToAngle;
```

MUST NOT use

```java
import frc.robot.commands.*;
```

# Method / class modifiers

* MUST be given in the following order

```java
<access> static abstract final
```
(access aka public, private, etc.)

For example: 
```java
public static XBoxController driverController;
```

MUST NOT use

```java
static public XboxController operatorController;
```

# Javadoc

* Java classes, methods, and constants MUST have a valid and complete Javadoc entry accompanying them
* MUST describe the full function of the object they are documenting
* MUST accurately describe the function of any parameters
* MUST describe the return type and returned object if applicable
* SHOULD include any implementation specifics that might be useful to whoever is using the object
* References to classes MUST be linked to the classes they are referencing to make browsing the hosted Javadoc easier

Examples:
```java
/**
	 * safely set the target angle for the arm
	 * 
	 * @param targetDegrees
	 *            the target angle for the arm in degrees
	 */
  public void setArmTarget(double targetDegrees) {
    ...
  }
```
```java
/**
   * get the velocity of the arm
   *
   * @return the velocity of the arm in m/s
   */
  public double getArmVelocity(){
    ...
  }
```
When you hover over a function with Javadoc anywhere in the project it will apear. 
![Javadoc in VSCode](/code-standards/assets/images/javadoc-vscode.png)

An example of what the hosted Javadoc looks like can be found [here](https://roboblazers7617.github.io/TShirtLauncher/).

# Comments

* Code behavior and general landmarks SHOULD be described in comments
* Contributors MAY decide where and how to use comments, but they SHOULD at least describe enough that someone who hasn’t ever seen the class before can quickly find what they need to change and understand the basic function of the class
