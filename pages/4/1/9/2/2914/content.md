

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition ##

+-- {: .num_prop}
###### Proposition


For $C$ a [[model category]] and $X \in C$ an [[object]], the [[over category]] $C/X$ as well as the [[undercategory]] $X/C$ inherit themselves structures of model categories whose [[fibrations]], [[cofibration]]s and [[weak equivalences]] are precisely the morphism that become fibrations, cofibrations and weak equivalences in $C$ under the forgetful functor $C/X \to C$ or $X/C \to C$.

=--

## Properties ##

### Cofibrant generation, properness, combinatoriality

+-- {: .num_prop #ModelStructureInheritsGoodProperties}
###### Proposition

If $\mathcal{C}$ is

* a [[cofibrantly generated model category]]

* or a [[proper model category]]

* or a [[cellular model category]]

then so are $\mathcal{C}_{/X}$ and $\mathcal{C}^{X/}$.

More in detail, if $I,J \subset Mor(\mathcal{C})$ are the classes of [[generating cofibrations]] and of generating acylic cofibrations of $\mathcal{C}$, respectively, then 

* the generating (acyclic) cofibrations of $\mathcal{C}^{X/}$ are the image under $X \sqcup(-)$ of those of $\mathcal{C}$.

=--

This is spelled out in ([Hirschhorn 05](#Hirschhorn05)).

+-- {: .num_prop #ModelStructureInheritsCombinatorial}
###### Proposition

If $\mathcal{C}$ is a [[combinatorial model category]], then so is $\mathcal{C}_{/X}$.

=--

+-- {: .proof}
###### Proof

By [basic properties](locally+presentable+category#Properties) of [[locally presentable categories]] they are stable under slicing. Hence with $\mathcal{C}$ locally presentable also $\mathcal{C}_{/X}$ is, 
and by prop. \ref{ModelStructureInheritsGoodProperties} with $\mathcal{C}$ cofibrantly generated also $\mathcal{C}_{/X}$ is. 

=--

+-- {: .num_prop #ModelStructureInheritsEnriched}
###### Proposition

If $\mathcal{C}$ is an [[cartesian enriched model category]], then so is $\mathcal{C}_{/X}$.

=--

+-- {: .proof}
###### Proof

By basic properties of [[cartesian enriched categories]] they are stable under slicing, where tensoring is computed in $\mathcal{C}$.
Hence with $\mathcal{C}$ enriched also $\mathcal{C}_{/X}$ is.
The [[pushout product axiom]] now follows from the fact
that in overcategories pushouts can be computed in the underlying category $\mathcal{C}$.
The [[unit axiom]] follows from the unit axiom of $\mathcal{C}$
using the fact that tensorings are computed in $\mathcal{C}$.

=--

### Models for over (∞,1)-categories]

When restricted to fibrant objects, the operation of forming over category of a model category induces the operation of forming the [[over (∞,1)-category]] of an [[(∞,1)-category]].

More explicitly, for a model category $C$, let $\gamma : C \to L(C)$ denote the localization (as an [[(∞,1)-category]]) inverting the weak equivalences. (this can equivalently be computed by a [[simplicial localization]]; see the [[model structure on relative categories]])

+-- {: .num_prop #PresentationOfSliceInfinityCatAlt}
###### Proposition

If $C$ is a [[model category]] and $X \in C$ is fibrant, then $\gamma$ induces a map $C/X \to L(C)/\gamma(X)$, which induces an equivalence $L(C/X) \to L(C)/\gamma(X)$.

=--

The main result is corollary 7.6.13 of ([Cisinski](#Cisinski20)). Model categories are (∞,1)-categories with weak equivalences and fibrations as defined in
definition [Cisinski 7.4.12](#Cisinski20).


### Derived hom-spaces

+-- {: .num_prop #PresentationOfSliceInfinityCat}
###### Proposition

If $C$ is a [[simplicial model category]] and $X \in C$ is fibrant, then
the [[overcategory]] $C/X$ with the above slice model structure is a [[presentable (infinity,1)-category|presentation]] of the 
[[over-(∞,1)-category]] $C^\circ / X$: we have an [[equivalence of (∞,1)-categories]]

$$
  (C/X)^\circ \simeq C^\circ / X
  \,.
$$

=--


+-- {: .proof}
###### Proof

It is clear that we have an [[essentially surjective (∞,1)-functor]] $C^\circ/X \to (C/X)^\circ$. What has to be shown is that this is a [[full and faithful (∞,1)-functor]] in that it is an [[equivalence in an (∞,1)-category|equivalence]] on all [[hom-object|hom]]-[[∞-groupoid]]s $C^\circ/X(a,b) \simeq (C/X)^\circ(a,b)$.

To see this, notice that the hom-space in an [[over-(∞,1)-category]] $C^\circ/X$ between objects $a : A \to X$ and $b : B \to X$ is given (as discussed there) by the 
[[(∞,1)-pullback]]

$$
  \array{
    C^\circ/X(A \stackrel{a}{\to} X, B \stackrel{b}{\to} X) 
     &\to& C^\circ(A,B)
    \\
    \downarrow && \downarrow^{\mathrlap{b_*}}
    \\
    {*} &\stackrel{a}{\to}& C^\circ(A,X)
  }
$$

in [[∞Grpd]].

Let $A \in C$ be a cofibrant representative and $b : B \to X$ be a 
fibration representative in $C$ (which always exists) of the objects of these names in $C^\circ$, respectively. In terms of these we have a cofibration

$$
  \array{
    \emptyset &&\hookrightarrow&& A
    \\
    & \searrow && \swarrow_{\mathrlap{a}}
    \\ 
    && X
  }
$$

in $C/X$, exhibiting $a$ as a cofibrant object of $C/X$;  and a fibration

$$
  \array{
    B &&\stackrel{b}{\to}&& X
    \\
    & {}_{\mathllap{b}}\searrow && \swarrow_{\mathrlap{Id}}
    \\ 
    && X
  }
$$

in $C/X$, exhibiting $b$ as a fibrant object in $C/X$.
 
Moreover, the diagram in [[sSet]] given by

$$
  \array{
    C/X(a, b) &\to& C(A,B)
    \\
    \downarrow && \downarrow^{\mathrlap{b_*}}
    \\
    {*} &\stackrel{a}{\to}& C(A,X)
  }
$$

is 

1. a [[pullback]] diagram in [[sSet]] (by the definition of morphism in an ordinary [[overcategory]]);

1. a [[homotopy pullback]] in the [[model structure on simplicial sets]], because  by the axioms on the [[sSet]]${}_{Quillen}$ [[enriched model category]] $C$ and the above (co)fibrancy assumptions, all objects are [[Kan complex]]es and the right vertical morphism is a [[Kan fibration]]. 

1. has in the top left the correct [[derived hom-space]] in $C/X$ (since $a$ is cofibrant and $b$ fibrant).

This means that this correct hom-space $C/X(a,b) \simeq (C/X)^\circ(a,b) \in sSet$ is indeed a model for $C^\circ/X(a,b) \in \infty Grpd$.

=--

## Quillen adjunctions between slice categories

+-- {: .num_prop #AdjunctionSliceCat}
###### Proposition

Given an adjunction $L\dashv R$ with $L\colon A\to B$ and $R\colon B\to A$,
the following compositions define two Quillen ajdunctions between associated slice categories.
If $X\in A$, then
$$L:A/X\leftrightarrows B/L X:R$$
is an adjunction,
where is the composition $R\colon B/L X\to A/R L X\to A/X$, the second arrow is the base change functor along the unit $X\to R L X$.
If $Y\in B$, then
$$L:A/R Y\leftrightarrows B/Y:R$$
is an adjunction,
where $L\colon A/R Y\to B/L R Y\to B/Y$.
The first adjunction is a Quillen equivalence if $X$ is cofibrant and $L X$ is fibrant.
The second adjunction is a Quillen equivalence if $Y$ is fibrant.

=--


+-- {: .proof}
###### Proof

These adjunctions are Quillen adjunctions because their left (respectively right) adjoints
are left (respectively right) Quillen functors: in the model structures on
slice categories (co)fibrations and weak equivalences are created by the forgetful functor to $A$ or $B$,
see Hirschhorn's note ([Hirschhorn 05](#Hirschhorn05)).
An object in $A/X$ given by an arrow $Z\to X$ is cofibrant if and only if $Z$ is cofibrant and fibrant if and only if $Z\to X$ is a fibration.
Quillen's criterion for Quillen equivalences now yields the statements about equivalences.

=--

## Examples

* the [[classical model structure on pointed topological spaces]] is the model structure on the undercategory under the point of the [[classical model structure on topological spaces]].

## Related concepts


* [[over-category]] 

  * [[slice category]] 

  * [[under category]] 

  * [[over topos]]


* [[over (∞,1)-category]],

  * **model structure on an over-category**

  * [[over-(∞,1)-topos]]

* [[opposite model structure]]



## References 

* {#Hirschhorn02} [[Philip Hirschhorn]], Theorem 7.6.5 of: _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

* {#Hirschhorn05} [[Philip Hirschhorn]], _Overcategories and undercategories of model categories_, 2005 ([pdf](http://www-math.mit.edu/~psh/undercat.pdf), [arXiv:1507.01624](https://arxiv.org/abs/1507.01624))

* {#Cisinski20} [[Denis-Charles Cisinski]], _Higher category theory and homotopical algebra_ ([pdf](http://www.mathematik.uni-regensburg.de/cisinski/CatLR.pdf))

[[!redirects model structure on an overcategory]]
[[!redirects model structure on an under category]]
[[!redirects model structure on an undercategory]]

[[!redirects model structure on a slice category]]
[[!redirects model structure on a coslice category]]

[[!redirects model structures on a slice category]]
[[!redirects model structures on a coslice category]]


[[!redirects slice model category]]
[[!redirects slice model categories]]

[[!redirects slice model structure]]
[[!redirects slice model structures]]

[[!redirects coslice model category]]
[[!redirects coslice model categories]]

[[!redirects coslice model structure]]
[[!redirects coslice model structures]]

[[!redirects co-slice model category]]
[[!redirects co-slice model categories]]

[[!redirects co-slice model structure]]
[[!redirects co-slice model structures]]
