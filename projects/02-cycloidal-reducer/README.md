# Cycloidal Gear Reducer for the Rover Arm

**Role:** Designer and Mechanical Team Lead, University Rover Challenge (Robotics and Automation Society)
**Tools:** SOLIDWORKS, 3D printing (PLA, heat-treated PLA, carbon-fiber PLA)
**Focus:** Gear-reducer design, fit and tolerance, failure analysis, iterative redesign

## Summary

I designed, modeled, printed, and tested a cycloidal gear reducer for a rover arm joint. The final design gives a 12:1 ratio and cut volume by about 50%. It also failed in several ways on the way there, and those failures drove the biggest design changes.

<!-- IMAGE: images/cad-assembly.png (full CAD assembly) -->
<!-- IMAGE: images/exploded-view.png (exploded view with labels) -->
<!-- IMAGE: images/printed-assembly.png (photo of the printed unit) -->

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

## Why a cycloidal reducer

An arm joint needs a lot of torque in a small package. I wanted a high reduction ratio from a single stage in as little volume as possible.

<!-- NEEDS (Q2.1): what did you compare it against (planetary, harmonic, worm) and what made cycloidal win? -->
<!-- NEEDS (Q2.2): the 50% volume reduction is compared to what? -->
<!-- NEEDS (Q2.3): why 11 lobes and 12 rollers, 7 mm pins, 2.5 mm eccentricity? What does the 14.4 mm hole size include (pin plus 2 x eccentricity is 12 mm, so what is the extra clearance)? -->
<!-- NEEDS (Q2.4): is the 12:1 from the shell-output version, and was the earlier disc-output version about 11:1? -->

## What failed

These are the failures I saw while testing printed versions:

- **Uneven contact.** The load was not always shared evenly across the rollers.
- **Housing deflection.** The housing could flex and twist under load.
- **Cracked parts.** PLA cracked and snapped under load.
- **Backlash.** The output had slack and a springy feel.
- **Shaft failure.** Earlier versions that were expected to lift more eventually broke at the shaft.

<!-- NEEDS (Q2.5): did you expect any of these before printing? Which ones, and what did you do ahead of time to reduce them? -->
<!-- NEEDS (Q2.6): for each failure, what did you find was the cause, and how did you confirm it? -->

## How I fixed it

I changed the output approach to a shell-output configuration. One modified version lifted about 0.5 kg. I also tried heat-treated PLA and carbon-fiber PLA, and I am considering stainless steel for the next iteration.

<!-- NEEDS (Q2.7): why shell output specifically, and what did it change about the failures above? -->
<!-- NEEDS (Q2.8): did the heat-treated and carbon-fiber parts help? What did you measure or see? -->

## What I took from it

Printed tests showed things CAD did not: where load concentrates, how much a housing flexes, and how PLA behaves near its limit. I revise designs from what I observe on the bench, not from the model alone.

<!-- NEEDS (Q2.9): your own lessons, especially about tolerances and material choice -->
<!-- NEEDS (Q2.10): next iteration plan and target (torque, mass, material) -->
