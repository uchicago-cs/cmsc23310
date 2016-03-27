Spring 2016 Calendar and Reading List
-------------------------------------

**Note: This reading list is still tentative, and subject to change!**

Make sure you don't miss the :ref:`additional-reading` at the bottom of this page.

Week 1
~~~~~~

No required reading for this week. We will be covering basic terminology and
concepts in distributed systems.

**Suggested Reading**

Note: Some of these readings go into topics that we will cover later in the quarter.
As such, you may not get that much out of reading these references at the start
of the quarter. Instead, they can be good reference material to re-read later on
and see how everything fits together.

- `Distributed Systems for Fun and Profit <http://book.mixu.net/distsys/>`_
- `Notes on Distributed Systems for Young Bloods <https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/>`_
- `Distributed systems theory for the distributed systems engineer <http://the-paper-trail.org/blog/distributed-systems-theory-for-the-distributed-systems-engineer/>`_
- Samuel C. Kendall, Jim Waldo, Ann Wollrath, and Geoff Wyant. 1994. 
  `A Note on Distributed Computing <http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.41.7628&rep=rep1&type=pdf>`_. 
  Technical Report. Sun Microsystems, Inc., Mountain View, CA, USA.
- `Fallacies of Distributed Computing Explained <https://pages.cs.wisc.edu/~zuyu/files/fallacies.pdf>`_. Arnon Rotem-Gal-Oz.

Week 2 - Distributed Time
~~~~~~~~~~~~~~~~~~~~~~~~~

**Required reading for Monday, April 4**

-  Leslie Lamport. `Time, Clocks, and the Ordering of Events in a
   Distributed
   System <http://research.microsoft.com/en-us/um/people/lamport/pubs/time-clocks.pdf>`__.
   Commun.ACM, 21(7):558–565, July 1978

**Required reading for Wednesday, April 6**

-  C. J. Fidge.\ `Timestamps in Message-Passing Systems that Preserve
   the Partial
   Ordering <http://zoo.cs.yale.edu/classes/cs426/2012/bib/fidge88timestamps.pdf>`__.
   Proceedings of the 11th Australian Computer Science Conference,
   10(1):5666, 1988
-  Friedemann Mattern. `Virtual Time and Global States of Distributed
   Systems <http://www.vs.inf.ethz.ch/publ/papers/VirtTimeGlobStates.pdf>`__.
   In Parallel and Distributed Algorithms, pages 215–226. North-Holland,
   1989

**Suggested papers**

-  Parameswaran Ramanathan, Kang G. Shin, and Ricky W. Butler.
   `Fault-tolerant Clock Synchronization in Distributed
   Systems <http://lass.cs.umass.edu/~shenoy/courses/spring04/677/readings/ramanathan_clksync.pdf>`__.
   Computer, 23(10):33–42, October 1990
-  David L. Mills. `Improved Algorithms for Synchronizing Computer
   Network
   Clocks <http://eia.udg.es/~teo/sd/documents/documents_temps/mills94improved.pdf>`__.
   SIGCOMM Comput. Commun. Rev., 24(4):317–327, October 1994

Week 3 - Distributed Consensus I
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Required reading for Monday, April 11**

-  Leslie Lamport, Robert Shostak, and Marshall Pease. `The Byzantine
   Generals
   Problem <http://research.microsoft.com/en-us/um/people/lamport/pubs/byz.pdf>`__.
   ACM Trans. Program. Lang. Syst., 4(3):382–401, July 1982

**Required reading for Wednesday, April 13**
   
-  D. Skeen. `A Quorum-Based Commit Protocol <https://ecommons.cornell.edu/handle/1813/6323>`_. Technical Report 82-483. Department of
   Computer Science, Cornell University. February 1982.   
-  D. Skeen and M. Stonebraker. `A Formal Model of Crash Recovery in a
   Distributed
   System <http://www.inf.fu-berlin.de/lehre/SS10/DBS-TA/Reader/3PCSkeenStonebr.pdf>`__.
   IEEE Trans. Softw. Eng., 9(3):219–228, May 1983

**Suggested papers**

-  J. Gray. `Notes on Database Operating Systems <http://research.microsoft.com/en-us/um/people/gray/papers/DBOS.pdf>`_. Operating Systems, an Advanced Course, 
   Bayer et. al. eds., Lecture notes in Computer Science 60, Springer-Verlag, 1978, pp. 393-481. 
-  Butler W. Lampson and Howard E. Sturgis. `Crash Recovery in a
   Distributed Data Storage
   System <http://research.microsoft.com/en-us/um/people/blampson/21-CrashRecovery/Abstract.html>`__,
   1979
-  M. Pease, R. Shostak, and L. Lamport. `Reaching Agreement in the
   Presence of
   Faults <http://research.microsoft.com/en-us/um/people/lamport/pubs/reaching.pdf>`__.
   J.ACM, 27(2):228–234, April 1980
-  Philip A. Bernstein, Vassco Hadzilacos, and Nathan Goodman.
   `Concurrency Control and Recovery in Database
   Systems <http://research.microsoft.com/en-us/people/philbe/ccontrol.aspx>`__.
   Addison-Wesley Longman Publishing Co., Inc., Boston, MA, USA, 1987
-  Fred B. Schneider. `Implementing fault-tolerant services using the
   state machine approach: A
   tutorial <http://www.cs.cornell.edu/fbs/publications/smsurvey.pdf>`__.
   ACM Comput. Surv., 22(4):299–319, December 1990
-  Miguel Castro and Barbara Liskov. `Practical Byzantine Fault
   Tolerance and Proactive
   Recovery <http://www.itu.dk/stud/speciale/bepjea/xwebtex/litt/practical-byzantine-fault-tolerance-and-proactive-recovery.pdf>`__.
   ACM Trans. Comput. Syst., 20(4):398–461, November 2002

**Other suggested reading**

-  `Consensus Protocols: Two-Phase Commit <http://the-paper-trail.org/blog/consensus-protocols-two-phase-commit/>`_. Henry Robinson. The Paper Trail.
-  `Consensus Protocols: Three-phase Commit <http://the-paper-trail.org/blog/consensus-protocols-three-phase-commit/>`_. Henry Robinson. The Paper Trail.

Week 4 - Limits of Distributed Systems
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Required reading for Monday, April 18**

-  Michael J. Fischer, Nancy A. Lynch, and Michael S. Paterson.
   `Impossibility of distributed consensus with one faulty
   process <http://discolab.rutgers.edu/classes/cs519-old/papers/p374-fischer.pdf>`__.
   J. ACM, 32(2):374–382, April 1985
-  Danny Dolev, Cynthia Dwork, and Larry Stockmeyer. `On the Minimal
   Synchronism Needed for Distributed
   Consensus <http://www.geocities.com/stockmeyer@sbcglobal.net/dds.pdf>`__.
   J. ACM, 34(1):77–97, January 1987

**Required reading for Wednesday, April 20**

-  Seth Gilbert and Nancy Lynch. `Brewer's Conjecture and the
   Feasibility of Consistent, Available, Partition-Tolerant Web
   Services <http://lpd.epfl.ch/sgilbert/pubs/BrewersConjecture-SigAct.pdf>`__.
   SIGACT News, 33(2):51–59, June 2002
-  E. Brewer, `CAP twelve years later: How the "rules" have changed <http://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed>`_. 
   in Computer, vol. 45, no. 2, pp. 23-29, Feb. 2012.

**Suggested papers**

-  Cynthia Dwork, Nancy Lynch, and Larry Stockmeyer. 
   `Consensus in the presence of partial synchrony <http://theory.lcs.mit.edu/tds/papers/Lynch/jacm88.pdf>`_. J. ACM 35, 2 (April 1988), 288-323.
-  N. Lynch. `A Hundred Impossibility Proofs for Distributed
   Computing <http://groups.csail.mit.edu/tds/papers/Lynch/podc89.pdf>`__.
   In Proceedings of the eighth annual ACM Symposium on Principles of
   distributed computing, PODC ’89, pages 1–28, New York, NY, USA, 1989.
   ACM
   
**Other suggested reading**

-  `A Brief Tour of FLP Impossibility <http://the-paper-trail.org/blog/a-brief-tour-of-flp-impossibility/>`_. Henry Robinson. The Paper Trail.
-  `Papers We Love - Impossibility of Consensus with One Faulty Process <http://www.slideshare.net/HenryRobinson/pwl-nonotes>`_. Henry Robinson.
-  `FLP and CAP aren't the same thing <http://the-paper-trail.org/blog/flp-and-cap-arent-the-same-thing/>`_. Henry Robinson. The Paper Trail.
-  `The CAP FAQ <http://henryr.github.io/cap-faq/>`_. Henry Robinson.
-  `You Can't Sacrifice Partition Tolerance <https://codahale.com/you-cant-sacrifice-partition-tolerance/>`_. Coda Hale.
-  `Clarifications on the CAP Theorem and Data-Related Errors <https://voltdb.com/blog/clarifications-cap-theorem-and-data-related-errors>`_. Michael Stonebraker.
-  `The Theorem That Will Not Go Away <http://the-paper-trail.org/blog/the-theorem-that-will-not-go-away/>`_. Henry Robinson. The Paper Trail.


Week 5 - Paxos
~~~~~~~~~~~~~~

**Required reading for Monday, April 25 and Wednesday April 27**

-  Leslie Lamport. `The Part-Time
   Parliament <http://research.microsoft.com/en-us/um/people/lamport/pubs/lamport-paxos.pdf>`__.
   ACM Trans. Comput. Syst., 16(2):133–169, May 1998
-  Leslie Lamport. `Paxos Made
   Simple <http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf>`__.
   ACM SIGACT News, 32(4):18–25, December 2001

**Other suggested reading**

-  `Consensus Protocols: Paxos <http://the-paper-trail.org/blog/consensus-protocols-paxos/>`_. Henry Robinson. The Paper Trail.


Week 6 - Distributed Consensus II
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Required reading for Monday, May 2**

-  Mike Burrows. `The Chubby Lock Service for Loosely-Coupled
   Distributed
   Systems <http://research.google.com/archive/chubby-osdi06.pdf>`__. In
   Proceedings of the 7th symposium on Operating systems design and
   implementation, OSDI ’06, pages 335–350, Berkeley, CA, USA, 2006.
   USENIX Association
-  Tushar D. Chandra, Robert Griesemer, and Joshua Redstone. `Paxos Made
   Live: An Engineering
   Perspective <http://www.cs.ucla.edu/~kohler/class/08w-dsi/chandra07paxos.pdf>`__.
   In Proceedings of the twenty-sixth annual ACM symposium on Principles
   of distributed computing, PODC ’07, pages 398–407, New York, NY, USA,
   2007. ACM

**Required reading for Wednesday, May 4**

-  Diego Ongaro and John Ousterhout. `In search of an understandable
   consensus algorithm <http://ramcloud.stanford.edu/raft.pdf>`__, 2014

**Other suggested reading**

- `Raft <https://raft.github.io/>`_ website.

Week 7 - Distributed Hash Tables
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Required reading for Monday, May 9**

-  Ion Stoica, Robert Morris, David Karger, M. Frans Kaashoek, and Hari
   Balakrishnan. `Chord: A scalable peer-to-peer lookup service for
   internet
   applications <http://pdos.csail.mit.edu/papers/chord:sigcomm01/chord_sigcomm.pdf>`__.
   SIGCOMM Comput. Commun. Rev., 31(4):149–160, August 2001
-  Antony I. T. Rowstron and Peter Druschel. `Pastry: Scalable,
   decentralized object location, and routing for large-scale
   peer-to-peer
   systems <http://www.cs.unibo.it/~babaoglu/courses/cas12-13/resources/tutorials/pastry.pdf>`__.
   In Proceedings of the IFIP/ACM International Conference on
   Distributed Systems Platforms Heidelberg, Middleware ’01, pages
   329–350, London, UK, UK, 2001. Springer-Verlag

**Required reading for Wednesday, May 11**

-  Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, Gunavardhan
   Kakulapati, Avinash Lakshman, Alex Pilchin, Swaminathan
   Sivasubramanian, Peter Vosshall, and Werner Vogels. `Dynamo: Amazon’s
   Highly Available Key-Value
   Store <http://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf>`__.
   In Proceedings of twenty-first ACM SIGOPS symposium on Operating
   systems principles, SOSP ’07, pages 205–220, New York, NY, USA, 2007.
   ACM

Week 8 - Distributed Data I
~~~~~~~~~~~~~~~~~~~~~~~~~~~

*Note: Instructor will be out of town this week, and the discussions will be led by a
guest instructor to be determined.*

**Required reading for Monday, May 16**

-  Sanjay Ghemawat, Howard Gobioff, and Shun-Tak Leung. `The Google File
   System <http://static.googleusercontent.com/media/research.google.com/en/us/archive/gfs-sosp2003.pdf>`__.
   SIGOPS Oper. Syst. Rev., 37(5):29–43, October 2003
-  Jeffrey Dean and Sanjay Ghemawat. `MapReduce: Simplified Data
   Processing on Large
   Clusters <http://research.google.com/archive/mapreduce-osdi04.pdf>`__.
   Commun. ACM, 51(1):107–113, January 2008

**Required reading for Wednesday, May 18**

-  James C. Corbett, Jeffrey Dean, Michael Epstein, Andrew Fikes,
   Christopher Frost, J. J. Furman, Sanjay Ghemawat, Andrey Gubarev,
   Christopher Heiser, Peter Hochschild, Wilson Hsieh, Sebastian
   Kanthak, Eugene Kogan, Hongyi Li, Alexander Lloyd, Sergey Melnik,
   David Mwaura, David Nagle, Sean Quinlan, Rajesh Rao, Lindsay Rolig,
   Yasushi Saito, Michal Szymaniak, Christopher Taylor, Ruth Wang, and
   Dale Woodford. `Spanner: Google’s globally-distributed
   database <http://static.googleusercontent.com/media/research.google.com/en/us/archive/spanner-osdi2012.pdf>`__.
   In Proceedings of the 10th USENIX Conference on Operating Systems
   Design and Implementation, OSDI’12, pages 251–264, Berkeley, CA, USA,
   2012. USENIX Association

**Suggested papers**

-  Daniel Ford, Francois Labelle, Florentina Popovici, Murray Stokely, Van-Anh Truong, Luiz Barroso, Carrie Grimes, Sean Quinlan. 
   `Availability in Globally Distributed Storage Systems <http://static.usenix.org/events/osdi10/tech/full_papers/Ford.pdf>`__.
   Proceedings of the 9th USENIX Symposium on Operating Systems Design and Implementation, USENIX (2010)
-  Avinash Lakshman and Prashant Malik. `Cassandra: A Decentralized
   Structured Storage
   System <http://www.cs.cornell.edu/projects/ladis2009/papers/lakshman-ladis2009.pdf>`__.
   SIGOPS Oper. Syst. Rev., 44(2):35–40, April 2010
-  Fay Chang, Jeffrey Dean, Sanjay Ghemawat, Wilson C. Hsieh, Deborah A.
   Wallach, Mike Burrows, Tushar Chandra, Andrew Fikes, and Robert E.
   Gruber. `Bigtable: A Distributed Storage System for Structured
   Data <http://research.google.com/archive/bigtable-osdi06.pdf>`__. In
   Proceedings of the 7th USENIX Symposium on Operating Systems Design
   and Implementation - Volume 7, OSDI ’06, pages 15–15, Berkeley, CA,
   USA, 2006. USENIX Association

Week 9 - Distributed Data II
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Readings TBD

Week 10 - Review
~~~~~~~~~~~~~~~~

*Note: There will be no class on May 30 (Memorial Day)*

**Required reading for Wednesday, June 1**

-  Edsger W. Dijkstra. `Self-stabilizing systems in spite of distributed
   control <http://courses.csail.mit.edu/6.852/05/papers/p643-Dijkstra.pdf>`__.
   Commun. ACM, 17(11):643–644, November 1974
-  Leslie Lamport. `Solved Problems, Unsolved Problems and Non-problems
   in
   Concurrency <http://research.microsoft.com/en-us/um/people/lamport/pubs/solved-and-unsolved.pdf>`__.
   SIGOPS Oper. Syst. Rev., 19(4):34–44, October 1985


.. _additional-reading:

Additional Suggested Reading
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`Aphyr's blog <https://aphyr.com/posts/>`_ is a great source of easy-to-read posts on a number of distributed systems topics.
The blog also includes a lot of posts on Aphyr's projects, so here are some links to specific
posts on distributed systems:
  
- `The trouble with timestamps <https://aphyr.com/posts/299-the-trouble-with-timestamps>`_
- `The network is reliable <https://aphyr.com/posts/288-the-network-is-reliable>`_
- `Strong consistency models <https://aphyr.com/posts/313-strong-consistency-models>`_

Henry Robinson's `The Paper Trail <http://the-paper-trail.org/>`_ blog has a plethora of posts
related to many of the papers we discuss in this class.

Survey of important papers on distributed consensus: `A brief history of Consensus, 2PC and Transaction Commit. <http://betathoughts.blogspot.com/2007/06/brief-history-of-consensus-2pc-and.html>`_

`Notes on Theory of Distributed Systems <http://www.cs.yale.edu/homes/aspnes/classes/465/notes.pdf>`_
James Aspnes, Yale University.