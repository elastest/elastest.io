---
layout: post
title:  "ElasTest Makes Testing Productive"
date:   2018-04-19 10:00:00 +0200
main-image: "/images/blog/elastest-services.png"
image-alt: "Testing"
authors:
- andy_edmonds
---

There is no doubt that the delivery of services to end-users is a huge productivity gain. It is this that is a key aspect when we talk about digitisation of business today. Being able to provide a service on-demand to a user, a business, a family or a developer allows that person to concentrate on the key tasks that they need to accomplish. In the world of business this is understood to be focusing on the core business that is carried out. Distractions away from this core business results in wasted efforts and takes from the core business focus. This decreases the potential for increased value and ultimately earning. Defocusing results in reduced opportunity potential, something that is needed by all businesses in order to seize and execute new means of growth.

**So what has this all got to do with testing and ElasTest?!** 

Consider a development house who has a large software system to test. There are core systems within it that are the key differentiator that provides the value, which attract customers and influence purchasing decisions. For those systems, the development house will invest heavily in testing of those systems. However in order to carry out successful and complete testing of the system, they require additional functionality to be offered, deployed and supported in-house. This is exactly the manifestation of distracting from core business value, introducing further technical debt and expense, when it should not be required. 

The answer to this issue is for the required expertise and functionality to be brought in-house from an external provider. That is, for the functionality to be delviered as a service by an external company.

**"But how can this be done?", you question...**

It is exactly this capability (and other related ones) that the [Zürich University of Applied Sciences (ZHAW)](https://www.zhaw.ch/en/university/) at the [ICCLab](http://blog.zhaw.ch/icclab) is providing within ElasTest - providing the means to deliver external services into a complete testing scenario. ZHAW is developing a standards-based service delivery framework that allows a varied set of cloud-native services to be created on-demand and made ready for use within test runs (known as TJobs in ElasTest-talk). The software that is being developed is known as the [ElasTest Service Manager (ESM)](https://elastest.github.io/elastest-service-manager/) and provides an [Open Service Broker API (OSBA)](https://www.openservicebrokerapi.org) compliant interface to offered services, making it easy to integrate with enterprise systems. Currently the set of services that the ESM delivers are:

* [ElasTest User-emulator Service (EUS)](https://github.com/elastest/elastest-user-emulator-service): provides browsers for both manual interaction and automated interacion under the control of tests, by means of starting browsers in containers. This service is developed by the [Universidad Rey Juan Carlos (URJC)](http://www.urjc.es/).
* [ElasTest Device Emulation Service (EDS)](https://github.com/elastest/elastest-device-emulator-service) provides a service to emulate behaviors of sensors, actuators and smart devices. This service is developed by [Technische Universität Berlin (TUB)](http://www.tu-berlin.de/menue/home/parameter/en/).
* [ElasTest Monitoring Service (EMS)](https://github.com/elastest/elastest-monitoring-service): provides a monitoring infrastructure suitable for inspecting executions of a SuT (System under Test) and the ElasTest platform itself online. This service is developed by the [IMDEA Software Institute](http://software.imdea.org/).
* [ElasTest Big Data Service (EBS)](https://github.com/elastest/elastest-bigdata-service): provides a service to process large quantities of data using user provided algorithms. This service is developed by [Relational](http://www.relationalfs.com/).
* [ElasTest Security Service (ESS)](https://github.com/elastest/elastest-security-service): provides a service to detect security vulnerabilities in the system under test. This service is developed by the [IMDEA Software Institute](http://software.imdea.org/).

From the research challenges angle, the ESM will provide ElasTest and us the means to understand experiment with reliable, just-in-time service delivery. We envison the importance and need for: 

* Near-real time service delivery with minimal wait times in having network-based access to a particular service. This will require the consideration of resource frameworks that far exceed the performance of current container-based technologies such as Docker;
* In order to make such services reliable and measurable suitable observability mechanisms will be needed and this work on observability tooling is being carried out by ZHAW in a related area of the [ElasTest Monitoring Platform (EMP)](https://github.com/elastest/elastest-monitoring-platform);
* With information collected on running services of the ESM, the question on how leveraging machine and deep learning arises, where such approaches can be used to detect anomalous behaviours that could indicate runtime errors or issues and signal remediation actions.
* From a business perspective, how can scaling of delivered services be supported yet respect financial cost targets set by the end-user. Indeed how can SLAs of delivered services be defined in such a way to be self-validating?

There are more challenges to be researched in the context of service delivery, as well as the open source engineering efforts with ElasTest. Be sure to keep an eye both on [this blog](http://elastest.io/blog/) but also the [ElasTest Github community](https://github.com/elastest) for more developments.