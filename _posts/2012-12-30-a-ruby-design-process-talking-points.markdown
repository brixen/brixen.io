--- 
title: A Ruby Design Process - Talking Points
layout: post
author: Brian
---

_At RubyConf 2012, I gave a talk [proposing a Ruby design
process](http://confreaks.com/videos/1278-rubyconf2012-toward-a-design-for-ruby).
Following the conference, I detailed the process [in a blog
post](http://brixen.io/2012/12/11/a-ruby-design-process). I submitted [a
ticket on the MRI bug tracker](http://bugs.ruby-lang.org/issues/7549) asking
Matz to consider my proposal. The [proposed design
process](http://rubyspec.org/design/) is summarized on the RubySpec website.
If you support the proposed process, please add your voice by signing at the
above link._

The discussion of a Ruby design process is emotionally charged. People focus
on their own ideas and illusions far more than facts. Conversations resemble
political debates, not technical discussions. Consequently, ten times more
energy is invested in clarifying misunderstandings and misinformation than in
substantive discussions about the merits of the proposal.

To help keep the discussion focused on the merits, the following points
amplify and further explain the proposal.


## Priorities

Every reasonably complex endeavor has elements that compete. Examples are all
around us. "You can have it fast, cheap, good; pick any two." The CAP theorem.
Enough time for recreation but enough money to pay the bills. The only way to
resolve such tensions is to prioritize. The same is true of a Ruby design
process.

The Ruby programming language is complex. Any implementation of the language
is unavoidably complex. There are half a dozen significant implementations of
Ruby. Those all represent different interests in Ruby. Attempting to implement
a unified definition of Ruby is undeniably complex and difficult.

It's easy to imagine that Matz would have different priorities than another
team implementing Ruby. _The purpose of the proposed design process is to
prioritize those things that create a unified Ruby programming language._

For businesses and developers whose salaries derive from writing Ruby, the
value of a unified Ruby programming language should be obvious. If someone
believes that businesses, customers, and developer salaries would be better
served by a fragmented Ruby language, they are encouraged to give their
argument in support of it.

_**There is no definition of the Ruby programming language that is complete and
accurate enough to provide unity to the Ruby community.**_

The proposed Ruby design process prioritizes the following things:

1. A precise and clear description of what exactly is the Ruby programming
   language.
1. Efficient use of the time and attention of implementers.
1. Fairness to all implementations in deciding Ruby programming language
   features.


## The Design Process Is Focused On The Definition Of Ruby

_The product of the proposed design process is a precise, verifiable, and
unified definition of the Ruby programming language._ The definition is
independent of any particular implementation. There are numerous programming
languages used to implement Ruby. None of those languages, or implementation
artifacts that result from the use of those languages, should be given special
preference in the definition of Ruby semantics.

The RubySpec project is the only project that has the explicit goal of a
complete, executable description of the Ruby programming language. The
product of the proposed design process is a more complete and more accurate
RubySpec exactly describing the behavior of the Ruby language in a way that
gives developers and the rest of the Ruby community clarity and confidence in
understanding Ruby.


## The Design Process Is As Simple As Possible, But No Simpler

The proposed design process does not impose any restriction on any
implementation with respect to experimenting with Ruby language features. This
appears to be one of the most misunderstood parts of the proposal.

Every implementation is completely free to experiment with language features.
They can use whatever development model they choose, whatever source control
they like, write or not write tests in any framework they fancy. They may
collaborate with other implementations in any way they wish. They can discuss
features in any language, on any mailing list they choose, or by means of any
medium they wish.

In other words, the MRI developers can continue doing exactly what they have
been doing.

The design process is only concerned with what becomes the official definition
of Ruby. Experimental features may or may not ultimately have value. The
design process is optimized for reaching consensus on the features that will
be part of a unified definition of Ruby with the least amount of
work or ceremony.


## The Design Process Is Open To The Community

Right now there is no formal design process for determining what features are
officially Ruby. There has never been a design process. People sometimes
propose a feature to Matz and sometimes he accepts it. Most of the time,
language features result from Matz's experimentation with the language. Matz
has repeatedly said he has the absolute authority to decide what features can
be called Ruby. If this _ad hoc_ process is "open" to the community, then so
is the proposed design process.

Under the proposed design process, anyone, whether from the Ruby community or
not, can propose a feature to Matz, just like they can now. If Matz agrees
with the proposed feature he, or other MRI developers, can bring it to the
Ruby design council for discussion and approval. Hence, the proposed process
is just as "open" to the community.

However, the proposed process is even more open to the actual Ruby community.
There are Ruby developers that are entering the community from Java and may
never use MRI at all. If they have an idea for a Ruby feature, they may be
able to implement it in Java but not C. They would be able to work with JRuby
to propose a feature that has been implemented, tested, and validated with
actual experience.


## The Design Process Is Efficient

The proposed design process requires that language experiments are clearly
documented and described by precise specs before being proposed as official
Ruby features. The discussion then focuses on concrete issues. This approach
makes efficient use of the attention of Ruby implementers. It also limits
communication about irrelevant details, further reducing the burden on Ruby
implementers when reviewing proposals.

Most important, precise specs makes the effort of implementing the feature as
small as possible. This also makes the most sense: Who is more qualified to
describe precisely how a feature works by writing specs but the people
proposing the feature?

While the design process requires documentation and RubySpecs, it does not
prevent an implementation from writing fully functional code for the feature.
The design process only lists what is _required_ in a proposal. It's doubtful
any feature could be proposed with sufficiently detailed documentation and
RubySpecs without any code.


## The Design Process Concerns Language Evolution, Not Experimentation

Under the proposed process, Matz is as free to experiment with the Ruby
language as he ever has been. So is every other Ruby implementation. However,
developers, businesses, and Ruby implementers get clarity, visibility, and
transparency for what is officially Ruby. The proposed process is only
concerned with features that will be part of the unified definition of the
Ruby language.

The proposed design process is not concerned with how implementations
experiment with language features, with what VCS they use, or what bug
tracking software, whether they practice BDD/TDD or write tests at all, what
language they use while discussing Ruby over lunch, or any of a myriad other
activities not explicitly defined by the process.


## English Is A Reasonable Language For Collaboration

The proposed design process attempts to reduce as much as possible the need
for all implementers to discuss proposed language features. The discussion
occurs after clear documentation is written, after precise RubySpecs are
written, and after everyone implements the feature so that it passes RubySpec.
The discussions then focus on concrete facts about the impact of the proposed
feature to existing and future code, whether it is in libraries, frameworks,
or applications.

For the limited discussion that is required, English is a reasonable language.
It is the only language that is likely to be used to some extent by all the
Ruby implementations. It is the language used by international communities in
computing, science, mathematics, and other fields.

In fact, English is the language in which the Ruby ISO standard is written.
And that standard was written by MRI Japanese developers.


## The Design Process is Fair

Matz and other MRI developers have put a tremendous amount of effort into the
Ruby language. However, so have all the developers of other implementations of
Ruby. In fact, the combined effort on other implementations of Ruby very
likely far exceeds all the effort dedicated to MRI. Every implementation of
Ruby is helping Ruby and helping Ruby developers.

Most importantly, other implementations of Ruby are helping Ruby developers in
ways that MRI and Matz are not. Furthermore, while Matz may know a lot about
Ruby, he doesn't know everything about the many challenges Ruby faces. Matz is
not a concurrency guy, or a business guy. He's said that himself. He's also
not likely a Java guy, or C# guy, or crypto guy.

The Ruby language needs a design process that fairly distributes authority
over what features become officially Ruby. There is no process more fair than
consensus among all the Ruby implementations. These are people who have
dedicated tremendous effort to understand and implement the many complex
idiosyncratic Ruby behaviors and support developers in many difficult
environments.

If all the implementations believe that a feature is bad for Ruby, Matz should
not ignore their collective wisdom and dedication to Ruby.  The proposed
design process merely formalizes that fact. Finally, if Matz disagrees, he is
still free to include the feature in MRI and demonstrate its importance. The
same is true of every other Ruby implementation.


## A Design Process Is Critical At This Stage Of Ruby's Development

At this stage of Ruby's development, a design process is critical. Point out a
single other widely used programming language with a half-dozen
implementations with a unified definition of the language and no formal
process for agreeing on that definition.

_Ruby has no formal design process, despite Ruby being an industrial strength
programming language, having hundreds of millions of dollars invested in
businesses built around the language. There is no process to maintain unity of
the Ruby language. There is no definitive resource defining Ruby. Developers
can only support multiple Ruby implementations with trial and error._

It is short-sighted and irresponsible to advocate for the ease of
experimenting with random language features over the stability and unity of
the Ruby language. Ruby is not a toy language. It is almost twenty years old.
It powers many businesses and pays tens of thousands of developer salaries.

Matz created the language. His creation has been a gift to the world. The Ruby
community has been and continues to be immensely grateful to Matz and
deferential to his opinions and there is every reason to believe that will
continue. Insisting that one's ownership of a language is paramount at this
stage of its development is unreasonable.

The proposed design process seeks to create these three things:

1. A definition of the Ruby language that is independent of any particular
   implementation of Ruby.
1. A definition of Ruby that is explicit and verifiable by running RubySpec.
1. A process of deciding what features are in the Ruby language that is fair
   to all implementations of Ruby.

If you disagree with those goals, please explain why the goals are not good
for Ruby. If you believe the proposed process would not promote those goals,
please explain why.

If you support the proposed process, please talk to people about it and why
you support it. Also, please [add your voice](http://rubyspec.org/design/) in
support.
