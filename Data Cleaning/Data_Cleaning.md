# Task 3: Automated Cleaning and Structuring of Inconsistent Reports Using Fuzzy Matching

## Objective  
To automate the cleaning and structuring of inconsistent `.xls` production reports using Python and fuzzy logic, enabling a reusable, scalable solution for audit and dashboard use cases.

## Background  
The company’s production software exports outdated `.xls` reports that differ across departments and contain inconsistent formats.  
- Column names are often misaligned or renamed.  
- Names of employees, machines, and stages appear in inconsistent forms (e.g., spelling variations, abbreviations, or typos).  
- Manual merging was time-consuming and had to be repeated every time a report was generated.

## Description  
- Extracted multiple `.xls` reports using `pandas` and `openpyxl`.
- Applied **fuzzy matching** (`fuzzywuzzy.process.extractOne`) to align mismatched names across files.
- Used **regular expressions** (`re`) and string cleaning logic to normalize values like names, dates, and item descriptions.
- Wrote **modular Python functions** to encapsulate cleaning steps — allowing reuse for future reports with minimal changes.
- Implemented **error handling** and logging to identify failed merges or missing data during execution.
- Combined multiple inconsistent reports into a single, structured dataset using `merge()` and `join()` operations.
- Validated edge cases with domain experts to ensure accuracy.
- Structured the cleaned data to align with audit requirements such as traceability, completeness, and correctness.
- Merged multiple departmental reports into a single analysis-ready DataFrame using joins and reference mappings.
- Validated matches and cleaned edge cases manually where needed, with input from domain experts.

## Tools & Technologies Used  
- Python: `pandas`, `fuzzywuzzy`, `openpyxl`, `re`, `logging`, `joblib`  
- Excel: (for final spot-checking)  
- Modular function-based architecture for reusability  
- Performance optimization using vectorized operations

## Output  
A robust and reusable Python workflow that:
- Automatically cleans and merges inconsistent reports  
- Tracks fuzzy matches and unmatched records  
- Outputs a clean, audit-ready DataFrame suitable for dashboarding and compliance reviews
- Automated what was previously a manual and error-prone cleaning process  
- Improved data reliability for decision-making and compliance audits  
- Enabled downstream tasks like dashboard creation, KPI tracking, and production performance analysis


## Business Impact  
- **Saved 5–6 hours/week** of manual cleanup previously required for each report batch  
- Reduced human error and improved data consistency  
- Enabled downstream teams (e.g., finance, audit, dashboard teams) to use clean data without technical skills  
- Scalable solution — now usable for any future `.xls` exports from the production system
