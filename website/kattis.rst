============
Using Kattis
============

`Kattis <http://open.kattis.com/>`_ is a website that allows students to submit
solutions to programming problems, and have them evaluated automatically by
running a series of test cases on the submitted solutions.

You will be able to test your solution to the programming assignments on Kattis.
However, please take into account:

* Kattis is **not** how you will submit your work for grading. You must submit
  your programming assignments using `chisubmit <chisubmit.html>`_.
* You can test your work on Kattis as many times as you want. Making multiple
  incorrect submissions on Kattis will *not* affect your grade in a programming
  assignment.
* When asking for help on an assignment, it is much easier if you point us
  to your last submission on Kattis, since that allows us to see exactly what
  test cases you are passing and failing.

Setup
-----

Before you can submit code through Kattis, you need to complete the following steps:

1. Go to the `Open Kattis registration page <https://open.kattis.com/register>`_ and 
   create an account **with your UChicago e-mail**. If you do not use your UChicago e-mail,
   we will not be able to find your submissions on Kattis.

2. Log into the UChicago Kattis site using the account you just created: https://uchicago.kattis.com/login

3. Go to the `CMSC 23310 Spring 2018 page on Kattis <https://uchicago.kattis.com/courses/CMSC23310/Spring-2018>`_, 
   and click on the link that says "I am a student taking this course and I want to register for it on Kattis."

4. Go to your User Settings (click on the user icon on the top-right corner of the Kattis
   page, and then select "Settings") and change the following:

   * By default, the information on what problems you have solved is shown to everyone in the class
     (you can see what this looks like by clicking on the `Queue <https://uchicago.kattis.com/submissions>`_
     link on the top of the site). If you would prefer not to show this information,
     check the "Anonymous mode" option.

   * Set your preferred time zone to "America/Chicago"

   * Set your default language to your language of choice.

Familiarizing yourself with Kattis
----------------------------------

Before you attempt any of the problems we give you, you should familiarize yourself
with Kattis to ensure you know how it works. We suggest you start by solving the 
`Hello World <https://uchicago.kattis.com/problems/hello>`_ problem. This problem
has a very simple solution: you just need to write a program that prints out 
a "secret message", which happens to be exactly this text::

    Hello World!

The way you submit a problem is by clicking on the green "Submit" button that appears
on the right sidebar. This
will take you to a page where you can either upload a file, or switch to an editor
where you can write the code directly on your browser. Make sure that you select
the correct programming language before you submit.

After you've submitted the code, Kattis will "judge" it, and will send you an
e-mail notification with the result. If you solved the problem correctly, you 
will get an "Accepted" judgement. 

You can also check the status of all your
submissions by clicking on the user icon on the top-right corner of the Kattis
page, and then clicking on "My Profile". This will show a list of all your submissions.
Take into account that this list does not update automatically; if a submission 
shows up as pending (either "Compiling" or "Running"), you need to reload the page 
to see its latest status.

You can also get more details on any submission by clicking on the
6-7 digit number on the left column (this is number is the *submission identifier*).

Next, try to make an *incorrect* submission. Submit a program that prints
this::

    Hello Lamport!

The submission should be judged as "Wrong Answer".

Solving the programming assignments
-----------------------------------

As you'll see in the programming assignments, you must write code that receives some 
input in a well-specified format, and must produce output in a well-specified way.

All input is done via **standard input**. All output is done via **standard output**.

**You should not read or write from any files**

The problems will include some sample data that you can use to test your solution. However,
Kattis will run your solution with additional test cases that are known only to the
instructors.

So, if you get a "Wrong Answer", make sure you look at the details of that submission
(by going to the list of submissions and clicking on the submission identifier). This
will show you how many of the instructors' test cases you are passing.

Kattis may return judgements other than "Accepted" and "Wrong Answer". You can see
a list of all the possible Kattis judgements here: https://uchicago.kattis.com/help/judgements

Testing your solution before submitting to Kattis
-------------------------------------------------

Before submitting a solution to Kattis, you may want to run your solution on your own
machine to make sure there are no major issues with your code, such as syntax errors or
small mistakes that will makes your code return a Wrong Answer even with the sample input.

Suppose you write a solution in Python in a file called ``problem.py``. To test your
solution, just run the program::

    python problem.py

Since input is done through standard input, your program should now wait for input. You
should just type (or copy-paste) some valid input (e.g., from the provided sample input)
and then press Control-D to indicate the end of input. Alternatively, you can save the 
sample input to a file, and use input redirection to feed that file into the program's standard input::

    python problem.py < sample.in

In either case, your program will run with the provided input. If the output matches the sample output provided
in the Kattis problem statement, it means your solution works for that input. At this point, your solution
is probably safe to submit to Kattis.

If, on the other hand, your program crashes or the output that doesn't match the expected output, you may want
to debug your solution a bit more before you submit it on Kattis. Otherwise, you will have to debug it using the
(sometimes limited) feedback that Kattis provides.


Asking for help
---------------

If you keep getting a "Wrong Answer" on a problem, and you can't figure out what
the issue is, it will be really helpful if you can tell us the submission identifier of your
latest submission. That way, we can take a look at the code you submitted and
see why it isn't working.


Open Kattis
-----------

Many of you were probably not familiar with Kattis before this class. Besides providing
sites to university courses, Kattis also hosts a treasure trove of
interesting programming problems that can be good preparation for job interviews or just
for your own edification. You can access their complete collection of problems on their
`Open Kattis <https://open.kattis.com/>`_ site.

For avoidance of doubt: we are pointing you to Open Kattis just because some of your
may find it of interest. Solving problems on Open Kattis will have no bearing on your
grade for this course.



