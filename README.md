# CSx278-Asgn5-CheckMyGrades

After conducting interviews with three different students at Vanderbilt, it was clear that all of them shared similar complaints about the difficulty of checking grades on Brightspace. The site is cluttered with an unreasonable number of tabs and poor organization. Simply checking grades requires a series of clicks and does not show your actual class average or standing. They all expressed interest in a texting bot that returns your grades when you send it a message. With people spending so much time on their phones now, creating this option is a natural extension of the way the world is moving. 

In terms of the functionality sought by the interviewees, the primary desire was for a method to retrieve recent grades. Additional features include filtering by class and update text notifications. Student 3 pointed out that part of the problem was the fault of professors, not necessarily with the web site itself, so this application will not end up fixing all the problems associated with keeping up with grades.

Overall, the students surveyed found significant issues with the current system of checking grades on Brightspace. This new application will reply to a text message and return the most recent assignments in a particular class for a student. This will be the core function of the application, but other things such as returning the category of the assignment and the percentage of the grade that category is worth will also be implemented. 


# Questions:
1. What complaints, if any, do you have about Brightspace? 
2. How often do you check your grades?
3. How do you currently keep up with your grades in your classes?
4. Why do you keep up with your grades that way?
5. Would you text a bot that returned your grades on recent assignments?
6. When/Why would you use this over Brightspace?
7. Is there any additional information you would want that bot to return?
8. Would you like to have the option to specify which class you are searching in, or just have all recent grades returned?
9. Is a two-week history of grades enough or would you prefer the last ‘x’ number of assignments?
10. Would you like text notifications to be automatically sent to you?

# Answers:

## Question 1:
1. Brightspace is not good for seeing what your grades are. The gradebook is hard to navigate to and difficult to read when you do find it.
2. Very cluttered and has too many tabs.
3. Teachers take forever to post grades. I’d like to see my current average in different categories.


## Question 2:
1. Once a week I will probably check my gradebook.
2. I look whenever I see a notification, but I look at the gradebook every week or so.
3. Once a day.


## Question 3:
1. I do not consistently check my grades, but when I do, I generally look at my printed copy of a syllabus and check the physically returned papers.
2. Usually I set up an excel sheet with received grades and projections for my averages and future assignments.
3. I look at Brightspace and compute averages myself.


## Question 4:
1. I don’t really like the layout of Brightspace, and the colors are ugly.
2. I like to know how I am standing in the class.
3. I like to plan for the future.


## Question 5:
1. Yes, absolutely.
2. Probably not. I think checking my Brightspace would be just as quick.
3. Yes, I would.


## Question 6:
1. It gets straight to the point of what I want. Currently, I must make a series of clicks to get similar information on Brightspace.
2. If I get automatic messages I would use this over Brightspace.
3. If I am on my phone rather than a computer.


## Question 7:
1. Upcoming quizzes, tests, or assignments.
2. Notifications for future assignments.
3. Information for upcoming assignments.


## Question 8:
1. Yes, that sounds good.
2. Yes, having those options would be helpful.
3. I would like to have that option to specify the class.


## Question 9:
1. It depends on the class, but in general I think the latter option is better. Some courses have relatively few assignments, and I think the point of this would be to see how you are doing in the class right now.
2. I would rather have the ‘x’ number of assignments returned.
3. I would rather see my scores for the last ‘x’ number of assignments.


## Question 10:
1. I wouldn’t mind having that option, but I prefer being the one who initiates it.
2. Yes, that would probably be the main reason I would want this service to exist.
3. Yes, automatically would be ideal.

# Requirements

## Goals
1. Provide simpler alternative for keeping up with grades
2. Provide more information to users than just the grade for a single assignment
3. Allow for as many customization options as possible
4. Simple inputs and intuitive user interface
	
## Functionality
1. Find secure method for linking student account to a cell phone
2. Options for determining the data being output
	⋅⋅* How many grades do you want returned?
	⋅⋅* Set to return the grades from the past 2 weeks
	⋅⋅* Set to return 5 most recently input grades
	⋅⋅* Percentage of grade the category of the assignment is worth (e.g. quizzes are 15%)
3. Potential concerns to handle
	⋅⋅* Student sends invalid class identifier (e.g. misspells word or uses wrong number)
	⋅⋅* Student drops a course, or the semester ends
4. Implement option for automatically generated messages when new grades are posted

# Development Approach

## User Perspective
After conducting interviews, I discovered that potential users of this application are seeking a simple way to keep up with their grades without the hassle of navigating Brightspace. They find the current system to takes way too many clicks to find a gradebook and limited information about their semester progress without looking towards the syllabus manually.

## Development Summary/Rationale
This new application will become an extension of Brightspace in which you simply add a phone number to your account when logged in that you can then send messages from. This ensures security of accounts. During development, it is important to consider minimizing the need for excessive input to receive the desired output. For this reason, this program will simply take in a message with the class identifier (e.g. CS 1101-01) and return the ‘x’ most recent graded assignments as applicable. This number will be defaulted to 5 but can be raised or lowered at the discretion of the user. When testing it is important to make sure the message is easily legible and has the appropriate information based off user preferences. Each part of this application will be developed in an individual function to ensure unit testing is simple and efficient. In terms of maintaining this application, consistently surveying users is critical to pointing out the current issues and brainstorming potential solutions. Having too much or too little information or required input defeats the purpose of this project. Overall, the goal of this application is to be as simple and customizable as possible.


