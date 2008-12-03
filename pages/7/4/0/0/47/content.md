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