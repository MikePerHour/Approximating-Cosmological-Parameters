# Approximating Cosmological Parameters Ω and Λ from High-Redshift Supernovae using a non-linear least squares approach 
## Background

## Description
In this project, my goal was to estimate the Cosmological Parameters Ω<sub>M</sub> and Ω<sub>Λ</sub> from data taken from "Measurements of the Cosmological Parameters Ω and Λ from the First 7 Supernovae at z ≥ 0.35" by Perlmutter et al 1996. This data contained Redshift and Magnitude measurements from seven Type Ia Supernovae gathered by Perlmutter et al during the Supernova Cosmology Project. To find the Ω<sub>M</sub> and Ω<sub>Λ</sub> parameters, I attempted to fit the Redshift and Magnitude data to a luminosity distance function, which tells us how far an object is from Earth relative to its apparent and peak brightness. The luminosity distance function that was used is given below, with c and H<sub>o</sub> excluded in my own calculation: 
 
 ![image](https://user-images.githubusercontent.com/113722000/190884664-7e52473d-dd30-447d-bef9-97b02b875887.png)
 ![image](https://user-images.githubusercontent.com/113722000/190884297-2c78b0b8-af37-4de6-93b9-2f8270c6f51c.png)
 ![image](https://user-images.githubusercontent.com/113722000/190884412-f234c0c4-e7a1-4dac-8ac8-3d1d6a33987e.png)
 ![image](https://user-images.githubusercontent.com/113722000/190884427-2c551f1c-9a95-48ef-9246-bc6647b90a38.png)
 
This function was used in two parts, one where Ω<sub>M</sub> + Ω<sub>Λ</sub> ≠ 1 and another where I set Ω<sub>M</sub> + Ω<sub>Λ</sub> = 1

## Method  
To find Ω<sub>M</sub> and Ω<sub>Λ</sub>, I used curve fit from SciPy to find the optimal parameters needed to fit the Redshift and Magnitude measurements to the luminosity distance function. To test the accuracy of this model, I applied Chi-Squared Minimization to measure the goodness of fit and Mean Squared Estimation to meaure the difference between the approximate and real Redshift and Magnitude values. 



## Results for Ω<sub>M</sub> + Ω<sub>Λ</sub> ≠ 1
```
Omega Matter:  0.6337216810462113
Omega Lambda:  1.1048258157863622
Reduced chi-squared:  1.1017675850177235
Probability of chi-squared:  0.28529445346456467
Mean Squared Error:  0.07225730198828448

```
