--- 
title: One cuckoo flew over the nest
layout: post
author: Brian
---
Firstly, a disclaimer in the words of the inimitable Ken Kesey:
>Take what you can use and let the rest go by.

Interestingly, when I googled this quote to ensure I was recalling it correctly, I found some other [excellent quotes](http://en.wikiquote.org/wiki/Ken_Kesey). Another that seems apropos:
>You don't plow under the corn because the seed was planted with a neighbor's shovel.

If Dialog Driven Development is merely [rounded corners](http://mechanismalley.com/blog/2006/08/04/on-product-backlogs/) to you, please continue to enjoy your square ones. This exploration is not aimed at gathering the true believers. I'm not the evangelist type. So, if you're worried I'll show up on your doorstep thumping my bible, rest assured I won't. I'm an atheist.

That said, I think there is value in creating distinctions to better understand the terrain. Agile is a big umbrella. If the processes were formulaic, all we would need to worry about is a good algorithm. 

Recently on a flight to DC to meet with a new client, I delved into a book [Robby](http://www.robbyonrails.com) brought along: _Agile Project Management with Scrum_ by Ken Schwaber, one of the co-founders of the Scrum method. Below are a few notes I jotted down on my index cards while reading the first 4 chapters and browsing the appendices. Since then I've browsed some of the other chapters but I haven't finished the book. 

**advantages of Scrum**

* emphasis on empirical process control
* iterations
* daily team meetings where each member presents what she did in the past 24 hours, what she'll do in the next 24 hours, and any blockers
* frequent feedback loop
* clear separation of responsibility using the pigs and chickens metaphor to facilitate more effective decision making and reduce interference by chickens, which can bog down the process
* The three legs that hold up the implementation of empirical process control: 1) visibility - aspects that affect the outcome must be visible to those controlling the process; 2) inspection - these aspects must be inspected frequently enough to change course if necessary before too much has elapsed; and 3) adaptation - changing course when new information suggests it is necessary
* emphasis on having a _vision_, it must be a vision that is fairly resistant to change in order to guide the project, but able to change when required


>"_You can get through almost anything if you don't try to impose rigid solutions before problems even arise, instead devising solutions as necessary when problems crop up._" (page 131)

**drawbacks to Scrum**

* specifying the product backlog - this suggests too much _dictation_ and not enough _collaboration_. According to the book, the product owner specifies the backlog and prioritizes the items in it. The team meets to decide which items it can deliver in the next sprint. That process is two monologues not a dialogue.
* 30-day sprint is too long. I don't think the feedback cycle is nearly as effective at this scale because we need feedback long before functionality is "deliverable". More frequent testing is needed to refine features. Imagine getting a haircut where you tell the stylist what you want. She then takes you to a room with no mirrors and starts chopping away. When she's done she takes you to another room to demo your new haircut. Fortunately, the difference between a bad haircut and a good one is about 2 weeks. The same is hardly true of software.

The process of software development requires a lot of educating of the people involved. The product backlog does not encourage thinking in this way. I dislike the sequential list where the only explicit organizing idea is priority. Where is the context and relation between what is being specified? And how does the process ensure that the product owner doesn't fall back to specifying things like, "Dialog X needs a dropdown field to display Y", or "Build a screen to display user stats"? If you haven't had to deal with this, then I desperately want to come visit your universe. If you don't know why this is the biggest ingredient in a recipe for disaster, just continue building software this way.

The way to challenge this is with true, effective dialogue. What that looks like varies a lot. But it's not about particular artifacts. If you read [Manley's](http://mechanismalley.com/blog/about/) criticism of our [rounded corners](http://mechanismalley.com/blog/2006/08/04/on-product-backlogs/), he relates the necessity of educating product owners. If dialogue is at the center of your process, the product backlog could function as a passable way to document the evolving mutual understanding.

My favorite idiocy in software development is the crystal ball method. Everyone has a crystal ball on their desks from which they can conjure a precise, detailed, perfectly focused picture of any event at any point in the future. Of course, this is an absolute absurdity. But that doesn't stop people from believing such feats are possible. The product backlog easily falls prey to this delusion.

A much more useful metaphor is based on the simple fact of vision that any sighted person can appreciate. From where I stand, there are a number of things in crisp focus. Beyond that, things are mostly distinguishable by shape and relationship. I'm seeing the forest. Beyond that, only the vaguest, broadest features are distinguishable. I see that mountain, but the dark areas juxtaposing the snow may be forest or exposed rock. I can't tell.

Attempting to draw on this fact of vision to inform and structure dialogue about a recent project, we set up a wiki with a page to capture descriptions of the software's behavior in terms of goals. We have three sections: 1) near term goals, 2) medium range goals, and 3) long range goals. These follow the rough divisions of visual clarity described above.

The process of transforming those goals into software features and determining their priority based on architectural constraints is **not** something a client can dictate. You don't tell your architect how to construct your house, you describe what you want in it. The reason for that is simple: physics dictates what is a viable structure. In software, we have no appreciation for physics. Clients believe they can do anything. All the rusting hulks of failed software littering the desert notwithstanding.

The essential way to bring the analogue of physics to software development is mutual education mediated by effective dialogue. What that actually looks like needs a great deal of definition. If this is just rounded corners on existing work, please point us in the right direction.
