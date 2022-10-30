
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


Generally, for $E$ an [[E-∞ ring]] [[spectrum]], and $P \to X$ a [[sphere spectrum]]-bundle, an _$E$-orientation_ of $P$ is a trivialization of the [[associated bundle|associated]] $E$-bundle.

Specifically, for $P = Th(V)$ the [[Thom space]] of a [[vector bundle]] $V \to X$, an $E$-orientation of $V$ is an $E$-orientation of $P$.

More generally, for $A$ an $E$-algebra spectrum, an $E$-bundle is $A$-orientable if the associated $A$-bundle is trivializable. For more on this see [[(∞,1)-vector bundle]].

## Definition


### General abstract

Let $E$ be a [[E-∞ ring]] [[spectrum]]. Write $\mathbb{S}$ for the [[sphere spectrum]].

#### $GL_1(R)$-principal $\infty$-bundles

Write $R^\times$ or $GL_1(R)$ for the [[general linear group]] of the $E_\infty$-ring $R$: it is the subspace of the degree-0 space $\Omega^\infty R$ on those points that map to multiplicatively invertible elements in the ordinary ring $\pi_0(R)$.

Since $R$ is $E_\infty$, the space $GL_1(R)$ is itself an [[infinite loop space]]. Its one-fold [[delooping]] $B GL_1(R)$ is the [[classifying space]] for $GL_1(R)$-[[principal ∞-bundle]]s (in [[Top]]): for $X \in Top$ and $\zeta : X \to B GL_1(R)$ a map, its [[homotopy fiber]]


$$
  \array{
    GL_1(R) &\to& P &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    * &\stackrel{x}{\to}& X
   &\stackrel{\zeta}{\to}&
   B GL_1(R)
  }
$$

is the $GL_1(R)$-principal $\infty$-bundle $P \to X$ classified by that map.


+-- {: .num_example}
###### Example

For $R = \mathbb{S}$ the [[sphere spectrum]], we have that $B GL_1(\mathbb{S})$ is the [[classifying space]] for spherical fibrations.

=--

+-- {: .num_example}
###### Example

There is a canonical morphism

$$
  B O \to B GL_1(\mathbb{S})
$$

from the classifying space of the [[orthogonal group]] to that of the [[infinity-group of units]] of the [[sphere spectrum]], called the _[[J-homomorphism]]_. Postcomposition with this sends real [[vector bundle]]s $V \to X$ to sphere bundles. This is what is modeled by the [[Thom space]] construction


$$
  J : V \mapsto S^V
$$

which sends each fiber to its [[one-point compactification]].

=--


#### $GL_1(R)$-associated $\infty$-bundles

For $P \to X$ a $GL_1(R)$-[[principal ∞-bundle]] there is canonically the corresponding [[associated ∞-bundle]] with fiber $R$. Precisely, in the [[stable (∞,1)-category]] $Stab(Top)$ of [[spectra]], regarded as the [[stabilization]] of the [[(∞,1)-topos]] [[Top]]


$$
  Stab(Top) \simeq Spectra
   \stackrel{\overset{\Sigma^\infty}{\leftarrow}}{\underset{\Omega^\infty}{\to}}
  Top
$$

the associated bundle is the [[smash product]] over $\Sigma^\infty GL_1(R)$

$$
  X^\zeta := \Sigma^\infty P \wedge_{\Sigma^\infty GL_1(R)} R
  \,.
$$

This is the generalized **Thom spectrum**. For $R = K O$ the real [[K-theory spectrum]] this is given by the ordinary [[Thom space]] construction on a [[vector bundle]] $V \to X$.

An $E$-orientation of a vector bundle $V \to X$ is a trivialization of the $E$-module bundle $E \wedge S^V$, where fiberwise form the [[smash product]] of $E$ with the [[Thom space]] of $V$.

+-- {: .num_prop}
###### Proposition

For $f : R \to S$ a morphism of $E_\infty$-rings, and $\zeta : X \to B GL_1(R)$ the classifying map for an $R$-bundle, the corresponding associated $S$-bundle classified by the composite

$$
  X \stackrel{\zeta}{ \to } B GL_1(R) \stackrel{f}{\to} B GL_1(S)
$$

is given by the [[smash product]]

$$
  X^{f \circ \zeta} \simeq X^\zeta \wedge_R S
  \,.
$$

=--

This appears as ([Hopkins, bottom of p. 6](#Hopkins)).

#### $R$-Orientations

For $X \stackrel{\zeta}{\to} B GL_1(\mathbb{S})$ a sphere bundle, an **$E$-orientation** on $X^\zeta$ is a trivialization of the associated $R$-bundle $X^\zeta \wedge R$, hence a trivialization (null-homotopy) of the classifying morphism

$$
  X \stackrel{\zeta}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
  \,,
$$

where the second map comes from the unit of $E_\infty$-rings $\mathbb{S} \to R$ (the sphere spectrum is the [[initial object]] in $E_\infty$-rings).

Specifically, for $V : X \to B O$  a [[vector bundle]], an $E$-orientation on it is a trivialization of the $R$-bundle associated to the associated [[Thom space]] sphere bundle, hence a trivialization of the morphism

$$
  \array{
  B O &\stackrel{J}{\to}& B GL_1(\mathbb{S})
    &\stackrel{\iota}{\to}&
   B GL_1(R)
   \\
   {}^{\mathllap{V}}\uparrow & \nearrow_{\mathrlap{\zeta}}
   \\
   X
  }
  \,.
$$

This appears as ([Hopkins, p.7](#Hopkins)).

A natural $R$-orientation of _all_ vector bundles is therefore a trivialization of the morphism

$$
  B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
 \,.
$$

Similarly, an $R$-orientation of _all_ [[spinor bundle]]s is a trivialization of

$$
  B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

and an $R$-orientation of all [[string group]]-bundles a trivialization  of

$$
  B String \to B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

and so forth, through the  [[Whitehead tower]] of $B O$.

Now, the [[Thom spectrum]] [[MO]] is the [[spherical fibration]] over $B O$ [[associated infinity-bundle|associated]] to the $O$-[[universal principal bundle]]. In generalization of the way that a trivialization of an ordinary $G$-principal bundle $P$ is given by a $G$-equivariant map $P \to G$, one finds that trivializations of the morphism

$$
  B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

correspond to $E_\infty$-maps

$$
  M O \to R
$$

from the [[Thom spectrum]] to $R$. Similarly trivialization of 

$$
  B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

corresponds to morphisms 

$$
  M Spin \to R
$$

and trivializations of 

$$
  B String \to B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

to morphisms

$$
  M String \to R
$$

and so forth.

This is the way orientations in generalized cohomology often appear in the literature.


+-- {: .num_example}
###### Example

The construction of the [[string orientation of tmf]], hence a morphism

$$
  M String \to tmf
$$

is discussed in ([Hopkins, last pages](#Hopkins)).

=--

### Concretely for vector bundles

For $H$ the [[multiplicative cohomology theory]] corresponding to $E$, and $V \to X$ a [[vector bundle]] of rank $n$, an $H$-**orientation** of $V$ is an element $u \in H^n(Th(V))$ in the cohomology of the [[Thom space]] of $V$ -- a **Thom class** -- with the property that its restriction $i^* u$ along $i : S^n \to Th(V)$ to any fiber of $Th(V)$ is 

$$
  i^* u = \epsilon \cdot \gamma_n 
  \,,
$$

where

* $\epsilon \in H^0(S^0)$ is a multiplicatively invertible element;

* $\gamma_n \in H^n(S^n)$ is the image of the multiplicative unit
  under the [[suspension isomorphism]] $H^0(S^0) \stackrel{\simeq}{\to}H^n(S^n)$.   

Multiplication with $u$ induces hence an [[isomorphism]]

$$
  (-)\cdot u : H^\bullet(X) \stackrel{\simeq}{\to} H^{\bullet + n}(Th(V))
  \,.
$$

This is called the [[Thom isomorphism]].

The existence of an $H$-orientation is necessary in order to have a notion of [[fiber integration]] in $H$-cohomology.

## Properties

### Relation between Thom classes and trivializations

The relation (equivalence) between choices of [[Thom classes]] and trivializations of [[(∞,1)-line bundles]] is 
discussed e.g. in [Ando-Hopkins-Rezk 10, section 3.3](#AndoHopkinsRezk10)

### Relation to genera
 {#RelationToGenera}

Let $G$ be a [[topological group]] equipped with a [[homomorphism]] to the [[stable orthogonal group]], and write $B G \to B O$ for the corresponding map of [[classifying spaces]]. Write $J \colon B O \longrightarrow B GL_1(\mathbb{S})$ for the [[J-homomorphism]].

For $E$ an [[E-∞ ring]], there is a canonical homomorphism $B GL_1(\mathbb{S}) \to B GL_1(E)$ between the [[deloopings]] of the [[∞-groups of units]]. A trivialization of the total composite

$$
  B G \to B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to B GL_1(E)
$$

is a universal $E$-orientation of [[G-structures]]. Under [[(∞,1)-colimit]] in $E Mod$ this induces a homomorphism of $E$-[[∞-modules]]

$$
  \sigma \;\colon\; M G \to E
$$

from the universal $G$-[[Thom spectrum]] to $E$. 

If here $G \to GL_1(\mathbb{S})$ is the $\Omega^\infty$-component of a map of [[spectra]] then this $\sigma$ is a homomorphism of [[E-∞ rings]] and in this case there is a [[bijection]] between universal orientations and such $E_\infty$-ring homomorphisms ([Ando-Hopkins-Rezk 10, prop. 2.11](#AndoHopkinsRezk10)).

The latter, on passing to [[homotopy groups]], are [[genera]] on manifolds with [[G-structure]].



 
## Examples

* For $V \to X$ a vector bundle of rank $k$, an ordinary [[orientation]] is a trivialization of the line bundle $\wedge^k V$. This is indeed equivalently a trivialization of $V \wedge H(\mathbb{R})$ of smashing with the [[Eilenberg-MacLane spectrum]].

* For spin orientation of vector bundle the construction is given by forming [[Clifford algebra]] bundles.

* [[K-orientation]]

* [[sigma-orientation]], [[string orientation of tmf]]

* For string orientation of vector bundle the construction is supposed to be given by forming free fermion [[local net]]-bundle. See [[Andre Henriques]]' website.

### Atiyah-Bott-Shapiro orientation

* [[Atiyah-Bott-Shapiro orientation]]

#### $Spin$-orientation of $KO$

#### $Spin^c$-orientation of $KU$


### Complex orientation

An $E_\infty$ [[complex oriented cohomology theory]] $E$ is indeed equipped with a universal complex orientation given by an $E_\infty$-ring homomorphism $MU \to E$, see [here](complex+oriented+cohomology+theory#InTermsOfGenera).

### Ando-Hopkins-Rezk string orientation of $tmf$


## Related concepts

* [[differential Thom class]]

* [[differential orientation]], [[fiber integration in differential cohomology]]

* [[(infinity,1)-vector bundle]]

## References

A comprehensive account of the general abstract persepctive (with predecessors in [Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)) is in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 {#ABGHR}

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], section 6 of _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 
Lecture notes include

* [[Mike Hopkins]] (notes by[[Andre Henriques]]), _The String orientation of tmf_  ([arXiv:0805.0743](http://arxiv.org/abs/0805.0743))
 {#Hopkins}

which are motivated towards constructing the [[string orientation of tmf]], based on 

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

Orientation of vector bundles in $E$-cohomology is discussed for instance in

* [[eom]], _[Orientation](http://eom.springer.de/o/o070200.htm)_

[[!redirects Thom class]]
[[!redirects Thom classes]]


[[!redirects orientations in generalized cohomology]]