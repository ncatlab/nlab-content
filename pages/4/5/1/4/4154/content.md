
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-category theory
+--{: .hide}
[[!include quasi-category theory - contents]]
=--
=--
=--

# Homotopy exact squares
* automatic table of contents
{:toc}

## Idea

A *homotopy exact square* is the analogue of an [[exact square]] which applies to [[homotopy Kan extensions]], or equivalently to [[(∞,1)-Kan extensions]].  It is especially important in the theory of [[derivators]], which provide a calculus for computing with homotopy Kan extensions whose primary tool is the use of homotopy exact squares.

## Definition

Let $A$, $B$, $C$, and $D$ be small [[categories]], and consider a square of [[functors]]
$$\array{A & \overset{f}{\to} & B\\
  ^u\downarrow & \swArrow & \downarrow^v\\
  C& \underset{g}{\to} & D}$$
which is inhabited by a [[natural transformation]] (which might be an [[identity]]).  Let $M$ be either

* a [[model category]],
* a [[simplicially enriched category]] (or a topologically enriched category, or a [[dg-category]]),
* an [[(∞,1)-category]] (of any sort), or
* a [[derivator]].

We write $M^A$, $M^B$, etc. for the model categories, simplicial categories, $(\infty,1)$-categories, or homotopy categories of diagrams in $M$ of whatever shape.  We write $f^*\colon M^B\to B^A$, $g^*\colon M^D\to M^C$, and so on for precomposition functors, which are always homotopically meaningful, and we write $u_!\colon M^A\to M^C$, $v_!\colon M^B\to M^D$ and so on for the homotopically meaningful notions of pointwise [[left Kan extension]].  Specifically:

* If $M$ is a model category, then $u_!$ denotes the left [[derived functor]] of pointwise Kan extension along $u$.
* If $M$ is a simplicially enriched category, then $u_!$ is the coherent pointwise [[homotopy left Kan extension]] along $u$, which may be defined explicitly in various ways, such as using a [[bar construction]].
* If $M$ is an $(\infty,1)$-category, then $u_!$ denotes the pointwise [[(∞,1)-Kan extensions]] along $u$.
* If $M$ is a derivator, then $u_!$ simply denotes the left adjoint of $u^*$ (which is assumed to exist and to "be pointwise" by the derivator axioms).

Assume that $M$ is such that the relevant extensions $u_!$ and $v_!$ exist.  Then there is a canonical [[Beck-Chevalley transformation]]
$$ u_! f^* \to g^* v_! $$
defined as the composite
$$ u_! f^* \to u_! f^* v^* v_! \to u_! u^* g^* v_! \to g^* v_!. $$
and we say that the given square is **$M$-exact** if this transformation is an [[equivalence]].  If the square is $M$-exact for all $M$, we say it is **homotopy exact**.  Note that by the general calculus of [[mates]], this is equivalent to requiring that the dual transformation
$$ v^* g_* \to f_* u^* $$
is an equivalence, where $f_*$ and $g_*$ denote the analogous sort of *right* Kan extension.

Of course when we say "for all $M$" we need to specify what sorts of $M$ we consider.  However, we actually get the *same* definition regardless of whether we mean "for all model categories $M$" or "for all simplicially enriched categories $M$" or "for all $(\infty,1)$-categories $M$" or "for all derivators $M$".  This is a nontrivial theorem, especially in the case of derivators.

## Remarks

Since any 1-category is a degenerate sort of $(\infty,1)$-category, any homotopy exact square is [[exact square|exact]] in the usual 1-categorical sense, but the converse is not true.  This also implies that a square can be $M$-exact for some particular $M$ without being homotopy exact.  However, there exists a "universal" $M$ such that $M$-exactness is equivalent to homotopy exactness, namely $M=\infty Gpd$.

## Characterization

Of course, the above definition is "functional", while in practice we want some more combinatorial characterization which is easier to check.  This can be done completely analogously to the characterization of ordinary [[exact squares]] using comma objects, except that at the last step we need to consider a more restricted notion of "equivalence" (i.e. a more restricted [[basic localizer]]).

The characterization is the following.  Given $b\in B$ and $c\in C$ and $\varphi\colon v(b) \to g(c)$, let $(b/A/c)_\varphi$ denote the category whose objects are triples $(a,\alpha,\beta)$ with $\alpha\colon u(a)\to c$ and $\beta\colon b\to f(a)$ such that $g(\alpha) \circ v(\beta) = \varphi$, and whose morphisms are morphisms $a\to a'$ making two triangles commute.

+-- {: .un_theorem}
###### Theorem
A square is homotopy exact if and only if each category $(b/A/c)_\varphi$ has a [[contractible space|contractible]] [[nerve]].
=--

* See [exact square](/nlab/show/exact+square#CommaObj) for the proof that is being generalized.
* See [derivator](/nlab/show/derivator#ExactSquares) for the proof in the case of derivators, which relies on Cisinski's characterization of [[basic localizers]].
* The proof in the (∞,1)-categorical case generalizes the characterization of [final (∞,1)-functors](/nlab/show/final+(∞,1%29-functor#Properties).

## Examples

### Comma squares

Any [[comma square]] is homotopy exact.  In other words, if $A=(v/g)$ is the [[comma category]] with $f$ and $u$ the canonical projections, then the square is homotopy exact.  If in addition $C=*$ is the [[terminal category]], then $g$ just picks out an object $d\in D$ and $A$ is the comma category $(v/d)$; thus this says that (pointwise) homotopy Kan extensions can be computed pointwise as homotopy limits over such comma categories.

### Fully faithful functors

If $u\colon A\to B$ is a [[fully faithful functor]], then the square
$$\array{A & \overset{id}{\to} & A\\
  ^{id}\downarrow && \downarrow^u\\
  A & \underset{u}{\to} & B}$$
is homotopy exact.  This just says that the unit $Id_A \to u^* u_!$ is an isomorphism, i.e. that left (and equivalently right) homotopy Kan extensions along $u$ are "honest" extensions.

### Final functors

A functor $u\colon A\to B$ is a [[homotopy final functor]] if and only if the square
$$\array{A & \overset{u}{\to} & B\\
  \downarrow && \downarrow\\
  *& \underset{}{\to} & *}$$
is homotopy exact.  Homotopy exactness of this square says that for $F\colon B\to M$, the canonical map $hocolim_A u^*F \to hocolim_B F$ is an isomorphism, which is one equivalent definition of when $u$ is homotopy final.  In this case, the characterization theorem reduces to saying that $u$ is homotopy final if and only if each comma category $b/u$ has a contractible nerve, which is a known characterization of homotopy final functors.

### Pullbacks of fibrations {#PullbacksOfFibrations}

This example is due to [Moritz Groth](#Groth).  Let $p\colon C\to D$ be a [[Grothendieck opfibration]], and suppose that
$$\array{ A & \xrightarrow{u} & C \\
  ^v\downarrow && \downarrow^p\\
  B & \xrightarrow{q} & D } $$
is a [[pullback]] in [[Cat]].  Then we claim that this square is homotopy exact.

For a proof, suppose given $b\in B$ and $c\in C$ and a morphism $\phi\colon p(c) \to q(b)$, and let $X$ be the category whose contractibility we must check.  By definition, since $A = B\times_D C$, an object of $X$ consists of objects $c'\in C$ and $b'\in B$ such that $p(c') = q(b')$, and morphisms $\alpha\colon c\to c'$ and $\beta\colon b' \to b$ such that $q(\beta) . p(\alpha) = \phi$.

Let $Y$ be the full subcategory of $X$ consisting of those objects with $b'=b$ and $\beta$ the identity, so that an object of $Y$ is an object $c'\in C$ such that $p(c') = q(b)$ together with a morphism $\alpha\colon c\to c'$ such that $p(\alpha) = \phi$.  Then the inclusion $Y\hookrightarrow X$ has a left adjoint, which sends $(b',c',\alpha,\beta)$ to $(b, q(\beta)_!(c'), \overline{q(\beta)}.\alpha, 1_b)$, where $\overline{q(\beta)}\colon c' \to q(\beta)_!(c')$ is an opcartesian arrow over $q(\beta)$.  Therefore, the nerves of $Y$ and $X$ are homotopy equivalent.

But $Y$ has an initial object, namely $(\phi_!(c), \overline{\phi})$, where $\overline{\phi}\colon c \to \phi_!(c)$ is an opcartesian arrow over $\phi$.  Thus the nerve of $Y$ is contractible, and thus so is the nerve of $X$.

Groth has also proved that homotopy-exactness of such squares can be used to replace that of comma squares in the definition of a [[derivator]].


## References

* An [nCaf&#233; post](http://golem.ph.utexas.edu/category/2010/06/exact_squares.html) about (mostly ordinary) [[exact squares]]

* [[Moritz Groth]], "Derivators, pointed derivators, and stable derivators" [PDF](http://www.math.uni-bonn.de/~mgroth/groth_derivators.pdf)
{#Groth}

* [[Georges Maltsiniotis]], "Carr&#233;s exacts homotopiques, et d&#233;rivateurs", Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques 53 (2012), 3-63
[PDF](http://webusers.imj-prg.fr/~georges.maltsiniotis/ps/carhex.pdf)
{#Maltsiniotis}


[[!redirects homotopy exact squares]]
[[!redirects homotopically exact square]]
[[!redirects homotopically exact squares]]
