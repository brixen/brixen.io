--- 
title: Tracer bullets are about aiming, not firing
layout: post
author: Brian
---
There's more than one way to shoot down a moving target. [Dave Thomas](http://blogs.pragprog.com/cgi-bin/pragdave.cgi) and [Andy Hunt](http://www.toolshed.com/blog/) have used the metaphor of tracer bullets to describe an approach to software development. [Martin](http://martin.ankerl.org/2006/03/03/tracer-bullet-development-versus-extreme-programming/), [Badgerism](http://www.badgerism.com/archives/2005/11/21/ship-it-chapter-3-pragmatic-project-techniques-2/), [Peter](http://www.pbell.com/index.cfm/2006/7/9/Ready-Fire-Aim), [Lights Out Production](http://www.lightsoutproduction.com/index.php?option=com_content&task=view&id=32&Itemid=71), and [Jeff](http://www.codinghorror.com/blog/archives/000256.html), in no particular order<a href="#sub1"><sup>1</sup></a> and among many others, have weighed in with their thoughts.

But how does firing at a moving target with tracer bullets work? It's a gross over-simplification to say you just fire-aim-fire-aim. In fact, the key to the process is how aiming itself provides immediate feedback to refine aiming. As Dave himself says,

> Basically, it all comes down to feedback. The more quickly you can get feedback, the less change you need to get back on target.

So, the process actually goes something like this:

1. you have already acquired a target
2. you have initially aimed the gun
3. you fire and watch where the tracers go
4. you re-aim based on where the target is now in relation to the tracers

That's a single person aiming, firing, watching, aiming, ... That's a process that is happening over short instants of time. Where you aimed a fraction of a second ago is still visible in the stream of tracer bullets when you adjust your aim.

Now translate that to a team developing software. No longer is it one person. No longer is the feedback loop on the order of fractions of a second. Time stretches to weeks or months between the initial target acquisition and aiming until the feedback comes in. How does that feedback inform the original rationale for the design decisions or even for the target acquisition?

In the process we are refining at [PLANET ARGON](http://www.planetargon.com), we insist that we document the rationale for our design decisions. This includes documenting our discussions with the client and domain experts to identify the goals of the software and its users. This is a very lightweight process, usually about a small paragraph per major design decision. We typically use a wiki to record the documentation and aggregate in the same place useful references, project documentation, interviews, etc.

To some folks, documentation may be a dirty word, something to shun or dread. Not for us. Documentation is simply our way of providing a record of the decisions we make so that feedback can be evaluated in context. From my dashboard dictionary:

> _documentation_, n.
>
> Material that provides official information or evidence or that serves as a record

I'm at a loss to understand how else you would do it. Tracer bullets don't help you a bit if you are just firing randomly. And I think that's what people miss about the process. You really do _aim_ first. And if you can't remember why you aimed where you did, or if the person who did the aiming  has left by the time feedback is coming in, that feedback may be interesting, but it certainly isn't going to enable you to refine your decisions.

<p>&nbsp;</p>
<a name="sup1"><sup>1</sup></a> Thanks to [Robby](http://www.robbyonrails.com) for providing links to some of these articles
