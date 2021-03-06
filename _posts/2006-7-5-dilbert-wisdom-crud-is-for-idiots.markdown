--- 
title: "Dilbert wisdom: CRUD is for idiots"
layout: post
author: Brian
---
Last week, my esteemed colleague [Jeremy](http://www.jvoorhis.com), at his characteristic morning unveiling<sup>[1]</sup>, brought in a couple books on "Death March" projects. While he tackled the other, he lent me _Death March_: second edition, by Edward Yourdon. Edward defines a death march project as "one whose 'project parameters' exceed the norm by at least 50 percent". That is, one or more of the following is true: the project has less than half the budget, the staff, the time, or more than double the functionality, features, performance, or technical requirements. He discusses why death march projects are created, why people participate in them, and some things one might do to try to handle such a project (although he's pretty pessimistic about successfully changing a project of this type).  

Under the heading, _Why Do Death March Projects Happen_, Edward starts off with a great quote by the author of the _Dilbert_ cartoons, Scott Adams:

>When I first started hearing these stories [about irrational corporate behavior] I was puzzled, but after careful analysis I have developed a sophisticated theory to explain the existence of this bizarre workplace behavior. People are idiots.

>Including me. Everyone is an idiot, not just the people with low SAT scores. The only difference among us is that we're idiots about different things at different times. No matter how smart you are, you spend much of your day being an idiot.

Hopefully everyone is not totally insulted at this point. As in _Dilbert_, this idea can be a great source of inspiration. It's really not as derogatory or as hopeless as it sounds. And for me, it puts some recent events in perspective.

Since DHH's keynote at RailsConf, there has been noticeable buzz about CRUD. Everything from [new acronyms](http://jimonwebgames.com/articles/2006/06/26/dont-say-crud-say-fucd) to [debates](http://www.jvoorhis.com/articles/2006/06/28/journaled-domain-models-via-the-command-pattern-or-its-all-just-crud-pt-ii) about [nouns versus verbs](http://blog.jasonwatkins.net/articles/2006/06/27/are-nouns-better-than-verbs). All good stuff, interesting, thought provoking. But for me, probably the greatest benefit of more CRUDful modeling is better managing of complexity. I think this is the raison d'être of CRUD.

Similar to when OOP was capturing hearts and minds, many people waxed poetic about reuse, more faithful domain modeling, etc. But the golden egg of OOP is encapsulation, and encapsulation is another powerful abstraction that helps manage complexity. If there were one thing I would lobby to be added to the agile manifesto, it would be "Simplicity over big, amazing, mind-boggling complexity". Certainly, the "less software" mantra is related to this, but even a tiny piece of software does not necessarily mean simple, not complex.

So, if you notice your controller method count is ballooning, or your controllers are more cross-wired than your plate of spaghetti, you might see an opportunity for using CRUD to restore sanity. But you can also ruthlessly adopt Einstein's wisdom at every stage of development and use CRUD to make your app as simple as possible, but not simpler.

<hr style="width: 10em;">

<sup>[1]</sup> Jeremy often comes to work with an announce if you will. For instance, one day we were discussing something about languages; I mentioned Erlang. The next day Jeremy announces when he arrived, "I learned Erlang last night." Sweet!
