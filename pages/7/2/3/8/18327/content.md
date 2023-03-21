
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Given a [[group object]] in the context of [[homotopy theory]] then the [[free construction]] of a [[ring object]] from it in [[stable homotopy category]] is the corresponding "[[group ring]]" construction generalized to homotopy theory.





## Definition

One may consider the construction at various levels of algebraic structure:

* for [[∞-groups]] and [[E-∞ rings]]: _[∞-Group E-∞ rings](InfinityGroupInfintyRings)_

* for [[H-groups]] and [[ring spectra]]: _[H-group ring spectra](#HGroupRingSpectra)_

### $\infty$-Group $\infty$-rings
 {#InfinityGroupInfintyRings}

+-- {: .num_defn #GroupOfUnitsFunctor} 
###### Definition

Write

$$
  gl_1 \; \colon \;  CRing_\infty \to AbGrp_\infty
$$

for the [[(∞,1)-functor]] which sends a [[E-∞ ring|commutative ∞-ring]] to its [[∞-group of units]]. 

=--


+-- {: .num_theorem}
###### Theorem

The [[∞-group of units]] [[(∞,1)-functor]] of def. \ref{GroupOfUnitsFunctor} is a  right-[[adjoint (∞,1)-functor]]

$$
  CRing_\infty 
  \stackrel{\overset{\mathbb{S}[-]}{\leftarrow}}{\underset{gl_1}{\to}}
  AbGrp_\infty
  \,.
$$

=--

This is ([ABGHR 08, theorem 2.1/3.2, remark 3.4](#ABGHR08)).

+-- {: .num_remark} 
###### Remark

The [[left adjoint]]

$$
  \mathbb{S}[-] \colon AbGrp_\infty \to CRing_\infty
$$

is a higher analog of forming the [[group ring]] of an ordinary [[abelian group]] over the [[integers]] 

$$
  \mathbb{Z}[-] \colon Ab \to CRing
  \,,
$$

which is indeed [[left adjoint]] to forming the ordinary [[group of units]] of a ring.

We might call $\mathbb{S}[A]$ the **[[∞-group ∞-ring]]** of $A$ over the [[sphere spectrum]].

=--

### H-Group ring spectra
 {#HGroupRingSpectra}

We consider here the simpler concept after passage to [[equivalence classes]].

Recall

the [[classical homotopy category]] $(Ho(Top), \times, \ast)$ which is a [[symmetric monoidal category]] with respect to forming [[Cartesian product|Cartesian]] [[product spaces]] ([[tensor unit]] is the [[point space]])


its [[pointed objects]] version $(Ho(Top^{\ast/}), \wedge, S^0)$, which is a [[symmetric monoidal category]] with respect to [[smash product]] of [[pointed topological spaces]] ([[tensor unit]] is the [[0-sphere]])


the [[stable homotopy category]] $(Ho(Spectra), \wedge, \mathbb{S})$ which is a [[symmetric monoidal category]] with respect to the [[smash product of spectra]] ([[tensor unit]] is the [[sphere spectrum]])

There is a [[free-forgetful adjunction]]

$$
  Ho(Top^{\ast/})
    \underoverset
      {\underset{U}{\longrightarrow}}
      {\overset{(-)_+}{\longleftarrow}}
      {\bot}
  Ho(Top)
$$

The [[left adjoint]] functor $(-)_+$ adjoins basepoint. This is a [[strong monoidal functor]] (by [this example](pointed+object#WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces)) in that there is a [[natural isomorphism]]

$$
  (X \times Y)_+ \simeq X_+ \wedge Y_+
  \,.
$$

Then there is the [[stabilization]] [[adjunction]]

$$
  Ho(Spectra)
    \underoverset
      {\underset{\Omega^\infty}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {}
  Ho(Top^{\ast/})
$$

(by [this prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory))

Again the left adjoint is a [[strong monoidal functor]] in that there is a [[natural isomorphism]]

$$
  \Sigma^\infty( (X,x) \wedge (Y,y) )
    \simeq
  \left(\Sigma^\infty (X,x)\right) 
    \wedge 
  \left(
    \Sigma^\infty (Y,y)
  \right)
$$

(by [this prop](Introduction+to+Stable+homotopy+theory+--+1-2#SuspensionSpectrumStructuredStrictQuillenAdjunction))


Accordingly also the composite functor

$$
  \mathbb{S}[-] \coloneqq \Sigma^\infty(-)_+
$$

given by

$$
  Ho(Spectra)
    \underoverset
      {\underset{\Omega^\infty}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {}
  Ho(Top^{\ast/})
    \underoverset
      {\underset{U}{\longrightarrow}}
      {\overset{(-)_+}{\longleftarrow}}
      {\bot}
  Ho(Top)
$$

are strong monoidal.


That $\mathbb{S}[-] = \Sigma^\infty((-)_+)$ is [[strong monoidal functor]] for a [[monoid]] $(A,\mu)$ in $(Ho(Top), \times , \ast)$ (an [[H-space]]), then also

$$
  \Sigma^\infty (A_+)
  \;\in\;
  Ho(Spectra)
$$

is a monoid. This is the "monoid ring spectrum" of $A$. 


If $A = G$ is in fact a [[group object]] in $(Ho(Top),\times, \ast)$ (hence an [[H-group]]), then we may call the ring spectrum 

$$
  \Sigma^\infty(G_+)
    \;\in \;
  Ho(Spectra)
$$ 

the _H-group ring spectrum_ of $G$.

+-- {: .num_remark #HGroupRingSpectrumSplitsAsDirectSumWithSphereSpectrum}
###### Remark
**(H-group ring spectrum is a direct sum with the [[sphere spectrum]])**


Notice that an [[H-group]] $G$ already is canonically a [[pointed object]] itself, pointed by its [[neutral element]] $e \colon \ast \to G$. Regarded as an object $(G,e) \in Ho(Top^{\ast/})$ this way then the pointed object $G_+$ above is equivalently the [[wedge sum]] of $G$ with the [[0-sphere]]:

$$
  G_+ \simeq (G,e) \vee S^0
  \,.
$$

Since $\Sigma^\infty$ preserves [[wedge sum]], this means that there is an [[isomorphism]] in $Ho(Spectra)$ 

$$
  \begin{aligned}
    \Sigma^\infty(G_+)
      & \simeq
     \Sigma^\infty 
     \left( 
      (G,e) 
      \vee
       S^0
    \right)
    \\
    & \simeq
    \left( \Sigma^\infty(G,e)  \right) \vee \mathbb{S}
    \\
    & \simeq
    \left( \Sigma^\infty(G,e)  \right) \oplus \mathbb{S}
  \end{aligned}
$$

(where the last isomorphism exhibits that [[wedge sum]] is the [[direct sum]] in the [[additive category]] $Ho(Spectra)$ (by [this lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryHasCoproducts))).

=--


## Examples

* The localization of the $E_\infty$-group ring $\Sigma^\infty(BU(1)_+)$ of the  [[circle 2-group]] at the [[Bott element]] $\beta$ is equivalently the [[Brown representability theorem|representing]] [[spectrum]] [[KU]] of complex [[topological K-theory]]:

  $\mathbb{S}[B U(1)][\beta^{-1}]  \simeq KU$

  This is _[[Snaith's theorem]]_.

## References

* {#ABGHR08} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))


[[!redirects H-group ring spectrum]]
[[!redirects H-group ring spectra]]

[[!redirects H-space ring spectrum]]
[[!redirects H-space ring spectra]]

[[!redirects ∞-group ∞-rings]]

[[!redirects ∞-group E-∞-ring]]
[[!redirects ∞-group E-∞-rings]]

[[!redirects ∞-group E-∞ ring]]
[[!redirects ∞-group E-∞ rings]]

[[!redirects ∞-group E-infinity-ring]]
[[!redirects ∞-group E-infinity-rings]]

[[!redirects ∞-group E-infinity ring]]
[[!redirects ∞-group E-infinity rings]]


[[!redirects ∞-group ring]]
[[!redirects ∞-group rings]]

[[!redirects group ∞-ring]]
[[!redirects group ∞-rings]]

[[!redirects infinity-group infinity-ring]]
[[!redirects infinity-group infinity-rings]]

[[!redirects infinity-group ring]]
[[!redirects infinity-group rings]]

[[!redirects group infinity-ring]]
[[!redirects group infinity-rings]]


