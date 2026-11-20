# Computational Fluid Dynamics (CFD) Studies | Ansys Fluent

**University of Central Florida · EML 3701 Fluid Mechanics · Summer 2026**  
**Project type:** Two academic CFD projects completed in a three-person team  
**Software:** Ansys Fluent, Microsoft Excel  
**Topics:** Boundary-layer theory, laminar external flow, wall shear stress, skin friction, pressure and velocity distributions

> **Project summary:** Examined 2D laminar airflow over a flat plate and airflow through a converging-diverging duct in Ansys Fluent. Compared simulation outputs with theoretical predictions for the flat plate and investigated the effect of three reported operating settings on duct pressure and velocity fields.

📄 **[View the illustrated CFD engineering case study (PDF)](Ansys_Fluent_CFD_Case_Study.pdf)** — simulation contours, comparisons, key calculations, results, and limitations.

## Study 1 — Laminar airflow over a flat plate

**Objective:** Evaluate how a laminar boundary layer develops along a 1.0 m plate and compare CFD-based thickness, wall shear stress, skin friction, and drag with theoretical correlations.

**Reported conditions and results**

| Quantity | Result |
| --- | ---: |
| Plate length | 1.0 m |
| Free-stream velocity | 2 m/s |
| Reynolds number | 1.33 × 10⁵ |
| Mesh size reported in the project | Approximately 101,000 nodes |
| Theoretical drag coefficient | 0.003637 |
| Ansys Fluent drag coefficient | 0.004463 |
| Difference from theoretical value | 22.7% |

**Boundary-layer thickness comparison**

| Downstream position | Fluent | Theory | Reported difference |
| --- | ---: | ---: | ---: |
| x = 0.35 m | 0.00665 m | 0.00810 m | 17.8% |
| x = 0.75 m | 0.01006 m | 0.01186 m | 15.2% |

The extracted velocity profiles show **boundary-layer growth with downstream distance**. The report also compares simulated and theoretical wall shear stress and skin-friction coefficient, both of which generally decline along the plate as the boundary layer thickens.

**Important limitation:** A 101,000-node mesh was reported, but a systematic mesh-convergence or mesh-independence study was **not** documented. The 22.7% drag-coefficient discrepancy should be presented as a modeling result requiring investigation, not as proof of a validated model.

## Study 2 — Converging-diverging duct flow

**Objective:** Examine how velocity and pressure distributions respond to changes in operating conditions in a 2D converging-diverging duct.

The team produced static, dynamic, and total pressure contours alongside velocity contours at **20, 40, and 60 Hz** reported operating settings. Comparison plots show increasing peak velocity at higher settings and a static-pressure minimum near the throat, consistent with the qualitative behavior expected as flow accelerates through a contraction.

The duct report emphasizes visualization and comparison rather than numerical validation. It does not provide enough information to claim an experimentally validated pressure-drop or mass-flow prediction.

## Engineering takeaways

- **External flow:** CFD results can be evaluated against analytical fluid mechanics relations, and differences help identify mesh, domain, numerical, and near-wall modeling questions.
- **Internal flow:** Geometric contraction produces a velocity increase and corresponding change in static pressure; operating settings influence the magnitude of the predicted flow field.
- **Engineering communication:** A useful simulation portfolio explains model assumptions and errors—not just contour plots.

## Suggested improvements for a follow-up revision

1. Document mesh element/node counts, boundary conditions, material properties, solver model, and convergence criteria.
2. Perform and graph at least three mesh refinements for the flat-plate drag coefficient.
3. Export raw data to clean CSV files and remake plots with clearly labeled axes, units, and legends.
4. Quantify duct pressure loss using consistently defined inlet and outlet locations.
5. Add original Fluent project and mesh files only if available and permissible to publish.

## Team-project disclosure

These studies were completed in a **three-person UCF course team**. Plots and numerical results come from the team submissions rather than from independently verified new runs.

