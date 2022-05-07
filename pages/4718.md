
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The concept of _nonunital ring_ is like that of [[ring]] but without the requirement of the existence of an [[identity]] element ("unit" element). 

Nonunital rings with [[homomorphisms]] between them form the [[category]] [[Rng]].

Historically, this was in fact the original meaning of "ring", and while mostly "ring" has come to mean by default the version with identity element, nonunital rings still play a role (see e.g. the review in [Anderson 06](#Anderson06)) and in some areas of mathematics "nonunital ring" is still the default meaning of "ring". In particular, non-unital rings may naturally be identified with the [[augmentation ideals]] of $\mathbb{Z}$-[[augmented algebra|augmented]] unital rings, see the discussion [below](#AsSlicesOfRings).
  
+-- {: .num_remark}
###### Remark on terminology

The term "non-unital ring" may be regarded as an example of the "[[red herring principle]]", as a non-unital ring is not in general a ring in the modern sense of the word. 

In [[Bourbaki|Bourbaki 6, chapter 1]] the term _pseudo-ring_ is used, but that convention has not become established.

Another terminology that has been suggested for "nonunital ring", and which is in use in part of the literature (e.g. [Anderson 06](#Anderson06)) is "rng", where dropping the "i" in "ring" is meant to be alluding to the absence of _i_dentity elements. This terminology appears in print first in ([Jacobson](#Jacobson)), where it is attributed to Louis Rowen.

Similarly there is, for whatever it's worth, the suggestion that a ring without negatives, hence a [[semiring]], should be called a _[[rig]]_ (although here one may make a technical distinction about the _additive_ identity). 

=--


## Definitions

### For rings

Specifically:

+-- {: .num_defn}
###### Definition


A __nonunital ring__ or _rng_ is a [[set]] $R$ with operations of addition and multiplication, such that:

*  $R$ is a [[semigroup]] under multiplication;
*  $R$ is an [[abelian group]] under addition;
*  multiplication distributes over addition.

=--

More sophisticatedly, we can say that, just as a ring is a [[monoid object]] in [[Ab]], so 

+-- {: .num_defn}
###### Definition

A _nonunital ring_ or _rng_ is a [[semigroup]] object in [[Ab]].

=--

+-- {: .num_remark}
###### Remark

A non-unital ring may well contain an element that behaves as the [[identity]] element, i.e. it may be in the image of the [[forgetful functor]] from unital rings to nonunital rings. But if so, then this element is still not part of the defining data and in particular a [[homomorphism]] of non-unital rings need not to preserve whatever identity elements may happen to be present.

=--


### For $\mathbb{E}_k$-algebras

[[nonunital Ek-algebras]] are discussed in ([Lurie, section 5.2.3](#Lurie)).


## Properties

### Unitization

+-- {: .num_defn #Unitisation}
###### Definition

Given a non-unital commutative ring $A$, then its _[[unitisation]]_ is the [[commutative ring]] $F(A)$ obtained by [[free construction|freely]] adjoining an [[identity]] element, hence the ring whose underlying [[abelian group]] is the [[direct sum]] $\mathbb{Z} \oplus A$ of $A$ with the [[integers]], and whose product operation is defined by

$$
  (n_1, a_1) (n_2, a_2) \coloneqq (n_1 n_2, n_1 a_2 + n_2 a_1 + a_1 a_2)
  \,,
$$

where for $n \in \mathbb{Z}$ and $a \in A$ we set $n a \coloneqq \underset{n\;summands}{\underbrace{a + a + \cdots + a}}$.


=--

+-- {: .num_remark}
###### Remark

In the unitization $\mathbb{Z} \oplus A$ we have $(n,0) + (0,a) = (n,a)$ and hence it makes sense to abbreviate $(n,a)$ simply to $n+a$.  The product in the [[unitisation]] is then fixed by the defining requirement that $1 \cdot a = a$ and by the [[distributivity law]].

=--

+-- {: .num_remark}

###### Remark

One can also think of the unitisation as the quotient of the polynomial ring "$A[x]$" ($A$ "with a generic element adjoined", i.e. a term algebra) quotiented by the relations $ax - a = 0, xa - a = 0$, so that this $x$ must be a right and left identity for multiplication $a$. Cosets must be represented by expressions of the form $a + nx$; this provides an obvious isomorphism to the above definition, and motivates the multiplication for $\mathbb{Z} \oplus A$ above.

=--

+-- {: .num_remark}

###### Remark

Since $A$ embeds into its unitisation $F(A)$, every [[rng]] lives as an ideal in some [[unital ring|ring]]. We can consider $A$-linear actions $A \curvearrowright M$ on abelian groups $M$. Since the endomorphism rings of abelian groups are always unital, the [[universal property]] of the unitisation-forgetful adjunction (see below) ensures that there is a unique extension of the action map $A \to \operatorname{End}_{\mathbf{Ab}}(M)$ along $A \hookrightarrow \operatorname{for} \circ F(A)$ to an action map $F(A) \to \operatorname{End}_{\mathbf{Ab}}(M)$. This induces an equivalence $A\text{-}\mathbf{Mod} \simeq F(A)\text{-}\mathbf{Mod},$ so that one may as well study $F(A)$ if one wanted to study $A$ through its module category.

=--

+-- {: .num_remark}
###### Remark

Similar [[unitisation]] prescriptions work for non-commutative rings and for [[nonunital algebras]] over a fixed base ring, see also at

* _[[unitisation of C*-algebras]]_.

=--


+-- {: .num_prop}
###### Proposition

Unitisation in def. \ref{Unitisation} extends to a [[functor]] from $CRng$ to [[CRing]] which is [[left adjoint]] to the [[forgetful functor]] from [[commutative rings]] to non-unital commutative rings.

$$
  F \colon CRng \leftrightarrow CRing \colon U
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is because the definition of any ring [[homomorphism]] out of $F(A)= (\mathbb{Z} \oplus A, \cdot)$ is uniquely fixed on the $\mathbb{Z}$-summand.

=--

### Nonunital rings as slices of rings
 {#AsSlicesOfRings}

+-- {: .num_defn #AugmentationIdealFunctor}
###### Definition


Write $CRing_{/\mathbb{Z}}$ for the [[slice category]] of [[CRing]] over the ring of [[integers]] ([[augmented algebra|augmented commutative rings]]). Write

$$
  CRing_{/\mathbb{Z}} \longrightarrow CRng
$$

for the [[functor]] to commutative non-unital rings which sends any $(R \stackrel{\phi}{\to} \mathbb{Z})$ to its _[[augmentation ideal]]_, hence to the [[kernel]] of $\phi$

$$
  (R \stackrel{\phi}{\to} \mathbb{Z}) \mapsto ker(\phi)
  \,.
$$

=--

+-- {: .num_defn #EquivalenceOfNonunitalAndSliced}
###### Proposition

The [[augmentation ideal]]-functor in def. \ref{AugmentationIdealFunctor} is an [[equivalence of categories]] whose inverse is given by [[unitisation]], def. \ref{Unitisation}, remembering the [[projection]] $(\mathbb{Z} \oplus A) \to \mathbb{Z}$:

$$
  CRng \simeq CRing_{/\mathbb{Z}}
  \,.
$$

=--

+-- {: .proof}
###### Proof

That the functor is [[fully faithful]] is to observe that for a ring $R \stackrel{\phi}{\to} \mathbb{Z}$ the [[fiber]] $R_{n}$ over $n \in \mathbb{Z}$ is a [[torsor]] over the additive group underlying the [[augmentation ideal]] $A = R_0 = ker(\phi)$, and moreover it is a pointed torsor, the point being $n$ itself, hence is canonically equivalent to the [[augmentation ideal]] $A$, the equivalence being addition by $n$ in $R$. Hence any homomrphism of rings with identity over $\mathbb{Z}$

$$
  \array{
    R_1 && \stackrel{f}{\longrightarrow} && R_2
    \\
    & {}_{\mathllap{\phi_1}}\searrow && \swarrow_{\mathrlap{\phi_2}}
    \\
    && \mathbb{Z}
  }
$$

is uniquely fixed by its restriction to the augmentation ideal $ker(\phi_1)$, whose image, moreover, has to be in the augmentation ideal $ker(\phi_2)$. 


=--

The identification of non-unital algebras as augmentation ideals of augmented unital algebras is used for instance in ([Fresse 06](#Fresse06)).

+-- {: .num_remark}
###### Remark

In terms of [[arithmetic geometry]], the [[Isbell duality|formally dual]]  statement of prop. \ref{AugmentationIdealFunctor} is that arithmetic geometry induced by non-unital rings is equivalently ordinary arithmetic geometry _under_ [[Spec(Z)]].

=--

+-- {: .num_remark}
###### Remark

The generalization of prop. \ref{EquivalenceOfNonunitalAndSliced} to [[nonunital Ek-algebras]] is ([Lurie, prop. 5.2.3.15](#Lurie)).

=--


## Related concepts

* [[unitisation of C*-algebras]]

* [[noncommutative ring]], [[nonassociative ring]]

* [[rig]]

* [[nonunital Ek-algebra]]

* [[possibly empty nonunital ring]]


## References
 {#References}

### Nonunital ring theory
 {#ReferencesTheory}

The terminology "rng" originates in

* {#Jacobson} Nathan Jacobson _Basic Algebra_.  

A survey of commutative rng theory is in 

* {#Anderson06} D. Anderson, _Commutative rngs_, in J. Brewer et al. (eds.) _Multiplicative ideal theory in Commutative Algebra_, 2006

Discussion of [[module]] theory over rngs (with close relation to [[torsion modules]]) is in 

* {#Quillen96} [[Daniel Quillen]], _Module theory over nonunital rings_, August 1996 ([[QuillenModulesOverRngs.pdf:file]])

Discussion of non-unital rings as [[augmentation ideals]] of augmented unital rings includes

* {#Fresse06} [[Benoit Fresse]], _The Bar Complex of an E-infinity Algebra_, Adv. Math.  223 (2010), pages 2049-2096 ([arXiv:math/0601085](http://arxiv.org/abs/math/0601085))

A definition of [[algebraic K-theory]] for nonunital rings is due to

* {#Quillen} [[Daniel Quillen]], _$K_0$ for nonunital rings and Morita invariance_, J. Reine Angew. Math., 472:197-217, 1996.

with further developments (in [[KK-theory]]) including

* [[Snigdhayan Mahanta]], _Higher nonunital Quillen K'-theory, KK-dualities and applications to topological T-dualities_,  J. Geom. Phys., 61 (5), 875-889, 2011. ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf))

Discussion in the context of [[higher algebra]] ([[nonunital Ek-algebras]]) is in 

* {#Lurie} [[Jacob Lurie]], section 5.2.3 of _[[Higher Algebra]]_


[[!redirects rng]]
[[!redirects rngs]]

[[!redirects nonunital ring]]
[[!redirects nonunital rings]]
[[!redirects non-unital ring]]
[[!redirects non-unital rings]]

[[!redirects unitization of a ring]]
[[!redirects unitization of rings]]
[[!redirects unitizations of rings]]
[[!redirects unitisation of a ring]]
[[!redirects unitisation of rings]]
[[!redirects unitisations of rings]]

[[!redirects unitization of a commutative ring]]
[[!redirects unitization of commutative rings]]
[[!redirects unitizations of commutative rings]]
[[!redirects unitisation of a commutative ring]]
[[!redirects unitisation of commutative rings]]
[[!redirects unitisations of commutative rings]]
