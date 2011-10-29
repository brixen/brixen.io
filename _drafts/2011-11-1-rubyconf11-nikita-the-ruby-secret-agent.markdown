--- 
title: RubyConf11 "Nikita - The Ruby Secret Agent"
layout: post
author: Brian
---

_NOTE: This post discusses in more detail the topics I covered in my
RubyConf11 talk. The video is [available on Confreaks](http://t.co/FQAKgu4s)._

---

## Forests

> _Ruby has the best tools_ -- No One Ever

The title of my talk refers to a specific tool, _Nikita_, that I am building
to use the features of Rubinius to create a much richer experience for Ruby
developers. Working on my ideas for Nikita, one thing constantly perplexed me.
_Why does Ruby have essentially zero tools?_ This is a big-picture question.
So we're going to talk about forests for a while. Eventually, we'll get back
to the trees.

We typically hear things like "Ruby is a beautiful language" or "Ruby makes me
happy". Ruby _is_ a beautiful and elegant language. Many people report being
more productive and happier writing Ruby code than writing code in many other
languages. Unless they are all delusional, we have to take that seriously.
Ruby has some special characteristics, not the least of which is the
designer's intent to help programmers better enjoy their craft. We owe Matz a
huge debt of gratitude for making a _value_-based versus technical choice to
respect the programmer's experience. Emotion is tremendously important in human
experience. It is a particular strength of Ruby that it values emotion. We all
want to be happy, right?

Ruby, however, is not just all fluff and fuzzy warm feelings. Ruby's elegant
and powerful features empowered developers to build Rails. Whatever your
personal feelings about Rails, it is undeniable that it changed the world of
web development. Whether comparing against Rails or distinguishing itself from
Rails, every other framework in many other languages, Ruby included, holds
Rails up as _the thing_ against which their value is measured. The stature of
Rails certainly makes us proud of Ruby and, if we are Rails developers, proud
to be using such a great framework.

> _proud_ adj. feeling deep pleasure or satisfaction as a result of one's own
> achievements, qualities, or possessions or those of someone with whom one is
> closely associated

Wow, just reading the definition conjures some of the positive experience of
feeling proud, doesn't it? Pride is tightly bound to another fundamental
aspect of human existence, the feeling of belonging. We can _personally_ feel
proud just seeing someone from the group to which we belong do something well.

Again, though, Rails is not the measure of web frameworks simply because it
makes some developers feel happy. Rails repeatedly demonstrated its utility in
building successful websites and skillfully handling the complexity involved
in doing so. Rails repeatedly proved itself. That is what got businesses to
take Rails seriously. Not just a little seriously. If we totalled the
investment in Rails directly and indirectly through the value of customer
relationships and market capitalization of companies who bet on Rails, I am
certain that value would be in the _billions_ of dollars.

Think about that for a moment. Rails challenged a well-established industry
with _billions_ in corporate backing for a language that had more than a
decade of heavy use and Rails, against the odds, has succeeded and proven
itself. Consequently, whereas just a few short years ago, a handful of people
at RubyConf were being paid to write Ruby, now almost _everyone_ there is paid
to write Ruby. Not only that, but there are numerous other developers who
_could_ be getting paid to write Ruby. There is a _shortage_ of Ruby
developers. _Why the hell is that?!_ If Ruby is everything we are claiming it
to be, why are we not attracting away Java developers, laboring away in their
primitive static type prisons of crushing complexity, in droves?

The reality is, people are leaving Ruby. Prominent Rubyists who would have
been at RubyConf were not here this year. In fact, when asked at one keynote
who was attending their first RubyConf, a large majority of the people raised
their hands. We can extrapolate that the Ruby community is growing, which
would be great. Or we can wonder if all the spots for new attendees were freed
up by experienced Rubyists who no longer saw the value in attending _the
official annual international Ruby Conference_. Of course, it's most likely
both.

So, what is attracting away Ruby developers? Based on conversations I've had,
there are three prominent technologies: Node.js, Clojure, Scala. While it is
no longer politically correct to make fun of Java in the Ruby community, Java
is still the most potent threat to Ruby's survival as an industrial language.
Clojure and Scala are two languages that give developers plausible deniability
to distance themselves from Java while still deeply relying on Java.

The shift to other languages is accompanied by a good deal of rationalization
and chest-thumping about being a _polyglot_ and using the right tool for the
job. These rationalizations have all the surface validity of a logical
argument with none of the substance.

Ruby can run multiple concurrent event loops along with normal, sequential
code in one process on multiple platforms with the rich libraries and package
management one would expect from a powerful, general purpose programming
language. How the hell is Node.js a better tool for server-side programming?

Clojure is an elegant system with all the success of decades of Lisp syntax
barely warmed over to be ever so slightly more palatable to developers who
have come to expect _not_ to have to repeatedly re-invent the wheel of syntax.

The errors that a static type system catches are not the errors that I need to
worry about. The problems that static type systems solve are not the problems
that I want to solve. Type systems are actually really sharp knives. We lament
what junior developers do when we give them spoons and forks, and you want to
tell them to go play with sharp knives. Great, this will end well.

Don't mistake me, I'm all for using the correct tool for the job. But as I
have seen it playing out, _polyglot_ is the new liberal. Everything is good
and everyone's choices must be respected, however batshit crazy they are. This
really makes no sense. If a politician were running for office on the
platform, "All the candidates are equally qualified, but you should choose
me", would you expect them to get elected? Do we expect Ruby to be successful
if we don't fight for it, if we don't stand up and show why Ruby is a better
  choice for a majority of developers solving a wide variety of problems?

In fact, in many cases the reasons people are leaving Ruby have almost nothing
to do with the Ruby language and everything to do with the technical deficits
that exist in MRI and have not been solved after 18 years of development. The
confusion that MRI _is_ Ruby complicates the discussion of which technology
is a better choice. _This is extremely frustrating._ For Ruby to prosper, we
must convince the world, Ruby community included, that **MRI != Ruby**.

Why should we take the technical deficits of MRI so seriously? I'll tell you
why. There is an emotion as powerful in deciding our actions as ignorance
or even fear. That emotion is _disappointment_. What happens when someone
uses Ruby, is delighted in the application they have built, but when they run
it the performance is impossibly unacceptable? They just can't use it. So they
tweak and try to optimize, but their efforts are not rewarded. Eventually the
glow of happiness wears off and is replaced by disappointment. They realize
they are willing to sacrifice happiness for a viable solution to their
problem. That disappointment may even lead to resentment. A disappointed
person may become a vocal critic to justify the resentment they feel.

To fully understand the danger of disappointment, however, we must consider
_why_ Ruby is popular today. Ruby is popular because _business_ has bet on
Ruby.  Business is hard. Business is customers. No customers, no business.
Business decisions balance fear and greed. Business is afraid someone will
steal their customers and motivated to get all the customers they possibly
can. We need a reality check. Developers are _not paid to be happy_.
Developers are paid to make customers happy so businesses can make profits. If
developer happiness and customer happiness collide, who loses? I'll give a
hint, it's not the customer. If we as developers want to be paid to be happy,
we better make customers happier faster than anyone else can. That's the
golden ticket.

Sometimes Ruby enables us to deliver and cash in on our golden ticket. These
days, that's not always the case anymore. Fortunately, we don't have to wonder
what business will do when they become disappointed with Ruby because Twitter
has laid it all out for us in bullet points. The following video is the most
damning five minutes about Ruby on the internet. The problems Raffi enumerates
against Ruby will be echoed by increasing numbers of serious businesses if we
don't pay attention and fix them.

<iframe src="http://player.vimeo.com/video/29993216?title=0&amp;byline=0&amp;portrait=0"
  width="640" height="360" frameborder="0">
</iframe>

(You may be interested in the [full-length video](http://www.oscon.com/oscon2011/public/schedule/detail/20527))

Let's summarize the issues that Raffi listed:

**Critical Ruby Issues**

* Garbage collection
* Concurrency
* Performance
* Tools

Am I worried when I watch Raffi's talk? You bet I am. I love Ruby. I find it
to be a fantastically good language. And I have worked incredibly hard on
Rubinius and RubySpec for the past nearly five years to improve the quality of
Ruby and extend its availability. I want developers to be happy. I want
customers to be happy, too. What I absolutely do not want is to be sitting
around talking about how "Ruby _was_ a great programming language" while
lamenting some poorly integrated or retarded feature in Java 10.

We have covered a lot of ground on this roller coaster from developer
happiness to disappointment and ultimately worry about Ruby's future. But what
about the topic of tools that kicked off the whole discussion? If _tools_ are
the answer, what are the _questions_? From my perspective, tools answer two
vital questions that are really sides of one coin:

* _How do I understand this code?_
* _What should I be afraid of in this code?_

We need understanding of and _insight_ about our application's code to do our
job well. We don't fear things we understand well and are capable of handling.

If those are the questions, how do tools help answer them? Well, I'm not going
to tell you yet. First, to underscore several real problems, we're going to
look at a handful of actual and proposed _solutions_ from MRI. Yes, this is
backwards. We need to fully understand a problem _before_ we can fashion a
suitable solution. By examining these broken or incomplete solutions in MRI,
we can better understand the actual problems. Then we will more clearly see
how tools can help.

## Solutions & Problems

The following are four of the most worrisome things that I see either in or
orbiting around Ruby.

* Optional typing
* Hidden typing
* Refinements
* -w

Optional typing is one of those zombie topics in Ruby. No matter how many
times you kill it, it will keep coming back. The flawed reasoning goes
something like this, "Statically-typed programs are generally faster than
Ruby. Therefore, Ruby is slow because it lacks static typing." At the least,
this confuses correlation with causation. In reality, Ruby has been slow for a
lot of reasons and static typing is _not_ a central issue.

Most importantly, however, is that static or optional typing is extremely
_inconsistent_ with the design of Ruby. Ruby is about _behavior_. It's not
_who_ you are but _what_ you do that matters. We typically use the term
_ducktyping_ to describe this.

This is one of the most important points here, so pay attention.

Classes organize code for humans to understand. That is their most important
role. Furthermore, classes support _encapsulation_. Data and the logic that
operates on that data are bound together inside a container that separates an
object from its environment. You send messages to an object to induce
computation. Let me repeat: Classes support encapsulation, which helps humans
conceptually organize code to effectively tackle complexity when modelling
some domain.

Classes are not the most important concept in object-oriented design.

Quoting Josh Susser, "There are three pillars of OO: encapsulation,
polymorphism, and inheritance." Of those three, inheritance is the least
important. Moreover, inheritance does not require classes. Prototypes are just
as useful for implementing inheritance as classes are.

Attempts to bring optional typing to Ruby are really attempts to impose some
rigid class requirements. This rigidity can severely weaken Ruby's power to
handle complexity, the power that derives from focusing on _behavior_ in Ruby
instead of class structure. To illustrate the importance of this, consider
invokedynamic in the Java world. It's all the buzz right now. _But
invokedynamic is 100% a work-around for the fact that Java needlessly
hardwired rigid class requirements right into the virtual machine._ It's a
hack.

As wrong-headed as optional typing is for Ruby, there is something even worse
that is actively being added to MRI:

> **Hidden Typing** - _typing requirements that are hidden from Ruby code_

I don't think there's an actual term for this so I'm making one up.  What I'm
referring to as _hidden typing_ is described by its several unpleasant
characteristics: It's not in Ruby code. It is often undocumented or MRI claims
it is undefined behavior. Most importantly, _your Ruby code cannot
participate_.

Consider the following C code in MRI:

{% highlight cpp linenos %}
VALUE
rb_to_float(VALUE val)
{
  if (TYPE(val) == T_FLOAT) return val;
  if (!rb_obj_is_kind_of(val, rb_cNumeric)) {
    rb_raise(rb_eTypeError, "can't convert %s into Float",
    NIL_P(val) ? "nil" :
    val == Qtrue ? "true" :
    val == Qfalse ? "false" :
    rb_obj_classname(val));
  }
  return rb_convert_type(val, T_FLOAT, "Float", "to_f");
}
{% highlight %}

If we rewrite this in Ruby and imagine seeing this in some Rails application
on which we've been called in to consult, we would immediately detect the code
smell and start asking why this code is coupled to a _particular_ class. Why
should our standards for our Ruby applications be higher than our standards
for our Ruby implementations?

{% highlight ruby linenos %}
def wrong(a, b)
  unless a.kind_of? Numeric
    raise "must be an instance of Numeric"
  end
  # ...
end
{% highlight %}

The critical thing to understand here is that Ruby is dictating the
_structure_ of our programs. Ponder that. This is brittle, _unnecessary_, and
wrong. I'm not going to mince words here; this is alarming.

One of Ruby's greatest strengths is the focus on behavior. It allows us to
model complexity easily and evolve a system over time by computing with
objects that act a particular way. Types only tell you what you _cannot_ do.
Like all walls, people will either try to defeat them, or bash their heads
into them. The rigidity caused by your programming language dictating the
structure of your programs leads only to more complexity, and with it, more
pain. Types, we don't need 'em.

Emphasizing types distorts the focus of Ruby on behavior. And how do we model
behavior in Ruby? With message sends, of course. Messages are implemented with
methods, which have names. So far, Ruby has been an A+ object-oriented
language. How could we mess that up real good? I'll tell you, _refinements_.

Refinements are one of the leading proposals out there for _ruining_ Ruby. I'm
not being hysterical here. It's really that serious. The _primary_ purpose of
refinements is to _hide incompatible changes_. It takes _naming_, one of our
most powerful abstractions for handling complexity, and turns it into a
horror-house of funny mirrors where things are no longer what they look like.
With refinements, all we get is more complexity. Refinements do nothing to
help program comprehension for our applications. Instead, they unnecessarily
complicate it. Further, refinements do nothing to lighten our burden.
Libraries still need integration testing, just as they did before, but now the
testing will need to be more complex, I guarantee it.

Most importantly, refinements not just encourage, but practically demand what
I call _"What if?"_ programming. Rather than solving actual problems by
modeling actual systems, "what if" programming is about illusion. It is
motivated by _fear_ ("what will happen if?") or by _arrogance_ ("I know better
than you what you need"). Both attitudes of fear and arrogance are common in
programming, and quite understandable. But they both have deleterious effects
on the quality of software.

Ruby's dynamic nature presents two axes of integration that both must be
respected. The Ruby core library is a very broad base of integration points.
Ruby code that breaks the Ruby core library just isn't permitted. Sorry. One
thing that severely hampers good horizontal integration is the fact that MRI
uses C to write the core library, does not uniformly dispatch to Ruby methods,
and does not document what other core methods are composed by a particular
core method. Think about that. What if Array#[] _documented_ that it composes
Fixnum#+ and Fixnum#/ to calculate an index. Then it is obvious to a library
author that if she breaks the Fixnum#/ post-condition, she must fix all the
code that depends on it.

The other integration axis is vertical integration. Not all libraries written
for Ruby will necessarily work with any arbitrary application or other
library. To expect that a library would is unreasonable. There may be class
name clashes or both libraries may define a method of the same name
incompatibly. That is life. That is what tests are for. Furthermore, if there
is a particularly use idiom that evolves in a framework or library, it is
probably a good candidate for inclusing in the Ruby core library. The fact
that this has happened very slowly for some excellent Rails idioms indicts
more the MRI development process than the language for lacking such a harmful
feature as refinements.

Finally, in my list here of solutions (a non-exhaustive list for certain),
there is the _-w_ command line switch.  Ostensibly, -w is supposed to help us
write better code. In fact, it won't help much. Firstly, the functionality is
hidden away in the parser and is fairly _ad hoc_. Secondly, it does not deal
in _Ruby objects_, which are the currency of Ruby programs. Thirdly, there is
no programmatic control and no configuration. There is no way to tell it that
is _not a useless use of ==_.  Finally, it does no real semantic analysis. It
detects a few syntactic patterns and that's it. We should have much better.

Let's take stock for a moment. What were the critical Ruby issues that Raffi
enumerated?

**Critical Ruby Issues**

* Garbage collection
* Concurrency
* Performance
* Tools

I can't find any of these hot-topic solutions that I've been discussing on
Raffi's list. In fact, it's embarrassing to compare the internal Ruby
community dialog with what Raffi is saying. _Ruby is bringing a knife to a gun
fight_ and we're gonna get served.

## Foundations

Each of the "solutions" above, proposed or implemented in Ruby, attempt to
answer the two important questions posed above: 

* _How do I understand this code?_
* _What should I be afraid of in this code?_

But they do so poorly, or in a way that will severely weaken Ruby's utility
for building elegant solutions to complex problems.

What should we do instead? I'll tell you what we are working on in Rubinius:

* Precise, generational garbage collection
* GIL-free, concurrent and parallel native threads
* Tiered just-in-time native machine code compiler
* Tool-friendly infrastructure

### Generational Garbage Collection




### GIL-free Concurrency

### Tiered Just-in-time Compiler

There is only one way to make programs run faster. Do less. While parallelism
is often possible, shortening the total time for a task by doing the same
amount of work but doing it simultaneously, the time to complete an operation
is still dictated by the slowest running part. Whether parallelism is possible
depends heavily on the nature of the problem being solved as well. So, while
parallelism is an important feature to have, it's not the main character in
the ever-popular story of Blazing Speed.

### Tool Support

The generation GC, GIL-free concurrency, and JIT compiler all make Rubinius a
compelling platform for building dynamic languages, including Ruby, that are
robust and perform well.


## Nikita

