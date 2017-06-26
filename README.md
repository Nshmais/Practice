# Practice


1.	*What is the most influential book or blog post you’ve read regarding web development?*
- There are no specific blog or book that was really influential to me in process of perusing the web development. Several years ago, I was interested in learning HTML and how to create simple web pages from zero without the prebuild templets that allow the user to just add section and create a web page. As always with a simple google search I read some blogs and watch some videos about the use of HTML. One of the google search result was a web pages called [w3school.com](https://www.w3schools.com/) which was very helpful.      


2.	*Tell me about a web application you have built. Why did you choose to build it? What did you learn? What challenges did you face and how did you overcome them?*

- Developed an application that pin the locations of sights and landmarks in the Dallas and Fort Worth, Texas area on the map. When clicking on the side nav-bar the application display a list of sights and landmarks, which clicking on any of them will trigger a info window that will display some relevant background information about the sight and a hyperlink to the sight web page address. It also display the weather in that sight area. The click also trigger a pin on map with the corresponding location of the sight on the map.  The app also allow the user to filter the sights and landmarks. Another feature of the app is that you are able to input city and state and the app will use Yahoo API to display the current weather condition in the requested area using Ajax request. The app is based on Google Map API and Yahoo Weather API. It also uses knockout (organizational library) to organize the code and its bindings. The app also required knowledge in HTML, CSS, Bootstrap, JavaScript, and Ajax request.
 I choose to develop this application because it is a part of the Udacity Nano degree program. The second reason and more important is to practice and use the skills that I have acquired in this course. In building this project I have learned a lot. Knockout was definitely one of these things. Knockout makes the binding between the code and the view easier and seamless to apply. It also organize the code and the planning process. In the development of this application I have faced many challenges one of these challenges was the use of Ajax request and the duration that took to get the results after the request has been issued and not fitting in my code. But I have overcome this challenge by saving the request result and supply them when needed.              



3.	*Write a function in Python that takes a list of strings and returns a single string that is an HTML unordered list `(<ul>...</ul>)` of those strings. You should include a brief explanation of your code. Then, what would you have to consider if the original list was provided by user input?*
```python 
 def list(strings):
     u_list = "<ul>"
     # Iteration over the strings items
     for item in strings:
         # append the list items in the strings
         u_list += '<li>%s</li>' %s
     u_list += '</ul>'
     # returns unordered list
     return u_list
```
If the original list was provided by user input, we should consider the function should check if the user has inputted the right form of data, list and has strings inside of it.



4.	*List 2-3 attacks that web applications are vulnerable to. How do these attacks work? How can we prevent those attacks?*
- **HTML Injection**: is the type of attack that allow the user the ability to input data to a vulnerable web page. This input point is not usually restricted or bleached the input to the page. The page use the input data as it's received. Usually the hackers use a HTML code that allow them to steal users’ credentials, or it can allow the hacker to modify the page content. To prevent HTML injection we can Escape HTML. 
- **SQL Injection**: is the type of attack that allow the hacker the access to the website database. Ones the hacker has the access to the database he/she can add, delete or alter the database in any shape or form, and steal the database info. SQL injection occurs when malicious SQL statements are inserted into form fields to try and gather info from the database. To minimize or prevent SQL attacks we can escaping all user supplied Input, enforce least privileges methods, and use white list input validation.   
- **Cross-site request forgery (CSRF)**: it's also called *one click attack*, this type of attack occur when authenticated user trigger a state-changing requests unwanted by the user aiming to steal his info. There are many ways to prevent this type of attacks like  Synchronizer token pattern and the use of cookies "set cookie containing a random token that remains the same for the whole user session". 


5.	*Here is some starter code for a Flask Web Application. Expand on that and include a route that simulates rolling two dice and returns the result in JSON. You should include a brief explanation of your code.*

```python
from flask import Flask
app = Flask(__name__)

import json
import random

@app.route('/')
def hello_world():
  return '<strong>Hello world!</strong>'

@app.route('/roll_dice/<int:num_of_sides>/json')
def roll_dice(num_of_sides):

    # Assign the random dice  number to the two dices
    dice_1 = random.randint(1, num_of_sides)
    dice_2 = random.randint(1, num_of_sides)

    # Print the results of the dice rolled on the console
    print json.dumps({'dice 1' :dice_1 ,'dice 2':dice_2}, sort_keys = True)

    # Return the results of the dice rolled as JSON string
    return json.dumps({'dice 1' :dice_1 ,'dice 2':dice_2}, sort_keys = True)


if __name__ == '__main__':
 app.debug = True
 # use local host port(5000) to run project
 app.run(host='0.0.0.0', port=5000)   
```


6.	*If you were to start your full-stack developer position today, what would be your goals a year from now?*
- For the next year from now, I am looking forward to learn Django, explore more and polishing my skills in JavaScript  and Angular.js.

