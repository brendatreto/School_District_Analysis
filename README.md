# School District Analysis

## Overview of the school district analysis
After finishing the complete analysis for the district, we were notified of evidence of academic dishonesty in one of the schools included in the original assessment. The board decided to replace the school grades with NaNs and later decide what to do with those results. This decision means that we will repeat the analysis considering this modifications and compare how the results changed.

### Resources
Data Source: students_complete.csv, school_complete.csv
Software: Python 3.7.6, Jupyter Notebook

## Results
The first step was again to clean the data, we searched for missing values, and we remove prefixes and suffixes to work with only the students names in the **student_data** file.
In that same data frame we imported numpy and used the loc function to select all reading and math scores from Thomas High School 9th graders and replace them with NaN.

*student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "reading_score"] =np.nan*

Now that the **student_data** file was cleansed we merged the data frame with the school information in order to work with one single data frame that would provide information on the whole district. With this information we were able to find the new district summary.

1. How is the district summary affected?
The total number of schools, students and budget was not affected. However, the Average Math and Reading scores and, consequently the percentage of students passing math, reading and math and reading, decreased slightly.

**Fig 1. District summary before adjustment
![District Summary](https://user-images.githubusercontent.com/22451540/151420442-89921a71-d907-460a-8a0a-1b746bffbec6.PNG)

**Fig 2. District summary after adjustment
![District_summary(New)](https://user-images.githubusercontent.com/22451540/151419881-5305176a-eea3-44b0-aa7a-ac969506cfa9.PNG)

2. How is the school summary affected?


3. How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to the other schools?
4. How does replacing the ninth-grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type

## Summary
