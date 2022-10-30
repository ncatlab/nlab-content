
If you think you have worthwhile material to add to the [[HomePage|nLab]], be it

* a tiny correction

* a major correction

* a missing aspect

* a missing topic

* a missing reference

or whatever, _please do it_ . It's quick and easy. 

The following gives you a quick idea how to proceed. 

If you feel you want more details you can still consult the main [[HowTo]] page.

# Don't worry, just go ahead and add your material #

First a remark on what not to worry about.

## no need to be perfect in the first go ##

  Don't worry if things don't come out quite the way you would like them at the first go &#8211; the important point is that we have your material in some form - others will eventually go over the entry and polish it, if necessary

## no need to worry about breaking anything ##

  Never worry about "breaking" or "ruining" anything. Each and every revision is stored and we can always "Rollback" to an earlier version if you make some mistake, e.g. delete material on accident. To see a list of revisions for any page, hit the "History" link at the bottom of any page.

## learn by example ##

     A good way to learn about how to format $n$Lab pages is to hit the "Edit" button on an existing page, look at the content and see how it is written, then hit "Cancel". There will be no record that you ever hit "Edit".


#Copying and Pasting Material from an $n$Cafe#

Chances are that you are already familiar with discussions and with posting comments at the [n-Cafe](http://golem.ph.utexas.edu/category/). Then this section is for you.

When you write a comment on the [n-Cafe](http://golem.ph.utexas.edu/category/), most of the formatting will carry straight over to the n-Lab with little need for modification. This is true even for <nowiki>LaTeX</nowiki> content (which is actually [itex](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html), but that is not important). So all you really need to know to get started is how to paste material to the nLab.

+-- {: .query}
[[Bruce Bartlett|Bruce]] (_This is true even for LaTeX content_). Hold on, that's not quite true, isn't it? Copying to the clipboard gives you a bunch of Unicode characters on the clipboard, and then pasting it into the nLab indeed recovers back the math, but in "text mode" which can be a hassle later on if (a) someone wants to edit an equation or (b) or if you'd like to see the math displayed in math font, not in text font. Not really a biggie, I know, but it would be nice to have a "Copy as iTex" button at the bottom of the n-category caf&#233; posts.

[[Urs Schreiber]]: the above is about taking the _source code_ that you'd post to a blog entry and copy-and-paste that here. If the blog post chooses the _markdown_ textfilter the blog comment source code should go through here unmodified

should that clarify the issue, please make the corresponding  emphasis in the above paragraph and then remove the query box here (this page is to help people, not to confuse, we want to get rid of query boxes here)

=--

To do this, note the "Edit" link at the bottom of each page.

***
<img src="http://ncatlab.org/ericforgy/files/edit.jpg" width = "500"/>
***

This will bring up the edit box.

***
<img src="http://ncatlab.org/ericforgy/files/editbox.jpg" width = "500"/>
***

From here, you simply paste whatever content you want into the edit box and hit the "Submit" button at the bottom. Putting your name in the text box next to the "Submit" button is optional.

#Inserting a Link to the n-Cafe#

The first thing you want to do in order to insert a link on the n-Lab that points to the n-Cafe is to get a copy of the n-Cafe link.

***
<img src="http://ncatlab.org/ericforgy/files/permalink.jpg" width = "500"/>
***

The link to this comment on the n-Cafe is:

<blockquote>

http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025514

</blockquote>

To add a link with the label "Link to the n-Cafe", you need a combination of square brackets and parentheses <nowiki>[Link Name](Link URL)</nowiki> as indicated below:

<blockquote>

<nowiki>[Link to the n-Cafe](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025514)</nowiki>

</blockquote>

This results in a [Link to the n-Cafe](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025514).

#Additional Comments#



## OPTIONAL: how to place your material in context ##

  if you do feel like going a bit further, here are some remarks on how to make your material interplay nicely with the whole structure
  
### use Google to check for existing content ###

If you don't know where to put your material, Google for "nLab [your keywords]" to see which entries exist. Better yet, you can google 

* [your keywords site:http://ncatlab.org/nlab](http://www.google.de/search?hl=de&client=firefox-a&channel=s&rls=org.mozilla%3Ade-DE%3Aofficial&hs=EwF&q=category+site%3Ahttp%3A%2F%2Fncatlab.org%2Fnlab&btnG=Suche&meta=) 

and it will look for only keywords on the $n$Lab.


### create a new entry by creating a link to it ###

  If the entry with the title that you are looking for does not yet exist, find some entry that is somehow related, go to the edit window as described above and add a line "see also <nowiki>[[your keyword]]</nowiki>". Then after hitting submit the <nowiki>[[your keyword]]</nowiki> will appear with a clickable question mark. Click on that question mark to create the desired entry.

### cross-link your material ###

  if you want to be sophisticated: add links back and forth between other [[HomePage|nLab]] entries: enclose important keywords in your material in double square brackets <nowiki>[[your keyword]]</nowiki>. That equips them with links to the corresponding other $n$Lab entries. Conversely, go to related $n$Lab entries and add pointers to the entry you just created.



***

For more information, try the [[nlab:HowTo|HowTo]] page.


[[!redirects How to Copy and Paste Material from the n-Cafe and Include Links Back and Forth]]
