

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _strict_ or _$C*$-algebraic deformation quantization_ is an attempt to formalize [[quantization]] of [[phase spaces]] or more generally of [[Poisson manifolds]] by _[[continuous field of C*-algebras|continuously deforming]]_, in a precise sense, their [[commutative algebra|commutative]] [[algebras of functions]] ([[algebras of observables]]) to non-commutative [[C*-algebras]] whose [[commutators]] are, to "first order" in a suitable sense, determined by the given [[Poisson bracket]].

This is in contrast to _[[formal deformation quantization]]_, where one asks not for [[C*-algebras]] but just for [[formal power series algebras]]. Where formal deformation quantization is _[[perturbative quantum field theory|perturbative]]_ quantization ([[perturbation]] in [[Planck's constant]], see [Collini 16](perturbative+algebraic+quantum+field+theory#Collini16)), strict deformation quantization is meant to reflect [[non-perturbative quantum field theory|non-perturbative]] quantization.

While there are good examples of strict $C^\ast$-algebraic deformation quantization for toy examples such as low spacetime dimension (notably [[quantum mechanics]]) to date no examples of interacting field theories in spacetime dimension $\geq 4$ have a known non-perturbative quantization. (For the case of [[Yang-Mills theory]]/[[QCD]] the construction of its non-perturbative quantization is one of the open "Millenium Problems" listed by the Clay Mathematics Institute, see at _[[quantization of Yang-Mills theory]]_.) 

Typically the $C^\ast$-algebraic deformation takes the quantum algebra to be a suitable [[convolution algebra]] of suitably [[polarization|polarized]] sections over a [[Lie groupoid]] that [[Lie integration|Lie integrates]] a [[Poisson Lie algebroid]] which encodes the original [[Poisson bracket]] to be quantized ([Hawkins 06](#EH)), see at _[[geometric quantization of symplectic groupoids]]_.

## Properties

### Relation to formal deformation quantization

Under favorable circumstances, one can form from a strict $C^\ast$-algebraic deformation 
quantization given by a [[continuous field of C*-algebras]] over a subset of the interval the "differentiation"
as $\hbar \in [0,1]$ tends to 0, such that this reproduces a [[formal deformation quantization]].

Conversely, a natural intuition might be that given a [[formal deformation quantization]] then the subalgebra of [[convergence|converging]] [[power series]] inside all [[formal power series]] has a completion to a [[C*-algebra]] which constitutes a strict deformation quantization.

While this seems natural, the only actual example where this is understood to date 
seems to be the simple case of the standard Poisson structure on $\mathbb{R}^{2n}$
with its [[Weyl algebra]] [[star product]]. (See [this MO discussion](http://mathoverflow.net/a/141410/381)).

## Examples

* [[deformation quantization of the 2-sphere]]

## Related concepts

* [[geometric quantization of symplectic groupoids]]

[[!include infinitesimal and local - table]]


## References

[[convergence|Convergence]] of [[formal power series]] in [[formal deformation quantization]] is discussed for instance in 

* M. Bordemann, M. Brischle, C. Emmrich, [[Stefan Waldmann]], _Subalgebras with Converging Star Products in Deformation Quantization: An Algebraic Construction for $\mathbb{C}P^n$_ ([arXiv:q-alg/9512019](http://arxiv.org/abs/q-alg/9512019))

* H. Omori, Y. Maeda, N. Miyazaki, A. Yoshida, _Deformation quantization of Fr&#233;chet-Poisson algebras of Heisenberg type_ 2001 ([pdf](http://www.math.keio.ac.jp/library/research/report/2001/01002.pdf))

and in the textbook

* [[Stefan Waldmann]], _Poisson-Geometrie und Deformationsquantisierung_,

The notion of strict $C^\ast$-algebraic deformation quantization was introduced in 

* [[Marc Rieffel]], _Quantization and $C^\ast$-algebras_, Contemporary mathematics vol. 167 (1994) ([pdf](http://math.berkeley.edu/~rieffel/papers/quantization.pdf))

A brief review with a list of open questions is in 

* [[Marc Rieffel]], _Questions on quantization_, Contemp.Math. 228 (1998) 315-326 ([arXiv:quant-ph/9712009](http://arxiv.org/abs/quant-ph/9712009))

More details are in

* [[Marc Rieffel]], _Deformation quantization and operator algebras_, in: Operator theory: operator algebras and applications, Part 1 (Durham, NH, 1988), 411&#8211;423, Proc. Sympos. Pure Math. __51__, Part 1, Amer. Math. Soc. 1990, [MR91h:46120](http://www.ams.org/mathscinet-getitem?mr=1077400);  ([pdf](http://math.berkeley.edu/~rieffel/papers/deformation.pdf))
  {#Rieffel90}

* [[Marc Rieffel]], _Deformation quantization for actions of $\mathbb{R}^d$_, Mem. Amer. Math. Soc. __106__ (1993), no. 506, x+93 pp. [MR94d:46072](http://www.ams.org/mathscinet-getitem?mr=1184061)

Discussion of strict deformation quantization in terms of [[geometric quantization of symplectic groupoids]] is in


* {#EH} [[Eli Hawkins]], _A groupoid approach to quantization_,  J. Symplectic Geom. Volume 6, Number 1 (2008), 61-125. ([arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363))
  

A review of variants of the definition of strict deformation quantization is in section 2 of 

* [[Eli Hawkins]], _An Obstruction to Quantization of the Sphere_ ([arXiv:0706.2946](http://arxiv.org/abs/0706.2946))

see also

* {#BordemannMeinrenkenSchlichenmaier93} Martin Bordemann, [[Eckhard Meinrenken]], Martin Schlichenmaier, _Toeplitz Quantization of K&#228;hler Manifolds and $gl(N)$ $N\to\infty$_,  	Commun.Math.Phys. 165 (1994) 281-296 ([arXiv:hep-th/9309134](http://arxiv.org/abs/hep-th/9309134))
 


For the special case of [[Poisson manifolds]] that are total spaces of [[Lie algebroids]], discussion is in

* [[Klaas Landsman]], B. Ramazan, _Quantization of Poisson algebras associated to Lie algebroids_ ([arXiv:math-ph/0001005](http://arxiv.org/abs/math-ph/0001005))

* [[Klaas Landsman]], _Strict deformation quantization of a particle in external gravitational and Yang-Mills fields_, Journal of Geometry and Physics __12__:2, p. 93-132 ([web](http://adsabs.harvard.edu/abs/1993JGP....12...93L))

[[!redirects C-star algebraic deformation quantizations]]

[[!redirects strict deformation quantization]]
[[!redirects strict deformation quantizations]]

[[!redirects C-star algebraic deformation quantization]]

[[!redirects strict C*-algebraic deformation quantization]]
