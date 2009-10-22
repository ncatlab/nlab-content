[[!include contents]]

An easy introduction for elementary basics is

* [[How to get started]].

The following provides more details.

See also the [[FAQ]].

# Contents

* Automatic table of contents
{: toc}

# Technical #

## Software required to use the $n$Lab ##

The $n$Lab displays mathematical symbols using [MathML](http://en.wikipedia.org/wiki/MathML).  Displaying MathML requires support from your web browser.  The browser with the best support for MathML is [Firefox](http://www.mozilla.com/firefox/), especially if you install the [STIX fonts](http://www.mozilla.org/projects/mathml/fonts/).  Firefox is a great browser in many other ways too, so if you aren't using it, why not give it a try?

Recent versions of Opera also apparently support MathML.  For InternetExplorer, one needs to install the [MathPlayer](http://www.dessci.com/en/products/mathplayer/) plugin. Download is quick and easy and free, but installation may require Administrator privileges on your computer.  Other browsers such as Safari and Chrome seemingly do not support MathML at present.

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


## How to customize the nLab ##

(Firefox - and clones - specific)

You may wish to customize the font scheme (both for math or text) on the nLab, as well as tweak things such as the small edit box for comments. Try the [nLab Stylish theme](http://userstyles.org/styles/17934) theme if you are using Firefox. (Stylish is a plug-in for firefox enabling you to customize websites; it is available [here](https://addons.mozilla.org/en-US/firefox/addon/2108)). The nLab theme changes the fonts on the nLab to a serif-style, and makes the edit box much bigger for an overall more pleasant experience! Experienced users can also do this themselves by tweaking the CSS. You might also want to try a Firefox [extension](https://addons.mozilla.org/en-US/firefox/addon/4125) which allows you to edit the text box using your favourite text editor. 

## How to Download a Local Copy of the n-Lab ##

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

Hit "edit page" to see how pages are coded. Use the [[Sandbox|Sandbox]] to warm up.

**Creating a new page** is done by 

 * first creating a preliminary link (represented by a question mark) by entering double square brackets;

 * then clicking on the question mark and following the instructions.

_Watch out_: the name of a page is case sensitive, so make your link lowercase if it comes at the beginning of a sentence. (`[[like this|Like this]]`.) We loosely agreed to try to follow that and some other naming conventions; see below.

However, this is less of an issue now that we have [[redirects]].

##Note to new contributors##

When you edit a page, you can (and should) put your name (with normal capitalisation and spacing) in the box after 'Submit as'. If you don\'t, then your contribution will be credited to the [[AnonymousCoward]].

Once you edit a page for the first time, your name will appear at the bottom, grayed out with a question mark since there is no page with your name yet.  You may take this as an invitation to create a user page and tell us about yourself.  But if you don't want to or don't have the time right now, you can forget about this. If you just want to show up on [category: people](http://www.ncatlab.org/nlab/list/people), then you make a page containing only 'category: people' (or someone else may do this for you).

To create your user page, simply click the question mark that appears next to your name at the bottom of the page after making a modification and add content to the edit box that appears. If you'd like to make a user page prior to modifying an existing page, you can do so by making some trivial modification to the [[Sandbox]], which will put your name at the bottom of the page where you can click the question mark. (Or hack the URL.)

## Naming conventions ##

These are not set in stone, but we\'re following them for now. Most days, [[Toby Bartels]] goes around and corrects any violations (while reading the new material). But changing page titles results in unnecessary kruft (in [category: redirect](http://www.ncatlab.org/nlab/list/redirect)), so you should try to follow these if possible (or dispute them if not!).

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

##How to leave comments and questions##

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

If your comment or question is more general than a specific page or person, then try the [n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum).  Previous discussions have been on the [[General Discussion]] page and on an entry at the [n-Cafe](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html).  These previous discussions should not be added to but you may find your question answered there.  Important answers are being migrated to [[HowTo|this How To]] and the [[FAQ]].  As this is a Wiki, if you find an answer to your question and feel it should be added to one of those then do so.

##How to make a standout box##

If you want to make some text stand out (an important theorem, or slogan), you can do it using a __standout box__:

    +-- {: .standout}
    First quantization is a mystery, but second quantization is a functor. 
    =--

which produces

+-- {: .standout}
First quantization is a mystery, but second quantization is a functor. 
=--

## How to fiddle with the CSS (i.e. create query boxes, etc.) on your personal ncatlab space ##

To fiddle with the CSS code, go to "Edit web" on the main page of your wiki, and then click on "Stylesheat tweaks". Here you can add new CSS gismos like query boxes and standout boxes. These kind of gismos come from the mechanism of putting CSS classes into the Markdown syntax, in the  [same way](http://golem.ph.utexas.edu/~distler/blog/archives/001820.html) that Jacques created the Theorem environments in Instiki. In other words, a query box is like a theorem environment: it's a way in Markdown to create an HTML block with a specific id, which you can then style in the CSS. You can grab the CSS code for query boxes from the main nLab page. It requires a password to change the CSS, but to view it does not require one. 


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


##How to add an automatically generated table of contents##

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

## How to draw commutative diagrams and pictures

The itex syntax accepted by the nlab doesn't understand the syntax of any diagram-drawing package akin to xypic or tikz.  (Many of us would love to improve matters; see the [forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/?CategoryID=2), and chime in if you have any suggestions.)  At present there are basically three ways to make diagrams: hack it together with arrays, include an image file, or include SVG.

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

## survey of available math typesetting commands ##

* [itex2MML Command Summary](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html)

category: meta