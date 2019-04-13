---
title: A Software Engineering Manifesto
subtitle: "Not because my opinions won't evolve on these topics, but because it's good to see where one stands."
layout: post
categories: ["Practices"]
description: "A snapshot of my best practices and preferences related to software engineering/development."
comments: true
---
Disclaimer: "Best practices" are less like objective truths and more like pragmatic successes in the software engineering field. This is not to say that the correct way or even _best_ way of doing something doesn't exist, but rather given our finiteness and the external forces of the worlds we inhabit, one should expect some variability here. While I state these in the indicative sense ("X shall be Y") at the end of the day, the best way to write and ship software will differ from context to context and will (hopefully!) look different in coming years.

## Deployments Shall Be
- Automated
- Scheduled
- Repeatable
- Often
- While the system is in use

## Databases Shall Be
- Migrated automatically during deployments
- Locally accessible for developers
- Optimized just in time

## Code Shall Be
- Version controlled
- Style-enforced at build time by automated tooling
- As simple as could possibly work
- Nearly comment free
- Deleted if unused
- Test-driven
- Treated as a liability
- Paired on as needed
- Deleted with joy

## Project Management Shall Be
- Pull-based
- Optimized for end-results, not implementation details

## Developers Shall be
- Courageous to simplify the system in almost all circumstances
- Teliocentric in their efforts
- Mildly over-affectionate towards their text editors
- Allowed to work uninterrupted for generous amounts of time

## System Design Shall Be
- Evolving as necessary with every feature
- Changing as the team’s understanding of the problem domain changes
- Ultimately enforced at code review time
- Consistent whenever possible
- Delegated to widely-used open source implementations when possible

---
Did I miss something? Was I completely wrong in some way? Was there something I got right? Let me know in the comments.