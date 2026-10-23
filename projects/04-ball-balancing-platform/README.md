# Ball-Balancing Platform

**Role:** Team project, February to March 2025
**Tools:** Arduino, C++, MG90S servos, touchscreen and sensor input
**Focus:** Closed-loop control, servo actuation, PID tuning

## Summary

We built a two-axis, servo-driven platform that balances a ball on its surface using feedback control. The platform tilts on two axes driven by MG90S servos (pins 9 and 10), and a PID controller turns the ball's measured position into servo commands. I designed and built the physical platform, integrated the servos, and programmed and tuned the PID.

<!-- IMAGE: images/platform-with-ball.png -->
<!-- IMAGE: images/axes-diagram.png (simple diagram labeling the two axes and servos) -->
<!-- VIDEO: ball balancing demo, linked or uploaded -->

## Objective

Balance a ball by tilting a platform in response to where the ball is.

## Design decisions

<!-- NEEDS (Q4.1): why a touchscreen vs other position sensing? Why MG90S servos? Why this linkage geometry? -->
<!-- NEEDS (Q4.2): was there a CAD model? What did you design versus buy? -->
<!-- NEEDS (Q4.3): this was a team project. Which parts were yours and which were teammates'? -->

## Challenges

- Balancing something that is naturally unstable and needs constant correction.
- Tuning the gains so the platform reacts quickly without oscillating.
- Accounting for mechanical movement and servo response when judging the control behavior.
- Making the mechanical design fit what the controller needs.

<!-- NEEDS (Q4.4): these are general. What did the ball do at first (oscillate, drift, fall off)? What did you change in P, I, and D to fix it, and in what order? -->
<!-- NEEDS (Q4.5): did backlash or servo limits get in the way? Did you expect that? -->

## Result

Hands-on experience tuning a feedback system where the mechanics and the software directly affect each other. The public project description gives no settling time, tracking error, or final performance figure.

<!-- NEEDS (Q4.6): how long does it hold the ball, and how does it recover from a nudge? Even rough numbers help. -->
<!-- EVIDENCE: video of the ball balancing, the PID code (put it in a code/ folder), and any tuning notes -->

## What I took from it

In a system like this, mechanical geometry, actuator response, and controller tuning all affect each other. A controller cannot fix a loose joint.

<!-- NEEDS (Q4.7): your own lessons -->
