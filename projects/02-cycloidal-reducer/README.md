# Cycloidal Gear Reducer for the Rover Arm

**Role:** Designer, University Rover Challenge (Robotics and Automation Society). I started this in September 2024 as a team member and became Mechanical Team Lead in May 2026, so all of the reducer work below happened before I was lead.
**Tools:** SOLIDWORKS, 3D printing (PLA, heat-treated PLA, carbon-fiber PLA)
**Focus:** Gear-reducer design, fit and tolerance, failure analysis, iterative redesign

## Summary

I designed, modeled, printed, and tested a cycloidal gear reducer for a rover arm joint. The best version gives a 12:1 ratio and cut volume by about 50%. The shaft kept deforming across versions and I never fully fixed it. After that I decided to move to a different gearbox type instead of patching this one.

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
| Disc clearances used | 0.1 mm and 0.2 mm combined (two offset discs) |
| Volume | About 50% smaller |
| Best tested load | About 0.5 kg lifted (one modified version) |

## What I did

- Modeled the reducer in SOLIDWORKS around two offset cycloidal discs, an eccentric input, pins, and output components.
- 3D printed the parts, assembled the mechanism, tested it, and revised it based on where it failed.
- Worked through how gear geometry, fit, and clearances affect performance.

## Design decisions

**Why a cycloidal reducer.** An arm joint needs a lot of torque in a small package. I wanted a high reduction ratio from a single stage in as little volume as possible.

**Why shell output.** With the output on the outer shell, the arm attaches to the outside, which makes the arm easy to stabilize, and I can make the internal parts very strong and sturdy. If the outside were the fixed part, the arm would be supported on one end only.

**Why two clearances.** There are two offset discs inside, so I combined two clearances, 0.1 mm and 0.2 mm. That gave me the best result of what I tried.

<!-- NEEDS (Q2.1): what did you compare cycloidal against (planetary, harmonic, worm) before choosing it? -->
<!-- NEEDS (Q2.2): the 50% volume reduction is compared to what? -->
<!-- NEEDS (Q2.3): why 11 lobes and 12 rollers, 7 mm pins, 2.5 mm eccentricity? What is the 14.4 mm hole, and what are the 0.1 mm and 0.2 mm applied to (roller holes, discs, pins)? -->
<!-- NEEDS (Q2.4): is the 12:1 from the shell-output version, and was the earlier disc-output version about 11:1? -->

## Challenges

- Getting the discs, rollers, pins, and eccentric motion to work without binding.
- Holding dimensional accuracy and clearances in 3D-printed parts.
- Finding out why early versions failed instead of trusting the CAD.
- Balancing compactness, torque transmission, friction, and durability.

The hardest one was the shaft. It kept deforming across versions. My best guess, which I have not confirmed, is that my math and tolerances were slightly off, so extreme loads were passing into the shaft instead of being shared by the rollers.

## What failed

- **Shaft deformation.** The shaft kept deforming. This was the main failure and the reason for the redesign.
- **Uneven contact.** The load was not always shared evenly across the rollers.
- **Housing deflection.** The housing could flex and twist under load.
- **Cracked parts.** PLA cracked and snapped under load.
- **Backlash.** The output had slack and a springy feel.
- **Shaft failure.** Earlier versions that were expected to lift more eventually broke at the shaft.

**What I expected and what I did not.** I expected the PLA to flex a little with the shell output, because two eccentric discs rotate inside it. I did not expect much trouble from the shaft. I thought it would do better under compression, and it was a D-shaft. It deformed anyway.

<!-- NEEDS (Q2.5): "the 3 shaft kept deforming" in your message: do you mean a 3 mm shaft, or the third version's shaft? -->
<!-- NEEDS (Q2.6): how did you see it deform (bent, twisted, flat of the D crushed)? Where did it fail? That tells us whether it was torque, bending, or both. -->
<!-- NEEDS (Q2.7): did you check the math or tolerances after a failure to test your guess? -->

## How I fixed it, and where it stands

I changed the output to a shell-output configuration, and one modified version lifted about 0.5 kg. I also tried heat-treated PLA and carbon-fiber PLA, and I have considered stainless steel.

I did not solve the shaft deformation. I am now switching to a Wolfrom planetary gearbox, because it should give me a high ratio without the precise manufacturing that cycloidal discs need.

<!-- NEEDS (Q2.8): did heat-treated and carbon-fiber parts help? What did you see? -->
<!-- NEEDS (Q2.9): "Wolfrom" is my guess for how you spelled it. Is that right? What ratio and what size are you targeting? -->

## Result

A physical cycloidal reducer that I improved through several printed versions, with real experience in mechanism design, fit adjustment, and load testing. It is relevant to robotics, industrial automation, and compact actuators.

## What I took from it

Printed tests showed things CAD did not: where load concentrates, how much a housing flexes, and how PLA behaves near its limit.

<!-- NEEDS (Q2.10): your own lessons, especially about tolerances, material choice, and choosing a mechanism. -->
