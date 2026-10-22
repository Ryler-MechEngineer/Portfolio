# Two-Link Robotic Arm: Inverse Kinematics and Simulation

**Role:** Independent learning project
**Tools:** MATLAB, Simulink, Simscape Multibody
**Focus:** Forward and inverse kinematics, workspace and joint limits, trajectory planning, multibody simulation

This is a software-only project. There is no physical arm.

## Summary

I built a simulated two-link planar arm and drove its end effector along a square path using inverse kinematics. I learned to derive the two-link kinematics with the law of cosines, working with an AI tutor, instead of copying formulas. The final model feeds a MATLAB-computed joint trajectory into Simscape Multibody revolute joints, and the arm traces the square correctly.

<!-- IMAGE: images/arm-model.png (Simscape arm model) -->
<!-- IMAGE: images/square-trajectory.png (square path and workspace) -->
<!-- VIDEO/GIF: images/square-trace.gif -->

## How it works

1. MATLAB computes joint angles for each point on the path with inverse kinematics.
2. The angles go into Simulink through From Workspace blocks and Simulink-PS Converters.
3. Revolute joints in Simscape Multibody move the arm.

## Where the first attempt failed

A solution that works on paper is not always one the arm can reach. There were two problems:

- **Elbow-up and elbow-down.** Each reachable point has two valid joint solutions, so I had to pick one and keep it consistent along the path.
- **Reachability and joint limits.** Some target points were outside the workspace or past a joint limit. I adjusted the desired path so every point was a valid, physically possible configuration.

<!-- NEEDS (Q5.1): which joint limits and link lengths did you use, and what did the unreachable path look like before you fixed it? -->
<!-- NEEDS (Q5.2): how did you detect an unreachable point in code (the acos domain check)? -->
<!-- NEEDS (Q5.3): did you expect the first path to be unreachable? Why did you choose a square? -->

## Next steps

A mentor I met on LinkedIn, an automation engineer, suggested extending this to 6 degrees of freedom and using numerical root-solving for inverse kinematics. The plan is to add a third link, then move the kinematics into ROS 2.

## What I took from it

Inverse kinematics has more than one answer, and sometimes none. The geometry of the workspace decides what is possible before any controller gets involved.

<!-- NEEDS (Q5.4): okay to keep the line about learning with an AI tutor, or do you want different wording? -->
<!-- NEEDS (Q5.5): upload the .m and .slx files to the matlab/ folder if you want them public -->
