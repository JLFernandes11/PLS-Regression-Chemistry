# PLS-Regression-Chemistry

Partial Least Squares Regression for chemical spectroscopy multivariate calibration. Written in Python with a TKinter-based GUI. 

This tool reads spectral CSV data, applies **Savitzky–Golay preprocessing**, performs **PLS calibration**, and outputs the **predicted concentrations** as a CSV file.

# What is PLS Regression

The Partial Least Squares Regression (PLS) is a linear regression model that the reduces the dimensionality of the data while maximizing the **covariance** between the concentrations (response variable) and spectral (independent variable) data. As a result, PLS provides a multivariate linear model that is **more robust** than the classical calibration method and the PCR model. 

In that process, the dimensionality of the concentrations (response variable) and spectral (independent variable) data are reduced to principal components or latent variables, which the optimum number is determined by **cross validation**. 

To perform PLS, it was used the **NIPALS algorithm** which is the default used by **Scikit-learn**. 

***

To run the `PLS_Regression.py` file make sure the following dependencies are installed: 
<ul>
  <li>Pandas</li>
  <li>Numpy</li>
  <li>Matplotlib</li>
  <li>Scipy</li>
  <li>Scikit-learn</li>
  <li>Tkinter</li>
  <li>Customtkinter</li>
</ul> 

After running `PLS_Regression.py`, the GUI will prompt you to upload four `.csv` files:
<ul>
  <li>Spectral data (absorbance) of the standards (training)</li>
  <li>Wavelength or wavenumber values the spectral data were colected</li>
  <li>Known concentrations of the standards (training)</li>
  <li>Spectral data (absorbance) of the sample</li>
</ul> 

Each file must follow a specific format: 

![image_alt](https://github.com/JLFernandes11/PLS-Regressions-Chemistry/blob/5ac0693d9665bbe440caa5c750c539bbb8f0b2ad/Screenshot.png) 

You can test the application using:
<ul>
  <li>standards_spectral.csv</li>
  <li>wavelength.csv</li>
  <li>standard_concentrations.csv</li>
  <li>sample_simulation.csv</li>
</ul> 

Output:
<ul>
  <li>Preprocessing and calibration plots will be shown.</li>
  <li>Model performance metrics will be shown.</li>
  <li>Final predicted concentrations are saved as "predicted_concentrations_pls.csv".</li>
</ul> 
