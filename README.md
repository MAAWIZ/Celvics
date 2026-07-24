# Analytical Derivations and Structural Calculations

This document outlines the known FEA parameters and the derived mechanical calculations for the ASTM A36 Celvics component under a static 5000 N load.

## 1. Known System Parameters
* **Component Volume ($V$):** $1.5342 \times 10^{-5} \text{ m}^3$
* **Component Mass ($m$):** $0.12044 \text{ kg}$
* **Applied Force ($F$):** $5000 \text{ N}$
* **Max Deformation ($\delta$):** $3.324 \times 10^{-4} \text{ m}$
* **Max von-Mises Stress ($\sigma_{max}$):** $327.06 \times 10^6 \text{ Pa}$
* **Material Yield Strength ($\sigma_y$):** $250 \times 10^6 \text{ Pa}$

## 2. Derived Physical Properties

### 2.1 Volumetric Density ($\rho$)
Verification of the material assignment using mass and volume.
$$\rho = \frac{m}{V}$$
$$\rho = \frac{0.12044}{1.5342 \times 10^{-5}} = 7850.34 \text{ kg/m}^3$$

## 3. Derived Mechanical Behavior

### 3.1 Global Structural Stiffness ($k$)
Determining the effective spring constant of the component along the axis of loading.
$$k = \frac{F}{\delta}$$
$$k = \frac{5000}{3.324 \times 10^{-4}} = 1.504 \times 10^7 \text{ N/m}$$

### 3.2 Total Strain Energy ($U$)
Calculating the internal work done on the component, assuming linear elastic behavior prior to yielding.
$$U = \frac{1}{2} F \delta$$
$$U = 0.5 \times 5000 \times (3.324 \times 10^{-4}) = 0.831 \text{ J}$$

## 4. Failure Analysis & Redesign Derivations

### 4.1 Factor of Safety (FoS)
$$FoS = \frac{\sigma_y}{\sigma_{max}}$$
$$FoS = \frac{250 \times 10^6}{327.06 \times 10^6} = 0.764$$
*Conclusion: Plastic deformation occurs at the stress concentration because FoS < 1.0.*

### 4.2 Derived Effective Load-Bearing Area ($A_{eff}$)
Calculating the current theoretical cross-section absorbing the peak stress.
$$A_{eff} = \frac{F}{\sigma_{max}}$$
$$A_{eff} = \frac{5000}{327.06 \times 10^6} = 1.528 \times 10^{-5} \text{ m}^2 = 15.28 \text{ mm}^2$$

### 4.3 Required Area for Target Safety Factor ($A_{req}$)
Deriving the necessary effective area in the failure zone to achieve a standard FoS of 1.5.
$$A_{req} = \frac{F \times 1.5}{\sigma_y}$$
$$A_{req} = \frac{5000 \times 1.5}{250 \times 10^6} = 3.0 \times 10^{-5} \text{ m}^2 = 30.0 \text{ mm}^2$$
*Conclusion: The local geometry in the failure zone must be reinforced to roughly double its current effec
