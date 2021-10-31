---
author: <a href="https://www.linkedin.com/in/naman2001/"> Naman Lakhwani</a>
categories:
- Google Summer of Code
- Open Source
- CNCF
- Thanos
- GoLang
- TLS
comments: true
date: "2021-08-15T00:00:00Z"
published: true
title: Google Summer of Code with Thanos (CNCF)
---

Namaste! :pray:

I am Naman Lakhwani, an undergraduate student at the Indian Institute of Information Technology, Gwalior, India. I worked on the Thanos project over the summer as part of the Google Summer of Code program 2021. In this blog, I would be encapsulating my journey shedding light upon the learnings I earned.

### :point_right: What is Google Summer of Code?
[Google Summer of Code](https://summerofcode.withgoogle.com/) is a global program focused on bringing more student developers into open source software development. Students work with an open-source organization on a 10-week programming project during their break from school/university.

### :point_right: What is Thanos?
[Thanos](https://thanos.io/) is an open-source, highly available Prometheus setup with long-term storage capabilities, and It is a CNCF Incubating project. Thinking of what Prometheus is? Prometheus is an open-source system monitoring and alerting toolkit. Thanos seamlessly extends Prometheus in a few simple steps and it is already used in production by hundreds of companies that aim for high multi-cloud scale for metrics while keeping low maintenance cost.

### :point_right: Starting my Google summer of code journey with Thanos.
I have been contributing to Thanos since December 2020. Fortunately, I got to know that Thanos is taking part in GSoC this year too. So I went through the proposed project, drafted a detailed proposal for the same, and submitted it, which the mentors finally selected, and I got the opportunity to work under them. The official coding period started on the 8th of June 2021. We decided the workflow for the next three months and discussed the expectations we had from each other. We decided to meet over a video call weekly on Thursdays to get unblocked, discuss the progress made so far and action items for the next week.

Accepted proposal can be found here: [Automated TLS client support](https://docs.google.com/document/d/1UMdpJulzImtOkjNRl4_JJplX1E3HpypMgAYkYZcJd_M/edit?usp=sharing)

### :point_right: What was Planned?
So the problem with Thanos' Querier component was that it supports basic mutual TLS configuration for internal gRPC communication, which works great for primary use cases. However, it still requires extra forward proxies (e.g., envoy) to make it work for bigger deployments. It was also hard to rotate certificates automatically and configure safe mTLS. So the main goals we decided were to remove the dependency for extra forward proxies by adding support for per-endpoint TLS configuration in Thanos Query Component and to enable automatic certificate rotation without restart. In big projects, before starting the actual implementation, it’s always helpful to have a consensus on a proper roadmap for the upcoming changes and to note down which parts of the code will be affected by our changes. Therefore, after iterating for a few weeks over my drafted proposal, it was accepted, and I started the implementation.

### :point_right: What were the technical learnings?
The project required a deep understanding of Go, gRPC, TLS and how it works and to be honest, I didn't know much about TLS before drafting a proposal for GSoC. Still, gradually after reading about it on the internet, I found it exciting and prepared a detailed proposal. I learned about TLS, mutual TLS, TLS handshake, TLS certificate rotation, and a bit about Kubernetes cert-manager. Want to know about them? Head over to this [blog](../202108-tls-in-brief) post which summarises my learnings. 

### :point_right: Challenges I faced?
So basically, we can split the whole GSoC journey into three parts a) Proposal period, b) coding period, and c) Testing period.
#### a) Proposal period
Finalizing and having a consensus over a proposal was challenging for me as we have to think from the users’ and the developer’s perspectives. This part requires a lot of understanding of the current implementation and working of various Thanos components. In this period, I spent a lot of time reading the Thanos code and about TLS.

#### b) Coding period
As we already had a solid proposal to work upon, I faced only some minor challenges in this period. I learned about YAML and how to use it with GoLang.

#### c) Testing period
Testing the code you have written is not that tough because you know the entire internal execution. But when it fails, it’s hard (sometimes) to debug and find out whether the problem is in the test code or the main code. The same happened to me as I was configuring mutual TLS in Thanos querier for both client-side and server-side (unknowingly and which is possible), which was wrong as for the server-side, it was needed to enable TLS on the Thanos sidecar. In this process, I doubted the actual implementation of the mutual TLS feature and the TLS certificates created for the testing purpose. Eventually, it was solved with the help of mentors but consumed a lot of my time.

### :point_right: Key takeaways.
- A decent proposal is a must if you are implementing a significant feature as it provides a structured path to move on and a good amount of surety that your changes would not be revoked.
- Don’t panic if you are not sure of the code you have written, instead open a pull request, wait for the reviews and iterate over them to make your changes perfect to be merged.
- Any problem which seems hard at first seems too easy once solved, so search for the solution but again, don’t panic.
- We should never compromise with our health.

### :point_right: Overall experience.
The overall mentorship experience was incredible. I got this GSoC mentorship opportunity in the summer break of my second year of university. In this mentorship program I was able to overcome my fear of contributing to large codebases and now I’m more confident in working with Go, gRPC, TLS,  distributed systems and microservices.  The weekly interactions with the mentors helped to accomplish all the milestones set for this mentorship period, entirely.

### :point_right: Curious to see the work done?
- [Revised proposal](https://github.com/thanos-io/thanos/pull/4377)
- Implementation part 1: [Per-endpoint TLS configuration feature](https://github.com/thanos-io/thanos/pull/4389)
- Implementation part 2: [Automatic certificate rotation feature](https://github.com/thanos-io/thanos/pull/4493) 
- Virtual talk: [TLS in brief-Recording](https://www.youtube.com/watch?v=s9L0XukF6jQ&t=3856s)

### :point_right: Shout out to the wonderful mentors.
:star: [Bartek Plotka](https://www.linkedin.com/in/bwplotka/): He is a Principal Software Engineer at Red Hat; (London, United Kingdom)\
:star: [Kemal Akkoyun](https://www.linkedin.com/in/kakkoyun/): He is a Senior Software Engineer at Polar Signals; (Berlin, Germany)

\
Until next time...
