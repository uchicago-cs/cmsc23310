Project
=======

**Due (Graduating Students):** Friday, June 5th @ 8pm

**Due (Non-Graduating Students):** Sunday, June 14th @ 8pm

Distributed data storage is an important case study for many of the concepts explored in this course. The sharp rise of NoSQL databases in the late 2000's popularized data models, such as key-value stores, that departed from the traditional relational model. The development of these new models was usually motivated by the emerging field of large-scale distributed computing, and issues such as consistency and availability dominated the discussion of these models, with a bias towards sacrificing consistency for availability.

Many of these design decisions and tradeoffs of these models frequently reference Eric Brewer's CAP theorem but, as we discussed in class, distilling the CAP theorem into a "choose 2 of 3" rule of thumb can be misleading. In "CAP twelve years later", Brewer restated the CAP theorem in contemporary terms with numerous clarifications. Among them, he stresses the original purpose of the CAP theorem and relates it to the BASE (Basically Available, Soft State, Eventually consistent) and ACID (Atomicity, Consistency, Isolation, Durability) models. When designing a database, or any other distributed system, Brewer argues for looking at the full range of possible designs, and he puts ACID and BASE at opposite ends of the CAP spectrum: ACID is consistent, BASE is available. As an example of how to think about these tradeoffs, Brewer mentions that doing Paxos, "just delays the decision. At some point the program must make the decision; retrying communication indefinitely is in essence choosing C over A." Many examples of these types of tradeoffs are explored throughout the course, from distributed hash tables like Chord and Tapestry, to Google's Bigtable and Spanner.

In this project, you will explore these tradeoffs by developing a simple distributed key-value store (which we will refer to simply as the "data store"). You will develop your project using `chistributed <http://chi.cs.uchicago.edu/chistributed/>`_, a framework that will allow you to simulate a distributed system on a single machine, allowing you to focus on the algorithms and protocols of your system, without having to deal with all the low-level details (like launching separate machines for each node in your distributed system, etc.). chistributed will also allow you to easily and deterministically simulate a variety of failures, to test whether your data store is resilient to them. While chistributed does impose a few constraints, such as a specific protocol for communications both inside the data store and with the external world, the actual implementation and features of your project will be up to you. In other words, your implementation could internally use the OM(m) algorithm, Paxos, Raft, a DHT, etc. Several implementation options are presented further below.

Project requirements
--------------------

The project is divided into two parts: the implementation and a paper. The implementation can be done in any language, as long as we can compile it and run it on a CS machine. The implementation grade will be based on whether you meet a set of requirements (described below). Your paper will describe your data store's goals and requirements, the design decisions you made based on those requirements (including a justification of those decisions, based on relevant course readings or other literature) and a description of your implementation.

The implementation is divided into the following components:

* 20 points: Implementing *get* and *set*: Your implementation must be able to process *get* and *set* requests to the data store. For this part of the project, you do not have to replicate the data to other nodes (besides the one receiving the *get* or *set* message) or even be fault-tolerant.
* 20 points: Basic replication: Your implementation must create replicas of the values (but not necessarily in a fault-tolerant manner).
* 30 points: Fault tolerance: Given a call to *set* or *get*, the call must eventually succeed or return an error message. Either call can be delayed in the presence of failures but, in the absence of failures, all calls must eventually succeed. The consistency model is up to you, but the returned values cannot be trivially consistent (e.g., a data store that always returns the value 42). These conditions should be met in the presence of...

  * Byzantine, fail-stop, or fail-recover failures (15 points). Note: it is enough for you to be resilient one of these types of failures; you do not need to be resilient to all of them.
  * Network partitions (15 points)

* 20 points: Style. Your code must be well-documented and easy to read. There must be a README file explaining the general structure of the implementation, and every file must include a header explaining the purpose of the file. All data structures must be documented, and non-trivial pieces of code must include comments explaining what the code does. Functions/methods must, at the very least, include a short description of what the function/method does.

Take into account that, as described later, we will not be testing your code with arbitrary scripts. Instead, you must supply chistributed scripts that demonstrate that your implementation fulfils the above requirements.

The paper is divided into the following components:

* 20 points: Summary of fault-tolerance algorithm/protocol used in your project, citing all sources you consulted.

* 35 points: Description of your implementation. This must include, at least, a description of how *set* requests are processed, how *get* requests are processed, and the specific fault tolerance features supported by your project. Note that this is distinct from the README file included in your implementation, which should be a to-the-point (and not necessarily prosaic) summary of how your implementation is structured, to help us navigate the files and main data structures of your implementation.

* 30 points: Discussion of at least two example chistributed scripts (with failures) and an explanation of how your implementation reacts in the presence of those failures.

* 15 points: Discussion of the issues, challenges, and lessons learned while implementing your data store.

There is no minimum length requirement, but we suggest you aim for at least 8 single-spaced pages.


Implementation options
----------------------

In this project, you are free to implement your data store in any way you want, as long as it meets the requirements outlined above. However, unless there is a fault tolerant distributed algorithm you've really really really been dying to try out, we encourage you to choose from one of the following four project ideas.

Multi-Paxos
~~~~~~~~~~~

In Programming Assignment \#2, you implemented a basic version of Paxos where you always ran a single instance of Paxos at a time, without the possibility of having multiple instances running concurrently. You can build on this and write a data store that uses Multi-Paxos at its heart, similar to the Chubby service. If you choose this option, your project should do more than simply run a full instance of Paxos for each *get* and *set* operation; you should, at the very least, incorporate the notion of a distinguished proposer such that, as long as the proposer does not fail, the first phase of the algorithm does not have to be re-run for every instance.

Raft
~~~~

As we saw in class, Raft is specifically designed to be easier to implement than Paxos, which can make it an attractive option for this project. However, unlike Paxos, you have not had to implement Raft before this project, so you should weigh whether it will be better to implement a known-difficult algorithm that you already have some experience with, or a known-easy algorithm that you have not yet implemented. Choose wisely.


DHT
~~~

Multi-Paxos and Raft both fall on the CP side of the CAP theorem. If you are interested in exploring what happens in the AP side of the theorem, you can implement a Distributed Hash Table. While you may draw inspiration from Pastry and Chord, you do not have to implement them verbatim. You may even look up other Distributed Hash Tables to implement.


Scatter: DHTs and Paxos
~~~~~~~~~~~~~~~~~~~~~~~

Can't choose between consistency and availability? Why not do both? If you're feeling particularly brave, you can implement Scatter, a system we did not discuss in class. `Scatter <http://homes.cs.washington.edu/~arvind/papers/scatter.pdf>`_ is a DHT which tries to be more consistent than a simpler DHT, while maintaining high availability. As usual, this is a tradeoff: it is neither perfectly consistent nor perfectly available, as nodes come and go in the network. The basic idea is that when partitioning the keyspace amongst the nodes, the nodes are put into discrete groups. Updates to keys must be agreed upon via Paxos within the responsible group. This drastically improves consistency, since any nodes responsible for a given key will have the same value (subject to the assumptions and constraints of Paxos).

Scatter also extends Paxos to deal cleanly with adding and removing nodes over time, further improving availability. You can think of it as keeping the information about which nodes are in a given group under the same consistency restraints as keys in that group: to add a node to a group, the group runs Paxos. Scatter exploits this to avoid routing inconsistencies, where a node may think it is responsible for a given key range, when changes to the network topology have made it responsible for another.

Both of these (key range consistency and routing consistency) are separate optimizations. Either would be an approachable extension of a DHT system such as Chord or Pastry, and would be very appropriate for this project.

Note that if you choose to implement a more-or-less "vanilla" DHT, you should focus on the fundamental design choices of a DHT: keyspace partitioning method, routing algorithm, etc. If you choose to do a DHT+Paxos project, as described here, the choice of those fundamentals will be less important than how you integrate Paxos with them.

Other Options
~~~~~~~~~~~~~

If none of the options above sound interesting, you are welcome to propose other algorithms/protocols to implement, as long as they can meet the project requirements specified earlier.


Registering for the project
---------------------------

You may do the projects in groups of up to three students. Groups can be formed across sections. Groups with at least one graduating student must submit their work by the graduating student deadline.

Once you have decided who will be in your team, you must register as described in the `chisubmit <http://chi.cs.uchicago.edu/chisubmit/students.html>`_ page. A shared repository will be created for all the team members shortly after you register.


Submitting the project
----------------------

Your repository must be organized into, at least, the following directories:

* ``impl``: This directory must include all your source code. If you used a compiled language, you *must* include a Makefile to compile your code. This directory must include the implementation-oriented README file described earlier.
* ``impl/scripts``: chistributed scripts and configuration files that we can use to test your implementation. You must include, at least, the scripts that are described in your paper.
* ``paper``: Must contain a PDF file, ``project.pdf``, with your final paper. If you are using LaTeX, Markdown, etc. you may also store your paper's source code in this directory.

The root of your repository must include a ``README.md`` file with the following information:

* Names and e-mail addresses of all the students in the group
* For groups of two or three, a description of what each student worked on.
* Concise instructions on how we should run chistributed (with what parameters, from what directory, etc.) to run your scripts.

