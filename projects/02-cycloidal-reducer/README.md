# Cycloidal Gear Reducer for the Rover Arm

**Role:** Designer, University Rover Challenge (Robotics and Automation Society). Mechanical Team Lead since May 2026.
**Started:** September 2024
**Tools:** SOLIDWORKS, 3D printing (PLA, heat-treated PLA, carbon-fiber PLA)
**Focus:** Gear-reducer design, fit and tolerance, failure analysis, iterative redesign

<!-- NEEDS (Q2.0): the start date of September 2024 came from your notes, but your lead role started May 2026. When did this project start, and did the failed versions come before or after you became lead? -->

## Summary

I designed, modeled, printed, and tested a cycloidal gear reducer for a rover arm joint. The final design gives a 12:1 ratio and cut volume by about 50%. It also failed in several ways on the way there, and those failures drove the biggest design changes.

<!-- IMAGE: images/cad-assembly.png (full CAD assembly) -->
<!-- IMAGE: images/exploded-view.png (exploded view with labels) -->
<!-- IMAGE: images/printed-assembly.png (photo of the printed unit) -->

## Objective

Get reduced output speed and higher torque from a compact reducer for a robotic rover arm.

## Key numbers

| Item | Value |
|------|-------|
| Reduction | 12:1 |
| Rollers | 12 |
| Disc lobes | 11 |
| Pin diameter | 7 mm |
| Disc hole diameter | 14.4 mm |
| Eccentricity | 2.5 mm |
| Volume | About 50% smaller |
| Best tested load | About 0.5 kg lifted (one modified version) |

## What I did

- Modeled the reducer in SOLIDWORKS around a cycloidal disc, eccentric input, pins, and output components.
- 3D printed the parts, assembled the mechanism, tested it, and revised it based on where it failed.
- Worked through how gear geometry, fit, and clearances affect performance.

## Design decisions

An arm joint needs a lot of torque in a small package. I wanted a high reduction ratio from a single stage in as little volume as possible.

<!-- NEEDS (Q2.1): what did you compare it against (planetary, harmonic, worm) and what made cycloidal win? -->
<!-- NEEDS (Q2.2): the 50% volume reduction is compared to what? -->
<!-- NEEDS (Q2.3): why 11 lobes and 12 rollers, 7 mm pins, 2.5 mm eccentricity? What is the extra clearance in the 14.4 mm holes? -->
<!-- NEEDS (Q2.4): is the 12:1 from the shell-output version, and was the earlier disc-output version about 11:1? -->

## Challenges

- Getting the disc, rollers, pins, and eccentric motion to work together without binding.
- Holding dimensional accuracy and clearances in 3D-printed parts.
- Finding out why early versions failed instead of assuming the CAD would work as modeled.
- Balancing compactness, torque transmission, friction, and durability.

<!-- NEEDS (Q2.5): these are general. Pick the hardest one and tell me the specifics: what bound, where, what clearance did you try, what did you change, and what did it do? -->

## What failed

These are the failures I saw while testing printed versions:

- **Uneven contact.** The load was not always shared evenly across the rollers.
- **Housing deflection.** The housing could flex and twist under load.
- **Cracked parts.** PLA cracked and snapped under load.
- **Backlash.** The output had slack and a springy feel.
- **Shaft failure.** Earlier versions that were expected to lift more eventually broke at the shaft.

<!-- NEEDS (Q2.6): did you expect any of these before printing? Which ones, and what did you do ahead of time to reduce them? -->
<!-- NEEDS (Q2.7): for each failure, what did you find was the cause, and how did you confirm it? -->

## How I fixed it

I changed the output approach to a shell-output configuration. One modified version lifted about 0.5 kg. I also tried heat-treated PLA and carbon-fiber PLA, and I am considering stainless steel for the next iteration.

<!-- NEEDS (Q2.8): why shell output specifically, and what did it change about the failures above? -->
<!-- NEEDS (Q2.9): did the heat-treated and carbon-fiber parts help? What did you measure or see? -->

## Result

A physical cycloidal reducer that I improved through several printed versions, with real experience in mechanism design, fit adjustment, and load testing. It is relevant to robotics, industrial automation, and compact actuators.

<!-- NEEDS (Q2.10): do you have test data, such as the load or torque reached and the failure that prompted the biggest redesign? -->

## What I took from it

Printed tests showed things CAD did not: where load concentrates, how much a housing flexes, and how PLA behaves near its limit. I revise designs from what I observe on the bench, not from the model alone.

<!-- NEEDS (Q2.11): your own lessons, especially about tolerances and material choice -->
<!-- NEEDS (Q2.12): next iteration plan and target (torque, mass, material) -->
