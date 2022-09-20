# A non-linear least squares approach to find cosmological parameters Ω<sub>M</sub> and Ω<sub>Λ</sub> by using redshift and magnitude data from seven high-redshift Type Ia Supernovae 
## Description
In this project, my goal was to estimate the Cosmological Parameters Ω<sub>M</sub> and Ω<sub>Λ</sub> from data taken from "Measurements of the Cosmological Parameters Ω and Λ from the First 7 Supernovae at z ≥ 0.35" by Perlmutter et al 1996. This data contained Redshift and Magnitude measurements from seven Type Ia Supernovae gathered during the Supernova Cosmology Project. To find the Ω<sub>M</sub> and Ω<sub>Λ</sub> parameters, I attempted to fit the Redshift and Magnitude data to a function of apparent brightness, m(z), that takes luminosity distance, d<sub>L</sub> , as input. The functions and constraints used are given below, with M being the absolute magnitude. H<sub>o</sub> and c are excluded in my own calculation. 

![image](https://user-images.githubusercontent.com/113722000/191138243-4a2cd913-da4a-4ee4-9fc0-5408d1110f34.png)
![image](https://user-images.githubusercontent.com/113722000/191138192-aef152c7-f200-4283-91d1-a06f032c095e.png)
![image](https://user-images.githubusercontent.com/113722000/191138008-498ff1c7-04e1-4f01-9800-5f65a03f84cc.png)
![image](https://user-images.githubusercontent.com/113722000/191138104-4d783c65-9034-46e7-8626-d6491b347b29.png)
![image](https://user-images.githubusercontent.com/113722000/191138161-d3869cde-0678-45fe-9542-40e90224619c.png)

These functions were used in two parts, one where Ω<sub>M</sub> and Ω<sub>Λ</sub> do not have a constraint, and another where I set the constraint Ω<sub>M</sub> + Ω<sub>Λ</sub> = 1 i.e. a flat universe.

## Background 
- Explain what Redshift and Magnitude are (Also candlestick approach for measure distance) 

In the early 1920's, Edwin Hubble found that there was a linear relationship between the redshifts and distances of galaxies. As galaxies were more redshifted i.e. farther away, the faster these galaxies were moving away from the Milky Way. Implicitly, this means that there is some rate that the universe is expanding. 
- Explain what omega matter and lambda are and why they are important. 

Ω<sub>M</sub> is defined as matter density and Ω<sub>Λ</sub> is defined as energy density.
- Explain what M + L = 1 means in terms of flat universe. 
- Explain H not and C and why they are excluded from the calculation. 

## Method 
To find Ω<sub>M</sub> and Ω<sub>Λ</sub>, I used curve fit from SciPy to find the optimal parameters needed to fit the Redshift and Magnitude measurements to the luminosity distance function. Curve fit from SciPy's optimize library uses non-linear least squares (Specifically the Levenberg-Marquardt algorithm) to fit a function to the data where the parameters found will minimize the sum of the squared residuals. To test the accuracy of this model, I applied Chi-Square Minimization to measure the goodness of fit. Chi-Square Minimization is a technique that minimizes the value of the Chi-Square Test Statistic, which when divided by my degrees of freedom, can determine if my curve matched nicely to my data points. This process of dividing the Chi-Square Test Statistic by the degrees of freedom is called the Reduced Chi-Square Statistic. If the Reduced Chi-Square Statistic is near 1 then we can assume that the model is a good fit. I then used Mean Square Estimation Error to further confirm the accuracy of our model by comparing how close the difference between the approximate and real Redshift and Magnitude values are to one another. When this measure is close to 0, we can say that the model fits well to our data. 
 
## Results 
### Ω<sub>M</sub> and Ω<sub>Λ</sub> do not have a constraint

```
Omega Matter:  0.6337216810462113
Omega Lambda:  1.1048258157863622
Reduced chi-square:  1.1017675850177235
Probability of chi-square:  0.28529445346456467
Mean Squared Error:  0.07225730198828448
```
![image](https://user-images.githubusercontent.com/113722000/191159442-44364487-78d7-4c33-991a-1a78f6bdd90e.png)
![image](https://user-images.githubusercontent.com/113722000/191159570-550be766-966e-4998-b664-d3e5e683a7a2.png)


###  Ω<sub>M</sub> + Ω<sub>Λ</sub> = 1

```
Constrained Omega Matter:  0.29175800883954417
Constrained Omega Lambda:  0.7082419911604558
Reduced chi-square for constraint:  1.0890196146779565
Probability for reduced chi-square:  0.30514195335647476
Mean Squared Error:  0.07173226319591595
```
![image](https://user-images.githubusercontent.com/113722000/191163492-5f446a7c-a749-4189-8b57-d7c6d37a0e4b.png)
![image](https://user-images.githubusercontent.com/113722000/191163529-a7dab9ab-e221-42e1-aba8-05781626425e.png)


- Explain what results mean
- Explain what the probability means for chi square
- Show the actual measurements of matter and lambda from scientific data
