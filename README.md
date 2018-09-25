# Alexa-Stack-Overflow
Alexa skill for Stack overflow
## Inspiration

As the time passes by we are getting more advanced and what happens in future depends on the outcome of the contributions that people will make in the present. We are living in the world in which we are having voice assistant in our pockets, which helps in simplifying our day to day life. I also like when things can be done easily without any hassle. Being a programmer I wanted to solve some problems faced during programming. And I thought why cant voice assistant help us with programming related query, why cant we ask Alexa how to solve the programming error that I am facing.

## What it does

The aim of this Alexa skillis to provide solutions to the programmers over voice. All they have to do is ask Alexa their programming query and Alexa will search for answer to the programming query and provide the user with proper answer. To get started with the skill. What the skill currently does is it takes in the query and Bing search the query and find the links related to stack overflow and then using the info of the link parameters it do an api call to the stack overflow to get info about that posted question of the stack overflow. Then in the lambda function I am making a list of questions related to the query. And then the lambda function first confirms whether the question on the stack overflow is related to his query or not. If not related then it provides the next question and it goes on till the list of questions exhaust. If the question is related to the query that the user asked then it will tell the accepted answer in the answer thread and user will be provided this answer and the code included in the answer as a response card to his Alexa app. Then the user will be provided with an option whether or not he/she wants to hear the comments to the answer that was just provided or it wants to repeat the answer. If yes then the Alexa provide the comment and if no the Alexa will ask whether he/she wants to hear the next best answer in the answer list. The next best answer is considered on the basis of up votes to the answer.

# Link to the Skill on Amazon Skill store

US - [Stack Overflow US skill Store](https://www.amazon.com/dp/B07HGW33GQ/ref=sr_1_2?s=digital-skills&ie=UTF8&qid=1537339798&sr=1-2&keywords=stack+overflow)<br />
India - [Stack Overflow India skill Store](https://www.amazon.in/s/ref=sr_nr_n_0?fst=as%3Aoff&rh=n%3A11928183031%2Cn%3A12113608031%2Ck%3Astack+overflow&keywords=stack+overflow&ie=UTF8&qid=1537338810&rnid=11928185031)<br />
UK - [Stack Overflow UK skill Store](https://www.amazon.co.uk/Yash-Stack-Overflow/dp/B07HGW33GQ/ref=sr_1_2?ie=UTF8&qid=1537683988&sr=8-2&keywords=stack+overflow)<br />
Australia - [Stack Overflow Australia skill Store](https://www.amazon.com.au/Yash-Stack-Overflow/dp/B07HGW33GQ/ref=sr_1_1?ie=UTF8&qid=1537684024&sr=8-1&keywords=stack+overflow)<br />
Canada - [Stack Overflow Canada skill Store](https://www.amazon.ca/Yash-Stack-Overflow/dp/B07HGW33GQ/ref=sr_1_1?ie=UTF8&qid=1537684055&sr=8-1&keywords=stack+overflow)

# Video-Demonstration
[Link to Youtube video](https://youtu.be/tuy70RlCJXg) 

# Getting Started
```python
# Clone the github repo
git clone https://github.com/mr-yamraj/Alexa-Stack-Overflow.git
cd Alexa-Stack-Overflow

#install all the dependencies
pip install requirements.txt

#run the function
python lambda_function.py <test-case-index>
Ex : python lambda_function.py 2 
# You can change the testcases by changing the index number 0 to 9 description of all the test cases is provided below
```

## Description of Test Cases

test_case[0] - Launch Request "Alexa, open stack overflow"<br />
test_case[1] - Help Intent "Alexa, ask stack overflow help"<br />
test_case[2] - Library Install request "Alexa, ask stack overflow how to install opencv in python"<br />
test_case[3] - When Alexa ask to coinfirm the question and user responds "no"<br />
test_case[4] - When Alexa ask to coinfirm the question and user responds "yes"<br />
test_case[5] - When Alexa provide answer to the question and user responds "repeat"<br />
test_case[6] - When user says yes to provide comments to the answer "yes"<br />
test_case[7] - When Alexa asks user whether or not to provide second best answer to the question and user responds "yes"<br />
test_case[8] - Error Intent "Alexa, ask stack overflow ehat is identation error in python"<br />
test_case[9] - Comparision Intent "Alexa, ask stack overflow which is superior Python or C++"<br />
