readme_content = """
# Task 2: Dataset Preprocessing

## Objective
Clean and validate Merged01.csv and Merged02.csv.

## Input Datasets
- Merged01.csv: 712,311 rows and 40 columns
- Merged02.csv: 748,585 rows and 40 columns

Each dataset contains 39 features and one target column: Label.

## Preprocessing Performed
1. Verified dataset structure and column consistency.
2. Investigated missing values and infinity values.
3. Replaced positive and negative infinity with missing values.
4. Imputed missing values in Rate, Std, and Variance using
   the median calculated separately for each file.
5. Preserved all rows, labels, columns, and duplicate records.
6. Validated the cleaned datasets.

## Results
| Dataset | Original Rows | Cleaned Rows | Original Missing Cells | Original Infinity Values |
|---|---:|---:|---:|---:|
| Merged01.csv | 712311 | 712311 | 22 | 14 |
| Merged02.csv | 748585 | 748585 | 12 | 13 |

Both cleaned datasets contain zero missing cells and zero
infinity values according to the validation report.

## Output Files
- output/Merged01_clean.csv
- output/Merged02_clean.csv

## Reports
- reports/before_after_comparison.csv
- reports/cleaning_validation.csv
- reports/final_preprocessing_report.csv

## Scope
Only Merged01.csv and Merged02.csv were processed.
Duplicate records were retained. No model training or
train/test split was performed.

## Conclusion
Both datasets were cleaned and validated successfully,
with all original rows and columns preserved.
"""

readme_path = TASK2_DIR / "README.md"
readme_path.write_text(readme_content.strip(), encoding="utf-8")

print("README created:", readme_path)
print("File exists:", readme_path.exists())