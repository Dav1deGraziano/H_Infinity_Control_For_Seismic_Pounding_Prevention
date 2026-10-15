# H∞ Control for Seismic Pounding Prevention

This project accompanies a short paper on the use of **active shared tuned mass dampers (ASTMDs)** to prevent seismic pounding between adjacent buildings in the presence of model uncertainty.

## Overview

Pounding is the collision of neighbouring structures vibrating out of phase, most often during earthquakes. Shared tuned mass dampers (STMDs) are a natural countermeasure when space and cost are limited, but passive STMDs have been reported to be ineffective in some configurations.

The paper uses a chain of three buildings, modelled as single-degree-of-freedom oscillators and coupled by two shared TMDs, as a test bench. The full system has 5 degrees of freedom. The main points are:

- **Passive control is insufficient.** The unactuated system is nominally stable, but relative displacements between buildings greatly exceed the pounding threshold.
- **Nominal H∞ control works.** Two H∞ controllers are synthesised for the nominal plant. The second includes weighting functions so that the actuation limit is also met. Both prevent pounding across 50 real earthquake records scaled to a peak ground acceleration of 0.1 g.
- **Uncertainty is modelled explicitly.** Actuation uncertainty (sensor bandwidth and delay) and dynamic uncertainty (up to 5% error in all mechanical properties) are captured as structured multiplicative uncertainty.
- **Robust H∞ control via D-K iteration.** A robust controller is synthesised with D-K iteration based on the structured singular value (μ). Robust performance at the 5 mm level is achieved after two iterations.
- **Worst-case validation.** Under the computed worst-case perturbation, the robust controller still prevents pounding in all earthquake scenarios, whereas the nominal controller largely fails.

## Contents

The paper is organised as follows:

1. Introduction and system model (Euler–Lagrange equations, state-space form)
2. Objectives and simulation criteria
3. Nominal H∞ control law and results
4. Structured uncertainty model
5. Rationale behind H∞ control
6. Robust H∞ control via D-K iteration and results

## Repository structure

```
.
├── H∞_Control_For_Seismic_Pounding_Prevention.pdf   
├── LICENSE.pdf   
└── README.md
```

## Keywords

H∞ control, robust control, structured singular value, D-K iteration, tuned mass dampers, seismic pounding, structural vibration control.

## License

The paper is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
