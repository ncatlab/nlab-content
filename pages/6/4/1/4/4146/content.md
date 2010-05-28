# Exact squares
* automatic table of contents goes here
{: toc}

## Definition

Let $A$, $B$, $C$, and $D$ be (usually small) [[categories]], and consider a square of [[functors]]
$$\array{A & \overset{f}{\to} & B\\
  ^u\downarrow & \Downarrow & \downarrow^v\\
  C& \underset{g}{\to} & D}$$
which is inhabited by a [[natural transformation]] (which might be an [[identity]]).  This is said to be an **exact square** if the canonical [[Beck-Chevalley transformation]]
$$ u_! f^* \to g^* v_!, $$
relating functors with values in some other category $M$, is always an isomorphism.  Here $f^*\colon M^B\to B^A$ and $g^*\colon M^D\to M^C$ denote precomposition with $f$ and $g$ respectively, and $u_!\colon M^A\to M^C$ and $v_!\colon M^B\to M^D$ denote pointwise left [[Kan extensions]] along $u$ and $v$.  The Beck-Chevalley transformation is defined to be the composite
$$ u_! f^* \to u_! f^* v^* v_! \to u_! u^* g^* v_! \to g^* v_!. $$
By the general calculus of [[mates]], this definition is equivalent to requiring that the dual transformation
$$ v^* g_* \to f_* u^* $$
is an isomorphism, where $f_*$ and $g_*$ denote pointwise *right* Kan extensions.

This definition refers to Kan extensions of diagrams with values in any category $M$ (whenever such Kan extensions exist).  If a square is exact only relative to diagrams defined in a *particular* category $M$, we may call it **$M$-exact**.

This is a "functional" definition, which generalizes correctly to other contexts (see below).  However, in the case of ordinary categories and Kan extensions, there is a precise combinatorial characterization of which squares are exact.  Analogous, but different, combinatorial characterizations exist in other contexts.  Thus, when using exactness to compute with Kan extensions in practice, we can use the combinatorial characterization to verify that a square is exact, then apply the definition above to compute one Kan extension in terms of another.  

## Examples

### Comma squares

In ordinary category theory, any [[comma square]] is always exact.  In other words, if $A$ is the [[comma category]] $(v/g)$, with $f$ and $u$ the canonical projections, then the square is exact.  If additionally $C=*$ is the [[terminal category]], then $g$ simply picks out an object $d\in D$, and $A=v/d$ is the comma category of $v$ over $d$.  Exactness of this square then says that the value of $v_! F$ at $d\in D$ is the colimit of $F$ pulled back to $v/d$, i.e.
$$ (Lan_v F)(d) = colim_{v(b) \to d} F(b) $$
which is (for ordinary categories) one of the equivalent definitions of when a Kan extension is pointwise.

This example also makes clear why we define exactness only relative to pointwise Kan extensions.  If we allowed non-pointwise ones, then we would have hardly any exact squares.  Exactness is essentially a generalized version of pointwiseness, telling us how Kan extensions along one functor can be computed by transferring them to another functor, but for non-pointwise Kan extensions (which "exist by accident") we have basically no hope of doing this.

### Fully faithful functors

If $u\colon A\to B$ is a [[fully faithful functor]], then the square
$$\array{A & \overset{id}{\to} & A\\
  ^{id}\downarrow && \downarrow^u\\
  A & \underset{u}{\to} & B}$$
is exact.  This just says that the unit $Id_A \to u^* u_!$ is an isomorphism, i.e. that left (and equivalently right) Kan extensions along $u$ are "honest" extensions.

### Final functors

A functor $u\colon A\to B$ is a [[final functor]] if and only if the square
$$\array{A & \overset{u}{\to} & B\\
  \downarrow && \downarrow\\
  *& \underset{}{\to} & *}$$
is exact.  Exactness of this square says that for $F\colon B\to M$, the canonical map $colim_A u^*F \to colim_B F$ is an isomorphism, which is one equivalent definition of when $u$ is final.


## Characterization

...

## Generalizations

The notion of exact square makes sense for squares inhabited by 2-cells in any [[2-category]], and for any suitable notion of "(pointwise) Kan extension."  This includes:

* Internal [[pointwise Kan extension]]s in any [[2-category]] with finite [[2-limits]].
* Enriched pointwise Kan extensions in a 2-category $V Cat$ of [[enriched categories]].  Note that this notion of "pointwiseness" is not the "internal" one in $V Cat$.
* Pointwise Kan extensions can also be defined in any [[Yoneda structure]], and more or less equivalently in any [[2-category equipped with proarrows]].  This specializes both to the classical case, to internal pointwise extensions in a 2-category, and to the enriched case.
* Exact squares play an especially important role in the theory of [[derivators]]; see [[homotopy exact square]].

[[!redirects exact squares]]
