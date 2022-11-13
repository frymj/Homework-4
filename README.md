# Homework-4
Birthday Problem

Premise
Many of you have likely heard of the Birthday Problem Links to an external site.in the context of probability. In short, it says that if you have  people together, and assume birthdays are equally distributed across all 365 days in a year (sorry leap day people), what is the probability at least two will share a birthday? 

It turns out, once n > 30, this probability exceeds 0.5. 

In this assignment, we will study the distribution of how many days match (or repeat) given a collection of  individuals. So for example, suppose 6 people are in a room together, we may get the following outcomes:

All 6 have unique birthdays, thus 0 matches.
2 people share a birthday, and everyone else has a unique birthday, thus 1 match.
3 people share a birthday, and the other 3 people have unique birthdays, thus 1 match.
2 people share a birthday (say March 14) and another 2 people share a birthday (say July 22), and the others have unique birthdays, thus 2 matches.
3 people share a birthday (say March 14) and 2 others share a different birthday (say July 22), with the sixth person different, thus 2 matches.
3 people share a birthday (say March 14) and the other 3 share a different birthday (say July 22), thus 2 matches.
2 people share a birthday (say March 14), 2 others share a different birthday (say July 22) and 2 others share yet another birthday (say Oct 31), thus 3 matches.
4 people share a birthday, and the other 2 people have unique birthdays, thus 1 match.
4 people share a birthday (say March 14), with the other 2 people sharing a different birthday (say July 22), thus 2 matches.
5 people share a birthday (say March 14), with the other person having a different birthday, thus 1 match.
All 6 people share the same birthday, thus 1 match.
Stated Problem
Write a function in R that randomly generates a number of birthdays and determines how many matches there are (provided above is an example). Use this function to study the distribution of the number of matches as a function of the number of people that are together.

Coding specifics
You function must accept the following parameter:

num_people corresponding to the number of people that are together, default value of 23
Your function shall return a single value:

the number of days that have a match (see outline above for an example)
Demonstrate that your function works by simulating 100,000 iterations of the process with the following details:

Set the random number generate seed to 314159 before each run of 100,000 iterations
Run the simulation 10 times: for num_people equal to 10, 20, 30, 40, 50, 60, 70, 80, 90 and 100 people.
Provide the summary() output and a bargraph for each of the simulation runs
Comment (as a comment or text in an Rmd) about the distribution of the number of matches
Some hints and pointers
Use Julian days for the birthdays (Jan 01 is 1, Jan 02 is 2, .... Feb 26 is 57, Feb 27 is 58, ..., April 15 is 105, ..., Oct 31 is 305, ..., Dec 31 is 365).
Think of it like "rolling a 365-sided die" num_people times to generate the birthdays!
To determine the number of matches, the following functions in R may be helpful:
unique()
duplicated()
For plotting you can use hist(), but it is not quite correct given the context. You should use a combination of:
table()
barplot()
Directions
Submit a GitHub Repo URL that includes your completed code (either a .R or .Rmd file). Share/invite the github repo with your instructor (tjfisher19 or MichaelHughes1963). The repo should include the following:

A readme file that explains the purpose of the repository.
Code that includes the function outlined above with its specification (15pts: 10 points for general solution and 5 points for following the specifications).
Code that performs the above simulations for all scenarios, including output and discussion (10pts).
The remaining 5pts of your grade will be determined based on: 

Proper GitHub repository creation (with readme file)
Well commented and readable code
Reproducible results
