[[!redirects redirects]]
Instiki now includes the ability to redirect pages.  

#Example: Plural nouns and capitalization#

To redirect the plural 

<nowiki>[[categories]]</nowiki> 

to the existing page 

<nowiki>[[category]]</nowiki>, 

simply edit [[category]] and insert 

<nowiki>[[!redirects categories]]</nowiki>

at the bottom of the page. From then on, whenever you link to [[categories]], you are taken to [[category]]. This saves you the headache of typing things like

<nowiki>[[category|categories]].</nowiki>

For example, if you edit [[category]] and look at the bottom, you will find


<nowiki>[[!redirects categories]]</nowiki><br>
<nowiki>[[!redirects Category]]</nowiki><br>
<nowiki>[[!redirects Categories]].</nowiki><br>

Therefore, [[categories]], [[Category]], and [[Categories]] all redirect to [[category]] now.

##Caveat##

Redirects only work if the desired redirected page <nowiki>[[categories]]</nowiki> _does not already exist_. 

Don't worry, this is a feature, not a bug, designed to avoid silly things like infinite redirect loops, etc. 

In the event that <nowiki>[[categories]]</nowiki> does exist already, then it probably should not if <nowiki>[[category]]</nowiki> aready exists. 

If you run into this situation, you can help by transferring material from <nowiki>[[existing pages]]</nowiki> to <nowiki>[[existing page]]</nowiki> and change the name of <nowiki>[[existing pages]]</nowiki> to <nowiki>[[existing pages -- history]]</nowiki>. Now the redirects will work AND we maintain the history of any revisions that were made to <nowiki>[[existing pages]]</nowiki>.

#Example: Links with non-ASCII symbols

Currently, there are many pages with titles that would ideally include symbols, e.g. [[(infinity,1)-category]].

Prior to redirects, if you wanted to link to this page, you could either write the _ugly_ version

<nowiki>[[(infinity,1)-category]]</nowiki>

or worse, if you were using the plural version you could write

<nowiki>[[(infinity,1)-category|(infinity,1)-categories]]</nowiki>

Alternatively, you could get a little fancy with

<nowiki>$(\infty,1)$-[[(infinity,1)-category|(infinity,1)-categories]]</nowiki>

which but doesn\'t allow the link to cover the entire linking phrase.

Currently, if you edit [[(infinity,1)-category]], and look at the bottom, you will see

<nowiki>[[!redirects (∞,1)-category]]</nowiki><br>
<nowiki>[[!redirects (∞,1)-categories]]</nowiki><br>
<nowiki>[[!redirects (infinity,1)-categories]]</nowiki><br>
<nowiki>[[!redirects infinity comma one category]].</nowiki><br>

This means that we can now simply insert links like [[(∞,1)-categories]] and be redirected to [[(infinity,1)-category]].  The only downside here (compared to the previous alternative) is that math material is in the text font.  (Some of us even write `$2$-[[2-category|category]] for this reason.)

##Caveat##

The $\infty$ symbol included in the link is not obtained via the itex syntax <nowiki>\infty.</nowiki> To actually include non-ASCII symbols in links, you either need to be an expert at unicode OR simply find the $\infty$ symbol already displayed somewhere, copy it, and paste the symbol into the edit box. To see what I mean, you can edit this page to look at the source code for the link: [[(∞,1)-categories]].

***

See also [the official Instiki guidelines](http://golem.ph.utexas.edu/instiki/show/Syntax#redirecting).

[[!redirects redirects]]