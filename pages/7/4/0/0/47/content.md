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

{:commentjohn}
I always fix them. I hate 'em. - [[John Baez|John]]

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
I would say '$n$-category'. However, that doesn\'t work in links: '[[$n$-category]]', '[[n-category|$n$-category]]'. So for that I write '$n$-[[n-category|category]]'. In any case, we should be happy to accept contributions from people that say 'n-category'; somebody that cares more can always pretty it up afterwards. &#8212;[[Toby Bartels|Toby]]
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
See [what Wikipedia has to say](https://secure.wikimedia.org/wikipedia/en/wiki/Wikipedia%3ACopyrights#Reusers.27_rights_and_obligations). &#8212;[[Toby Bartels|Toby]]
=--

Here's another serious issue: how easy or impossible is it to draw _diagrams_ in this environment?  Without diagrams, we're crippled.

-[[John Baez|John]]

+--{: response}
Ya mean like this one (from the page on [[oriental|orientals]]):

$$
\array{\arrayopts{\rowalign{center}}
O(\Delta^0) = & \{ 0\} \\
O(\Delta^1) = & \left\{ 0 \to 1\right\} \\
O(\Delta^2) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="6em" height="4em" viewBox="0 0 60 40">
 <defs>
  <marker id="svg295arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="5" orient="auto">
   <path fill="#930" d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
  <marker id="svg296arrowhead" viewBox="0 0 10 10" refX="0" refY="5" markerUnits="strokeWidth" markerWidth="4" markerHeight="2.5" orient="auto">
   <path fill="#930" d="M 0 0 L 10 5 L 0 10 z"/>
  </marker>
 </defs>
 <g font-size="10">
  <foreignObject x="25" y="-2" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
  <foreignObject x="0" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
  <foreignObject x="50" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
 </g>
 <g fill="none" stroke="#930">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M10,30 23, 15"/>
   <path d="M35,12 48, 27"/>
   <path d="M15,37 45, 37"/>
  </g>
  <g>
   <path stroke-width="3" d="M30,15 30,27" marker-end="url(#svg296arrowhead)"/>
   <path stroke="#FFF" d="M30,15 30,27"/>
  </g>
 </g>
</svg>
\end{svg}}
\right\}\\
O(\Delta^3) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="13em" height="5em" viewBox="0 0 130 50">
 <defs>
  <g id="myRect256">
   <g font-size="10">
    <foreignObject x="0" y="-3" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="0" y="37" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="40" y="-3" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="40" y="37" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
   </g>
   <g fill="none" stroke="#930">
    <g marker-end="url(#svg295arrowhead)">
     <path d="M10,7 37, 7"/>
     <path d="M6,42 6, 17"/>
     <path d="M10,47 37, 47"/>
     <path d="M46,12 46, 37"/>
    </g>
   </g>
  </g>
 </defs>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myRect256" x="0" y="0"/>
 <g fill="none" stroke="#930">
  <path d="M11,43 38, 15" marker-end="url(#svg295arrowhead)"/>
  <g stroke-width="3" marker-end="url(#svg296arrowhead)">
   <path d="M12,12 20,20"/>
   <path d="M40,18 27,40"/>
  </g>
  <g stroke="#FFF">
   <path d="M12,12 20,20"/>
   <path d="M40,18 27,40"/>
  </g>
 </g>
 <g fill="none" stroke="#930">
   <path stroke-width="5" d="M55,25 72,25"/>
   <path stroke-width="3" stroke="#FFF" d="M55,25 72,25" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="1" d="M55,25 72,25"/>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myRect256" x="80" y="0"/>
 <g fill="none" stroke="#930">
  <path d="M92,12 118, 39" marker-end="url(#svg295arrowhead)"/>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M92,20 100,38"/>
    <path d="M120,12 113,19"/>
   </g>
   <g stroke="#FFF">
    <path d="M92,20 100,38"/>
    <path d="M120,12 113,19"/>
   </g>
  </g>
 </g>
</svg>
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="28em" height="23em" viewBox="-35 0 245 230">
 <defs>
  <g id="myPent256">
   <g font-size="10">
    <foreignObject x="25" y="-2" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>2</mi></math></foreignObject>
    <foreignObject x="0" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>1</mi></math></foreignObject>
    <foreignObject x="50" y="27" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>3</mi></math></foreignObject>
    <foreignObject x="13" y="57" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>0</mi></math></foreignObject>
    <foreignObject x="38" y="57" width="12" height="14"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><mi>4</mi></math></foreignObject>
   </g>
   <g fill="none" stroke="#930" marker-end="url(#svg295arrowhead)">
    <path d="M8,32 25,13"/>
    <path d="M35,10 52,28"/>
    <path d="M54,41 48,57"/>
    <path d="M24,67 36,67"/>
    <path d="M16,62 8,45"/>
   </g>
  </g>
 </defs>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="0" y="0"/>
 <g fill="none" stroke="#930">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M10,36 45,36"/>
   <path d="M22,60 47,41"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M31,12 31,26"/>
    <path d="M12,38 25,48"/>
    <path d="M45,48 35,60"/>
   </g>
   <g stroke="#FFF">
    <path d="M31,12 31,26"/>
    <path d="M12,38 25,48"/>
    <path d="M45,48 35,60"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="110" y="0"/>
 <g fill="none" stroke="#930">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M120,36 155,36"/>
   <path d="M122,41 147,60"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M141,12 141,26"/>
    <path d="M125,47 135,58"/>
    <path d="M162,38 145,48"/>
   </g>
   <g stroke="#FFF">
    <path d="M141,12 141,26"/>
    <path d="M125,47 135,58"/>
    <path d="M162,38 145,48"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="160" y="80"/>
 <g fill="none" stroke="#930">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M172,119 195,140"/>
   <path d="M194,98 201,138"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M175,127 185,138"/>
    <path d="M212,116 206,116"/>
    <path d="M189,98 184,121"/>
   </g>
   <g stroke="#FFF">
    <path d="M175,127 185,138"/>
    <path d="M212,116 206,116"/>
    <path d="M189,98 184,121"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="55" y="160"/>
 <g fill="none" stroke="#930">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M74,220 83,180"/>
   <path d="M87,178 96,218"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M86,187 86,216"/>
    <path d="M63,196 71,196"/>
    <path d="M107,196 99,196"/>
   </g>
   <g stroke="#FFF">
    <path d="M86,187 86,216"/>
    <path d="M63,196 71,196"/>
    <path d="M107,196 99,196"/>
   </g>
  </g>
 </g>
 <use xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="#myPent256" x="-50" y="80"/>
 <g fill="none" stroke="#930">
  <g marker-end="url(#svg295arrowhead)">
   <path d="M-31,140 -22,100"/>
   <path d="M-29,143 -3,120"/>
  </g>
  <g>
   <g stroke-width="3" marker-end="url(#svg296arrowhead)">
    <path d="M-40,116 -35,116"/>
    <path d="M-17,97 -17,123"/>
    <path d="M-5,128 -15,140"/>
   </g>
   <g stroke="#FFF">
    <path d="M-40,116 -35,116"/>
    <path d="M-17,97 -17,123"/>
    <path d="M-5,128 -15,140"/>
   </g>
  </g>
 </g>
 <g fill="none" stroke="#930">
  <g stroke-width="5">
   <path d="M60,35 100,35"/>
   <path d="M158,75 168,90"/>
   <path d="M118,190 168,155"/>
   <path d="M3,150 43,185"/>
   <path d="M-3,95 11,79"/>
  </g>
  <g stroke-width="3" stroke="#FFF" marker-end="url(#svg296arrowhead)">
    <path d="M158,75 168,90"/>
    <path d="M60,35 100,35"/>
    <path d="M118,190 168,155"/>
    <path d="M3,150 43,185"/>
    <path d="M-3,95 11,79"/>
  </g>
  <g stroke-width="1">
   <path d="M60,35 100,35"/>
   <path d="M158,75 168,90"/>
   <path d="M118,190 168,155"/>
   <path d="M3,150 43,185"/>
   <path d="M-3,95 11,79"/>
  </g>
 </g>
 <g fill="none" stroke="#930">
   <path stroke-width="7" d="M85,43 85,140"/>
   <path stroke-width="5" stroke="#FFF" d="M85,43 85,140" marker-end="url(#svg296arrowhead)"/>
   <path stroke-width="3" d="M85,43 85,140"/>
   <path stroke-width="1" stroke="#FFF" d="M85,43 85,140"/>
 </g>
</svg>
\end{svg}}
\right\}
}
$$

&mdash; [[Jacques Distler|Jacques]]

=--

### Backups

+-- {: commenturs}

I think it was mentioned before, but I missed it: is there a quick web-interface way to upload files to the server that an entry wants to link to?

Another thing: the more work we invest in this the more I become worried that we have some data loss. Is there any way too have an automated mirror image of the site created every now and then? Jacques said the whole wiki itself sits in one big file. What about pictures etc on the server that it links to?

 -Urs

=--
+-- {: commentjohn}

Urs writes: "The more work we invest in this the more I become worried that we have some data loss" - yes, I'm worried about that too.  I'd imagined you had already solved that problem by now!  I think I won't do any more work on this wiki until we solve this problem.  I hate losing work, and I back up all my work to 2 or 3 sites.

"Jacques said the whole wiki itself sits in one big file."  Is there at least a way for you or I to manually copy this file to another site?  Of course an automatic backup procedure is better - until it stops working for some reason; one still needs to check it regularly.

-[[John Baez|John]]

=--

+--{: response}

Well, you'll have to ask your webhosts why

     scp -v /usr/local/instiki/db/production.db.sqlite3 distler@golem.ph.utexas.edu:Desktop/

produces the following error (lots of other junk, but this is the important line):

     debug1: read_passphrase: can't open /dev/tty: No such device or address

which is a little strange, since

      ls -l /dev/tty

yields

      crw------- 1 root root 5, 0 Dec 14 06:32 /dev/tty

One should also be able to initiate a `scp` operation *from* the remote machine. That doesn't work either, presumably for the same reason.
=--

+--{commenttoby}
Can one make use of the Atom feeds (see 'Feeds' at top)? I don\'t really know anything about feeds, but I probably should learn.
=--

+--{: response}
You can [export](http://ncatlab.org/nlab/export) the entire wiki. That's not the point. You should also be able to mirror the database file and any attendant files

    scp -r /usr/local/instiki/public/nlab/files distler@golem.ph.utexas.edu:Desktop/

to some remote location (your laptop, even). That's not possible because the setup here seems not to assign a `tty` to the shell one obtains when one `ssh`s into the VPS. This makes it impossible to use `scp` (or `rsync -e ssh` or whatever).
=--

+-- {: commenturs}

To John: 
So there is no reason to be worried about loss of the content of the entries. Please don't make this stop anyone work on the wiki!! As Jacques points out, using
[export](http://ncatlab.org/nlab/export) gives a zip-file with all the typed content. I am keeping regular backup
copies of that.

But I was wondering what happens when we start uploading lots of auxiliary files, such as .gifs, to the server. Apparently that requires more thoughts/work...

To Toby: subscribing to the feed is a convenient way to keep track of which entries were changed in which way.

\-\- [[Urs Schreiber|Urs]]
=--

+--{commenttoby}
So if we want to back up the current wiki, then we export it. If we want to back up the wiki and its history, then we (once only) go through the history of each page and back it up by hand, then use the feed to track all further changes. If we want to back up uploaded files too, will these show up in the feed or the export? (Do we have any yet for a test?)

{: response}
That's a *silly* way to do things. Just `cp` the database file into the `/usr/local/instiki/public/nlab/files/` directory, download the copy with your web browser, and then delete the copy.

{: responsetoby}
Heh, maybe I should say that\'s how *I* could do it (^_^). I don\'t want to make assumptions about what can be done in the shell, which apparently has some bad behaviour. In any case, I don\'t have access to the shell, but I am capable of the (otherwise much sillier) method above. (Not that I expect to do that either &#8230; although I did export the wiki last night and might do so again in a week or so.)

{: response}
I understand. I presumed that Urs would be the one doing the off-site backups. In any case, I want to emphasize that placing a copy of the database file in the downloadable `files` directory is a security risk. So it should not be named something obvious, like "`production.db.sqlite3`", and it should not be left there any longer than absolutely necessary.

{: responsetoby}
If Urs is reading this, then he will probably do that (until `scp` is fixed), and that will settle it. But by the way, what is the security risk in the database? (Backups are more secure if widely spread, and without your warning, Urs might even have invited others to download it, although doubtless he, John, and David would be more than sufficient.) Does it contain my unencrypted password or something? (Of course, feel free to link to a general Instiki page if you\'ve already explained this elsewhere.)

{: response}
Unencrypted passwords (including the Instiki password needed on the "`Edit Web`" page) and all the purportedly password-protected data.

As far as avoiding the danger of lost effort, I think that the problem is solved. But backing up will be much easier and smoother if the `tty` problem is solved too.

{: response}
One operation instead of three.
=--

#Uploading resources#

+-- {: commenturs}

I was going to upload some pictures, but I am experiencing problems sft-ing into the server. Not sure why.

Generally, it would be nice if everybody could upload resources together with the entries he or she submits. Maybe with a password protection. I am not sure how to proceed on this matter...


\-\- [[Urs Schreiber|Urs]]
=--

+--{commenttoby}
[Jacque says](http://golem.ph.utexas.edu/instiki/show/File+Uploads) that one shouldn\'t allow uploads without password protection, I guess to prevent spam. Perhaps uploads should be restricted to a separate web (for uploads only), which this web can link to. (I gather that allowing uploads and requiring passwords is done web by web within the Instiki installation.)

Uploaded files can also overwhelm the memory limits (even without spam). That\'s one reason to make images SVG whenever possible.

{: response}
If you keep a reasonable upper limit on the allowed size of uploaded files and if someone is willing to check periodically that miscreants are not abusing the site by using it as a file drop-box, then I suppose the risk is relatively low. Nowadays, with the popularity of P2P filesharing systems, the temptation of using some random unsecured website as a drop-box is somewhat diminished.
=--

## Another category, another naming convention ##

I\'ve gone through all the names of categories (like $\Set$, the category of sets) and tagged the pages category\: category. Also, I\'ve imposed a naming convention on categories, that they should be singular and abbreviated if long. I\'m not sure that I agree with these, but they seemed to be more common already than the alternatives, and I think that it will be good to have a convention. If anybody doesn\'t like this convention, then please say so! (It\'s not too late to change things back.) &#8212;[[Toby Bartels|Toby]]

##Algebroids##

_[[Eric Forgy|Eric]] says_:

I was thinking about the categorical definition of [[algebra|algebras]] as a [[monoid]] in Vect. Then I was trying to think of how you would similarly define a graded algebra. A thought that came to mind, which seems to make sense, is that a graded algebra could be thought of as a "category in Vect". Or something like that.

Come to think of it, could you say that given a monoid $M$, an algebra is a functor $A:M\to Vect$? 

Could you say that given a category $C$, an algebroid is a functor $A:C\to Vect$?

Then a graded algebra is a special kind of algebroid. It sounds kind of poetic. Is there any truth to it?

Does that make any sense?

After some doodling, I think that a graded algebra should be a monoid in the category of graded vector spaces. Is that better? 

If a graded algebra is a monoid in graded vector spaces, what is a clean "categorical" way to probe the degree of the element?

What is a clean categorical way to define graded vector spaces? 

_[[Urs Schreiber|Urs]] says_: If you want you can say that
a $G$-graded vector space is a functor $G \to Vect$.
Notice: NOT a functor $\mathbf{B}G \to Vect$ from the
group $G$, regarded as a one-object [[groupoid]], but
just a functor from the underlying [[set]] of $G$. 

_[[Toby Bartels|Toby]] says_: Given an [[abelian group]] $G$, the [[functor category]] of functors from $|G|$ to $\Vect$ (where $|G|$, the order of the group $G$, is a [[set]]) is the category of $G$-graded vector spaces with homogeneous linear maps as morphisms. To make this a [[monoidal category]], let $(V \otimes W)_g$ (where $V = (V_g)_{(g:G)}$ is a functor) be
$$\bigoplus_{h:G} V_h \otimes W_{g-h} = \bigoplus_{h,k:G, \atop h+k=g} V_h \otimes W_k$$
(a kind of [[convolution product]]). Then a $G$-graded algebra should be a monoid in this monoidal category. (To some extent, this should still work even if $G$ is just a non-abelian monoid. What we really need is to describe that convolution product arrow-theoretically.)

See also: <https://secure.wikimedia.org/wikipedia/en/wiki/Super_vector_space#The_category_of_super_vector_spaces>. But it looks like $G$ must be a ring (or at least rig) to define the braiding.

_[[John Baez|John]] says_:  Eric wrote: 

_I was thinking about the categorical definition of [[algebra|algebras]] as a [[monoid]] in Vect. Then I was trying to think of how you would similarly define a graded algebra._

It's a monoid in GradedVect, the monoidal category of graded vector spaces.

_A thought that came to mind, which seems to make sense, is that a graded algebra could be thought of as a "category in Vect". Or something like that._

No, a category in Vect is precisely a 'Baez-Crans 2-vector space': it has a vector space of objects, a vector space of morphisms, and all the category operations are linear.

_Come to think of it, could you say that given a monoid $M$, an algebra is a functor $A:M\to Vect$?_

You could say it, but that wouldn't make it true.  <img src = "http://math.ucr.edu/home/baez/emoticons/tongue2.gif" alt = ""/>  

In fact, a functor $A: M \to Vect$ is none other than a [[representation]] of the monoid $M$.   

_Could you say that given a category $C$, an algebroid is a functor $A:C\to Vect$?_

You could say it, but that wouldn't make it true.  <img src = "http://math.ucr.edu/home/baez/emoticons/tongue2.gif" alt = ""/>  

In fact, a functor $A: C \to Vect$ is a [[representation]] of your category $C$, which is very different than an algebroid.  An algebroid is a category enriched in $Vect$.

_Then a graded algebra is a special kind of algebroid. It sounds kind of poetic. Is there any truth to it?_

Yes, there's some truth to this guess, despite the errors that led up to it.  Jim Dolan and I have been working on ideas related to this, and (more interestingly) their applications to algebraic geometry.  But we prefer to shock the world with these ideas at a later time.

_What is a clean categorical way to define graded vector spaces?_

Toby already answered this, but let me note that one can and should define [[graded vector space|$S$-graded vector spaces]] for any set $S$; these then acquire special properties when $S$ is a monoid (like the natural numbers) or a group (like the integers).  An $S$-graded vector space is a functor $F: S \to Vect$, where we think of the set $S$ as a [[discrete category]].

Please don't take my slapdowns the wrong way!  I'm very glad you're trying to understand lots of math from a categorical viewpoint.  But, in my 'Wizard' persona it's my duty to crush errors --- with a certain crazed glee, and utter disregard for the sensitive feelings of the victim.

[[Eric Forgy|Eric]] says: Thanks! Fortunately (I think), I am comfortable admitting I don't understand something and one way I learn is to state things as I see them hoping to be corrected. Slap away!

##Discussion Pages##

On some pages, e.g. [[quiver]], some discussion is forming. Rather than polluting the page and rather than just deleting the discussion after it has been settled, what if we create special "Discussion" pages that relate to specific pages? For example, <nowiki>[[Discussion: quiver]]</nowiki> and link to this page from <nowiki>[[quiver]]</nowiki>.

If we decide to do this, we may want to settle now on a proper page title format.

+--{commenttoby}
That\'s a possibility. However, I don't think that ongoing discussions are pollution, certainly not when they\'re in their query blocks, easy to separate from the rest of the page.

A lot of discussion will have no value worth saving (and it\'s in the edit history if really needed). A lot of useful discussion can be refactored (when finished) into the normal page text. Until we get into back-and-forth arguments and haggled compromises like on Wikipedia, I\'m not sure what would be left to move to a dedicated discussion page.
=--

_[[John Baez|John]] says:

Right now I like the idea of putting the discussion in the same page, at the end, in a section labelled Discussion.  

I think that people can learn a lot from these discussions, where you see the interplay of ideas better than in the formal portion of the text.  This is, after all, not an encyclopedia but a "Lab" - a place where people come to work and think.  We haven't quite discovered what that means yet. But, it could involve a lot of discussion.

##Definitions --- Boldface or Italics##

_[[John Baez|John]] says_:

I've been putting definitions in _italics_.  Someone else is putting them in **boldface**.  We should settle on a convention.  Meet me at dawn in the town square --- bring your pistol.

{: response}
If you used the [Theorem Environment](http://golem.ph.utexas.edu/instiki/show/Theorems) to mark then up, then this decision could be made globally, by adjusting the CSS. But, since I've pointed this out 6 or 8 times, now, maybe I should just let you have recourse to your pistols.

{: response}
_[[Eric Forgy|Eric]] says_: I'm still learning and wasn't aware of the Theorem Environment. We should definititely encourage its use, however, I think John is referring to the first use of the word _within_ a definition. I've noticed that too. I've been using **bold**, but could switch to _italic_ if that is what you want.

{: response}
_[[John Baez|John]] says_: In this case I'm more interested in consistency than enforcing my will upon the world, despite my joke about pistols at dawn.  **Bold** jumps out you more than _italics_, I think.  A theorem environment would let us make (and change) this decision globally, but we won't want all our definitions to be stated as part of a formal **Definition** environment --- sometimes it's nice to make a definition as part of a paragraph of ordinary text, and in my own papers I always put the defined term in **boldface**, to 1) make the definitions easy to spot, and 2) make it clear that I'm defining something instead of stating a fact about something (I hate it when someone says "Pr&uuml;fer rings are hereditary and Noetherian" and I can't tell if this is supposed to be the _definition_, or merely a cute _fact_ about Pr&uuml;fer rings).

##Linking to Wikipeda##

_[[Eric Forgy|Eric]]_ says: How would I link to an external address that itself contains parentheses, e.g.

http://en.wikipedia.org/wiki/Field_(mathematics)

Attempting

<nowiki>[Field](http://en.wikipedia.org/wiki/Field_(mathematics))</nowiki>

picks up the first closing parentheses and tries to link to

http://en.wikipedia.org/wiki/Field_(mathematics

{: response}
<nowiki>[Field](http://en.wikipedia.org/wiki/Field_%28mathematics%29)</nowiki> produces [Field](http://en.wikipedia.org/wiki/Field_%28mathematics%29).

_[[John Baez|John]] says_: I ran into this problem too, but not remembering the good solution described above, I adopted a crude hack: I left out the parentheses around, say, "(mathematics)".  It worked, but only because Wikipedia forgave my sin.  I need to go back and fix my mistakes someday.

##Deleting Pages##

I created a page on accident (typo) and didn't realize until I modified it. Is there a way to delete it?

category: meta