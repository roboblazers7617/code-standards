---
layout: default
title: Test Guidelines
---

# Introduction

The test process used by 7617 prioritizes safety and is designed to show bugs while testing changes instead of after. The test process is described below.

* You SHOULD merge main into the branch before testing to ensure that any changes since the branch was created work with the changes in the branch.
* You MUST test changes using the simulator and make sure that everything works properly.
* If everything works in the simulator, you MUST test on the robot.

# Test before enabling

The robot MUST NOT be enabled until the logic has been confirmed in simulation and on the robot through Shuffleboard.

