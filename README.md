q# School District Analysis

## Overview of the School District Analysis
The purpose of this analysis was to organize the data to provide insight on how certain variables effect student outcomes.  Multiple Data Frames were created to show student outcomes by school, school spending per student, school size, and school type.  All of these variables play important roles in student development that is quantitatively measured by overall passing percentage of the students.  With the data organized in this fashion it makes it easy to identify the primary factors that influence student success.  Additionally, there was an incidence of cheating at one particular high school, Thomas High School, and those grades needed to be removed to validate the dataset. 

## Results

*  The school district summary was barely affected by having the ninth grade data from Thomas High School removed.  The numbers were essentially unchanged and this is probably due to the fact that the district summary is averaging all the schools together.  This makes the adjusted test scores of one school insignificant to the entire dataset
   
* The difference between the unadjusted school summary and adjusted school summary for Thomas High School was drastic.  Obviously, when the entire 9th grade scores are replaced with NANs it will drastically skew the average passing rate of the entire school towards zero.  The skew can be seen between the dataframes presented below.
    ###### The Unadjusted DataFrame: 9th Grade Scores Replaced with NAN
    ![unadjusted_df](/Users/robertyokabaskas/Desktop/Class/School_District_Analysis/Resources/unadjusted_df.png)
    
    ###### The Adjusted DataFrame: 9th Grade Scores from Thomas High School were Removed from the Dataset Analysis
    ![adjusted_df](/Users/robertyokabaskas/Desktop/Class/School_District_Analysis/Resources/adjusted_df.png)
    
* This very much affects the standing of Thomas High School in the school district rankings.  Under normal circumstances, Thomas High School stands at #2 in the district rankings.  However, with the 9th grade scores being factored in as NANs the school comes in at the #8 spot in the district rankings. 

* Replacing the ninth grade scores caused major changes in the dataset for Thomas High School.  As far as the math and reading scores by grade, everything was unchanged except for the scores of the 9th grade, that were replaced with NaNs.  This essentially deems the grades as Null or 0.  Since these grades are not factored in, when the averages are calculated to create the Overall passing percentage based on the total students, the school overall passing percentage plummets.  This causes Thomas High School to drop in the school district ranking by school spending, school size, and school type.  However, if the 9th grade is dropped completely from the Thomas High School Analysis.  The data remains almost completely unchanged. 

## Summary
The main changes that occur in reading and math scores is major drops in all of the relevant metrics for the school.  Although the reading and math scores for the school remain unchanged, the passing percentages for the school, which are used for primary ranking of the school within the district, drop below 70.  This causes a massive skew in the data for the distributions by school size, school type, and spending per student.  This is why the data for the entire 9th grade at Thomas High School, including the 9th grade from the total student count, had to be dropped.  If the 9th grade scores are dropped, but the total student count including the 9th grade is still being used to derive all of the metrics, the data for the school becomes so heavily skewed that you might as well just drop the school from the entire dataset.  Once the DataFrames are adjusted to only factor in the 10th-12th grade students at Thomas High School the DataFrames are much more reliable and valid for representing the School.  However, Until the data can be corrected for academic dishonesty, there should be some sort of identifier for Thomas High School to indicate an incomplete or questionable dataset.
