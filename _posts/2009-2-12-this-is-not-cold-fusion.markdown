--- 
title: This is NOT cold fusion
layout: post
---
Um, whoops. It was really late last night. Have I mentioned you're wearing a great outfit today. Ok, already.

There's this slight matter of `DEV=1 rake build` in Rubinius. Yes, I was debugging something. Started running some stuff under the stackfull branch, was intrigued by what I was seeing, decided to make some comparisons, could swear I ran <code>rake clean; rake</code> in the master branch, had a lot of green tea yesterday...

*All right already*. It's not 4x faster. Here's some new numbers:

Master branch:

<pre style="overflow:auto">
$ bin/mspec ci core/string
rubinius 0.10.0 (ruby 1.8.6) (781eb14d3 12/31/2009) [i686-apple-darwin9.6.0]
.....................................................................

Finished in 10.576468 seconds

69 files, 763 examples, 5632 expectations, 0 failures, 0 errors

</pre>

Stackfull:

<pre style="overflow:auto">
rubinius 0.10.0 (ruby 1.8.6) (325174a8e 12/31/2009) [i686-apple-darwin9.6.0]
..................E.....E...E...F............E..E.EE..E........F..F..

Finished in 6.124444 seconds

69 files, 763 examples, 5545 expectations, 6 failures, 19 errors
</pre>

That's about 58% as long, or 42% faster, or creeping up on 2x. 

If you rushed out and bought Evan a Valentine's bear, I do apologize. But send
it anyway. All the rest in my [previous post](/2009/2/12/all-shiny-and-new) about this being the beginning of a very good thing still holds. We'll be getting more results soon and fixing the spec breakage on the stackfull branch. Stay tuned!
