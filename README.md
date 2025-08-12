# JOINS-PRACTICE-TASK-1
Table-1 Student Table

QUERIE FOR  CREATING TABLE AND INSERTING VALUES FOR TABLE-1 :
CREATE TABLE Students (
    StudentID INT PRIMARY KEY,
    Name VARCHAR(50),
    CourseID INT
);

INSERT INTO Students (StudentID, Name, CourseID) VALUES
(1, 'Alice', 101),
(2, 'Bob', 102),
(3, 'Charlie', 103),
(4, 'Diana', NULL);

|studentid |  name    | courseid   |
|----------|----------|------------|
|    1     |  Hindu   |   101      |
|    2     |   Chandu |   102      |
|    3     |   Yoshi  |   103      |
|    4     |   Laddu  |   NULL     |

 Table-2 Course Table

QUERIE FOR CREATING TABLE AND INSERTING VALUES FOR TABLE-2 :

CREATE TABLE Courses (
    CourseID INT PRIMARY KEY,
    CourseName VARCHAR(50)
);

INSERT INTO Courses (CourseID, CourseName) VALUES
(101, 'Python'),
(102, 'Java'),
(104, 'Data Science');
 
|Courseid |Coursename    |
|---------|--------------|
| 101     | Python       |
| 102     | Java         |
| 104     | Data Science |

JOINS QUERIES AND OUTPUTS:

1.INNER JOIN :

Q: SELECT Student.name,Course.Coursename FROM Student INNER JOIN Courses ONStudent.Courseid=Course.Courseid;

OUTPUT:

|Name  | Coursename |
|------|------------|
|Hindu |  Python    |
|Chandu|  Java      |

EXPLAINATION: Only matching Courseids between Student and Course are shown.

2.LEFT JOIN :

Q: SELECT Student.name,Course.Coursename FROM Student LEFT JOIN Course ON Student.Course.Courseid;

OUTPUT :

|Name  |Coursename |
|------|-----------|
|Hindu | Python    |
|Chandu| Java      |
|Yoshi | NULL      |
|Ladddu| NULL      |

EXPLAINATION: Shows all student,even if their Courseid doesn't match.

3.RIDHT JOIN :

Q: SELECT Student.name,Course.Coursename FROM Student ROGHT JOIN Course ON Student.Courseid=Course.Courseid;

|Name  |Coursename   |
|------|-------------|
|Hindu | Python      |
|Chandu| Java        |
|NULL  | Data Science|

EXPLAINATION: Shows all Course,even those with no studnet.

4.FULL OUTER JOIN :

Q: SELECT Student.name,Course.Coursename FROM Student FULL OUTER JOIN Course ON Studnet.Courseid=Course.Courseid;

|Name   |Coursename   |
|-------|-------------|
|Hindu  | Python      |
|Chandu | Java        |
|Yoshi  | NULL        |
|Laddu  | NULL        |
|NULL   | Data Science|

EXPLAINATION: Combines results of LEFT and RIGHT JOIN -all records from both tables.












