[[!redirects local net]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[quantum field theory]] (or [[classical field theory]]) a _causally local net of observables_ is a system (a [[co-presheaf]]) of [[algebras of observables]] assigned to regions of [[spacetime]],  such that this satisfies a few basic properties, such as notably _[[causal locality]]_, saying that observables whose spacetime [[support]] is [[spacelike]]-separated (graded-)commute with each other ([[Poisson bracket|Poisson]]-commute, in the case of classical field theory).

(Beware that the meaning of "net" here is vaguely similar to, but different from, the concept of _[[net]]_ (as in: generalized [[sequences]] of points) as used in [[topology]]. Better terminology might be "causally local system of spacetime-localized observables". But "local net" is traditional and has become standard.)

In the context of [[algebraic quantum field theory]] the structure of the local net of quantum observables is used as the very [[axiom|axiomatization]] of what a [[quantum field theory]] actually is ("[[Haag-Kastler axioms]]"). This may be thought of as a formalization of a spacetime-localized form of the [[Heisenberg picture]] of [[quantum physics]] (or rather the [[interaction picture]] in the case of [[perturbative AQFT]]); as opposed to the formalization of the [[Schrödinger picture]] in [[FQFT]], where instead the [[state]]-propagation is used as the basic axiom.

Traditionally local nets of observables are assumed to take values in [[C*-algebras]], but the basic form of the axioms does not actually refer to [[topology|topological]] structure on the algebras, and makes sense more generally.

In particular in [[perturbative quantum field theory]] made precise via [[causal perturbation theory]], the [[algebras of quantum observables]] are taken to be [[formal power series algebras]] (reflecting the [[infinitesimal]] nature of [[perturbation theory]]) and one _derives_ from [[causal additivity]] of the [[S-matrix]] that the perturbative [[quantum observables]] form a local not of formal power series algebras (see at _[S-matrix -- Causal locality and Quantum observables](S-matrix#CausalLocality)_). Accordingly, this infinitesimal/pertrubative version of [[AQFT]] is called _[[perturbative AQFT]]_.

Other variants may be considered. For [[AQFT on curved spacetimes]] one generalizes from observables associated with regions of [[Minkowski spacetime]] toobsrvables associated with more general [[globally hyperbolic spacetimes]]. Combining this with perturbation theory is then called _[[locally covariant perturbative AQFT]]_.

Moreover, if [[gauge theory]] with nontrivial global [[gauge field]] configurations is to be considered ([[instantons]]) then one may show that one needs to consider some kind of [[homotopy theory|homotopy theoretic]] local nets of _[[homotopical algebras]]_. See at _[[homotopical AQFT]]_.




## Definition

In the literature there is a certain variance and flexibility of what precisely the axioms on a local net of observables are, though the core aspects are always the same: it is a [[copresheaf]] of ([[C-star algebra|C-star]] [[associative algebra|algebra]] s) on pieces of [[spacetime]] such that algebras assigned to [[causal locality|causally disconnected]] regions commute inside the algebra assigned to any joint neighbourhood. 

Historically this was first formulated for [[Minkowski spacetime]] only, where it is known as the [[Haag-Kastler axioms]]. Later it was pointed out ([BrunettiFredenhagen](#BrunettiFredenhagen)) that the axioms easily and usefully generalize to arbitrary [[spacetime]]s. 

We give the modern general formulation first, and then comment on its restriction to special situations.

### Basic general definition

+-- {: .num_defn #CatOfSpacetimeEmbeddings}
###### Definition

Write $LorSp$ for the [[category]] whose

* [[object]]s are [[spacetime]] manifolds; ([[Lorentzian manifold]]s equipped with a time-orientation);

* [[morphism]] are _causal_ [[isometry|isometric]] [[embedding]].

Here we say a morphism $f : X \hookrightarrow Y$ is a **causal embedding** if for every two points $x_1,x_2 \in X$ we have that $f(x_1)$ is in the [[future]] of $f(x_2)$ in $Y$ only if $x_1$ is in the future of $x_2$ in $X$.

=--


Write $Alg$ for a suitable [[category]] of [[associative algebra]]s. Usually this is taken to be the category of [[C-star algebra]]s or that of [[von Neumann algebra]]s. Write

$$
  Alg_{inc} \hookrightarrow Alg
$$

for the [[subcategory]] on the [[monomorphism]]s.

+-- {: .num_defn}
###### Definition

A **causally local net of observables** is a [[functor]]

$$
  \mathcal{A} : LorSp \to Alg_{inc} \to Alg
$$

such that whenever $X_1 \coprod X_2 \hookrightarrow X$ is a causal embedding, def. \ref{CatOfSpacetimeEmbeddings}, we have that $\mathcal{A}(X_1) \subset \mathcal{A}(X)$ commutes with $\mathcal{A}(X_2) \subset \mathcal{A}(X)$.

=--

+-- {: .num_remark}
###### Remark

The [[local quantum field theory|locality]] [[axiom]] encodes the the physical property known as _[[Einstein-causality]]_ or _micro-causality_, which states that physical effects do not propagate faster that the speed of light.

=--

+-- {: .num_remark}
###### Remark

Many _auxiliary_ [[linear operator|operators]] in [[quantum field theory]] do _not_ satisfy causal locality: for instance operators associate to [[current]]s in [[gauge theory]]. The idea is that those operators that actually do qualify as _[[observables]]_ do satisfy the axiom, however, i.e. in particular those that are [[gauge symmetry|gauge invariant]].

=--

### Extra axioms

#### Einstein locality 
 {#EinsteinLocalities}

Commutativity of spacelike separated observables can be argued to capture only part of [[causal locality]]. 

A natural stronger requirement is that [[spacelike]] separated regions of [[spacetime]] are literally [independent quantum subsystems](quantum%20mechanics#Subsystems) of any larger region. By the formalization of _independent subsystem_ in [[quantum mechanics]] this means the following:

+-- {: .num_defn #EinsteinLocality}
###### Definition

A local net $\mathcal{A}$ satisfies **Einstein locality** if for every causal embedding $X_1 \coprod X_2 \to X$ the [subsystems](http://ncatlab.org/nlab/show/quantum%20mechanics#Subsystems) 

$$
  \mathcal{A}(X_1) \hookrightarrow \mathcal{A}(X)
$$

and 

$$
  \mathcal{A}(X_2) \hookrightarrow \mathcal{A}(X)
$$

are _independent_ in that the algebra $\mathcal{A}(X_1) \vee \mathcal{A}(X_2) \in \mathcal{A}(X)$ which they generate is [[isomorphism|isomorphic]] to the [[tensor product]] $\mathcal{A}(X_1) \otimes \mathcal{A}(X_2)$.

=--

This appears as ([BrunettiFredenhagen, 5.3.1, axiom 4](#BrunettiFredenhagen)).

+-- {: .num_remark}
###### Remark

A local net  is Einstein local precisely if it is a [[monoidal functor]]

$$
  \mathcal{A} : (LorSp, \coprod) \to (Alg, \otimes)
  \,.
$$

=--


This appears as ([BrunettiFredenhagen, 5.3.1, theorem 1](#BrunettiFredenhagen)).


+-- {: .num_remark}
###### Remark

Einstein locality implies [[causal locality]], but is stronger.

=--

+-- {: .num_remark}
###### Remark

Other properties implied by Einstein locality are sometimes extracted as separate axioms. For instance the condition that for $X_1 \coprod X_2 \to X$ a causal embedding, we have

$$
  \mathcal{A}(X_1) \cap \mathcal{A}(X_2) = \mathbb{C}
  \,.
$$

=--

#### Strong locality
 {#StrongLocality}

In ([Nuiten 11](#Nuiten11)) the following variant of [[causal locality]] was considered and shown to be equivalent to a [[descent]] condition for the system of [[Bohr toposes]] associated with a local net of observables

+-- {: .num_defn #StrongLocality}
###### Definition

A net of observables is **strongly local** if it is microlocal in that algebras $A_1 = A(O_1)$ and $A_2 = A(O_2)$ associated with  spacelike separated regions commute with each other, and in addition for all commutative subalgebras $C_1 \subset A_1$ and $C_2 \subset A_2$ the algebra $C_1 \vee C_2 \subset A(O_1 \vee O_2)$ satisfies

1. $(C_1 \vee C_2) \cap A_1 = C_1$

1. $(C_1 \vee C_2) \cap A_2 = C_2$.

=--

This is ([Nuiten 11, def. 14](#Nuiten11)).

+-- {: .num_remark }
###### Remark

It is clear that Einstein locality implies strong locality, def. \ref{EinsteinLocality}

$$
   Einstein\;locality \;\;\Rightarrow  \;\; Strong\;locality
  \,.
$$

In fact strong locality is strictly weaker than Einstein locality in that there are strongly locally embedded subalgebras which are not Einstein locally embedded. More discussion of this is in ([Wolters 13, section 6.3.3](#Wolters13)).

=--


#### Time-slice axiom

+-- {: .num_defn}
###### Definition

A local net is said to satisfy the **[[time slice axiom]]** if whenever 

$$
  i : X_1 \to X_2
$$

is a causal embedding of [[globally hyperbolic]] [[spacetime]]s such that $X_1$ contains a [[Cauchy surface]] of $X_2$, then 

$$
  \mathcal{A}(i) : \mathcal{A}(X_1) \stackrel{\simeq}{\to}
   \mathcal{A}(X_2)
$$

is an [[isomorphism]].

=--


#### Duality

See [[dual net of von Neumann algebras]]

#### Positive energy condition

(...)


#### Spectrum condition

(...)


### Special cases and variants

#### Minkowski nets / Vacuum representation

* [[Haag-Kastler vacuum representation]]

#### Conformal nets

The notion of local net in the context of [[conformal field theory]] is a [[conformal net]].

## Examples

see for instance ([B&#228;r-Ginoux 11](#BarGinoux11))


## Related concepts

* [[quantum field theory]]

  * [[local quantum field theory]], [[local prequantum field theory]]

  * [[causal locality]], [[Einstein locality]]

  * [[AQFT]]

    * [[Haag-Kastler axioms]]

    * **local net of observables**

      * [[net of C-star systems]] ([[global gauge group]], [[actions]])

      * [[field net]]

      * [[cohomology of local net of observables]]

      * [[factorization algebra of observables]], [[chiral algebra]], [[topological chiral homology]], [[blob complex]].

  * [[FQFT]]


## References

For more details see the references at [[AQFT]].

### General

The axioms of local nets on general spacetimes were first articulated in

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Backgrounds_ ([arXiv:0901.2063](http://arxiv.org/abs/0901.2063))
 {#BrunettiFredenhagen}

A comprehensive review, with plenty of background information, is in

* {#BaerFredenhagen} [[Christian Bär]], [[Klaus Fredenhagen]], (eds.) _Quantum field theory on curved spacetime_ , Lecture notes in physics, Springer (2009)
  

Discussion of Einstein locality of a net of observables equivalently as a [[descent]] condition on the system of [[Bohr toposes]] induced by the [[algebras of observables]] is in 

* {#Nuiten11} [[Joost Nuiten]], _[[schreiber:bachelor thesis Nuiten|Bohrification of local nets of observables]]_, Proceedings of [QPL 2011](http://qpl.science.ru.nl/), [EPTCS 95, 2012](http://rvg.web.cse.unsw.edu.au/eptcs/content.cgi?QPL2011), pp. 211-218 ([arXiv:1109.1397](http://arxiv.org/abs/1109.1397))  

A review of this with some further discussion is in section 6 of 

* {#Wolters13} Sander Wolters, _Quantum toposophy_, PhD Thesis 2013 ([pdf](http://www.math.ru.nl/~landsman/Wolters.pdf))
  

Discussion of properly co-stacky nets of local observables in [[gauge theory]] is in 

* {#BeniniSchenkelSzabo15} [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], _Homotopy colimits and global observables in Abelian gauge theory_ ([arXiv:1503.08839](http://arxiv.org/abs/1503.08839))

### Examples

Discussion of standard example includes

* {#BarGinoux11} [[Christian Bär]], N. Ginoux, _Classical and quantum fields on lorentzian manifolds_, in _Global Differential Geometry_, Springer Proceedings in Math. 17, Springer-Verlag (2011), 359-400  ([arXiv:1104.1158](http://arxiv.org/abs/1104.1158))


### In perturbation theory

The observation that in [[perturbation theory]] the [[renormalization|Stückelberg-Bogoliubov-Epstein-Glaser]] local [[S-matrix|S-matrices]] yield a [[local net of observables]] was first made in 

* V. Il'in, D. Slavnov, _Observable algebras in the S-matrix approach_ Theor. Math. Phys. **36** , 32 (1978)

which was however mostly ignored and forgotten. It is taken up again in

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_  Commun.Math.Phys.208:623-661 (2000) ([arXiv](http://arxiv.org/abs/math-ph/9903028))

(a quick survey is in section 8, details are in section 2).


[[!redirects local nets]]

[[!redirects Haag-Kastler net]]

[[!redirects net of observables]]
[[!redirects nets of observables]]
[[!redirects local net of observables]]
[[!redirects local nets of observables]]

[[!redirects net of quantum observables]]
[[!redirects nets of quantum observables]]
[[!redirects local net of quantum observables]]
[[!redirects local nets of quantum observables]]


[[!redirects causal net]]
[[!redirects causal nets]]
[[!redirects causal net of algebras]]
[[!redirects causal nets of algebras]]
