# Bluetooth-Controlled Battle Bot

**Role:** Team project, January to March 2025
**Tools:** SOLIDWORKS, Arduino, C++, Bluetooth
**Focus:** Custom armor, chassis and drivetrain, wireless drive control, input smoothing

## Summary

We built a small robot for sumo-style matches, with wireless control, a stable drivetrain, and protective custom armor. I designed the armor plating in CAD, programmed Bluetooth motor control and steering in Arduino and C++, and assembled the chassis, electronics, and drivetrain, with attention to stability, pushing force, and where parts sit.

<!-- IMAGE: images/armor-cad.png -->
<!-- IMAGE: images/assembled-robot.png -->
<!-- VIDEO: short demo of it driving or in a match -->

## Design decisions

<!-- NEEDS (Q6.1): armor shape and thickness, and why (coverage vs weight vs access to the electronics vs stability)? -->
<!-- NEEDS (Q6.2): drivetrain and motor choice, and why? -->
<!-- NEEDS (Q6.3): this was a team project. Which parts were yours? -->

## Challenges

- Trading armor coverage and protection against the weight and space limits of a small robot.
- Getting the chassis and drivetrain to push hard without tipping or losing stability.
- Linking wireless commands to motor behavior.
- Leaving room in the structure for the electronics.

## What failed: control lag and spikes

The Bluetooth control felt laggy. When I suddenly turned the controls up, other components that I was not trying to move seemed to get voltage. My best explanation, which I did not confirm, is that the sudden increase caused a voltage spike.

A capacitor would likely have fixed it completely, but I did not have one. Instead I wrote a weighted average that blends the previous input with the current one, so the command cannot jump suddenly. That improved it, but did not remove the problem.

<!-- NEEDS (Q6.4): did you expect this before you built it? What weights did you use in the average (for example 70% old and 30% new)? -->
<!-- NEEDS (Q6.5): how did the robot do in matches? What was the record or result, even if it lost, and did anything else break? -->

## Result

Experience combining CAD-designed parts, embedded programming, wireless control, and a physical mobile robot. No match record is published here because none has been given.

## What I took from it

<!-- NEEDS (Q6.6): your own lessons. Candidates from what you told me: plan for power supply and spikes up front, and use software smoothing as a patch, not a fix. Are those yours? -->
