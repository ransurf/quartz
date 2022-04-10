---
title: CMPT 225 Assignments
aliases:
---
Status:
Tags:
Links: [) CMPT 225 - Data Structures and Programming](out/-cmpt-225-data-structures-and-programming.md)
___

# CMPT 225 Assignments

## 1
- [ ] Add list destructor
- [ ] proper commenting
- [ ] descending order
### Questions
-   modify a patient's record (for example, adding the patient's information or making a change of address, etc...).
	-   Is setParam() enough? or do we have to provide a console interface where they have to select what they want to change
### Info
[Link](https://www2.cs.sfu.ca/CourseCentral/225/alavergn/Assignments/1/Assignment_1.html)

- Design and implement a List (data collection) abstract data type (ADT) class that satisfies a set of given requirements.
- Apply the 4 steps of the software development process while creating an object-oriented (OO) solution to a problem.
- manage the medical records of all the patients of the walk-in clinic
	- patient's name (first and last name), address, phone number, email address and care card number.

- enter a new patient into the system
- remove a patient from the system
- search for an existing patient
- modify a patient's record (for example, adding the patient's information or making a change of address, etc...).
- print all its patients by descending order of care card numbers.
	```sh
		9234567890 - Patient: To be entered, To be entered, To be entered, To be entered
		6789012345 - Patient: Louis Pace, 98 West Fort Coquitlam, 604-853-0000, louis@nowhere.com
		3456789012 - Patient: Xiao Wong, 32487 16th Street Surrey, 778-778-7788, xw123@coldmail.com
		2345678901 - Patient: Marie Lower, 123 A Ave Vancouver, 778-123-1234, marie@somewhere.ca
	```

### Requirements
- [ ]  Each of your files must contain a comment header block composed of filename, class description, class invariant (if any), author, date of creation.
- [ ]  All your class methods (public and private) must have appropriate documentation: 
	- a description
	- a precondition (if any)
	- a postcondition (if any). 
	- must appear in the header file (.h) **and** in the class implementation file (.cpp) of each of your classes.
- [ ]  The file that represents the walk-in clinic patient system, i.e., the file that contains the _main_ function must be called **walkIn.cpp**.
- [ ]  Download [Patient.h](https://www2.cs.sfu.ca/CourseCentral/225/alavergn/Assignments/1/Patient.h) and [Patient.cpp](https://www2.cs.sfu.ca/CourseCentral/225/alavergn/Assignments/1/Patient.cpp). As you read through them you will notice that they are incomplete. You need to complete them following the requirements and hints included in these files.
	- [ ]  Add more parameterized constructors to the Patient class.
	- [ ]  Your solution must not make use of already existing container classes such as the STL vector class, etc... You cannot use STL in this assignment.
- [ ]  Download [List.h](https://www2.cs.sfu.ca/CourseCentral/225/alavergn/Assignments/1/List.h) and read its content. You can add more data members/methods to this class, but you cannot remove its data members/methods nor can you change them.
	- [ ]  Your List must be implemented using a dynamically allocated array.
	- [ ]  The print method of the List class must have a time efficiency of O(n) where n is the number of elements in the List. Note: What does this imply for the rest of the methods of List?
- [ ]  All the classes you create and use as part of your solution must be designed and implemented as abstract data type (ADT) classes.
- [ ]  Your solution must not break any of the class invariants.
- [ ]  Finally, make sure your code satisfies the _Good Programming Style_ described on the Good Programming Style web page of our course web site.
___

### S2 - Design
### TODO
- [ ] List Constructor troubleshooting
	- Why it like this bruh
### Questions
- By including more parameters, do you want it to slowly increment
- max list size?
# Backlinks
```dataview
list from [CMPT 225 Assignments](out/cmpt-225-assignments.md) AND !outgoing([CMPT 225 Assignments](out/cmpt-225-assignments.md))
```
___
References:

Created:: 2022-01-22 15:40
