# Error and Uncertainty Series Analyzer

This software provides tools for importing, analyzing, and exporting error and uncertainty data from simulation series in CSV format. It supports calculating various objective functions (such as RMSE, MAE, BIAS, r, r², and NSE) and generating uncertainty measures using the 95PPU, R-Factor, and P-Factor theory [1]. The results can be exported to an Excel report (.xlsx), including plots.

---

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [Graphical User Interface](#graphical-user-interface)
- [Example](#example)
- [Input Table Requirements](#input-table-requirements-citation)
- [Authors](#authors)
- [License](#license)
- [Citation](#citation)
- 
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

![Main Window](https://github.com/dhiegosales/Timeseries-Error-and-Uncertainty-Analyzer/blob/main/GUI.png)

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

- CSV file with data from simulations.

### Example CSV File Structure (example_csv_file.csv):

| Date       | Observed | SIM1    | SIM2    | SIM3    | SIM4    | SIM5  | SIM6    | ...     |
|------------|----------|---------|---------|---------|---------|-------|---------|---------|
| 01/01/2008 | 6.5699   | 9.14    | 11.18   | 11.5187 | 12.3320 | 13.32 | 12.8742 | ...     |
| 02/01/2008 | 6.5699   | 8.85    | 10.72   | 10.9041 | 11.6228 | 12.58 | 11.9903 | ...     |
| 03/01/2008 | 6.098    | 8.06    | 9.9     | 10.0471 | 10.7403 | 11.71 | 11.1084 | ...     |
| ...        | ...      | ...     | ...     | ...     | ...     | ...   | ...     | ...     |

#### Notes

- Ensure the CSV file follows the correct format: The first column should be the date, the second column the observed data, and subsequent columns the simulation data. The CSV file should not contain NaN values, and all series must have the same dimensions.
- The separator used should be ';'.
- An example.csv (example_csv_file.csv) file is provided with programn exe.

**Note:** It is not allowed NaN values in the series and all series (columns) must have the same dimensions.

[Back to top](#table-of-contents)

---

## Authors

Written by: Dhiego da Silva Sales  
Contact: dhiego.sales@outlook.com

---

## Citation:  
Sales, D. S.; Lugon Junior, J.; Costa, D. A.; Silva Neto, A. J. (2024). *Timeseries Error and Uncertainty Analyzer (Version 1.0.0)* [Computer software]. Available at: https://github.com/dhiegosales/Error-and-Uncertainty-Series-Analyzer. Accessed xx xxx xxxx.

[Back to top](#table-of-contents)

## License

This project is licensed under the MIT License, making it open access. You are free to use, modify, and distribute the software under the terms of the MIT License

[Back to top](#table-of-contents)

