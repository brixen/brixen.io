--- 
title: Are your tests findable
layout: post
author: Brian
---
I probably use Google search on average 20-30 times a day. It's an indispensable tool for me. It's definitely not the last word in search engines. I can imagine a lot of additional functionality, like contextualizing my searches over time or within categories. But overall, it works reasonably well.

Lately, I've been reading _Ambient Findability_ by Peter Morville. He provides this definition for findability:

<blockquote>
findability <em>n</em>
<ol>
<li>The quality of being locatable or navigable.</li>
<li>The degree to which a particular object is easy to discover or locate.</li>
<li>The degree to which a system or environment supports navigation and retrieval.</li>
</ol>
</blockquote>

Peter explains that findability is defined at both the object and system levels. For example, the title of a document or the color of a pen on your desk. At the system level, you can ask questions like, "Can a traveler navigate an airport," or "Can a user navigate a website."

While these ideas help us frame the concepts, how do we evaluate findability in concrete situations. Not surprisingly, there are elements of findability that we can examine:

<blockquote>
Findability requires definition, distinction, difference. In physical environments, size, shape, color, and location set objects apart. In the digital realm, we rely heavily on words. Words as labels. Words as links. Keywords.
</blockquote>

Hmm, interesting. At [PLANET ARGON](http://www.planetargon.com), we have been evaluating using the _rspec\_for\_rails_ plugin to focus more heavily on [BDD](http://behavior-driven.org/). One of the things BDD emphasizes is leveraging the power of words to help us think more effectively (accurately) about our code. We have been incorporating BDD style method naming into our TDD practices, as well as refining our ability to specify application behavior in our tests.

One thing I dislike about the regular `Test::Unit` framework is that the methods are often organized ad hoc. Whatever makes the most sense to the programmer when adding those particular tests. Sometimes it's just appending the method to the list of existing methods. Most often, I notice some sort of organization. Which makes sense; that's how we deal with information. But the framework doesn't provide any guidance here.

With the [RSpec](http://rspec.rubyforge.org/) framework (check out [RSpec on Rails](http://rspec.rubyforge.org/tools/rails.html)), you can arrange your methods into contexts. I think this encourages better organization and contributes to the quality of findability as discussed above. Tests are just another type of information we interact with. How much effort does it take to locate what you're looking for, understand what the tests are saying, understand the output when a test fails? Following along [Jeremy's](http://www.jvoorhis.com) questions about [acceptable](http://www.jvoorhis.org/articles/2006/08/26/is-your-test-suite-acceptable) tests:

Are your tests findable?
