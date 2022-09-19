# Using a non-linear least squares approach to find cosmological parameters Omega and Lambda by using redshift and magnitude data from seven high-redshift Type Ia Supernovae 
## Description
In this project, my goal was to estimate the Cosmological Parameters Ω<sub>M</sub> and Ω<sub>Λ</sub> from data taken from "Measurements of the Cosmological Parameters Ω and Λ from the First 7 Supernovae at z ≥ 0.35" by Perlmutter et al 1996. This data contained Redshift and Magnitude measurements from seven Type Ia Supernovae gathered during the Supernova Cosmology Project. To find the Ω<sub>M</sub> and Ω<sub>Λ</sub> parameters, I attempted to fit the Redshift and Magnitude data to a luminosity distance function, which tells us how far an object is from Earth relative to its apparent and peak brightness. The luminosity distance function that was used is given below, with c and H excluded in my own calculation

![image](https://user-images.githubusercontent.com/113722000/191138008-498ff1c7-04e1-4f01-9800-5f65a03f84cc.png)

- Show log formula and where constant term (23 ish) comes from (Mean of magnitude data)
This function was used in two parts, one where Ω<sub>M</sub> + Ω<sub>Λ</sub> ≠ 1, and another where I set Ω<sub>M</sub> + Ω<sub>Λ</sub> = 1

## Background 
- Explain what Redshift and Magnitude are (Also candlestick approach for measure distance) 
- Explain what omega matter and lambda are and why they are important. 
- Explain what M + L = 1 means in terms of flat universe. 
- Explain H not and C and why they are excluded from the calculation. 

## Method 
To find Ω<sub>M</sub> and Ω<sub>Λ</sub>, I used curve fit from SciPy to find the optimal parameters needed to fit the Redshift and Magnitude measurements to the luminosity distance function. 
- Explain what curve fit does and how it find parameters
To test the accuracy of this model, I applied Chi-Square Minimization to measure the goodness of fit and Mean Squared Estimation to measure the difference between the approximate and real Redshift and Magnitude values.
- Explain what chi square min is, reduced chi square, and MSE 
    - Explanation for chi square can be used from pdf paper 
## Results 
- Show results for both none and constraint equation
- Explain what results mean
- Explain what the probability means for chi square
- Show the actual measurements of matter and lambda from scientific data
