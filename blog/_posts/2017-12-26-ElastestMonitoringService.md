---
layout: post
title:  "Research in Monitoring within ElasTest"
date:   2017-12-26 15:00:00 +0200
main-image: "/images/blog/ems.png"
image-alt: "ElasTest Monitoring Service architectural diagram"
authors:
- cesar_sanchez
- felipe_gorostiaga
---

Software is becoming more and more oblivious in all aspects of our lives. Software based companies are becoming economically more dominant, opening new economic sectors with surprising innovations and making economic processes more efficient (see, for example, Marc Andreeseen "Why software is eating the world" [1]). Even in classical industries, like the automotive industry, software is involved in more and more functionalities, and very rapidly gaining a higher ratio of costs and resources in car development.

This tendency has two important consequences: (1) software is more complex to develop, deploy and maintain; and (2) our dependence on software reliability (and the complexity of the software reliability tasks)  presents important challenges.

Software reliability is a notoriously difficult and challenging process.  This is witnessed by the increasing costs, in terms of time and money, that is invested in increasing the reliability of the software before deployment. This trend is exacerbated in complex systems, not only in the critical software domains like automation, where software bugs can have catastrophic consequences, but also in areas dominated by the time to market, like for example cloud based applications.

Software reliability has received a lot of attention for decades, both in academia and in industry, and many techniques have been developed and applied.  Most techniques are based on a two-step effort, where the reliability techniques are applied a-posteriori, after the software development process creates the software artifact.  Even though software reliability has been improved by the invention of modern programming languages and the use of more sophisticated software development processes, verification and validation is still required.  Verification techniques range from formal verification on one hand that aims at providing a definite guarantee of the correctness, to testing at the other extreme where the actual software is exercised repeatedly, aiming to find bugs.

Formal techniques like static formal verification requires lots of expertise and human resources, and in spite of recent breakthroughs, it does not scale to large projects and complex properties. Consequently, it is typically only applied to small pieces of critical software. Testing is, by far, the dominant approach in all non-safety critical areas of software development, including cloud computing.

The project ElasTest aims to improve the process of testing large cloud applications, and in turn improve the quality of the resulting software and reduce the cost of this process.  Cloud computing applications share some of the characteristics that make software testing difficult.
- First, cloud application software is inherently concurrent. It is
  well-known that it is unfeasible to exercise all interleavings of
  concurrent software, and that concurrency bugs are extremely hard to
  find, repeat, explain and correct.
- Second, cloud application software is inherently distributed and
  lousily coupled, components can fail independently, and there are
  complex failure dependencies between components. This is witnessed by
  the merge of programming and operation activities in the same group of
  experts, modernly known as DevOps [3].
- The **elasticity** of cloud applications makes the problem even more
  difficult because concurrent and distributed components can be
  spawned and connected dynamically.
- As a consequence of the previous points, the run-time system that
  cloud applications depend on is more sophisticated than in earlier
  platforms and more often less reliable itself.
- Cloud applications are **reactive**, in the sense that there is an environment
  that the application interacts with including the cloud infrastructure, other
  applications and  the users. Cloud applications are typically **interactive**
  so unknown users are meant to use the application.
- The users of cloud applications can also sometimes be malicious,
  exercising the software in unexpected ways sometimes with the
  intention of breaking the functionality with some undesirable target
  goal.
  
The main interest of our IMDEA Software research group in ElasTest is the exploration of runtime verification techniques in improving the testing process of cloud elastic applications. Runtime Verification [2] is an attempt to leverage the research in static verification, and in particular in behavioral specification languages, to applicable dynamic techniques. In runtime verification a specification is used to generate a monitor that inspects the execution of a software system in order to detect violations of the specification. This technique has been used to complement testing, by facilitating the uncovering and explanation of bugs, or even be for dynamic repair.

In the context of the project ElasTest, we are focusing on the development of a monitoring component that can be spawned and used in a testing activity. The monitoring service is a Test Support Service that can be used in different tests independently.  The ElasTest Monitoring Service (EMS) will run outline (as opposed to inlined embedded in the system under test) by collecting information from the system under test with minimal instrumentation, and also collecting events. The EMS will also run online, alongside the system under test during the testing process (as opposed to offline analyzing traces in a post-mortem manner). 

The main research challenge of the EMS is to find a monitoring description language that can be:
- usable for the users describing tests, to effectively to collect and
  correlate the necessary information to assess the outcome,
- to facilitate the description of tests that dynamically
  *direct* the test to explore possible bugs more effectively,
- to make use of the resources to create an efficient online
  evaluation language, specific to the monitoring needs for testing

This challenge requires combining techniques from three active areas of research in recent years: runtime verification, event correlation and complex-event processing, and cloud monitoring.

These techniques have potential beyond the goals of ElasTest, like better orchestrating the bootstrap of cloud applications or specific monitoring systems in production.

We encourage you to follow us on [**Twitter**](https://twitter.com/elastestio). In addition, if you want to keep in touch, comments are very welcome in our [**user mailing list**](https://groups.google.com/forum/#!forum/elastest-users).

Happy testing!!

[1] Marc Andreessen, [Why software is eating the world](https://www.wsj.com/articles/SB10001424053111903480904576512250915629460), Wall Street Journal, Oct. 2011

[2] [Wikipedia entry on Runtime Verification](https://en.wikipedia.org/wiki/Runtime_verification)

[3] [Wikipedia entry on devops](https://en.wikipedia.org/wiki/DevOps)
