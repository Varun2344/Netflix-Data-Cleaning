# Netflix Movies and TV Shows - Data Cleaning Project

## 1. Project Overview

This project focuses on cleaning and preprocessing a raw dataset of Netflix titles. The primary goal was to transform the messy, real-world data into a clean, structured format suitable for analysis. This task is a foundational step in any data analysis workflow.

## 2. Dataset

The original dataset (`netflix_titles.csv`) contained information about movies and TV shows available on Netflix, including details like director, cast, country, release year, and duration.

## 3. Cleaning and Preprocessing Steps

The Python script (`data_cleaning_script.py`) performs the following actions:

* **Handled Missing Values:**
    * Dropped a small number of rows with missing `date_added`, `rating`, and `duration`.
    * Filled missing values in the `director`, `cast`, and `country` columns with the placeholder 'Unknown' to maintain data integrity.

* **Corrected Data Types:**
    * Converted the `date_added` column from a string object to a proper `datetime` format to enable time-based analysis.

* **Restructured the `duration` Column:**
    * Split the original `duration` column (e.g., "90 min", "2 Seasons") into two new columns: `duration_value` (integer) and `duration_unit` (category). This makes numerical analysis on duration possible.

* **Removed Duplicates:**
    * Checked for and removed any duplicate rows to ensure data accuracy.

## 4. Key Insights from the Cleaned Data

After cleaning, the dataset was used to derive a few quick insights:

* **Busiest Month for Content Addition:** July was the month with the most new content added to Netflix.
* **Average Movie Length:** The average runtime for a movie on Netflix is approximately 99.58 minutes.

*(Add any other insights you found here)*

## 5. How to Run

1.  Ensure you have Python and the pandas library installed.
2.  Place `data_cleaning_script.py` and `netflix_titles.csv` in the same directory.
3.  Run the script. It will automatically generate the `netflix_cleaned.csv` file.
