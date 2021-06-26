
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Exact squares
* automatic table of contents goes here
{: toc}

## Definition

Let $A$, $B$, $C$, and $D$ be (usually small) [[categories]], and consider a square of [[functors]]
$$\array{A & \overset{f}{\to} & B\\
  ^u\downarrow & \swArrow & \downarrow^v\\
  C& \underset{g}{\to} & D}$$
which is inhabited by a [[natural transformation]] (which might be an [[identity]]).  This is said to be an **exact square** if the canonical [[Beck-Chevalley transformation]]
$$ u_! f^* \to g^* v_!, $$
relating functors with values in some other category $M$, is always an isomorphism.  Here $f^*\colon M^B\to M^A$ and $g^*\colon M^D\to M^C$ denote precomposition with $f$ and $g$ respectively, and $u_!\colon M^A\to M^C$ and $v_!\colon M^B\to M^D$ denote pointwise left [[Kan extensions]] along $u$ and $v$.  The Beck-Chevalley transformation is defined to be the composite
$$ u_! f^* \to u_! f^* v^* v_! \to u_! u^* g^* v_! \to g^* v_!. $$
By the general calculus of [[mates]], this definition is equivalent to requiring that the dual transformation
$$ v^* g_* \to f_* u^* $$
is an isomorphism, where $f_*$ and $g_*$ denote pointwise *right* Kan extensions.

This definition refers to Kan extensions of diagrams with values in any category $M$ (whenever such Kan extensions exist).  If a square is exact only relative to diagrams defined in a *particular* category $M$, we may call it **$M$-exact**.

This is a "functional" definition, which generalizes correctly to other contexts (see below).  However, in the case of ordinary categories and Kan extensions, there is a precise combinatorial characterization of which squares are exact.  Thus, when using exactness to compute with Kan extensions in practice, we can use the combinatorial characterization to verify that a square is exact, then apply the definition above to compute one Kan extension in terms of another.  

## Generalizations

The definition given above generalizes directly to squares inhabited by a 2-cell in any [[2-category]], and any suitable notion of "(pointwise) Kan extension" which may exist along morphisms in that 2-category.  This includes:

* Internal [[pointwise Kan extension]]s in any [[2-category]] with finite [[2-limits]].
* Enriched pointwise Kan extensions in a 2-category $V Cat$ of [[enriched categories]].  Note that this notion of "pointwiseness" is not the "internal" one in $V Cat$; see [here](Kan+extension#In2cat) for a counterexample.
* Pointwise Kan extensions can also be defined in any [[Yoneda structure]], and more or less equivalently in any [[2-category equipped with proarrows]].  This specializes both to the classical case, to internal pointwise extensions in a 2-category, and to the enriched case.
* In the world of [[(infinity,1)-categories]] we have a notion of [[homotopy exact square]], which can also be defined and characterized in the easier context of [[derivators]].  In fact, one can argue that derivators are basically designed as a context for the study of homotopy exact squares.

The combinatorial characterization of exact squares has a corresponding version for any of these generalizations, although in different cases it will be more or less explicit.


## Examples

### Comma squares

In ordinary category theory, any [[comma square]] is always exact.  In other words, if $A$ is the [[comma category]] $(v/g)$, with $f$ and $u$ the canonical projections, then the square is exact.  If additionally $C=*$ is the [[terminal category]], then $g$ simply picks out an object $d\in D$, and $A=v/d$ is the comma category of $v$ over $d$.  Exactness of this square then says that the value of $v_! F$ at $d\in D$ is the colimit of $F$ pulled back to $v/d$, i.e.
$$ (Lan_v F)(d) = colim_{v(b) \to d} F(b) $$
which is (for ordinary categories) one of the equivalent definitions of when a Kan extension is pointwise.

This example also makes clear why we define exactness only relative to pointwise Kan extensions.  If we allowed non-pointwise ones, then we would have hardly any exact squares.  Exactness is essentially a generalized version of pointwiseness, telling us how Kan extensions along one functor can be computed by transferring them to another functor, but for non-pointwise Kan extensions (which "exist by accident") we have basically no hope of doing this.

### Fully faithful functors

A functor $u\colon A\to B$ is a [[fully faithful functor]] if and only if the square
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

### Adjunctions

A functor $f: A \to B$ is left adjoint to $u: B \to A$ with unit $\eta: 1_A \implies uf$ if and only if the square
$$\array{A & \overset{id}{\to} & A \\
  ^f\downarrow & ^\eta\swArrow & \downarrow^{id}\\
  B& \underset{u}{\to} & D}$$
is exact. Dually, $f \dashv u$ with counit $\varepsilon: fu \implies 1_B$ if and only if the square
$$\array{B & \overset{u}{\to} & A\\
  ^{id}\downarrow & ^\varepsilon \swArrow & \downarrow^f\\
  B& \underset{id}{\to} & B}$$
is exact.

## Characterization

Exact squares can be characterized in several ways, which generalize in different directions.

### Using profunctors

Recall that for any functor $u\colon A\to C$, the left Kan extension $u_!$ can be computed as the colimit weighted by the corepresentable profunctor $C(u,1)$, while restriction $u^*$ along $u$ is the colimit weighted by the representable profunctor $C(1,u)$.  Moreover, given composable profunctors $H$ and $K$, an $H K$-weighted colimit is the same as a $K$-weighted colimit of an $H$-weighted colimit.  Therefore, $u_! f^*$ can be computed as a $C(u,1) \circ B(1,f)$-weighted colimit, while $g^* v_!$ can be computed as a $D(1,g) \circ D(v,1)$-weighted colimit.  Note that $D(1,g) \circ D(v,1) \cong D(v,g)$ by [[Yoneda reduction]].  Thus sufficient condition for a square as above to be exact is that the canonical induced transformation of profunctors
$$ C(u,1) \circ B(1,f) \to D(v,g) $$
is an isomorphism.  Moreover, by considering colimits of the Yoneda embedding $B\to [B^{op},Set]$ it is easy to see that this condition is necessary as well.  Unraveling it, we see that it says that for all objects $b\in B$ and $c\in C$, the function
$$ \int^{a\in A} C(u(a),c) \times B(b,f(a)) \to D(v(b), g(c)) $$
is an isomorphism.

So far, this argument works to describe the exact squares in arbitrary [[enriched categories]], or more generally in any [[2-category equipped with proarrows]] where we have a sensible notion of profunctor that describes to the notion of pointwise Kan extension under consideration.  However, in the Set-based case, we can go further.  Given the construction of coequalizers in [[Set]], the above condition means that, calling $\psi \colon g u \to v f$ the given 2-cell, we have

1. For any morphism $\varphi\colon v(b) \to g(c)$ in $D$, there exists an $a\in A$ and morphisms $\alpha\colon u(a) \to c$ and $\beta\colon b\to f(a)$ such that $g(\alpha) \circ \psi_a \circ v(\beta) = \varphi$, and

2. For any $(a,\alpha,\beta)$ and $(a',\alpha',\beta')$ as above with $g(\alpha) \circ \psi_a \circ v(\beta) = g(\alpha') \circ \psi_{a'} \circ v(\beta')$, there is a [[zigzag]] of arrows connecting $a$ to $a'$ and rendering the evident induced diagram commutative.


We can state this equivalently as follows.  Given $b\in B$ and $c\in C$, define $(b/A/c)$ to be the category whose objects are triples $(a,\alpha,\beta)$ with $\alpha\colon u(a) \to c$ and $\beta\colon b\to f(a)$, and whose morphisms are morphisms $a\to a'$ making two triangles commute.  There is a functor
$$(b/A/c) \to D(v(b),g(c))$$
(considering the latter [[homset]] as a [[discrete category]]) which sends $(a,\alpha,\beta)$ to the composite $g(\alpha) \circ \psi_a \circ v(\beta)$, and the square is exact just when this functor is a bijection on [[connected component]]s.

#### Examples

+--{: .un_example}
###### Example
Note that in the case of a square
$$\array{A & \overset{u}{\to} & B\\
  \downarrow && \downarrow\\
  *& \underset{}{\to} & *}$$
this characterization reduces to saying that for any $b\in B$, the category $b/u$ is connected.  This is the standard combinatorial characterization of a [[final functor]].
=--

+--{: .un_example}
###### Example
This characterization implies directly that any [[cocomma square]] is exact, since the cocomma object of a cospan $C \overset{u}{\leftarrow} A \overset{f}{\to} B$ is precisely the [[cograph of a profunctor|cograph]] of the profunctor $C(u,1) \circ B(1,f)$.  This generalizes to any proarrow equipment (but unlike the case of comma squares, it does not generalize to [[homotopy exact squares]] unless we take a "homotopy cocomma object").
=--

### Using comma objects {#CommaObj}

Another approach is to argue as follows.  First note that any comma square of the form
$$\array{v/d & \overset{}{\to} & C\\
  \downarrow &\swArrow& \downarrow^v\\
  * & \underset{d}{\to} & D}$$
must be exact.  As observed above, this is one of the equivalent definitions of what it means to be a pointwise left Kan extension.  (Note that this ejects us from the world of enriched categories already.)  Dually,
$$\array{d/g & \overset{}{\to} & *\\
  \downarrow &\swArrow & \downarrow^d\\
  B & \underset{g}{\to} & D}$$
must also be exact, by definition of pointwise right Kan extensions.  Now suppose that a square
$$\array{A & \overset{f}{\to} & B\\
  ^u\downarrow & \swArrow & \downarrow^v\\
  C& \underset{g}{\to} & D}$$
is given.  The Beck-Chevalley transformation $u_! f^* \to g^* v_!$ between functors $C\to M$ will be an isomorphism as soon as it is an isomorphism componentwise, i.e. when evaluated at every object of $c$.  In other words, we want the transformation $c^* u_! f^* \to c^* g^* v_!$ to be an isomorphism.  Now consider the composite square
$$\array{u/c & \overset{q}{\to} & A & \overset{f}{\to} & B\\
  ^p\downarrow & \swArrow & \downarrow^u & \swArrow & \downarrow^v\\
  * & \underset{c}{\to}& C & \underset{g}{\to} & D.}$$
Since the left-hand square is of the form considered above, it is exact, so $p_! q^* \to c^* u_!$ is an isomorphism.  Thus $c^* u_! f^* \to c^* g^* v_!$ is an isomorphism if and only if the composite
$$ p_! q^* f^* \to c^* u_! f^* \to c^* g^* v_! $$
is an isomorphism, but this is just the Beck-Chevalley transformation for the composite square
$$\array{u/c & \overset{}{\to} & B\\
  \downarrow &\swArrow & \downarrow^v\\
  * & \underset{g(c)}{\to} & D.}$$
So the given square is exact just when all of these squares are exact.  But we can also play the same game dually, so the given square is exact just when for any $c\in C$ and $b\in B$, the square
$$\array{(b/A/c) & \overset{x}{\to} & *\\
  ^y\downarrow &\swArrow & \downarrow^{v(b)}\\
  * & \underset{g(c)}{\to} & D.}$$
is exact.  However, the comma square
$$\array{D(v(b),g(c)) & \overset{z}{\to} & *\\
  ^w\downarrow &\swArrow & \downarrow^{v(b)}\\
  * & \underset{g(c)}{\to} & D.}$$
is always exact, as observed previously, and by the universal property of a comma square, the previous one factors through this one via a functor $r\colon (b/A/c) \to D(v(b),g(c))$.  Hence we have $y = w r$ and $x = z r$, and the Beck-Chevalley transformation for the $(b/A/c)$ square factors as
$$y_! x^* \cong w_! r_! r^* z^* \to w_! z^* \overset{\cong}{\to} g(c)^* v(b)_!.$$
Hence it is an isomorphism if and only if $y_! x^* \to w_! z^*$ is an isomorphism, which is to say that colimits of constant diagrams on $(b/A/c)$ and on $D(v(b),g(c))$ agree.  But the colimit of a constant diagram is just a [[copower]] with the set of connected components of the domain category, so we recover the same characterization as before.

While this argument does not generalize to general enriched categories and proarrow equipments, it does generalize in a different direction.  The notion of [[derivator]] is essentially designed exactly so that this argument works, up until the last step: in a general derivator, colimits of constant diagrams may depend on more (or less) than the set of connected components of the domain.  For instance, in the derivator of [[∞-groupoids]], the colimit of a constant diagram is a copower with the [[nerve]] of the domain category, a finer invariant than its $\pi_0$.  It is a theorem of Cisinski that this is the finest possible: colimits of constant diagrams in a derivator never depend on anything more than the nerve of the domain.  Therefore, this yields a characterization of the [[homotopy exact squares]] for computing [[homotopy Kan extensions]] in derivators: the squares where the functor $(b/A/c) \to D(v(b),g(c))$ induces a weak equivalence of nerves.


##References

Some of the early theory is in

* [[René Guitart]], _Relations et carrés exacts,_ Ann. Sc. Math. Qué., juillet 1980, vol. IV, N° 2, p. 103-125.

[[!redirects exact squares]]
