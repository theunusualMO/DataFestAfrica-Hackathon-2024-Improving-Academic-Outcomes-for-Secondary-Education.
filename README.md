# DataFestAfrica-Hackathon-2024-Improving-Academic-Outcomes-for-Secondary-Education.
Improving Academic Outcomes for Secondary Education.

### Project Overview

This project aims to analyze various factors affecting academic outcomes for secondary education and provide data-driven recommendations for improvement. The analysis includes student demographics, study habits, family size, and internet access etc.

### Data Source
Nigeria Student Performance: The primary dataset used for this analysis is the "Nigeria_student_performance_dataset.csv" file, contaning student performance records. 
[Here](https://docs.google.com/spreadsheets/d/1xZGybnQNC9rbJv4fwhaxdepCrPvxyBDZRZ0-dZaBKBw/edit?gid=694029794#gid=694029794)

### Tools
- Excel - Data Cleaning, Excel Formulas (IF etc.)[Download here](https://microsoft.com)
- Power BI- Data Visualization, Dashboard Building,  [Download here](https://www.microsoft.com/en-us/power-platform/products/power-bi/desktop)


### Data Description

Columns:

A. Sex: Gender of the student

B. Age: Age of the student

C. Medu: Mother's education level

D. Fedu: Father's education level

E. Studytime: Study time per week

F. Famsize: Family size

G. SS3_mock_result: Results of the mock exams

H. Absences: Number of absences

I. Internet_access: Internet access at home

J. Pstatus: Parental Status

K. Extra Tutoring

L. School Support

M. CBT Preparation

N. CBT Outcome

O. Health Status

P. Wants Higher Education

Q. Wants Trade

R. SS1 Results

S. SS2 Results

### Key Performance Indicators (KPIs)

1. Average Academic Performance:
~~~ sql
AVERAGEX(Nigeria_student_performance_dataset,(Nigeria_student_performance_dataset[SS1 Result Avg] + Nigeria_student_performance_dataset[SS2 Result Avg])/ 2)
~~~

2. Pass Rate Mock:
~~~ sql
DIVIDE(
COUNTROWS(FILTER(Nigeria_student_performance_dataset,Nigeria_student_performance_dataset[SS3 Mock Result] = "pass")), COUNTROWS(Nigeria_student_performance_dataset),
0
)*100
~~~

3. Absenteeism Rate:
~~~ sql
COUNTROWS(FILTER(Nigeria_student_performance_dataset, Nigeria_student_performance_dataset[Absences]> 10)) / COUNTROWS(Nigeria_student_performance_dataset)
~~~

4. Percentage of Students Wanting Higher Education:
~~~ sql
COUNTROWS(FILTER(Nigeria_student_performance_dataset,Nigeria_student_performance_dataset[Wants Higher Education] = "Yes")) / COUNTROWS(Nigeria_student_performance_dataset)
~~~

5. Percentage of Students Wants Trade:
~~~ sql
COUNTROWS(FILTER(Nigeria_student_performance_dataset,Nigeria_student_performance_dataset[Wants Trade] = "Yes")) / COUNTROWS(Nigeria_student_performance_dataset)
~~~

6. Total_SS1_Average:
~~~ sql
AVERAGE(Nigeria_student_performance_dataset[SS1 Result Avg])
~~~

7. Total_SS2_Average:
~~~ sql
AVERAGE(Nigeria_student_performance_dataset[SS2 Result Avg])
~~~

8. Total Students:
~~~ sql
COUNTROWS('Nigeria_student_performance_dataset')
~~~ 

## Detailed Overview Of The Analysis

### Chart Visualization Requirements

### A. Academic Performance Analysis

Line Chart:

X-axis: Academic levels (SS1, SS2).

Y-axis: Average academic performance.

Goal: Show the academic trend 

Donut Chart:

Categories: Total Students by SS3 Mock

Goal: Showing the percentage of students who passed vs. failed the SS3 mock exam.


### B. Effect of Study Time and Tutoring

Donut Chart:

Categories: Total Students by Study Time

Goal: Showing the proportion of students in each study time category.

### C. Attendance and Academic 

Pie Chart:

Categories: Absence, SS3 mock results.

Goal: Show how student absences impact their academic outcomes.

### D. CBT Preparation and Outcome

Stacked Bar Chart:

X-axis: CBT_preparation (categorized).

Y-axis: CBT_outcome (pass/fail).

Goal: Visualize how different levels of CBT preparation affect the outcome.

### E. Parent Education and Total Student

Stacked Bar Chart:

X-axis: Total Student

Y-axis: Father Education, Mother Education

Goal: Show how parental education levels impact student success.

### F. Health and Total Students

Stacked Column Chart:

X-axis: health_status.

Y-axis: Total Student.

Goal: Show the impact of health on academic outcomes.

### G. Student Aspirations

Donut Chart:

Categories: wants_higher_education, wants_trade.

Goal: Show the proportion of students aiming for higher education vs. trade and compare their academic performance.

### H. Support and Internet Access

Pie Charts:

Categories: total student, internet_access.

Goal: Analyze the effect of support and access to the internet on student outcomes.

### I. Total Student by Family size and Internet access

Clustered Bar Chart:

X-axis: Total Students

Y-axis: Family size

Legend: Internet Access

Goal: Emphasize the relative proportions of students across different family size categories.

### J. Interactive Features

Slicers: Sex, Age to filter data dynamically.


## Dashboard Overview

![image](https://github.com/user-attachments/assets/0d8e0e34-4341-43ac-8dfb-551ad4ee9649)


### Recommendations
- Implement tutoring programs for students studying less than 2 hours.
   
- Enhance internet access for students to facilitate online learning.

- Students from larger families may have different support systems and resource availability compared to those from smaller families.
  
- Higher parental education levels appear to positively influence student performance.
  
### Conclusion

This project looked at what affects students’ school performance. We found that students who study more and have parents with higher education tend to do better in their exams. Many students are not studying enough, which is a concern.
To help students succeed, we recommend offering more study support and getting families involved in their education. By doing this, we can create a better learning environment for everyone.















