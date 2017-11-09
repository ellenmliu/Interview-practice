# Interview Practice
Author: Ellen Liu
<br>Last Edit: 11/9/2017

Udacity Full-Stack Nanodegree provided some interview questions for practice.

1) What is the most influential book or blog post you’ve read regarding web
development?

    The most influential blog post I have read about web development is 'So, You’re
a Web Designer, Right?' by Gorka Melero. In this post, he explains how web design
was like a few years ago, and how technology evolving affects the way
a web designer goes about their work. He goes on about how new tech is made for
the convenience of our lives, but so many people rejects it because they
are so used to what they are doing. It encourages me to keep updated with the
latest technologies and be opened to incorporate it.

2) Tell me about a web application you have built. Why did you choose to build
it? What did you learn? What challenges did you face and how did you overcome
them?

    One web application I built is Census, which is a plant tracker that accompanies
the phone app made for it. I chose to build it so that a user can have access to
their plants online and for users to have more details about the app. While building,
I learned how to use different services, like Firebase and Heroku,
which was challenging incorporating into the web app. I considered hosting on
the web app on Firebase, but they did not offer the support I made my web app in,
so I had to do some research and configured my web app to be hosted onto Heroku.
Even though it was challenging getting the web app hosted, I was able to learn
how to use new technology.

3) Write a function in Python that takes a list of strings and returns a single
string that is an HTML unordered list (`<ul>...</ul>`) of those strings. You
should include a brief explanation of your code. Then, what would you have to
consider if the original list was provided by user input?

    I made a function that takes in a list of strings and it would concatenate all
into one string. I started the string with the `<ul>` tag and used a for loop that
would iterate through the list. Each element will be wrapped with `<li>` and `</li>`
tags and concatenate with the result string. After the loop, I add in the end
`</ul>` tag and return the result. If the list was provided by the user, I would
have to consider checking if the input is a list and if the elements within the
list are all strings.


```
test = ["test", "here", "testing"]

def turn_to_list(arr):
  str = "<ul>"
  for st in test:
    str += "<li>"+ st + "</li>"
  return str+"</ul>"

print turn_to_list(test)
```

4) List 2-3 attacks that web applications are vulnerable to. How do these
attacks work? How can we prevent those attacks?

    Cross-Site Scripting is when the attacker insert JavaScript in the pages to the
site to have control over the information, like sending information from the
site to an evil server. Some ways to prevent this is input validation and use
HttpOnly attribute for cookies.
    DDoS Attacks is to make the network resource unavailable to its intended users
by either making it slow or even taking the site offline through generating
requests from thousands of IP addresses. There are many DDoS protection tools
out there to prevent these attacks from happening.
    SQL Injection is when it takes advantage of the vulnerabilities to gain control
of the database and the data stored in them, which includes name, email
addresses, and any other private information. To prevent this attack, we must
regularly check upon any vulnerabilities and fix them before the attacks would
happen. Using a parameterized API, running the application with minimal
privileges, and validating and sanitizing input would be a few ways to do so.

    Some other ways to prevent any of these attacks is to add in services, like
CAPTCHA, that checks if the user is a bot or a human. Also having the code to
be reviewed to see if there are any vulnerabilities.

5) Here is some starter code for a Flask Web Application. Expand on that and
include a route that simulates rolling two dice and returns the result in JSON.
You should include a brief explanation of your code.

    I provided a path for the site with the app route. Assuming the die has 6 sides
from 1-6, it returns a JSON string of result.

```
  from flask import Flask
  app = Flask(__name__)

  import json
  import random

  @app.route('/')
  def hello_world():
   return 'Hello World!'

  @app.route('/roll/json')
  def roll_dies():
   return json.dumps({'Dice1' : random.randint(1,6), 'Dice2' : random.randint(1,6)} )

  if __name__ == '__main__':
   app.debug = True
   app.run()
```

6) If you were to start your full-stack developer position today, what would be
your goals a year from now?

    If I were to start my full-stack developer today, I would aim to pick up other
libraries and modern technologies like Node.js and Angular.js. I have made a few
applications, but would like to gain knowledge on how to make it more efficient
and organized. I would also like to dive deeper on how to make a more secure web
application to ensure safety and privacy for all of intended users.

## Bibliography
1) https://securityintelligence.com/the-10-most-common-application-attacks-in-action/
2) https://stackoverflow.com/questions/16668511/python-dump-dict-as-a-json-string
3) https://www.business2community.com/crisis-management/common-web-application-attacks-prevent-0949592
4) https://tympanus.net/codrops/2013/09/23/so-youre-a-web-designer-right/
