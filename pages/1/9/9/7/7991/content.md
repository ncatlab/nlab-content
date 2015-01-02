
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
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

## Definition

### Double cover $Mp$ of $Sp$
 {#DoubleCover}

For $(V,\omega)$ a [[symplectic vector space]], the _metaplectic group_ $Mp(V,\omega)$ is the [[Lie group]] which is [[generalized the|the]] [[universal cover|universal]] [[double cover]] of the [[symplectic group]] $Sp(V,\omega)$.

This has various more explicit presentations. One is by [[quadratic Hamiltonians]]: The metaplectic group is that subgroup of the [[quantomorphism group]] of the [[symplectic manifold]] $(V,\omega)$ whose elements are given by paths of [[Hamiltonians]] that are [[homogeneously quadratic Hamiltonians]] (due to [Leray 81, section 1.1](#Leray81), see also [Robbin-Salamon 93, sections 9-10](#RobbinSalamon93)). (The more general subgroup given by possibly inhomogeneous [[quadratic Hamiltonians]] this way is the [[extended affine symplectic group]]. The subgroup given by linear Hamiltonians is the [[Heisenberg group]] $Heis(V,\omega)$.)

### Circle extension $Mp^c$ of $Sp$
  {#CircleExtension}

There is also a nontrivial  [[circle group]]-extension of the [[symplectic group]], called $Mp^c$. In terms of the [above](#DoubleCover) $Mp$ this is ([Forger-Hess 79 (2.4)](#ForgerHess79) [Cahen-Gutt 13](#CahenGutt13))

$$
  Mp^c(V,\omega) = Mp(V,\omega) \times_{\mathbb{Z}_2} U(1)
$$

(This is in direct [[analogy]] to the group [[Spin^c]] and its relation to [[Spin]].)

Again, this has various more explicit presentations. A standard one is the following. By the [[Stone-von Neumann theorem]] there is an essentially unique [[irreducible representation|irreducible]] [[unitary representation]] $W$ of the [[Heisenberg group]] $Heis(V,\omega)$. This being essentially unique implies that for each element $g\in Sp(V,\omega)$ of the [[symplectic group]], there is a unique [[unitary operator]] $U_g$ such that for all $v\in V$

$$
  W(g(v)) = U_g W(v) U^{-1}_g
  \,.
$$

The group $Mp^c$ is the [[subgroup]] of the [[unitary group]] of all such $U_g$ for $g\in Sp(V,\omega)$. The map $U_g \mapsto g$ exhibits this as a [[group extension]] by the [[circle group]]

$$
  U(1)\longrightarrow Mp^c(V,\omega) \longrightarrow Sp(V,\omega)
  \,.
$$

e.g. ([Robinson-Rawnsley 89, p. 19](#RobinsonRawnsley89), [Derezi&#324;ski-G&#233;rard 13, def. 10.24](#DerezinskiG&#233;rard13))

## Properties

### Relation to the metalinear group

Inside the [[symplectic group]] $Sp(2n, \mathbb{R})$ sits the [[general linear group]] 

$$
  Gl(n,\mathbb{R}) \hookrightarrow Sp(2n,\mathbb{R})
$$

as the subgroup that preserves the standard [[Lagrangian submanifold]] $\mathbb{R}^n \hookrightarrow \mathbb{R}^{2n}$. Restriction of the metaplectic [[group extension]] along this inclusion defines the [[metalinear group]] $Ml(n)$

$$
  \array{
    Ml(n, \mathbb{R}) &\hookrightarrow& Mp(2n, \mathbb{R})
    \\
    \downarrow && \downarrow
    \\
    Gl(n, \mathbb{R}) &\hookrightarrow& Sp(2n, \mathbb{R})
  }
  \,.
$$

Hence a [[metaplectic structure]] on a [[symplectic manifold]] induces a [[metalinear structure]] on its [[Lagrangian submanifolds]].

## Related concepts

* [[metaplectic structure]]

* [[metaplectic correction (in geometric quantization)]]

* [[metaplectic representation]]

## References

Original references include

* [[Andre Weil]], _Sur certains groupes d'op&#233;rateurs unitaires_, Acta Math. 111: 143&#8211;211. (1964).

* {#KashiwaraVergne78} M. Kashiwara; [[Michèle Vergne]], _On the Segal-Shale-Weil Representations and Harmonic Polynomials_, Inventiones mathematicae (1978) ([EuDML](https://eudml.org/doc/142517), [pdf](http://gdz-lucene.tc.sub.uni-goettingen.de/gcs/gcs?&&action=pdf&metsFile=PPN356556735_0044&divID=LOG_0008&pagesize=original&pdfTitlePage=http://gdz.sub.uni-goettingen.de/dms/load/pdftitle/?metsFile=PPN356556735_0044%7C&targetFileName=PPN356556735_0044_LOG_0008.pdf&))

* {#ForgerHess79} [[Michael Forger]], Harald Hess, _Universal metaplectic structures and geometric quantization_, Comm. Math. Phys. Volume 64, Number 3 (1979), 269-278. ([EUCLID](https://projecteuclid.org/euclid.cmp/1103904723))

* {#Leray81} [[Jean Leray]], _Lagrangian analysis and quantum mechanics_, MIT press 1981 [pdf](http://www.maths.ed.ac.uk/~aar/papers/leraybook.pdf)


Further discussion includes

* {#RobinsonRawnsley89} P. L. Robinson, [[John Rawnsley]], _The metaplectic representation, $Mp^c$-structures and geometric quantization_, 1989

* {#RobbinSalamon93} [[Joel Robbin]],  [[Dietmar Salamon]], _Feynman path integrals on phase space and the metaplectic representation_  Math. Z. __221__ (1996), no. 2, 307&#8211;335, ([MR98f:58051](http://www.ams.org/mathscinet-getitem?mr=98f:58051), [doi](http://dx.doi.org/10.1007/BF02622118), [[RobbinSalamonMetaplectic.pdf:file]]), also  in [[Dietmar Salamon]] (ed.), _Symplectic Geometry_, LMS Lecture Note series 192 (1993) 


* [[John Rawnsley]], _On the universal covering group of the real symplectic group_, Journal of Geometry and Physics 62 (2012) 2044&#8211;2058 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rawnsley.pdf))

* {#CahenGutt13} [[Michel Cahen]], [[Simone Gutt]], _$Spin^c$, $Mp^c$ and Symplectic Dirac Operators_, Geometric Methods in Physics Trends in Mathematics 2013, pp 13-28 ([pdf](http://homepages.ulb.ac.be/~sgutt/spinbiel.pdf))

* {#DerezinskiG&#233;rard13} Jan Derezi&#324;ski, Christian G&#233;rard, _Mathematics of Quantization and Quantum Fields_, Cambridge University Press, 2013

[[!redirects metaplectic groups]]

[[!redirects Mp]]
[[!redirects Mp^c]]