Instiki now includes the ability to redirect pages.  

#Example: Plural nouns and capitalization#

To redirect the plural 

    [[categories]]

to the existing page 

    [[category]]

simply edit [[category]] and insert 

    [[!redirects categories]]

at the bottom of the page. From then on, whenever you link to [[categories]], you are taken to [[category]]. This saves you the headache of typing things like

    [[category|categories]]

For example, if you open [[category]] for editing and look at the bottom, you will find

    [[!redirects categories]]
    [[!redirects Category]]
    [[!redirects Categories]]

Therefore, [[categories]], [[Category]], and [[Categories]] all redirect to [[category]] now.

##Caveat##

Redirects only work if the desired redirected page `[[categories]]` _does not already exist_. 

Don't worry, this is a feature, not a bug, designed to avoid silly things like infinite redirect loops, etc. 

In the event that `[[categories]]` does exist already, then it probably should not if `[[category]]` aready exists. 

If you run into this situation, you can help by transferring material from `[[existing pages]]` to `[[existing page]]` and change the name of `[[existing pages]]` to `[[existing pages > history]]`. Now the redirects will work *and* we maintain the history of any revisions that were made to `[[existing pages]]`.

#Example: Links with non-ASCII symbols

Currently, there are many pages with titles that would ideally include symbols, e.g. [[(infinity,1)-category]].

Prior to redirects, if you wanted to link to this page, you could either write the _ugly_ version

    [[(infinity,1)-category]]

or worse, if you were using the plural version you could write

    [[(infinity,1)-category|(infinity,1)-categories]]

Alternatively, you could get a little fancy with

    $(\infty,1)$-[[(infinity,1)-category|(infinity,1)-categories]]

which preserves the distinction between math and text but doesn\'t allow the link to cover the entire linking phrase.

Currently, if you open [[(infinity,1)-category]] for editing and look at the bottom, you will see

    [[!redirects (∞,1)-category]]
    [[!redirects (∞,1)-categories]]
    [[!redirects (infinity,1)-categories]]

This means that we can now simply insert links like [[(∞,1)-categories]] and be redirected to [[(infinity,1)-category]].  The only downside here (compared to the previous alternative) is that math material is in the text font.  (Some of us even write `$2$-[[2-category|category]]` for this reason.)

##Caveat##

The `?` symbol included in the link is not obtained via the itex syntax `$\infty$`. To actually include non-ASCII symbols in links, you either need to be an expert at unicode *or* simply find the '?' symbol already displayed somewhere, copy it, and paste the symbol into the edit box. To see what I mean, you can edit this page to look at the source code for the link: [[(∞,1)-categories]].

#Undoing a Redirect#

Occasionally you may come across a situation where a redirect exists for a link that you'd like to create a separate entry for. For example, [[constructivism]] is currently redirected to [[constructive mathematics]]. If you'd prefer to have a separate entry for constructivism (to discuss the philosophy rather than the mathematical practice), you can simply edit [[constructive mathematics]] and remove the line (likely at the bottom of the edit box) 

    [[!redirects constructivism]]

Now you can create [[constructivism]] as usual and any pages that had previously been redirected to [[constructive mathematics]] will now point to your new entry.

***

See also [the official Instiki guidelines](http://golem.ph.utexas.edu/instiki/show/Syntax#redirecting) on redirects.


[[!redirects redirects]]