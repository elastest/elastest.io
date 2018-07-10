---
layout: post
title:  "Say it in plain English"
date:   2018-07-10 08:00:00 +0200
main-image: "/images/blog/ere.png"
image-alt: "Testing"
authors:
- magda_kacmajor
---

Since the dawn of DevOps, the volume and frequency of required testing have increased significantly, making test automation indispensable for any large software project. However, test automation is a complex task, highly resource-consuming both in terms of time and the required skills.

ElasTest provides features that support [managing and running automated tests](https://elastest.io/docs/testing/unit/), paving a convenient path for [Continuous Testing](https://www.techwell.com/techwell-insights/2015/08/part-pipeline-why-continuous-testing-essential). But automated test scripts to be executed do not come out of blue – time and effort need to be spent to build them out.

### How to make test automation more efficient at the test case creation stage?
Any large software repository captures hundreds or thousands hours of work contributed by experienced and talented developers and testers. ElasTest Recommendation Engine (ERE), brought into ElasTest project by [IBM Ireland Innovation Exchange](https://www.ibm.com/ie-en/) team, employs deep learning to unlock this knowledge and use it to the advantage of other testers.

Key skills required from any test automation developer can be roughly divided into two sets: the competence to write code, and the competence to design test cases. These two sets of skills are rather loosely related – that is, one can be brilliant at one aspect of the job but not so good at the other, depending on their previous work experience and individual preferences.

Let’s start with a closer look at the first aspect. Coding test cases, as any programming job, is the act of human telling the computer what to do, and a programming language is the bridge between human thinking and machine thinking. A developer does not need to worry about translating source code into machine language, since this is done by automated utilities. However, the translation from human language to source code remains the responsibility of the programmer. 

Here is where ERE comes to aid: user can briefly describe the task for the machine using natural language, and cede the job of writing the source code to the engine. Rather than being guided by code structure or data flows, the engine learns directly from existing examples of tests created by experienced practitioners, and generates new code based on that knowledge. 

Furthermore, ERE uses abstract, deep representations of test cases already existing in the repository to find the examples that are most relevant to the generated code, and presents them for perusal of test developer. These existing examples can be either reused, or serve as an inspiration for designing further test cases.  

### Is that all?
No, it is just the beginning! Current work on ERE focuses on enabling direct recommendations on designing new test cases. Seeing inspiring examples is nice, but a busy tester will surely appreciate a more straightforward advice – ideally, a full list of new test cases recommended for a given project. The way to achieve this is to reuse knowledge not only from a single software repository but also take advantage of the wisdom of big data stored in numerous open source repositories available online. 

If there are any other forms of recommendations that you’d love to see as a tester, do not hesitate [to let us know](https://groups.google.com/forum/#!forum/elastest-users)!
