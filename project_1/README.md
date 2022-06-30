# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Problem Statement

This project aims to explore trends in SAT and ACT participation and score data by state in 2017-2019 and make recommendations to increase SAT participation rates.

## Executive summary
SAT and ACT are standardized exams that are frequently used in the United States for determining entrance to colleges.  As the SAT and ACT are equally challenging, most colleges don't favor one test over another when choosing applicants. The SAT test, however, predominates in some States, while the ACT test holds the majority of the states for a variety of reasons.

In recent years, the ACT has outperformed the SAT in terms of participation. In an effort to keep up with rising ACT participation rates across the United States, the redesigned SAT format was introduced in March 2016. The SAT underwent some significant design changes as part of an effort by the College Board to make the exam more relevant.  In order to raise SAT participation rates in the future, this project intends to identify relevant trends and approaches that the College Board might use to boost SAT takers by utilizing the data on SAT and ACT participation and score by state from 2017 to 2019.

### Key Findings: 

- SAT and ACT participation has a strong negative correlation
- There are more states having a 100% participation rate for ACT compared to SAT
- Participation and total/composite score have a strong negative correlation  
- There is a strong positive correlation on year on year participation
- The variables in the dataset are not normally distributed
- The state mandate, the fee waiver, or the SAT School Day program are the main causes of the rise in SAT participation rates.

## Conclusion and Recommendation

In order to replicate comparable techniques, the College Board should consider the states where SAT participation rates have increased noticeably. Due to the SAT exams becoming mandatory, participation rates in Illinois and Colorado have significantly increased. On the other hand, the SAT school day program helped Florida and West Virginia raise their participation rates. Additionally, several states also use Khan Academy as a free study resource and introduce exam fees waiver to attract more test takers.

This dataset also reveals that there is an inverse relationship between participation rates and ACT and SAT scores. While tests with high participation rates, for instance, because of fee waivers, test a lot of students from lower-income families who are unfamiliar with the exam setting or even do not really have a clear plan to enter college, tests with low participation rates test the best students who are well-prepared for the exam.
In order to adequately prepare students for this exam, the College Board needs to come up with fresh, creative solutions. One such concept is to collaborate with more online learning platforms to help students learn more extensively. To improve execution, a deeper investigation of the effectiveness of the SAT School Day and exam fee waiver is required.


## Data Dictionary
|        Feature        |   Type  |    Range   | Dataset      |                             Description                            |
|:---------------------:|:-------:|:----------:|--------------|:------------------------------------------------------------------:|
| state                 | object  | all states | combined_all | name of US states                                                  |
| sat17_participation   | float64 | 0-1        | combined_all | State SAT participation rate in 2017                               |
| sat17_reading_writing | int64   | 200-800    | combined_all | State average SAT Evidence-Based Reading and Writing score in 2017 |
| sat17_math            | int64   | 200-800    | combined_all | State average SAT Math score in 2017                               |
| sat17_total           | int64   | 400-1600   | combined_all | State average SAT total score in 2017                              |
| act17_participation   | float64 | 0-1        | combined_all | State ACT participation rate in 2017                               |
| act17_english         | float64 | 1-36       | combined_all | State average ACT English score in 2017                            |
| act17_math            | float64 | 1-36       | combined_all | State average ACT Math score in 2017                               |
| act17_reading         | float64 | 1-36       | combined_all | State average ACT Reading score in 2017                            |
| act17_science         | float64 | 1-36       | combined_all | State average ACT Science score in 2017                            |
| act17_composite       | float64 | 1-36       | combined_all | State average ACT Composite score in 2017                          |
| sat18_participation   | float64 | 0-1        | combined_all | State SAT participation rate in 2018                               |
| sat18_reading_writing | int64   | 200-800    | combined_all | State average SAT Evidence-Based Reading and Writing score in 2018 |
| sat18_math            | int64   | 200-800    | combined_all | State average SAT Math score in 2018                               |
| sat18_total           | int64   | 400-1600   | combined_all | State average SAT total score in 2018                              |
| act18_participation   | float64 | 0-1        | combined_all | State ACT participation rate in 2018                               |
| act18_composite       | float64 | 1-36       | combined_all | State average ACT Composite score in 2018                          |
| sat19_participation   | float64 | 0-1        | combined_all | State SAT participation rate in 2019                               |
| sat19_reading_writing | int64   | 200-800    | combined_all | State average SAT Evidence-Based Reading and Writing in 2019       |
| sat19_math            | int64   | 200-800    | combined_all | State average SAT Math score in 2019                               |
| sat19_total           | int64   | 400-1600   | combined_all | State average SAT total score in 2019                              |
| act19_participation   | float64 | 0-1        | combined_all | State ACT participation rate in 2019                               |
| act19_composite       | float64 | 1-36       | combined_all | State average ACT Composite score in 2019                          |