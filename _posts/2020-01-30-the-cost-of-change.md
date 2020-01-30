---
title: "Flatten the Cost of Change Curve, you must."
subtitle: "A key success factor of software development teams."
layout: post
categories: ["Practices"]
description: "A healthy codebase is inexpensive to change."
comments: true
---

In software development, there is a key success factor that often goes unnamed. It lies below many debates that software teams have and is at the root of many failure and success stories. Kent Beck aptly described this factor in the early chapters of the first edition of his *Extreme Programming Explained* book. In my experience developers and managers are unlikely to have read this book so I'm here doing my best to accurately convey them. This thinking is not original to me.

---

First, let me attempt to express the essence of the idea:

*A software system's cost of change is inversely proportional to its potential ongoing economic advantage.*

In argument form, it might look like this:

1. Software is highly malleable medium
2. Software's ability to change is a primary competitive advantage
3. Therefore, consistently low cost of change is essential to maximizing its intrinsic benefits

Let's take a look at each point of the argument.

## Software is a highly malleable medium

Software has induced a revolution into our world that is on the order of the printing press. We now interface with all the domains of our lives with the help of software. Nearly everything we create and consume is aided or mediated by software.

Why?

Software itself is highly malleable which allows its output to likewise be very pliable.

There are many angles to this (sociological, economic, cultural, etc...) but it seems to me that a key factor is how easy it can be to change software and thus modify its output. Costs associated with changing software (including time) different from other media by orders of magnitude.

## Software's ability to change is a primary competitive advantage

Software has taken the world by storm precisely because it can be so malleable at such a low cost.

Double-entry accounting done on paper includes an enormous amount of work if something changes once calculations are made. With software, the change is easy and thus the recalculations are automatic. 

Yes, submitting information digitally rather than physically reduces errors (by validating input) and slashes delivery costs, but at the end of the day the value of a digital submission process is in how easy it is to change. Adding a new validation rule, requiring a different type of information or adding a review process is relatively inexpensive to implement once a system is up and running.

Publishing is another industry revolutionized by software. Just think about the difference between publishing updates to an ebook compared to printing the second edition of a physical book.


## Therefore, consistently low cost of change is essential to maximizing its intrinsic benefits

So, how is this discussion relevant to an individual software developer or a software team?

**To achieve these economic advantages, software must *remain* inexpensive to change.**

We all know that possible the most common problem to crop up in software teams is that as a codebase or system ages and gains more functionality, it can become very difficult to change. This can be magnified by having a multiplicity of contributors spanning cultures and continents. As functions get longer, if statements are added, comments become stale, and files get huge, a system loses the economic benefits that made it profitable in the first place.

In light of this, software teams must focus on keeping their products' cost of change consistently low.

There is an ever growing pool of tools and methods to achieve this. Test-driven development, automated checks, automatic code styling, lint rules, CI jobs, and code review processes are among some of the most prominent.

If a software team fails to keep the cost of change low ("not enough time!", "I can do that later", "We don't really need that yet") they are really just biding their time until the next expensive rewrite.

#### If a team cannot exercise discipline to manage the cost of change, as a wise man once said, ["then the Emperor has already won"](https://getyarn.io/yarn-clip/609961ff-f41a-4056-8368-f87e438c3eb1#/OT5Cc0Nu3m).
