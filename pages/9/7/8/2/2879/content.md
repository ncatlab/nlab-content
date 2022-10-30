
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _Hopf algebroid_ is a (possibly [[noncommutative geometry|noncommutative]]) generalization of a structure which is dual to a [[groupoid]] (equipped with [[atlas]]) in the sense of [[Isbell duality|space-algebra duality]]. This is the concept that generalizes [[Hopf algebras]] with their relation to [[groups]] from groups to groupoids.

Just as for [[groups]] and their [[Hopf algebras]], there are _two_ ways to assign a Hopf algebroid to a [[groupoid]] $\mathcal{G}_\bullet$:

1. **commutative but non-co-commutative** Form the [[commutative algebra|commutative]] [[algebras of functions]] $C(\mathcal{G}_1)$ and $C(\mathcal{G}_0)$ and regard the operation induced by the partially defined [[composition]] in $\mathcal{G}_\bullet$ as an in general non-co-commutative [[coalgebra]] structure on $C(\mathcal{G}_1)$ over $C(\mathcal{G_0})$;

1. **non-commutative but co-commutative** Form the in general non-commutative [[groupoid convolution algebra]] $C_{conv}(\mathcal{G})$ and regard it as a co-commutative [[coalgebra]] over $C(\mathcal{G}_0)$.

Both of these resulting bialgebra structures can then be further generalized to allow them to be both non-commutative as well as non-co-commutative. 

(...)

 
## Definition


(...)

### Commutative Hopf algebroids

Given an internal [[groupoid]] in the category $Aff_k$ of affine algebraic $k$-[[schemes]], where $k$ is a field, the $k$-algebras of [[global sections]] over the scheme of objects and the scheme of morphisms have an additional structure of a commutative Hopf algebroid. In fact this is an [[dual equivalence|antiequivalence of categories]]. Commutative Hopf algebroids are useful also in a version in [[brave new algebra]] (the work of John Rognes). 

### Noncommutative Hopf algebroids 

There are several generalizations to the noncommutative case. A difficult part is to work over the noncommutative base (i.e., the object of objects is noncommutative). The definition of a [[bialgebroid]] is not that difficult and there is even a very old definition due Takeuchi. To add an antipode is nontrivial. A definition of Lu from mid 1990s is rather nonselfdual unlike the case of [[Hopf algebras]]. So a better solution is to abandon the idea of an antipode and have some replacement for it. There are two approaches, one via [[monoidal bicategory|monoidal bicategories]] due to Day and Street, and another due Gabi B&#246;hm, using pairs of a left and right bialgebroid. Gabi has later shown that the two definitions are in fact equivalent.

## Examples

### Higher groupoid convolution algebras and n-vector spaces/n-modules

> under construction

We discuss here a natural generalization of the notion of [[groupoid convolution algebras]] to [[higher algebra|higher algebras]] for [[n-groupoid|higher groupoids]]. 

There may be several sensible such generalizations. The one discussed now follows the principle of iterated [[internalization]] and naturally matches to the concept of [[n-modules]] ([[n-vector spaces]]) as they appear in [[extended prequantum field theory]].

In order to disentangle conceptual from technical aspects, we first discuss [[discrete ∞-groupoid|geometrically discrete higher groupoids]]. The results of this discussion then in particular help to suggest what the right definition of "higher Lie groupoid" in the ontext of higher convolution algebras should be in the first place.

The consideration are based on the following

+-- {: .num_remark}
###### Remark

By the discussion at _[[2-module]]_ we may think of the [[2-category]] $k Alg_b$ of $k$-[[associative algebras]] and [[bimodules]] between them as a model for the 2-category [[2Mod]] of $k$-[[2-modules]] that admit a 2-[[basis]] ([[2-vector spaces]]). Hence the groupoid convolution algebra constructiuon is a 2-functor 

$$
  C \;\colon\; Grpd \to 2 Mod
  \,.
$$


There is then the following systematic refinement of this to higher groupoids and higher algebra: by the discussion at _[[n-module]]_, 3-modules are algebra objects in [[2Mod]] and maps between them are [[bimodule]] objects in there. An algebra object in  $k Alg_b$ is equivalently a [[sesquialgebra]], an algebra equipped with a second algebra structure up to coherent homotopy, that is exhibited by structure bimodules. 

Special cases of this are [[bialgebras]], for which these structure bimodules come from actual algebra homomorphisms. Examples of these in turn are [[Hopf algebras]]. These we naturally re-discover as special higher groupoid convolution higher algebras in example \ref{DoubleGroupoid2AlgebraOfDeloopingOfFiniteGroup} below. 

=--


This iterated internalization on the codomain of the groupoid convolution algebra functor has a natural analog on its domain: a 2-groupoid we may present by a [[double groupoid]], namely a [[groupoid object in an (∞,1)-category]] in [[Grpd]] which is 3-[[coskeleton|coskeletal]] as a [[simplicial object]] in [[Grpd]].

+-- {: .num_remark}
###### Remark

Given a [[groupoid object in an (∞,1)-category|groupoid object]] $\mathcal{G}_\bullet$ in the [[(2,1)-topos]] [[Grpd]] hence a [[double groupoid]], applying the groupoid convolution algebra $(2,1)$-functor $C$ to the corresponding [[simplicial object]] $\mathcal{G}_\bullet \in Grpd^{\Delta^{op}}$ yields:

* groupoid convolution algebras $C(\mathcal{G}_0)$ and $C(\mathcal{G}_1)$,

* a $C(\mathcal{G}_1) \otimes_{C(\mathcal{G}_{0,1})} C(\mathcal{G}_1)-C(\mathcal{G}_{0})$-bimodule, assigned to the [[composition]] functor $\partial_1 \colon \mathcal{G}_1 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1 \to \mathcal{G}_1$.

Under the 2-functoriality of $C$, the [[Segal conditions]] satisfied by $\mathcal{G}_\bullet$ make this bimodule exhibi a [[sesquialgebra]] structure over $C(\mathcal{G}_{0,1})$.

This sesquialgebra we call the the **double groupoid convolution 2-algebra** of $\mathcal{G}_\bullet$.

(Here we make invariant sense of the [[tensor product]] by evaluating on a [[Reedy model structure|Reedy fibrant]] representative.)

=--

+-- {: .num_example #DoubleGroupoid2AlgebraOfDeloopingOfFiniteGroup}
###### Example

Let $G$ be a [[finite group]]. Write $\mathbf{B}G$ for its [[delooping]] [[groupoid]] (the connected groupoid with $\pi_1 = G$). There are two natural ways to present $\mathbf{B}G$ as a [[double groupoid]]:

1. $\underset{\longrightarrow}{\lim}(\cdots \mathbf{B}G \stackrel{\overset{id}{\to}}{\underset{id}{\to}} \mathbf{B}G) \simeq \mathbf{B}G$;

1. $\underset{\longrightarrow}{\lim}(\cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} *) \simeq \mathbf{B}G$.

Applying the [[groupoid convolution algebra]] functor to the first presentation yields the groupoid convolution algebra $C(\mathbf{B}G)$ equipped with a trivial multiplication bimodule, hence just the group convolution algebra $C(\mathbf{B}G) \simeq C_{conv}(G)$.

Applying however the [[groupoid convolution algebra]] functor to the second presentation yields the _commutative_ algebra of functions $C(G)$ equipped with the multiplication bimodule which is $C(G \times G)$ regarded as a $(C(G\times G), C(G))$-bimdodule, where the right action is induced by pullback along the group product map $G \times G \to G$.

This bimodule is in the image of the functor $Alg \to Alg_b$ that sends algebra homomorphisms to their induced bimodules, by sending $f \colon A \to B$ to $A$ regarded as an $(A,B)$-bimodule with the canonical left action on itself and the right action induced by $f$. Namely this bimdoule correspondonds to the map

$$
  \Delta \colon C(G) \to C(G \times G) \simeq C(G) \otimes C(G)
$$

given on $\phi \in C(G)$ and $g_1, g_2 \in G$ by

$$
  \Delta \phi \colon (g_1, g_2) \mapsto \phi
  \,.
$$

In summary this means that (for $G$ a finite group)

1. if we regard $\mathbf{B}G$ as presented as a  double groupoid constant on $\mathbf{B}G$, then the corresponding groupoid convolution [[sesquialgebra]] (basis for a [[n-module|3-module]]) is the convolution algebra of $G$;

1. if instead we regard $\mathbf{B}G$ as presented as the double groupoid which is degreewise constant as a groupoid, then the corresponding groupoid convolution sesquialgebra is the standard ("dual") [[Hopf]] algebra structure on the commutative pointwise product algebra of functions on $G$.

=--




## References

The commutative version is classical, and there is an extensive literature. Some of the recent works on commutative case, related to homotopy theory and stacks are

* [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_, [pdf](http://math.wesleyan.edu/~mhovey/papers/comodule.pdf); _Morita theory of Hopf algebroids_, [pdf](http://math.wesleyan.edu/~mhovey/talks/hopfalgebroids.pdf)

* [[Paul Goerss]], _Quasi-coherent sheaves on the moduli stack of formal groups_, [pdf](http://www.math.northwestern.edu/~pgoerss/papers/modfg.pdf)

* Barry Walker, _Hopf algebroids and stacks_  ([pdf](http://www.math.umn.edu/~tlawson/old/stackstalk.pdf))

For the relation to [[groupoid convolution algebras]] see also at _[groupoid convolution algebra -- References -- Convolution Hopf algebroids](category%20algebra#ReferencesConvolutionHopfAlgebroids)_.

* [[Mark Hovey]], _Morita theory for Hopf algebroids and presheaves of groupoids_ ([arXiv:math/0105137](http://arxiv.org/abs/math/0105137))

The version in [[brave new algebra]]

* A. Baker, A. Jeanneret, _Brave new Hopf algebroids and extensions of $M U$-algebras_, Homology Homotopy Appl. __4__:1 (2002), 163-173, [MR1937961](http://www.ams.org/mathscinet-getitem?mr=1937961), [euclid](http://projecteuclid.org/euclid.hha/1139840059)

One can straightforwardly keep the base commutative while having the total algebra noncommutative, and the image of source and target maps are required to commute mutually. This version is due Maltsiniotis; he also generalized this to [[quasi-Hopf algebra|quasi-Hopf]] version:

* [[Georges Maltsiniotis]], _Groupo&#239;des quantiques_, Comptes R
Rendus Acad. Sci. Paris __314__, pp. 249-252 (1992) [ps](http://people.math.jussieu.fr/~maltsin/ps/GRN-1.PS)
* G. Maltsiniotis, _Quasi-groupo&#239;des quantiques_ (travail en commun avec A. Brugui&#232;res), C.R. Acad. Sci. Paris __319__, pp. 933-936 (1994) [ps](http://people.math.jussieu.fr/~maltsin/ps/N-QSBIG.PS) 

Over a noncommutative base ring, there is a nonsymmetric version due J-H. Lu and a similar version is later studied by [[Ping Xu]]

*  Jiang-Hua Lu, _Hopf algebroids and quantum groupoids_, Int. J. Math. __7__, 1 (1996) pp. 47-70, [q-alg/9505024](http://arxiv.org/abs/q-alg/9505024), [MR95e:16037](http://www.ams.org/mathscinet-getitem?mr=95e:16037), [doi](http://dx.doi.org/10.1142/S0129167X96000050); _On the Drinfeld double and the Heisenberg double of a Hopf algebra_, Duke Math. J. __7__:3 (1994) 763-776, [MR1277953](http://www.ams.org/mathscinet-getitem?mr=1277953), [doi](http://dx.doi.org/10.1215/S0012-7094-94-07428-0)
* [[Ping Xu]], _Quantum groupoids_, Commun. Math. Phys., 216:539581, 2001, [q-alg/9905192](http://arxiv.org/abs/math/9905192), [doi](http://dx.doi.org/10.1007/s002200000334); _Quantum groupoids and deformation quantization_, [q-alg/9708020](http://arxiv.org/abs/q-alg/9708020), _Quantum groupoids associated to universal dynamical R-matrice_, [q-alg/9811172](http://arxiv.org/abs/math/9811172)
* blog discussion at [Theoretical Atlas](http://theoreticalatlas.wordpress.com/2009/03/18/a-note-on-quantum-groupoids)

The modern concept over the noncommutative base is discovered in two formally different formalisms, but the two concepts are equivalent: 
 
* [[B. Day]], [[R. Street]], _Monoidal bicategories and Hopf algebroids_, Advances in Mathematics __129__, 1 (1997) 99--157 

* [[G. Böhm]], _An alternative notion of Hopf algebroid_; in "Hopf algebras in noncommutative geometry and physics",  31--53, Lecture Notes in Pure and Appl. Math. __239__, Dekker, New York, 2005; <a href="http://arxiv.org/abs/math.QA/0301169"> math.QA/0301169 </a>
* [[G. Böhm]], _Hopf algebroids_, (a chapter of) Handbook of algebra, [arxiv:math.RA/0805.3806](http://arxiv.org/abs/0805.3806)
* G. B&#246;hm, [[K. Szlachányi]], _Hopf algebroids with bijective antipodes: axioms, integrals and duals_, Comm. Algebra __32__ (11) (2004) 4433 - 4464 [math.QA/0305136](http://arxiv.org/abs/math.QA/0305136)
* [[T. Brzezi?ski]], G. Militaru, _Bialgebroids, $\times_A$-bialgebras and duality_,  J. Algebra __251__: 279-294, 2002
[math.QA/0012164](http://arxiv.org/abs/math.QA/0012164)
[[!redirects Hopf algebroids]]