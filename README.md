# Predict Student Performance 
- Predicting students' academic performance and year-end exam scores using Linear Regression and K-NN models in Spark
Using PySpark framework, code on Jupiter Notebook
- Predicting academic performance can help schools and teachers gain a deeper understanding of students' learning characteristics and trends, enabling timely interventions and support. The results of this study may contribute to enhancing the learning experience and providing new development opportunities for students.

## Dataset
- Dataset contains demographic and academic performance data of Secondary Education (Highschool) students in Portugal, which corresponds to upper secondary education in Vietnam
- DataSource: https://www.kaggle.com/datasets/dillonmyrick/high-school-student-performance-and-demographics 

## Problem Description
- The KNN Regression and Linear Regression models are applied to predict students' final exam scores 
- The KNN Classifier model is used to determine whether a student is academically strong based on demographic factors

❖ Predicting students' final exam scores:

- Input: Scores from the previous two terms (grade_1, grade_2), along with students' demographic and academic information
- Output: The third-term or final exam score (final_grade)

❖ Predicting students' academic performance throughout the year:

- Input: Students' demographic and academic information
- Output: Academic performance (good or not, is_good)
- Classification criteria: 
■ A reference group is used based on the student classification method in Portugal [1]
■ All three term scores must be at least "fair" (14), or the scores must not decrease over the time, with the final score being at least "fair" 
■ The second criterion acknowledges students who have maintained and improved their academic performance throughout the year to achieve a strong final result

| First criterion  | Second criterion |
| --------------- | --------------- |
| (grade_1 + grade_2 + final_grade) / 3 >= 14 | final_grade >= 14 và final_grade >= grade_2 và grade_2 >= grade_1  |



[1] “Portugal Grading System.” Accessed: Jun. 02, 2024. [Online]. Available: 
https://www.scholaro.com/db/Countries/Portugal/Grading-System

