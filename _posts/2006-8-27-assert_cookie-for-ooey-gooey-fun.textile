--- 
title: assert_cookie for ooey gooey fun
layout: post
author: Brian
---
I love cookies. There are, of course, tons of varieties and I'm no connoisseur but I love the soft chocolate chip right out of the oven, hot and gooey. But, if you're like me, you don't want your Rails code to be gooey. 

Last Friday, after spending a good frustrating hour trying to figure out why my tests were failing with a nil when a cookie was expected, I finally tried a google search for "assert cookies". (A lot of more detailed searches pulled up nothing but Java stuff, a not-so-subtle reminder that Ruby is not yet the dominant language out there.) Seems that [Pluit Solutions](http://www.pluitsolutions.com/2006/08/02/rails-functional-test-with-cookie/) ran into the same problem. This got me thinking that a nice custom assertion might be in order. Actually, I just wrote a quick helper because that was faster than trying to figure out why Rails wasn't performing [as advertised](http://api.rubyonrails.com/classes/Test/Unit/Assertions.html). But it kept bugging me, so I wrapped it up as a plugin. It's still rough and tests are coming. Perhaps I'm putting too much into a single assertion. Install it with `script/plugin install http://svn.planetargon.org/rails/plugins/assert_cookie`. And please send feedback.

The idea is to allow various assertions about cookies using a hash of arguments. In particular, you can do such things as:

<pre><typo:code lang="ruby">
assert_cookie :pass, 
    :value => lambda { |value| UUID.parse(value).valid? }
assert_cookie :yellow, :value => ['sunny', 'days']
assert_cookie :delight, :value => 'yum'
assert_cookie :secret, :path => lambda { |path| path =~ /secret/ }, 
    :secure => true
</typo:code></pre>
