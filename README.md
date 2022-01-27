# School District Analysis

## Overview of the school district analysis
After finishing the complete analysis for the district, we were notified of evidence of academic dishonesty in one of the schools included in the original assessment. The board decided to replace the school grades with NaNs and later decide what to do with those results. This decision means that we will repeat the analysis considering this modifications and compare how the results changed.

### Resources
Data Source: students_complete.csv, school_complete.csv
Software: Python 3.7.6, Jupyter Notebook

## Results
The first step was again to clean the data, we searched for missing values, and we remove prefixes and suffixes to work with only the students names in the *student_data* file.
In that same data frame we imported numpy and used the loc function to select all reading and math scores from Thomas High School 9th graders and replace them with NaN.

student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "reading_score"] =np.nan

1. How is the district summary affected?
2. How is the school summary affected?
3. How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to the other schools?
4. How does replacing the ninth-grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type

## Summary
