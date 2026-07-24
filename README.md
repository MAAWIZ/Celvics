# Structural Analysis and GD&T of Celvics Component

## 1. Project Overview
This repository contains the digital geometric definition, ASME Y14.5-2018 GD&T specifications, and Finite Element Analysis (FEA) results for the structural Celvics component.

* **Author:** Mohammad Maawiz
* **Date:** July 2026
* **CAD/CAE Stack:** PTC Creo (2D Drafting), Siemens NX (3D Modeling), Ansys (Static Structural FEA)

## 2. Material Definition
* **Material:** ASTM A36 Structural Steel
* **Density:** 7850 kg/m³
* **Young's Modulus:** 200 GPa 
* **Poisson's Ratio:** 0.3
* **Yield Strength:** 250 MPa 
* **Ultimate Tensile Strength:** 460 MPa 

## 3. GD&T and Tolerancing
* **Standard:** ASME Y14.5-2018
* **Datum Reference Frame:** Datums A, B, and C
* **Tolerances:** Unspecified linear dimensions X.X = ±0.5 mm, X.XX = ±0.1 mm; Angles = ±0.5°.
* **Feature Controls:** Position within 0.1 to A, B, C; Profile of a surface within 0.1 to A, B; Circular runout within 0.1 to B.

## 4. FEA Setup & Results
* **Mesh:** 11,578 nodes, 6,182 elements
* **Boundary Condition:** Fixed support at the base face.
* **Loading:** 5000 N static force in the +Y direction.
* **Maximum von-Mises Stress:** 327.06 MPa
* **Maximum Total Deformation:** 0.3324 mm
* **Maximum Equivalent Elastic Strain:** 0.0017379 m/m
* **Analysis Status:** Failed (Yield strength exceeded).
