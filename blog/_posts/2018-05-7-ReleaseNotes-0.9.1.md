---
layout: post
title:  "ElasTest Release Notes v0.9.1"
date:   2018-05-14 08:00:00 +0200
main-image: "/images/blog/e2e-rest-flow.png"
image-alt: "Testing"
authors:
- patxi_gortazar
---

The new ElasTest release, version 0.9.1, has brought some new features, along with a more stabilized core platform. The following is a list of the main improvements in the project.

* [Jenkins integration](/docs/jenkins/). You don't need to abandon your CI tools. Use ElasTest straight from your Jenkins jobs (Freestyle or Pipeline). For instance, if you're using Pipeline jobs, just wrap up your Pipeline in an elastest step, and you'll be ready to use all the fancy features we bring to testers and developers, like managed browsers! See our [advanced example](/docs/jenkins/advanced-example/) for a more complex scenario.

```
node{
    elastest(tss: ['EUS']) {
        stage ('Executing Test') {
            echo 'Print env variables'
            sh 'env'
            echo 'Set up test environment'
            mvnHome = tool 'M3.3.9'
            echo 'Cloning repository'
            git 'https://github.com/elastest/demo-projects'
            echo 'Run test'
            sh "cd ./simple-web-java-test/;'${mvnHome}/bin/mvn' test"
        }
    }
}
```

* [TestLink integration](https://elastest.io/docs/testlink/). TestLink is the most widely used web-based test management tool and ElasTest provides integration with TestLink. With this integration now you can easily record videos and gather logs and metrics when manually running your tests.
* [New browser Docker images](https://hub.docker.com/u/elastestbrowsers/). We have been developing a new set of browser Docker images that brings the benefits of both Selenoid and Selenium docker images. These images are ready for some awesome features we will be developing in the following months, like changing browser resolution to adapt better to the desktop of our users.
* [Browser recordings](https://elastest.io/docs/web-browsers/manual-browsers/) can now be opened as a new tab or on a floating dialog.
* [Our powerful Log Analyzer](https://elastest.io/docs/log-analyzer/) now remembers previous configurations.
* Added [commands containers](https://elastest.io/docs/testing/sut/) as a new way to launch a SuT, where a new Docker image can be generated on the fly, and then run as SuT.
* The [ElasTest endpoint](https://elastest.io/docs/testing/environment-variables/) for sending metrics from an external SuT has changed, and the ET_MON_LSHTTP_API environment variable is now available also for Test Support Services.
* There are new environment variables available: ET_SUT_CONTAINER_NAME, ET_MON_INTERNAL_LSBEATS_PORT and ET_SUT_LOG_TAG. Those allows ElasTest to do a better job when identifying what's coming from which SuT.
* We have changed the name of the status for a TJob that has been stopped manually to STOPPED.
* [Command line options available when launching ElasTest](https://elastest.io/docs/try-elastest/) are explained in its own subsection

If you want to give it a try, follow our [(brief) instructions here](https://elastest.io/docs/try-elastest/). If you already have ElasTest installed, update instructions can be found [here](https://elastest.io/docs/try-elastest/) in the Update section.

Please, if you find any issue, let us know by reporting it in our [ElasTest GitHub repository](https://github.com/elastest/elastest) using the template provided.

Happy testing!!