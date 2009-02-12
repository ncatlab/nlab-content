# Frequently Asked Questions

Also including questions that should be frequently asked but aren't.

### Instiki features and "features"

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

   You can get nicer-looking output by using SVG.  The way to get math into the SVG is to use the SVG `<foreignObject>` tag with itex math `$...$` inside it.  As in the previous question, for this to work you need to put `markdown="1"` on the `<foreignObject>` tag or else on a `<g>` tag containing it.

   As for how to get the SVG itself, including the arrows, there are several options.  You can use a vector graphics program that produces SVG output (anyone have a good one to suggest?).  You'll probably have to modify it by hand, though, to put in the itex math.  You can also just copy the SVG from another page and modify it by hand; some pages currently containing SVG diagrams are [[monoidal category]] and [[comma object]].

1. *My reference cites the wrong theorem*

    If you want to use references with numbered theorems and the like then there has to be a reference for _every_ numbered theorem.
    Specifically, if you want to reference a particular theorem then every previous numbered theorem has to have a label otherwise the counters are not synchronised.
    (This is an unfortunate but necessary consequence of being able to easily add new theorem-like environments via CSS.)

### _n_-Lab Specifics

1.  *Why did my page get redirected?*

    Did you read the _Naming Conventions_ section on the HowTo?

1.  *Where do I ask a question?*

    How many times have you wanted to ask it?  If more than three times, put it here (*joke*!).

    Seriously, if about a specific page then put it on that page in a query block:

        +-- {: .query}
        How do I prove the Riemannian Hypothesis?
        =--

    If about the _n_-Lab then try the [n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum).
    If about something mathematical then try to convince [[John Baez|John]], [[Urs Schreiber|Urs]], or [[David Corfield|David]] to start a blog entry on the _n_-Category Caf&eacute; about it.

category:meta