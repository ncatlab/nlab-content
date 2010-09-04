+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Contents### {: .clickToReveal}
###Contents### {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include contents]]
=--
=--
=--


If you have any material you'd like to add to the [[HomePage|nLab]], be it

* a tiny correction,
* a major correction,
* a missing aspect,
* a missing topic,
* a missing reference,

or whatever, _please do it_. It's quick and easy. 

The following gives you a quick idea of how to proceed. 

If you feel you can most easily start by modifying an example, look at the [[template page]].

If you feel you want more details, there is more information on the main [[HowTo]] page.


## Don't worry too much! ##

First a remark on what **not to worry** about.

+-- {: .un_remark}
###### No need to be perfect in the first go

Don't worry if things don't come out quite the way you would like them at the first go &#8211; the important point is that we have your material in some form - the [[lab elves]] will eventually go over the entry and polish it, if necessary, expand it, if necessary, etc.
=--

+-- {: .un_remark}
###### No need to worry about breaking anything

Never worry about "breaking" or "ruining" anything. Each and every revision is stored and we can always "Rollback" to an earlier version if you make some mistake, e.g. delete material on accident. To see a list of revisions for any page, hit the "History" link at the bottom of any page.
=--

+-- {: .un_remark}
###### Learn by example

A good way to learn about how to format $n$Lab pages is to look at the source of another page.  Near the bottom of each page is a list of "views" (these are different displays of the page) one of which is "source".  This shows the raw code that generates that page and can be cut-and-pasted into another page.

See the [latest changes](http://www.math.ntnu.no/~stacey/Mathforge/nForum/?CategoryID=5) to get an impression for what other contributors are working on currently.
=--


## Forwarding your blog comment to the $n$Lab ##

Chances are that you are already familiar with discussions and with posting comments at the [n-Cafe](http://golem.ph.utexas.edu/category/). This section describes how you forward material from a blog comment to the $n$Lab. 


After you typed your blog comment into the [n-Cafe](http://golem.ph.utexas.edu/category/) comment edit box and **before** you hit submit copy the **source code** of the comment: the text that you just typed.


To paste that into an $n$Lab page, note the "Edit" link at the bottom of each $n$Lab page.

<img src="http://ncatlab.org/ericforgy/files/edit.jpg" width = "500"/>

Clicking on this will bring up the edit box.

<img src="http://ncatlab.org/ericforgy/files/editbox.jpg" width = "500"/>

From here, you simply paste your copied content into the edit box and hit the "Submit" button at the bottom. 

Putting your name in the text box next to the "Submit" button is optional but recommended.

This works best if your original comment was composed using the text filter (see the pulldown menu atop the blog comment edit box) called _Markdown with itex to MathML_.  If you're writing a lot on the Caf&#233; and want to write on the Lab too, then it may be wise to use that filter by default.


## Copying material from elsewhere on the web into the $n$Lab ##

If you wish to copy into the $n$Lab a blog comment _after_ it has been posted -- or if you wish to copy other material from elsewhere on the web --, you proceed as above but should be aware of two dangers: 

* cutting-and-pasting from what is on the _screen_ will result in much of the formatting being lost, 
* and what happens to any non-standard characters will depend on a variety of factors (they may come out as unicode characters, they may get converted to the nearest alternatives in your charset).  

Slightly better is to copy the `XHTML+MathML` source (in _Firefox_ : "View" followed by "Page Source") except that then you are pasting raw `XHTML` into the $n$Lab.  Whilst this will work, it makes it harder to others to edit afterwards.  (But a [[lab elf]] will probably come by to clean it up afterwards, so don't worry about this too much.)


## OPTIONAL -- how to place your material in context ##

If you do feel like going a bit further, here are some remarks on how to make your material interplay nicely with the whole structure.
  

### Use Google to check for existing content ###

If you don't know where to put your material, Google for "nLab your keywords" to see which entries exist. Better yet, you can Google 

* [your keywords site:http://ncatlab.org/nlab](http://www.google.com/search?q=your+keywords+site%3Ahttp%3A%2F%2Fncatlab.org%2Fnlab)

and it will look for only keywords on the $n$Lab.  (Most other search engines can do similar tricks.)


### Create a new entry by creating a link to it ###

If the entry with the title that you are looking for does not yet exist, find some entry that is somehow related, go to the edit window as described above and add a line "see also <nowiki>[[your keyword]]</nowiki>". Then after hitting submit the <nowiki>[[your keyword]]</nowiki> will appear with a clickable question mark. Click on that question mark to create the desired entry.


### Cross-link your material ###

Add links back and forth between other [[HomePage|nLab]] entries: enclose important keywords in your material in double square brackets <nowiki>[[your keyword]]</nowiki>. That equips them with links to the corresponding other $n$Lab entries. Conversely, go to related $n$Lab entries and add pointers to the entry you just created.


### Insert a link to the $n$-Caf&eacute; discussion ###

Depending on the kind of material you included, you may feel like adding a reference back to the $n$Caf&eacute; discussion.

The first thing to do that is to get a copy of the $n$Caf&eacute; link, which may be obtained via "permalink" at the bottom of the comment.

<img src="http://ncatlab.org/ericforgy/files/permalink.jpg" width = "500"/>

The link to this comment on the $n$Caf&eacute; is:

    http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025514

To add a link with the label "Link to the $n$Caf&eacute;", you need a combination of square brackets and parentheses <nowiki>[Link Name](Link URL)</nowiki> as indicated below:

    [Link to the n-Cafe](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025514)

This results in a [Link to the n-Cafe](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025514).


### Log your changes ###

In order that the rest of the $n$Lab crew has a chance of becoming aware of your changes, drop a note about what you did at [latest changes](http://www.math.ntnu.no/~stacey/Mathforge/nForum/?CategoryID=5).  Click on "Start a new discussion," enter a descriptive title, and then describe the changes you made.  Please include a link to the page(s) you edited; the same link syntax `[[page name]]` to nlab pages works on the "latest changes" forum.  You'll have to either create an account at the forum, or reply to a captcha in order to post as a guest.  For more detailed instructions, see the sticky post at the top of the link.


### Pat yourself on the back ###

Congratulations!  By helping the $n$Lab, you have done your good deed for the day.  All glory comes from daring to begin.

***

For more information, try the [[nlab:HowTo|HowTo]] page.


[[!redirects How to Copy and Paste Material from the n-Cafe and Include Links Back and Forth]]
[[!redirects How to Copy and Paste Material from the n-Cafe and Include L]]

category: meta