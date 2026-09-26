NETFLIX TITLES - CLEANED DATASET
=================================

FILES IN THIS FOLDER
---------------------
1. netflix_titles_cleaned.csv  -> the final cleaned dataset (8,793 rows, 14 columns, 0 missing values, 0 duplicates)
2. clean_netflix.py            -> the Python code used to clean it
3. README.txt                  -> this file

WHAT CODE WAS USED
-------------------
Language: Python
Library: pandas (numpy also used)
File: clean_netflix.py

The script does the following, in order:
1. Loads the raw Netflix dataset (netflix_titles_raw.csv).
2. Trims stray whitespace from all text columns.
3. Fixes 3 rows where a duration value ("74 min") was wrongly entered in the rating column.
4. Removes 4 duplicate titles (same title/type/year, different letter case).
5. Converts date_added from text to a real date, and splits duration into a number + unit.
6. Fills missing director/cast/country with "Not Specified" and missing rating with "Not Rated".
7. Drops 10 rows that had no usable date.
8. Saves the result as netflix_titles_cleaned.csv.

WHERE / HOW TO USE IT
-----------------------
- To just use the data: open netflix_titles_cleaned.csv directly in Excel, Google Sheets,
  Power BI, Tableau, pandas, or any SQL tool (import as a table). No further cleaning needed.

- To re-run or edit the cleaning yourself:
  1. Install Python and pandas:  pip install pandas
  2. Place the raw file next to the script, named netflix_titles_raw.csv
  3. Run:  python clean_netflix.py
  4. It will regenerate netflix_titles_cleaned.csv

- To use this as your GitHub submission for the assignment: upload this whole folder
  (or its contents) as a repo, with netflix_titles_cleaned.csv as the deliverable dataset
  and clean_netflix.py as the cleaning code.
