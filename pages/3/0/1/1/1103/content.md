
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential-graded objects
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents
{:toc}

## Definition

### Abstract definition

A __dg-algebra__, or __[[differential graded algebra]]__, is equivalently

1. An [[associative algebra]] $A$ which is in addition [[graded algebra]] and a [[differential algebra]] in a compatible way (with the [[differential]] [[derivation]] being of degree $\pm$ 1);

1. a [[monoid]] in the [[symmetric monoidal category]] of (possibly unbounded) [[chain complexes]] or [[cochain complex]]es with its standard structure of a [[monoidal category]] by the [[tensor product of chain complexes]];

For the case of chain complexes we also speak of **chain algebras**.

For the case of cochain complexes we also speak of **cochain algebras**.

Recall 

* that the standard tensor product on (co)chain complexes is given by
$$
(A\otimes B)_n = \sum_{i+j=n} A_i\otimes B_j,
$$
with the differential $d_{A\otimes B} = d_A\otimes B + A\otimes d_B$.

* that a [[monoid]] in a [[monoidal category]] $C$ is an object $A$ in $C$ together with a morphism

  $$
    \cdot : A \otimes A \to A
  $$

  that is unital and associative in the obvious sense.

This implies that a dg-algebra is, more concretely, a graded algebra $A$ equipped with a linear map $d : A \to A$ with the property that

* $d\circ d = 0$

* for $a \in A$ homogeneous of degree $k$, the element $d a$ is of degree $k+1$ (for monoids in cochain complexes) or of degree $k-1$ (for monoids in chain complexes)

* for all $a,b \in A$ with $a$ homogeneous of degree k the **graded Leibniz rule** holds

  $d (a \cdot b) = (d a) \cdot b + (-1)^k a \cdot (d b)$.   

The dg-algebras form a category, [[dgAlg]].


### Detailed component definition

#### Pre-graded algebras

A _pre-graded algebra- (pre-ga) or $\mathbb{Z}$-graded algebra_ is a pre-gvs, $A$, together with an algebra multiplication satisfying $A_p.A_q \subseteq A_{p+q}$ for any $p,q$.  The relevant morphisms are pre-gvs morphisms which respect the multiplication.  This gives a category $pre GA$.

An _augmentation_ of a pre-ga, $A$, is a homomorphism $\varepsilon : A \to k$.  The _augmentation ideal_ of $(A,\varepsilon)$ is $ker \varepsilon$ and will also be denoted $\bar{A}$.  The pair $(A,\varepsilon)$ is called an _augmented pre-ga_.  

A morphism $f:(A,\varepsilon)\to (A',\varepsilon')$ of augmented pre-gas is a homomorphism $f : A \to A'$ (thus of degree zero) such that $\varepsilon = \varepsilon ' f$.  The resulting category will be written $pre \varepsilon GA$. 


#### Tensor product

If $A$, $A'$ are two pre-gas, then $A\otimes A'$ is a pre-ga with

$$(a\otimes a')(b\otimes b') = (-1)^{|{a^'} | |b|} a b \otimes a' b'$$

for homogeneous $a,b \in A$, $a', b' \in A'$.

If $\varepsilon, \varepsilon$ are augmentations of $A$ and $A'$ respectively, then $\varepsilon\otimes \varepsilon'$ is an augmentation of $A\otimes A'$.


#### Derivations

Let $A$ be a pre-ga. An _(algebra) derivation_ of degree $p\in \mathbb{Z}$ is a linear map $\theta \in Hom_p(A,A)$ such that 

$$\theta(ab) = \theta(a)b + (-1)^{p|a|}a\theta(b)$$

for homogeneous $a,b \in A$.

A derivation $\theta$ of an augmented algebra, $(A, \varepsilon)$, is an algebra derivation which, in addition, satisfies $\varepsilon \theta = 0$.

Let $Der_p(A)$ be the vector space of derivations of degree $p$ of $A$, then $Der(A) = \bigoplus_p Der_p(A)$ is a pre-gvs.

#### N.B.

In the case of upper gradings, an element of $Der_p(A)$ sends $A^n$ into $A^{n-p}$.



#### Pre-DGAs

A _differential_ $\partial$ on an (augmented) pre-ga is a derivation of the (augmented) algebra of degree -1 such that $\partial\circ\partial = 0$.


  The pair $(A,\partial)$ is called a _pre-differential graded algebra_ (pre-dga).  If $A$ is augmented, then $(A,\partial)$ will be called an _augmented pre-dga_ $pre \varepsilon dga$. 

If $(A,\partial)$ and $(A',\partial')$ are pre-dgas, then $(A,\partial)\otimes (A',\partial')$, with the conventions already noted, is one as well.


A morphism of pre-dgas (or pre-$\varepsilon$-dgas) is a morphism which is both of pre-gdvs and of pre-gas (with $\varepsilon$ as well if used).  This gives categories $pre DGA$ and $pre \varepsilon DGA$.



#### Commutative graded algebras (CGA)


A pre-ga $A$ is said to be _[[graded commutative algebra|graded commutative]]_ if $ab = (-1)^{|a||b|}ba$ for each pair, $a, b$, of elements of $A$ of homogeneous degree.
 
Commutativity is preserved by tensor product. 

We get obvious full subcategories $pre CDGA$ and $pre \varepsilon CDGA$ corresponding to the case with differentials.


#### CDGAs

A cdga is a **negatively** graded pre-cdga (in upper grading), $A= \bigoplus_{p\geq 0} A^p.$

There is an augmented variant, of course.  These definitions give categories $CDGA$, etc.

See at _[[differential graded-commutative algebra]]_.


#### $n$-connectivity

An $\varepsilon$cdga $(A,d)$ is _$n$-connected_ (resp. _cohomologically $n$-connected_ if $\bar{A}^p = 0 $ for $p\leq n$, (resp. $\overline{H(A,d)}^p = 0$ for $p\leq n$).  This gives subcategories $CDGA^n$ and $CDGA^{c n}$.



#### Filtrations

A filtration on a pre-ga, $A$, is a filtration on $A$, so that $F_p A \subseteq F_{p+1}A$, $F_p A.F_n A \subseteq F_{p+n}A$ (and, if $A$ is differential, also $\partial F_p A \subseteq F_p A$).



##### Example: Word length filtration.

Let $A$ be an augmented pre-ga and denote by 

$$\bar{\mu}^p : \bigotimes^{p+1}\bar{A} \to \bar{A},$$ 

the iterated multiplication.  The **decreasing word length filtration**, $F^p A$ is given by:

$$F^0 A = A, \quad F^p A = Im\bar{\mu}^{(p-1)}  if p\geq 1.$$

$Q(A) = \bar{A}/Im\bar{\mu}$ is the _space of indecomposables_ of A.

If $(A,\partial)$ is an augmented pre-dga, $F^p A$ is stable under $\partial$ and we get $Q(\partial)$ is a differential on $Q(A)$ and hence we get a functor  $Q: pre \varepsilon DGA\to pre DGVS.$


#### Free GAs: $T(V)$, the tensor algebra

Given a pre-gvs, $V$, the tensor algebra generated by $V$ is given by $T(V) = \bigotimes_{n\geq 0}V^{\otimes n}$.  

The augmentation sends $V$ to 0. $V^{\otimes n}$ is given the tensor product grading, and the multiplication is given by the tensor product.
+-- {: .lemma }
###### Lemma (classical: freeness of $T(V)$, $T$ is a left adjoint)
If $A$ is a pre-ga and $f: V\to A$, a morphism to the underlying pre-gvs of $A$, there is a unique extension $\hat{f} :T(V)\to A$, which is a morphism of pre-gvs.
=--


#### Free CGAs: $\bigwedge V$

This is the tensor product of the exterior algebra on the odd elements and the symmetric algebra on the even ones:

$$\bigwedge V = E(\bigoplus V_{2p+1})\otimes S(\bigoplus V_{2p}).$$

It satisfies $\bigwedge(V \oplus W) \cong (\bigwedge V)\oplus (\bigwedge W)$.

If $A$ is a pre-cga, any morphism, $f : V\to A$, to the underlying pre-gvs of $A$, has a unique extension to a pre-cga morphism $\bar{f} :\bigwedge V \to A$.

If $(e_\alpha)_{\alpha \in I}$ is a homogeneous basis for $V$, $\bigwedge V$ and $T(V)$ may be written $\bigwedge((e_\alpha)_{\alpha \in I})$ and $T((e_\alpha)_{\alpha \in I})$ respectively.

**Note:**
 
*  $T(V)$ is a non-commutative polynomial algebra, 

*  $\bigwedge V$ is a commutative polynomial algebra.


#### Word length filtrations on $\bigwedge V$ and $T(V)$.

On $\bigwedge V$ (resp.  $T(V)$) write 

$$\bigwedge V = \bigoplus_{k\geq 0}\bigwedge^k V,$$

where $\bigwedge^k V$ is the subspace generated by all $v_1\wedge \ldots \wedge v_k$ with $v_1 \in V$.  Then $F^p  \bigwedge V = \bigwedge^{\geq p} V = \bigoplus_{k\geq p}\bigwedge^k V$, resp. $T^k (V) = V^{\otimes k}$ and $F^p T(V) = T^{\geq p}(V) = \bigoplus_{k\geq p} T^k (V)$).

If $(\bigwedge V,d)$ is a pre-cdga, which is free as a pre-cga on a fixed $V$, then $d$ is the sum of derivations $d_k$ defined by the condition $d_k (V) \subseteq \bigwedge^k V$.  There is an isomorphism between $V$ and $Q(\bigwedge V)$, which identifies $d_1$ with $Q(d)$. The derivation $d_1$ (resp. $d_2$) is called the _linear part_ (resp. _quadratic part_) of $d$.



#### Sum and Product of CDGAs.

If $(A,d)$ and $(A',d')$ are two cdgas, their (categorical) _sum_ (i.e. coproduct) is their tensor product, $(A,d)\otimes(A',d' )$, whilst their product is the 'direct sum', $(A,d)\oplus (A',d' )$.


#### Koszul convention

Given a permutation $\sigma$ of a graded object $(x_1, \ldots, x_p)$, the _Koszul sign_, $\varepsilon(\sigma)$ is defined by 

$$x_1\wedge \ldots \wedge x_p = \varepsilon(\sigma)x_{\sigma(1)} \wedge \ldots \wedge x_{\sigma(p)}$$

in $\bigwedge(x_1, \ldots, x_p )$. We note that although we write $\varepsilon(\sigma)$, $\sigma$ does not suffice to define it as it depends also on the degrees of the various $x_i$.

### Terminology

Baues (in his book on [_Algebraic Homotopy_](#Baues)) has suggested using the terminology **chain algebra** for positively graded differential algebras  and **cochain algebras** for the negatively graded ones. This seems to be a very useful convention.

### Enrichment of dg-algebras over dg-coalgebras

Given a dg-coalgebra $C$ and a dg-algebra $B$,
the vector space of linear maps $C\to B$
admits a dg-algebra structure
using the coproduct on $C$ and product on $B$.
This dg-algebra is known as the __convolution algebra__ of $C$ and $B$
and is denoted by $[C,B]$.

The resulting functor
$$[-,-]: dgCoalg^op \times dgAlg \to dgAlg$$
is a part of an [[adjunction in two variables]], whose other adjoints are
$$\triangleright: dgCoalg\times dgAlg\to dgAlg$$
(the Sweedler product)
and
$$\{-,-\}:dgAlg^op\times dgAlg\to dgCoalg$$
(the Sweedler hom).

Taken together, these three functors
turn the [[symmetric monoidal category]]
of dg-algebras into an [[enriched category]]
over the [[closed symmetric monoidal category]]
of dg-coalgebras.

See [Anel and Joyal](#AnelJoyal) for more information.


## Related concepts

* [[differential algebra]]

### Model category structure

There is a standard [[model category]] structure on $dgAlg$.See [[model structure on dg-algebras]].

### Cosimplicial algebras

The [[monoidal Dold-Kan correspondence]] effectively identifies non-negatively graded [[chain complex]] algebras with simplicial algebras, and non-negatively graded [[cochain complex]] algebras with [[cosimplicial algebra]]s.

Since cosimplicial algebras have a fundamental interpretation dual to [[∞-space]], as described at [[∞-quantity]], this can be understood as explaining the great role differential graded algebras are playing in various context, suchh as notably in 

* [[rational homotopy theory]].

### dg-coalgebra

Dually, a [[comonoid]] in [[chain complex]]es is a [[dg-coalgebra]].

### Homological smoothness

A dga $A$ is __[[homologically smooth dga|homologically smooth]]__ if as a dg-bimodule $_A A_A$ over itself it has a bounded resolution by finitely generated projective dg-bimodules.

### Formal dg-algebra

A dg-algebra $A$ is a [[formal dg-algebra]] if there exists a morphism

$$
  A \to H^\bullet(A)
$$

to its [[chain homology and cohomology|chain (co)homology]] (regarded as a dg-algebra with trivial differential) that is a [[quasi-isomorphism]].

### Curved dg-algebra

* [[curved dg-algebra]]


## References

* {#Baues} [[Hans Joachim Baues]], _[[Algebraic Homotopy]]_, Cambridge Studies in Advanced Mathematics **15**, Cambridge University Press (1989) &lbrack;[doi:10.1017/CBO9780511662522](https://doi.org/10.1017/CBO9780511662522)&rbrack;

* {#AnelJoyal} [[Mathieu Anel]], [[André Joyal]], _Sweedler theory of (co)algebras and the bar-cobar constructions_ &lbrack;[arXiv:1309.6952](https://arxiv.org/abs/1309.6952)&rbrack; 

Twisted tensor products of smooth dg algebras:

* [[Dmitri Orlov]]. *Smooth DG algebras and twisted tensor product*, Russian Math. Surveys, 78 (2023), 5, 853–880. ([arXiv:2305.19799](https://arxiv.org/abs/2305.19799)).

* [[Dmitri Orlov]]. *Twisted tensor product, smooth DG algebras, and noncommutative resolutions of singular curves* (2024). ([arXiv:2405.04738](https://arxiv.org/abs/2405.04738)).

[[!redirects differential graded algebras]]
[[!redirects differential graded module]]
[[!redirects chain algebra]]
[[!redirects cochain algebra]]
[[!redirects dg-algebra]]
[[!redirects dg-algebras]]

[[!redirects differential-graded algebra]]
[[!redirects differential-graded algebras]]

[[!redirects graded differential algebra]]
[[!redirects graded differential algebras]]

[[!redirects commutative dg-algebra]]
[[!redirects commutative dg-algebras]]

[[!redirects commutative differential graded algebra]]
[[!redirects commutative differential graded algebras]]


[[!redirects homologically smooth differential graded algebra]]
[[!redirects homologically smooth dga]]
