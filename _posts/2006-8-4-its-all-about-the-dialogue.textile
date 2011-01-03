--- 
title: It's all about the dialogue
layout: post
author: Brian
---
[Martin Fowler](http://www.martinfowler.com) is a paradox. That is, if you accept one of the common connotations of "enterprise software": evil. "I concentrate on designing enterprise software – looking at what makes a good design and what practices are needed to come up with good design.", says Martin. Yet, he is one of the giants of agile software development. Recently, at the second annual [foscon](http://oscamp.org/FOSCON), I won a raffle for a book. The one I selected from those available was Martin's _Patterns of Enterprise Application Architecture_. If you have not yet listened to his [RailsConf 2006 Keynote](http://blog.scribestudio.com/articles/2006/07/03/martin-fowler-railsconf-2006-keynote-address), I strongly urge you to do so.

A couple days ago, [Robby](http://www.robbyonrails.com) posted about [Dialogue Driven Development](http://www.robbyonrails.com/articles/2006/08/02/dialogue-driven-development). We'll leave it to the art historians to decide if the following artifact proves that while sitting together at Martin's talk during RailsConf 2006, I first wrote the words, or jotted them down after Robby summarized one of Martin's points. Robby often encourages "blog early, blog often". So I can hardly complain if he pre-empted me on publishing DDD since RailsConf was over six weeks ago.

<img src="http://blog.brightredglow.com/assets/2006/10/3/ddd_small.jpg" />


The important thing is that DDD is not just another marketing term. Although, it could be useful as one, so we want to distinguish between __dialog__, those artifacts from desktop applications that we on the web infrequently encounter, and __dialogue__, _n. a discussion between two or more people or groups, esp. one directed toward exploration of a particular subject or resolution of a problem_ (from my dashboard dictionary).

For me, the _-ue_ is all about user experience. And that is the meat and potatoes of application development that we should be targeting. Don't believe me? Think it's more about business logic, fancy technology, web 2.0, &lt;insert favorite CS concept here&gt;? I don't think so. But, don't take my word for it. You too can pre-empt me on a coming post by heading over and reading, if you have not, Alan Cooper, _About Face: The Essentials of User Interface Design_.

So, DDD. What we're trying to do is label a concept that is sorely in need of development. To flesh it out a bit from my perspective, here are a few points from Martin's keynote that I found particularly interesting.

<pre><code>martin_keynote.points.each do |point|</code></pre>

<blockquote>
<ul><li>The interesting thing about Rails is that it tries to do things differently than other software over the last few years. It doesn't try to be the one-size-fits-all solution.</li>

<li>What we are seeing is a drive toward simplicity. Conventional wisdom once was "quick necessarily means dirty". Ruby challenges that. As did Smalltalk, which showed that you could be quick and clean.</li>

<li>What's important about technology is the way it affects the whole conversation between customer and developers. It affects how we go about building software. The essence of XP from Kent Beck is this change in relationship so it is not a one way stream of "this is what I want": want -> tell -> build -> all is well. People may know what they want, but not what they need. We can build exactly what they want and still fail because it is not what they need.</li>
</blockquote>

<pre><code>end</code></pre>

It was after jotting down that last note that I wrote "dialog-based develepment" and then "dialog driven development" in my notes (I know, I misspelled it, too). The DDD term was prompted by the recent conversations [Jeremy](http://www.jvoorhis.com) and I had with [Steven Baker](http://blog.lavalamp.ca/) and [David Goodlad](http://david.goodlad.ca/) on the train to Chicago about Behavior Driven Development as they worked a bunch on a next-generation RSpec.

My pie in the sky is a Ruby DSL something like RSpec that could be used with clients to talk about the software. It would allow a spectrum from less specific-more tolerant to more-specific-less tolerant. At the left end is client dialogue about behavior of the software. Something like, "app should require login". A "failure" at this high level could be something like, _not implemented_. The spectrum continues down to the level of BDD with something like RSpec, where the focus is on behavior of the code.

Also on the train, [Josh Knowles](http://joshknowles.com/) was strongly advocating for much better acceptance testing. Of course, using iterative development, acceptance testing is not something done at the end, months or years into the project, but should be done frequently. The left end of the spectrum could support this _expectation based software behavior dialogue_.

Of course, these are very rough ideas. What I want to do is build out the understanding behind the word "collaboration" in the [Agile Manifesto](http://www.agilemanifesto.org) and identify how "individuals and interactions" work to create excellent software. Join the fun!
