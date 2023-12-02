

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
 {#Idea}

What is called the *strict* or *$C^\ast$-algebraic* form of  [[deformation quantization]] (sometimes just: *strict quantization*) is an attempt to formalize [[quantization]] of [[phase spaces]] or more generally of [[Poisson manifolds]] by _[[continuous field of C*-algebras|continuously deforming]]_, in a precise sense, their [[commutative algebra|commutative]] [[algebras of functions]] ([[algebras of observables]]) to non-commutative [[C*-algebras]] whose [[commutators]] are, to "first order" in a suitable sense, determined by the given [[Poisson bracket]].

This is in contrast to _[[formal deformation quantization]]_, where one asks not for [[C*-algebras]] but just for [[formal power series algebras]]. Where formal deformation quantization is _[[perturbative quantum field theory|perturbative]]_ quantization ([[perturbation]] in [[Planck's constant]], see [Collini (2016)](perturbative+algebraic+quantum+field+theory#Collini16)), strict deformation quantization is meant to reflect [[non-perturbative quantum field theory|non-perturbative]] quantization.

In general, by *[[deformation quantization]]* one means notions of [[quantization]] of [[Poisson manifolds]] $\big(X, \{-,-\}\big)$ in terms of [[sequences]] of [[noncommutative algebra|non-commutative]] [[algebras]] $A_{\hbar}$ parameterized by specific admissible (formal) values of [[Planck's constant]] $\hbar$ including $\hbar = 0$, where $A_0 = C^\infty(X)$ is the ordinary commutative [[algebra of functions]] on the [[underlying]] [[smooth manifold]]. The idea is that $A_{\hbar}$ is the [[algebra of observables]] of the corresponding [[quantum system]] at that value of $\hbar$, arising from "deforming" the commutative product of $A_0$ in a way that increases with $\hbar$ and is [[infinitesimal|infinitesimally]] controlled by the given [[Poisson bracket]] $\{-,-\}$.

Beware that the term "[[deformation quantization]]" is often taken by default to refer to the historically first notion of [[formal deformation quantization]], where $\hbar$ is just a formal [[variable]] (i.e. an [[infinitesimal]], but not an actual [[number]]) and the [[underlying]] [[vector space]] of all algebras in question is that of [[formal power series]] in $\hbar$.

One might naively imagine that the [[formal power series]] appearing in [[formal deformation quantization]] have a finite [[radius of convergence]] $\epsilon \in \mathbb{R}_+$ thus yielding actual (non-formal) deformation quantizations for $\hbar \lt \epsilon$, but in practice this happens rarely (see the first references [below](#ConvergingFormalDeformationQuantization)). Indeed, [[geometric quantization]] makes manifest that [[prequantization]] conditions typically force admissible values of [[Planck's constant|$\hbar$]] to form a [[discrete space|discrete]] [[subspace]] of $\mathbb{R}_+$ with only an [[accumulation point]] at $\hbar = 0$.

Therefore, in *strict* or $C^\ast$-algebraic deformation quantization the parameter [[Planck's constant|$\hbar$]] is typically allowed to take discrete [[positive number|positive]] [[real numbers|real values]] with an [[accumulation point]] at $\hbar = 0$, and where to each such value is associated an actual [[C*-algebra]]-[[algebra of observables|of observables]]. There are a variety of similar but different proposals for what exactly this should mean in detail, see [Hawkins (2008a), Section 2](#Hawkins08a) for overview and references.

In its focus on [[algebras of observables]] the notion of deformation quantization is roughly dual to *[[geometric quantization]]*, which primarily constructs the [[spaces of quantum states]]. In special sitations both notions are compatible, but in general there is a large amount of ambiguity in [[quantization]], between but also within the different approaches.

Typically the $C^\ast$-algebraic deformation takes the quantum algebra to be a suitable [[convolution algebra]] of suitably [[polarization|polarized]] sections over a [[Lie groupoid]] that [[Lie integration|Lie integrates]] a [[Poisson Lie algebroid]] which encodes the original [[Poisson bracket]] to be quantized &lbrack;[Hawkins (2008b)](#Hawkins08b)&rbrack;, see at _[[geometric quantization of symplectic groupoids]]_.

While there are good examples of strict $C^\ast$-algebraic deformation quantization for toy examples such as low spacetime dimension (notably [[quantum mechanics]]) to date no examples of interacting field theories in spacetime dimension $\geq 4$ have a known non-perturbative quantization. (For the case of [[Yang-Mills theory]]/[[QCD]] the construction of its non-perturbative quantization is one of the open "Millennium Problems" listed by the Clay Mathematics Institute, see at _[[quantization of Yang-Mills theory]]_.) 


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

### Converging formal deformation quantization
 {#ConvergingFormalDeformationQuantization}

On [[convergence]] of [[formal power series]] in [[formal deformation quantization]]:

* M. Bordemann, M. Brischle, C. Emmrich, [[Stefan Waldmann]], _Subalgebras with Converging Star Products in Deformation Quantization: An Algebraic Construction for $\mathbb{C}P^n$_ ([arXiv:q-alg/9512019](http://arxiv.org/abs/q-alg/9512019))

* H. Omori, Y. Maeda, N. Miyazaki, A. Yoshida, _Deformation quantization of Fr&#233;chet-Poisson algebras of Heisenberg type_ 2001 ([pdf](http://www.math.keio.ac.jp/library/research/report/2001/01002.pdf))

Textbook account:

* [[Stefan Waldmann]], _Poisson-Geometrie und Deformationsquantisierung_, Springer (2007) &lbrack;[doi:10.1007/978-3-540-72518-3](https://doi.org/10.1007/978-3-540-72518-3)&rbrack;

### Strict deformation quantization proper

The notion of strict $C^\ast$-algebraic deformation quantization was introduced in 

* [[Marc Rieffel]], _Quantization and $C^\ast$-algebras_, Contemporary mathematics vol. 167 (1994) ([pdf](http://math.berkeley.edu/~rieffel/papers/quantization.pdf))

A brief review with a list of open questions is in 

* [[Marc Rieffel]], _Questions on quantization_, Contemp.Math. 228 (1998) 315-326 ([arXiv:quant-ph/9712009](http://arxiv.org/abs/quant-ph/9712009))

More details are in

* {#Rieffel90} [[Marc Rieffel]], _Deformation quantization and operator algebras_, in: Operator theory: operator algebras and applications, Part 1 (Durham, NH, 1988), 411&#8211;423, Proc. Sympos. Pure Math. __51__, Part 1, Amer. Math. Soc. 1990, [MR91h:46120](http://www.ams.org/mathscinet-getitem?mr=1077400);  ([pdf](http://math.berkeley.edu/~rieffel/papers/deformation.pdf))
  
* [[Marc Rieffel]], _Deformation quantization for actions of $\mathbb{R}^d$_, Mem. Amer. Math. Soc. __106__ (1993), no. 506, x+93 pp. [MR94d:46072](http://www.ams.org/mathscinet-getitem?mr=1184061)

Comparative review of notions of strict deformation quantization:

* {#Hawkins08a} [[Eli Hawkins]], Section 2 of: *An Obstruction to Quantization of the Sphere*, Communications in Mathematical Physics **283** (2008) 675–699  &lbrack;[arXiv:0706.2946](http://arxiv.org/abs/0706.2946), [doi:10.1007/s00220-008-0517-2](https://doi.org/10.1007/s00220-008-0517-2)&rbrack;
 
Discussion of strict deformation quantization in terms of [[geometric quantization of symplectic groupoids]] via [[polarization|polarized]] twisted [[groupoid convolution algebras]] is in

* {#Hawkins08b} [[Eli Hawkins]], *A Groupoid Approach to Quantization*, J. Symplectic Geom. **6** 1  (2008) 61-125 &lbrack;[arXiv:math/0612363](https://arxiv.org/abs/math/0612363), [euclid](https://projecteuclid.org/journals/journal-of-symplectic-geometry/volume-6/issue-1/A-groupoid-approach-to-quantization/jsg/1215032733.full)&rbrack;

For the special case of [[Moyal deformation quantization]] &lbrack;[Hawkins (2008b), section 6.2](#Hawkins08b)&rbrack; this construction had been suggested without proof in 

* [[Alan Weinstein]], in P. Donato et al. (eds.) _Symplectic Geometry and Mathematical Physics,  (Birkh&#228;user, Basel, 1991); p. 446.

and a detailed proof was given in
 
* {#GraciaBondiaVarilly94} [[José Gracia-Bondia]], [[Joseph Varilly]], _From geometric quantization to Moyal quantization_, J.Math.Phys. 36 (1995) 2691-2701 ([arXiv:hep-th/9406170](https://arxiv.org/abs/hep-th/9406170)) 



see also

* {#BordemannMeinrenkenSchlichenmaier93} Martin Bordemann, [[Eckhard Meinrenken]], Martin Schlichenmaier, _Toeplitz Quantization of K&#228;hler Manifolds and $gl(N)$ $N\to\infty$_,  	Commun.Math.Phys. 165 (1994) 281-296 ([arXiv:hep-th/9309134](http://arxiv.org/abs/hep-th/9309134))
 


On the special case of [[Poisson manifolds]] that are total spaces of [[Lie algebroids]]:

* [[Klaas Landsman]], B. Ramazan, _Quantization of Poisson algebras associated to Lie algebroids_ ([arXiv:math-ph/0001005](http://arxiv.org/abs/math-ph/0001005))

* [[Klaas Landsman]], _Strict deformation quantization of a particle in external gravitational and Yang-Mills fields_, Journal of Geometry and Physics __12__:2, p. 93-132 ([web](http://adsabs.harvard.edu/abs/1993JGP....12...93L))

On [[continuous field of C-star algebras|continuous fields]] of [[Weyl algebras]] as [[continuous deformation quantizations]] of [[symplectic vector spaces]]:

* [[Ernst Binz]], [[Reinhard Honegger]], [[Alfred Rieckers]], *Field-theoretic Weyl Quantization as a Strict and Continuous Deformation Quantization*, Annales Henri Poincaré **5** (2004) 327–346 &lbrack;[doi:10.1007/s00023-004-0171-y](https://doi.org/10.1007/s00023-004-0171-y)&rbrack;

On [[group algebras]] of ([[underlying]] [[discrete group|discrete]]) [[Heisenberg groups]] as [[strict deformation quantizations]] of [[presymplectic manifold|pre-]][[symplectic vector spaces|symplectic]] [[topological vector spaces]] by [[continuous field of C-star algebras|continuous fields of]] [[Weyl algebras]]:

* [[Ernst Binz]], [[Reinhard Honegger]], [[Alfred Rieckers]], *Infinite dimensional Heisenberg group algebra and field-theoretic strict deformation quantization*, International Journal of Pure and Applied Mathematics **38** 1 (2007) &lbrack;[ijpam:2007-38-1/6](https://ijpam.eu/contents/2007-38-1/6/index.html), [pdf](https://www.ijpam.eu/contents/2007-38-1/6/6.pdf)&rbrack;

* [[Reinhard Honegger]], [[Alfred Rieckers]], *Heisenberg Group Algebra and Strict Weyl Quantization*, Chapter 23 in: *Photons in Fock Space and Beyond, Volume I: From Classical to Quantized Radiation Systems*, World Scientific (2015) &lbrack;chapter:[doi;10.1142/9789814696586_0023](https://doi.org/10.1142/9789814696586_0023), book:[doi:10.1142/9251-vol1](https://doi.org/10.1142/9251-vol1)&rbrack;


[[!redirects C-star algebraic deformation quantizations]]

[[!redirects strict deformation quantization]]
[[!redirects strict deformation quantizations]]

[[!redirects C-star algebraic deformation quantization]]
[[!redirects C*-algebraic deformation quantization]]

[[!redirects strict C*-algebraic deformation quantization]]

[[!redirects strict algebraic deformation quantization]]
[[!redirects strict algebraic deformation quantizations]]

[[!redirects continuous deformation quantization]]
[[!redirects continuous deformation quantizations]]
