--- 
title: Ethical Software Needs Dialogue
layout: post
author: Brian
---
Growing up in the United States in the late 70's, early 80's, futbol was something I knew very little about. Let's see, we played once in a great while in gym class, my most memorable experience there was taking a hard-kicked ball right in the face. Later in high school, the soccer team was a mere blip on the screen in the shadow of football and baseball. Much later I started playing soccer and, having so much fun, lament that I didn't play as a kid. The interesting thing to me about soccer (and many games, but you'll especially appreciate this if you listen to a soccer game on a hispanic radio station) is that the myriad plays and activities that make up the game are all directed toward scoring a goal (and preventing the opposing team from doing so). In other words, the goal of the game is simple and clear, though not easily achieved.

[Alex Bunardzic](http://jooto.com/blog/) is a champion of what he terms "ethical software". The idea goes by many names. My favorite is software that doesn't suck. I highly value Alex's ideas, so when I read his recent post, [Should-Driven Development](http://jooto.com/blog/index.php/2006/08/15/should-driven-development/), I couldn't easily dismiss his criticisms of Behavior Driven Development. At the same time, I don't agree that BDD itself is flawed as an approach to creating better software. BDD is a developer's tool. It's about coding. Of course, BDD cannot specify the goals of the software. So, if it is expected to, it will fail to produce software that doesn't suck.

One of the things about Scrum that I think is tremendously valuable, and yet one of those things that makes you say, "Duh!", is the emphasis on empirical process control. There are three components to that: 1) observability, 2) inspection, and 3) adaptation.

What both Scrum and BDD need to be effective is a clear and accurate statement of the goals. With a goal-directed process you have these components: 

1. somewhere you are trying to get to (using a geographic metaphor)
2. some process that accurately compares where you are at with where you want to go
3. a plan to move you incrementally closer to where you want to go
4. a process to evaluate whether your plan got you any closer

Or more briefly: goal, assessment, plan, implementation, feedback and around again and again.

The practice of BDD captures this well. Write the test to capture the expected behavior of the system relative to the goal. The test fails. Write the _minimum_ code necessary to make the test pass. Refactor. And around. The process alternates between writing new tests to describe expected behavior and the code to make the test pass and then refactoring to make the code better without changing its behavior. The process is powerful.

But as I said earlier, it is a developer's tool. Developers should never be specifying the goals for the software, just as the client and user should never be specifying the implementation. I'm rarely dogmatic, but about that I will be.

The problem that we face is how we can more accurately capture the goals for the software in our dialogue with the clients and users. Our exploration of that is what we are calling [d3](http://www.robbyonrails.com/articles/2006/08/08/d3-not-ddd). One significant part of that is education. Our experience is that _everyone_ from clients to developers begins thinking and talking in terms of the software implementation way, way too early. It's like talking to an architect about what finishes to use and what the windows look like long before you have established a vague idea of where the walls will be or if there will even be walls. The process is too often backwards. Talking about the minutiea of text field this and that before we have even established why in the world the user would be doing that in the first place. One approach that we are trying is dialoguing with the client about goals without talking at all about the web site. In other words, for that exploration, the web site doesn't even exist. Talk about thinking outside the tubes.

Another part of this is fostering a general respect for that fact that software that doesn't suck is constructed according to certain principles. Just because anyone can create an HTML form doesn't mean they should. As long as we collectively persist in thinking that _anything's possible_ and therefore it all boils down to a matter of opinion about software design, we will continue to create software that sucks.

So rather than putting down BDD for failing, we need to recognize that right now in the state of our craft there is a huge chasm between client interaction to establish goals for the software and the much lower level development that can excel through application of BDD.

What we need to develop is how to dialogue to create common understanding. What I am noticing as I try hard to be more aware of how we are communicating with clients is that "process" and "process artifacts" can often be counter-productive and obscure issues. If we are just trying to "fill in" the boxes in our process, are we stopping to really listen? It's like assertiveness training where you are taught to reframe your expressions using "I" statements. Rather than, "you are really pissing me off" someone might as an initial stab try "I feel like you are really pissing me off". Yeah, not very effective. Try that with your girlfriend if you don't believe me. More effective is, "I feel hurt when you say you don't want to play with my new Mephisto blog." One approach attempts to conform to the structure of assertiveness, one effectively conforms to the principles. What are the principles of effective dialogue?
