# Idea #

An **$n$-fibration** is the version of a [[Grothendieck fibration]] appropriate for $n$-[[n-category|categories]].

The idea is that a functor $p:E\to B$ between $n$-categories is an $n$-fibration if the assignation $x\mapsto E_x = p^{-1}(x)$ of an object $x\in B$ to its fiber can be made into a (contravariant) functor from $B$ to the $(n+1)$-category $n Cat$.


# Definition #

(This definition is schematic, and needs to be adapted to be made precise for any particular definition of $n$-category.)

Let $p:E\to B$ be a functor between $n$-categories.

+--{: .num_defn}
###### Definition
A morphism $\phi:b\to a$ in $E$ is **cartesian** (relative to $p$) if for any $c\in E$, the following square:
$$\array{E(c,b) & \overset{\phi\circ -}{\to} & E(c,a)\\
  ^p \downarrow && \downarrow ^p\\
  B(p c, p b) & \underset{p\phi\circ -}{\to} & B(p c, p a)}$$
(which commutes by functoriality of $p$) is a [[pullback]] of $(n-1)$-categories.
=--

+--{: .num_defn}
###### Definition
We say that $p:E\to B$ is an **$n$-fibration** (or just a **fibration**) if
1. For any object $a\in E$ and morphism $f:x\to p a$ in $B$, there exists a cartesian $\phi:b\to a$ and an [[equivalence]] $p\phi \simeq f$ in the [[over category|slice]] $n$-category $B/p a$.
1. For any objects $a,b\in E$, the functor $p:E(b,a) \to B(p b, p a)$ is an $(n-1)$-fibration.
1. For any $a,b,c\in E$ and $\psi:c\to b$, the square
$$\array{E(b,a) &\overset{-\circ \psi}{\to} & E(c,a)\\
  ^p\downarrow && \downarrow^p\\
  B(p b, p a) & \underset{-\circ p\psi}{\to} & B(p c, p a)}$$
is a morphism of $(n-1)$-fibrations.
=--

+--{: .num_defn}
###### Definition
If $p_1:E_1\to B_1$ and $p_2:E_2\to B_2$ are $n$-fibrations, a commutative square
$$\array{E_1 & \overset{h}{\to} & E_2\\
  p_1 \downarrow && \downarrow p_2\\
  B_1 & \underset{g}{\to} & B_2}$$
is a **morphism of $n$-fibrations** if
1. Whenever $\phi$ is cartesian for $p_1$, $h(\phi)$ is cartesian for $p_2$, and
1. For any $a,b\in E_1$, the square
$$\array{E_1(b,a) & \overset{h}{\to} & E_2(h b, h a)\\
  p_1 \downarrow && \downarrow p_2\\
  B_1(p_1 b, p_1 a)& \underset{g}{\to} & B_2(g p_1 b, g p_1 a)}$$
is a morphism of $(n-1)$-fibrations.
=--


# Remarks

* The definition is recursive in $n$, but if we unravel it, it makes perfect sense for $n=\omega$.

* When $n=1$, this reduces to Street's weakened version of a [[Grothendieck fibration]].  We recover Grothendieck's original notion by requiring that for any $a\in E$ and $f:x\to p a$ in $B$, there exists a cartesian $\phi:b\to a$ such that $p\phi$ and $f$ are _equal_ (an [[evil]] condition).

* Likewise, when $n=2$ this is a weakened version of Hermida's definition of 2-fibration.


# From fibrations to functors

If $p:E\to B$ is an $n$-fibration, we define a functor (or '$n$-pseudofunctor') from $B$ to $n Cat$ as follows.  (Like the above definition, this is only a schematic sketch.)

* Send $x\in B$ to the [[essential fiber]] $E_x$, whose objects are objects $a\in E$ equipped with a equivalence $p a \simeq x$.

* For a morphism $f:y\to x$ in $B$, define $f^*:E_x\to E_y$ by choosing, for each $a\in E_x$, a cartesian $\phi:b\to a$ over $f$ and defining $f^*(a)=b$.  The universal property of cartesian arrows makes $f^*$ a functor.

* For a 2-cell $\alpha:f\to g:y\to x$ in $B$, define a transformation $\alpha^*:g^*\to f^*$ as follows.  Given $a\in E_x$, we have a cartesian arrow $\phi:g^*a\to a$ over $f$.  Now choose a cartesian 2-cell $\mu:\psi\to \phi$ over $\alpha$ in $E(g^*a,a)$.  Since $p \psi = f$, $\psi$ factors essentially uniquely through the cartesian arrow $\chi:f^*a\to a$, giving a morphism $g^*a \to f^*a$; we define this to be the component of the transformation $\alpha^*$ at $a$.

* and so on...

Note that the functor we obtain is "totally contravariant:" it is contravariant on $k$-cells for all $1\le k\le n$.

One expects that in this way, the $(n+1)$-category of fibered $n$-categories over $B$ is equivalent to the $(n+1)$-category of functors $B\to n Cat$.  The inverse should be a generalization of the [[Grothendieck construction]], which is known only for $n=2$.


# References #

[Claudio Hermida](http://maggie.cs.queensu.ca/chermida) introduced 2-fibrations in:

* Claudio Hermida, "Some properties of Fib as a fibred 2-category," J. Pure Appl. Algebra 134 (1), 83--109, 1999; [preprint version ps.gz](http://maggie.cs.queensu.ca/chermida/papers/jpaa.ps.gz)

In fact they also appeared earlier, in some form, in [[Gray-adjointness-for-2-categories|Gray's book]]. 

A definition for strict $n$-categories due to Hermida is unpublished, but it is used and presented in another joint work with [Marta Bunge](http://www.math.mcgill.ca/bunge), presented at CATS07 at Calais:

* Marta Bunge, "Intrinsic $n$-stack completions over a topos," slides [here](http://saxo.univ-littoral.fr/CT08/slides/Bunge.pdf)

 $n$-pseudofunctors may be viewed (and defined) as [[anafunctor]]s.  For $n$-groupoids such an approach to $n$-pseudofunctors has been studied in

* [D. Bourn](http://www-lmpa.univ-littoral.fr/~bourn), 
Pseudo functors and non abelian weak equivalences, in "Categorical algebra and its applications", Springer LNM 1348 (1988), 55--70.
