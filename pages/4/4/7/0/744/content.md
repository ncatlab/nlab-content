# Frequently Asked Questions #

* tic
{:toc}

Also including questions that should be frequently asked but aren't.  See also [[HowTo]].

## Instiki features and "features" ##

### How do I put math inside HTML?

By default, the itex syntax `$...$` is disabled inside raw HTML.  However, you can re-enable it by giving the HTML parameter `markdown="1"`.  Thus

    <table markdown="1"><tr><td>I can has $m^a_t \hbar$!!</td></tr></table>

produces

<table markdown="1"><tr><td>I can has $(m^a)_t \hbar$!!</td></tr></table>

However, for tables you can also use the [PHP Markdown Extra](http://michelf.com/projects/php-markdown/extra/#table) syntax inside which `$...$` works without a problem.

### How do I make commutative diagrams?

See the [[HowTo]]

### My reference cites the wrong theorem

If you want to use references with numbered theorems and the like then there has to be a reference for _every_ numbered theorem.

Specifically, if you want to reference a particular theorem then every previous numbered theorem has to have a label otherwise the counters are not synchronised.

(This is an unfortunate but necessary consequence of being able to easily add new theorem-like environments via CSS.)

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

* Numbers include punctuation.  Periods and commas _within_ numbers are numbers.  This is so that `$1,000,000.00$` (or `$1.000.000,00$` if you are European) renders correctly as $1,000,000.00$ and not ${1},{000},{000}.{00}$.  When combined with the previous difference, this means that `$t^3,2$` renders as $t^3,2$ instead of $t^{3},2$.  Either use braces or spaces.

* Operator names.  Since iTeX does not have macro support, extending the list of operator names would be difficult except for the fact that neighbouring strings of letters get combined into an operator name.  Thus `$cos$` produces $cos$.  However, in LaTeX this produces $c o s$.  Where the operator name is a standard LaTeX one, such as `\cos`, the backslash can be added so `$\cos$` renders correctly in both cases.  Where the operator name is not a standard LaTeX one, say `Poly`, the **safe** syntax is to use `\operatorname`; thus `$\operatorname{Poly}$` renders correctly as $\operatorname{Poly}$ in both situations.  If you *don\'t* want an operator name, then use spaces; thus `$c o s$` produces $c o s$.

* Whitespace in embedded text.  In LaTeX `$x \text{ and } y$` renders as $x\;\text{and}\;y$ but in iTeX it renders as $x\text{ and }y$.  This is because MathML says that fore and aft whitespace on `mtext` elements should be swallowed.  The **safe** syntax is `$x\;\text{and}\;y$`.

* Two-character relations.  In LaTeX, two neighbouring relation symbols are combined into one relation symbol.  Thus `$y := f(x)$` becomes $y \mathrel{:=} f(x)$, while `$y = -f(x)$` becomes $y = -f(x)$ because a minus sign is a unary operator instead of a binary relation.  Since MathML doesn\'t know the difference between unary operators and binary relations, it is inconvenient for iTeX to do this, so `$y := f(x)$` comes out as $y := f(x)$ instead.  The __safe__ syntax is `$y \mathrel{:=} f(x)$`, which produces $y \mathrel{:=} f(x)$.  However, in many cases, there is a combined command that you can use.  In this case, `$y \coloneqq f(x)` produces $y \coloneqq f(x)$.  This method is better when [available](http://golem.ph.utexas.edu/~distler/blog/itex2MMLcommands.html); even in LaTeX, it will adjust the vertical positioning a bit to look nice.

## HTML, XML, etc.

### How do I get accented characters?

You can use HTML/XML/SGML [character entity references](http://www.w3schools.com/tags/ref_entities.asp).  If the character you want has a mnemonic HTML name, like &amp;eacute; for &eacute;, you can use that.  Otherwise, you can use an SGML numerical code, like &amp;#x34AB; for &#x34AB;, that corresponds directly to Unicode.  To look up the numbers for SGML characters, try the [Unicode Character Names Index](http://unicode.org/charts/charindex.html).  [[Toby Bartels|Toby]] has a [complete list of HTML and XML character entity references](http://tobybartels.name/characters/) (or try the Unicode Databank pages listed below) with individual pages where you can check browser compliance (originally for when you couldn\'t take even things like &amp;harr; for granted, but even now &amp;lrm; and &amp;thinsp; may be lacking).  While you can use this technique for mathematical symbols too, it\'s best to do those in iTeX as explained above.

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

* __NB.__  Depending on your font settings, the less ordinary symbols may look better if you enclose them in a TeX + \text wrapper.  Cf and Contrast:
  1. direct : `&#8472;` or <code>&amp;weierp;</code> or `&#x2118;` &rarr; '&#8472;'
  1. TeX : <code>$&amp;weierp;$</code> or `$&#x2118;$` (but not `$&#8472;$`) &rarr; '$&#x2118;$'
  1. TeX + \text : `$\text{&#8472;}$` or <code>$\text{&amp;weierp;}$</code> or `$\text{&#x2118;}$` &rarr; '$\text{&#8472;}$'

## _n_-Lab Specifics

### Why did my page get redirected?

Did you read the _Naming Conventions_ section on the [[HowTo]]?

### Where do I ask a question?

How many times have you wanted to ask it?  If more than three times, put it here (*joke*!).

Seriously, if about a specific page then put it on that page in a query block:

    +-- {: .query}
    How do I prove the Riemannian Hypothesis?
    =--

If about the _n_-Lab then try the [n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum).

If about something mathematical then try to convince [[John Baez|John]], [[Urs Schreiber|Urs]], or [[David Corfield|David]] to start a blog entry on the _n_-Category Caf&eacute; about it.

### How can I get a personal section of the nLab?

Some users have personal areas of the _n_-Lab where they can have password protected pages and do work without fitting it into the rest of _n_-Lab.  If you would like to have such an area, email [[Urs Schreiber|Urs]].

category:meta
