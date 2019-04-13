---
layout: post
title: An Atlas for Learning React
subtitle: "Something like a mind map, because learning something like React is complicated."
categories: ["How Things Work", "React"]
description: "A guide to learning the concepts and ecosystem of react (a somewhat popular javascript library)"
comments: true
---

Learning something like [React](https://reactjs.org/) takes time. For every excellent react resource that exists on the internet, there are several poorly written tutorials showing you how to make a todo list app. This 'atlas' serves as a guide for myself and others. 
It will probably be updated over time.
Information found in the glossary of terms is largely indebted to the various resources mentioned here. 

## Conceptual Overviews

* [The official React guide to main concepts](https://reactjs.org/docs/hello-world.html)
* [React as a UI Runtime](https://overreacted.io/react-as-a-ui-runtime/) (Learning react from first principles)

## Tools

* [Create React App](https://facebook.github.io/create-react-app/), A CLI and set of sensible defaults for react projects
* [React devtools](https://github.com/facebook/react-devtools), Chrome and Firefox extension fo view react stuff along with dev tools

## Ecosystem

* [Next.js](https://nextjs.org/), Server-side rendering
* [Redux](https://redux.js.org/)

## Tutorials

* [Official React Tutorial](https://reactjs.org/tutorial/tutorial.html)
* [The Road to React with Firebase](https://roadtoreact.com/course-details?courseId=THE_ROAD_TO_REACT_WITH_FIREBASE)

## People

* [Jordan Walke](https://twitter.com/jordwalke), creator of React
* [Dan Abramov](https://overreacted.io/), creator of Redux and Create React App

## Glossary of Terms

### Elements
React *elements* are plain javascript objects that represent something that react will render in the DOM.

* Treated as immutable by react
* Can reference valid DOM tags or user-created components

### Components
React *components* functions or instances of classes that receive props and return elements.

* Can be as simple as a js function that receives an object and returns and element
* Can also be a class that extends `React.component`
* Components start with an uppercase char
* Must not mutate props

#### State
*State* is essentially a property on component classes that is accessible at `this.state`.

* Only mutate state using `setState`
* `setState` is asynchronous
* `setState` merges properties shallowly
* state is local to a given component and uses a top-down data flow

#### Mounting

* *Mouting* is when an element is rendered to the DOM for the first time
* *Unmounting* is when an element is removed from the DOM

#### Lifecycle Methods

* `componentDidMount`
* `componentWillUnmount`

---

Did you come across some excellent resources when learning React? Did you have a turning point where react suddenly 'made sense' to you? Let me know in the comments.
