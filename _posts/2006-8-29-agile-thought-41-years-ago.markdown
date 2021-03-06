--- 
title: Agile thought 41 years ago
layout: post
author: Brian
---
Recently, [Robby](http://www.robbyonrails.com) dropped off his copy of _The New Utopians_ by Robert Boguslaw at my desk with a section marked: "For Whom and For What". Here are a couple interesting quotes on page 45:

> This, then, is one of the fundamental problems of application: on the one hand, the temptation is almost overpowering to establish the techniques and practices of practitioners as handbook truths available in situations of the sort we have termed established. It is the temptation to speak with the same degree of assurance under all professional circumstances as does the familiar stereotype of the TV repairman or journeyman carpenter.

> On the other hand, there may be found equally strong temptation to revert to unbridled intuitionism--on the part of those who somehow sense the inadequacy of established situation science applied to emergent situation reality.

This reminded me of the recent blog exchange between [Peat](http://peat.wordpress.com/2006/08/14/software-and-common-sense-part-ii/) and [Alex](http://jooto.com/blog/index.php/2006/08/16/why-do-geeks-hate-common-sense/) regarding the role of common sense and intuition in application development.

It is an attractive and beguiling illusion that attempts to persuade us to think that if we just apply enough analysis from correct principles, we'll produce something "correct." And we should do the analysis first. That pretty siren sings so sweetly over the shipwreck mess of many development projects. The allure is so powerful, of course, because sometimes it is correct. The problem is when to do this and at what scale.

Sometimes it is much better to analyze things first. Some people will say, "First make it correct, then optimize it." But when speaking with [Stefan Kaes](http://railsexpress.de/blog/) at RailsConf 2006 after his talk, I thanked him for pointing out that some consideration for performance _must_ be made up front. To paraphrase his reply, "Absolutely". Here, the scale is large. Broad decisions are made, not detailed ones. And it is necessary to do it earlier rather than later because this broad decision will dictate the confines under which many small decisions are made that create a structure of significant weight that will resist change.

I was a bit disturbed to read [this comparison](http://martin.ankerl.org/2006/03/03/tracer-bullet-development-versus-extreme-programming/) of Tracer Bullet Development versus eXtreme Programming where it was asserted that TBD uses up-front design while XP does not. Obviously, using XP, you don't just start randomly writing code. _Somewhere_, _somehow_ a bunch of decisions were made that create the context in which you start writing tests. Disregarding appropriate situations at which to make preliminary decisions is as dangerous as deciding too much.

Even if we know extremely well the technical details of the small bits of test-driven code we are writing, it's probably guaranteed that we have but a faint understanding of how those pieces will make a complete application. As Robert points out summarizing Kurt Lewin in "Field Theory and Learning"

> In short, it is not ... that the whole is _more_ than the sum of its parts; it is _different_ from the some of its parts

