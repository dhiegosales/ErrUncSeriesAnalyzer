# Error and Uncertainty Series Analyzer

This software provides tools for importing, analyzing, and exporting error and uncertainty data from simulation series in CSV format. It supports calculating various objective functions (such as RMSE, MAE, BIAS, r, r², and NSE) and generating uncertainty measures using the 95PPU, R-Factor, and P-Factor theory [1]. The results can be exported to an Excel report (.xlsx), including plots.

---

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [Graphical User Interface](#graphical-user-interface)
- [Example](#example)
- [Input Table Requirements](#input-table-requirements)
- [Notes](#notes)
- [Authors](#authors)
- [License](#license)

---

## Features

- Performance Calculation: Supports RMSE, MAE, BIAS, r, r², and NSE as objective functions.
- Uncertainty Calculation: Uses 95PPU, R-Factor, and P-Factor theory [1].
- Data Import: Imports simulation data from a CSV file.
- Data Export: Exports results to an Excel report (.xlsx).
- Plotting: Generates and exports plots of the results.
  
[Back to top](#table-of-contents)

---

## Requirements

- Operating System: Windows 10/11 64-bit
- Python 3
  
[Back to top](#table-of-contents)

---

## Usage

### Run the Application

Use the executable available on GitHub to open the graphical user interface.

[Back to top](#table-of-contents)

---

## Graphical User Interface

### Main Window

The main window consists of several sections:

- Import Section
- Error Calculation Section
- Uncertainty Calculation Section
- Export Section

#### Import Section

- File Name Input: Input field for the CSV file name.
- Browse Button: Opens a file browser to select the CSV file.
- Import Button: Imports the selected CSV file.
- Read Button: Reads and displays the data from the CSV file.

[Back to top](#table-of-contents)

#### Error Calculation Section

- Objective Function Selection: Radio buttons to select the desired objective function (BIAS, RMSE, MAE, r, r², NSE).
- Calc Error Button: Calculates errors based on the selected objective function.
- Error Table Button: Displays a table of calculated errors.
- Best Simulation Button: Displays the best simulation based on the selected objective function.

[Back to top](#table-of-contents)

#### Uncertainty Calculation Section

- Error in Observed Input: Input field for the error in observed values.
- Uncertainty Calc Button: Calculates uncertainties.
- Read Uncertainty Button: Displays a table of calculated uncertainties.
- View Plot Button: Displays a plot of the uncertainties.

[Back to top](#table-of-contents)

#### Export Section

- Export File Name Input: Input field for the export file name.
- Export Directory Input: Input field for the export directory.
- Folder Browse Button: Opens a folder browser to select the export directory.
- .xls Report Button: Exports results to an Excel file.

[Back to top](#table-of-contents)

---

## Example

To import a CSV file, calculate errors using RMSE, calculate uncertainties, and export the results to an Excel file, follow these steps:

1. Run the application.
2. Browse and select your CSV file.
3. Click "Import" to load the data.
4. Select "RMSE" as the objective function.
5. Click "Calc Error" to calculate errors.
6. Enter the error in observed values (e.g., 0.1).
7. Click "Uncertainty Calc" to calculate uncertainties.
8. Enter the export file name and directory.
9. Click ".xls Report" to export the results to an Excel file.

[Back to top](#table-of-contents)

---

## Input Table Requirements

- CSV file with simulations data. 

### Example CSV File Structure (example_csv_file.csv):
| Date       | Observed | SIM1  | SIM2  | SIM3        | SIM4        | SIM5  | SIM6        | SIM7        | ...        |
|------------|----------|-------|-------|-------------|-------------|-------|-------------|-------------|------------|
| 01/01/2008 | 6.5699   | 9.14  | 11.18 | 11.51873672 | 12.33203402 | 13.32 | 12.87425878 | 13.22578492 | ...        |
| 02/01/2008 | 6.5699   | 8.85  | 10.72 | 10.90419215 | 11.62284684 | 12.58 | 11.99037908 | 12.37486219 | ...        |
| 03/01/2008 | 6.098    | 8.06  | 9.9   | 10.04710097 | 10.7403933  | 11.71 | 11.10841073 | 11.50045562 | ...        |
| 04/01/2008 | 5.7909   | 7.59  | 9.37  | 9.495616076 | 10.12828598 | 11.11 | 10.44220738 | 10.83883922 | ...        |
| 05/01/2008 | 5.7909   | 12.54 | 13.72 | 16.28932582 | 15.5283375  | 12.86 | 13.72133141 | 11.90436727 | ...        |
| 06/01/2008 | 11.185   | 17.09 | 17    | 17.69950231 | 16.73132768 | 14.33 | 14.7862309  | 13.1575171  | ...        |
| 07/01/2008 | 11.3804  | 13.06 | 13.24 | 12.8217692  | 12.8425763  | 12.66 | 12.23776574 | 11.85497255 | ...        |
| 08/01/2008 | 7.7213   | 13.09 | 13.48 | 13.83316418 | 13.57105305 | 12.6  | 12.43770012 | 11.70279927 | ...        |
| 09/01/2008 | 8.063    | 13.24 | 13.23 | 12.84975747 | 12.69980697 | 12.36 | 11.82078484 | 11.51162844 | ...        |
| 10/01/2008 | 6.5699   | 13.26 | 13.4  | 13.88394896 | 13.51561512 | 12.4  | 12.1979165  | 11.42525459 | ...        |
| 11/01/2008 | 10.0395  | 22.09 | 20.51 | 21.41428653 | 19.45589964 | 15.92 | 16.12705842 | 14.41034013 | ...        |
| 12/01/2008 | 15.3283  | 27.34 | 23.96 | 23.62159905 | 21.57383117 | 18.32 | 18.2712125  | 17.01282931 | ...        |
| 13/01/2008 | 10.2272  | 20.07 | 17.66 | 16.08664606 | 15.72260422 | 15.62 | 15.10553576 | 15.09769122 | ...        |
| 14/01/2008 | 8.9412   | 11.93 | 11.72 | 10.57369936 | 11.10646109 | 12.4  | 11.4547722  | 12.01793019 | ...        |
| 15/01/2008 | 7.5525   | 10.32 | 10.81 | 10.36533268 | 10.76591244 | 11.56 | 10.70756545 | 11.1048298  | ...        |
| 16/01/2008 | 7.7213   | 9.58  | 10.36 | 9.97610834  | 10.26544921 | 10.98 | 10.1161662  | 10.47987823 | ...        |
| 17/01/2008 | 6.4111   | 12.71 | 13.13 | 14.16410799 | 13.59933922 | 12.03 | 12.06931939 | 11.3550626  | ...        |
| ... | ...   | ... | ... | ... | ... | ... | ... | ...  | ...        |


# Notes

- Ensure the CSV file follows the correct format: The first column should be the date, the second column the observed data, and subsequent columns the simulation data. The CSV file should not contain NaN values, and all series must have the same dimensions.
- The separator used should be ';'.
- An example.csv (example_csv_file.csv) file is provided with programn exe.

**Note:** It is not allowed NaN values in the series and all series (columns) must have the same dimensions.

[Back to top](#table-of-contents)

## Authors

Dhiego da Silva Sales  
Email: dhiego.sales@outlook.com

[Back to top](#table-of-contents)

## License

This project is licensed under the MIT License.

[Back to top](#table-of-contents)

This updated README now includes the formatted CSV table within the "Input Table Requirements" section and integrates the additional information seamlessly. Adjust any styling or formatting according to your documentation standards.

