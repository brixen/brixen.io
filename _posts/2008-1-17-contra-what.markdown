--- 
title: Contra--what?
layout: post
author: Brian
---
I'm going to be pedantic for a minute. If you are Betrand Russell, feel free to spend your time more productively. Everyone else, don't be afraid of a few symbols.

If you read my "last post":http://blog.brightredglow.com/2008/1/17/evil-can-be-dangerous, you might be inclined, as is every human mind, to reduce all those words to something simple you can put in your back pocket (maybe take it out later and show it to a friend). Perhaps something like this:

<pre>
  Immutable == Security == Good
</pre>

If you do that, you might get lots of nods and a fair bit of affirmation from folks. Makes perfect sense, right. You can make all sorts of analogies that _prove_ this to you. Consider my front door, if it's not easily opened, I feel more secure. Perfect. Must be true.

It's not. Things are not so easily distilled into such nifty little boxes.

Now, once they have this shiny, handy, palm-sized summary in their back pocket, folks tend to go the extra mile. They decide to make one of the most fundamental logic errors. Essentially, trying to think all the way around this hairy problem, they decide:

<pre>
  If Immutable == Security
  Then Not Immutable == Not Security
</pre>

Doh. That's where this contra thing comes in. Read the gory details on "Wikipedia":http://en.wikipedia.org/wiki/Contraposition, but here's the summary:

In logic, something like <code>A -> B</code> is read "A implies B" or "if A then B". It is very tempting to then think, "if not A then not B". Unfortunately, that is not generally true. Given "A implies B", the statement "if not A then not B" is called the _inverse_. Again, these are not generally logically equivalent. The statement "if not B then not A" is called the _contrapositive_, and it _**is**_ generally true that a statement and it's contrapositive are logically equivalent.

Applying this to the above, we can see that *IF* (a very big if) it is true that "if Immutable then Secure" is true, then the statement "if not Secure then not Immutable" is equivalently true. However, it has not been demonstrated that immutability is equivalent to security. And indeed there are numerous ways to achieve "security" (a word that begs precise definition) in a variety of different systems.

So, before you start touting something like Java because it is statically typed, immutable and "secure", consider whether you are making the mistake of confusing the inverse for the contrapositive. If you're feeling extra nimble and up for some mental gymnastics, consider this rather hyperbolic assertion:

> Ruby is a very, very sharp knife. Java is a little more like a butter knife. We safely leave butter knives on the table when the kids are around. But, we probably grumble more than a little when trying to cut our steak with a butter knife.

If we want to make Ruby "safer", it's possible to do so in the same manner as dealing with sharp knives: we make something like a sheath. We don't just take a hammer to the blade and dull it.
