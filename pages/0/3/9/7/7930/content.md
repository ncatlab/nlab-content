+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[representation]] of the [[spin group]].

## Properties
 {#Properties}

### Complex representations

Complex representations of the [[spin group]] follow a mod-2 [[Bott periodicity]].

In even $d = 2n$ there are two inequivalent complex-linear [[irreducible representations]] of $Spin(d-1,1)$, each of complex [[dimension]] $2^{d/2-1}$, called the two _chiral_ representations, or the two _Weyl spinor_ representations.

For instance for $d = 10$ one often writes these as $\mathbf{16}$ and $\mathbf{16}^\prime$. 

The [[direct sum]] of the two chiral representation is called the _Dirac spinor_ representation, for instance $\mathbf{16} + \mathbf{16}^\prime$.

In odd $d = 2n+1$ there is a single complex [[irreducible representation]] of complex [[dimension]] $2^{(2-1)/2}$. For instance for $d = 11$ one often writes this as $\mathbf{32}$. This is called the _Dirac spinor_ representation in this odd dimension.

For $d = 2n$, if $\{\Gamma^1, \cdots, \Gamma^n\}$ denote the generators of the [[Clifford algebra]] $Cl_{d-1,1}$ then there is the _chirality operator_

$$
  \Gamma^{d+1} \coloneqq \Gamma^1 \cdot \Gamma^2 \cdots \Gamma^d
$$

on the Dirac representation, whose [[eigenspaces]] induce its decomposition into the two chiral summands. 

The unique irreducible Dirac representation in the odd dimension $d+1$ is, as a complex vector space, the sum of the two chiral representations in dimension $d$, with the Clifford algebra represented by $\Gamma^1$ through $\Gamma^d$ acting diagonally on the two chiral representations, and the chirality operator $\Gamma^{d+1}$ in dimension $d$ acting on their sum, now being the representation of the $(d+1)$st Clifford algebra generator.



### Real and quaternionic representations

One may ask in which dimensions $d$ the above complex representation admit a [[real structure]] or a [[quaternionic structure]].

Real spinor representations are also called _Majorana representations_, and an element of a real/Majorana spin representation is also called a _Majorana spinor_. On a Majorana representation $S$ there is a non-vanishing symmetric and $Spin(d-1,1)$-invariant [[bilinear form]] $S \otimes S \longrightarrow \mathbb{R}^d$, projectively unique if $S$ is [[irreducible representation|irreducible]]. This serves as the odd-odd [[Lie bracket]] in the [[super Lie algebra]] called the [[super Poincaré Lie algebra]] [[Lie algebra extension|extension]] of the ordinary [[Poincaré Lie algebra]] induced by $S$. This is "[[supersymmetry]]" in [[physics]].

The above irreducible complex representations admit a [[real structure]] for $d = 1,2,3 \, mod \, 8$. 

Therefore in dimension $d = 2 \, mod \, 8$ there exist _Majorana-Weyl spinor_ representations.

The above irreducible complex representations admit a [[quaternionic structure]] for $d = 5,6,7 \, mod \, 8$. 





## Related entries

* [[spinor]], [[spinor bundle]]

* [[Fierz identity]]

* [[unitary representation of the super Poincaré group]]

* [[charge conjugation matrix]]

* [[metaplectic representation]]



## References

Chapter I.5 of 

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], _[[Spin geometry]]_, Princeton University Press (1989)


* Anna Engels, _Spin representations_ ([pdf](http://www.math.uni-bonn.de/people/ag/ga/teaching/seminare/ws0304/repr.pdf))

For [[Lorentzian manifold|Lorentzian]] signature and with an eye towards [[supersymmetry]] in [[QFT]], see 

* [[Daniel Freed]], _Lecture 3 of [[Five lectures on supersymmetry]]_

* [[Antoine Van Proeyen]], _Tools for supersymmetry_ ([arXiv:hep-th/9910030](http://arxiv.org/abs/hep-th/9910030))

* [[Joseph Polchinski]], part II, appendix B of _[[String theory]]_, Cambridge Monographs on Mathematical Physics (2001)

[[!redirects spin representations]]

[[!redirects spinor representation]]
[[!redirects spinor representations]]

[[!redirects Weyl spinor]]
[[!redirects Weyl spinors]]
[[!redirects Weyl representation]]
[[!redirects Weyl representations]]

[[!redirects Dirac spinor]]
[[!redirects Dirac spinors]]
[[!redirects Dirac representation]]
[[!redirects Dirac representations]]

[[!redirects Majorana spinor]]
[[!redirects Majorana spinors]]
[[!redirects Majorana representation]]
[[!redirects Majorana representations]]

[[!redirects Majorana-Weyl spinor]]
[[!redirects Majorana-Weyl spinors]]
[[!redirects Majorana-Weyl representation]]
[[!redirects Majorana-Weyl representations]]



