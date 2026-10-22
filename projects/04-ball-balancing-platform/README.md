# Ball-Balancing Platform

**Role:** Team project, February to March 2025
**Tools:** Arduino, C++, MG90S servos, touchscreen and sensor input
**Focus:** Closed-loop control, servo actuation, PID tuning

## Summary

We built a two-axis, servo-driven platform that balances a ball on its surface using feedback control. The platform tilts on two axes driven by MG90S servos (pins 9 and 10), and a PID controller turns the ball's measured position into servo commands. I designed and assembled the platform and servo arrangement, and I worked on programming and tuning the PID.

<!-- IMAGE: images/platform-with-ball.png -->
<!-- IMAGE: images/axes-diagram.png (simple diagram labeling the two axes and servos) -->

## Design decisions

<!-- NEEDS (Q4.1): why a touchscreen vs other position sensing? Why MG90S servos? Why this linkage geometry? -->
<!-- NEEDS (Q4.2): was there a CAD model? What did you design versus buy? -->

## What failed and how I tuned it

<!-- NEEDS (Q4.3): what did the ball do at first (oscillate, drift, fall off)? What did you change in P, I, and D to fix it, and in what order? -->
<!-- NEEDS (Q4.4): did mechanical backlash or servo limits get in the way? Did you expect that? -->
<!-- NEEDS (Q4.5): final result (how long it holds, how it recovers from a disturbance) -->

## What I took from it

In a system like this, mechanical geometry, actuator response, and controller tuning all affect each other. A controller cannot fix a loose joint.

<!-- NEEDS (Q4.6): your own lessons -->
