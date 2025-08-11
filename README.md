# JOINS-PRACTICE-TASK-1
Table-1 Student Table
|studentid |  name    | courseid   |
|----------|----------|------------|
|    1     |  Hindu   |   101      |
|    2     |   Chandu |   102      |
|    3     |   Yoshi  |   103      |
|    4     |   Laddu  |   NULL     |

 Table-2 Course Table
|Courseid |Coursename    |
|---------|--------------|
| 101     | Python       |
| 102     | Java         |
| 104     | Data Science |

JOINS QUERIES AND OUTPUTS:

1.INNER JOIN :

SELECT Student.name,Course.Coursename FROM Student INNER JOIN Courses ONStudent.Courseid=Course.Courseid;

OUTPUT:

|Name  | Coursename |
|------|------------|
|Hindu |  Python    |
|Chandu|  Java      |

2.LEFT JOIN :

SELECT Student.name,Course
