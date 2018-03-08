The following scripts handle data of academic courses from multiple data sources,
in order to summarize which students are not able to sign in to a certain course,
given this course has requirements they can handle (AKA pre-course they did not passed).

In order to manage this, the following files are provided :
- courses.list : an example for the expected format of list of courses and requirements,
				according to the following :
				Course ID | Course name | Points | Pre-courses required
				
- <CourseNumber>.course : an example for the expected format of registration list for a certain course
				according to the following :
				Student ID | Student name | Year and semester | student grade
				
Scripts are :

--1--
semesterialGrades <StudentId> <Semester>
Input : student id, semester.
Output : the grades of the student in this semester.

--2--
preCourses <CourseId>
Input : course id
Output : all the pre-courses that are required
(NOTE : if course X is pre-course of Y, and course Y is pre-course of Z,
then X is pre-course of Z and should take under consideration).

--3--
getStudents <CourseId> <Semester>
Input : course ID and semester
Output : all the students that are registered for the course and haven't pass all it's pre-courses

--4--
getCourses <Semester>
Input : semester
Output : all the courses that were tought in this semester