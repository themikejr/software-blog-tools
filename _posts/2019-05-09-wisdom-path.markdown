---
title: The Software Developer's Path to Wisdom
subtitle: "A Model of Ideological Adoption"
layout: post
categories: ["Practices"]
description: "A description of the stages one undergoes when adopting a proposition."
comments: true
---
Have you ever worked with someone who was seemed able to know the right thing to do in almost all situations? This person wasn't only very good at solving technical problems but knew how to handle people, systems, and situations too. This was a person that possesed _wisdom_. In this blog post I will set out to define wisdom and then present the way that I think about how someone becomes wise in a given domain.

## Wisdom?
What is wisdom? There are many alternative defitions that you will encounter. First, let's begin with what it isn't:

What wisdom is not:

* Experience
* Old age
* Intellectual prowess
* Common sense

Any of the above factors may correlate to a wise person, but wisdom itself is something more. My definition:

> _Wisdom_ is the ability to understand reality and act accordingly. 
 
Knowledge, experience, and emotional intelligence are all crucial to being able to apply wisdom, but on the whole wisdom comes across as that someone develops over time.

## The Model (Brinker's Model of Ideological Adoption?)

As I have thought about the acquisition of wisdom in my life and reflected on various environments in which I have sought it, I began to see a pattern. I noticed that whenever someone is presented with something new (an idea, tool, method, or system) there are stages of adoption which the person undergoes as they try that new thing out. For the sake of example, we'll just call the thing in question "the new thing". Here is what I'm calling the stages for now:

1. Ignorance
2. Awareness
3. Zeal
4. Wisdom

### Ignorance

The first stage, **ignorance**, is when you are blissfully unaware of _the new thing_. You haven't heard of it. You may have experienced the problem that the new things solves but that's about it.

### Awareness

The second stage, **awareness**, is when you become aware of _the new thing_, but for whatever reason don't attempt to apply it. Maybe you think it won't be useful, or maybe you think it will be useful but that you don't have time to try it out. Finally, you may be aware of _the new thing_ but don't fully understand it.

### Zeal

The third stage, **zeal**, is a dangerous one. It could fairly be called the 'cage stage' because you should be locked in a cage until you are through it. In this stage you understand _the new thing_ to a degree and seek to apply it to every thing and every one, often yielding unfortunate results. You haven't yet learned when _the new thing_ isn't applicable, so you are an evangelist for it, blind to any situation where it isn't useful and self-wise regarding its application. You know you are in this stage when you annoy friends/family/colleagues by blathering on and on about the glory of _the new thing_.

### Wisdom

The fourth stage, **wisdom**, is the stage you want to be in. In this stage, the shininess has worn off a bit, and you are on a journey of knowing when not to use _the new thing_. This stage asymptotically approaches perfection. You know you are getting here when you can find some aspect of _the new thing_ that you disagree with or could be a problem in some contexts. After the cage stage, this is where you become sane and tolerable regarding _the new thing_.

## Wisdom in Software Development

I have seen myself move through these stages at a macro level with regards to software development (and many other things) and also at a micro-level with certain tools, methods, and technologies. For a case study, let's take a look at the way I adopted Test-Driven Development.

## A Case Study: Test-Driven Development

### Ignorance

In college I had a programming class or two. No one ever mentioned TDD. I had no idea what it was. I did notice that the one programming project I had seemed to break often as I was changing it.

### Awareness

In my first programming job I joined a team that lived and taught TDD. As soon as I began pairing with my team members I was introduced to the concept. It seemed like it might be helpful, but writing a program that tests the program which I'm writing felt very odd to think about. I always began coding a new feature and then heard one of my coworkers say "did you write a test for that?". As I learned how to write tests and was introduced to mocks, stubs, and spies, I became proficient but still didn't consistently write tests first.

### Zeal

On my first software project as a full-fledged junior, I engaged in TDD with much zeal. 

Was I about to define a class? Write a test first.    
Extracting something into a private method? Write a test first.     

Not only did I behave this way myself but I demanded that the team maintain a near 100% coverage rate.

The result?

The tests were brittle. The slightest refactor caused a lot of rework in the tests. We went to great lengths to test our getters and setters. Some teammates found me annoying.


### Wisdom

I eventually realized that some of my tests provided no value. Testing getters and setters didn't buy us much. And writing a test before defining a class? That was the essence of an overzealous junior developer. I scaled back a bit and focused on writing tests that the project _needed_. Eventually I was even able to grok the difference between London and Detroit style TDD and understand where I fit in the scheme of things. At this point people could bear to hear me talk about TDD again. I was even able to mentor and help a few people figure it out along the way. I'm not a zen master by any means, but the benefits that TDD provides as a tool are clear to me and I also understand when it isn't that helpful. Now I remain on the long road of wisdom.

## In Sum

Hopefully you see some concordance with reality in this model. It's been a helpful tool for me to understand people and team dynamics in some cases.

---
Was this helpful in any way? Did I miss a step? Do you have a better name for this thing? Let me know in the comments.