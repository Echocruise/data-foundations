## preparation for project

1. I combined some columns about answers for different  into one column， such as the reason why you want to learn Nanodgree,Which item in the swag store appeals to you most tec.
2. I transfered the birth date to the age of every student。

> After reading the table seriously, I pose four questions and find my answers. 

## questions
### questions 1 Which academic group has the lowest employment rate?
I want to know the employment situation of different academic groups, so I chose two columns:Are you employed?,and What is your highest level of education?Then I get a sorted information by using pivot table.

I use the sorted informationt to calculate the employment rate.
In the end, I generate a histogram. So I know the employment rate in different academic group.

### questions 2 Does Udaicty graduates like the nanodegree program?

I want to know how much Udacity graduates likes this program.So I get the data source from the coulum:How likely is it that you would recommend Udacity to a friend or colleague?
Then I get a sorted information by using pivot table.
Next, I got the mode, median, mean ,standard deviation by using some functions.
From the chart I genereated, we could know most of Udacity graduates like this program.

### questions 3 How long does most students sleep?

I want to know howlong does most students sleep.So I get the data source from the coulum:On average, how many hours of sleep do you get per night?
Then I get a sorted information by using pivot table.
Next, I got the mode, median, mean ,standard deviation by using some functions.
From the chart I genereated, we could know most of students sleep 7 hours per night.

To clarify:
When I see the data, I find that there are some outliers:1,45,65,85,9141984.I find the outliers would affect the garph and our judgement.So I exclude these outliers.

### questions 4 Which ways do most students choose for help?


I want to know which ways do most students choose for help.So I get the data source from the coulum:What was most helpful when you got stuck in the Nanodegree program(s)?
Then I get a sorted information by using pivot table.
I found that there some duplicate ways.
So I clean the data again.

- "StackOverflow" and 'official Documentation i.e. on Keras.org or tensorflow.org" I combine into one called stackoverflow.
- "google", "Google search","Internet searches","Just googling for answers"  I combine into one called internet search.
- "Feedback from graders","Feedback from submissions",I combine into one called feedback.- "External resources (khan academy, coursera)","Books","Videos"I combine into one called External resources
- I rename "Mentor Help (classroom or 1:1 mentors)"  as  Mentor Help 
- "I received no help."and "me","So far, I did not get really stuck"I combine into one called personal learning
- I found there are some blank ,so I rename blank to other ways.Next,I generated a pie chart.From the pie chart,you would found that 42.9% people choose Forums to slove their people, 22.97% people choose slack to slove their problem,19.26% people choose stack overflow to slove their problem.


## Note
This data is from Survey Respondents and is not from the entire Udacity Student population. 