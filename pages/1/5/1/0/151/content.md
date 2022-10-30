
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--

# Duality
* table of contents
{: toc}

## Idea

Instances of "dualities" relating two different, maybe opposing, but to some extent equivalent concepts or phenomena are ubiquitous in [[mathematics]] (and in [[mathematical physics]], see at _[[dualities in physics]]_). 

In terms of general abstract concepts in [[category theory]] instances of dualities might be (and have been) organized as follows:

1. **involution** -- any [[automorphism]] which is an [[involution]], hence which squares to the [[identity]] may be though of as exhibiting two dual perspectives on the objects that it acts on;

   * **abstract duality** --  the operation of sending a [[category]] to its [[opposite category]] is such an involution on [[Cat]] itself (and in fact this is the only non-trivial automorphism of [[Cat]], see [here](%28infinity%2Cn%29Cat#automorphisms)). This has been called _abstract duality_. While the construction is a priori tautologous, any given [[opposite category]] often is equivalent to a [[category]] known by other means, which makes abstract duality interesting.

   * **concrete duality** -- given a [[closed category]] $\mathcal{C}$ and any [[object]] $D$ of it, then the operation $[-,D] : \mathcal{C} \to \mathcal{C}^{op}$ obtained by forming the [[internal hom]] into $D$ sends each object to something like a $D$-dual object. This is particularly so if $D$ is indeed a [[dualizing object in a closed category]] in that applying this operation twice yields an [[equivalence of categories]] $[[-,D],D] : \mathcal{C} \stackrel{\simeq}{\to} \mathcal{C}$ (so that $[-,D]$ is a (contravariant) [[involution]] on $\mathcal{C}$). If $\mathcal{C}$ is in addition a [[closed monoidal category]] then under some conditions on $D$ (but not in general) this kind of concrete dualization coincides with the concept of forming [[dual objects]] in [[monoidal categories]].

   From ([Lawvere-Rosebrugh, chapter 7](#LawvereRosebrugh)):

   > Not every statement will be taken into its formal dual by the process of dualizing with respect to $V$, and indeed a large part of the study of mathematics

   >>space vs. quantity

   > and of logic

   >>theory vs. example

   >may be considered as the detailed study of the extent to which formal duality and concrete duality into a favorite $V$ correspond or fail to correspond. (p. 122)


1. **adjunction** -- another categorical concept of duality is that of [[adjunction]], as in pairs of [[adjoint functors]]. Via the many incarnations of [[universal constructions]] in [[category theory]] this accounts for all dualities that arise as instances as the dual pairs 

   * [[limit]] and [[colimit]]

   * left and right [[Kan extension]]

   * [[end]] and [[coend]]

   * [[dependent sum]] and [[dependent product]]

   * [[existential quantification]] and [[universal quantification]]

   (Given that the saying has it that "Everything in mathematics is a Kan extension", this goes some way in explaining the ubiquity of duality in mathematics.)

   When the adjoint functors are [[monads]] and hence [[modalities]], then adjointness between them has been argued to specifically express the concept of [[duality of opposites]].

   Adjunctions and specifically [[dual adjunctions]] ("[[Galois connections]]") may be thought of as a generalized version of the above abstract duality: every [[dual adjunction]] induces a _maximal dual equivalence_ between [[subcategories]].



## Examples

* [[opposite category]]

* [[dual object]], [[dualizing object]], [[dualizing object in a closed category]]

* [[dual space]], [[dual vector space]]
* the duality between [[space and quantity]]
* [[Poincaré duality]] for finite dimensional (oriented) closed manifolds

* [[Spanier-Whitehead duality]], [[Brown-Comenetz duality]], [[Anderson duality]]

* [[Pontryagin duality]] for commutative ([[Hausdorff space|Hausdorff]]) [[topological group|topological groups]]
* [[Cartier duality]] of a finite flat commutative [[group scheme]]
* [[Serre duality]] on nonsingular projective algebraic varieties which has as a special case the statement of the [[Riemann-Roch theorem]]
* [[Grothendieck duality]], [[coherent duality]] for [[coherentsheave|coherent sheaves]]
* [[Verdier duality]] for abelian categories of sheaves; e.g. for a category of sheaves of abelian groups.
* [[Artin-Verdier duality]] generalizing [[Tate duality]] for constructible sheaves over the spectrum of a ring of [[algebraic number|algebraic numbers]]
* [[Koszul duality]]
* [[Stone duality]]
* [[syntax - semantics duality]]
* [[Eckmann-Hilton duality]]

* [[Tannaka duality]]






## Dualizing objects

Of particular interest are concrete dualities between [[concrete categories]] $C, D$, i.e. categories equipped with faithful functors
$$ f : C \to Set$, $\hat f : D \to Set $$
to [[Set]], which are represented by objects $a \in C$, $\hat a \in D$ with the same underlying set $f(a) = \hat f(\hat a)$. Such objects are known as [[dualizing objects]]. 


## Related concepts

* [[de Morgan duality]]

* [[unity of opposites]]

* [[duality in physics]]



## References

* {#LawvereRosebrugh}[[Lawvere]] and [[Rosebrugh]], chaper 7 of _Sets for Mathematics_
([web](http://www.mta.ca/~rrosebru/setsformath/))

* H.-E. Porst, W. Tholen, _Concrete Dualities_ in _Category Theory at Work_, Herrlich, Porst (eds.) [pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf)

* [[David Corfield]]; _[More on duality](http://golem.ph.utexas.edu/category/2007/01/more_on_duality.html)_ (blog)

* wikipedia [duality (mathematics)](http://en.wikipedia.org/wiki/Duality_%28mathematics%29)
* MathOverflow: [the-concept-of-duality](http://mathoverflow.net/questions/73711/the-concept-of-duality)

Discussion of duality specifically in [[homological algebra]] and [[stable homotopy theory]] with emphasis on the concept of [[dualizing object in a closed category]] (and the induced [[Umkehr maps]] etc.) is in

* [[William Dwyer]], [[John Greenlees]], S. Iyengar, _Duality in algebra and topology_, [Hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Dwyer-Greenlees-Iyengar/duality)

    
[[!redirects duality]]
[[!redirects dualities]]

[[!redirects dualization]]