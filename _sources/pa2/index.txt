Programming Assignment 2: Paxos
-------------------------------

**Due:** Thursday, May 12st @ 8pm

In this homework, you will be implementing a single-instance (or "Single Synod") version of the Paxos consensus algorithm. Instead of running the algorithm across multiple machines, you will instead simulate a distributed system composed of multiple machines connected with a basic (and deterministic) network.

You are allowed to use any programming language you want and, before the deadline, you will be able to test your solution using `Kattis <https://open.kattis.com/>`_, a website that allows students to submit solutions to programming problems, and have them evaluated automatically by running a series of test cases on the submitted solutions. Please note that, while you are allowed to use any language, Kattis itself only supports a limited number of languages; if you do not use one of their supported languages, you will not be able to test your solution on Kattis (but you will still be able to submit your code for grading).

The full specification of the programming assignment is available on Kattis:

    https://uchicago.kattis.com/problems/uchicago%3Apaxos

We also provide detailed descriptions of :download:`Sample Input 1 <paxos_sample1.pdf>` and :download:`Sample Input 2 <paxos_sample2.pdf>`.

The points for this homework are divided as follows:

* 35 points: Implementing the "Simulate" function.
* 35 points: Implementing a single-instance version of the Paxos algorithm that works in the absence of failures.
* 30 points: Making your implementation work in the presence of failures.

We recommend you follow the specification of the algorithm presented in *Paxos Made Simple*. Take into account that the bulk of the Paxos algorithm will be contained in your implementation of the "Deliver-Message" function. Our reference implementation is about 400 lines of Python, of which only 100 relate directly to the Paxos algorithm (the rest are the scaffolding to run the simulation).

You are not provided with any starter code; you must implement your solution from scratch following the provided problem specification.

For more instructions on how to use Kattis, please see our `Using Kattis <../kattis.html>`_ page.

You will each be provided with an individual Git repository on the `department's GitLab server <https://mit.cs.uchicago.edu>`_ to work on your programing assignments. Place your work for this programming assignment in a top-level ``pa2`` directory. Besides including your code in this directory, you must also include a ``README`` file with precise instructions on how to compile and run your code on a CS machine.

You must submit your work using `chisubmit <../chisubmit.html>`_. The assignment identifier you should use is ``pa2``.
