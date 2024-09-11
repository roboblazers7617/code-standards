---
layout: default
title: Style Guide
---

# Introduction

In general, most code MAY be formatted according to the formatter settings files in the git repository. The style that defines those files is defined in this section.

# Indentation

* Tabs MUST be used for indentation wherever possible. The only exception to this is when the usage of tabs will break functionality, in which case spaces MAY be used.
* Continuation lines MUST be indented twice.

# Line wrap

* Lines SHOULD NOT be truncated simply because they are too long
* Long lines SHOULD be split up where it makes sense (for example, long sequences of chained methods and long arrays should be split up over multiple lines)
* In wrapped arrays, the last item MUST have a separator appended to it to reduce the size of git diffs and make merges easier

# Class and interface names

* SHOULD be a noun
* MUST use pascal case
* MUST use full words instead of acronyms

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
public static Command getAutonomousCommand()
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
<access> static abstract synchronized <unusual> final native
```

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

An example of what the hosted Javadoc looks like can be found [here](https://roboblazers7617.github.io/2024Robot/).

# Comments

* Code behavior and general landmarks SHOULD be described in comments
* Contributors MAY decide where and how to use comments, but they SHOULD at least describe enough that someone who hasn’t ever seen the class before can quickly find what they need to change and understand the basic function of the class
