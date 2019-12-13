---
title: "Healthy Codebase Habit: Regular Dependency Updates"
subtitle: ""
layout: post
categories: ["Practices"]
description: "Keep your team, project, and personal development healthy by updating your codebase's dependencies at a regular interval."
comments: true
---
Do you have a habit of updating your team's dependencies? Congratulations, you've got **fresh** dependencies.

Do you lack a habit of upgrading your projects dependencies? Oh man, you're dependencies are probably **stale**.

I've learned that it's better in almost every way to regularly update your dependencies. Read on for more.

## Stale Dependencies

*Stale dependencies lead to suffering.*

### This is your team on stale dependencies

Everyone can guess what happens when you don't keep your dependencies up to date on a project. Dependencies get out of date, then become harder and harder to upgrade. This is true, but there are actually deeper, darker problems to projects with stale dependencies.

The first couple of projects that I worked on as a software developer did not value regular dependency updates. They were java projects in a large-ish IT organization. The progression went something like this:

*First, an approved version of a large framework was picked.* This was usually at least the n - 1 version. From here the project began and dependencies would begin to accumulate. There was very little discussion over the fact that as time passed the project dependencies would become more and more out date, but this was the case.

*Next, a developer faced a problem and wished to solve it*. A developer faces a problem and realizes that one of the project's dependencies could easily solve the problem. They go to upgrade a dependency to use it's new feature and spend a few days in dependency resolution [sheol](https://en.wikipedia.org/wiki/Sheol) until they give up.

*Then, the team accumulates an identity that is disconnected from its technology community.* The team is stuck on old technology so why read about what is up and coming? Why contribute back to the open source community? Why spend time thinking about ways we can improve and new patterns we can adopt?

*Finally, much toil is had and the cycle repeats.*  Silly workarounds solve problems rather than new patterns available latest dependencies. One broken window turns into 50. Eventually a new project needs to be funded to bring the app into a usable state again.

All in all, stale dependencies cut a team off from its community and the valuable feedback loops contained therein. They incur large costs down the line and make daily life on a software development team less enjoyable.

### Some problems with stale dependencies

* Major frameworks lock you into a specific version
* Difficulties resolving dependencies that have desired features
* Team becomes a disconnected user of the dependencies they use
	* unable to contribute back to the community
	* unable to take advantage
* Cost of modifying product becomes so high, a new project must be funded to upgrade the app once it becomes a security concern or liability
* All of these negative side effects increase cost in sundry ways

## Fresh dependencies

*Fresh dependencies breed new feedback loops*.

### This is your team on fresh dependencies

If you haven't worked on a project that prioritized fresh dependencies, you may not be aware of the advantages that spring up. I myself was surprised.

After spending a while on Java projects with stale dependencies, I joined a team in Javascriptland. In Javascriptland, 'new' things were happening so often that the team's evergreen app would become unworkable from an engineering point of view if they didn't regularly keep dependencies fresh. When I first joined the team I was surprised at how much the codebase was constantly improve. I eventually identified *fresh dependencies* as a core practice that enabled these feedback loops.

*Dependency updates signal the misuse of frameworks, libraries, and APIs as breaking changes were encountered.* Dependency maintainers regularly find ways that the APIs of their projects are miused or underused. To counter this, they make deprecations and modify the way the dependency should be consumed. Watching these changes happen makes a team aware of things maintainers are doing to improve their product. Often, seeing this happen is infectious and spurs the improvement of internal APIs or even the overall adoption of say functional programming principles over the imperative. Immutability can be contagious.

*Constantly improving lint rule sets help developers improve their codebases.*  If you work in Javascriptland you should definitely be taking advantage of establish lint rulesets like the famous [Airbnb](https://github.com/airbnb/javascript) repo. Upgrading these rulesets along with your dependencies will often introduce new rules that break your build. Taking time to explore why these rules were introduced and how you can follow them will lead you down new avenues of improving your codebase and programming practices. As the community learns, you learn.

*Updating your language/runtime helps you to take advantage of new language features.* Typescript is a great example of this. With typescript, if your regularly update to the latest stable version and read the blog post they produce explaining new features, you are incrementally learning about what will become part of the javascript spec in the next 12 months. Your codebase is able to take advantage of these features right away and you are using them as soon as they come out.

*Proactively upgrading dependencies preemptively removes potential blockers.* Rather than finding out you can't use some feature that you need or that you will have to migrate a bunch of old code to maintain platform support, you will be ahead of the curve on the platforms, frameworks and libs that you use. No more worrying about running out of time to upgrade before something breaks in production.

### Some advantages to fresh dependencies.

* Dependency updates signal the misuse of frameworks, libraries, and APIs as breaking changes were encountered
* Constantly improving lint rule sets help developers improve their codebases
* Updating your language/runtime helps you to take advantage of new language features
* Proactively upgrading dependencies preemptively removes potential blockers

## In Sum

Keep your team, project, and personal development healthy by updating your codebase's dependencies at a regular interval. Like our health or our relationships, doing good things often yields unpredictable benefits, while neglecting them will create emergency situations and make you feel like a lame human being.

---

Please share in the comments: advantages you have seen from keeping dependencies up to date, or stale dependency horror stories you've lived through.
