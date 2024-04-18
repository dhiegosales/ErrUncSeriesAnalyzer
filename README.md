# Error-and-Uncertainty-Series-Analyzer

Features: 

-Performance calculation using one of the following objective functions: RMSE, MAE, BIAS, r, r2 or NSE;

-Uncertanty calculation using 95PPU, R-Factor and P-factor theory;

-Exporting *.xlxs report.'



Input table requeriments

-Build a *.csv file where the first column must be a DATE, second column must be a OBSERVED (reference) and the other columns are the simulations.

-the separator is ';'

Example:

Header=>      Date;     Observated;    SIM1;      ...;    ...',

Lines =>  01/01/2019;     value;       value;     ...;    ...',

	      ...

	      ...

	      ...


     
Note: It is not allowed NAN values in sthe series and all series (columns) must have the same dimensions

An example .csv file is provided with programn exe.
