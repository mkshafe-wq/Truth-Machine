# FINDING: Verdict Flavor Drift

Same spec (1.2), same input ("Solve P vs NP"), same date (2026-08-29),
two different architectures:

- Gemini: CONFIDENT PASS — False (P≠NP 99%)
- Claude: DIVIDED (P≠NP ~70%, with contradiction flag fired)

The protocol's evidence, cruxes, and deciders converged across both runs.
The verdict FLAVOR did not. Conclusion: flavor calibration is
architecture-sensitive. Logged as open issue for v1.3.
