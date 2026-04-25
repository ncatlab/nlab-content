+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Yang-Mills moduli space_ (short _YM moduli space_, also _instanton moduli space_) is the [[moduli space]] of the [[Yang-Mills equations]], hence the space of its solutions up to [[gauge]]. It is used in the proof of [[Donaldson's theorem]], which was listed as [[Simon Donaldson]]'s contributions for winning the [[Fields medal]], and to defined the [[Donaldson invariants]] used to study [[4-manifolds]]. A difficulity is, that the Yang-Mills moduli space is usually not compact and has to be compactified around singularities through laborious techniques. An improvement later appeared with the always compact [[Seiberg-Witten moduli space]]. The Yang-Mills moduli space is named after [[Chen Ning Yang]] and [[Robert Mills]], who introduced the underlying [[Yang-Mills equations]] in 1954.

In four dimensions, important subspaces of the Yang-Mills moduli space are the _self-dual Yang-Mills moduli space_ (short _SDYM moduli space_, also _self-dual instanton moduli space_) of solutions of the [[self-dual Yang-Mills equations]] up to gauge and the _anti self-dual Yang-Mills moduli space_ (short _ASDYM moduli space_, also _anti self-dual instanton moduli space_) of solutions of the [[anti self-dual Yang-Mills equations]] up to gauge. See also [[D=4 Yang-Mills theory]] and [[self-dual Yang-Mills theory]].

## Definition
 {#Definition}

Consider 

* $G$ a [[Lie group]] 

* with [[Lie algebra]] $\mathfrak{g}$,

* $\pi\colon P\twoheadrightarrow X$ a smooth [[principal bundle|principal $G$-bundle]] 

* over a [[smooth manifold]] $X$. 

Write

$$
  \mathcal{A}
  \;\coloneqq\;
  \Omega^1_{conn}(P;\mathfrak{g})
  \;\subset\;
  \Omega^1(P;\mathfrak{g})
  \,,
$$

for the set of [[Lie algebra valued 1-forms|Lie algebra valued]] [[Ehresmann connection|Ehresmann]] [[connection on a principal bundle|connection]] [[differential 1-form|1-forms]] on $P$.

This is an [[infinite-dimensional manifold|infinite-dimensional]] affine space, [[group action|acted on]] by the group of [[gauge transformations]]

$$
  \mathcal{G}
  \;\coloneqq\; 
  Aut(P)
  \simeq
  \Gamma\big(Ad(P)\big) 
$$

with quotient 

$$
  \begin{array}{rcl}
    \mathcal{A} 
      &\xrightarrow{\phantom{--}[-]\phantom{--}}& 
    \mathcal{A}/\mathcal{G}
  \end{array}
$$

The [[Yang-Mills equations]] $d_A \star F_A=0$, being [[gauge invariance|gauge invariant]], carve out a subspace of this quotient

$$
  \mathcal{M}_P
  \;\coloneqq\;
  \big\{
    [A] \in \mathcal{A}/\mathcal{G}
    \,\big|\,
   d_A\star F_A=0
  \big\}.
$$

If $X$ is a [[4-manifold]], then [[D=4 Yang-Mills theory]] furthermore allows the definition of the _(anti) self-dual Yang-Mills moduli space_:
$$
  \mathcal{M}_P^{\pm}
  \;=\;
  \;\coloneqq\;
  \big\{
    [A] \in \mathcal{M}_P 
    \;\big|\; 
    \star F_A = \pm F_A
  \big\}
  \mathrlap{\,.}
$$



## Properties

If $X$ is a [[4-manifold]], then: ([Donaldson 1983, p. 290](#Donaldson83), [Donaldson 1987, Eq. (2.1)](#Donaldson87), [Freed & Uhlenbeck 1991, Eq. (2.28) ](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=2p_1(Ad(P))[X]
-\dim G(1-b_1+b_2^-).
$$
In particular for $G$ being the second [[special unitary group]] [[SU(2)]] and $P$ a [[principal SU(2)-bundle]]: ([Freed & Uhlenbeck 1991, between eq. (2.28) and (2.29) on p. 42](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=-8c_2(P)[X]
-3(1-b_1+b_2^-).
$$
In particular for $G$ being the third [[special orthogonal group]] [[SO(3)]] and $P$ a [[principal SO(3)-bundle]]: ([Freed & Uhlenbeck 1991, Eq. (2.29) on p. 42 & eq. (10.3) on p. 155](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=2p_1(P)[X]
-3(1-b_1+b_2^-).
$$

## Examples

### SU(2) Yang-Mills moduli spaces

For an oriented $4$-manifold $X$, [[principal SU(2)-bundles]] are fully classified by their second [[Chern class]], meaning that $c_2\colon Prin_{SU(2)}(X)\rightarrow \mathbb{Z}$ is a [[bijection]]. For an [[integer]] $n\in\mathbb{Z}$, let $P_n\twoheadrightarrow X$ be the unique [[principal SU(2)-bundle]] with $c_2(P_c)=c$, then:
$$
p_1 Ad(P_n)[X]
=-4c_2(P_n)[X]
=-4n.
$$
([Donaldson & Kronheimer 97, Eq. (2.1.39)](#DonaldsonKronheimer97)) (The [[adjoint representation]] $Ad\colon SU(2)\rightarrow SO(3)$ is the [[double cover]].)

For $X=S^4$, one has [[signature]] $\sigma(S^4)=0$ and [[Euler characteristic]] $\chi(S^4)=2$. Hence the dimension formulas give:
$$
dim\mathcal{M}_{S^4,P_n}^SDYM
=-8n-3;
$$
$$
dim\mathcal{M}_{S^4,P_n}^ASDYM
=-8n-3.
$$

For $X=\mathbb{C}P^2$, one has [[intersection form]] $Q_{\mathbb{C}P^2}=(+1)$, [[signature]] $\sigma(Q_{\mathbb{C}P^2})=1$ and [[Euler characteristic]] $\chi(\mathbb{C}P^2)=3$. Hence the dimension formulas give:
$$
dim\mathcal{M}_{\mathbb{C}P^2,P_n}^SDYM
=-8n-3;
$$
$$
dim\mathcal{M}_{\mathbb{C}P^2,P_n}^ASDYM
=-8n-6.
$$

For $X=\overline{\mathbb{C}P^2}$, one has [[intersection form]] $Q_{\overline{\mathbb{C}P^2}}=(-1)$, [[signature]] $\sigma(Q_{\overline{\mathbb{C}P^2}})=-1$ and [[Euler characteristic]] $\chi(\overline{\mathbb{C}P^2})=3$. Hence the dimension formulas give:
$$
dim\mathcal{M}_{\overline{\mathbb{C}P^2},P_n}^SDYM
=8n-6;
$$
$$
dim\mathcal{M}_{\overline{\mathbb{C}P^2},P_n}^ASDYM
=8n-3.
$$
With $[\overline{\mathbb{C}P^2}]=-[\mathbb{C}P^2]$, there is an additional sign change compared to the previous example.

### SO(3) Yang-Mills moduli spaces

For an oriented $4$-manifold $X$, [[principal SO(3)-bundles]] are fully classified by their second [[Stiefel-Whitney class]] and first [[Pontrjagin class]], meaning that $(w_2,p_1[X])\colon Prin_{SO(3)}(X)\rightarrow H^2(X,\mathbb{Z}_2)\times\mathbb{Z}$ is a [[bijection]]. For a [[cohomology class]] $w\in H^2(X,\mathbb{Z}_2)$ and an [[integer]] $m\in\mathbb{Z}$, let $P_{c,m}\twoheadrightarrow X$ be the unique [[principal SO(3)-bundle]] with $w_2(P_{w,n})=w$ and $p_1(P_{w,n})[X]=n$, then:
$$
p_1 Ad(P_{w,n})[X]
=p_1(P_{w,n})[X]
=n.
$$
(The [[adjoint representation]] $Ad\colon SO(3)\rightarrow SO(3)$ is the [[identity morphism|identity]].)

For $X=S^4$, one has [[signature]] $\sigma(S^4)=0$ and [[Euler characteristic]] $\chi(S^4)=2$. Hence the dimension formulas give:
$$
dim\mathcal{M}_{S^4,P_{w,n}}^SDYM
=2n-3;
$$
$$
dim\mathcal{M}_{S^4,P_{w,n}}^ASDYM
=2n-3.
$$

## Related entries

[[!include Yang-Mills theory -- table]]

* [[Seiberg-Witten moduli space]] (monopole moduli space)

## References

* {#Donaldson83} [[Simon Donaldson]]. _An application of gauge theory to four-dimensional topology_. In: Journal of Differential Geometry. 18. Jahrgang, Nr. 2, 1. Januar 1983, [doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)

* {#Donaldson87} [[Simon Donaldson]]. _The orientation of Yang-Mills moduli spaces and 4-manifold topology_. In: Journal of Differential Geometry. 26. Jahrgang, Nr. 3, 1. Januar 1987, [doi:10.4310/jdg/1214441485](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-26/issue-3/The-orientation-of-Yang-Mills-moduli-spaces-and-4-manifold/10.4310/jdg/1214441485.full)

* {#FreedUhlenbeck91}  [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

See also:

* Wikipedia, _[Yang–Mills moduli space](https://en.wikipedia.org/wiki/Yang–Mills_moduli_space)_

[[!redirects YM moduli space]]
[[!redirects instanton moduli space]]

[[!redirects self-dual Yang-Mills moduli space]]
[[!redirects SDYM moduli space]]
[[!redirects self-dual instanton moduli space]]

[[!redirects anti self-dual Yang-Mills moduli space]]
[[!redirects ASDYM moduli space]]
[[!redirects anti self-dual instanton moduli space]]