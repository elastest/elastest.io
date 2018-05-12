---
layout: post
title:  "ElasTest Release Notes v0.9.1"
date:   2018-05-11 08:00:00 +0200
main-image: "/images/blog/e2e-rest-flow.png"
image-alt: "Testing"
authors:
- patxi_gortazar
---

The new ElasTest release, version 0.9.1, has brought some new features, along with a more stabilized core platform. The following is a list of the main improvements in the project.

* [**Jenkins integration**](/docs/jenkins/). You don't need to abandon your CI tools. Use ElasTest straight from your Jenkins jobs (Freestyle or Pipeline). For instance, if you're using Pipeline jobs, just wrap up your Pipeline in an elastest step, and you'll be ready to use all the fancy features we bring to testers and developers, like managed browsers! See our [advanced example](/docs/jenkins/advanced-example/) for a more complex scenario.
* [**TestLink integration**](https://elastest.io/docs/testlink/). TestLink is the most widely used web-based test management tool and ElasTest provides integration with TestLink. With this integration now you can easily record videos and gather logs and metrics when manually running your tests.
* [**New Docker images for browsers**](https://hub.docker.com/u/elastestbrowsers/). We have been developing a new set of browser Docker images that brings the benefits of both Selenoid and Selenium docker images. These images are ready for some awesome features we will be developing in the following months, like changing browser resolution to adapt better to the desktop of our users.
* [**Browser recordings**](https://elastest.io/docs/web-browsers/manual-browsers/) can now be opened as a new tab or on a floating dialog.
* [Our powerful **Log Analyzer**](https://elastest.io/docs/log-analyzer/) now remembers previous configurations.
* **Generate your SuT on the fly** with [Commands Containers](https://elastest.io/docs/testing/sut/): a new Docker image can be generated on the fly, and this image will be run as the SuT.
* [**ElasTest Command line options documented**](https://elastest.io/docs/try-elastest/) in its own subsection within the installation page
* **Changes in environment variables**: the [ElasTest endpoint](https://elastest.io/docs/testing/environment-variables/) for sending metrics from an external SuT has changed, and the ET_MON_LSHTTP_API environment variable is now available also for Test Support Services.
* There are **new environment variables available**: ET_SUT_CONTAINER_NAME, ET_MON_INTERNAL_LSBEATS_PORT and ET_SUT_LOG_TAG. Those allows ElasTest to do a better job when identifying what's coming from which SuT.
* We have changed the name of the status for a TJob that has been stopped manually to STOPPED.

If you want to give it a try, follow our [(brief) instructions here](https://elastest.io/docs/try-elastest/). If you already have ElasTest installed, update instructions can be found [here](https://elastest.io/docs/try-elastest/) in the Update section.

Please, if you find any issue, let us know by reporting it in our [issue tracker](https://github.com/elastest/elastest) using the template provided.

Do you want to support the project, and keep it going? **Give us extra energy by starring the [ElasTest repository](https://github.com/elastest/elastest)!!**