
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Over the [[complex numbers]] an [[elliptic curve]] (hence a [[complex manifold|complex]] [[torus]]) may be, and often is, presented as a [[quotient]] of the [[complex plane]] by a framed [[lattice]], determined by a point $\tau$ in the [[upper half plane]] $\mathfrak{h}$. But indeed this data determines a [[framed elliptic curve]], namely the underlying [[curve]] $\Sigma$ together with the "edges along which it is glued" by this construction. These are equivalently a choice of [[ordering|ordered]] [[basis]] 

$$
  (a_1,a_2)\in H_1(\Sigma,\mathbb{Z})
$$

of the first [[ordinary homology]] of $\Sigma$ with [[integer]] [[coefficients]] (and vanishing [[intersection number]]).  The [[modular group|modular]] [[special linear group]] [[SL(2,Z)|$SL_2(\mathbb{Z})$]] naturally acts on this data (by [[Möbius transformations]] on $\tau$) and the [[quotient]] [[projection]] exhibits an infinite [[covering]] ([[atlas]]) of the  [[moduli stack of elliptic curves]] over the complex numbers

$$
  \mathfrak{h} \longrightarrow 
 
 \mathfrak{h}
  \sslash
  SL_2(\mathbb{C}) 
   \simeq 
 \mathcal{M}_{ell}(\mathbb{C})
  \,.
$$

The concept of _level structure_ on an elliptic curve is a structure weaker than that of a [[framed elliptic curve|framing]] which analogously gives a [[finite number|finite]] [[covering]]. Instead of considering cycles in integral homology, a _level $n$-structure_ for [[natural number]] $B$ is given by cycles in homology with [[coefficients]] just in the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ (e.g. [Hain 08, def. 4.6](#Hain08)).

On such level-$n$ data now acts instead just the group $SL_2(\mathbb{Z}/n\mathbb{Z})$. The [[kernel]] of the [[projection]] maps is called the _level $n$-subgroup_ (an example of a _[[congruence subgroup]]_)

$$
  \Gamma(n) \to SL_2(\mathbb{Z}) \to SL_2(\mathbb{Z}/n\mathbb{Z})
  \,.
$$

There is then a [[moduli space]] of complex elliptic curves equipped with level $n$-structure

$$
  \mathcal{M}_{ell}(\mathbb{C})[n] \simeq \mathfrak{h}//\Gamma_n
$$

called the _[[modular curve]]_, and this is now a finite cover (of rank the [[order of a group|order]] of the [[finite group]] $SL_2(\mathbb{Z}/n\mathbb{Z})$) of the actual [[moduli stack of elliptic curves|moduli stack of complex elliptic curves]]

$$
  \mathcal{M}_{ell}[n](\mathbb{C})
  \longrightarrow
  \mathcal{M}_{ell}[n](\mathbb{C})//SL_2(\mathbb{Z}/n\mathbb{Z})
  \simeq
  \mathcal{M}_{ell}(\mathbb{C})
  \,.
$$

## Definition

### Congruence subgroups

Let $n \in \mathbb{N}$ be a [[natural number]]. Write

$$
  p_n \;\colon\; SL_2(\mathbb{Z}) \to SL_2(\mathbb{Z}/\mathbb{Z}_n)
$$

for the projection from the [[special linear group]] induced by the [[quotient]] [[projection]] $\mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$ to the [[cyclic group]].

The [[congruence subgroups]] of the [[special linear group]] $SL_2(\mathbb{Z})$ (essentially the [[modular group]]) are defined as follows.

The **principal congruence subgroup** is

$$
  \Gamma(n) \coloneqq ker(p_n) = p_n^{-1}\left(\left\{\array{ 1 & 0 \\ 0 & 1}\right\}\right)
$$

The other two are

$$
  \Gamma_0(n) \coloneqq p_n^{-1}\left(\left\{\array{ \ast & \ast \\ 0 & \ast}\right\}\right)
$$

$$
  \Gamma_1(n) \coloneqq p_n^{-1}\left(\left\{\array{ 1 & \ast \\ 0 & \ast}\right\}\right)
$$


### Over general rings

(e.g [Voloch, def. 1.1](#Voloch)  [Ando 00, section 1.4](#Ando00), [Ando-Hopkins-Strickland 02, section 15.2](#AndoHopkinsStrickland02), [Hill-Lawson 13, section 3.6](#HillLawson13))


## Properties

### Relation to spin structures on elliptic curves
 {#RelationToSpinStructures}

For [[elliptic curves]] over the [[complex numbers]] ([[complex manifold|complex]] oriented pointed [[tori]]) the congruence subgroup $\Gamma_0(2)$ has the interpretation as being precisely the subgroup of the [[modular group]] which preserves one of the "NS-R" [[spin structures]].

In detail, the elliptic curve $\Sigma$, being [[framed manifold|framed]] has a canonical [[spin structure]]  given by the trivial [[double cover]]. The space of all spin structures is a [[torsor]] over $H^1(\Sigma, \mathbb{Z}/2\mathbb{Z}) \simeq [\pi_1(\sigma), \mathbb{Z}/2\mathbb{Z}] \simeq [\mathbb{Z} \times \mathbb{Z}, \mathbb{Z}/2\mathbb{Z}] \simeq (\mathbb{Z}/2\mathbb{Z})^2$. In terms of this action the canonical one is labeled $(0,0)$ and then there are three more, labeled $(1,0)$, $(0,1)$ and $(1,1)$. The full [[modular group]] acts on these via the quotient map $p_2 \;\colon\;  SL_2(\mathbb{Z}) \to SL_{2}(\mathbb{Z}/2\mathbb{Z})$. Hence it preserves $(0,0)$ and mixes the other three spin structures. Precisely the subgroup $\Gamma_0(2)$ preserves $(1,0)$ (and an isomorphic subgroup of course preserves $(0,1)$), while the principal congruence subgroup $\Gamma(2)$ is the one which preserves all four spin structures jointly.

In terms of [[type II string theory]] the spin structure $(1,0)$ is called the "NS-R boundary condition" for the spinors. The [[partition function]] of the [[type II superstring]] "in the NS-R sector" is therefore (at best, indeed it is, being the universal [[Ochanine elliptic genus]]) a [[modular form]] not for the full [[modular group]], but for $\Gamma_0(2)$ ([Witten 87a, below (13)](Witten87a)). For more on this see at _[Witten genus -- Modularity -- For the type II string](Witten+genus#ModularityForTypeIISuperstring)_. The homotopy-theoretic refinement of this involves [[tmf0(2)]], see at _[[spin orientation of Ochanine elliptic cohomology]]_.


## Properties

### Topological modular forms with level structure

The construction of [[topological modular forms]] ([[tmf]]) may be generalized to curves with level structure ([Mahowald-Rezk 09](#MahowaldRezk09)). A systematic kind of "[[modular equivariant elliptic cohomology]]" in this sense is discussed in ([Hill-Lawson 13](#HillLawson13)).


## References

### Over the complex numbers

The principal congruence subgroups are discussed for instance in

* {#Hain08} [[Richard Hain]], section 4.2 of _Lectures on Moduli Spaces of Elliptic Curves_ ([arXiv:0812.1803](http://arxiv.org/abs/0812.1803))

The relation of $\Gamma_1(2)$ to [[spin structures]] is discussed for instance in 

* {#Freed87} [[Daniel Freed]], pages 24-25 of _On determinant line bundles_, 1987 ([pdf](http://www.ma.utexas.edu/users/dafr/detsur.pdf))

* {#Witten87a} [[Edward Witten]],  _Elliptic Genera And Quantum Field Theory_ , Commun.Math.Phys. 109 525 (1987) ([Euclid](http://projecteuclid.org/euclid.cmp/1104117076))


### Over general base rings

The concept of level structure on an elliptic curve is due to

* Nicholas M. Katz, [[Barry Mazur]], _Arithmetic moduli of elliptic curves_, Princeton University Press, Princeton, NJ, 1985

Review of the definition includes

* {#Voloch} [[Felipe Voloch]], _Modular curves -- 1. Level structures_ ([pdf](https://www.ma.utexas.edu/users/voloch/Ellnotes/feb23.pdf))

General discussion is in 

* {#Greicius09} [[Aaron Greicius]], _Elliptic curves with surjective adelic Galois representations_ ([arXiv:0901.2513](http://arxiv.org/abs/0901.2513))

* David Zywina, _Elliptic curves with maximal Galois action on their torsion points_ ([arXiv:0809.3482](http://arxiv.org/abs/0809.3482))

Discussion of the corresponding [[moduli stack]] and its [[tmf]]$(n)$-spectrum is in 

* {#Ando00} [[Matthew Ando]], section 1.4 of _Power operations in elliptic cohomology and representations of loop groups_ Transactions of the American
Mathematical Society 352, 2000, pp. 5619-5666. ([JSTOR](http://www.jstor.org/stable/221905), [pdf](http://www.math.uiuc.edu/~mando/papers/POECLG/poeclg.pdf))

* {#AndoHopkinsStrickland02} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], part 3 of _The sigma orientation is an H-infinity map_. American Journal of Mathematics Vol. 126, No. 2 (Apr., 2004), pp. 247-334 ([arXiv:math/0204053](http://arxiv.org/abs/math/0204053))

* {#MahowaldRezk09} [[Mark Mahowald]] [[Charles Rezk]], _Topological modular forms of level 3_, Pure Appl. Math. Quar. 5 (2009) 853-872 ([pdf](http://www.math.uiuc.edu/~rezk/tmf3-paper-final.pdf))

* {#HillLawson13} [[Michael Hill]], [[Tyler Lawson]], _Topological modular forms with level structure_ ([arXiv:1312.7394](http://arxiv.org/abs/1312.7394))

Specifically Level-2 structure in this context is discussed in 

* {#Stojanoska11} [[Vesna Stojanoska]], _Duality for Topological Modular Forms_ ([arXiv:1105.3968](http://arxiv.org/abs/1105.3968))

* {#Behrens05} [[Mark Behrens]], section 1.3 of _A modular description of the K(2)-local sphere at the prime 3_ ([arXiv:math/0507184](http://arxiv.org/abs/math/0507184))

[[!redirects level structures on an elliptic curve]]

[[!redirects level structures on elliptic curves]]

[[!redirects level N-structure]]
[[!redirects level N structure]]
[[!redirects level N-structures]]
[[!redirects level N structures]]

[[!redirects level-n structure]]
[[!redirects level-n structures]]

[[!redirects level-n structure]]
[[!redirects level-n structures]]

[[!redirects level n-structure]]
[[!redirects level n structure]]
[[!redirects level n-structures]]
[[!redirects level n structures]]


[[!redirects level n subgroup]]
[[!redirects level n subgroups]]



[[!redirects level n-structure on an elliptic curve]]
[[!redirects level n-structure on elliptic curves]]

[[!redirects elliptic curve with level-n structure]]
[[!redirects elliptic curves with level-n structure]]

[[!redirects elliptic curve with level structure]]
[[!redirects elliptic curve with level structures]]

[[!redirects elliptic curves with level structure]]
[[!redirects elliptic curves with level structures]]