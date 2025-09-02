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

The _Yang-Mills moduli space_ (short _YM moduli space_, also _instanton moduli space_) is the [[moduli space]] of the [[Yang-Mills equations]], hence the space of its solutions up to [[gauge]]. It is used in the proof of [[Donaldson's theorem]], which was listed as [[Simon Donaldson]]'s contributions for einning the [[Fields medal]], and to defined the [[Donaldson invariants]] used to study [[4-manifolds]]. A difficulity is, that the Yang-Mills moduli space is usually not compact and has to be compactified around singularities through laborious techniques. An improvement later appeared with the always compact [[Seiberg-Witten moduli space]]. The Yang-Mills moduli space is named after [[Chen Ning Yang]] and [[Robert Mills]], who introduced the underlying [[Yang-Mills equations]] in 1954.

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
In particular for $G=\operatorname{SU}(2)$ the second [[special unitary group]]: ([Freed & Uhlenbeck 1991, between eq. (2.28) and (2.29) on p. 42](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=-8c_2(P)[X]
-3(1-b_1+b_2^-).
$$
In particular for $G=\operatorname{SO}(3)$ the third [[special orthogonal group]]: ([Freed & Uhlenbeck 1991, Eq. (2.29) on p. 42 & eq. (10.3) on p. 155](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=2p_1(P)[X]
-3(1-b_1+b_2^-).
$$

## Related entries

* [[Seiberg-Witten moduli space]] (monopole moduli space)

## References

* {#Donaldson83} [[Simon Donaldson]]. _An application of gauge theory to four-dimensional topology_. In: Journal of Differential Geometry. 18. Jahrgang, Nr. 2, 1. Januar 1983, [doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)
* {#Donaldson87} [[Simon Donaldson]]. _The orientation of Yang-Mills moduli spaces and 4-manifold topology_. In: Journal of Differential Geometry. 26. Jahrgang, Nr. 3, 1. Januar 1987, [doi:10.4310/jdg/1214441485](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-26/issue-3/The-orientation-of-Yang-Mills-moduli-spaces-and-4-manifold/10.4310/jdg/1214441485.full)
* {#FreedUhlenbeck91}  [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

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