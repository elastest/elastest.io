---
layout: post
title:  "Introducing ElasTest"
date:   2017-03-28 15:22:00 +0100
main-image: "/images/blog/elastest_logo_grey_horizontal_706x200.png"
image-alt: "ElasTest logo"
---

It has been almost six years since Marc Andreessen published his article "Why software is eating the world" [1], but it could have been written just a month ago. Wherever we look, we find software supporting our actions, likings, and jobs. Software is becoming so pervasive that software developers are pushed towards their limits by developing applications that scale in and out, that are adapted to the cloud, fault-tolerant and resilient. From small startups and SMEs to big companies, nowadays everyone is running complex distributed systems on cloud infrastructures. Whether you build your own or you rely on third party services (Amazon RDS is a good example), your system is distributed in nature. 

The problem is that we move so fast that we can hardly develop the tools that can assist us with **assessing** that our distributed software complies with the **quality** demanded by our users. A good toolkit is like a lifeguard when developers need to reproduce things, identify problems and fix bugs. There is no bug-free software; however, with current ratios of shipping software and deploying applications, the question that arises is whether we are adequately and effectively testing our software.

Recent trends like microservice architectures [2], Command Query Responsibility Segregation (CQRS) [3], event-driven distributed systems, domain driven design, among others, are requiring testing practices that are far beyond the possibilities of the current tools for testing software, because they require difficult to implement techniques, state-of-the-art approaches and, in the end, a lot of effort to test just a simple condition like ensuring a message is delivered to the corresponding service.

This gets even worse when it comes to test our application under **real conditions**. If we are exposing REST APIs to mobile applications, we may want to test it through a 4G/5G connection; or we may want to simulate packet loss. In addition, if we are building resilient systems, we may want to test that the system still works under pressure: node lost, connection loss, application killed, or CPU/network bursts. There are tools out there that can help us to test these conditions (Simian Army from Netlix being one of the most prominent [4]); however, **developers and testers** will need to spend whole weeks tuning these tools to adapt them to their specific infrastructure and use cases. Furthermore, QA teams are used to define test use cases and run them against "the platform." They are user-oriented, and they want to push the system towards real conditions. They are the last step before production. 

So, what if testers could have a tool that enabled them to build test cases based on simpler ones defined by the development team? What if they could run tests under specific conditions of the system under test? What if they could get **logs, monitors, probes, and oracles** to ensure everything works as expected through **a GUI that focuses on end-to-end testing**?

This kind of problems of modern, distributed software is what ElasTest will address. Within the ElasTest project, we are building a set of **open source** tools specifically tailored to **end-to-end testing**. However, all these promises might seem a big hype. That is the reason why we came up with very concrete objectives. Most of them are business objectives, that is, they are tailored towards providing a tangible business value. Other objectives focus on the team helping with assessing the product.

The list of **business outcomes** is the following one:

* To reduce the overall **time to market** of large distributed systems in an average factor of 20%.
* To increase the **reusability** of code, tools and architectures devoted to non-functional software testing on large distributed systems in a factor of, at least, 500% (that is, x6).
* To increase the overall **tester productivity** (measured as lines of code tested per time unit) for integration and system tests in a factor of, at least, 100% (that is, x2).
* To decrease the **corrective maintenance** effort of SiL in a factor of, at least, 50%.
* To decrease field **failure reports** of large distributed systems in a factor of, at least, 30%.
* To increase the **scalability** (measured as the total number of concurrent supported sessions), **robustness** (measured as down-time after computing failures), **security** (measured in incidents per time unit) and **QoE** (Quality of Experience) of large distributed systems in an average factor of 20%.

**Subjective outcomes**, related to the teams, are listed below:

* To increase the tester subjective feelings of **simplicity, satisfaction, efficacy, confidence and usefulness** when involved in testing tasks for large distributed systems in a factor of at least 1 each in a scale of 5.
* To increase the subjective feelings of end-users in terms of **efficiency, overall satisfaction and lack of risks** when using large distributed systems in a factor of at least 1 each in a scale of 5.

These objectives may seem ambitious, but the team behind ElasTest has long, wide and valuable experience in developing and testing large complex distributed systems. We will leverage this knowledge to build something that is not only new, but that is also going to be shipped as an extensible, [**open source toolkit for end-to-end testing**](https://github.com/elastest).

If you want to stay tuned, we encourage you to follow us on [**Twitter**](https://twitter.com/elastestio). In addition, if you want to keep in touch, comments are very welcome in our [**user mailing list**](https://groups.google.com/forum/#!forum/elastest-users), where we would love to hear from you and your specific use cases regarding end-to-end testing. After all, we all want to make something useful for everyone. 

**Good bug hunting!**

[1] Marc Andreessen, Why software is eating the world, *Wall Street Journal*, Oct. 2011

[2] Chris Richardson, Pattern: Microservice Architecture, [http://microservices.io/patterns/microservices.html](http://microservices.io/patterns/microservices.html)

[3] Martin Fowler, CQRS, [https://martinfowler.com/bliki/CQRS.html](https://martinfowler.com/bliki/CQRS.html)

[4] The Netflix Simian Army, [http://techblog.netflix.com/2011/07/netflix-simian-army.html](http://techblog.netflix.com/2011/07/netflix-simian-army.html)