```SQL
-- Basic Questions

-- 1st Question
SELECT COUNT(*) FROM student_grades_assignment;
-- 2nd Question
SELECT AVG(GRADE) FROM student_grades_assignment;
-- 3rd Question
SELECT MAX(GRADE) FROM student_grades_assignment;
-- 4th Question
SELECT MIN(GRADE) FROM student_grades_assignment;
-- 5th Question
SELECT COUNT(DISTINCT(StudentID)) FROM student_grades_assignment;
-- 6th QUestion
SELECT AVG(Grade),CourseID FROM student_grades_assignment
GROUP BY CourseID;
-- 7th Question
SELECT COUNT(StudentID) AS Total_Students,Department FROM student_grades_assignment
GROUP BY Department;
-- 8th Question
SELECT MAX(Grade) AS Max_Grade,CourseID FROM student_grades_assignment
GROUP BY CourseID;
-- 9th Question
SELECT MIN(Grade) AS Max_Grade,Department FROM student_grades_assignment
GROUP BY Department;
-- 10th Question
SELECT COUNT(CourseID) AS Number_of_Courses,StudentID FROM student_grades_assignment
GROUP BY StudentID;

-- Intermediate Questions

-- 11th Question
SELECT AVG(Grade),CourseID FROM student_grades_assignment
GROUP BY CourseID
HAVING AVG(Grade) > 75;
-- 12th Question
SELECT COUNT(CourseID) AS Number_of_Courses,StudentID FROM student_grades_assignment
GROUP BY StudentID
HAVING COUNT(CourseID) > 3;
-- 13th Question
SELECT AVG(Grade),Department FROM student_grades_assignment
GROUP BY Department
HAVING AVG(Grade) < 65;
-- 14th Question
SELECT MAX(Grade),StudentID FROM student_grades_assignment
GROUP By StudentID
HAVING MAX(Grade) = 100;
-- 15th Question
SELECT COUNT(StudentID) AS Number_of_Students,CourseID FROM student_grades_assignment
GROUP BY CourseID
HAVING COUNT(StudentID) >= 20;

-- Advanced Questions

-- 16th Question
SELECT COUNT(CourseID) AS Number_of_Courses,AVG(Grade),StudentID FROM student_grades_assignment
GROUP BY StudentID
HAVING COUNT(CourseID) >= 4 AND AVG(Grade) > 80;
-- 17th Question
SELECT Department,MAX(Grade) FROM student_grades_assignment
GROUP BY Department
HAVING MAX(Grade) >= AVG(Grade) * 2;
-- 18th Question
SELECT CourseID,AVG(Grade) FROM student_grades_assignment
GROUP BY CourseID
HAVING AVG(Grade) > (SELECT AVG(Grade) FROM student_grades_assignment);
-- 19th Question
SELECT StudentID,MIN(Grade) FROM student_grades_assignment
GROUP BY StudentID
HAVING MIN(Grade) > 70;
-- 20th Question
SELECT StudentID,MIN(Grade) FROM student_grades_assignment
GROUP BY StudentID
HAVING MIN(Grade) < 70;
```
