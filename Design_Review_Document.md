# Engineering Design Review: Clevis (Celvics) Component

**Project:** Clevis Mechanical Assembly & Validation  
**Author:** Mohammad Maawiz  
**Date:** July 2026  
**Status:** Design Verification & Structural Analysis Complete  

---

## 1. Executive Summary

This document outlines the design verification and structural validation of the solid Clevis component (`Celvics`). It details the Geometric Dimensioning and Tolerancing (GD&T) specifications per industry standards and presents the findings of a static structural Finite Element Analysis (FEA) performed to assess component viability under maximum operational load.

---

## 2. Geometric & Manufacturing Specifications

The component drawing specifies strict adherence to standardized manufacturing tolerances, material selection, and surface finishing to ensure operational reliability.

| Parameter | Specification |
| :--- | :--- |
| **Drafting Standard** | ASME Y14.5-2018 |
| **Material Designation** | ASTM A36 Structural Steel |
| **Protective Finish** | Zinc Plating (ASTM B633) |
| **Linear Tolerances** | X.X = Â±0.5 mm, X.XX = Â±0.1 mm |
| **Angular Tolerance** | Â±0.5Â° |
| **Edge Treatment** | Remove all burrs; Chamfer 0.5x45Â° / R0.5 Max |

---

## 3. Finite Element Analysis (FEA) Setup

A computational simulation was modeled to replicate operational boundary conditions, evaluating how the geometry distributes structural stress under an applied force.

| Parameter | FEA Configuration |
| :--- | :--- |
| **Simulation Platform** | ANSYS 2025 R2 (Mechanical APDL) |
| **Mesh Architecture** | 11,578 Nodes \| 6,182 Elements |
| **Mesh Refinement** | 2.2 mm Element Size (Face Sizing) |
| **Boundary Conditions** | Fixed Support (Base Shaft) |
| **Applied Load** | 5,000 N (Ramped along Y-Axis) |
| **Material Yield Strength** | 250 MPa ($2.5 	imes 10^8$ Pa) |

---

## 4. Simulation Results

The static structural solver successfully converged, providing localized data for stress concentrations and structural displacement.

| Metric | Result Value |
| :--- | :--- |
| **Max Equivalent (von-Mises) Stress** | 327.06 MPa ($3.2706 	imes 10^8$ Pa) |
| **Max Total Deformation** | 0.3324 mm ($3.324 	imes 10^{-4}$ m) |
| **Max Equivalent Elastic Strain** | 0.0017379 m/m |
| **Total Strain Energy** | 0.09155 J |

> **âš ï¸  Critical Analysis: Stress Concentration**  
> The simulation recorded a peak stress of **327.06 MPa** at the transition fillets where the fork arms meet the main base. This magnitude strictly exceeds the specified A36 structural steel Tensile Yield Strength of **250 MPa**, indicating localized plastic yielding.

---

## 5. Engineering Conclusion & Optimization Plan

While the component will not undergo catastrophic ruptureâ€”as the maximum stress remains well below the ultimate tensile strength (~460 MPa)â€”the region exceeding 250 MPa will experience permanent plastic deformation. The current geometry is inadequate for repeated cyclical loading at 5,000 N.

### Recommended Next Steps:
1. **Geometry Iteration:** Increase the internal fillet radius (currently denoted as R.25 on the drawing) to drastically lower the stress concentration factor at the fork junction.
2. **Dimensional Adjustment:** Broaden the cross-sectional area of the arms near the root to increase the section modulus and resist bending moments more effectively.
3. **Material Alternative:** If volumetric constraints prevent geometry alterations, upgrading from ASTM A36 to a high-yield structural alloy is advised to maintain elastic behavior under peak stress.