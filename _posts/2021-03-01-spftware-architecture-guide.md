---
layout: post
title:  "Software Architecture Guide"
date:   2021-03-01 17:26:45 +0300
categories: architecture
---
## What is architecture?
People in the software world have long argued about a definition of architecture. For some it's something like the fundamental organization of a system, or the way the highest level components are wired together. My thinking on this was shaped by an email exchange with Ralph Johnson, who questioned this phrasing, arguing that there was no objective way to define what was fundamental, or high level and that a better view of architecture was the shared understanding that the expert developers have of the system design.

## Why does architecture matter?
Architecture is a tricky subject for the customers and users of software products - as it isn't something they immediately perceive. But a poor architecture is a major contributor to the growth of cruft - elements of the software that impede the ability of developers to understand the software. Software that contains a lot of cruft is much harder to modify, leading to features that arrive more slowly and with more defects.

## Application Architecture
The important decisions in software development vary with the scale of the context that we're thinking about. A common scale is that of an application, hence "application architecture".

The first problem with defining application architecture is that there's no clear definition of what an application is. My view is that applications are a social construction:

A body of code that's seen by developers as a single unit
A group of functionality that business customers see as a single unit
An initiative that those with the money see as a single budget
Such a loose definition leads to many potential sizes of an application, varying from a few to a few hundred people on the development team. (You'll notice I look at size as the amount of people involved, which I feel is the most useful way of measuring such things.) The key difference between this and enterprise architecture is that there is a significant degree of unified purpose around the social construction.

## Enterprise Architecture
While application architecture concentrates on the architecture within some form of notional application boundary, enterprise architecture looks architecture across a large enterprise. Such an organization is usually too large to group all its software in any kind of cohesive grouping, thus requiring coordination across teams with many codebases, that have developed in isolation from each other, with funding and users that operate independently of each other.

Much of enterprise architecture is about understanding what is worth the costs of central coordination, and what form that coordination should take. At one extreme is a central architecture group that must approve all architectural decision for every software system in the enterprise. Such groups slow down decision making and cannot truly understand the issues across such a wide portfolio of systems, leading to poor decision-making. But the other extreme is no coordination at all, leading to teams duplicating effort, inability for different system to inter-operate, and a lack of skills development and cross-learning between teams.

Like most people with an agile mindset, I prefer to err on the side of decentralization, so will head closer to the rocks of chaos rather than suffocating control. But being on that side of the channel still means we have to avoid the rocks, and a way to maximize local decision making in a way that minimizes the real costs involved.

