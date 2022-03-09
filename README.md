# School District Analysis
Analyzing performance trends in school's standardized testing

## Overview of the school district analysis:
The purpose of this analysis was to investigate math and reading performance of 15 schools within a district.  Further analysis was performed based on school type (district or charter) and per student budget.

## Detailed analysis and findings:
* How is the district summary affected?
  * Average math scores decreased from 79.0 to 78.9
  * Average reading scores did not reflect any noticeable change
  * % passing math decreased from 75.0% to 74.8%
  * % passing reading decreased from 85.8% to 85.7%
  * % passing both subjects decreased from 65.2% to 64.9%

* How is the school summary affected?
  * Average math scores for Thomas High School decreased from 83.42% to 83.35%
  * Average reading scores for Thomas High School increased from 83.85% to 83.90%
  * % passing math for Thomas High School decreased from 93.27% to 93.19%
  * % passing reading for Thomas High School decreased from 97.31% to 97.02%
  * % passing both subjects for Thomas High School decreased from 90.95% to 90.63%

* How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
  * The average reading scores for Thomas High School rose slightly. The school saw a decrease in average math scores and passing percentages in all categories (math, reading, overall).

* How does replacing the ninth-grade scores affect the following:
  * Math and reading scores by grade
    * Average math scores for Thomas High School decreased from 83.42% to 83.35%
    * Average reading scores for Thomas High School increased from 83.85% to 83.90%
    * % passing math for Thomas High School decreased from 93.27% to 93.19%
    * % passing reading for Thomas High School decreased from 97.31% to 97.02%
    * % passing both subjects for Thomas High School decreased from 90.95% to 90.63%

  * Scores by school spending
    * Thomas High School is categorized in this analysis in the ($630 to $644) spending range per student.  With that in mind, that category reflected the following:
      * Average math scores decreased from 78.52 to 78.50
      * Average reading increased from 81.62 to 81.64
      * % passing math decreased from 73.48% to 73.46%
      * % passing reading decreased from 84.39% to 84.32%
      * % passing both subjects decreased from 62.86% to 62.78%

  * Scores by school size
    * Thomas High School is categorized in this analysis as a medium sized school (1,000 - 2,000 students).  With that in mind, the medium sized school category reflected the following:
      * Average math scores decreased from 83.37 to 83.36
      * Average reading increased from 83.86 to 83.87
      * % passing math decreased from 93.60% to 93.58%
      * % passing reading decreased from 96.79% to 96.73%
      * % passing both subjects decreased from 90.62% to 90.56%

  * Scores by school type
    * Thomas High School is a charter school.  With that in mind, the charter school category reflected the following:
      * Average math and reading scores did not reflect any noticeable change
      * % passing math decreased from 93.62% to 93.61%
      * % passing reading decreased from 96.59% to 96.55%
      * % passing both subjects decreased from 90.43% to 90.39%

## Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
Excluding the scores from 9th graders at Thomas High School did not have a large impact on the overall analysis.  The analysis called for decimal place formatting to one point in a few areas but in order to see any impact at all, two were required in certain instances.  That being said, there was a slight decrease in all three categories (math, reading, overall) for passing percentage.  The same can be said for average math grades.

## References:
### Code examples:
`reading_ninth_grade_THS = student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"),"reading_score"] = np.nan`

`students_THS = student_data_df.loc[(student_data_df["school_name"] == "Thomas High School")]`

`students_THS_count = students_THS["Student ID"].count()`


## Database pics:
### Per School Summary: Original
![Per School Summary: Original](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/per_school_summary_without_nan.png);

### Per School Summary: Modified
![Per School Summary: Modified](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/per_school_summary_with_nan.png);

### District Summary: Original
![District Summary: Original](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/district_summary_without_nan.png);

### District Summary: Modified
![District Summary: Modified](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/district_summary_with_nan.png);

### Type Summary: Original
![Type Summary: Original](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/type_summary_without_nan.png);

### Type Summary: Modified
![Type Summary: Modified](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/type_summary_with_nan.png);

### Spending Summary: Original
![Spending Summary: Original](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/spending_summary_without_nan.png);

### Spending Summary: Modified
![Spending Summary: Modified](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/spending_summary_with_nan.png);

### Size Summary: Original
![Size Summary: Original](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/size_summary_without_nan.png);

### Size Summary: Modified
![Size Summary: Modified](https://github.com/tonyferri/School_District_Analysis/blob/main/Resources/size_summary_with_nan.png);