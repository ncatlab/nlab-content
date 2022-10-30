
# Frequently Asked Questions
* tic
{:toc}

Also including questions that should be frequently asked but aren't.  See also [[HowTo]].

## Instiki features and "features"

### How do I make less-than and greater-than signs?

The characters < and > are interpreted as beginning or ending HTML tags.  To make a less-than or greater-than sign in iTeX math mode, use `\lt` and `\gt` respectively.  For example, `$0\lt 1$` produces $0\lt 1$.


### How do I put math inside HTML? {#markdown1}

By default, the itex syntax `$...$` is disabled inside raw HTML.  However, you can re-enable it by giving the HTML parameter `markdown="1"`.  Thus

    <table markdown="1"><tr><td>I can has $m^a_t \hbar$!!</td></tr></table>

produces

<table markdown="1"><tr><td>I can has $(m^a)_t \hbar$!!</td></tr></table>

(Well, that *used* to work, but it seems to have broken along the way!)

At least for tables, you can also use the [PHP Markdown Extra](http://michelf.com/projects/php-markdown/extra/#table) syntax inside which `$...$` works without a problem.


### How do I make commutative diagrams?

See the [[HowTo]]

### My math doesn't look like math

One of the notable ways in which itex differs from latex is that in itex's math mode, a string of letters without spaces in between is interpreted as a single identifier.  This has the advantage that you can invent new identifiers without needing to use `\operatorname` or `\DeclareMathOperator`, but it means that when you _don't_ want a string of letters interpreted that way you need to put spaces in between.  For example, `$sin(x)$` produces $sin(x)$ which is probably what you want, but `$h=gf$` produces $h=gf$, whereas you probably wanted to write `$h=g f$` to get $h=g f$. On the other hand, you can (and, for the sake of the LaTeX output, probably should) use `$\sin(x)$`, etc.

### Lists are acting strangely.

There are several bugs (or "edge cases") in the handling of lists by Maruku (the formatting filter used by Instiki).  These include:

* [single-element unordered lists](http://rubyforge.org/tracker/index.php?func=detail&aid=22109&group_id=2795&atid=10735)
* [indentation by more than one space](http://rubyforge.org/tracker/index.php?func=detail&aid=8862&group_id=2795&atid=10735)

### My LaTeX produces gobbledygook in iTeX and vice versa.

iTeX is not LaTeX.  iTeX is a pure converter whereas LaTeX is a mixture of a converter and renderer (technically, latex is the rules for converting the input into pure TeX which is then rendered by tex, but since the conversion is also handled by tex, it can cheat and use information about the rendered output to reinterpret the input).  Therefore getting the two to do exactly the same is **never** going to happen.

On the other hand, the aim is to keep iTeX as close as possible to standard LaTeX whilst keeping in mind that iTeX produces MathML.  Their similarity can make the differences all the more jarring.  Here is a list of the differences that we know about together with suggested work-arounds.

* Numbers are one thing.  The syntax `$10^10$` produces $10^10$ in iTeX but $10^{1}0$ in LaTeX.  The **safe** syntax is to always use braces: `$10^{10}$` is consistent.

* Numbers include punctuation.  Periods and commas _within_ numbers are numbers.  This is so that `$1,000,000.00$` (or `$1.000.000,00$` if you are European) renders correctly as $1,000,000.00$ and not ${1},{000},{000}.{00}$.  When combined with the previous difference, this means that `$t^3.2$` renders as $t^3.2$ instead of $t^{3}.2$.  Either use braces or spaces.  (However, for some reason, `$t^3,2$` renders as $t^3,2$ like you\'d expect from TeX, so the two differences don\'t interact entirely logically.  This might have been different in earlier versions of iTeX.)

* Operator names.  Since iTeX does not have macro support, extending the list of operator names would be difficult except for the fact that neighbouring strings of letters get combined into an operator name.  Thus `$cos$` produces $cos$.  However, in LaTeX this produces $c o s$.  Where the operator name is a standard LaTeX one, such as `\cos`, the backslash can be added so `$\cos$` renders correctly in both cases.  Where the operator name is not a standard LaTeX one, say `Poly`, the **safe** syntax is to use `\operatorname`; thus `$\operatorname{Poly}$` renders correctly as $\operatorname{Poly}$ in both situations.  If you *don\'t* want an operator name, then use spaces; thus `$c o s$` produces $c o s$.

* Whitespace in embedded text.  In LaTeX `$x \text{ and } y$` renders as $x\;\text{and}\;y$ but in iTeX it renders as $x\text{ and }y$.  This is because MathML says that fore and aft whitespace on `mtext` elements should be swallowed.  The **safe** syntax is `$x\;\text{and}\;y$`.

* Two-character relations.  In LaTeX, two neighbouring relation symbols are combined into one relation symbol.  Thus `$y := f(x)$` becomes $y \mathrel{:=} f(x)$, while `$y = -f(x)$` becomes $y = -f(x)$ because a minus sign is a unary operator instead of a binary relation.  Since MathML doesn\'t know the difference between unary operators and binary relations, it is inconvenient for iTeX to do this, so `$y := f(x)$` comes out as $y := f(x)$ instead.  The __safe__ syntax is `$y \mathrel{:=} f(x)$`, which produces $y \mathrel{:=} f(x)$.  However, in many cases, there is a combined command that you can use.  In this case, `$y \coloneqq f(x)$` produces $y \coloneqq f(x)$.  This method is better when [available](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html); even in LaTeX, it will adjust the vertical positioning a bit to look nice.

* Non-ascii characters.  iTeX is designed only to parse the mathematical sections of any page and so it assumes that any strange characters will be generated via iTeX commands such as `\infty` instead of being directly input as ?.  iTeX actually takes an extreme view on this and will not parse mathematics if it includes non-ascii characters.  In ordinary mathematics this should not be a problem since one should use the iTeX commands themselves to produce such characters.  Where it can be a problem is in `\text` commands embedded in mathematics because these are **still** parsed by iTeX even though it does nothing with them.  Thus `\text{?}` is not a legal construct and will simply produce $\text{?}$.  Since iTeX does not allow nesting, the construction `\text{$\infty$}` will not work.  There are two possibilities:
   1. Break the `\text` command: `\text{in~}\infty{-categories}` produces $\text{in}\;\infty{-categories}$ (note the forced space, simple whitespace there will not work).
   2. Use **numbered** entities: `\text{in ∞-categories` produces $\text{in ∞-categories}$.  Named entities will not work here as they get converted to unicode internally before being sent to the iTeX parser.

### I searched for a page that I know exists, but I couldn't find it

Instiki's search uses regular expressions.  That means you can do all sorts of fancy searches, but it also means that pages with special characters in their names are hard to search for.  For instance, if you search for `(n,r)-category` you will come up with nothing, because Instiki interprets the parentheses as a regular expression grouping construct.  To search for actual parentheses, you need to backslash them: search instead for `\(n,r\)-category`.

### Why is there no "Preview" button?

Instiki's philosophy is that the "Preview" button is the one labeled "Save".  If you don't like the result, just click "Edit" again.  Multiple edits by the same person within a 30 minute interval are collapsed into a single "edit" in the revision history.

One merit of this approach is that in the case when your preview was correct and doesn't require re-editing, it saves you an extra click.  Another is that it prevents you from ever *forgetting* to make the extra click.


### itex is a pain, why do you guys use MathML? {#WhyMathML}

Many web sites "support" LaTeX by running it through a script which converts LaTeX equations to image files for display.  While this produces acceptable results for many users, it is not true "support" for mathematics.  Images can sometimes be hard to see, and the user cannot easily resize them or change their color or font, nor can software easily read them aloud to a blind user.  In contrast, MathML is a markup language, like HTML, specifically designed to carry information not only about the display of mathematics, but its content and meaning.  A suitable client application can resize MathML along with the rest of the page, change its color or font, or even read it aloud, making MathML a much more accessible way to display mathematics.  See, for instance, [this comment](http://terrytao.wordpress.com/2009/10/29/displaying-mathematics-on-the-web/#comment-42119).

### I want to help out with the software, what can I do?

See [this discussion](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1112).


## HTML, XML, etc.

### How do I get accented characters?

You can use HTML/XML/SGML [character entity references](https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references).  If the character you want has a mnemonic HTML name, like &amp;eacute; for &eacute;, you can use that.  Otherwise, you can use an SGML numerical code, like &amp;#x34AB; for &#x34AB;, that corresponds directly to Unicode.  To look up the numbers for SGML characters, try the [Unicode Character Names Index](http://unicode.org/charts/charindex.html).  [[Toby Bartels|Toby]] has a [complete list of HTML and XML character entity references](http://tobybartels.name/characters/) (or try the Unicode Databank pages listed below) with individual pages where you can check browser compliance (originally for when you couldn\'t take even things like &amp;harr; for granted, but even now &amp;lrm; and &amp;thinsp; may be lacking).  While you can use this technique for mathematical symbols too, it\'s best to do those in iTeX as explained above.

* [Unicode Data Bank](http://www.sql-und-xml.de/unicode-database/) pages:
  1.  [Math Symbols](http://www.sql-und-xml.de/unicode-database/sm.html)
  1.  [Math Operators](http://www.sql-und-xml.de/unicode-database/mathematical-operators.html)
  1.  [Math Miscellaneous A](http://www.sql-und-xml.de/unicode-database/miscellaneous-mathematical-symbols-a.html)
  1.  [Math Miscellaneous B](http://www.sql-und-xml.de/unicode-database/miscellaneous-mathematical-symbols-b.html)
  1.  [Letterlike Symbols](http://www.sql-und-xml.de/unicode-database/letterlike-symbols.html)
  1.  [Miscellaneous Symbols](http://www.sql-und-xml.de/unicode-database/miscellaneous-symbols.html)
  1.  [General Punctuation](http://www.sql-und-xml.de/unicode-database/general-punctuation.html)
  1.  [Open Punctuation](http://www.sql-und-xml.de/unicode-database/ps.html)
  1.  [Other Punctuation](http://www.sql-und-xml.de/unicode-database/po.html)
  1.  [Close Punctuation](http://www.sql-und-xml.de/unicode-database/pe.html)
  1.  [Geometric Shapes](http://www.sql-und-xml.de/unicode-database/geometric-shapes.html)
  1.  [Other Symbols](http://www.sql-und-xml.de/unicode-database/so.html)
  1.  [Dingbats](http://www.sql-und-xml.de/unicode-database/dingbats.html)

* __NB.__  Depending on your font settings, the less ordinary symbols may look better if you use "iTeX + \text + numerical entity".  Compare and contrast:
  1. direct : `&#8472;` or <code>&amp;weierp;</code> or `&#x2118;` &rarr; '&#8472;'
  1. iTeX : `$&#x2118;$` (but not `$&#8472;$` or <code>$&amp;weierp;$</code>) &rarr; '$&#x2118;$'
  1. iTeX + \text + numerical entity: `$\text{&#x2118;}$` &rarr; '$\text{&#x2118;}$'

## _n_-Lab Specifics

### Why did my page get redirected?

Did you read the _Naming Conventions_ section on the [[HowTo]]?

### Where do I ask a question? {#AskAQuestion}

How many times have you wanted to ask it?  If more than three times, put it here (*joke*!).

Seriously, if about a specific page then put it on that page in a query block:

    +-- {: .query}
    How do I prove the Riemannian Hypothesis?
    =--

If about the _n_-Lab then try the [n-Forum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/).

If about something mathematical then try to convince [[John Baez|John]], [[Urs Schreiber|Urs]], or [[David Corfield|David]] to start a blog entry on the _n_-Category Caf&eacute; about it.

### How do I cite a page on the nLab? {#Citing}

You should, of course, include a link or URL to the page or pages that you wish to cite.  You should also give the information about which *version* of the page you are citing, since pages change over time.  The version number can be found as follows: look at the bottom of the page where it says "Back in time ($N$ revisions)"; the current version number is $N+1$.

You can link directly to the version you want to cite by using a url such as

    http://ncatlab.org/nlab/revision/PageName/VERSIONNUMBER

We recommend that if you only include one URL, it be of the form `show/PageName` which will point to whatever version of the page is current when it is accessed.  This is because pages generally improve over time, and whoever is following your reference ought to be taken to the best, up-to-date version of the page.  Anyone who cares about finding the exact version of the page that you cited can figure out how to find it in the history.

On the other hand, if you can give two URLs (this would be cumbersome in a printed paper, but is possible with links on a web page), then it may be helpful to give the appropriate `revision` link as well as the `show` one.


### I want to help, but writing math on a wiki is scary; what can I do?

There are numerous ways you can help out and get acquainted with the community even if you don't (yet) feel comfortable writing math publically on a wiki.

1.  You can do [[lab elf]] duty, such as correcting typos and spelling errors, fixing links, creating links, creating redirects (there are many pages that still need redirects created for alternate and plural forms of the title), organizing pages, and so on.

2.  You can ask questions (see previous question), and join discussions, at the nForum, and comment at the nCafe.

3.  You can try writing small additions to existing pages, for instance a paragraph or two that helps explain something that puzzled you initially.  If you aren't entirely positive that what you wrote was correct, when you announce your edit at Latest Changes on the nForum, you can mention that you're unsure and someone will usually reassure you or give a correction.

4.  If you don\'t sign your edits, then they are attributed to the [[AnonymousCoward]].  We prefer that you sign your edits, but anonymous help is better than none at all, so that option is available to you.

### How can I get a personal section of the nLab?

Some users have personal areas of the _n_-Lab where they can have password protected pages and do work without fitting it into the rest of _n_-Lab.  If you would like to have such an area, ask the [[nlabmeta:steering committee|steering committee]].

### I got "Access denied" when editing a page.

The _n_-Lab has a spam filter that checks your IP against a blacklist.  The blacklists used are maintained by [spamcop.net](http://www.spamcop.net/) and [spamhaus.org](http://www.spamhaus.org/).  IPs are added to these lists if they are detected doing things usually associated with computers infected with viruses.  There are instructions on the webpages for finding out if your IP has been added to these lists and what to do to remove your IP from them.  Three things to point out are:

1. The _n_-Lab cannot remove your IP from the list, you have to do that yourself.
2. The _n_-Lab is not going to remove its spam protection.
3. If you got your IP dynamically (e.g. using some wireless providers) it is entirely possible that it is not your computer that was behaving badly but a previous one using the same IP.  A quick workaround is to disconnect from the network and try reconnecting (sometimes you have to wait a bit before reconnecting to get a new IP).  Of course, you should ensure that your virus software is up to date.

### I got "Internal application error" when doing something.

Sometimes something doesn't work quite right with the software and it bails out.  If you think that you were doing something that should work, please log the error message at the [n-Forum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/).  The more information that you log, the easier it is for us to debug.  Useful information is: your IP, the time and date, and the URL that you were trying to access.

There is actually more information contained in the HTML source of the error message ("view source"): some errors can be down to malformed input when editing a page and that can help you fix it yourself.


category: meta
