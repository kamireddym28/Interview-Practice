# Interview-Practice -- Udacity FSND

## Qusestion 1:

**What is the most influential book or blog post you’ve read regarding web development?**

Earlier when I started with web development, as a part of self-learning, I found this website called _w3schools.com_ very much helpful to understand basic concepts. This website provides an opportunity to gain hands on experience while learning which influenced me to dig deep into the topics of web development. 

In recent times, I started following _David Walsh’s_ blog interesting as it showcases all the latest advancement in web development. 

## Question 2:

**Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?**

I recently built a very interesting app of Smartphone Catalog as a part of my nanodegree program. It is an app that holds various models of smartphones available in the market along with their respective specifications and price. Users have an option to login to the app to add any new categories launched into the market and edit or delete them if needed.

To build this web application, I used python’s Flask frame work at the back-end to perform CRUD operations and learnt to implement RESTful APIs that serves JSON outputs.  In the front-end, HTML Jinga2 web template and CSS were used to deal with the aesthetics of the application. Through out its implementation, I got better exposure to using flask frame work. I used to google to know more about SQLAlchemy and various other libraries that flask supports. I also learnt the ways to debug errors. I found it little more challenging to implement OAUTH using google sign in. I overcame this by going through the lesson multiple times and with detailed understanding of concepts in bits and pieces, I was able to accomplish the task.

## Question 3:

**Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (< ul > ... < /ul >) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?**

```

def  uo_list(strings):
     # Initialize a list with <ul> tag
     list1 += "<ul>"
     # Iterate over the parsed in strings
     for i in strings:
     	# append each list item in strings to list1 
	list1 += "<li>"+ i +"</li>"
     # append closing <ul> tag to the list1
     list1 += "</ul>"
     # return the unordered list
     return list1
	
```
- This is a function of unordered list items which iterates over the parsed in list items using for loop and returns the unordered list output. 
- If the original list was provided by the user, the function should check whether the input is a list and it has list items that are strings.

## Question 4

**List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?**

Common attacks that websites are vulnerable to are:

- Cross Site Request Forgery: A cross site request forgery or XSRF attack occurs when information stored in cookies in a browser are used to perform unauthorized HTTP requests. Link leading to download of an in appropriate files is an example of XSRF attack. This attack can be prevented by generating an access token that matches the user server’s token to process the request. Implementing CAPTCHA on some websites is a method to ensure prevention of XSRF attack. 

- SQL Injection attack: This is a type of attack in which user injects SQL code into input fields to make malicious use of data in the database. This can be avoided by using pre-built functions to perform SQL queries rather than generating entire SQL query based on user input. Limiting database privileges to users to perform actions on database.

- Brute force attack: This is an attack to gain access to password protected content. This can be prevented by configuring a robust firewall that can monitor the traffic and identify potential attacks.

## Question 5

**Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.**

```
from flask import Flask, jsonify 
import json
import random

app = Flask(__name__)

@app.route('/’)
def hello_world():
    return ‘Hello World!’

@app.route('/rolldice/JSON')
def rollDiceJSON():
    d1 = random.randint(1,6)
    d2 = random.randint(1,6)
    die_total = d1 + d2
    return jsonify(d1=d1, d2=d2, die_total=die_total)

if __name__ == '__main__':
    app.debug = True
    app.run()    
```
- Rolling a dice results a value between 1 and 6. This can be obtained by using randint() imported from random in python. The outcome of each dice is stored in two variables respectively. The total outcome is the sum of the outcome of individual dice. This value is returned as a JSON object using python flask’s ‘jsonify’.

## Question 6

**If you were to start your full-stack developer position today, what would be your goals a year from now?**

If I am hired as a full-stack developer, a year from now I would master python’s flask frame work and will target to host the web applications I built using AWS. I will master React JS frame work on the front-end part. I will be looking forward to performing challenging tasks with the skills I learnt over the past year. I will contribute to team in delivering the project with accuracy and efficiency.

## Reference
- [Common web application attacks](https://blog.sucuri.net/2014/11/most-common-attacks-affecting-todays-websites.html)
