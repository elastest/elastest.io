---
layout: post
title:  "ElasTest architecture and components"
date:   2017-09-18 11:30:00 +0200
main-image: "/images/blog/3rdMeeting.jpg"
image-alt: "ElasTest architecture"
authors:
- patxi_gortazar
---

During the first iteration of the project, running from January to May, we focused, among other things, on defining the architecture of ElasTest. It was not easy, as first we all needed to be aligned on what was ElasTest supposed to be. Thus, we tried to identify end-users. Developers were clearly a target, but testers turned out to be interested also in some of the features ElasTest could provide. Since the very beginning, it was clear that the project needed to follow a lean startup approach to development. This approach requires us to be aligned with the industry. We have partially addressed this issue in our Advisory Board, a group of experts external to the project intended to give advice on the project targets, status and risks. Some members of this board comes from the industry with a huge experience in testing in different domains. But we are also embracing this lean startup model by pivoting when needed during the development. 

Obviously, this kind of progress, engineering-driven, requires much more coordination effort. Hence, we are having several calls per week on different topics. However, we strongly believe that this minimize the risk of integration. Indeed, by December we plan to have end-to-end tests for each of the components that will check at any time later on that those components can be integrated into the platform. We think this is a big achievement, and all partners in the project's consortium are working hard to make this possible. From January 2018 on, each of the partners will be able to focus on their own components, developing new features, doing research or innovation, with confidence. Our Jenkins CI server will monitor that all components can be integrated by running their respective end-to-end tests. 

Introducing our development procedure was needed in order to make clear that our achitecture is live, and changes over time. Changes in the architecture are driven by three forces: end-users, as we scout the market; features we need to implement, because either they were compromised in the project proposal or they were seen as useful by end-users; and quick feedback, as we plan to release early and often to get feedback as fast as possible in order to steer the project based on the feedback received.

Up to now the architecture more or less resembles a microservice architecture. There's one big difference: storage is centralized. This is to allow the import/export of data to/form the platform. And we will go into more details in a moment.



In a forthcoming post we are going to describe our architecture and components, but for the moment, probably a high level overview is all what we need to understand what's going on in the videos. Basically, the ElasTest platform is split into 4 big areas:

In a forthcoming post we are going to describe our architecture and components, but for the moment, probably a high level overview is all what we need to understand what's going on in the videos. Basically, the ElasTest platform is split into 4 big areas:

* **Core platform components**: these are components needed to run ElasTest itself. These components are always running and work as services for other ElasTest components. Basically they provide resources to other components, monitor the platform, and provide storage capabilities. The GUI of ElasTest is also part of the core, and the main entry point for users.

* **Test Support Services**: these are components that provide added value to testers and developers. Test Support Services are supposed to be used either by the end user (for instance for manual testing) or by developers when programming tests. Basically, they provide some functionalities to tests, enriching the kind of assertions (oracles) we can build and easing some tasks that are usually complex (like setting up browsers to be used in end-to-end tests). ElasTest will support five different Test Support Services out of the box, although more can be added through plugins: browser and mobile devices as a service within the platform; emulation of IoT devices, actuators and sensors; a monitoring service to build runtime probes; security services; and big data services to enable analysis of the huge amount of data that can be generated when exercising a large system under test.

* **Engines**: these components provide value to end-users by means of helping users in the definition, building, programming or running of tests. The following engines are going to be built: a cost engine to estimate and measure actual costs of running tests on cloud infrastructure; a way of orchestrating tests for defining complex test scenarios; a recommendation engine providing suggestions on which tests to implement based on previous knowledge; and a question & answer engine that can be used to ask natural-language questions.

* **Integration with third-party tools**: we plan to build integrations with [Jenkins](https://jenkins.io/), and at least one widely adopted IDE. These integrations pretend to ease the usage of the ElasTest platform for your daily tasks. In addition, we will build a toolbox to ease the installation of ElasTest on different environments and infrastructures. 

During this third meeting in Madrid we spent two whole days working together on two main axes:

* Solving integration issues. We dedicated the week before the meeting to start the integration efforts to try to end up with an ElasTest platform including all the components. Some issues were found, and those were discussed in the meeting, working out solutions for each of them.

* Refining our thoughts about how to provide value to end-users. Here we discussed in which ways ElasTest could be leveraged so that value is added for different stakeholders. So far, we identified four stakeholders: testers, developers, business people, and researchers.

During this iteration we've been also designing some marketing material (you know, a picture worth 1,000 words) and communicating the project in different events, like the [ExpoQA conference](http://expoqa.com/) (slides [here](https://www.slideshare.net/elastest/expoqa-2017) and [here](https://www.slideshare.net/elastest/expoqa-2017-using-docker-to-build-and-test-in-your-laptop-and-jenkins)) and the [TAROT 2017 Summer School](http://tarot2017.dieti.unina.it/) (slides [here](https://www.slideshare.net/elastest/tarot-2017)). We didn't have anything that could be demonstrated or shown, but we wanted to gather feedback on the features planned and the initial architecture. In particular, talking to testers was very insightful and gave us some new ideas and features that were not considered at first.

We also prepared a [technical presentation](https://www.slideshare.net/elastest/elas-test-technical-presentation), where the main challenges in software testing of large complex distributed applications are depicted. We also show the main features and architecture of ElasTest, so worth having a look if you're interested on the take-aways for this project.

We can keep you on the loop for next releases and updates. Just follow us on [Twitter](https://twitter.com/elastestio/), join our [user mailing list](https://groups.google.com/forum/#!forum/elastest-users), or subscribe to our [newsletter](http://elastest.io/#newsletter).

Have a nice week!

