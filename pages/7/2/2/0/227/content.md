

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents 
{:toc}

## Idea
 {#Idea}

A _ring_ (also: _number ring_) is a basic structure in [[algebra]]: a [[set]] equipped with two [[binary operation]]s called _addition_ and _multiplication_, such that the operation of addition forms an [[abelian group]] and the operation of multiplication a [[monoid]] structure which [[distributivity law|distributes]] over addition.

All the familiar number systems such as the [[integer numbers]], [[rational numbers]], [[real numbers]], [[complex]] numbers are rings under the standard operations of addition and multiplication. Except for the first in this list they are indeed [[fields]], which are rings in which also the multiplication operation has an inverse for every element except 0 (the additive neutral element).

Other basic examples of rings are the [[cyclic groups]] $\mathbb{Z}_n$ under their mod-$n$ operations inherited from the integers ([[cyclic rings]]); the [[polynomial rings]], etc.

More abstractly, a [[ring]] is a [[monoid object|monoid]] [[internalization|internal to]] [[abelian groups]] (with their [[tensor product of abelian groups]]), and this perspective helps to explain the central relevance of the concept, owing to the fundamental nature of the notion of _[[monoid objects]]_. Accordingly monoids internal to other [[abelian categories]] and more generally [[stable infinity-categories]] constitute generalizations of the notion of _ring_ that are of interest. Notably when abelian groups are generalized to their analogs in [[stable homotopy theory]], namely to [[spectra]], the corresponding internal monoids are [[E-infinity rings]], a basic structure in [[higher algebra]].

Rings form a category, [[Ring]], which contains the category of commutative rings, [[CRing]], as a subcategory.

## Definition


+-- {: .num_defn}
###### Definition

A [[ring]] (unital and not-necessarily commutative) 
is an [[abelian group]] $R$ equipped with 

1. an element $1 \in R$ 

1. a [[bilinear map]], hence a [[group homomorphism]]

   $$
     \cdot : R \otimes R \to R
   $$

   out of the [[tensor product of abelian groups]], 

such that $\cdot$ is [[associativity law|associative]] and [[unit law|unital]] with respect to 1.

=--

+-- {: .num_remark}
###### Remark

The fact that the product is a [[bilinear map]] is the 
**[[distributivity law]]**: for all $r, r_1, r_2 \in R$ we have

$$
  r \cdot (r_1 + r_2) = r \cdot r_1 + r \cdot r_2
$$

and

$$
  (r_1 + r_2) \cdot r = r_1 \cdot r + r_2 \cdot r
  \,.
$$


=--


+-- {: .num_prop}
###### Proposition

A (unital, non-commutative) **ring** is (equivalently)

* a [[monoid object|monoid]] [[internalization|internal to]] [[Ab]] regarded as a [[monoidal category]] equipped with the [[tensor product of abelian groups]];  
* a [[pointed object|pointed]] [[enriched category|category enriched over]] [[Ab]] with a single [[object]].
* a [[ringoid]] with a single [[object]].

A **commutative** (unital) ring is a [[commutative monoid]] object in $(Ab, \otimes)$.

=--

+-- {: .num_remark}
###### Remark

In usual ring theory people often talk about **[[nonunital rings]]**  as well: multiplicative [[semigroups]] with additive [[abelian group]] structure where the multiplication is distributive toward addition; these are semigroup objects in $Ab$.  As in the unital case, if the semigroup is abelian then the ring is said to be **commutative nonunital**.  Note the adjective 'nonunital' is an example of the [[red herring principle]].

=-- 

+-- {: .num_remark} 
###### Remark 
If one removes the assumption that the additive group is abelian but retains the remaining ring axioms, the result is still a ring. More generally, this holds for nonunital rings of which multiplicative semigroup is left/right [[weakly reductive semigroup|weakly reductive]].  The result is false for arbitrary nonunital rings: for any group $(G, +, 0)$ we could define multiplication to be the $x\cdot y := 0$, and all the axioms except additive commutativity are trivially satisfied. This occurs because $\cdot$ doesn't distinguish between elements of $G$.
=-- 

## Generalizations

It is possible to [[internalization|internalise]] the notion of ring in at least two different ways.  Either one can replace the [[Set|category of sets]] in the classical definition with another category $C$ -- see [[ring object]] -- , or one can replace [[Ab]] in the fancy definition with another category $M$.


### Internalising the sets

If $C$ is a [[cartesian monoidal category]], then any [[Lawvere theory]] may be internalised in $C$.  The theory of rings is an example, so we can speak of _ring objects_ in $C$.  Then a ring object in $Set$ is simply a ring.  (This works whether your rings are unital or nonunital, commutative or noncommutative, etc.)  However, not every notion of internal ring takes this form.

The theory of rings is a combination of a monoid (or semigroup, if nonunital) and an abelian group structure. Thus, ring objects are algebras over a composed [[operad]] (or [[monad]]) of a monoid operad and an abelian group operad, using a standard [[distributive law]] for that situation in the sense of operads (or monads), which corresponds to the usual distributive law in the classical definition of a ring.

A particular example of this is a ring in a [[topos]]. In a topos one usually alternatively defines a ring object by the standard set-theoretic definition of a ring, and interpret the formulas in the sense of topos-theoretic semantics. 

Picking a ring object $R$ in a [[topos]] $\mathcal{T}$ promotes it into a [[ringed topos]].

In cartesian categories one can also define the structure of an (abelian) group object as the lifting of the correspoding [[representable presheaf]] to a presheaf into (abelian) groups. This kind of lifting of some algebraic structure in sets to algebraic structure in a cartesian category makes sense when some category of algebras creates the limits needed to define them in sets. 


### Internalising the abelian groups

If $M$ is a [[monoidal category]], then we can speak of [[monoid objects]] in $M$.  However, we usually want $M$ to be somewhat like $Ab$ to think of monoid objects in $M$ as internal rings.  For example, if $M$ is the category of abelian [[group objects]] in a cartesian monoidal category $C$, then we recreate the notion of ring object in $C$ from above.  Or, if $M$ is any [[Ab-enriched category]], then it behaves enough like $Ab$ that we may consider its monoid objects as internal rings.  There are yet other examples, however: a [[ring spectrum]] is a monoid object in [[spectra]], even though these are not $Ab$-enriched.

Other examples are [[simplicial ring]]s (as monoids in [[simplicial abelian group]]s) and [[dg-ring]]s, as well as the $A$-rings below.


### Rings over a ring ($A$-rings)

If $K$ is a commutative ring (or especially a [[field]]), then an [[associative algebra]] over $K$ is a monoid object in $K$-[[Mod]]; this is a special case of the previous section.

If $A$ is a noncommutative ring, then a __ring over $A$__, or simply an __$A$-ring__, is a monoid object $R$ in $A$-[[Bimod]] (that is, in $_A Mod _A$).  Every $A$-ring is a ring in the usual sense, in the sense that there is an obvious [[forgetful functor]] to the usual rings. In fact the unit map $A \to R$ is a morphism of rings, and the category of $A$-rings is precisely the [[coslice category]] or under-category $A/Ring$. Thus by category-theoretic rules, one might be led to unconventionally call $A$-rings "rings *under* $A$". Unfortunately, standard name for $A$-rings is "rings *over* $A$", like conventionally calling $k$-algebras the "algebras *over* $K$". 

Unlike for the $k$-algebras, the multiplication $R\times R\to R$ which is the morphism of $A$-[[bimodules]], is not (left) $A$-linear in the *second* factor, but only $A^{op}$-linear (that is, $A$-linear on the right). In other words, the axiom for $K$-algebras $k (r s) = r (k s)$ is not true, for $k\in A$, $r,s\in R$, although $k (r s) = (k r) s$ and $(r s) k = r (s k)$ do hold.  

Both for a discussion for under-over and also for this difference between $K$-algebras and $A$-rings see the Caf&#233;\'s [quick algebra quiz](http://golem.ph.utexas.edu/category/2008/12/a_quick_algebra_quiz.html).

A dual notion to an $A$-ring is an $A$-[[coring]]. 

The structure of an $A\otimes A^{op}$-ring $(R,\mu,\eta)$ is determined by
the structure of $A$ as a ring, together with the two natural homomorphisms
of rings
$s = \eta(-\otimes 1_A):A\to R$ and $t=\eta(1_A\otimes -):A^{op}\to R$ which have commuting images ($s(a)t(a')=t(a')s(a)$, for all $a,a'\in A$). 

### Higher rings

By replacing in the sentence "a ring is a [[monoid]] in [[Ab]]" the [[abelian category]] [[Ab]] with a [[higher category theory|higher category]] of _symmetric monoidal_ higher groupoids, one obtains higher notion of rings.

Of particular interest is the maximal case of symmetric monoidal [[∞-groupoid]]s and, even more generally, that of [[spectrum|spectra]]. A [[monoid in an (∞,1)-category]] in the [[stable (∞,1)-category of spectra]] is an [[A-infinity-ring]] or [[associative ring spectrum]]. The commutative case is a [[commutative monoid in an (∞,1)-category]]: an [[E-infinity ring]] or [[commutative ring spectrum]].


## Examples
 {#Examples}



+-- {: .num_example}
###### Example

* The [[integers]] $\mathbb{Z}$ are a ring under the standard addition and multiplication operation. 

* For each  $n$, this induces a ring structure on the [[cyclic group]] $\mathbb{Z}_n$, given by operations in $\mathbb{Z}$ modulo $n$ ([[cyclic rings]]).

* The [[rational numbers]] $\mathbb{Q}$, [[real numbers]] $\mathbb{R}$ and [[complex numbers]] are rings under their standard operations, in fact these are even _[[fields]]_.

=--

+-- {: .num_example}
###### Example

For $R$ a ring, the [[polynomials]] 

$$
  r_0 + r_1 x + r_2 x^2 + \cdots + r_n x^n
$$

(for arbitrary $n \in\mathbb{N}$) in a [[variable]] $x$ with [[coefficients]] in $R$ form another ring, the _[[polynomial ring]]_ denoted $R[x]$.
This is the [[free construction|free]] $R$-[[associative algebra]] on a single generator $x$.

=--

+-- {: .num_example}
###### Example

For $R$ a ring and $n \in \mathbb{N}$, the set 
$M(n,R)$
of $n \times n$-[[matrices]] with [[coefficients]] in $R$
is a ring under elementwise addition and [[matrix multiplication]].

=--

+-- {: .num_example}
###### Example

For $X$ a [[topological space]], the set of [[continuous functions]]
$C(X,\mathbb{R})$ or $C(X,\mathbb{C})$ with values in the 
[[real numbers]] or [[complex numbers]] is a ring under pointwise 
(points in $X$) addition and multiplication.

=--

+-- {: .num_example}
###### Example

For $X$ a [[topological space]], the [[direct sum]] of its [[ordinary cohomology]] groups $H^\bullet(X,\mathbb{Z})$ forms a ring whose multiplication operation is the [[cup product]]. This is a [[graded object|graded ring]], graded by the cohomological degree.

=--

## Types of rings

* [[integral domain]]

* [[principal ideal domain]]

* [[Noetherian ring]]

* many more...

## Related concepts

* [[monoid]], [[monoid object]]

* [[nonunital ring]], [[nonassociative ring]]

* [[group]], [[group object]]

* **ring**, [[E-∞ ring]]

  * [[associative algebra]]

  * [[commutative ring]], [[commutative algebra]]

  * [[ring object]]
 
    * [[topological ring]]

    * [[normed ring]]

  * [[localization of a ring]]

  * [[filtered ring]], [[associated graded ring]]

  * [[w-contractible ring]]

  * [[core of a ring]]

* [[ideal]]

* [[prime ring]]

* [[spectrum of a commutative ring]]

  * [[affine scheme]], [[affine scheme]], [[spectral topological space]]


* [[ring extension]], 
 
  * [[infinitesimal extension]]

    [[nilradical]], [[reduced ring]], 

* [[Pythagorean ring]]

* [[near-ring]]

* [[module]], [[bimodule]]


## References
 {#References}

### General
 {#ReferencesGeneral}

Lecture notes include

* Arno Fehm, _Ringe_ ([pdf](http://www.math.uni-konstanz.de/~fehm/teaching/algebra/geyer2.pdf)) (in German)

### History
 {#ReferencesHistory}

[[Richard Dedekind]] had introduced the concept today called _ring_ under the name _Ordnung_ (Ger: order, as in [taxonomic order](http://en.wikipedia.org/wiki/Order_%28biology%29)). The word _Zahlring_ (Ger: number ring/ring of numbers) for this was introduced in section 9.31 of

* [[David Hilbert]], _Die Theorie der algebraischen Zahlk&#246;rper_, Jahresbericht der  Deutschen Mathematiker-Vereinigung 4 (1879)

There, the word ring just appears with a footnote mentioning Dedekind's use of the word "Ordnung", no further motivation is given. So probably Hilbert meant to use "ring" as in "collection of things holding together", not in the sense of circles or loops (as one might guess from the rings of [[cyclic groups]] $\mathbb{Z}_n$).

The first abstract axiomatic description of rings is in 

* Adolf Fraenkel, Journal f&#252;r die reine und angewandte Mathematik **145** (1914)

which however contains some additional axioms not used anymore. The set of axioms in its modern form appears first in 

* [[Emmy Noether]], _Ideal Theory in Rings_, Mathematische Annalen **83** (1921)

For historical accounts see

* I. Kleiner, _From numbers to rings: the early history of ring theory_, Elemente der Mathematik 53 (1998) 18-35. ([web](http://dx.doi.org/10.5169/seals-3627))

* _The development of ring theory_ ([pdf](http://www-history.mcs.st-and.ac.uk/HistTopics/Ring_theory.html))
[[!redirects rings]]

[[!redirects unital ring]]
[[!redirects unital rings]]
[[!redirects ring with unit]]
[[!redirects rings with unit]]
[[!redirects rings with units]]
[[!redirects ring with identity]]
[[!redirects rings with identity]]
[[!redirects rings with identities]]

[[!redirects associative ring]]
[[!redirects associative rings]]

[[!redirects associative unital ring]]
[[!redirects associative unital rings]]

[[!redirects noncommutative ring]]
[[!redirects noncommutative rings]]

[[!redirects non-commutative ring]]
[[!redirects non-commutative rings]]


[[!redirects commutative ring]]
[[!redirects commutative rings]]

[[!redirects commutative unital ring]]
[[!redirects commutative unital rings]]

[[!redirects ring unit]]
[[!redirects ring units]]

