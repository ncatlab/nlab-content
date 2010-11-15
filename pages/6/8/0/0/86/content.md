
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}



## Idea

### The $n$POV {#nPOVIdea}

A [[BRST-complex]] is a [[Chevalley-Eilenberg algebra]] of an [[action Lie algebroid]]. A **BV-BRST complex** is the same for a [[derived ∞-Lie algebroid]].

the _configuration space_ $Conf$ of a physical system -- notably that of a [[gauge theory]] -- is in general not a naive space, such as a [[manifold]], but instead a [[space]] in the general sense of [[higher geometry]]: it is in fact an object in the [[(∞,1)-topos]] of [[derived stack]]s/[[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] on the [[(∞,1)-site]] 

$$
  C :=(dgAlg_k^-)^{op}
$$ 

of formal duals to [[differential graded algebra|cochain differential graded algebras]] in non-postive degree:

$$
  Conf \in \mathbf{H} = Sh_{(\infty,1)}(C)
  \,.
$$  

The way to understand how such [[∞-stack]]s are [[space]]s is described at [[motivation for sheaves, cohomology and higher stacks]]:

we think here of an object $Spec A \in (dgAlg_k^-)^{op}$ as a test space with [[derived geometry|derived]] algebra of functions $A \in dgAlg$.  An object in $Sh_{(\infty,1)}(C)$ is an [[∞-groupoid]] with geometric structure given by such test objects: it can be _probed_ by such test objects.

Every such [[∞-groupoid]] $X$ modeled on objects in $C$ has also a _global_ function algebra $\mathcal{O}(X) \in dgAlg$. This is in general an _unbounded_ [[differential graded algebra]]: it may be nontrivial in positive and negative degrees. For $X = Conf$ the configuration space of a [[gauge theory]], the dg-algebra

$$
  \mathcal{O}(Conf) \in dgAlg
$$

is called the **BV-BRST-complex** of the physical system. Roughly, in positive degrees this dg-algebra remembers the [[k-morphism]]s of the $\infty$-groupoid $Conf$, while in negative degrees it remembers the negative degrees of the derived function algebra of the space of objects of the $\infty$-groupoid.

In the physics literature 

* the elements in degree 0 of $\mathcal{O}(Conf)$ are called the **fields** (really they are the functions on the naive space of fields);

* the elements in positive degree are called the **ghost**s -- this are really the duals to the [[k-morphism]]s of the [[L-∞-algebroid]] $Conf$;

* the elements in negative degree are called **anti-fields** and **anti-ghosts**.  (This is just formal terminology made up in physics for lack of a better term. It has in particular _nothing_ to do with the notion of _anti-particles_ !)

The operation $X \mapsto \mathcal{O}(X)$ extends to an [[(∞,1)-functor]] $\mathcal{O} : \mathbf{H} \to dgAlg^{op}$, which is part of an [[adjoint (∞,1)-functor|(∞,1)-adjunction]]

$$
  (\mathcal{O} \dashv Spec) \;\; : \;\;
  \mathbf{H} \stackrel{\overset{Spec}{\leftarrow}}{\overset{\mathcal{O}}{\to}}
  dgAlg^{op}
  \,.
$$

In detail, $\mathcal{O}$ acts as follows: every [[∞-stack]] $X$ may be written as a ([[homotopy colimit|colimit]]) over [[representable functor|representable]] $Spec A_i \in dgAlg_i$

$$
  X \simeq \lim_{\to^i} Y(Spec A_i)
  \,,
$$

where $Y : (dgAlg^-)^{op} \to \mathbf{H}$ is the [[Yoneda embedding]].

The functor $\mathcal{O}$ takes any such colimit-description, and simply reinterprets the colimit in $dgAlg^{op}$, i.e. the limit in $dgAlg$:

$$
  \mathcal{O}(X) = \lim_{\leftarrow^i} A_i
  \,.
$$

This is proposition 3.1 in

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:math/1002.3636](http://arxiv.org/abs/1002.3636))


### The pedestrian POV

BV theory is the answer to the second of two different questions:

 * **Hamiltonian BFV**: taking quotients of constraint surfaces in [[Poisson manifold]]s by group actions and more generally by the foliation determined by first class constraints;

 * **Lagrangian BV**: integrating forms over [[NQ-supermanifolds]].

### Hamiltonian BFV

The F is for Fradkin.
In this context, the BFV-complex is a [[homological resolution]] of the problem of taking quotients of symplectic manifolds by group actions. 

+-- {: .query}

_Question_: Can you explain more about this? What do you mean by a "homological resolution of the problem"? Is there a nice example? I went over the [blog entry](http://golem.ph.utexas.edu/category/2008/07/poisson_reduction.html) but it seemed to talk about symplectic/Poisson reduction in its own right and didn't yet make the link with the BV formalism. (Bruce)

(Jim)  Thanks, Bruce.  My initial edit here is just to set the record straight - BV $\neq$ BFV. Will expand further and try to answer your query.
=--

See [[homological resolution]].

+-- {: .query}

_Comment_: Kevin Costello is preparing a [book](http://www.math.northwestern.edu/~costello/renormalization) on _Renormalization of quantum field theories_, available on his webpage. He has a section entitled _The BV construction as symplectic reduction_ [](http://www.math.northwestern.edu/~costello/chap3.pdf#page=7). Could you somehow link your explanation to that in some way?

_Urs says:_ I have (only) a vague hunch that Lagrangian and Hamiltonian BV are related in some way by "holography" of sorts, in a way that explains why the master equation in Lagrangian BV -- $\Delta exp(S) = 0$ -- looks like a Schr&#246;dinger equation if one re-interprets the space of histories with the space of states of a system of one dimension higher. Some very useful observations in this regard are in S.L. Lyakhovich, A.A. Sharapov,
_Quantization of Donaldson-Uhlenbeck-Yau theory_
[arXiv](http://arxiv.org/abs/0705.1871), which I talk about at the end of [this](http://golem.ph.utexas.edu/category/2007/08/lyakhonov_and_sharapov_on_qft.html).

(Jim)  I would hope they were related by a homological version of the usual Hamiltonian - Lagrangian correspondence.

Zoran: It sound like, there might be a role of microlocalization in understanding this correspondence. 

=--


### Poisson/symplectic reduction ###

 * _Basics of Poisson reduction_ ([blog](http://golem.ph.utexas.edu/category/2008/07/poisson_reduction.html))

 * Alejandro Cabrera, _Homological BV-BRST methods: from QFT to Poisson reduction_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Charla_IMPA_BRST.pdf))

 * J. Butterfield, _On symplectic reduction in classical mechanis_ ([pdf](http://philsci-archive.pitt.edu/archive/00002373/01/ButterfieldNHSympRed.pdf))


### Homological interpretation of BV-Poisson reduction

* Jim Stasheff, _Homological Reduction of Constrained Poisson Algebras_ ([arXiv](http://arxiv.org/abs/q-alg/9603021))

* Jim Stasheff, _The (secret?) homological algebra of the Batalin-Vilkovisky approach_ ([arXiv](http://arxiv.org/abs/hep-th/9712157))

The latter is NOT in a Poisson context, any more than Lagrangians are only for symplectic manifolds.

##Lagrangian BV

###Idea

* Lagrangian BV-formalism is a means to describe 
[[integration over supermanifolds]] for [[NQ-supermanifolds]] given by $L_\infty$-[[Lie infinity-algebroid|algebroid]]s.
  +-- {: .query}
  Maybe nowadays?, but not originally.  It was meant for
  Lagrangians with symmetries.
  =--
  (Recall that in the physics literature the function algebra of these [[NQ-supermanifolds]] is addressed as the [[BRST complex]].)



The [[path integral]] in [[quantum field theory]] is supposed to be the integral over a space $X$ of field configurations
using a measure $d\mu_S$ which is conceived in the form
$$
  \mu_S(\phi) = \exp(\frac{i}{\hbar} S(\phi)) \mu(\phi)
  \;\;\;\;
  \phi \in X
  \,,
$$
for $\mu$ some other measure and $S : X \to \mathbb{R}$ the _action functional_.

If one thinks of $X$ as an ordinary $(d \lt \infty)$-dimensional smooth manifold, $d\mu_S$ will be given by a volume form, $\mu_S \in \Omega^d(X)$. By contraction of multivector fields with forms, every choice of volume form on $X$ induces an isomorphism between differential forms and multivectors
$$
  \mu : \Omega^\bullet(X) \stackrel{\simeq}{\to}
  \wedge^{-\bullet} \Gamma(T X)
  \,,
$$
which is usefully thought of as reversing degrees. Under this isomorphism the deRham differential maps to a divergence operator conventionally denoted
$$
  \mu : d \mapsto \Delta
$$
which interacts naturally with the canonical bracket on multivector fields: the [Schouten bracket](http://en.wikipedia.org/wiki/Schouten-Nijenhuis_bracket)
This idea can be found recalled for instance on p.3 of Willwacher, Calaque [Formality of cyclic cochains](http://arxiv.org/PS_cache/arxiv/pdf/0806/0806.4095v2.pdf#page=3).

The point to notice now is

* if we think of 

  * the measure $\mu$ as some closed reference differential form on $X$;

  *  the exponentiated action functional $exp(\frac{i}{\hbar}S(-))$ as a multivector field on $X$;

  * the expression $exp(\frac{i}{\hbar}S(-)) \mu$ as the contraction of this multivector field with $\mu$

* then the **BV quantum master equaton**
$\Delta \exp(\frac{i}{\hbar}S) = 0$ says nothing but that
$exp(\frac{i}{\hbar}S(-)) \mu$ is a _closed differential form_.

* If we furthermore take into account that in the presence of gauge symmetries the space $X$ is not a plain manifold but the $L_\infty$-[[Lie infinity-algebroid|algebroid]] of the gauge symmetries acting on the space of fields, hence an [[NQ-supermanifold]] (whose Chevalley-Eilenberg algebra is the **BRST complex**), then this just says that $\exp(\frac{i}{\hbar}S) \mu$ is an [[integration over supermanifolds|integrable form]] in the sense of [[integration over supermanifolds|integration theory of supermanifolds]].

This means that Lagrangian BV formalism is nothing but a way of describing closed differential forms on $L_\infty$-[[Lie infinity-algebroid|algebroid]]s in terms of multivectors contracted into a reference differention form. The multivectors dual to degree 0 elements in the $L_\infty$-[[Lie infinity-algebroid|algebroid]] are the so-called "**anti-fields**", while those dual to the higher degree elements are the so-called "**anti-ghosts**".

### Examples

See [[examples for Lagrangian BV]].


### Relation to groupoid cardinality

There ought to be a close relation between the 
integration over $L_\infty$-[[Lie infinity-algebroid|algebroid]]s using BV-formalism and the notion of [[groupoid cardinality]]
for finite groupoids, which was recently generalized to 
a notion of [[volume of a Lie groupoid]].



## References and related entries

#### Usual BRST (not BV)

* Marc Henneaux, Teitelbaum, _Quantization of gauge systems_, Princeton University Press 1992. xxviii+520 pp.

* [[Glenn Barnich]], Friedemann Brandt, Marc Henneaux, _Local BRST cohomology in gauge theories_, Phys. Rep. __338__ (2000), no. 5, 439&#8211;569, [hep-th/0002245](http://xxx.lanl.gov/abs/hep-th/0002245), <a href="http://dx.doi.org/10.1016/S0370-1573(00)00049-1">doi</a>

#### BV Formalism

* [[homotopy BV algebra]]
* I. Batalin, G. Vilkovisky, _Gauge algebra and quantization_, Phys. Lett. 102B, 27 (1981), _Quantization of gauge theories with linearly dependent
generators_, Phys. Rev. D29, 2567 (1983)
* B. Zwiebach, _Closed string field theory: Quantum action and the B-V master equation_, Nucl. Phys. B 390, 33-152 (1993)
* [[Glenn Barnich]], Friedemann Brandt, Marc Henneaux, _Local BRST cohomology in the antifield formalism. I. General theorems_, [euclid](http://projecteuclid.org/euclid.cmp/1104275094), [MR97c:81186](http://www.ams.org/mathscinet-getitem?mr=97c:81186)

A comprehensive recent review is

* Carlo Albert, Bea Bleile, J&#252;rg Fr&#246;hlich, _Batalin-Vilkovisky integrals in finite dimensions_, [arXiv/0812.0464](http://eprintweb.org/S/article/math-ph/0812.0464)

Geometrical aspects were pioneered in 

* [[Albert Schwarz]], _[[semiclassical approximation|Semiclassical approximation]] in Batalin-Vilkovisky formalism_, Comm. Math. Phys.  __158__ (1993), no. 2, 373--396, [euclid](http://projecteuclid.org/euclid.cmp/1104254246)
* [[Albert Schwarz]], _Semiclassical approximation in Batalin-Vilkovisky formalism_, Comm. Math. Phys.  __158__ (1993), no. 2, 373--396, [euclid](http://projecteuclid.org/euclid.cmp/1104254246)
* M. Alexandrov, [[M. Kontsevich]], A. Schwarz, O. Zaboronsky, _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A 12(7):1405&#8211;1429, 1997, [hep-th/9502010](http://arxiv.org/abs/hep-th/9502010)

Other introductions include

* [[D. Fiorenza]], _An introduction to the Batalin-Vilkovisky formalism_, Lecture given at the Recontres Math&#233;matiques de Glanon, July 2003, [arXiv:math/0402057](http://arxiv.org/abs/math/0402057)

*  [[A. Cattaneo]], _From topological field theory to 
deformation quantization and reduction_, ICM 2006. ([pdf](http://www.math.uzh.ch/fileadmin/math/preprints/icm.pdf))

*  M. B&auml;chtold, _On the finite dimensional BV formalism_, 2005. ([pdf](http://www.math.uzh.ch/reports/04_05.pdf))

The interpretation of the BV quantum master equation as a description of closed differential forms acting as measures on infinite-dimensional spaces of fields is described in

* [[E. Witten]], _A note on the antibracket formalism_, Modern Physics Letters A, __5__, n. 7, 487--494, [MR91h:81178](http://www.ams.org/mathscinet-getitem?mr=91h:81178), [doi](http://dx.doi.org/10.1142/S0217732390000561), [scan](http://ccdb4fs.kek.jp/cgi-bin/img_index?9004090)

* MO: [what is the BV formalism and its uses](http://mathoverflow.net/questions/30352/what-is-the-batalin-vilkovisky-formalism-and-what-are-its-uses-in-mathematics/32443#32443)

[[!redirects BV-theory]]
[[!redirects BV theory]]
[[!redirects BV-BRST formalism]]
[[!redirects BV-BRST quantization]]
[[!redirects BV-BRST quantisation]]
[[!redirects BV/BRST formalism]]
[[!redirects BV/BRST quantization]]
[[!redirects BV/BRST quantisation]]
  
[[!redirects BRST complex]]
[[!redirects BRST-complex]]


[[!redirects BV-BRST complex]]