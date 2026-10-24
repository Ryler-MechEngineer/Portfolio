# Two-Link Robotic Arm: Inverse Kinematics and Simulation

**Role:** Independent learning project, October 2026
**Tools:** MATLAB, Simulink, Simscape Multibody
**Focus:** Forward and inverse kinematics, workspace and joint limits, trajectory planning, multibody simulation

This is a software-only project. There is no physical arm. It is also part of a wider [MATLAB and robotics self-study](../../learning/matlab-robotics-self-study/).

## Summary

I built a simulated two-link planar arm and drove its end effector along a square path using inverse kinematics. I learned to derive the two-link kinematics with the law of cosines, working with an AI tutor, instead of copying formulas. The final model feeds a MATLAB-computed joint trajectory into Simscape Multibody revolute joints, and the arm traces the square correctly.

<!-- IMAGE: images/arm-model.png (Simscape arm model) -->
<!-- IMAGE: images/square-trajectory.png (square path and workspace) -->
<!-- VIDEO/GIF: images/square-trace.gif -->

## Objective

Learn the math and simulation tools needed to command a robot arm to reach specific positions, moving from mechanical design into robotics software.

## How it works

1. MATLAB computes joint angles for each point on the path with inverse kinematics.
2. The angles go into Simulink through From Workspace blocks and Simulink-PS Converters.
3. Revolute joints in Simscape Multibody move the arm.

## Challenges

Nothing in this project broke. The challenge was that all of it was new to me and I did not know how to start. I had to learn MATLAB, the kinematics, and Simulink at the same time.

Along the way I ran into the limits of the arm itself:

- **Elbow-up and elbow-down.** Each reachable point has two valid joint solutions, so I had to pick one and keep it consistent along the path.
- **Reachability and joint limits.** A solution that works on paper is not always one the arm can reach. Some target points were outside the workspace or past a joint limit, so I adjusted the path so every point was a valid configuration.

<!-- NEEDS (Q5.1): you said nothing broke, but you also changed the path because some square points were unreachable. Is that accurate? If so, I would describe that as the first path not working, and I need to know what you saw (an error, a NaN, the arm stopping). -->
<!-- NEEDS (Q5.2): which link lengths and joint limits did you use? How much did you shrink or shift the square, and what did you give up? -->
<!-- NEEDS (Q5.3): how did you detect an unreachable point in code? -->

## Result

The two-link arm traces a square in simulation using inverse kinematics. Next I plan to extend the method to a third link.

## Next steps

A mentor I met on LinkedIn, an automation engineer, suggested extending this to 6 degrees of freedom and using numerical root-solving for inverse kinematics. The plan is a third link first, then moving the kinematics into ROS 2.

## What I took from it

Inverse kinematics has more than one answer, and sometimes none. The geometry of the workspace decides what is possible before any controller gets involved.

<!-- NEEDS (Q5.4): okay to keep the line about learning with an AI tutor? Your own lessons override mine. -->
<!-- NEEDS (Q5.5): upload the .m and .slx files to the matlab/ folder if you want them public -->
