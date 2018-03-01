---
layout: post
title:  "WebRTC Quality of Experience and testing"
date:   2018-02-26 14:00:00 +0200
main-image: "/images/blog/Naevatec-WebRTC.png"
image-alt: "WebRTC Testing"
authors:
- guiomar_tunon
---

# WebRTC QoE and testing

The multimedia real-time communications area has been traditionally a complex arena where different interests, standards, technologies and visions compete pushing into divergent directions. The arrival of **WebRTC** brought promises of convergence and openness. 

## But what WebRTC exactly is?

[**WebRTC**][WEBRTC] *("Web Real-Time Communication")* is a collection of communications protocols and application programming interfaces that enable real-time communication over P2P (peer-to-peer) connections. This allows web browsers to not only request resources from back-end servers, but also real-time information from browsers of other users. WebRTC is being standardized by the World Wide Web Consortium ([W3C]) and the Internet Engineering Task Force ([IETF]). The reference implementation is released as free software under the terms of a BSD license. OpenWebRTC provides another free implementation based on the multimedia framework [GStreamer].

WebRTC applications deal with communication between people and this adds complexity to the testing process. Traditional functional and load tests won't grant a satisfying communication. The media flow could be affected in many ways and traditional web application testing wouldn't detect this. We need to be able to test what the user is experiencing during the communication session, not only how the system and the application behaves under specific circumstances. We call that Quality of Experience (QoE) testing.

## What is QoE and how we measure it?

QoE is defined by the International Telecommunication Union ([ITU]) as "The overall acceptability of an application or service, as perceived subjectively by the end-user."[1] It is quite abstract definition but the key is that is is subjective to the user. So can we assert QoE without having the user present? We can't, but we can focus in objective parameters that influence the QoE e.g. transmission rate, delay, jitter, bit error rate, packet loss rate, etc. We can measure these ones and we can define some thresholds from where we can assure QoE is unacceptable. 

Once we have defined these parameters we can measure them and automate tests to record and assert those thresholds aren't surpassed. This isn't easy at all, and multiple approaches have been made over the years, but it doesn’t exits one generic approach private or OpenSource. **ElasTest will change that!**

[**Naeva Tec**][NAEVATEC] has worked with **WebRTC** technologies for many years now, and it's involved in some amazing OpenSource projects such as **[Kurento]** or **[OpenVidu]**. From our experience we believe there is potential for those tools that helps testing WebRTC applications and there fore we have joined the **ElasTest Project** to provide our experience with WebRTC services. We collaborate with a specific WebRTC Use Case called [Full-Teaching]an open-source application to leverage on-line classes for teachers as well as students. It provides multiple communication channels between teachers and students (forums, chats, and real-time video sessions). 

[**Naeva Tec**][NAEVATEC] is also expert in CI/CV so is leading related tasks within the ElasTest Project enabling the CI environment with the appropriate tools and procedures that will help make ElasTest even more awesome!

## References

1. [Vocabulary for performance, quality of service and quality of experience](http://handle.itu.int/11.1002/1000/13408-en?locatt=format:pdf&auth). Recommendation ITU-T P.10/G.10. (PDF)

[WEBRTC]: <https://webrtc.org/>
[NAEVATEC]: <https://www.naevatec.com/en>
[W3C]: <https://www.w3.org/>
[IETF]: <https://www.ietf.org/>
[GStreamer]: <https://gstreamer.freedesktop.org/>
[ITU]: <https://www.itu.int/en/Pages/default.aspx>
[Kurento]: <http://www.kurento.org/> 
[OpenVidu]: <http://openvidu.io/>
[Full-Teaching]: https://github.com/elastest/full-teaching-experiment