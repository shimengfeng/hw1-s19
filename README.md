# Homework 1

* Assigned: 1/24
* Due:
    * Part 1: 1/31 10AM
    * **Part 2: 2/12 10AM**
* Value: 3.75% of your grade
* Done and submitted individually (as with all the homeworks) **via [Gradescope](https://www.gradescope.com),  (Entry code for gradescope: )**

# Part 1

## 1.1. (5 points) Database Design: UniDB


You will design a database for an Ivy League university (of some sort). 
This database will include information about departments, students, courses (and their offerings):

* Information about **students** includes their UNI, name and age. The UNI of a student is assumed to be unique, not shared by any other student. Each student is either a **graduate** or or an **undergraduate**. Students should be at least 18 years old to be admitted to university.

  * Each student must be in one category or the other, and cannot be in both categories simultaneously.
  * For graduate students, we record what their research field is. 
  * For undergraduate students, we record their concentration.

* Information about **departments** includes their name and address. The name of a department
  is assumed to be unique, not shared by any other department.

* We need to be able to associate student with the departments with which they
  are affiliated. Each student has to be affiliated with exactly one department.

* Information about a course includes its number (e.g., "4111"), name (e.g.,
  "Introduction to Databases"), and capacity (e.g., 140). 
  We also need to be able to know the unique department that owns each course: 
  no cross-listing of courses across departments is allowed, and every course is 
  owned by exactly one department. 

  * **Note/hint**: you cannot assume that course number uniquely identifies a course; in fact, you
    cannot assume even that course number together with course name uniquely
    identify a course. However, course number uniquely identifies courses *within a
    department*.

* Finally, we need to note which professors teach each course. Note that a course can be taught by more than one professor (that is, Professors Wu and Gravano both teach Introduction to Databases).

* Assume that for a course to be offered, it has at least one student enrolled and has a professor. 

* Finally, assume that a student can take courses “owned” by departments with which the student is not affiliated. And a student should be enrolled in at least one course.

**Your Task**: Render the university database in the version of the
E/R model that we studied in class, with exactly the constraints and requirements
specified above. 

* Please state any assumptions that you make, but make sure that
  you don’t introduce new constraints that are not listed in the problem definition.
* **Note/hint**: a weak entity set is a “regular” entity set in that it can
  participate in relationship sets other than the identifying relationship set, just as any
  other entity set.


## 1.2. (5 points) More Database Design

GitHub is a web based Git repository hosting service that provides version control and source code management functionality. It provides several collaboarative features like bug tracking, task management, contribution analytics for every project. Handling big code-bases and with multiple people working on them, indeed becomes a tedious task, GitHub helps to make this exercise easier. GitHub’s bug tracker is called Issues, and has its own section in every repository. Issues are kind of like shared e-mails, and a great way to keep track of tasks, enhancements, and bugs for the projects. You may learn more about github issues at [Github-Issues](https://guides.github.com/features/issues/) 

Visit the issues page of any public repository on Github, For example visit [Tensorflow-Issues](https://github.com/tensorflow/tensorflow/issues). Analyze the page and the linked issue pages to understand its data requirements. 
Then, 
* design an E-R diagram for the website that captures its main functionality of issues, and comments.
* Include at least 4 entities, 4 relationships, and 3 constraints, in the same format as part 1 of this homework.
* 2 of the entities should be **Issues** and **comments**.  You are free to choose the other two.
* For each entity, relationship and constraint, include a 1-2 sentence description that justifies your decision to include it and design it in the matter that you did.


# Part 2

## 2.1. (5 points) Database Design: UniDB Schema

* Show the SQL CREATE TABLE statements needed to convert your E/R diagram **from item 1.1** into a relational schema. If your translation cannot capture any of the constraints in the E/R diagram, explain why.
