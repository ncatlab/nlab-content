+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Contents### {: .clickToReveal}
###Contents### {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include contents]]
=--
=--
=--

An easy introduction for elementary basics is

* [[How to get started]].

The following provides more details.

You can copy the source code of the $n$Lab's [[template page]] to ease your own creation of new pages.


See also the [[FAQ]].

# Contents

* Automatic table of contents
{: toc}

# Technical #

## Software required to use the $n$Lab
{#software}

The $n$Lab displays mathematical symbols using [MathML](http://en.wikipedia.org/wiki/MathML).  Displaying MathML requires support from your web browser.  The browser with the best support for MathML is [Firefox](http://www.mozilla.com/firefox/), especially if you install the [STIX fonts](http://www.mozilla.org/projects/mathml/fonts/).  Firefox is a great browser in many other ways too, so if you aren't using it, why not give it a try?

Recent versions of Opera also apparently support MathML, but as a blog post on [Jacques Distler's Musings](http://golem.ph.utexas.edu/~distler/blog/archives/001588.html) points out, this may not work properly.  For InternetExplorer, one needs to install the [MathPlayer](http://www.dessci.com/en/products/mathplayer/) plugin. Download is quick and easy and free, but installation may require Administrator privileges on your computer.  Other browsers such as Safari and Chrome seemingly do not support MathML at present.

## How to search the nLab & nForum from firefox ##

(Firefox - and clones - specific)

Here are some search plugins for firefox that will let you search the nLab from the firefox search bar.

* [[nlab-search.xml:file]]: searches the nLab (like the search box at the top of every page).
* [[nlab-goto.xml:file]]: takes you directly to the page with a given exact title (if it exists; otherwise it takes you to an edit box to create such a page).
* [[nlab-edit.xml:file]]: takes you directly to the "edit" page for a given title.
* [[nforum-topic-search.xml:file]]: searches the nForum Topics.
* [[nforum-comment-search.xml:file]]: searches the nForum Comments.

It would be nice if these had different icons.  To use one or more of these, drop them in the 'searchplugins' directory of your firefox profile.

## How to edit nLab pages in your favorite text editor ##

(Firefox - and clones - specific)

One way to do this is to install [this firefox extension](https://addons.mozilla.org/en-US/firefox/addon/4125) or another one like it.

If your favorite editor is [Emacs](http://www.gnu.org/software/emacs/) with [AucTeX](http://www.gnu.org/software/auctex/), you may find the following snippet useful to put in your `.emacs` file:

    (add-to-list 'auto-mode-alist '("/\\(www.\\)?ncatlab.org" . latex-mode))
    (add-to-list 'auto-mode-alist '("/golem.ph.utexas.edu" . latex-mode))
    (defun nlab-latex-fixes ()
      (when (or (string-match "/\\(www.\\)?ncatlab.org" buffer-file-name)
                (string-match "/golem.ph.utexas.edu" buffer-file-name))
      (longlines-mode t)
      (set (make-local-variable 'TeX-open-quote) "\"")
      (set (make-local-variable 'TeX-close-quote) "\"")))
    (add-hook 'LaTeX-mode-hook 'nlab-latex-fixes)

This will tell Emacs to automatically edit nLab pages (and nCafe comments as well, for good measure) in LaTeX mode, with long lines wrapped using soft returns, and ordinary double-quotes rather than LaTeX ones.

## How to print a page from the nLab ##

If you just print it directly, the logo will become a huge blob that takes up the entire first page.  I know, we can and should fix this, but we haven\'t.  So for now, use the 'Print' link at the bottom of the page.  As a shortcut in most browsers on most operating systems, hit Alt-Shift-P while the focus is in the page to go to the printable page.

## How to customize the nLab ##

(Firefox - and clones - specific)

You may wish to customize the font scheme (both for math or text) on the nLab, as well as tweak things such as the small edit box for comments. Try using the Stylish add-on if you are using Firefox; Stylish is a plug-in for firefox enabling you to customize websites; it is available [here](https://addons.mozilla.org/en-US/firefox/addon/2108).

Currently, the following stylish themes are available:

* [nLab Stylish theme](http://userstyles.org/styles/17934) by [[Bruce Bartlett]].  This nLab theme changes the fonts on the nLab to a serif-style, and makes the edit box much bigger for an overall more pleasant experience!
* [nLab -- nCafe style](http://userstyles.org/styles/22800) by [[Daniel Schappi|Daniel Schäppi]].  This is based on Bruce Bartlett's theme but changes the overall colour scheme somewhat to something a little more like the n-Cafe.


## How to Download a Local Copy of the n-Lab {#download}

The inbuilt export features of the n-Lab have been switched off.  However, it is still possible to get a local version of the n-Lab.  This is a _static_ version in that you cannot edit pages, but is complete and all the links correctly point to the pages on the local version.

One way to do this on a Unix-based system (Linux, MacOSX, BSD), is to use the `wget` command.  The command is:

    wget --output-document=- http://ncatlab.org/nlab/list \
     | perl -lne '/<div id="allPages"/ and $print = 1;
                  /<div id="wantedPages"/ and exit;
                  /href="([^"]*)"/ and $print and print "http://ncatlab.org$1";' \
     | wget -i - -kKEpN

If you are fortunate enough to be using the Z-shell then you can type it exactly as written.  Other shells may complain at the line-breaks in the perl code (they should be alright with the backslashed line-breaks).  If so, simply type it all as one line.

One huge advantage of this script over the inbuilt export is that if you run it from the same place each time, it will only download _modified_ pages.  That saves a lot of bandwidth and time.

The following is an explanation of how it works.  The first step is to get a list of all the pages, we do this by downloading the `All pages` page and extracting a list of the pages (via a perl script). We feed this back into wget as a list of pages to get (using the `-i` option). For each downloaded page we ensure that we have the required extras to display it correctly (`-p` option), we convert the links so that they work correctly: links to downloaded files point to downloaded files, links to non-downloaded files point to non-downloaded files (`-k` option), we use time-stamping to only get new pages (`-N`), but because we're doing a little post-processing we need to keep the original files for time-stamping to work correctly (`-K`). Files are also converted to html extension (`-E`) since no matter how they were generated, they are now boring html (well, okay, xhtml+mathml+svg) files.

If anyone can post instructions for other operating systems, or other programs (such as `curl`) then please do so.


# Getting Started #

##How to use a Wiki##

Hit "edit page" to see how pages are coded. Use the [[Sandbox|Sandbox]] to warm up.  They key point is that links to other pages are placed in `[[double brackets]]`.

There is no feature to preview your edits.  Instead, submit them and then edit again.  Two successive submissions with the same signature and made within 30 minutes of each other count as one in the record, so don\'t worry about cluttering up the database with multiple submissions in a row.


## How to start a new page
{#newpage}

You do this in two steps, the first of which may have already been done:

1. Create a preliminary link (represented by a question mark) by editing a current page and putting the name of the new page in double square brackets.  (You can do this in the [[Sandbox]] if there is no better place, but probably you want to do this in context on a relevant page that should link to your new page.)

2. Clicking on the question mark to begin editing the new page.  (It will not actually be created until you hit Submit.)

_Watch out_: the name of a page is case sensitive, so make your link lowercase if it comes at the beginning of a sentence. (`[[like this|Like this]]`.) We loosely agreed to try to follow that and some other naming conventions; see [below](#naming).

However, this is less of an issue now that we have [[redirects]].


##Note to new contributors##

When you edit a page, you can (and should) put your name (with normal capitalisation and spacing) in the box after 'Submit as'. If you don\'t, then your contribution will be credited to the [[AnonymousCoward]].

Once you edit a page for the first time, your name will appear at the bottom, grayed out with a question mark since there is no page with your name yet.  You may take this as an invitation to create a user page and tell us about yourself.  But if you don't want to or don't have the time right now, you can forget about this. If you just want to show up on [category: people](http://www.ncatlab.org/nlab/list/people), then you make a page containing only 'category: people' (or someone else may do this for you).

To create your user page, simply click the question mark that appears next to your name at the bottom of the page after making a modification and add content to the edit box that appears. If you'd like to make a user page prior to modifying an existing page, you can do so by making some trivial modification to the [[Sandbox]], which will put your name at the bottom of the page where you can click the question mark. (Or hack the URL.)


## How to merge pages
{#merging}

Suppose we have two pages, named 'A' and 'B', and you decide that they ought to be merged into a single page, say 'A'.  Of course, you need to edit 'A' to contain the material from 'B' and make a coherent whole, but there are also some technical aspects.  We do *not* want to simply delete 'B', since it contains the history of the edits to that page, which might turn out to be useful.  However, we *do* want these two things:

1.  links to 'B' ought to send the reader to 'A';
2.  the old page 'B' should be clearly marked as archive material.

We accomplish (1) with a [[redirect]]; we accomplish (2) with a [[page move]].  If you do this too carelessly, then it will not work; in the worst case, links to 'B' will still go to the archive page, and that will look to the casual reader like a regular page.  So follow these steps:

1.  Edit 'A' so that it looks how you want, and add the line '[[!redirects B]]' to the bottom.  Submit.
2.  Open 'B' for editing.
3.  Click the checkbox 'Change page name.', which will bring up a new field 'New name:'.
4.  In that field, add ' > history' to the end, so that 'B' becomes 'B > history'.
5.  Click in the big edit box, which will automatically add '[[!redirects B]]' to the top.
6.  Change the line '[[!redirects B]]' into '< [[B]]' instead.
7.  Delete everything else (consisting of the material that you already merged into 'A').
8.  Submit.

The result is that links to 'B' will redirect to 'A' (not to 'B > history').  And if anyone does land on 'B > history', all that they will see is '<&#160;[[HomePage|B]]' with a link to 'B' (properly redirected to 'A').


## Naming conventions ##
{#naming}

These are not set in stone, but we\'re following them for now. Changing page titles results in unnecessary work for the [[lab elves]], so you should try to follow these if possible (or dispute them if not).  It is most important to follow these in links to pages that don\'t yet exist, so that the pages will be created at the correct title (and only once).

* Page titles should contain only ASCII characters.
  * Examples: `[[omega-category]]` instead of `[[$\omega$-category]]` or `[[∞-category]]`.
  * Tricks: To produce '$\omega$-[[omega-category|category]]', try `$\omega$-[[omega-category|category]]`. Unfortunately, [[omega-category|$\omega$-category]] does not work.
  * Reason: It's possible to put non-ASCII characters in a name, but not ones generated by iTeX or &...; character entities, so this can be difficult, depending on your browser. To keep things easy, therefore, use only ASCII characters in links.
  * With the introduction of [[redirects]] to Instiki many non-ASCII links now point to the correct ASCII page, e.g. `[[∞-category]]` is now redirected to [[∞-category]].
* Page titles should be singular nouns.
  * Examples: Use `[[category]]` instead of `[[categories]]`, `[[faithful functor]]` instead of `[[faithful]]`, and `[[categorification]]` instead of `[[categorify]]` or `[[categorified]]`.
  * Tricks: To produce '[[category|categories]]', try `[[category|categories]]`. To produce '[[faithful functor|faithful]] [[endofunctor]]', try `[[faithful functor|faithful]] [[endofunctor]]`.
  * Reason: We want only one page on a given concept, regardless of variations in grammar.
  * Again, with the introduction of [[redirects]] many plural links now point to the singular pages, e.g. [[categories]] gets you to [[category]] without needing to type `[[category|categories]]`. If you find yourself frequently typing `[[internalization|internal to]]`, then you might consider adding a [[redirect]] to [[internalization]] (which we've done now) so that `[[internal to]]` is redirected to [[internal to]].
  * When creating a plural link _to an existing page_, e.g. groupoids, you can now link directly to [[groupoids]] (since [[groupoids]] is redirected to the singular page [[groupoid]] now). This is preferable to [[groupoid]]s. See [[Note on Formatting|?]].

* Page titles should be uncapitalised, except for word words that are always capitalised.
  * Examples: Use `[[homotopy theory]]` instead of `[[Homotopy Theory]]`, but use `[[Lie algebra]]`.
  * Tricks: To produce '[[homotopy theory|Homotopy theory]] is important!', try `[[homotopy theory|Homotopy theory]] is important!`.
  * Reason: We want only one page on a given concept, regardless of variations in grammar.

* Except as contradicted above, use standard American English spelling conventions.
  * Examples: Use `[[internalization]]` instead of `[[internalisation]]` and hyphens as shown in the ASCII-only requirement.
  * Tricks: To produce '[[internalization|internalisation]]', try `[[internalization|internalisation]]`.
  * Reason: Most of this is written by [[Urs Schreiber]] and [[John Baez]], who use American English spelling.

* Regardless of the above, pages named after specific categories should use the capitalised singular abbreviated form.
  * Examples: Use `[[Set]]` instead `[[Sets]]` and `[[Cat]]` instead of `[[Category]]`.
  * Tricks: Although things like '$\Disc: \Set \to \Cat$' work best in math mode and even '$\Set$' alone looks most consistent that way, you have to make the link '[[Set]]' outside math mode.

# Special Typesetting Features #

##How to leave comments and questions## {#query}

If you want to make a comment or question about a page without changing its main content, then edit the page and put your comment or question in a __query block__ as shown in this example:

    +-- {: .query}
    How do I ask a question?
    =--

which produces

+-- {: .query}
How do I ask a question?
=--

Note that a query block should be less permanent than the rest of the page; once your comment is addressed or your question is answered, you can probably remove your query block.

If you want to ask a question of a specific person, then you can place a query block on their user page (which is just a page whose title is their name). You should be able to find all user pages [here](http://ncatlab.org/nlab/list/people).

If your comment or question is more general than a specific page or person, then try the [n-Forum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/).  Previous discussions have been on the [[General Discussion]] page and on an entry at the [n-Cafe](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html).  These previous discussions should not be added to but you may find your question answered there.  Important answers are being migrated to [[HowTo|this How To]] and the [[FAQ]].  As this is a Wiki, if you find an answer to your question and feel it should be added to one of those then do so.

##How to make a standout box##

If you want to make some text stand out (an important theorem, or slogan), you can do it using a __standout box__:

    +-- {: .standout}
    First quantization is a mystery, but second quantization is a functor. 
    =--

which produces

+-- {: .standout}
First quantization is a mystery, but second quantization is a functor. 
=--


## How to fiddle with the CSS (i.e. create query boxes, etc.) on your personal ncatlab web ##

As changes even to personal webs require the system password, to make such changes you need to ask a [[lab elf]] with sufficient priveleges to do this for you.  The best method of doing this is to post a request at the [n-forum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/).

However, you do not need any password to **see** the stylesheet tweaks on the various webs, so if you see a feature that you would like on one of the other webs (including the main one), then go to the "Edit Web" link at the bottom of that web\'s [[HomePage]] to view the 'Stylesheet tweaks >>'.


## How to include one page within another ##

If you have some material at a page called `foo` that you want to include directly in pages called `bar` and `baz`, then type <nowiki><code>[[!include foo]]</code></nowiki> in `bar` and `baz`.  For an example, see how [[contents]] is included at the tope of this page.  Also see how [[contents]] itself has been formatted so that it will appear as a sidebar when included.

Besides such sidebars that appear in many pages, you can also use inclusion to put in something that contains a bunch of ugly code (such as raw <abbr title="scalable vector graphics">SVG</abbr>) without mucking up the rest of the page.  That is, you put your messy code in `bar/foo` and then put <nowiki><code>[[!include bar/foo]]</code></nowiki> in `bar`.  Note that this is for something that, logically, should appear within `bar` itself, which is why `bar` appears in the name of the included page.

Note that the included page goes directly in where it is called with no surrounding whitespace.  This can mean that formatting rules are broken on the include.  For example, if the included file starts and ends with a `div` tag and is included with no surrounding blank lines then this breaks the rules and will generate an error.



## How to use redirects ##

See [[redirects]].


## How to put parentheses in external links ##

Since the mechanism for inserting links uses parentheses to delimit the link, it's not obvious how to put parentheses actually in the link itself.  Since Wikipedia uses them a fair bit, it's worth knowing how to put them in.  The trick is to use the URL codes rather than the actual characters.  URL codes are generally used to send "unsafe" characters in URLs (safe characters are `a`-`zA`-`Z0`-`9$-_.+!\*'(),`).  Although parentheses are actually "safe", due to their special meaning for the markdown filter, to put them in URLs here they need to be treated as "unsafe".  URL codes have the syntax `%hex` where `hex` is the index of the character in the ASCII character set represented as a 2-digit hexadecimal.  Wikipedia (among other places) has a [table](http://en.wikipedia.org/wiki/ASCII#ASCII_printable_characters) of the character set from which one can read off the required hexadecimal.  In particular, we see that `(` is `%28` and `)` is `%29`.  Thus

    [Monad (category theory)#Monads and adjunctions](http://en.wikipedia.org/wiki/Monad_%28category_theory%29#Monads_and_adjunctions)

produces

:  [Monad (category theory)#Monads and adjunctions](http://en.wikipedia.org/wiki/Monad_%28category_theory%29#Monads_and_adjunctions)


## How to make links to subsections of a page ##

When you create a section header, you can add an HTML anchor tag to it with the following syntax:

     ## Heading {#anchorname}

Then you can make a link to it, from that page or from another one, with the syntax:

     [a link](/nlab/show/some+page#anchorname)

Of course, you can link to it from outside the nLab by adding `http://ncatlab.org` at the beginning of the link.

Note that if you skip the first step, it is still *possible* to create a link to a subsection, since (at least if the page has a table of contents) every section on the page is automatically assigned an HTML anchor by Instiki.  However, using such links is *not* encouraged, since the automatically generated anchor names will change whenever the page is rearranged and go away if a manual anchor name is added, which will cause such links to break.

When you write a numbered theorem, you can also simultaneously create an anchor by writing:

     +-- {: .num_theorem #theoremname}
     ###### Theorem
     ...
     =--

And then you can link to it in the same way:

     [see this theorem](/nlab/show/some+page#theoremname)

When you link to a theorem on the *same* page, however, it's better to use the syntax:

     see Theorem \ref{theoremname}

(which inserts the number, as well as creates a hyperlink) since that will also work properly when the page is exported to LaTeX.


## How to add an automatically generated table of contents ##

Insert the symbols

     * tic 
     {:toc}

(including the line break!) at the position where the table of contents is to appear. Its items will be the section headlines marked by

     # top leven headline #


     ## second level headline ##


     etc.

Instead of "tic" (which is just a joke inspired by "toc" for "Table Of Contents") here you can write anything you like: this line will not be displayed but is still required. A useful thing to type is for instance

     * automatic table of contents goes here
     {:toc}

since this will indicate to everyone looking just at your source code what the command will accomplish.

It is also important that the section headings not contain anything that shouldn't go in the table of contents.  Whilst formatting is allowed, wiki-links are not (since then the entry in the table of contents would be double linked).

## How to draw commutative diagrams and pictures {#diagrams}

The itex syntax accepted by the nlab doesn't understand the syntax of any diagram-drawing package akin to xypic or tikz.  (Many of us would love to improve matters; see the [forum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/?CategoryID=2), and chime in if you have any suggestions.)  At present there are basically three ways to make diagrams: hack it together with arrays, include an image file, or include SVG.

1. _Use arrays or matrices_.  For example,

       $$
       \begin{matrix}
         (f/g)& \to & A \\
         \downarrow&\underset{\alpha}{\swarr}&\, \downarrow f\\
         B &\underset{g}{\to} & C
       \end{matrix}
       $$

   produces
   $$
   \begin{matrix}
     (f/g)& \to & A \\
     \downarrow&\underset{\alpha}{\swarr}&\, \downarrow f\\
     B &\underset{g}{\to} & C
   \end{matrix}
   $$

   In many cases, you want to tweak the alignments (say, of vertical arrows), using `\mathrlap{}` or `\mathllap{}`:

   $$
\begin{matrix}
B^{\mathrlap{A}} & \longrightarrow & 1^{\mathrlap{A}} \\
\mathllap{\scriptsize{\sigma^A}}\downarrow & & \downarrow\mathrlap{\scriptsize{t^\alpha}} \\
P(B)^{\mathrlap{A}} & \underset{\chi_\sigma^A}{\longrightarrow} & P(1)^{\mathrlap{A}}
\end{matrix}
   $$

   is produced by

        $$
        \begin{matrix}
        B^{\mathrlap{A}} & \longrightarrow & 1^{\mathrlap{A}} \\
        \mathllap{\scriptsize{\sigma^A}}\downarrow & & \downarrow\mathrlap{\scriptsize{t^\alpha}} \\
        P(B)^{\mathrlap{A}} & \underset{\chi_\sigma^A}{\longrightarrow} & P(1)^{\mathrlap{A}}
        \end{matrix}
        $$

1. _Include an image file_: This is the quick-and-dirty method.  To create the image file, either use a program like [textogif](http://www.fourmilab.ch/webtools/textogif/textogif.html) to create the image from a TeX file locally, or use a web service like [codecogs](http://www.codecogs.com/components/equationeditor/equationeditor.php).  Then follow the instructions [here](http://golem.ph.utexas.edu/instiki/show/File+Uploads) for putting it on the lab.

1. _Include SVG_: This is arguably a "better" method, since unlike an image (and like MathML) SVG can be scaled with the text, and (in theory) edited by other users without recreating the entire diagram.  There are various methods for producing SVG.  You can use a vector graphics program that produces SVG output (anyone have a good one to suggest?).  You can also just copy the SVG from another page and modify it by hand; some pages currently containing SVG diagrams are [[monoidal category]], [[oriental]] and [[comma object]].  Once you have some SVG, you can modify it by hand to put in the itex math; use the SVG `<foreignObject>` tag with a `$...$` inside it.  You need to put `markdown="1"` on the `<foreignObject>` tag, or else on a `<g>` tag containing it.

   Once you have the SVG, you can include it on a page as described [here](http://golem.ph.utexas.edu/instiki/show/SVG).  Since raw SVG is a bit ugly, you may want to put the SVG on a "subpage" by itself (with a name like `pagename > imagename`) which is included from the main page (see above for the syntax to include other pages).

   You can also use the SVG-editor to create and edit SVGs right here in the lab.  For more details see [this entry](#svgedit) below.

1. Use the CodeCogs-server to produce [xypic](http://www.tug.org/applications/Xy-pic/)-coded diagrams.

   For that, code a diagram in _xypic_ as usual. Then write the code
   _all in one line without any spaces_ and in addition replace all
   appearances of the symbol "&" with "%26".

   Then add the line

        <img src="http://latex.codecogs.com/gif.latex?YOUR-CODE-GOES-HERE" />

    in the $n$Lab page where the diagram should appear. This will make some server somewhere on this planet produce an image displaying the desired diagram.

   For instance 

        <img src="http://latex.codecogs.com/gif.latex?\xymatrix{(f/g)\ar[r]\ar[d]%26A\ar[d]^f\ar[dl]^\alpha\\B\ar[r]_g%26C}" />

   produces

   <img src="http://latex.codecogs.com/gif.latex?\xymatrix{(f/g)\ar[r]\ar[d]%26A\ar[d]^f\ar[dl]^\alpha\\B\ar[r]_g%26C}" />

# How to use the SVG editor {#svgedit}

There is now a WYSIWYG SVG-editor embedded within Instiki (the software running the nLab).  The homepage for this editor is [here](http://code.google.com/p/svg-edit/). The Instiki implementation is not feature-complete, yet. In particular, it should be possible to embed itex equations, but those don't show up in the editor (currently).

## Quick Start

1. Click "Edit page" on a page in which you wish to insert an SVG diagram.
2. Click in the edit box where you want the diagram to go.
3. In the list on the right-hand side above the links to the formatting tips is a button labelled "Create SVG graphic".  Click on this.  Note: if you forget to do step 2, you won't be able to click on this button.
4. The SVG-editor will now launch in a new window.  Create your SVG.
5. When you are done, select "Save SVG" from the file menu.  The SVG code will now appear in the edit box of the page.
6. To edit an **existing** SVG, select the text between (and including) the `<svg>` and `</svg>` tags (but **don't** include any whitespace before or afterwards).  The "Create SVG" button changes to "Edit existing SVG graphic". 

+-- {: style="text-align:center"}
<svg width="277" height="172" xmlns="http://www.w3.org/2000/svg" se:nonce="42945" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_42945_fw" viewBox="0 0 10 10">
   <path fill="#000000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <path marker-end="url(#se_arrow_42945_fw)" id="svg_42945_5" d="m39.5,28.85708c37.004852,-4.90707 137.927185,-3.90707 198,31.14292" stroke-width="2" stroke="#000000" fill="none"/>
  <path marker-end="url(#se_arrow_42945_fw)" id="svg_42945_6" d="m26.5,46c1.770121,48.323517 47.793098,104.441177 77.000008,106" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_arrow_42945_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_42945_7" y2="135" x2="116.5" y1="87" x1="114.5"/>
  <line marker-end="url(#se_arrow_42945_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_42945_8" y2="72" x2="235.5" y1="71" x1="146.5"/>
  <line stroke-dasharray="5,5" marker-end="url(#se_arrow_42945_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_42945_9" y2="60" x2="86.5" y1="40" x1="42.5"/>
  <foreignObject height="20" width="44" font-size="16" id="svg_42945_10" y="61" x="89">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>Y</mi>
      <mspace width="thinmathspace"/>
      <mo>&#215;</mo>
      <mspace width="thinmathspace"/>
      <mi>Z</mi>
     </mrow>
     <annotation encoding="application/x-tex">Y\, \times\, Z</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="20" font-size="16" id="svg_42945_11" y="139.45001" x="105">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>Z</mi>
     </mrow>
     <annotation encoding="application/x-tex">Z</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="20" font-size="16" id="svg_42945_12" y="62.45001" x="233">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>Y</mi>
     </mrow>
     <annotation encoding="application/x-tex">Y</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="20" font-size="16" id="svg_42945_13" y="22.45001" x="17">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>X</mi>
     </mrow>
     <annotation encoding="application/x-tex">X</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
=--

## Hints and Tips

1. The editor does not present all options straight away. For example, to get an arrow, you first need to draw a straight line. Then select that straight line (using the selection tool (denoted by an arrow) at the top of the left-hand menu) and a new list of options will appear. One of them is the choice of arrow type.

2. To get a curved arrow, you use another of the options --- the one to turn the line into a 'path'. After turning the line into a path, double-click on it. This brings up the path options, which include whether the path should be 'straight' or 'curved'. Curved paths are [cubic B&#233;zier curves](http://en.wikipedia.org/wiki/B&#233;zier_curve) and can also have arrowheads.

3. You can clone an existing element (an arrow, say), using the rubber-stamp tool.

4. To get rid of any extraneous whitespace around the picture, go to the "Main Menu" (the funny looking button top left) and select "Document Properties".  There you can set the size of the SVG, including "fit to content".  Only do this once the SVG is finished.

# Other Sources of Information #

## Instiki HowTo ##

For general information and help with Instiki, see the [Instiki](http://golem.ph.utexas.edu/instiki/show/HomePage) wiki.

Here are some useful specifics:
* [Use basic Markdown syntax](http://daringfireball.net/projects/markdown/syntax)
* [Make tables, footnotes, etc](http://maruku.rubyforge.org/maruku.html#extra)
* [Add definitions and theorems](http://golem.ph.utexas.edu/instiki/show/Theorems)
* [Add metadata to your markup](http://maruku.rubyforge.org/proposal.html)
* [Type itex equations](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html)
* [Use wiki syntax](http://golem.ph.utexas.edu/instiki/show/Syntax#wiki)
* [Embed SVG in equations](http://golem.ph.utexas.edu/instiki/show/SVG)
* [Upload files](http://golem.ph.utexas.edu/instiki/show/File+Uploads)
* [Use keyboard shortcuts](http://golem.ph.utexas.edu/instiki/show/AccessKeys)
* [Make slideshows](http://golem.ph.utexas.edu/instiki/show/S5)
* [SVG Editor](http://code.google.com/p/svg-edit/) Homepage for the SVG editor project.

## survey of available math typesetting commands ##

* [itex2MML Command Summary](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html)

category: meta
