---
layout: post
title: "Refactoring Doesn't Require Domain Knowledge"
subtitle: The code never lies
categories: ["What I've Been Reading"]
comments: true
---

I came across this great [GeePaw Hill](https://twitter.com/GeePawHill) [thread](https://twitter.com/GeePawHill/status/1099733643734470656) on twitter about refactoring and domain knowledge. The final tweet in the thread sums it up well:

> When I'm refactoring, I do my best work when I am entirely domain-blind, and am working with and thinking of all and only what the code that is actually there actually does. Prioritize reading code over studying the application domain.
>
> Have a pleasantly odd Sunday!

Over the years I have learned to trust the fact that _the code never lies_. In addition to possibly saying some interesting things about epistemology, this aphorism has proven trustful to me time and time again. While devs (and others) ~~argue~~ discuss what some code does, how it's working, etc... in almost every case the wise thing to do is say very little and begin reading the code. 

There are lessons in this thread about the value of readable code as well. In the thread, there seems to be a correlation between the refactoring effort (making the code easier to understand) and the discovery of the performance problem. The easier code is to read, the easier it is to reason about, which enables developers to make improvements to it, or at very least decreases their chance of screwing it up as they change it. An explanation of the _value_ of clean (read: readable) code is worthy of its own post.

Alas! The whole thread is a great read. [Read it unrolled](https://threadreaderapp.com/thread/1099733643734470656.html) on ThreadReader.
