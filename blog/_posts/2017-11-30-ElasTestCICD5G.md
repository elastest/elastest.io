---
layout: post
title:  "ElasTest as CI/CD for future 5G software-based networks"
date:   2017-11-30 15:30:00 +0200
main-image: "/images/blog/5Gdemo.png"
image-alt: "ElasTest demo at 5G Week"
---

The ElasTest team participated to this year’s Berlin5GWeek, by demoing the platform at the [IEEE Conference on Network Function Virtualization and Software Defined Networks](http://nfvsdn2017.ieee-nfvsdn.org/). The demo showcased the successful integration of the ElasTest Platform and the Management and Orchestration (MANO) platform [Open Baton](https://openbaton.github.io/) for the continuous integration and future 5G software based networks system validation. 

Open Baton is one of the few open source projects compliant with the ETSI Network Function Virtualization (NFV) MANO specifications. For those not familiar with this ETSI NFV standardization, it is an operators’ lead initiative with the objective of defining an architecture for network infrastructures development by porting and further adapting network functions to the specific cloud environment. ETSI NFV and, in particular, the architecture proposed, as shown in Figure 1, comprises three different domains: the Virtual Network Function (VNF), the Network Function Virtualization Infrastructure (NFVI), and the MANO domain. 

![NFV Reference Architecture](/images/blog/5grefarch.png){: .img-responsive reveal-inline-block offset-top-10 }

On the bottom left we have the NFVI domain constituted by all the hardware components providing on-demand computing, storage, and networking resources. Hardware resources are typically exposed through a virtualization layer to the other domains where VNFs are executed. This domain has been strongly influenced by cloud computing technologies where virtual compute, storage, and networking resources are provided on demand to the components part of the MANO domain. Typically, this layer is implemented by OpenStack considered as the de facto standard. 

Depicted on the top left is the VNF domain, including the VNFs, the Element Management System (EMS), and the classical OSS/BSS. VNFs could be of any type, and the initial set of use cases focused mainly on Virtualized CPE (vCPE), vIMS, and vEPC. Nowadays, there are many other use cases that have been defined as suitable for NFV-like architectures.

Last but not least, on the right side the MANO domain is depicted including all the components required for managing and orchestrating network services on top of the NFVI. It includes the Network Function Virtualization Orchestrator (NFVO), one or more Virtual Network Function Manager(s) (VNFM), and a Virtualized Infrastructure Manager (VIM). Starting from the top, the NFVO represents a completely new entity in the network operator's’ infrastructure, providing functionalities for the on-demand deployments of network services on top of the NFVI. The NFVO plays a central role in the architecture and puts together resource orchestration with service orchestration. In order to instantiate network services the NFVO makes use of two additional logical entities. Firstly, the VIM that is acting as an intermediate between the NFVO and the NFVI so that virtual resources could be acquired on demand. Secondly, one or more VNFMs are in charge of instantiating and configuring VNFs on top of the NFVI.

Open Baton is the result of an agile design process having as major objective the development of an extensible and customizable NFV MANO compliant framework, capable of orchestrating network services across heterogeneous NFVIs. It can manage a diverse ecosystem of VNFs through its Generic EMS and Generic VNFM, composing them at runtime in any kind of network services. It manages a multi-site NFVI supporting heterogeneous virtualization and cloud technologies.

The integration with ElasTest provides a comprehensive continuous integration system where network services as the System(s) Under Test (SUT) are deployed and managed through the Open Baton framework. Figure 2 provides an architectural overview of the integration between the ElasTest platform and the Open Baton framework.

![ElasTest Architecture](/images/blog/elastestarch.png){: .img-responsive reveal-inline-block offset-top-10 }

The SUT can be of any type. What ElasTest users have to do is to define a [network service descriptor](http://openbaton.org/documentation/ns-descriptor/) as composition of multiple VNFs, and deploy them on the NFV Infrastructure of preference (i.e. OpenStack). Once the deployment operation is executed, Open Baton provides runtime information (like endpoints, IPs, configuration parameters, etc.) which can be used for configuring testing jobs. Furthermore, the ElasTest and Open Baton communities are working together in automating the deployment operations of such network services directly from the ElasTest platform, as managed SUT. In this way, the user can define different kind of testing jobs, and execute them including the re-deployment operation of the SUT on top of the NFVI through Open Baton. 

A concrete example would be the SUT consisting of the Open5GCore network service, representing also one of the vertical demonstrators of the ElasTest project.  As mentioned in the previous blog post, Open5GCore is a reference implementation of the future 5G mobile core network architecture providing the following VNFs: HSS, SGWC-PGWC-MME, SGWU-PGWU, BT, INET-GW. 

You may be interested in having additional information about this activity don’t hesitate to contact us (info@elastest.io). 

Happy 5G testing!

\[1\]: [ETSI Network Function Virtualization (NFV) architecture specification](http://www.etsi.org/deliver/etsi_gs/nfv/001_099/002/01.01.01_60/gs_nfv002v010101p.pdf)