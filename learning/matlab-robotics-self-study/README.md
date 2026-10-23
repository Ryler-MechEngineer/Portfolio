# MATLAB and Robotics Self-Study

**Status:** Ongoing. This is a learning track, not a finished engineering project.
**Tools:** MATLAB, Simulink, Simscape Multibody, Python, ROS 2

## Objective

Build the math and programming skills I need to control robotic systems, on top of my mechanical design background.

## What I've done

- Started learning MATLAB for mathematical modeling and robotic-arm simulation.
- Learned to derive forward and inverse kinematics for a two-link arm.
- Went from basic joint motion to an inverse-kinematics-driven square trajectory. The full write-up is in the [two-link arm project](../../projects/05-two-link-arm-ik-simulation/).
- Started learning Python to broaden my programming toolkit.
- Set up ROS 2 (Jazzy) on Windows and ran turtlesim as a first test.

<!-- NEEDS (Q-S1): you described ROS as a future goal, but your notes say you already set up ROS 2 and tested turtlesim. Which is accurate right now? The line above follows your notes. -->

## Why I chose this path

My background is mechanical design. A robot also needs the math and software that tell the mechanism what to do, and I did not want to hand that half to someone else.

<!-- NEEDS (Q-S2): in your own words, why MATLAB first and then ROS 2 and Python? Was it a decision, or did the project push you there? -->

## Challenges

- Moving from mechanical design into mathematical modeling and programming.
- Seeing how geometry, joint angles, workspace constraints, and physical limits interact.
- Learning new software while carrying coursework and leadership roles.

<!-- NEEDS (Q-S3): these are general. What was the most confusing moment, a concept or an error, and how did you get through it? What did you stop doing or push back to make time? -->

## Result

The strongest completed milestone is the square-tracing arm simulation. My posts show the progression from first MATLAB experiments to a working inverse kinematics demonstration.

## Next

- Extend the arm to a third link.
- Use numerical root-solving for inverse kinematics, as a mentor (an automation engineer I met on LinkedIn) suggested, and work toward 6 degrees of freedom.
- Move the kinematics into ROS 2.
