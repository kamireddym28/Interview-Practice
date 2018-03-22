# Interview-Practice -- Udacity FSND

## Qusestion 1:

**1.	What is the most influential book or blog post you’ve read regarding web development?**

Earlier when I started with web development, as a part of self-learning, I found this website called _w3schools.com_ very much helpful to understand basic concepts. This website provides an opportunity to gain hands on experience while learning which influenced me to dig deep into the topics of web development. 

In recent times, I started following _David Walsh’s_ blog interesting as it showcases all the latest advancement in web development. 

## Question 2:

**2.	Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?**

I recently built a very interesting app of Smartphone Catalog as a part of my nanodegree program. It is an app that holds various models of smartphones available in the market along with their respective specifications and price. Users have an option to login to the app to add any new categories launched into the market and edit or delete them if needed.

To build this web application, I used python’s Flask frame work at the back-end to perform CRUD operations and learnt to implement RESTful APIs that serves JSON outputs.  In the front-end, HTML Jinga2 web template and CSS were used to deal with the aesthetics of the application. Through out its implementation, I got better exposure to using flask frame work. I used to google to know more about SQLAlchemy and various other libraries that flask supports. I also learnt the ways to debug errors. I found it little more challenging to implement OAUTH using google sign in. I overcame this by going through the lesson multiple times and with detailed understanding of concepts in bits and pieces, I was able to accomplish the task.

## Question 3:

**3.	Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list (< ul > ... < /ul >) of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?**

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
This is a function of unordered list items which iterates over the parsed in list items using for loop and returns the unordered list output. 
If the original list was provided by the user, the function should check whether the input is a list and it has list items that are strings.
