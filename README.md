# SkillForge

![бдшка2 drawio](https://github.com/user-attachments/assets/4e7cfc57-464a-4b1f-a03f-826d1ac9a59b)

# Entities:

1. **User**
   - `UserID`: Unique identifier for the user.
   - `Name`: Full name of the user.https://docs.google.com/spreadsheets/d/1VF3Td7vuCADhkz2BbyLQ9nim5Bhje89xxYjQazH4Jhc/edit?gid=0#gid=0
   - `Email`: Contact email address.
   - `Password`: Encrypted user password.
   - `Role`: Role of the user (e.g., student, teacher, admin).

2. **Profile**
   - `ProfileID`: Unique identifier for the profile.
   - `UserID`: Foreign key referencing the User.
   - `Bio`: Short biography of the user.
   - `SocialLinks`: Links to social media or personal websites.

3. **Course**
   - `CourseID`: Unique identifier for the course.
   - `Title`: Name of the course.
   - `Description`: Brief course overview.
   - `StartDate`: Course start date.
   - `EndDate`: Course end date.
   - `TeacherID`: Foreign key referencing the teacher (User).

4. **Lesson**
   - `LessonID`: Unique identifier for the lesson.
   - `CourseID`: Foreign key referencing the Course.
   - `Title`: Name of the lesson.
   - `VideoURL`: Link to any associated video.

5. **Resource**
   - `ResourceID`: Unique identifier for the resource.
   - `LessonID`: Foreign key referencing the Lesson.
   - `Title`: Name of the resource.
   - `FileURL`: Link to the resource file.

6. **Tag**
   - `TagID`: Unique identifier for the tag.
   - `Name`: Name of the tag.

7. **Enrollment**
   - `EnrollmentID`: Unique identifier for the enrollment record.
   - `UserID`: Foreign key referencing the User.
   - `CourseID`: Foreign key referencing the Course.
   - `EnrollmentDate`: Date when the user enrolled in the course.

8. **Exam**
   - `ExamID`: Unique identifier for the exam.
   - `CourseID`: Foreign key referencing the Course.
   - `Title`: Name of the exam.
   - `ExamDate`: Date of the exam.

9. **Question**
   - `QuestionID`: Unique identifier for the question.
   - `ExamID`: Foreign key referencing the Exam.
   - `Content`: The question content.
   - `QuestionType`: Type of the question.

10. **Answer**
    - `AnswerID`: Unique identifier for the answer.
    - `QuestionID`: Foreign key referencing the Question.
    - `UserID`: Foreign key referencing the User who answered.
    - `AnswerContent`: Content of the answer.
    - `IsCorrect`: Boolean indicating whether the answer is correct.
   
# Functionality:

**Student**
   - Student: Can Register, Login and Enroll on the course.
   - Teacher: Can Register, Login, Enroll on the course and create their own courses, review students' results.
   - Admin: Editing and approving courses, banning/unbanning users.
