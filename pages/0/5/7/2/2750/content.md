# Ordered pairs

* tic
{: toc}


## Idea

Given any things $a$ and $b$, the __ordered pair__ of $a$ and $b$ is a thing, usually written $(a,b)$, sometimes $[a,b]$ or $\langle{a,b}\rangle$.  The important property is
\[ \label{basic} (a,b) = (c,d) \;\Leftrightarrow\; a = c,\; b = d .\]
The things $a$ and $b$ are called the __components__ of the ordered pair $(a,b)$.  Given any two sets $X$ and $Y$, their [[Cartesian product]] is a set $X \times Y$ whose [[elements]] are precisely the ordered pairs whose components are respectively elements of $X$ and elements of $Y$.


## Formalisations

One may wish to declare ordered pairs to exist by fiat, which was done, for example, by both [[Bourbaki]] and [[Bill Lawvere]].  In Bourbaki\'s foundational [[set theory]], $\langle{-,-}\rangle$ is a fundamental binary operation on mathematical objects satisfying two axioms: \eqref{basic} and the existence (as a set) of the Cartesian product of any two sets.  In Lawvere\'s foundational set theory, [[ETCS]], one axiom is the existence of [[products]] in the category of sets; when applied to [[global elements]], this gives their ordered pair (with the product itself being the Cartesian product), and \eqref{basic} can be proved.  Other [[structural set theories]] should contain an axiom similar to Lawvere\'s axiom of products.

+-- {: .query}
I need to check that I remembered Bourbaki correctly.  ---Toby
=--

Instead, one may construct ordered pairs out of some more basic operation.  In a [[material set theory]], one may use Kuratowski\'s definition
$$ (a,b) \coloneqq \big\{\,\{a\},\{a,b\}\,\big\} ;$$
it is straightforward (using the [[axiom of extensionality]]) to prove that \eqref{basic} holds.  Sometimes one sees the alternative
$$ (a,b) \coloneqq \big\{a, \{a,b\}\,\big\} ;$$
but now the [[axiom of foundation]] is also needed to prove \eqref{basic}, so the first form is usually preferred.  To prove that the cartesian product of two sets is a set, one may use the [[axiom of separation]] to construct $X \times Y$ as a [[subset]] of the [[power set]] of the power set of the [[union]] of $X$ and $Y$, or else use the [[axiom of replacement]] (Weak Replacement is enough) to construct it directly, since its elements are indexed by the sets $X$ and $Y$.

In a foundational [[type theory]], ordered pairs are usually also given by fiat, but \eqref{basic} may not hold, depending on the type theory used.  Now Bourbaki\'s binary operation of pairing becomes a typed operation; given $a$ of type $X$ and $b$ of type $Y$, the ordered pair $(x,y)$ has type $A \times B$.  There are also two typed operations (either  basic or definable, depending on the style of type theory used) $\pi\colon X \times Y \to X$ and $\rho\colon X \times Y \to Y$, satisfying the [[beta-rule]]s $\pi(x,y) = x$ and $\rho(x,y) = y$.  Then we can either add the [[eta-rule]] $z = (\pi z,\rho z)$, which will allow \eqref{basic} to be proved, or else take \eqref{basic} as the *definition* of equality on the product type $X \times Y$ (which will then allow the eta-rule to be proved).


## Generalisations

... tuples ...

... pairings ...

... dependent sums ...


[[!redirects ordered pairs]]