## Definition ##

__Composition__ is the operation that takes [[morphism|morphisms]] $f\colon  x \to y$ and $g\colon  y \to z$ in a [[category]] and produces a morphism $g \circ f\colon  x \to z$, called the __composite__ of $f$ and $g$.


## Higher arity

Strictly speaking, composition as defined above is *binary* composition.  One can also define $n$-ary composites for any [[natural number]] $n \geq 0$: given $n + 1$ objects $x_0, \ldots, x_n$ and $n$ morphisms $f_i\colon x_{i-1} \to x_i$, we get the composite $f_n \circ \dots \circ f_1\colon x_0 \to x_n$.  Since composition in a category is associative, a definition of $n$-ary composition from binary composition via any choice of bracketing will be equal to that resulting from any other choice of bracketing.  The unary composite of $f_1\colon x_0\to x_1$ is simply $f$ itself, and the nullary composite of $x_0$ is its [[identity morphism]].

Conversely, a category can equivalently be defined as a [[directed graph]] equipped with an $n$-ary composition operation for every [[natural number]] $n\ge 0$, satisfying suitable associativity axioms.  This definition may be called *unbiased*, as opposed to the usual definition which is "biased" towards $0$ and $2$.


## Notation ##

Traditionally, the composite of $f$ and $g$ as above is written $g \circ f$, following the notation introduced by the followers of Leibniz for composition of [[function]]s.  This is often abbreviated as simply $g f$.  Of course, this notation preserves the order of symbols in the elementwise definition of function composition: $(g\circ f)(x) = g(f(x))$.

On the other hand, reading a diagram
$$ x \stackrel{f}\to y \stackrel{g}\to z $$
the notation $f g$ reads better.  One way to make this anti-Leibniz convention clearer is to write $f ; g$ (which is based on the interpretation of programming commands as morphisms in theoretical computer science).  Since this convention is motivated by the drawing of diagrams, it is also sometimes called **diagrammatic order**.

Therefore, the notations $g f$ and $f g$ are ambiguous, while $g \circ f$ and $f ; g$ are less so.  It seems that the notation $g f$ for $g\circ f$ is more common than $f g$ for $f ; g$, although the $f g$ notation occurs in some important older papers.

+-- {: .query}
Is $f; g$ really more common than $f g$, as Charles Wells wrote here a moment ago?  I\'ve seen $f g$ more often (even for this order) and $f; g$ mostly in CS-oriented literature, but my experience is probably not as broad.  ---Toby

The change you made is probably good.  Much of my work in category theory was done in connection with computer science, so my perception may be skewed.  --Charles

OK, thanks!  ---Toby

[[Mike Shulman]]: I hope I didn't mess up these statements when I merged the two pages.
=--

Although diagrammatic order has advantages and partisans, especially among category theorists and computer scientists, the "classical" order of composition is firmly entrenched in much of mathematics.  Many people who agree that diagrammatic order is "better" on its own merits nevertheless believe that trying to change the established "classical" order of composition creates more confusion than it removes.

In some older category theory papers, arrows were written pointing from right to left, so that the composition of arrows could be written in the "classical" style, while still preserving the diagrammatic intuition. Hom-sets were accordingly written $C(b,a)$, where $a$ is the [[source]], and $b$ is the [[target]].


[[!redirects composite]]
[[!redirects composites]]
[[!redirects diagrammatic order]]
