# simple_IPI
Calculate the inverse prediction interval of a linear calibration dataset

If this script is useful to your research, please cite:
McClelland, H. L., Halevy, I., Wolf‐Gladrow, D. A., Evans, D., & Bradley, A. S. (2021). Statistical uncertainty in paleoclimate proxy reconstructions. Geophysical Research Letters, 48(15), e2021GL092773.

Calculate simple IPI (Method 1 in McClelland et al. 2021)

[IPIout,regressionCoeff] = calculate_IPI(plotQ,varargin)
plotQ (1/0) will produce a graph of the data with IPI plotted
The second input can either be: not entered (function brings up a user interface to select data file) a filename in the current directory ('my_data.csv') an n*2 matrix (if the data are already loaded into the workspace)

If the data are loaded through a user interface or via a filename this data must be in the form of a csv file with the predictor values in the first column and the measured values in the second column, with one header row.

Examples: 
Calculate IPI & OLS regression coefficients, and produce a graph after manually selecting the data file:
[IPI,regressionCoeff] = calculate_IPI(1)
Read data from an exisiting variable in the workspace:
[IPI,regressionCoeff] = calculate_IPI(1,calData)
Load data using the filename:
[IPI,regressionCoeff] = calculate_IPI(1,'my_calibration_data.csv')
