# Frequently Asked Questions

Also including questions that should be frequently asked but aren't.  See also [[HowTo]].

## Instiki features and "features"

1. *How do I put math inside HTML?*

   By default, the itex syntax `$...$` is disabled inside raw HTML.  However, you can re-enable it by giving the HTML parameter `markdown="1"`.  Thus

       <table markdown="1"><tr><td>I can has $m^a_t \hbar$!!</td></tr></table>

   produces

   <table markdown="1"><tr><td>I can has $(m^a)_t \hbar$!!</td></tr></table>

   However, for tables you can also use the [PHP Markdown Extra](http://michelf.com/projects/php-markdown/extra/#table) syntax inside which `$...$` works without a problem.

1. *How do I make commutative diagrams?*

   One answer is to use the `\array` command of itex.  For example,

       $$\array{A & \to & B\\ \downarrow && \downarrow \\ C & \to &D}$$

   produces

   $$\array{A & \to & B\\ \downarrow && \downarrow \\ C & \to &D}$$

   or 

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

   You can get nicer-looking output by using SVG.  The way to get math into the SVG is to use the SVG `<foreignObject>` tag with itex math `$...$` inside it.  As in the previous question, for this to work you need to put `markdown="1"` on the `<foreignObject>` tag or else on a `<g>` tag containing it.

   As for how to get the SVG itself, including the arrows, there are several options.  You can use a vector graphics program that produces SVG output (anyone have a good one to suggest?).  You'll probably have to modify it by hand, though, to put in the itex math.  You can also just copy the SVG from another page and modify it by hand; some pages currently containing SVG diagrams are [[monoidal category]], [[oriental]] and [[comma object]].

1. *My reference cites the wrong theorem.*

    If you want to use references with numbered theorems and the like then there has to be a reference for _every_ numbered theorem.
    Specifically, if you want to reference a particular theorem then every previous numbered theorem has to have a label otherwise the counters are not synchronised.
    (This is an unfortunate but necessary consequence of being able to easily add new theorem-like environments via CSS.)

1. *My math doesn't look like math.*

   One of the notable ways in which itex differs from latex is that in itex's math mode, a string of letters without spaces in between is interpreted as a single identifier.  This has the advantage that you can invent new identifiers without needing to use `\operatorname` or `\DeclareMathOperator`, but it means that when you _don't_ want a string of letters interpreted that way you need to put spaces in between.  For example, `$sin(x)$` produces $sin(x)$ which is probably what you want, but `$h=gf$` produces $h=gf$, whereas you probably wanted to write `$h=g f$` to get $h=g f$. On the other hand, you can (and, for the sake of the LaTeX output, probably should) use `$\sin(x)$`, etc.

1. *Lists are acting strangely.*

   There are several bugs (or "edge cases") in the handling of lists by Maruku (the formatting filter used by Instiki).  These include:

   * [single-element unordered lists](http://rubyforge.org/tracker/index.php?func=detail&aid=22109&group_id=2795&atid=10735)
   * [indentation by more than one space](http://rubyforge.org/tracker/index.php?func=detail&aid=8862&group_id=2795&atid=10735)

## HTML, XML, etc.

1. *How do I get accented characters?*

   You can use HTML/XML/SGML [character entity references](http://www.w3schools.com/tags/ref_entities.asp).  If the character you want has a mnemonic HTML name, like &amp;eacute; for &eacute;, you can use that.  Otherwise, you can use an SGML numerical code, like &amp;#x34AB; for &#x34AB;, that corresponds directly to Unicode.  To look up the numbers for SGML characters, try the [Unicode Character Names Index](http://unicode.org/charts/charindex.html).  [[Toby Bartels|Toby]] has a [complete list of HTML and XML character entity references](http://toby.bartels.name/characters/) with individual pages where you can check browser compliance (originally for when you couldn\'t take even things like &amp;harr; for granted, but even now &amp;lrm; and &amp;thinsp; may be lacking).  While you can use this technique for mathematical symbols too, it\'s best to do those in iTeX as explained above.

## _n_-Lab Specifics

1.  *Why did my page get redirected?*

    Did you read the _Naming Conventions_ section on the [[HowTo]]?

1.  *Where do I ask a question?*

    How many times have you wanted to ask it?  If more than three times, put it here (*joke*!).

    Seriously, if about a specific page then put it on that page in a query block:

        +-- {: .query}
        How do I prove the Riemannian Hypothesis?
        =--

    If about the _n_-Lab then try the [n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum).
    If about something mathematical then try to convince [[John Baez|John]], [[Urs Schreiber|Urs]], or [[David Corfield|David]] to start a blog entry on the _n_-Category Caf&eacute; about it.

category:meta