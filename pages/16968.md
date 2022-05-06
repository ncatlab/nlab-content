
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

The generalization of the concept of [[suspension spectrum]] from [[stable homotopy theory]] to $G$-[[equivariant stable homotopy theory]]. 

## Definition

### As a spectrum indexed on a $G$-universe

Let $X$ be a [[pointed topological space|pointed]] [[topological G-space]]. For a [[representation]] $V$ in the [[G-universe]] $U$, write $S^V$ for its [[representation sphere]].

As a [[G-spectrum]] indexed on a [[G-universe]]:

1. the _suspension $G$-pre-spectrum_ is $\Pi^\infty X \colon V \mapsto S^V \wedge X$;

1. the suspension $G$-spectrum is $\Sigma^\infty X \colon V \mapsto Q(S^V \wedge X)$

where $Q (-) = \underset{V \in U}{\cup} \Omega^V \Sigma^V X$.

([Greenlees-May 95](#GreenleesMay95))

### As an orthogonal spectrum

The _equivariant suspension spectrum_ $\Sigma^\infty_G X$ of a [[pointed topological space|pointed]] [[topological G-space]] $X$ is the [[G-spectrum]] which, modeled as an [[orthogonal spectrum]] with $G$-action, is in degree $n$ given by the [[smash product]]

$$
  (\Sigma^\infty_G X)_n \coloneqq X \wedge S^n
$$

of $X$ with the [[n-sphere]], equipped with the canonical [[action]] of the [[orthogonal group]] $O(n)$ just on the $S^n$-factor and equipped with the given action  of $G$ on just $X$.

(e.g. [Schwede 15, example 2.11](#Schwede15))

## Properties
 {#Properties}

### Monoidalness
 {#Monoidalness}

In generalization to the [[strong monoidal functor|strong monoidal]]-[[structure]] on the ordinary [[suspension spectrum]] functor with respect to the [[symmetric monoidal smash product of spectra]] (see [there](suspension+spectrum#StrongMonoidalness))
also the equivariant suspension spectrum functor ought to constitute a [[monoidal (infinity,1)-functor]] from $G$-[[equivariant homotopy theory]] to $G$-[[equivariant stable homotopy theory]].

This follows from general properties of [[stabilization]] when regarding [[equivariant stable homotopy theory]] as the result of inverting [[smash product]] with all [[representation spheres]], via [Robalo 12, last clause of Prop. 4.1 with last clause of Prop. 4.10 (1) ](stabilization#Robalo12), generalized to sets of objects as in [Hoyois 15, section 6.1](stabilization#Hoyois15), see also [Hoyois 15, Def. 6.1](stabilization#Hoyois15).

Alternatively, under the [[equivalence of (infinity,1)-categories|equivalence]] of [[genuine G-spectra]] with [[spectral Mackey functors]] on the [[Burnside category]], it follows as in [Nardin 12, Remark A.12](#Nardin12).

### $RO(G)$-degrees
 {#ROGDegrees}

For $V$ an orthogonal linear $G$-[[representation]] then the value of the equivariant suspension spectrum in that [[RO(G)-grading|RO(G)-degree]] is the [[smash product]] of $X$ with the corresponding [[representation sphere]].

$$
  (\Sigma^\infty_G X)(V) \simeq X \wedge S^V
$$

### Relation between genuine and Bredon-equivariant suspension

For $U$ a complete $G$-[[universe]] and $U^G$ its [[fixed point]] universe, then the inclusion $i \colon U^G \longrightarrow U$ induces an [[adjunction]]

$$
  Spectra(G Top) \stackrel{\overset{i^\ast}{\longleftarrow}}{\underset{i_\ast}{\longrightarrow}}G Spectra 
$$

between [[naive G-spectra]] and [[genuine G-spectra]]. The genuine $G$-suspension spectrum is the naive $G$-suspension spectrum followed by $i$:

$$
  i_\ast \circ \Sigma^\infty_{U^G }  \simeq \Sigma^\infty_U
  \,.
$$

([Greenlees-May 95, p. 16](#GreenleesMay95))



## Examples

The $G$-[[equivariant sphere spectrum]] is 

$$
  \mathbb{S} = \Sigma^\infty_G S^0
$$ 

for $S^0$ regarded as equipped with the (necessarily) trivial $G$-action. It follows that for $V$ an orthogonal linear $G$-representation then in [[RO(G)-degree]] $V$ the equivariant sphere spectrum is the corresponding [[representation sphere]] $\mathbb{S}(V) \simeq S^V$.

### Equivariant homotopy groups and fixed point spectra

The [[equivariant homotopy groups]] and the [[fixed point spectra]] of equivariant suspension spectra $\Sigma^\infty_G X$ decompose into the naive [[fixed points]] of the $G$-action on $X$. This is the _[[tom Dieck splitting]]_, see there for details.


## References

* {#Blumberg17} [[Andrew Blumberg]], Example 2.5.9 in _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))


* {#Schwede15} [[Stefan Schwede]], _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))

Discussion in terms of [[spectral Mackey functors]] on the [[Burnside category]]:

* {#Nardin12} [[Denis Nardin]], section A.2 of _Stability and distributivity over orbital ∞-categories_, 2012 ([hdl.handle.net/1721.1/112895]( http://hdl.handle.net/1721.1/112895), [pdf](https://www.math.univ-paris13.fr/~nardin/thesis.pdf))


[[!redirects equivariant suspension spectra]]

