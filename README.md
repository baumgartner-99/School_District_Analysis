# School District Analysis

## Overview
The purpose of this analysis was to analyze school district data for a local school board. The data included information such as size, student grades, and other performance metrics. However, there were rumors circulating about a specific high school having invalid scores due to academic dishonesty. The same analysis had to be done without these invalid data points from 9th graders at Thomas High School.

## Results
* The first step in this analysis was to clean the data by removing prefixes and suffixes from student names, as these additions would cause contradition to the students' official files. 
* Another step to cleaning the data was removing the data points from the alleged dishonest sutudents. These numbers needed to be replaced with NaN's using a python package, NumPy. 
* Finally, the district analysis could be performed again. Here are some specific metrics that changed:
  * Total student count went from 39,170 students to 38,709 students.
  * Passing percentage did not change much, due to the relatively small size of the entire district that was affected.
    * Passing math percentage before the error was around 74.98% while post-removal was 74.76%.
    * Passing reading percentage before the error was around 85.81% while post-removal was 85.66%.
    * We can conclude that district passing percentages were adjusted by less than a percentage point.
* Next, we can review the school summary. This is where we see a larger adjustment in those percentage points. For instance, each of our passing percentages for Thomas High School students fall between 65% and 70% after the removal of 9th grade scores. However, when we remove those 9th graders from the total student count at Thomas High School and just measure performance of 10th-12th graders, we see a drastic increase in our passing percentages that are now between 90% and 98%. 
* Overall, replacing those ninth grade scores does not have a large impact on Thomas High School's performance relative to other schools, *if* we take our percentage from 10th-12th graders. Of course, including the whole school with 9th graders having null values will bring Thomas High School's performance down.
* As for math and reading scores by grade, scores by school spending, scores by school size, and scores by school type... all of these metrics are largely unaffected by the academic dishonesty alleged on Thomas High School ninth graders. 

## Summary
To summarize, here are four metrics that changed in the school district analysis as a result of replacing ninth grade scores at Thomas High School with NaNs: 
  * total student count decreased by 461 students. 
  * Passing math percentage changed by .28%.
  * Passing reading percentage changed by .15%.
  * The overall passing percentage changed from 65.17% to 64.86%. 
