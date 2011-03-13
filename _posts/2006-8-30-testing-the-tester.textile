--- 
title: Testing the tester
layout: post
author: Brian
---
I recently wrote about the [assert_cookie](http://blog.brightredglow.com/articles/2006/08/27/assert_cookie-for-ooey-gooey-fun) custom test assertion plugin I put together. When I started writing the assertion, it was just a helper method to wrap up the funky logic for testing stuff about a cookie. I wasn't thinking about tests. And my first tries were definitely not test-driven.

When I was wrapping it up as a plugin, this started bugging me a lot. Especially because my first tries at the assertion method weren't very good. (Ugh! `svn diff -r59:72 http://svn.planetargon.org/rails/plugins/assert\_cookie/lib/assert\_cookie.rb`) But the idea of testing it was confounding. How do you think about testing the tester?

The first thing I had to get straight was what I expected. It basically reduced to expecting the assertion to pass or fail. When an assertion fails, it raises the `AssertionFailedError` exception. Excellent, now I was making progress.

I started writing tests like:
{% highlight ruby linenos %}
def test_assertion_cookie_is_secure_should_pass_when_cookie_is_secure
  assert_nothing_raised { assert_cookie :secret, :secure => true }
end

def test_assertion_cookie_is_secure_should_fail_when_cookie_is_not_secure
  assert_raise(AssertionFailedError) { assert_cookie :open_secret, 
      :secure => true }
end
{% endhighlight %}

and notices a lot of repetition of `assert\_raise(AssertionFailedError)` and `assert\_nothing\_raised`. It was ugly to read. I decided to write a couple helper assertions:
{% highlight ruby linenos %}
def assert_pass
  assert_block("assert_pass must be called with a block.") { block_given? }
  yield
end

def assert_fail
  assert_block("assert_fail must be called with a block.") { block_given? }
  yield
rescue AssertionFailedError
end
{% endhighlight %}

The hard part again was figuring out what I was expecting. My first try was to use `assert\_raise` and `assert\_nothing\_raised` as before. But those failed miserable because they call `yield`. I lamented to [Andrew](http://www.stopdropandrew.com/) that I wished `yield` would work like `raise`. After thinking a bit more, I realized I only cared whether an `AssertionFailedError` exception was raised or not. The previous tests now look like this:
{% highlight ruby linenos %}
def test_assertion_cookie_is_secure_should_pass_when_cookie_is_secure
  assert_pass { assert_cookie :secret, :secure => true }
end

def test_assertion_cookie_is_secure_should_fail_when_cookie_is_not_secure
  assert_fail { assert_cookie :open_secret, :secure => true }
end
{% endhighlight %}

There is one last thing that bugs me. I wanted the tests to run outside of Rails but function correctly in Rails. Rails adds a method to `Test::Unit::Assertions` called `clean\_backtrace`. I couldn't figure out how to get that required correctly, so I created a stub in `test\_helper.rb`. Can anyone help me fix this?

Install the plugin with `script/plugin install http://svn.planetargon.org/rails/plugins/assert_cookie`. Navigate to the `vendor/plugins/assert_cookie` directory, type `rake` and watch the tests run. :)
