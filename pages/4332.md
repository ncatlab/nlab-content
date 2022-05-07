
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In [[physics]] there are (at least) two different concepts that go by the name **gauge group**:

* a _local gauge group_ $G$ is a structure group of $G$-[[principal bundle]]s in the configuration space of a classical [[gauge theory]]: it acts by [[gauge transformation]]s on the space of field configurations.

* a _global gauge group_ is a group of [[automorphism]]s that acts on the ([[local net]] of) [[observable]]s of a [[quantum field theory]].

Notably after [[quantization]] the gauge group in the first sense does _not_ become a gauge group in the second sense. On the contrary, observables in quantum field theory are required _not_ to depend on gauge transformations in the first sense, and part of what makes quantization of [[gauge theory]] nontrivial is to find among all potentiall candidate observables those that actually are invariant under gauge transformations, i.e. under isomorphisms of [[principal bundle]]s with [[connection on a bundle|connection]] in the configuration space of the gauge theory.

### Global gauge group

The concept of gauge groups is most prominent in [[quantum field theory]], where the gauge group of a [[physical system]] is the [[group]] of transformations of the mathematical model of the system that do not correspond to any measurable [[physics|physical]] effects. In this sense, nontrivial gauge groups arise from redundancies of the mathematical description. Gauge groups are a central ingredient of [[gauge theories]]. 

In  [[AQFT]] gauge groups are introduced via a [[net of C-star-systems]].

### Local gauge groups

In [[Yang-Mills theory]] and other [[gauge theories]] the _gauge groups_ is the structure group $G$ of the $G$-[[principal bundle]] on which the [[Yang-Mills field]] is a [[connection on a bundle|connection]].

Local gauge groups are visible in the [[Lagrangian mechanics|Lagrangian]] approach to [[quantum field theory]], where they act on the configuration space on which the [[action functional]] is a function by [[gauge transformation]]s. A large machinery has been developed to handle the ([[path integral]]) [[quantization]] of [[action functional]]s on such configuration spaces. See for instance [[BV-BRST formalism]].

## Properties
 {#Properties}

### Not a redundancy
 {#NotARedundancy}

Sometimes one sees the statement being made that gauge symmetry in theories of [[physics]] is just a sign of a _redundancy_ in the theory, since, after all, gauge equivalent configurations are equivalent.

But, instead, there is genuine information contained in the gauge group of a physical theory: it encodes the [[homotopy type]] of the [[moduli space]] of configurations; or in other words: the higher [[homotopy group]]s in the [[∞-groupoid]] of [[configuration space|configurations]] of the system.  [[infinitesimal object|Infinitesimally]] this is given by the [[BRST complex]] of the system, and the nature of the gauge group controls its higher [[cochain cohomology|cohomology groups]]. For instance the degree-1 cohomology of the BRST complex (meaning: "ghost degree-1") of a system contains the possible gauge [[quantum anomalies]] (as discussed there) of the system. This is clearly not redundant information.  

Abstractly speaking, the idea that symmetry is _just_ a redundancy is a mistake of [[decategorification]]: passing from a [[groupoid]] of [[configuration space|configurations]] -- where different configurations are related by [[morphism]]s called [[gauge transformation]]s -- to the [[quotient]] space of configurations modulo gauge transformations is the [[decategorification]] of the groupoid. More technically speaking, it is the _[[0-truncated|0-truncation]]_ . It computes the 0-th [[homotopy group]] and forgets all the higher homotopy groups.

While there is indeed some information extracted by this process, that about the gauge equivalence classes of configurations, other information is lost.

Physically speaking, notably the _locality_ of field theory would break down if one insisted on always passing to gauge equivalence classes of configurations. 

For instance in a finite [[QFT]] such as [[Dijkgraaf-Witten theory]] with gauge group $G$, the [[moduli space]] is  the [[delooping]]/[[classifying space]] $\mathbf{B}G$. This space is [[connected]], reflecting the fact that _locally_ every configuration of DW-theory is gauge equivalent to every other: namely the field configurations are $G$-[[principal bundle]]s and locally on a piece of space $U$ these are all equivalent to the trivial principal bundle $U \times G$. If one insisted that only gauge equivalence classes of configuration contain non-redundant information, then one would find that either DW theory is not a local QFT or else that it contains the trivial configuration.

Entirely analogous comments apply to more interesting theories such as [[Yang-Mills theory]], only that there the moduli space is richer: it is the [[differential cohomology|differential refinement]] $\mathbf{B}G_{conn} := [P_1(-),\mathbf{B}G]$ of $\mathbf{B}G$ (see _[[connection on a bundle]]_ for details). Again, this cannot be reconstructed from its decategorification and if one insisted on passing to gauge equivalence classes of configurations then either Yang-Mills theory would no longer appear as a local QFT, or else it would have just the the globally trivial configurations.

To say this more precisely, here instead of "[[moduli space]]" we should be saying "[[moduli stack]]". The mathematical theory of [[stacks]] is the theory that deals with systems that are both _local_ (in that global configurations are glued together from local data) as well as equipped with (gauge) symmetries. In that more refined language of [[higher topos theory]] one would find and say that the [[0-truncated|0-truncation]] of $\mathbf{B}G_{conn}$ is the [[sheaf]] of gauge equivalence classes of [[Lie algebra valued differential form]]s. Insisting that this is the only relevant information amounts to insisting that either Yang-Mills theory is not a local theory, or else that all configurations of Yang-Mills theory are given by globally defined differential form data. This would exclude from the theory all configurations with nontrivial [[Chern class]]es, hence in particular it would exclude the [[instanton]] solutions from the theory, which are known to crucuially encode information about the [[quantum field theory|quantum theory]].

That all said, one should note that in _higher_ [[gauge theory]] redundancies may appear after all. This is related to the fact that in [[higher category theory]]/[[homotopy theory]] the notion of _[[resolution]]s_ becomes relevant: there are higher [[moduli stack]]s that look very rich on first sight but turn out to be [[equivalence in an (infinity,1)-category|equivalent]] to simpler moduli stacks. 

For instance if $U(1) \to \hat G \to G$ is a [[central extension]] of the gauge group $G$, then there is a [[2-group]] denoted $(U(1) \to \hat G)$ (see _[[crossed module]]_) which is equivalent to $G$. Therefore 2-gauge theory (such as, say, the [[Courant sigma-model]]) with gauge 2-group $(U(1) \to \hat G)$ is in fact equivalent to ordinary $G$-gauge theory: there is indeed a lot of redundancy in $(U(1) \to \hat G)$. One can detect this by looking at the invariant information: the higher [[homotopy group]]s of $(U(1) \to \hat G)$ or else of its [[moduli stack]] (now a [[infinity-stack|2-stack]]) $\mathbf{B}(U(1) \to \hat G)$ are the same as that of $\mathbf{B}G$.

But even in such a situation, these redundant [[resolution]]s have a good use, in general as well as in applications to physics. In the above example the resolution serves to support an evident morphism $(U(1) \to \hat G) \to (U(1) \to 1) = \mathbf{B}U(1)$. Together with the equivalence to $G$ this constitutes an [[infinity-anafunctor|2-anafunctor]]

$$
  \array{
     \mathbf{B}(U(1) \to \hat G)
     &\to&
     \mathbf{B}^2 U(1)
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{B}G
  }
  \,.
$$

This structure exhibits a [[characteristic class]] of $G$-gauge theory (namely the class that classifies the [[group extension]]). The nontriviality of this class measures the failure of $G$-gauge theory to lift to $\hat G$-gauge theory.

A famous example of this in [[string theory]] comes from the case where $\hat G \to G$ is the projection $U(n) \to PU(n)$ from the [[unitary group]] to the [[projective unitary group]]. In this case a configuration of $PU(n)$-gauge theory is a [[twisted bundle]] representing a class in [[twisted K-theory]] as it appears on the worldvolume of [[D-brane]]s. The corresponding higher $\mathbf{B}U(1)$-gauge theory configuration is the [[Kalb-Ramond field]]([[B-field]]) restricted to the brane, which is the _twist_ that twists the bundle and prevents it from being a configuration in genuine $U(n)$-gauge theory.


## Examples
 {#Examples}

We list examples of local gauge groups and [[∞-groups]] for various higher [[gauge theories]].

* the gauge group of $G$-[[Yang-Mills theory]] is the given [[Lie group]] $G$; for the Yang-Mills theory appearing in the [[standard model of particle physics]] this is the [[unitary group]] $U(3) \times SU(2) \times U(1)$;

* the local gauge group of [[gravity]] on a [[manifold]] $X$ is the [[Poincare group]];

* the gauge [[2-group]] of the [[Kalb-Ramond field]] is the [[circle n-group|circle 2-group]] $\mathbf{B} U(1) = (U(1) \to 1)$;

* the gauge [[3-group]] of the [[supergravity C-field]] is the [[circle n-group|circle 3-group]] $\mathbf{B}^2 U(1) = (U(1) \to 1 \to 1)$;

* the gauge group of abelian [[higher dimensional Chern-Simons theory]] in dimension $4 k+3$ is the [[circle n-group|circle (2k+1)-group]] $\mathbf{B}^{2k} U(1)$;

* the 7-dimensional "[[differential fivebrane structure|fivebrane Chern-Simons theory]]" has as gauge 2-group the [[string 2-group]];

* the symmetry group of [[string field theory]] is some [[∞-group]] that is not an $n$-group for any finite $n$;

* an [[schreiber:∞-Chern-Simons theory]] has in general not only a gauge [[∞-group]] but an [[∞-groupoid]] of symmetries:

  * the [[Poisson sigma-model]] has as gauge groupoid the [[symplectic groupoid]] that is the [[Lie integration]] of the given [[Poisson Lie algebroid]];

  * the [[Courant sigma-model]] has as gauge [[2-groupoid]] the [[symplectic infinity-groupoid|symplectic 2-groupoid]] that integrates the given [[Courant Lie 2-algebroid]];

  * generally, the [[AKSZ sigma-model]] in grade $n$ has as gauge $\infty$-groupoid a [[symplectic infinity-groupoid|symplectic Lie n-groupoid]].


## Related concepts

* [[gauge]]

* [[structure group]], [[equivariance group]]

* [[gauge symmetry]]

* [[gauge fixing]]

* [[spontaneously broken symmetry]]

* [[enhanced gauge symmetry]]

## References

* Wikipedia: [gauge group](http://en.wikipedia.org/wiki/Gauge_group)

### Global gauge group

Chapter IV of 

* [[Rudolf Haag]], _[[Local Quantum Physics]]_

### Local gauge group

(...)

### Local gauging of global symmetries in quantum gravity

It is being argued that after embedding into consistent [[quantum gravity]], all [[global symmetries]] must become [[local symmetries]].

A substantiation of this argument via [[AdS/CFT]] is given in:

* [[Daniel Harlow]], [[Hirosi Ooguri]], _Symmetries in quantum field theory and quantum gravity_ ([arXiv:1810.05338](https://arxiv.org/abs/1810.05338))

* [[Daniel Harlow]], [[Hirosi Ooguri]], _Constraints on symmetry from holography_, Phys. Rev. Lett. 122, 191601 (2019) ([arXiv:1810.05337](https://arxiv.org/abs/1810.05337))

See also:

* Sylvain Fichet, Prashant Saraswat, _Approximate Symmetries and Gravity_ ([arXiv:1909.02002](https://arxiv.org/abs/1909.02002))



[[!redirects gauge group]]
[[!redirects gauge groups]]

[[!redirects global gauge group]]
[[!redirects local gauge group]]
[[!redirects global gauge groups]]
[[!redirects local gauge groups]]