# Using a non-linear least squares approach to find cosmological parameters Omega and Lambda by using redshift and magnitude data from seven high-redshift Type Ia Supernovae 
## Description
In this project, my goal was to estimate the Cosmological Parameters Ω<sub>M</sub> and Ω<sub>Λ</sub> from data taken from "Measurements of the Cosmological Parameters Ω and Λ from the First 7 Supernovae at z ≥ 0.35" by Perlmutter et al 1996. This data contained Redshift and Magnitude measurements from seven Type Ia Supernovae gathered during the Supernova Cosmology Project. To find the Ω<sub>M</sub> and Ω<sub>Λ</sub> parameters, I attempted to fit the Redshift and Magnitude data to a function of apparent brightness, m(z), that takes luminosity distance as input. The constant, M, is the absolute magnitude and d<sub>L</sub> , the luminosity distance function, is given below with c and H<sub>o</sub> excluded in my own calculation.

![image](https://user-images.githubusercontent.com/113722000/191138243-4a2cd913-da4a-4ee4-9fc0-5408d1110f34.png)
![image](https://user-images.githubusercontent.com/113722000/191138192-aef152c7-f200-4283-91d1-a06f032c095e.png)
![image](https://user-images.githubusercontent.com/113722000/191138008-498ff1c7-04e1-4f01-9800-5f65a03f84cc.png)
![image](https://user-images.githubusercontent.com/113722000/191138104-4d783c65-9034-46e7-8626-d6491b347b29.png)
![image](https://user-images.githubusercontent.com/113722000/191138161-d3869cde-0678-45fe-9542-40e90224619c.png)

This function was used in two parts, one where Ω<sub>M</sub> + Ω<sub>Λ</sub> ≠ 1, and another where I set Ω<sub>M</sub> + Ω<sub>Λ</sub> = 1

## Background 
- Explain what Redshift and Magnitude are (Also candlestick approach for measure distance) 
In the early 1920's, Edwin Hubble found that there was a linear relationship between the redshifts and distances of galaxies. As galaxies were more redshifted i.e. farther away, the faster these galaxies were moving away from the Milky Way. Implicitly, this means that there is some rate that the universe is expanding. 
- Explain what omega matter and lambda are and why they are important. 
- Explain what M + L = 1 means in terms of flat universe. 
- Explain H not and C and why they are excluded from the calculation. 

## Method 
To find Ω<sub>M</sub> and Ω<sub>Λ</sub>, I used curve fit from SciPy to find the optimal parameters needed to fit the Redshift and Magnitude measurements to the luminosity distance function. Curve fit from SciPy's optimize library uses non-linear least squares to fit a function to the data where the parameters found will minimize the sum of the squared residuals. To test the accuracy of this model, I applied Chi-Square Minimization to measure the goodness of fit and Mean Squared Estimation to measure the difference between the approximate and real Redshift and Magnitude values. Chi-Square minimization is a technique that minimizes the value of  the chi-square test statistic. I then used reduced chi-square to determine if my curve matched nicely to my data points. If the reduced chi-square is near 1 then we can assume that the model is a good fit. I then used Mean Square Error to further confirm the accuracy of our model by comparing how close  
- Explain what chi square min is, reduced chi square, and MSE 
    - Explanation for chi square can be used from pdf paper 
## Results 
- Show results for both none and constraint equation
- Explain what results mean
- Explain what the probability means for chi square
- Show the actual measurements of matter and lambda from scientific data
