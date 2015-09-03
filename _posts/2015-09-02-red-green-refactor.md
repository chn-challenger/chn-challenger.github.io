---
layout: post
title: Red -> Green -> Refactor by Joe Zhou and Michael Roger 
---

In short, red-green-refactor (RGR from this point on) is a mini TDD (test driven development) cycle.  The basic steps are:

* Red:  Make a failing unit test to test a small feature.
* Green:  Write minimal amount of code to make the test pass.
* Refactor:  Make the code readable, efficient and general with a view to scalability.

![](http://i.imgur.com/Y3LxecJ.png)
_Repeat this cycle for each small unit of features or user requirements._

Why refactor, why not get it right the first time?
Separation of writing code to pass the test then refactoring afterwards, allows us to first focus on solutions then tidy up, rather than attempting both at once which would add to the complexity.
Refactoring is an important stage in the process and should not be considered optional.

The benefits of RGR can include: 

* Efficient error management.
* Allows us to build more robust, scalable and maintainable software.
* Breaks down larger projects into more manageable chunks.
* When bugs occur they're easier to locate and rectify.
