---
layout: post
title:  "Third face to face meeting in Madrid on 5-6 September"
date:   2017-09-11 11:30:00 +0200
main-image: "/images/blog/3rdMeeting.jpg"
image-alt: "ElasTest third face to face meeting"
authors:
- patxi_gortazar
---

During the 5th and 6th of September we held our third face to face ElasTest meeting, this time in Madrid. For this meeting we were supposed to have a proof of concept (PoC) for each component, hence we were a bit nervous. Obviously, having PoCs for each of them by the first week of September required us to work hard during the Summer. However, during the 2nd face to face meeting in Berlin we defined carefully this second iteration so we could finish assets in time. 

The official deadline for this second release was 25th of August. All components were in a good shape by that time, although they only worked in isolation (no integration yet with one another). We have already talked about our Definition of Done for this second release on a [previous blog post](http://elastest.io/blog/2017/05/08/FaceToFaceMeetingAtBerlin.html). The idea of this iteration was to have a kind of MVP for each of the components, so we defined carefully the Definition of Done (DoD) for this release. Every component should have at least 70% code coverage, some main functionalities  working, a good user and developer documentation and a tag in the source code repository. In addition, as we choose Docker as our first supported platform, all images had to be available in DockerHub. And here we are: all components complied with the DoD. Results can be seen in the respective repositories for each of the ElasTest components at [our GitHub account](https://github.com/elastest/). 

For those readers that want to have a look at what we have built so far, we prepared a video demonstrating each of the components. Those **videos are available in [this PoC list](https://www.youtube.com/playlist?list=PLAu4uAuPmhO7WngYVdBoc2eaNjvl6dK3I)** in the ElasTest's YouTube account. Take into account that some components provide a GUI, but others do not. Hence, some videos are showing a user interacting with some kind of user interface, but others just show an interaction through the command line.

During this third meeting in Madrid we spent two whole days working together on two main axes:

* **Integration issues**. During the week before the meeting we start working on putting components to work together, to try to end up with an integrated ElasTest platform that included all the components. Some issues were found, and those were discussed during the first day of the meeting, working out solutions for each of them.

* **How to provide value to end-users**. During our second day we mainly discussed in which ways ElasTest could be leveraged so that all stakeholders could have added value on their specific processes. So far, we identified four stakeholders: testers, developers, business people/managers, and researchers.

During this iteration we've been also designing some marketing material (as it is well-known, a picture worth 1,000 words) and we've been communicating the project in different events, like the [ExpoQA conference](http://expoqa.com/) (slides [here](https://www.slideshare.net/elastest/expoqa-2017) and [here](https://www.slideshare.net/elastest/expoqa-2017-using-docker-to-build-and-test-in-your-laptop-and-jenkins)) and the [TAROT 2017 Summer School](http://tarot2017.dieti.unina.it/) (slides [here](https://www.slideshare.net/elastest/tarot-2017)). We didn't have anything that could be demonstrated but we wanted to gather feedback on the features we planned to develop. In particular, talking to testers was very useful and gave us some new ideas and features that were not considered at first.

As part of the marketing material **we prepared a [technical presentation](https://www.slideshare.net/elastest/elas-test-technical-presentation)** where the main challenges in software testing of large complex distributed applications are depicted. We also show the main features of ElasTest and its architecture. So worth having a look if you're interested on what can you take away from this project.

We can keep you on the loop for next releases and updates. Just follow us on [Twitter](https://twitter.com/elastestio/), join our [user mailing list](https://groups.google.com/forum/#!forum/elastest-users), or subscribe to our [newsletter](http://elastest.io/#newsletter). We are really happy to hear from you and your specific use cases, so keep us informed about how you would like to use ElasTest for your product.

Have a nice week!

