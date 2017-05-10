---
layout: post
title:  "Face to face meeting in Berlin"
date:   2017-05-8 15:32:00 +0200
main-image: "/images/blog/ElasTest_team.jpg"
image-alt: "ElasTest team"
---

During 4th and 5th May, we held our second face to face meeting, this time in Berlin, hosted by the Fraunhofer Institute. The [Fraunhofer Institute for Open Communication Systems (FOKUS)](https://www.fokus.fraunhofer.de/en) makes research in and develops application-oriented solutions related to communication technologies and services and their interoperability. They are paving the way for architectures and protocols of future communication networks and platforms by measuring and testing distributed telecommunication and software systems. Fraunhofer FOKUS has been developing innovative processes from the original concept to the pre-product in companies and institutions for more than 20 years. The institute can be considered a link between university research and industry.

In the context of the ElasTest project, Fraunhofer provides one of the vertical solutions that will be used to demonstrate the ElasTest platform as well as its capabilities for **reducing maintenance efforts and time-to-market**. In the telecommunications industry, solutions like the one provided by ElasTest can make a big difference that may push companies forward.

This second face to face meeting also marked the end of our first release. As a result of this iteration, we showcased a proof of concept of what ElasTest could look like when integrated within [Jenkins](https://jenkins.io/) (see screenshot), and presented our findings regarding the architecture for ElasTest. As part of this release, we also looked back and did a retrospective to improve our methodology. The retrospective was really fruitful, and once again it was clear that everyone involved in the project had a true interest in pushing it forward.

![ElasTest Proof of Concept]({{ site.url }}/images/blog/elastest-torm-poc-small.png)

We then entered into the planning of the second release. This release will last until the end of August, and it puts a huge pressure on the partners developing ElasTest, as each and every one of them needs to have a proof of concept of each of their components. 

However, before starting the development, we have to polish our APIs. We did a great job in the architecture in our previous iteration, but our APIs are still a bit rough. During the last iteration, we agreed on using the [Open API specification](https://www.openapis.org/) to define our REST APIs (we will also use non-REST APIs, but that's a story for a different post). So, by the end of May, we should have our different APIs refined and published on our website.

Regarding the development, we set some goals for this release. These may seem a bit ambitious, but everyone agreed on them. This is our **Definition of Done** for each component in this release:

* **Unit tests** & **end-to-end tests**
* **Test coverage** of at least 70%
* **Documentation** in markdown format, hosted within a docs folder in the repository and linked from the README.md file
* **Video** demoing the component
* **Automatic building and publishing** of development artefacts in ElasTest CI's platform 
* **Docker image** for the component published in [ElasTest's dockerhub organisation](https://hub.docker.com/u/elastest/) (as we plan to ship components as docker images)

Hence, during the following months, we will be starting the development of the platform, and you will see a lot of activity in our [GitHub organisation](https://github.com/elastest/). Watch us on GitHub, and don't forget to star the project!

Next face-to-face meeting will be held in Madrid. In the meanwhile... 

Happy coding!
