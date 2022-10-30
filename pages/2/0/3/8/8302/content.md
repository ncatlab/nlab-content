

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Ordinary homology_ is [[generalized homology]] with respect to an [[Eilenberg-MacLane spectrum]] $H A$, and often understood over $H \mathbb{Z}$. 

Equivalently this is computed by _[[singular homology]]_ with [[coefficients]] in $A$.


## Properties

### Relation to homotopy groups

Ordinary homology with [[coefficients]] in $\mathbb{Z}$ of a [[topological space]] $X$  serves to approximate the [[homotopy groups]] of $X$.

See for instance at _[[Hurewicz theorem]]_

### Description in terms of higher linear algebra
 {#InTermsOfHigherLinearAlgebra}

We discuss ([[twisted cohomology|twisted]]) ordinary homology and [[ordinary cohomology]] in terms of sections of [[(∞,1)-module bundles]] over the [[Eilenberg-MacLane spectrum]].

Let $k$ be a [[commutative ring]]. Write 

$$
  H k \in CRing_\infty
$$

for the [[Eilenberg-MacLane spectrum]] of $k$, canonically regarded as an [[E-∞ ring]]. Write

$$
  (H k) Mod \in (\infty,1)Cat
$$

for the [[(∞,1)-category of (∞,1)-modules]] over $H k$.

+-- {: .num_prop #DoldKan}
###### Proposition

There is an [[equivalence of (∞,1)-categories]]

$$
 (H k)Mod \simeq L_{qi} Ch_\bullet(k Mod)
$$

between the [[(∞,1)-category of (∞,1)-modules]] over the [[Eilenberg-MacLane spectrum]] $H k$ and the [[simplicial localization]] of the [[category of unbounded chain complexes]] of ordinary (1-categorical) $k$-[[modules]].

=--

This is the statement of the _[[stable Dold-Kan correspondence]]_, see at _[(∞,1)-category of (∞,1)-modules -- Properties -- Stable Dold-Kan correspondence](%28infinity%2C1%29-module#StableDoldKanCorrespondence)_.
  
+-- {: .num_defn}
###### Definition

Let $X$ be a [[topological space]] and write $\Pi(X) \in $ [[∞Grpd]] for its underlying [[homotopy type]] (its [[fundamental ∞-groupoid]]). Then we say that an [[(∞,1)-functor]]

$$
  \Pi(X) \to (H k) Mod
$$

is (the [[higher parallel transport]]) a _[[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]]_ over $X$, or a _[[local system]]_ of $H k$-[[(∞,1)-modules]] over $X$.

=--


+-- {: .num_prop}
###### Proposition
**([[Riemann-Hilbert correspondence]])**

If $X$ is an [[orientation|oriented]] [[closed manifold]], then there is an [[equivalence of (∞,1)-categories]]

$$
  [\Pi(X), (H k)Mod]
  \simeq
  (T X)Mod
$$

between [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundles]]/[[local systems]] and [[L-∞ algebroid representations]] of the [[tangent Lie algebroid]] of $X$. From right to left the equivalece is established by sending an [[L-∞ algebroid representation]] given (as discussed there) by a flat $\mathbb{Z}$-graded connection on bundles of chain complexes (via prop. \ref{DoldKan}), to its [[higher holonomy]] defined in terms of [[iterated integrals]].

=--

This is the main theorem in ([Block-Smith 09](#BlockSmith09)).

+-- {: .num_defn}
###### Definition

Write

$$
  \Gamma \;\coloneqq\; \underset{\to}{\lim} \;\colon\;
  [\Pi(X), (H k)Mod]
  \to 
  (H k) Mod
$$

for the [[(∞,1)-colimit]] functor.

=--

+-- {: .num_remark}
###### Remark

We may think of $\Gamma$ equivalently as

* forming flat [[sections]] of a [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]];

* sending a [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]] to its _[[Thom spectrum]]_ (see at _[Thom spectrum -- For (∞,1)-module bundles ](Thom+spectrum#ForInfinityModuleBundles)_).

=--


+-- {: .num_defn}
###### Definition

Write

$$
  \mathbb{I}_X^{H k} \;\colon\; \Pi(X) \to (K k)Mod
$$ 

for the [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]] which is constant on the chain complex concentrated on $k$ in degree 0, the [[tensor unit]] in $[\Pi(X), (H k)Mod] \simeq [\Pi(X), L_{qi}Ch_\bullet(k Mod)]$.

=--

+-- {: .num_prop}
###### Proposition


For $X$ a [[topological space]], we have a [[natural equivalence]] (in view of prop. \ref{DoldKan})

$$
  \Gamma(\mathbb{I}_X^{H k})
  \simeq
  C_\bullet(X,k)
$$

between the $(H k)$-[[(∞,1)-module]] of sections of the trivial $(H k)$-[[(∞,1)-module bundle]] $\mathbb{I}_X^{H k}$ and the [[singular chain complex]] of $X$ for ordinary homology with [[coefficients]] in $k$.

=--

+-- {: .proof}
###### Proof

This is a classical basic (maybe [[folklore]]) statement. Here is one way to see it in full detail.

First notice that the [[(∞,1)-colimit]] of functors out of [[∞-groupoids]] and constant on the [[tensor unit]] in $(H k)Mod$ is by definition the [[(∞,1)-tensoring]] operation of $(H k)Mod$ over [[∞Grpd]]. Now if we find a [[presentable (∞,1)-category|presentation]] of $(H k)Mod$ by a [[simplicial model category]] the by the dicussion at _[(∞,1)-colomit -- Tensoring and cotensoring -- Models](limit+in+a+quasi-category#ModelsForTensoring)_ this [[(∞,1)-tensoring]] is given by the left [[derived functor]] of the [[sSet]]-[[tensoring]] in that simplicial model category.

To obtain this, use prop. \ref{DoldKan} and then the discussion at _[[model structure on chain complexes]]_ in the section _[Projective model structure on unbounded chain complexes](model%20structure%20on%20chain%20complexes#ProjectiveModelStructureOnUnboundedChainComplexes)_ which says that there is a [[simplicial model category]] structure on the [[category of simplicial objects]] in the [[category of unbounded chain complexes]] which models $L_{qi} Ch_\bullet(k Mod)$, and whose weak equivalences are those morphisms that produce [[quasi-isomorphism]] under the [[total chain complex]] functor.

In summary it follows that with any [[simplicial set]] $(\Pi(X))_\bullet in L_{whe} sSet$ representing $\Pi(X)$ (under the [[homotopy hypothesis]]-theorem) we have

$$
  \underset{\to}{\lim} (\mathbb{I}_X^{H k})
  \simeq
  \int_{[n] \in \Delta}  (\Pi(X))_n \cdot \mathbb{I}
  \,,
$$

where on the right we have the [[coend]] over the [[simplex category]] of the [[tensoring]] (of [[simplicial sets]] with [[simplicial objects]] in the [[category of unbounded chain complexes]]) of the standard cosimplicial simplex with the simplicial diagram constant on the [[tensor unit]] [[chain complex]].

The result on the right is manifestly, by the very definition of [[singular homology]], under the ordinary [[Dold-Kan correspondence]] the [[chain complex of singular simplices]]:

$$
  \int_{[n] \in \Delta}  (\Pi(X))_n \cdot \mathbb{I}
  \simeq
  \Pi(X) \otimes k
  \simeq
  C_\bullet(X,k)
  \,.
$$

=--

## Related concepts

* [[ordinary cohomology]]

## References

The [[Riemann-Hilbert correspondence]]/[[de Rham theorem]] for $K k$-modules is established in 

* [[Jonathan Block]], Aaron Smith, _A Riemann--Hilbert correspondence for infinity local systems_ ([arXiv:0908.2843](http://arxiv.org/abs/0908.2843))
 {#BlockSmith09}

