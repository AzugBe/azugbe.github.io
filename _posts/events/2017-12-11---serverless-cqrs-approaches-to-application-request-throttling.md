---
layout: single
title: "2017-12-11 - Serverless CQRS & Approaches to application request throttling"
date: 2017-12-11 13:37:00 +0000
comments: true
published: true
categories: ["events"]
tags: ["Events"]
alias: ["/events/2017-12-11---serverless-cqrs-approaches-to-application-request-throttling"]
author: Tom Kerkhove
redirect_from:
 - /events/2017-12-11---serverless-cqrs-approaches-to-application-request-throttling.html
---

Serverless is one of the biggest buzzwords at the moment, so here's an event on serverless! But be warned, you need to protect your systems as well. Join us to learn about using serverless CQRS with Toon Vanhoutte and how you can add application request throttling with Maarten Balliauw.

## Sessions
### Serverless CQRS in Azure!
The CQRS pattern enables you to build highly scalable, distributed and event-driven applications. Microsoft Azure contains all the serverless building blocks you need to take advantage of the CQRS pattern. In this session, we're going to transform a monolithic web app into a modern cloud application, that easily handles peak loads and offers great flexibility. Expect architectural guidance, cost-effective designs and live demo's.

<img src="/assets/media/speakers/toon-vanhoutte.jpg" alt="Toon Vanhoutte" align="left" height="100" style="margin-right: 20px;">**Speaker:** *Toon Vanhoutte is Lead Architect at Codit Belgium and Microsoft Azure MVP. His duty is to design and deliver reliable, secure and scalable integration / backend solutions, both on-premises and in the Azure cloud. His focus is on integration, API Management, IoT and Azure solutions, in line with the Codit strategy.  As a solution architect, he's not scared to take up big challenges and to dive into a development mode. He's a quite active member of the Microsoft integration community and was speaker on several community and company events. Being a Microsoft Certified Trainer, he loves to share his experiences in workshops, presentations and blogs. As an Azure Advisor, he's actively collaborating with various Azure product teams.*


### Approaches to application request throttling
Speaking from experience building MyGet.org: users are insane. If you are lucky, they use your service, but in reality, they probably abuse. Crazy usage patterns resulting in more requests than expected, request bursts when users come back to the office after the weekend, and more! These all pose a potential threat to the health of our web application and may impact other users or the service as a whole. Ideally, we can apply some filtering at the front door: limit the number of requests over a given timespan, limiting bandwidth, ...

In this talk, we’ll explore the simple yet complex realm of rate limiting. We’ll go over how to decide on which resources to limit, what the limits should be and where to enforce these limits – in our app, on the server, using a reverse proxy like Nginx or even an external service like CloudFlare or Azure API management. The takeaway? Know when and where to enforce rate limits so you can have both a happy application as well as happy customers.


<img src="/assets/media/speakers/maarten-200x200.jpg" alt="Maarten Balliauw" align="left" height="100" style="margin-right: 20px;">**Speaker:** *Maarten Balliauw loves building web and cloud apps. His main interests are in ASP.NET MVC, C#, Microsoft Azure, PHP and application performance. He co-founded MyGet and is Developer Advocate at JetBrains. He’s an ASP Insider and MVP for Microsoft Azure. Maarten is a frequent speaker at various national and international events and organizes Azure User Group events in Belgium. In his free time, he brews his own beer. Maarten’s blog can be found at [http://blog.maartenballiauw.be](http://blog.maartenballiauw.be).*

## Practical details

**Event date:** December 12, 2017 - you are welcome from 18:00, session starts 18:30

**Event location:**<br />
To be determined - Interested to host this event? [Contact us](http://www.azug.be/contact)!

## Register via EventBrite
Coming soon.