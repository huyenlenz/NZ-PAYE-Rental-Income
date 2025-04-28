# NZ Rental Property Tax Calculator

A simple, self-contained HTML & JavaScript tool to estimate taxable rental income and related taxes/levies for residential properties in New Zealand. This calculator is specifically designed for the **2024-2025** and **2025-2026** tax years.

## Overview

This calculator helps New Zealand property owners estimate their tax position related to rental income. It caters to two main scenarios:
1.  **Main Home Rentals:** Renting out rooms within your primary residence (e.g., to flatmates).
2.  **Separate Rental Properties:** Owning an investment property that is fully rented out.

The tool calculates net rental income after apportioning expenses based on space and time, applies the relevant interest limitation rules for the selected tax year, and then estimates the overall Income Tax and ACC Earner's Levy based on the rental profit combined with the user's provided salary income.

**Note:** This tool provides **estimations only** and is **not** a substitute for professional tax advice.

## Features

* Calculates for NZ Tax Years **2024-2025** and **2025-2026**.
* Handles both "Main Home (Rented Rooms)" and "Separate Rental Property" types.
* Performs **Space Apportionment** for main home rentals based on the number of rooms rented vs. total rooms.
* Performs **Time Apportionment** based on monthly occupancy checkboxes (for main home) or full year if income received (for separate property).
* Applies the correct **Interest Limitation Rules**:
    * 2024-2025: 80% interest deductibility
    * 2025-2026: 100% interest deductibility
* Implements **Residential Loss Ring-fencing** (rental losses cannot offset other income but are carried forward).
* Calculates estimated **Income Tax** based on the total taxable income (Salary + Net Rental Income) using the official tax brackets for the selected year.
* Calculates estimated **ACC Earner's Levy** based on the provided Salary/Wages income, applying the correct rate and cap for the selected year.
* Provides a clear summary of income, deductions, net result, and tax/levy estimations.
* Allows users to **Export** the input data and calculation summary to an Excel (.xlsx) file.
* Pure client-side calculation (runs entirely in the browser).

## How to Use

1.  **Open:** The Link https://huyenlenz.github.io/NZ-PAYE-Rental-Income/.
2.  **Input Data:**
    * **Tab 1: Property Details:** Select the Tax Year, Property Type, enter bedroom counts (if applicable), property purchase date, and your Annual Salary/Wages (before tax).
    * **Tab 2: Monthly Income:** Enter the gross rental income received for each month (April to March). If renting rooms in your main home, check the boxes for each month a specific rentable room was occupied. Use the "Auto-Fill" button for convenience if income is consistent.
    * **Tab 3: Annual Expenses:** Enter the *total* expenses for the *entire tax year* (e.g., annual rates, insurance, mortgage interest, sum of monthly utility bills, etc.).
3.  **Calculate:** Click the "Calculate Results" button on the Expenses tab.
4.  **Review:** The results will appear in the "Calculation Results" panel, showing the income/expense breakdown, apportionment factors, net rental income, and estimated Tax/ACC liability.
5.  **Export (Optional):** Click the "Export to Excel" button to download a spreadsheet summary of your inputs and the calculated results.

## Tax Rules Included (2024-25 & 2025-26)

* **Income Tax Brackets:** Uses the specific multi-tier brackets announced for 1 April 2024 - 31 March 2025 and the updated brackets for 1 April 2025 - 31 March 2026.
* **ACC Earner's Levy:** Applies the relevant rate (1.60% for 24/25, 1.67% for 25/26) and income cap ($142,283 for 24/25, $152,790 for 25/26) to the *salary* portion of income.
* **Interest Limitation:** 80% claimable for 24/25, 100% for 25/26.
* **Expense Apportionment:** Standard methods for space (room count) and time (months occupied/available).
* **Loss Ring-fencing:** Implemented.

## Technology Stack

* HTML5
* CSS3
* Vanilla JavaScript (ES6+)
* [SheetJS (js-xlsx)](https://github.com/SheetJS/sheetjs) library (included via CDN) for Excel export functionality.

## Disclaimer

**This calculator provides an estimate for informational purposes only.** It is not intended as financial or tax advice. Tax laws are complex and subject to change, and individual circumstances vary widely.

* Calculations are based on the specific rates, brackets, and rules known for the 2024-2025 and 2025-2026 NZ tax years.
* The calculator does *not* account for all possible deductions, income types, tax credits (e.g., IETC), KiwiSaver, student loan repayments, specific depreciation rules, Bright-line tests, or complex ownership structures.
* Apportionment calculations are simplified and may need adjustment based on specific usage patterns and IRD guidance.

**Always consult with a qualified tax professional or accountant for advice tailored to your specific situation before making any financial decisions or filing tax returns.**

## Limitations

* Currently only supports the 2024-2025 and 2025-2026 tax years.
* Time apportionment is based on whole months, not specific days.
* Does not calculate depreciation.
* Does not calculate potential tax liability under the Bright-line test if the property is sold.
* Assumes standard income tax codes apply.
* Basic space apportionment calculation; users may need to apply more specific methods depending on their situation (e.g., floor area, shared spaces).

