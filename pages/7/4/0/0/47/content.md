# General Discussion #

Here we should brainstorm ideas about how to use the $n$Lab and how it should work. It's not the $n$_Wiki_, it's the $n$_Lab_, and we need to work out what that means.

-----------------------

#### Embedding questions about unclear text via abbreviation tags?

Bruce Bartlett says: Take a look at what I did at [[integration over supermanifolds]]. I'm using the hovertext feature to embed a question over the phrase "since odd graded differential 1-forms, being of total even degree, do not have a top exterior power"... if your mouse lingers over this. Maybe this is an idea?

Urs Schreiber says: That's a great idea! I have replied to your question in that entry now (check it out!) which means that the mouse-over effect is currently no longer visible (it still is present in the source code there, so everybody can check how this works: where did you leanr about this feature??), but let's consider sticking to that kind of inserting questions.


#### Slash lab entries?

_Bruce Bartlett says:_ I have the vague idea that mathematical entries (like [[integration over supermanifolds]] should have a "/lab" section where "lab" things get done, like a tutorial class. I don't know what that means.

_Urs Schreiber say:_ I don't know either! We are likely to have entries of very different nature, some of them just reviewing very standard stuff, some summarizing less well-known stuff, and in some areas we may want to think about new stuff, even. I think as long as every single page makes clear where the information presented there comes from, everything is okay.


#### Single-Author Areas ####

Instiki can run multiple Wikis ("Webs" in the Instiki Parlance). Urs, John and David have the password required to create additional Webs.

* Webs can be password-protected, so that only those in posession of the password can edit them.
* A password-protected Web can be "published" so that others can read, but not edit, the contents. (Or, of course, they can remain unpublished, so that the authors can carry out their *super sekrit* machinations in private).

These two features provide the possibility for single-author areas, where one person (or persons: whoever has the requisite password) is in authorial control.

Here is [[baez:HomePage|John's area]].

#### Importing CSS ####

I propose that, at least in these early days of the $n$Lab, that the CSS style sheet be tweakable by everyone. I propose the following mechanism to do this.

Here is a publically editable CSS file: [general.css](http://ncatlab.org/nlab/files/general.css). I want the stuff in here to piggyback onto the existing CSS declarations in instiki.css (as can be found by clicking on "Edit Web" on the main page).


Basically, one just needs to add the following line to the beginning of that file: 

    @import url('/nlab/files/general.css');

{:response: style="color:#930; font-size:0.9em;margin-left:2em;"}

{:response}
**Not a chance**. That would be a *completely unacceptable* security risk.

That way everyone is free to make some tweaks. The point is that Markdown has a nice CSS trick, which [Jacques used to create the Theorem environments ]([http://golem.ph.utexas.edu/~distler/blog/archives/001820.html). The idea is that if one types eg.

    +-- {: my_gismo}
    Some text here.
    =--

then one gets a div element whose class is "my_gismo". So in the CSS file general.css, we can style this block anyway we want.

{:response}
If that's all you want to do, you don't need access to the site's CSS file. You can use a combination of [Maruku's metadata format](http://maruku.rubyforge.org/proposal.html) and the `style` attribute to style your responses. (See the Markdown source of this page, to see how it's done.) Inline styles are [sanitized for your protection](http://golem.ph.utexas.edu/~distler/blog/archives/001181.html).

{:response}
I see that you've already noticed the existence of Maruku's metatdata format, though your example is slightly incorrect.

For instance, I created a "query" block, which I'm using to ask questions on Urs's pages (beware I will use it on _yours_ soon dear reader!). See [[integration over supermanifolds]]. (The query block will only display as green once that adjustment I suggested is made to the instiki.css file by someone with a password by clicking on Edit Web and then Stylesheet tweaks, to change the instiki.css file)

{:response}
More generally, for changing the overall look-and-feel, it would be nice to introduce theme-support for Instiki, just as we already have theme support for [slide shows](http://golem.ph.utexas.edu/instiki/show/S5) within Instiki.

Trying to reupload the general.css file: [[general.css:file]]

Darn, I was worried it might not work. Darn, that causes problems. This is a silly thing about Instiki --- you can't replace uploaded files with new ones. Jacques? Any suggestions?

{:response}
An interface for managing uploaded files is another item on the [TODO list](http://golem.ph.utexas.edu/instiki/show/TODO).

Yes you're right --- thanks. [[Bruce Bartlett]]

## Formatting of discussions##

{:commenturs: style="color:#040; font-size:0.9em;margin-left:2em;"}

{:commenturs}
_Urs Schreiber says:_ We need to do something about this: it is already becoming hard to recognize, read, let alone follow the flow of discussions. 

{:commenturs}
Let's agree on some kind of basic formatting rules for how to type personal speech here and, in particular, as comments into the other entries. I like Jacques' way of formatting his comments above. Maybe everybody should choose his or her color and then always insert comments using this kind of formatting with this kind of color.

{: style="color:#930; font-size:0.9em;margin-left:3em;"}
_Jacques says:_ I hope you don't mind, but I darkened the colour of your response. Bright green is hard on the eyes, when it occurs in large blocks of running text. Besides, it's the colour of hyperlinks on this wiki, which is a little confusing.

{:commentbruce: style="color:darkblue; font-size: 90%; margin-left:2em;"}


+-- {: commentbruce} 
_Bruce Bartlett says:_ Ok... that's a bit of a weird system for discussion, but I'm okay to go along with it... However, I'm quite fond of the green "query" block that I put on [[integration over supermanifolds]], as below:
=--

{:query: style="background: #f6fff3; border: solid #ce9; border-width: 2px 1px;	padding: 0 1em; margin: 0 1em;" }

+-- {: .query}
_Question:_ Okay, but what is the _differential $d\theta_1$ of an odd co-ordinate function_? How are we to think of it geometrically? Does it measure a rate of change of something? (Bruce Bartlett)

_Answer:_ See [[differential forms on supermanifolds]]. (Urs Schreiber)
=--

+-- {: commentbruce} 
I think that a lot of people (for instance Simon) maybe aren't that keen on writing stuff for the $n$Lab right at this moment, but certainly have a lot of questions about Urs's stuff. I see this query feature as a way for them to get involved. Place query blocks all over Urs's text :-) (sorry Urs!) 

I see these query blocks as staying on the page for a while (even after they are answered by Urs or someone else), because it makes people feel better when they see that they are not the only ones who didn't understand the material. At some point they can be taken down on any given page.

However, I would really like it if some of this CSS code would go directly into  instiki.css, instead of us having to reproduce it on each page. That is not a workable solution.

Thus I propose the following: if anyone has some CSS code that they would like to promote, email it to someone with a password (Urs, John, David, Jacques) and ask them to put it in via the "Edit Web" button.

+--{: response}
*Jacques said:* I agree. Once people have settled on a particular styling convention for content, it should go in the "Stylesheet Quirks" section of the "Edit Web" page, where it will automatically be reproduced on every page of this Web. Technically, that's *not* the `instiki.css` file. The latter is common to all instiki installations.

My point was that experimentation on this front does not require access to the site-wide stylesheet, since Instiki provides a convenient way to specify inline styles on a per-page, or per-element basis (as demonstrated here).

Please settle on something that everyone likes and the (and only then) add it to the Site-wide "Stylesheet Tweaks".
=--

I'm quite fond of messing around with colours, etc. and without this feature I feel a bit deflated :-)

For instance, I think it would be great to use CSS so as to style downloadable documents correctly, as [explained here](http://reference.sitepoint.com/css/css3attributeselectors). The idea is that every pdf link will have a tiny pdf icon next to it, and more importantly every n-category cafe link will have a tiny n-category cafe logo next to it; the same for arXiv links, etc.

Another thing I'd like to try in CSS is to set Georga (a serif font) as the main text (and math) font for the $n$Lab. Try it for a few days and see. 

=--


+-- {: commenturs}

_Urs says_: Bruce, I like the look of those query boxes. Graphical sophistication like that greatly improves the look-and-feel of the wiki.

You should explain at some promint point of the wiki, probably at the [[HowTo]] page what people need to do to insert such gadgets. 

Concerning contributions by others: let's see how it develops. I'd really enjoy having several people contributing here, eventually. But on the other hand it is also maybe good if we as the hosts have a bit of time to produce some context here first. 

I am hoping that eventually I will produce enough nonsense here that others can't stand it anymore and jump in to help out ;-)

Seriously, if it turns out that a few of us produce most of the content but many others contribute many little improvements, like correcting small mistakes, adding references, asking for clarifications or voicing other requests, establishing cross-links, etc., I'd already be happy. 

Toby Bartels is currently doing this already, which is great.

=--

+-- {: commentbruce}

_Bruce says:_ Okay. Yes I agree with you about the content; for a while the site will be dominated by you putting up your stuff on $L_\infty$ integration, etc.  But that's great, that serves a very valuable purpose. It creates a central repository of _expository_ stuff (note expository... it musn't be written in an encyclopeadic way... that's important I think). Then when you make a post at the n-category cafe, you can refer to this stuff. 

=--

+-- {: commenturs}

_Urs says:_ I am not sure about that thing about me "dominating" the site. I'll expect that as soon as John posts his first marvelous exposition things will change rapidly. So far I mainly invested energy to provide pages for all the keywords I just used in [this](http://golem.ph.utexas.edu/category/2008/12/zhu_on_lies_second_theorem_for.html) blog post.

For me that's one of the points of having this wiki here: that we establish a stable resource where we can refer to in entries without having to rehash all old disacussions in every new entry.


And in any case, one point about the wiki as opposed to the blog is also that there is no "title page" which can be dominated, but every reader is free to follow whichever way he prefers through the site, and ignore the content he or she is not interested in.


Concerning expository versus encyclopedic: I want both. In the best of all worlds each page is structured roughly similarly, with a section "basic idea" at the beginning, an expository part in the middle, and a concise and comprehensive list of the main definitions and facts at the end. Or the like.

But, you know. This requires work. And time. We'll get there.

=--

+-- {: commentbruce}
_Bruce says:_ Ok I've uploaded the new stylesheet tweaks. Now if you link to an arXiv, n-category cafe, pdf, or a _page_ inside a pdf file, a little icon will appear, like this:

 [arXiv link](http://arxiv.org/abs/q-alg/9503002), [n-category caf&#233; link](http://golem.ph.utexas.edu/category/2008/11/tom_leinster_in_the_reasoner.html#c020641), [pdf file](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf), [_page_ in pdf file](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf#page=4). 

If you _don't_ want that icon to appear (I can imagine a number of reasons why not), there is a temporary workaround: capitalize one of the important letters:

 * For pdf and page-in-pdf files, capitalize something in "pdf".
 * For n-category cafe files, capitalize something in "http://golem.ph.utexas.edu/category".
 * For arXiv links, capitalize something in "http://arxiv.org/".

Also, the query box is now in the stylesheet. If you want to make a query box, just type

    +-- {: .query}

    _Question_: Why did the chicken cross the road?

    =--

in the text and you'll get out:

+-- {: .query}

_Question_: Why did the chicken cross the road?

=--

=--

## Categories

{:commenttoby: style="color:indigo; font-size: 90%; margin-left:2em;"}
+-- {: commenttoby}
Those of you writing here must have noticed it, but I've put little category tabs at the bottom of some pages (such as this one). The first one was category\: people, put on [[Jacques Distler]] by Jacques himself, and I just followed that. I think that the categories are self explanatory; you can find them all from the 'All Pages' link (or click on 'category\: meta' below).

I've just created category\: redirect and trying to apply a few [naming conventions](http://golem.ph.utexas.edu/category/2008/11/nlab.html#c020626). Let me know (say with a query comment [[Toby Bartels|here]]?) if I do anything wrong.

Anyway, in the future, it may be useful also to have content-related categories, but that may want to wait until we know better what the shape of the content here will be.

&#8212;Toby
=--

+-- {: query}

I've noticed on several pages that some links have been created with partial words highlighted, e.g. [[coalgebra|coalgebra]]ic, endo[[functor]], etc. When I see that, my brain instinctively flashes a warning sign and I am tempted to "fix" it by replaing the partial highlights with [[coalgebra|coalgebraic]], [[functor|endofunctor]], etc. Is this by design? Would anyone object to my "fixing" it? Just curious... [[Eric Forgy|Eric]]

{: response}
I presume your fix is to replace <nowiki>[[coalgebra]]ic</nowiki> with <nowiki>[[coalgebra|coalgebraic]]</nowiki>. The latter produces the desired "[[coalgebra|coalgebraic]]" link, instead of the bizarre-looking "[[coalgebra]]ic". If so, I say: go ahead. <br/>&mdash;[[Jacques Distler]]

{:commenttoby}
I produce such links purely out of laziness. By all means fix them (as Jacques describes). &#8212;Toby
=--

## Naming conventions

+-- {: commenttoby}
I talked with Urs about naming conventions [here](http://golem.ph.utexas.edu/category/2008/11/nlab.html#c020626). To be complete, here are the naming conventions that I propose (and which I have, for now, imposed on every page currently in the wiki):
* Page titles should be nouns. If you want an adjective that normally modifies the same noun, then use the entire noun phrase. If you want an adjective that applies to many different contexts, then try adding '-ness' to make a noun. If you want a verb, then try adding '-ing' or '-ation' to make a noun (example: [[categorification]].
* Page titles should be uncapitalised, except for word words that are always capitalised. (Examples: [[light mill]], but [[Lie algebra]].)
* Page titles should be singular, unless the phrase usually occurs in the plural (so effectively a mass noun or a collective noun, rarely if ever referring to individuals). Examples: [[Lie groupoid]], but [[Lie's three theorems]].
* Titles should follow standard American English spelling conventions. Examples: [[internalization]] (with 'z'), [[omega-category]] (with hyphen as in $\omega$-category) but [[BRST complex]], [[Chevalley?Eilenberg algebra]] (with endash since they are two people) but [[Burali-Forti paradox]] (with hyphen since he is one person).

&#8212;Toby (who prefers British spelling, but Urs and John use American)
=--

+-- {: commentbruce}
Yes sir! &mdash;Bruce
=--

{:responsetoby: style="color:indigo; font-size: 90%; margin-left:3em;"}
+-- {: responsetoby}
I trust you're joking, Bruce, but I hope that nobody gets hard-nosed about these conventions, at least not yet. They are just suggestion, good ones I hope, but it's not too late to change or reject them, and the whole community should be involved in that.

Also, thanks for the comment style. I see now how they're made!

&#8212;Toby
=--

{:commentsimon: style="color: #8B4513; font-size: 90%; margin-left:2em;"}

+-- {: commentsimon}
Sorry, I haven't been keeping up, lots of other stuff on, but just stuck my nose through the door to see how the decorating is going.  With regard to these naming conventions I tried to rename the Math page Mathematics to get round the US/UK thing, I now see it has been renamed.  Keep up the good work.  &mdash;Simon
=--

+-- {: commenturs}

Thanks, Toby, for your efforts! I appreciate it. These naming convention suggestions are good. If and when I do not adhere to them, it is because of me not paying enough attention to what my fingers are doing, which happens. -- Urs

=--

+-- {: responsetoby}
Then I guess that I&#39;ll correct you whenever you violate the conventions. But as Jacques would point out, the wiki will be less cluttered if the actual creation of new pages always follows the conventions; that&#39;s the most important part. &#8212;Toby
=--

+-- {: commenttoby}
Another possible naming convention: only ASCII characters. It\'s possible to put non-ASCII characters in a name (but not ones generated by iTeX or `&`&hellip;`;` character entities), but this may be difficult, depending on the user. We\'re already applying this in cases like [[omega-category]] (rather than [[∞-category]]), but this idea would go further: to *overrule* the one about following standard spelling when that uses non-ASCII characters (principally dashes). In particular, while the rules above favour [[Chevalley?Eilenberg algebra]] (with endash), this proposed change would favour [[Chevalley-Eilenberg algebra]] (with hyphen) instead. Personally, I prefer the endash, but I can see that this may just expect too much of the writer.
=--

+--{.query}
A very fundamental little issue: should we usually write n-category or $n$-category? 
-[[John Baez|John]] 

{:commenttoby}
I would say '$n$-category'. However, that doesn\'t work in links: '[[$n$-category]]', '[[n-category|$n$-category]]'. So for that I write '$n$-[[n-category|category]]'. In any case, we should be happy to accept contributions from people that say 'n-category'; somebody that cares more can always pretty it up afterwards. &#8212;[[Toby artels|Toby]]
=--

#### Stylesheet update: removing icons in links

+-- {: commentbruce}
I disabled the icons that used to appear next to pdf files, n-category cafe links, etc., by commenting out that code in the CSS for the nLab under "Edit Web" on the main page. 

It's just a test. I was starting to feel that the little images were a distraction on the page, sort of like the feeling you get when there are too many advertisements on a page. How do people feel, or you in favour of them or not? They can be enabled again by just un-commenting them in the stylesheet tweaks by someone with a password. -- Bruce
=--

+-- {: commenturs}

I liked them. -Urs

=--

## Basic Math Entries, Diagrams

I'm glad people are tackling all sorts of fundamental issues in this discussion.  I've been keeping quiet mainly because I'm really busy, and prefer to spend my little time here creating new entries.  

I am very proud to be the first to create the entries for basic words like [[object]], [[morphism]], [[category]], [[adjunction]] and so on - it's like being God and coming up with the first star, the first rock and so on.  Other people may think it silly to have entries for such basic ideas, but I'm hoping this website will eventually grow into a complete introduction to $n$-category theory.  If and when I ever start writing my books on higher-dimensional algebra, I'll do it here, and include lots of link to pages where basic terms are defined.  So, I imagine we're planting seeds that will eventually grow into something quite large.

For this reason, I hope that Todd Trimble joins this project, as he once said he wanted to.  I also hope Tom Leinster and Eugenia Cheng and Simon Willerton and Robin Houston and many other folks contribute entries.  

I need to figure out a way to lure such people into adding new entries - and improving ones that already exist.  I may try some $n$-Cafe posts that basically say: "Hey, I just wrote a little entry on monoidal categories!  Can you help improve it?"

How easy is it to just grab a Wikipedia entry, fix it up a bit, and stick it in here?  What are our legal and/or moral obligations if we do that?

+--{commenttoby}
See [http://test/](test). &#8212;[[Toby Bartels|Toby]]
=--

Here's another serious issue: how easy or impossible is it to draw _diagrams_ in this environment?  Without diagrams, we're crippled.

-[[John Baez|John]] 


category: meta