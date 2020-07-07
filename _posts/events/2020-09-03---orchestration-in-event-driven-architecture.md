---
layout: single
title: "2020-09-03 - Orchestration in Event Driven architecture"
date: 2020-09-03 17:00:00 +0000
comments: true
published: true
categories: ["events"]
tags: ["Events"]
author: Maarten Balliauw
---

Service Bus, Event Hub and Event Grid - all can be used in Event Driven Architecture. Let's look at the fundamentals
underpinning Event Driven architecture, and which patterns can be used on Azure!

## Agenda

### Orchestration in Event Driven architecture

Event Driven architecture (EDA) becomes more and more popular and Azure comes with many services which you can use in
your solutions design to build EDA. However, choosing between Service Bus, Event Hub and Event Grid is not always easy.
On top of that, while you want to leverage parallelism, elasticity and all the goodness of the Cloud, you usually need
to reconciliate all the operations at the end of the day, and that is called orchestration.

In this session, I'll come back to the fundamental differences between ESB-like architectures and EDA and I'll demo
different orchestration patterns one can use to build resilient and robust EDA, mostly using Azure Durable Functions.
As usual, the session is inspired from real-world applications!

<img src="/assets/media/speakers/stephane-eyskens.jpg" alt="Stephane Eyskens" align="left" height="100" style="margin-right: 20px;">**Speaker:** **Stephane Eyskens** is a Cloud Architect and Digital Transformation advocate, blogger, author and speaker.
He has a particular interest for Hybrid Architectures, Modern Authentication & Security in general as well as Artificial Intelligence.
He is a DevSecOps practitioner, always trying to have a Lean approach while understanding what Service and Application Management are all about.

Stephane on Twitter: [@stephaneeyskens](https://twitter.com/stephaneeyskens)

## Practical details

**Event date:** September 03, 2020 - you are welcome to [<img src="/assets/media/icon-slack.png" width="16" height="16" /> hang out in our Slack team](https://join.slack.com/t/azugbe/shared_invite/MjE4MzI5NDM3OTM5LTE1MDExNDgyMzUtMzgwNjM2YmU0Zg) or on the YouTube Live chat from 16:30, sessions start at 17:00

**Event location:**<br />
Online at [www.azug.be/live](https://www.azug.be/live), details will be e-mailed closer to the event.

## Register via Pretix
<link rel="stylesheet" type="text/css" href="https://pretix.eu/azug/20200903/widget/v1.css">
<script type="text/javascript" src="https://pretix.eu/widget/v1.en.js" async></script>
<pretix-widget event="https://pretix.eu/azug/20200903/"></pretix-widget>
<noscript>
   <div class="pretix-widget">
        <div class="pretix-widget-info-message">
            JavaScript is disabled in your browser. To access our ticket shop without JavaScript, please <a target="_blank" rel="noopener" href="https://pretix.eu/azug/20200903/">click here</a>.
        </div>
    </div>
</noscript>