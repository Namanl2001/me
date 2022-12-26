---
author: <a href="https://www.linkedin.com/in/naman2001/"> Naman Lakhwani</a>
categories:
- Kubernetes
- Release team shadow
- Open Source
- CNCF
comments: true
date: "2022-12-26T00:00:00Z"
published: true
title: Experience with K8s v1.26 RT shadow role
---

Kubernetes 1.26 just got released :tada:, yay! I am fortunate to get a chance to work with the fantastic folks in the Kubernetes community! In this blog, I will share my experience as the CI Signal Shadow, helping with the Electrifying K8s 1.26 release :muscle:

&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ![can't access image](../images/kubernetes-1.26.png)

### :point_right: What is the the Release Team (RT) shadow program?

Kubernetes has grown exponentially in the last few years and has seen adoption by countless companies. But at the end of the day, it is still an open-source project being maintained by the community! For each new Kubernetes release, a team of community members is assembled and responsible for the day-to-day work which goes into successfully releasing the next version of Kubernetes. This is the Kubernetes Release Team.

The release team is further divided into various sub-teams to ensure the smooth functioning of all horizontals. Each release has a Release Lead, and 3-4 Release Lead Shadows help them. The same applies for each subteam (eg, CI Signal): there is the subteam lead, accompanied by 4-5 shadows. We start in the release team as one of the subteam’s shadows and can eventually grow our way up to the Release Lead!

Seven subteams take shadows: Bug Triage, CI Signal, Communications, Documentation, Enhancements, Lead, and Release Notes.

![can't access image](../images/rt-assemble.webp)

### :point_right: Application process for the RT shadow role.

A few weeks before each release cycle begins, an application form is floated to apply to be on the release team. You can receive notifications for this if you join the Kubernetes dev [mailing list](https://groups.google.com/a/kubernetes.io/g/dev).

> You can find the current 1.27 Release team application form [here](https://docs.google.com/forms/d/e/1FAIpQLSdpZy9HA7T2RQaVZGGQ759LN_OV6fvRQDYA_hekOD1GdZptPw/viewform). Open until 3rd January, 2023.

The application form does a pretty good job explaining what is expected in your responses so I won’t get into that. But I do want to point out something which I’ve seen discourages many people. It is okay not to be selected the first time, and you should keep applying again if you’re interested! The release team receives several applications each cycle for its limited number of roles.

I, too, got accepted in my third application. I know how it feels to get the rejection email in the inbox but not getting selected isn’t a reflection of your skills! Don’t lose faith if you don’t get accepted the first few times you apply. Prior contributions to the project and correctly researching the role help your application significantly!

Massive shoutout to [Nabarun Pal](https://www.linkedin.com/in/palnabarun/) for reviewing my answers for the application.

### :point_right: How does the onboarding process look like?

We had an onboarding session with [Nivedita](https://www.linkedin.com/in/nivedita-prasad-706719194/), the CI-Signal lead for release 1.26. We met other CI-Signal shadows and discussed how we would collaborate going forward. 

The weekly RT meetings were decided to happen in two time zones (APAC and EMEA), one on Wednesday and another on Friday. So we divided our work day-wise, like who will monitor the testgrid dashboard on respective days and who will give weekly updates in the meetings. Accordingly, we showed up in the meetings to give the update; however, the RT meetings are open to all!

### :point_right: What is the actual job of a CI-Signal RT shadow?

Our job was to monitor the testgrid (these two tabs: [sig-release-master-blocking](https://testgrid.k8s.io/sig-release-master-blocking) and [sig-release-master-informing](https://testgrid.k8s.io/sig-release-master-informing)), look at the failing/flaky jobs, try to debug the cause of a particular failure, open a tracking issue and inform the respective SIGs. Sounds simple right? but sometimes, it gets tricky!

Accordingly, we had to give the [Go or No-Go](https://github.com/kubernetes/sig-release/blob/master/release-team/role-handbooks/ci-signal/README.md#release-cutting---go-or-no-go) signal before each release cut. We also had to give updates at weekly meetings and send an email to the mailing list. I, fortunately, got a chance to give updates in 5 meetings.

### :point_right: Conclusion

I got featured on the beautiful stage of KubeCon NA 2022, along with the 1.26 Release Team :)

![can't access image](../images/kubecon-stage.jpg)

Being a first-time member of the Release Team was an amazing experience.
I met a lot of industry leaders who are actively involved in the Kubernetes community, my visibility in the community also rose during this program. Getting accepted on my third attempt made this experience special, “nothing great comes that easy.”

I would highly recommend this shadow program to everyone reading this blog and who is interested in starting with open source since this program doesn’t require much pre-requisite knowledge; everything could be learned along the way. But getting into this program can be a difficult task. All the best :thumbsup:

\
Until next time...:wave: