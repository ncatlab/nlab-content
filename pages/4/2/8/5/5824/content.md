
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[category theory]], the *pasting law* or *pullback lemma* is a statement about (de-)composition of [[pullback]]/[[pushout]] [[diagrams]]. 

## Statement

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a [[category]] or more generally an [[(∞,1)-category]]. Consider a [[commuting diagram]] in $\mathcal{C}$ of the following shape:


\begin{tikzcd}
  {}
  \ar[r]
  \ar[d]
  &
  {}
  \ar[r]
  \ar[d]
  &
  {}
  \ar[d]
  \\
  {}
  \ar[r,]
  &
  {}
  \ar[r]
  &
  {}  
\end{tikzcd}

Then:

1. if the right square is a pullback, then the total rectangle is a pullback precisely if the left square is a pullback.

1. if the left square is a [[pushout]], then the total rectangle is a pushout precisely if the right square is a pushout.

=--

For **proof** see

* for [[category theory]]: at _[pullback -- pasting law](pullback#Pasting)_

* for [[(∞,1)-category theory]]: at _[(∞,1)-limit -- pushout pasting law](limit+in+a+quasi-category#PushoutPasting)_



## Related statements

In general, the implications in the above result do require the hypothesis (e.g. in the pullback case that the right square is a pullback).  However, in some cases this can be omitted.

+-- {: .num_prop}
###### Proposition
Suppose we have a diagram of the above shape

$$
  \array{
    x & \longrightarrow & y & \longrightarrow & z
    \\
    \downarrow && \downarrow && \downarrow
    \\
    u & \longrightarrow & v & \longrightarrow & w
  }
$$

in which the total rectangle (consisting of $x,z,u,w$) is a pullback, and moreover the induced map $y\to v\times z$ is a [[monomorphism]].  Then the left-hand square (consisting of $x,y,u,v$) is also a pullback.
=--

In a [[regular category]] this also works in the other direction, if the bottom left morphisms is a [[regular epimorphism]]:
\begin{proposition}
\label{WrongWayPastingLawInRegularCategory}
  In a [[regular category]], consider a [[commuting diagram]] of the form
\begin{tikzcd}
  {}
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny(pb)}"]
  &
  {}
  \ar[r]
  \ar[d]
  &
  {}
  \ar[d]
  \\
  {}
  \ar[r, ->>]
  &
  {}
  \ar[r]
  &
  {}  
\end{tikzcd}
where 

1. the left square is a [[pullback]];

1. the bottom left morphism is an [[regular epimorphism]].

Then right right square is a pullback iff the total rectangle is.
\end{proposition}
(e.g. [Gran 2020, Lem. 1.15](regular+category#Gran20))


Another related statement involves a pair of rectangles and equalizers.

+-- {: .num_prop}
###### Proposition
Suppose $\mathcal{C}$ is any [[category]] with [[equalizers]] and that we have a diagram of the following shape:

$$
  \array{
    x & \longrightarrow & y & \rightrightarrows & z
    \\
    \downarrow && \downarrow && \downarrow
    \\
    u & \longrightarrow & v & \rightrightarrows & w
  }
$$

such that the vertical arrows are all [[monomorphisms]], the squares on the right are serially [[commutative diagram|commutative]], and the lower row is an [[equalizer]].  Then the upper row is an equalizer if and only if the left square is a [[pullback]].
=--

## References
 {#References}

### In 1-category theory

Discussion in [[1-category|1-]][[category theory]]:

Statements of the pasting law in textbooks, typically leaving the proof to the reader:

* [[Saunders MacLane]], Ex. 8 on p. 72 in: *[[Categories for the Working Mathematician]]*, Graduate texts in mathematics, Springer 1971 ([doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8))

* [[Jiri Adamek]], [[Horst Herrlich]], [[George Strecker]], Prop. 11.10 in: *[[Abstract and Concrete Categories]]*, John Wiley and Sons, New York (1990) reprinted as: Reprints in Theory and Applications of Categories **17** (2006) 1-507 ([tac:tr17](http://www.tac.mta.ca/tac/reprints/articles/17/tr17abs.html), [book webpage](http://katmat.math.uni-bremen.de/acc/), [pdf](http://katmat.math.uni-bremen.de/acc/acc.pdf))

The proof is spelled out in:

* [[Andrej Bauer]], *The pullback lemma in gory detail*, 2012 ([pdf](http://math.andrej.com/wp-content/uploads/2012/05/pullback.pdf), [[Bauer_PullbackLemma.pdf:file]])

### In model category theory

Discussion in [[model category]]-theory

for [[right proper model categories]]:

* {#Hirschhorn02} [[Philip Hirschhorn]], Prop. 13.3.15 of: _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

### In $(\infty,1)$-category theory

Discussion in [[(infinity,1)-category theory|$(\infty,1)$-category theory]]

* [[Jacob Lurie]], Lemma 4.4.2.1 in *[[Higher Topos Theory]]*

[[!redirects pasting law for pullbacks]]
[[!redirects pasting law for pushouts]]
[[!redirects pasting law]]
[[!redirects pullback lemma]]