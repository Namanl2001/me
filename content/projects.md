---
title: Projects
date: 2021-08-19
---
The open-source projects I have sufficiently contributed to so far are included in this section, along with a concise overview of my work within these projects.

### :point_right: kubernetes/kubernetes
[Kubernetes](https://github.com/kubernetes/kubernetes) doesn't need an introduction, right? During my internship at VMware, I was privileged to work on the upstream kubernetes full-time. There are three domains I worked at:

- Component maintaince - I worked on this contextual logging [issue](https://github.com/kubernetes/enhancements/issues/3077), which required labour across several Kubernetes components, I successfully migrated 7 of them to a more secure and efficient contextual logging system.
- Release Team member - I did non-code contributions during this phase, I was a CI-Signal RT shadow for the k8s v1.26 release. You may read about my adventure in this [blog](/posts/202212-k8s-rt-shadow-experience).
- [Cluster API](https://github.com/kubernetes-sigs/cluster-api) (CAPI) - I picked an issue to implement dockerless CAPD feature, everything related can be found in this [GH comment](https://github.com/kubernetes-sigs/cluster-api/issues/5836#issuecomment-1229552695). My [commits](https://github.com/kubernetes-sigs/cluster-api/compare/main...Namanl2001:cluster-api:dockerless-capd).
### :point_right: Kyverno
[kyverno](https://github.com/kyverno/kyverno) is a kubernetes native policy management tool. It is built and maintained by Nirmata. During my internship at Nirmata, I had the opportunity to work on this fun project.

Since kyverno is a young CNCF project I've had the chance to work on a variety of areas starting from software supply chain security (very hot topic today!), to refactoring the GitHub actions workflow, to [designing](https://github.com/kyverno/KDP/blob/main/proposals/yaml_signing_and_verification.md) and prototyping of k8s-manifest signing/verification feature and much more! All of my contributions can be seen [here](https://github.com/kyverno/kyverno/pulls?q=is%3Apr+author%3ANamanl2001).
### :point_right: kubernetes/test-infra
[kubernetes/test-infra](https://github.com/kubernetes/test-infra) is the test infrastructure for the Kubernetes project. I was aware of the K8s project, but the LFX mentorship programme gave me the opportunity to start making contributions. My project was to migrate the SIG-node related CI jobs from kubetest to kubetest2.

During the course of my mentorship I was successful in migrating all the pre-submit jobs to kubetest2, which were all up and running, after the continuous efforts from myself and my mentors. All of my contributions can be seen [here](https://github.com/kubernetes/test-infra/pulls?q=is%3Apr+author%3ANamanl2001). Interested to know more? (blog coming)

### :point_right: Thanos
[Thanos](https://github.com/thanos-io/thanos) is a highly available Prometheus setup with long term storage capabilities. A CNCF Incubating project. I started my open-source journey with Thanos, contributed to the frontend since I knew ReactJs, and gradually shifted to the GoLang backend.

My Google summer of code project was to implement per-endpoint TLS configuration in Thanos querier. All of my contributions to Thanos can be seen [here](https://github.com/thanos-io/thanos/pulls?q=is%3Apr+author%3ANamanl2001). Interested to know my whole GSoC journey? Head over to this [blog](/posts/202108-google-summer-of-code-2021).