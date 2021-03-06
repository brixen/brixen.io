--- 
title: A Ruby Design Process
layout: post
author: Brian
---

**Ed:** _Since the initial post, I have fixed some minor grammatical and
spelling errors pointed out by Rich Morin._

**Ed:** _If you support the proposed design process, please add your voice by [signing
here](http://rubyspec.org/design/)._

The Ruby programming language needs a design process.

I gave [a talk on this
topic](http://www.confreaks.com/videos/1278-rubyconf2012-toward-a-design-for-ruby)
at RubyConf 2012. While the talk presented reasons why we need a design
process, I'm mostly focusing on my proposal in this post. On Monday, December
10, 2012, we had an [IRC
meeting](https://bugs.ruby-lang.org/projects/ruby/wiki/DevelopersMeeting20121210)
of Ruby implementers. Most of the components of my proposal were discussed.
However, I think a fair amount of misunderstanding remains. With this post, I
hope to offer some clarification.


## Setting a Stage

Once upon a time, a very long time ago, there was a single implementation of
Ruby. Matz was the initial author and over time various people contributed to
the project. We generally refer to this implementation as **MRI** or **Matz's
Ruby Implementation**. Today, there are half dozen significant Ruby
implementations. These cover major platforms from the JVM to a Smalltalk VM to
Microsoft's DLR. Each of these platforms are quite different, having specific
limitations and advantages.

Matz still works on MRI to some extent, which is now only one implementation
out of many. Yet, for many people, MRI is still synonymous with Ruby. In other
words, people generally assume that "the Ruby programming language" and
whatever behavior MRI, the implementation, exhibits are one and the same
thing. However, Ruby is an extremely complex language with many special cases,
a big core library, and an even bigger standard library. For all the other
implementations of Ruby to have consistent behavior, there must be a way to
define _what is Ruby_.

We need a precise standard, or specification, for Ruby.

But wait, didn't I just say that we needed a design process for Ruby? Yes, I
did. A design process is a means to create a precise standard for Ruby. But
there is another reason that we need a design process for Ruby.

The world is constantly changing. As an industry, we have been reading and
hearing about the need to deal with concurrency as CPUs get more cores and
computers get more CPUs since the late 1980's (that's before a lot of
programmers today were born). But it is now becoming an unavoidable reality.
Discussions about concurrency in Ruby usually focus on the MRI global
interpreter lock. Unfortunately, that specific limitation of MRI gets an
unfair share of the attention. Concurrency and potential parallelism are much
bigger topics and need attention. A memory model, thread semantics,
concurrency primitives other than threads, and concurrent data structures are
all topics that must be addressed.

We are also seeing a huge change in the way applications are built and
deployed.  Heterogeneous networks of services deployed in the cloud and
interacting in unforeseen ways is the future. The future is not evenly
distributed but it is already all around us. In this environment, security is
a vital consideration.  Further, an extension API for Ruby to integrate with
libraries and applications written in numerous other languages is essential.
Not everything can be turned into a service natively and writing a service
layer may mean integrating a library or application written in another
language.


## The Great Benefits

It should be wildly uncontroversial that everyone in the Ruby community
benefits from a specification for Ruby. What may be under-appreciated is who
exactly we are referring to when we say _the Ruby community_. My definition is
broad and includes people who use applications written in Ruby, businesses who
use applications written in Ruby, businesses who pay people to write
applications in Ruby, and people who are paid to write applications in Ruby.

Ruby is a mature, industrial-strength programming language. Hundreds of
millions of dollars have been invested in Ruby, Ruby companies, and Ruby
applications. Think about that for a moment. About six years ago, a few
hundred Rubyists attended the first RailsConf. Many of them were not being
paid to write Ruby or Rails applications yet. That's just six years ago.
Today, it is hard to find a person attending a RubyConf or RailsConf or any of
numerous regional Ruby conferences who is not paid to write Ruby. That is a
huge number of families that depend on a salary that comes from writing Ruby
code.

It is incumbent upon all of us who can make a difference to ensure that we
give our best effort to make good decisions for Ruby. Decisions that further
the quality, reliability, security, and usability of Ruby. Decisions that
safeguard the well-being of people that depend on Ruby.


## A Decent Proposal

The foremost goals for this proposed Ruby design process are 1) the _quality_
of decisions made about Ruby, and 2) language unity.

I want this point to be as clear as possible. Ruby is a fantastic language.
It does not need huge changes. What Ruby needs is stability, unity, and
changes that address the challenges for using Ruby to create modern
applications. Wherever this proposed process seems heavy, it has been
_designed_ to produce good decisions and limit Ruby changes.

Here is the proposed process:

1. A _Ruby Design Council_ made up of representatives from any significant
   Ruby implementation, where significant means able to run a base level of
   RubySpec (which is to be determined).
1. A proposal for a Ruby change can be submitted by any member of the Ruby
   Design Council. If a member of the larger Ruby community wishes to submit a
   proposal, they must work with a member of the Council.
1. The proposal must meet the following criteria:
    1. An explanation, written in English, of the change, what use cases or
       problems motivates the change, how existing libraries, frameworks, or
       applications may be affected.
    1. Complete documentation, written in English, describing all relevant
       aspects of the change, including documentation for any specific methods
       whose behavior changes or behavior of new methods that are added.
    1. RubySpecs that completely describe the behavior of the change.
1. When the Council is presented with a proposal that meets the above
   criteria, any member can decide that the proposal fails to make a case that
   justifies the effort to implement the feature. Such veto must explain in
   depth why the proposed change is unsuitable for Ruby. The member submitting
   the proposal can address the deficiencies and resubmit.
1. If a proposal is accepted for consideration, all Council members must
   implement the feature so that it passes the RubySpecs provided.
1. Once all Council members have implemented the feature, the feature can be
   discussed in concrete terms. Any implementation, platform, or performance
   concerns can be addressed. Negative or positive impact on existing
   libraries, frameworks or applications can be clearly and precisely
   evaluated.
1. Finally, a vote on the proposed change is taken. Each implementation gets
   one vote. Only changes that receive approval from all Council members
   become the definition of Ruby.


### 1. A Ruby Design Council

A council of people with many different and sometimes competing interests has
been used at every level of government and organizations to ensure that
different viewpoints are considered and reasonably good decisions are made.

A council is the only equitable way to ensure that the definition of Ruby
fairly considers all the competing interests that exist. If the process is not
equitable, it will not be respected. The unity of the Ruby language is
something of tremendous value to the Ruby community.


### 2. Submitting a Proposal

I must emphasize that the proposal is not where the process of working on a
Ruby feature begins.

Any implementation is free to experiment with Ruby changes in any way they
choose and using whatever testing or coding style they select. They are free
to discuss the process in any forum using any language they choose.

Writing code and playing with it is one of the main ways to get a feel for a
feature. The design process proposed here does not intend to interfere with
that. It is also expected that discussions and collaboration between different
Council members would be undertaken long before a proposal is submitted.

Ruby is a very complex language. Changes to Ruby should not be considered
lightly. Ruby is not a playground. It is a language that has a responsibility
to a huge community.

Requiring that a proposed change be made by a Council member ensures that
poorly fitting changes are not added to Ruby. At the same time, any change
that has a clear and significant benefit deserves the effort to be presented
in a way that ensures it will be understood by the Council members and taken
seriously.


### 3. Criteria for a Proposal

Proposing a change to Ruby is not a trivial undertaking. It should be
deliberate and carefully thought out. It is not an unreasonable burden to
require that a proposed change be completely understood by the member
proposing it.

Writing documentation and RubySpecs is the best way to ensure that the
proposed change is understood and can be communicated to the rest of the
Council. Since the goal is the best decisions we can make for Ruby, setting a
high expectation for a proposal is a benefit.


### 4. Proceeding with a Proposal

Any proposed change that has met these criteria has been carefully thought out
and described. The specific details of behavior have been written down in a
way that any implementation can implement.

However, that does not mean the proposal is a good idea for any number of
possible reasons. As an initial sanity check, all Council members must decide
whether the effort to implement the feature is justified. This barrier should
be viewed as an additional guarantee that changes to Ruby will be adequately
understood and carefully selected for the benefit of the Ruby community.


### 5. Implementing a Proposal

Every Council member must implement a proposal that passes the initial
evaluation. The RubySpecs provided in the proposal will guide and clarify the
implementation.

Confronting the platform and system constraints while implementing the feature
ensure that it is completely understood. Likewise, having a complete and
working implementation is the best way to limit unintended consequences and
understand as much as possible how existing code will be affected by the new
feature.


### 6. Discussing the Implementation

Once the proposal has been implemented by all Council members, the time is
ripe for discussion. It is only with the concrete reality of how the feature
performs and interacts with the rest of Ruby that good decisions can be made.

The express intent of all Council members is to implement a _unified_
definition of Ruby. If the feature is going to be Ruby, it is going to be
implemented by all members. It presents no burden to require that the
implementation precede the discussion. If, after implementation, the feature
fails to meet the needs that motivated it, everyone can be satisfied that the
best possible evaluation was given. If unforeseen implementation issues are
discovered, the feature can be revised and resubmitted.


### 7. Voting on a Proposal

Just as a council is the equitable way to share responsibility and decisions
about Ruby, so it must be that every Council member's vote has equal validity.
It is true that every Council member holds veto power. But that should be seen
as a strength of the process, not as a liability.

Matz still has the ability to say what features become officially Ruby. He can
exercise his vote to not approve any feature. However, the rest of the Council
could also vote not to approve a feature that Matz wanted. If this causes the
slightest bit of fear for the well-being of Ruby, please allow me to dispel
it.

First of all, the Council is made up of people who have spent _years_
implementing Ruby. Many of those people spend some of their time as unpaid
volunteers. Every one of those people up to now has committed tremendous
effort to create a compatible implementation of Ruby _even when no actual
specification existed_.

Furthermore, people like Charles Nutter have gone to tremendous lengths to
implement features like POSIX-compatible behavior on top of the JVM so that
Ruby compatibility would be respected. That level of dedication must be
respected and applauded, not feared. We have all put the well-being of Ruby
first, and if we truly feel that a feature would cause harm to Ruby, we should
be allowed to prevent it from being included in the definition of Ruby.

In practice, I have absolutely no reservation about giving veto power to any
member of the Ruby Design Council.


## What Really Changes?

By formalizing a design process for Ruby, what really changes about how we do
our work?

Nothing in this proposal prevents any implementation, including MRI, from
experimenting with Ruby features. Any, or all, of the Council members could
collaborate on a proposed change to Ruby. An experiment for a new feature
could be used by a portion of the Ruby community for a significant period of
time before being formally included in Ruby. Any implementation is free to
discuss a feature in their own way and with their own preferred version
control system, bug tracker, testing methodology, means of communication and
language.


## Technology for Change

Finally, the question of what technology to use for submitting, discussing,
tracking, and voting on proposals must be addressed.

Email is not sufficient and neither is a bug tracker. We need an application
that allows commenting on each sub-section of a proposal, referencing multiple
previous comments in a comment, viewing comments by proposal or by
sub-section, tracking changes to a proposal, tracking references to RubySpecs
and implementation code, and recording votes. The contents of proposals should
be searchable and indexable. The process of deciding on proposals should be
secure and audit-able.

I will create a specific application for this purpose and host it at
[design.rubyspec.org](http://design.rubyspec.org). Ruby deserves a
sufficiently powerful tool to support making good decisions for the language.

## Conclusion

Ruby needs a design process. The process described here focuses on language
unity and making good decisions for the Ruby community. The process gives
maximum liberty to all implementations of Ruby to experiment with new features
while giving maximum clarity and support for the Ruby Design Council members
to decide which proposed Ruby changes to accept.

We can choose to make the Ruby design process as efficient and effective as we
wish. The intention should be collaboration and unity. Ruby, and especially
the Ruby community, deserve our best effort.
