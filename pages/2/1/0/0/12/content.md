[[!include contents]] 

Every wiki needs a sandbox! Just test _below_ and don't worry about messing things up.

****

\emph{Can we emphasize text?}

*Yes, we can emphasize text.*

Trying to upload a file: [[n.png:pic]].... nope didn't work, I get "Internal Server Error".

Okay worked this time. [[Bruce Bartlett]]

$$\array{\arrayopts{\rowalign{center}}\begin{svg}
<svg xmlns="http://www.w3.org/2000/svg" width="10em" height="10em" viewBox="0 0 120 120">
  <desc>A_n Quiver</desc>
  <g fill="none" stroke="black" stroke-width="1">
   <path d="M 60 25 l 25 20 l 0 30 l -25 20 l -25 -20 l 0 -30 z" />
   <g stroke-dasharray="2">
     <path d="M 60 0 l 0 25" />
     <path d="M 85 45 l 25 -20" />
     <path d="M 85 75 l 25 20" />
     <path d="M 60 95 l 0 25" />
     <path d="M 35 75 l -25 20" />
     <path d="M 35 45 l -25 -20" />
   </g> 
  </g>
  <g fill="red" stroke="none">
   <circle cx="60" cy="25" r="4" />
   <circle cx="85" cy="45" r="4" />
   <circle cx="85" cy="75" r="4" />
   <circle cx="60" cy="95" r="4" />
   <circle cx="35" cy="75" r="4" />
   <circle cx="35" cy="45" r="4" />
  </g>
  <foreignObject x="45" y="0" width="16" height="20"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><msub><mi>v</mi><mn>1</mn></msub></math></foreignObject>
  <foreignObject x="83" y="15" width="16" height="20"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><msub><mi>v</mi><mn>2</mn></msub></math></foreignObject>
  <foreignObject x="5" y="25" width="20" height="25"><math xmlns="http://www.w3.org/1998/Math/MathML" display="inline"><msub><mi>v</mi><mrow><msub><mi>n</mi><mn>1</mn></msub></mrow></msub></math></foreignObject>
</svg>
\end{svg}& \equiv \left({U(k)}^{n_1},\{v_i\}\right)}$$


| Function name | Description                    |http://ncatlab.org/nlab/cancel_edit/Sandbox
| ------------- | ------------------------------ |
| `help()`      | Display the help window.       |
| `destroy()`   | **Destroy your computer!**     |  

Apple
:   Pomaceous fruit of plants of the genus Malus in 
the family Rosaceae.

Orange
:   The fruit of an evergreen tree of the genus Citrus.

Term 1

:   This is a definition with two paragraphs. Lorem ipsum 
    dolor sit amet, consectetuer adipiscing elit. Aliquam 
    hendrerit mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus.

:   Second definition for term 1, also wrapped in a paragraph
    because of the blank line preceding it.

Term 2

:   This definition has a code block, a blockquote and a list.

        code block.

    > block quote
    > on two lines.

    1.  first list item
    2.  second list item

You can make abbreviations. Here I'm going to make an abbreviation for the n-category cafe: 

*[nCat]: n-category cafe
Is this a new line?

Now apparently I just type nCat and it should output "n-category cafe". Did it work?  No!

Trying theorem numbering:

+-- {: .num_theorem #Lagrange}
###### Theorem
**(Lagrange's Theorem)**. Let $G$ be a finite group, and let $H$
be a subgroup of $G$. Then the order of $H$ divides the order of
$G$.
=--

By Theorem \ref{Lagrange}, we know that the order of $H$ divides the order of $G$.


+-- {: .un_defn}
###### Definition
**(Definitive definition)**
By definition, this definition is a definition. Definitely.
=--

[[John Baez]]: Here's how include a link to a picture:

![A pic](http://math.ucr.edu/home/baez//cassini_over_enceladus.jpg)


Here goes the neighborhood( [[Eric Forgy]] )

~~~~
This is a code block, fenced-style
~~~~

Huh? That is [PHP Markdown extra code](http://michelf.com/projects/php-markdown/extra/#fenced-code-blocks). That should work here, right...? [[Bruce Bartlett]]

Uploading little pdf icon for linking to pdf's: [[pdficon_small.gif:file]]

Uploading little n-category cafe icon: [[n-cafe_5.gif:file]]

Attempting to link to an n-category cafe post: [My link](http://golem.ph.utexas.edu/category/2008/11/nlab.html#c020636)

Attempting to link to a pdf file: [My link](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf)

Attempting to link to a _page_ inside a pdf file: [My link](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf#page=12)

Attempting to link to an arXiv file: [Higher dimensional algebra and topological quantum field theory](http://arxiv.org/abs/q-alg/9503002)

+-- {: .my_gismo}
Hi is this a gismo?
=--

[[n-cafe_5.gif:pic]]

Am I going to get an undefined term in gray at the end of this [[question]]

 * Trying to make
   * Nested lists
   * lalala

Here's a Unicode WikiLink: [[??? ????]]. The only funky bit is mixing LTR and RTL scripts.

[[Contributors]]

lalala

<table><tr><td>Can I put $x^2$ math in a table?</td></tr></table>

Nor can you put it inside links: [[$\infty$-category]].
But you can put it inside *some* markup, such as boldface: **I love $\infty$-categories!!!**
I don\'t know what makes the difference.

$\leftrightarrow$

+-- {.query}
The example of query blocks on the HOWTO page is this syntax
=--

+-- {: .query}
But the maruku page says that this is right.  Do both work?
=--

[[3?2-colimit]]s have not yet been defined.  When they are, our [[HowTo|naming conventions]] would name the page [[3/2-colimit]].

Ta. 

We can put in a table, which is a block-level HTML construct, like this, remembering to separate it by blank lines top and bottom:

<table>
<tr><td>Foo</td></tr>
</table>

But we can't put in an iframe like this:

<iframe src="http://www.j-paine.org/cgi-bin/webcats/product.php" width="100%" height="300px">
Your browser does not support iframes.
</iframe>

Many spaces that occur in mathematics aren't manifolds but one would like to be able to treat them as if they were manifolds; in particular, they should have some *smooth* structure that goes beyond mere topology.  By considering examples of these spaces and by considering what specifically one would like to do with or to them, it is possible to generalise the idea of a smooth manifold to encompass the new examples whilst preserving enough structure to retain the old tools.  There have been several such generalisations in recent mathematical history.  A (partial) list is below.

Many spaces that occur in mathematics aren't manifolds but one would like to be able to treat them as if they were manifolds; in particular, they should have some *smooth* structure that goes beyond mere topology.
By considering examples of these spaces and by considering what specifically one would like to do with or to them, it is possible to generalise the idea of a smooth manifold to encompass the new examples whilst preserving enough structure to retain the old tools.
There have been several such generalisations in recent mathematical history.
A (partial) list is below.

Testing lists:

1. Hello World
1. This should be number 2

Ok, trying out a query box: 

+-- {: .query}
Am I mad?
=--

This is the original Markdown list:


1.  Bird
1.  McHale
1.  Parish

<table markdown="1"><tr><td>I can put $x^2$ math in a table!</td></tr></table>

| Another  | Way  |
| -------  | ---- |
| to $x^2$ | make |
| a table  |      |

[A pic](http://www.bangor.ac.uk/r.brown/fig6_10c2.jpg)

$$\begin{aligned}
  K(1,\mathbf{DFib(X)}(A,B)) \cong& K(1, Ran_X B^A)\\
  \cong& DFib(X)(1_X, B^A)
\end{aligned}$$

{:test: style="background:#ffccaa"}

{:testproof: .test .proof}

{:test1: style="background:#f6fff3"}

{:test2: style="border:\"solid #ce9\""}

+-- {: .query style="background:#888888"}
Basic query box
=--

+-- {: test .query}
Basic query box again
=--

+--
Testing modifying styles: test
=--
{:test}

+-- {: style="background:#f6fff3" .proof}
Testing modifying styles: testproof
=--

+--
Testing modifying styles: test1
=--
{:test1}

+--
Testing modifying styles: test2
=--
{:test2}

{:response: style="color:#930; font-size:0.9em;margin-left:2em;"}

+--
**Not a chance**. That would be a *completely unacceptable* security risk.
=--
{:response}

\* $*$ $\star$ $\ast$ $*f*$ *hi* *

Testing punctuation: $x^2 + y^2$.

Testing punctuation: $x^2 + y^2.$

`&amp;&rarr;`
<code>&amp;&rarr;</code>

Testing &lt;pre> tags for embedding program code:
<pre>
Code, code, code.
More code, code, code.
</pre>
After the pre tag.

Markdown method:

    Code, code, code.
    More code, code, code.

Testing in-line code. With markdown: `this is code`. With HTML: <code>this is code</code>.

Testing HTML comments:
<!-- this is a comment --> this is after the comment.

****

category: meta