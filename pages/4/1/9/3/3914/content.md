
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea


Generally, for $E$ an [[E-∞ ring]] [[spectrum]], and $P \to X$ a [[sphere spectrum]]-bundle, an _$E$-orientation_ of $P$ is a trivialization of the [[associated bundle|associated]] $E$-bundle.

Specifically, for $P = Th(V)$ the [[Thom space]] of a [[vector bundle]] $V \to X$, an $E$-orientation of $V$ is an $E$-orientation of $P$.

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


**Example** For $R = \mathbb{S}$ the [[sphere spectrum]], we have that $GL_1(\mathbb{S})$ is the [[classifying space]] for spherical fibrations.

**Example** There is a canonical morphism

$$
  B O \to B GL_1(\mathbb{S})
$$

from the classifying space of the [[orthogonal group]], called the **$J$-homomorphism**. Postcomposition with this sends real [[vector bundle]]s $V \to X$ to sphere bundles. This is what is modeled by the [[Thom space]] construction


$$
  J : V \mapsto S^V
$$

which sends each fiber to its [[one-point compactification]].



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

**Proposition** For $f : R \to S$ a morphism of $E_\infty$-rings, and $\zeta : X \to B GL_1(R)$ the classifying map for an $R$-bundle, the corresponding associated $S$-bundle classified by the composite

$$
  X \stackrel{\zeta}{ \to } B GL_1(R) \stackrel{f}{\to} B GL_1(S)
$$

is given by the [[smash product]]

$$
  X^{f \circ \zeta} \simeq X^\zeta \wedge_R S
  \,.
$$

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

Now, the [[Thom spectrum]] $ M O$ is the sphere bundle over $B O$ associated to the $O$-[[universal principal bundle]]. In generalization of the way that a trivialization of an ordinary $G$-principal bundle $P$ is given by a $G$-equivariant map $P \to G$, one finds that trivializations of the morphism

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

**Example** The construction of the $String$-orientation of [[tmf]], hence a morphism

$$
  M String \to tmf
$$

is discussed in ([Hopkins, last pages](#Hopkins)).

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

## Examples

* For $V \to X$ a vector bundle of rank $k$, an ordinary [[orientation]] is a trivialization of the line bundle $\wedge^k V$. This is indeed equivalently a trivialization of $V \wedge H(\mathbb{R})$ of smashing with the [[Eilenberg-MacLane spectrum]].

* For spin orientation of vector bundle the construction is given by forming [[Clifford algebra]] bundles.

* For string orientation of vector bundle the construction is supposed to be given by forming free fermion [[local net]]-bundle. See [[Andre Henriques]]' website.

(...)


## Related concepts

* [[differential Thom class]]

* [[differential orientation]]

## References

Orientation of vector bundles in $E$-cohomology is discussed for instance in

* [[eom]], _[Orientation](http://eom.springer.de/o/o070200.htm)_

The general abstract story of $E$-orientation of sphere fibrations is discussed in

* [[Mike Hopkins]], _The String orientation of tmf_ (talk notes by [[Andre Henriques]]) ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter14/MikesTalk3.pdf))
{#Hopkins}

with an eye towards constructing the [[string structure]]-orientation of [[tmf]].

[[!redirects Thom class]]