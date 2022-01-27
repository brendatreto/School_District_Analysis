# School District Analysis

## Overview of the school district analysis
After finishing the complete analysis for the district, we were notified of evidence of academic dishonesty in one of the schools included in the original assessment. The board decided to replace the school grades with NaNs and later decide what to do with those results. This decision means that we will repeat the analysis considering this modifications and compare how the results changed.

### Resources
Data Source: students_complete.csv, school_complete.csv
Software: Python 3.7.6, Jupyter Notebook

## Results
The first step was again to clean the data, we searched for missing values, and we remove prefixes and suffixes to work with only the students names in the **student_data** file.
In that same data frame we imported numpy and used the loc function to select all reading and math scores from Thomas High School 9th graders and replace them with NaN.

**Fig 1. Replacing Thomas High School 9th graders grade with NaNs**
![studentlocTH](https://user-images.githubusercontent.com/22451540/151423061-1d3b2bed-56f4-4336-b574-fee742cbd1a8.PNG)

Now that the **student_data** file was cleansed we merged the data frame with the school information in order to work with one single data frame that would provide information on the whole district. With this information we were able to find the new district summary.


1. How is the district summary affected?
The total number of schools, students and budget was not affected. However, the Average Math and Reading scores and, consequently the percentage of students passing math, reading and math and reading, decreased slightly.


**Fig 2. District summary before adjustment**
![District Summary](https://user-images.githubusercontent.com/22451540/151420442-89921a71-d907-460a-8a0a-1b746bffbec6.PNG)


**Fig 3. District summary after adjustment**
![District_summary(New)](https://user-images.githubusercontent.com/22451540/151419881-5305176a-eea3-44b0-aa7a-ac969506cfa9.PNG)

2. How is the school summary affected?
When whe ran again the summary by school we could verify that the only school that suffered changes was Thomas High School with a significant drop in the passing percentages. The percentage of overall passing went from 90.94% to 65.07% because with had not yet substracted the students with NaNs from the total count of students.
 
3. How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to the other schools?
Because we replaced the averages from Thomas High School substractin the ninth graders, there was not a significant shift in the placement relative to other schools. Thomas High School percentage of overall passing students went from 90.94% to 90.63% (not the 65.07% that considered the whole population of the school).

5. How does replacing the ninth-grade scores affect the following:
  - Math and reading scores by grade

**Fig 4. Math scores by grade before and after adjustment**

![mathbygrade](https://user-images.githubusercontent.com/22451540/151428454-b9e12c09-5e4f-474a-8fd4-794ec93e7cc9.PNG) ![Mathbygrade(new)](https://user-images.githubusercontent.com/22451540/151428467-c65b43df-acea-46c1-9eaf-4c99133f1d96.PNG)

As expected, there was no change in the other grades or in the other school, the only effect this new analysis had, was the NaN in ninth graders from Thomas High School. The same can be observed in reading scores by grade

**Fig 5. Reading scores by grade before and after adjustment**

![readingbefore](https://user-images.githubusercontent.com/22451540/151428900-72a0b138-0d97-4009-9db5-8d47d0a5e15b.PNG) ![Readingafter](https://user-images.githubusercontent.com/22451540/151428923-22a1ae3c-16a4-474b-a876-097fc15f98fe.PNG)

  - Scores by school spending
However, we ran the analysis once without replacing the grades and we discovered how the results would have been affected.

**Fig 6. Scores by school spending before and after adjustment**

![Spendingbefore](https://user-images.githubusercontent.com/22451540/151446149-7be5208a-dde0-4c9b-96ab-062a993aedde.PNG) 
![spendingafter](https://user-images.githubusercontent.com/22451540/151446159-d096b89c-64a1-4717-8e2d-ddbc13a31b59.PNG)

  - Scores by school size

**Fig 7. Scores by school size before and after adjustment**

![sizebefore](https://user-images.githubusercontent.com/22451540/151446236-8ba18358-a79f-43cd-ab31-6bc6fe52a590.PNG)
![sizeafter](https://user-images.githubusercontent.com/22451540/151446252-6e41ae1c-6697-4939-899c-1265d977429d.PNG)


  - Scores by school type
**Fig 8. Scores by school type before and after adjustment**

![typebefore](https://user-images.githubusercontent.com/22451540/151446291-01591634-82b4-4415-b0d0-cd788460e44d.PNG)
![typeafter](https://user-images.githubusercontent.com/22451540/151446298-f8950c07-165b-4ae8-9670-fb2a0f0e45aa.PNG)


## Summary
