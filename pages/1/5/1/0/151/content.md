
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

Instances of "dualities" relating two different, maybe opposing, but to some extent equivalent concepts or phenomena are ubiquitous in [[mathematics]] (and in [[mathematical physics]], see at _[[dualities in physics]]_). The term "duality" is widespread and doesn't have a single crisp meaning, but a rough guiding intuition is of pairs of concepts that are mirror images of one another. 

## General notions 

In terms of general abstract concepts in [[logic]] and [[category theory]], instances of dualities might be (and have been) organized as follows. 

### Abstract/formal/axiomatic duality

Instances here include projective duality, duality in lattice theory, and duality in category theory. In each case, one has a [[theory]] whose [[signature]] admits a nontrivial [[involution]], in such a way that "dualizing" or applying the involution to any axiom of the theory (but otherwise preserving the logical structure of formulae) results in another theorem of the theory. For example, for the theory of projective planes, the involution swaps points and lines, meets and joins, etc., and for each theorem there is a dual theorem. Similarly, in [[category]] theory, the involution swaps the domain and codomain and order of composition, etc., and for any theorem of formal category theory, the corresponding dual statement is also a theorem (because the set of axioms of category theory are closed under taking formal duals). 

Such formal duality can also be expressed at the level of [[models]] of the theory $T$: for each model $M$ there is a "dual" or "opposite" model $M^{op}$ obtained by re-interpreting each formal sort/function/relation of the theory as the dual sort/function/relation. This further induces an involution $Mod(T) \to Mod(T)$ on the category of models. For example, in the case of category theory, this operation $C \mapsto C^{op}$, mapping a category $C$ to its [[opposite category]], gives an involution $(-)^{op}: Cat \to Cat$ on the category [[Cat]] of (small) categories, viewing $Cat$ here as a 1-category. In fact this is the only non-trivial automorphism of [[Cat]], see [here](%28infinity%2Cn%29Cat#automorphisms)). 

This involution $(-)^{op}: Cat \to Cat$ is also known as _abstract duality_. While the construction is a priori tautologous, any given [[opposite category]] often is equivalent to a [[category]] known by other means, which makes abstract duality interesting (particularly so in cases of concrete duality, which we discuss next). 

### Concrete dualities 

Instances here include linear duality, Stone duality, Pontryagin duality, and projective inversions with respect to a conic hypersurface. In each such case there is some [[contravariant functor|contravariant]] process of "homming into" a suitable structure $V$ called a [[dualizing object]], which in the classical cases of what we will call "perfect duality", induces an equivalence of categories $C^{op} \stackrel{\sim}{\to} D$ where typically $C$ is the category of models of one type of concrete structure, and the equivalence maps the formal categorical dual $C^{op}$ to a category of models $D$ consisting of "dual" concrete structures. 

In other cases one might not obtain an equivalence or perfect duality, but in any case a contravariant [[adjoint pair]] of functors $S: C \to D$, $T: D \to C$ between categories which can be termed a duality of sorts, in that concepts developed in $C$ are mapped to dual concepts in $D$ and vice-versa. Quoting ([Lawvere-Rosebrugh, chapter 7](#LawvereRosebrugh)):

> Not every statement will be taken into its formal dual by the process of dualizing with respect to $V$, and indeed a large part of the study of mathematics

>>space vs. quantity

> and of logic

>>theory vs. example

>may be considered as the detailed study of the extent to which formal duality and concrete duality into a favorite $V$ correspond or fail to correspond. (p. 122)

Some examples follow. 

* In linear duality, say for vector spaces over a field $k$, the dual of a space $W$ is $W^\ast = \hom(W, k)$, the hom of $k$-linear maps into $k$. This induces a contravariant functor $(-)^\ast: Vect_k \to Vect_k$ that is adjoint to itself, in that there is a double-dual embedding $\delta_W: W \to W^{\ast\ast}$ such that 
$$1_{W^\ast} = (W^\ast \stackrel{\delta_{W^\ast}}{\to} W^{\ast\ast\ast} \stackrel{(\delta_W)^\ast}{\to} W^\ast).$$ 
This becomes a perfect duality if we restrict to finite-dimensional vector spaces, i.e., the contravariant functor $(-)^\ast: Vect_{fd} \to Vect_{fd}$ is adjoint-equivalent to itself (i.e., the covariant functor $((-)^\ast)^{op}: Vect_{fd} \to Vect_{fd}^{op}$ is left adjoint to $(-)^\ast: Vect_{fd}^{op} \to Vect_{fd}$ and the adjunction is an [[adjoint equivalence]]). 

* More generally, given a (usually [[symmetric monoidal category|symmetric]]) [[monoidal closed category]]) $\mathcal{C}$, any object $D$ induces an operation $[-,D] : \mathcal{C} \to \mathcal{C}^{op}$ obtained by forming the [[internal hom]] into $D$, sending each object to what may be termed its $D$-dual object. There is a corresponding double-dual embedding $\delta_C: C \to [[C, D], D]$ obtained as the composite 
$$C \to [[C, D], C \otimes [C, D]] \to [[C, D], [C, D] \otimes C] \to [[C, D], D]$$ 
where the first arrow uses the unit of an adjunction $(- \otimes B) \dashv [B, -]$ where $B = [C, D]$, the second uses a symmetry isomorphism $C \otimes B \cong B \otimes C$, and the third uses the counit of an adjunction $(- \otimes C) \dashv [C, -]$, aka an evaluation map. It may be shown that the contravariant functor $(-)^\ast \coloneqq [-, D]: \mathcal{C} \to \mathcal{C}$ is again dual to itself, exactly as in the case of linear duality above, where we have a triangular equation 
$$1_{C^\ast} = (\delta_C)^\ast \circ \delta_{C^\ast}$$ 
for an adjunction $[-, D]^{op} \dashv [-, D]$. Under certain circumstances, we have perfect duality, i.e., double dualization $[[-, D], D]: \mathcal{C} \to \mathcal{C}$ is an equivalence; see [[dualizing object in a closed category]] and [[star-autonomous category]]. Particular special cases of this may obtain when $D = I$, the monoidal unit, or even more particularly when every object has a [[dual object]] in the sense of [[monoidal categories]]; see also [[compact closed category]]. On the other hand, there is also a mild generalization of this type of example where we deal with a [[biclosed monoidal category]]; here the double dualization will involve both the left and right internal hom. 

* More general still is a concrete duality induced by a [[dualizing object]]. In this case one is given a pair of categories together with underlying-set functors 
$$U: \mathcal{C} \to Set, \qquad V: \mathcal{D} \to Set$$ 
(and often when one says "concrete", one intends that these functors be faithful as well, so that $\mathcal{C}, \mathcal{D}$ can be viewed as "sets with structure"; see [[stuff, structure, property]]). The concrete duality consists of a pair of objects $C \in \mathcal{C}, D \in \mathcal{D}$ together with an isomorphism $\omega: U C \cong V D$, such that the contravariant homs $\hom(-, C): C^{op} \to Set$ and $\hom(-, D): D^{op} \to Set$ lift to a contravariant adjunction between $C$ and $D$, in the sense described [here](/nlab/show/dualizing+object#ambi). Frequently in practice, such concrete dualities are "naturally represented" in the sense described [here](/nlab/show/dualizing+object#natural), involving certain lifts adapted from the theory of [[topological concrete categories]]. 

Again, in all of these examples, one can consider the further condition of "perfect duality" where the units and counits of the (lifted) adjunctions are isomorphisms.  

### Adjunctions 

Perhaps the loosest general notion of "duality" is that of [[adjunction]], as in pairs of [[adjoint functors]]. Here one may omit any concretizations via functors to $Set$, or even for that matter any explicit mention of opposite categories, and just work at the level of abstract categories themselves. 

Nevertheless, many adjunctions come packaged in "dual pairs". A famous slogan from [[Categories for the Working Mathematician]] is that "all concepts are Kan extensions", and in that light the dual pairs are instances of the general dual pair "(right Kan extension, left Kan extension)" which are formal duals in the axiomatic sense described earlier. Via the many incarnations of [[universal constructions]] in [[category theory]], we have for example 

   * [[limit]] and [[colimit]]

   * [[end]] and [[coend]]

   * [[dependent sum]] and [[dependent product]]

   * [[existential quantification]] and [[universal quantification]]

When the adjoint functors are [[monads]] and hence [[modalities]], then adjointness between them has been argued to specifically express the concept of [[duality of opposites]].

Again, adjunctions and specifically [[dual adjunctions]] ("[[Galois connections]]") may be thought of as generalized dualities, more general than "perfect duality" which involves equivalences between categories ("Galois correspondences"). However, it should also be noted that any such adjunction (or [[dual adjunction]]) restricts to a _maximal (dual) equivalence_ between [[subcategories]], by considering objects where the appropriate units and counits are isomorphisms. This generalizes the manner by which any Galois connection induces a Galois correspondence (where in this special case, one need only take the images of the poset maps which constitute the connection). 



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

* {#LawvereRosebrugh} [[William Lawvere]], [[Bob Rosebrugh]], chaper 7 of _Sets for Mathematics_ ([web](http://www.mta.ca/~rrosebru/setsformath/))

* H.-E. Porst, W. Tholen, _Concrete Dualities_ in _Category Theory at Work_, Herrlich, Porst (eds.) [pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf)

* [[David Corfield]]; _[More on duality](http://golem.ph.utexas.edu/category/2007/01/more_on_duality.html)_ (blog)

* wikipedia [duality (mathematics)](http://en.wikipedia.org/wiki/Duality_%28mathematics%29)
* MathOverflow: [the-concept-of-duality](http://mathoverflow.net/questions/73711/the-concept-of-duality)

Discussion of duality specifically in [[homological algebra]] and [[stable homotopy theory]] with emphasis on the concept of [[dualizing object in a closed category]] (and the induced [[Umkehr maps]] etc.) is in

* [[William Dwyer]], [[John Greenlees]], S. Iyengar, _Duality in algebra and topology_, [Hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Dwyer-Greenlees-Iyengar/duality)

    
[[!redirects duality]]
[[!redirects dualities]]

[[!redirects dualization]]

[[!redirects formal duality]]
[[!redirects formal dualities]]

[[!redirects abstract duality]]
[[!redirects abstract dualities]]
