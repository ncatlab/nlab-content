
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A Hopf algebroid is an associative [[bialgebroid]] with an [[antipode]]. 

A _Hopf algebroid_ is a (possibly [[noncommutative geometry|noncommutative]]) generalization of a structure which is dual to a [[groupoid]] (equipped with [[atlas]]) in the sense of [[Isbell duality|space-algebra duality]]. This is the concept that generalizes [[Hopf algebras]] with their relation to [[groups]] from groups to groupoids.

Specifically _[[commutative Hopf algebroids]]_ are the [[internal groupoids]] in the [[opposite category]] of [[CRing]]. These arise notably in [[stable homotopy theory]] as generalized [[dual Steenrod algebras]] for [[generalized cohomology]].

More generally there are _[[Hopf algebroids over a commutative base]]_, examples of which are [[convolution algebras]] of [[Lie groupoids]].


## Definition (under construction)

In the general case we should distinguish left and right bialgebroids, see [[bialgebroid]]. 

In one of the versions, a general Hopf algebroid 
is defined as a pair of a left algebroid and right algebroid together with a linear map from left to right bialgebroid taking the role of an antipode
(...).

### Commutative Hopf algebroids

Given an  [[internal groupoid]] in the [[category]] $Aff_k = Alg_k^{op}$ of affine algebraic $k$-[[schemes]], where $k$ is a [[field]], the $k$-algebras of [[global sections]] over the scheme of objects and the scheme of morphisms have an additional structure of a **[[commutative Hopf algebroid]]**. In fact this is an [[dual equivalence|antiequivalence of categories]]. 

These [[commutative Hopf algebroids]] play a key role in [[stable homotopy theory]]/[[brave new algebra]], as they arise as the [[dual Steenrod algebras]] for certain classes of [[generalized cohomology theories]] $E$  and as such govern the $E$-[[Adams spectral sequence]].

### Noncommutative Hopf algebroids 

There are several generalizations to the noncommutative case. A difficult part is to work over the noncommutative base (i.e., the object of objects is noncommutative). The definition of a [[bialgebroid]] is not that difficult and there is even a very old definition due Takeuchi. To add an antipode is nontrivial. A definition of Lu from mid 1990s is rather nonselfdual unlike the case of [[Hopf algebras]]. So a better solution is to abandon the idea of an antipode and have some replacement for it. There are two approaches, one due to Day and Street, and another due [[Gabi Böhm]], using pairs of a left and right bialgebroid. Gabi later showed that the two definitions are in fact equivalent.



## Examples

### Scalar extension Hopf algebroids

Given a [[Hopf algebra]] $B$ and a braided-commutative algebra $A$ in the category of Yetter-Drinfeld modules over $B$, the smash product algebra $B\sharp A$ is the total algebra of a Hopf algebroid over $A$. This is a noncommutative generalization (of formal dual of) an [[action groupoid]].


## References

The commutative version is classical, and there is an extensive literature, see [[Hopf algebroids over a commutative base]].  

Over a noncommutative base ring, there is a nonsymmetric version due J-H. Lu and a similar version is later studied by [[Ping Xu]]

*  Jiang-Hua Lu, _Hopf algebroids and quantum groupoids_, Int. J. Math. __7__, 1 (1996) pp. 47-70, [q-alg/9505024](http://arxiv.org/abs/q-alg/9505024), [MR95e:16037](http://www.ams.org/mathscinet-getitem?mr=95e:16037), [doi](http://dx.doi.org/10.1142/S0129167X96000050); _On the Drinfeld double and the Heisenberg double of a Hopf algebra_, Duke Math. J. __7__:3 (1994) 763-776, [MR1277953](http://www.ams.org/mathscinet-getitem?mr=1277953), [doi](http://dx.doi.org/10.1215/S0012-7094-94-07428-0)
* [[Ping Xu]], _Quantum groupoids_, Commun. Math. Phys., 216:539581, 2001, [q-alg/9905192](http://arxiv.org/abs/math/9905192), [doi](http://dx.doi.org/10.1007/s002200000334); _Quantum groupoids and deformation quantization_, [q-alg/9708020](http://arxiv.org/abs/q-alg/9708020), _Quantum groupoids associated to universal dynamical R-matrice_, [q-alg/9811172](http://arxiv.org/abs/math/9811172)
* blog discussion at [Theoretical Atlas](http://theoreticalatlas.wordpress.com/2009/03/18/a-note-on-quantum-groupoids)

The modern concept over the noncommutative base has been discovered by several different people in several different formalisms.  Some of the differences are merely cosmetic, but there are at least two main concepts, depending on the underlying concept of 'bialgebroid'.

Day and Street have a concept of Hopf algebroid here:
 
* [[B. Day]], [[R. Street]], _Monoidal bicategories and Hopf algebroids_, Advances in Mathematics __129__, 1 (1997) 99--157 

In this they start by taking an [[algebroid]] to be an "algebra with several objects" in the sense of a $k$-linear category $A$: that is, a $V$-[[enriched category]] with $V = Vect_k$.   The 2-category $V Cat$ of $k$-linear categories, functors and natural transformations is monoidal (where the tensor product of $V$-categories is defined by cartesian product on object sets and tensor product on hom-spaces).  So, they define a  **bialgebroid** to be a comonoid in $V Cat$.  Because the tensor product is cartesian product on object sets, the comultiplication in such a bialgebroid is forced to be the diagonal on objects.   Thus, their notion of bialgebroid amounts to a $k$-linear category $A$ equipped with linear maps

$$ A(a,b) \to A(a,b) \otimes A(a,b)$$

satisfying coassociativity, a version of the usual bialgebra axiom, and so on.   On page 142 of the above reference they define an **antipode** on a bialgebroid $A$ to be a $k$-linear functor $S: A \to A^{op}$ together with a natural isomorphism 

$$ A(b,c) \otimes A(a,S b) \cong A(b,c) \otimes A(a,c) $$

A **Hopf algebroid** is then roughly a bialgebroid with an antipode.  With this definition, a Hopf algebra gives a one-object Hopf algebroid.

A different and more widely used concept was developed independently in these two papers, which appeared on the arXiv within a couple of days of each other:

* [[G. Böhm]], _An alternative notion of Hopf algebroid_; in "Hopf algebras in noncommutative geometry and physics",  31--53, Lecture Notes in Pure and Appl. Math. __239__, Dekker, New York, 2005; <a href="http://arxiv.org/abs/math.QA/0301169"> math.QA/0301169 </a>

* [[R. Street]] and [[B. Day]], Quantum categories, star autonomy, and quantum groupoids, in "Galois Theory, Hopf Algebras, and Semiabelian Categories", Fields Institute Communications 43 (American Math. Soc. 2004) 187-226; <a href = "http://arxiv.org/abs/math/0301209">arXiv:0301209</a>

and also described in:

* [[G. Böhm]], _Hopf algebroids_, (a chapter of) Handbook of algebra, [arxiv:math.RA/0805.3806](http://arxiv.org/abs/0805.3806)
* G. B&#246;hm, [[K. Szlachányi]], _Hopf algebroids with bijective antipodes: axioms, integrals and duals_, Comm. Algebra __32__ (11) (2004) 4433 - 4464 [math.QA/0305136](http://arxiv.org/abs/math.QA/0305136)
* [[T. Brzeziński]], G. Militaru, _Bialgebroids, $\times_A$-bialgebras and duality_,  J. Algebra __251__: 279-294, 2002
[math.QA/0012164](http://arxiv.org/abs/math.QA/0012164)
* D. Chikhladze, Category of quantum categories, Theory and Applications of Categories __25__ (2011) 1 - 37.  ([pdf](http://www.tac.mta.ca/tac/volumes/25/1/25-01.pdf))

A class of examples of such Hopf algebroids internally in a monoidal category of cocomplete cofiltered vector spaces is in

* S. Meljanac, Z. &#352;koda, _Lie algebra type noncommutative phase spaces are Hopf algebroids_, [arxiv/1409.8188](http://arxiv.org/abs/1409.8188)

This starts with a different concept of [[bialgebroid]], which is discussed here on the nLab.  Namely: any $k$-algebra $R$ gives a pseudomonoid $R^e = R^{op} \otimes R$ in the bicategory $Mod_k$ of k-algebras, bimodules, and bimodule homomorphisms, and a **bialgebroid** is then an opmonoidal monad $A$ on $R^e$.   When the fusion (or Galois) operator for this opmonoidal monad is invertible, we say that $A$ is a **Hopf algebroid**.  In G. B&#246;hm's work this definition is stated in a less compressed, more down-to-earth way.


category: algebra
[[!redirects Hopf algebroids]]