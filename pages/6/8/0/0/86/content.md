
> under construction


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

What is called _BRST-BV formalism_ or more specificall the _BRST-BV_ complex is a model in [[dg-geometry]] of a joint [[homotopy theory|homotopical]] [[quotient]] and [[intersection]], hence of an [[(∞,1)-colimit]] and [[(∞,1)-limit]], of  a [[space]] in [[higher geometry]]/[[derived geometry]], in the presence of or induced by [[Poisson structure]].

The motivating applications are 

* homotopical [[symplectic reduction]];

* description of (covariant) [[phase spaces]] of [[gauge theories]].

In both cases one considers a [[space]] $X$ equipped with

1. a [[group]] [[action]] (or more generally a [[groupoid]] or [[∞-groupoid]] action)

   (by a group acting by [[Hamiltonian vector field]]s in the first case, being the [[gauge group]] acting on the space of field configurations in the second case)

1. a [[function]] or more generally [[section]] of some [[vector bundle]]

   (the [[Hamiltonian]] function in the first case, or the [[action functional]] of some [[gauge theory]] in the second)

and wishes to form

1. the [[quotient]] by the group action

1. followed by passage to the 0-locus $\Sigma \hookrightarrow X$ 
   of the function.

Tyically the [[category theory|1-category-theoretic]] version of these operations is ill-behaved and fails to capture the structure of interest in these applications, instead what is required is the [[(∞,1)-category theory|(∞,1)-category-theoretic]] notion of quotient and intersection in [[higher geometry]].

If $X$ is regarded as a space in [[dg-geometry]], the resulting joint homotopical quotient and intersection is modeled by a [[cochain complex]] that generalizes the [[BRST complex]]. This is called the **BV-BRST complex**.


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

is akin to the BV-BRST-complex of a physical system. Roughly, in positive degrees this dg-algebra remembers the [[k-morphism]]s of the $\infty$-groupoid $Conf$, while in negative degrees it remembers the negative degrees of the derived function algebra of the space of objects of the $\infty$-groupoid.

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

More on this at [[function algebras on ∞-stacks]].


## Lagrangian and Hamiltonian version

Much of [[nLab:physics]] is encoded in [[nLab:variational caluclus]]:

given a [[nLab:configuration space]] $C$ of a physical system, an [[nLab:action functional]]

$$
  \exp(i S(-)) : C \to S^1
$$

is specified. Its [[nLab:critical locus]] $C|_\{d S = 0\}$ is the space of physically realized field configurations: this is called the [[nLab:covariant phase space]] or _shell_ .

Typically $S$ is a _local action functional_ in that it is given by integration of a [[nLab:Lagrangian]] functional on the [[nLab:jet space]] of $C$. In this case the covariant phase space is canonically equipped with a [[nLab:presymplectic structure]]. 

In simple cases this may be reduced to a genuine [[nLab:symplectic structure]] on a [[nLab:reduced phase space]]. The study of these is called [[nLab:Hamiltonian mechanics]].

Homotopical incarnations of (covariant) phase spaces and their reduciton is given by [[nLab:BRST-BV complex]]es, which are combinations of [[nLab:BRST complex]]es/[[nLab:Chevalley-Eilenberg algebra]]s and [[nLab:Koszul-Tate resolution]]s.





## Hamiltonian BV
 {#HamiltonianBV}

### Homotopical Poisson reduction
  {#PoissonReduction}

The following is a rough survey of homotopical Poisson reduction, following ([Stasheff 96](#Stasheff96)).

Let $(X, \{-,-\})$ be a [[smooth manifold|smooth]] [[Poisson manifold]]. 

Let $A := C^\infty(X)$ be its [[associative algebra|algebra]] of [[smooth function]]s. 

Consider 

* an [[ideal]] $I \subset A$

* that is closed under the Poisson bracket

  $\{I,I\} \subset$

  (one says we have _first class constraint_ or that 0-locus of $I$ is _coisotropic_)

By the Poisson bracket $I$ acts on $A$. The **Poisson reduction** of $X$ by $I$ is the combined

1. passage to the 0-locus of $I$, which algebraically (dually) is passage to the quotient algebra $A/I$;

1. passage to the quotient of $X$ by the $I$-actioni, which dually is the passage to the invariant subalgebra $A^I$.

This may be achieve in different orders:

The **Sniatycky-Weinstein reduction is the object

$$
  A_{SW} := (A/I)^I
  \,.
$$


The **Dirac reduction** is

$$
  A_{Dirac} := N(I)/I
$$

where $N(I) = \{f \in A | \{f, I\} \subset I\}$ is the "subalgebra of [[observable]]s".

**Proposition** These two algebras are [[isomorphic]]

$$
  A_{red} := A_{SW} \simeq A_{Dirac}
  \,.
$$


**Example** Suppose a [[Lie algebra]] $\mathfrak{g}$ acts on the [[Poisson manifold]] $X$, by [[Hamiltonian vector field]]s. This is equivalently encoded in a [[moment map]] $\mu : X \to \mathfrak{g}^*$. 

Let then $I$ be the [[ideal]] of functions that vanish on $\mu^{-1}(0)$. This is always coisotropic. 

Then $A_{red}$ is the algebraic dual to the preimage $\mu^{-1}(0)$ quotiented by the Lie algebra action: the "constraint surface" quotiented by the symmetries.

In fact, if 0 is a [[regular value]] of $\mu$ then $X_{red} := \mu^{-1}(0)/G$ is a submanifold and

$$
  A_{red} \simeq C^\infty(X_{red})
  \,.
$$ 


We now discuss the BRST-BV complex for the set of constraints $I$ on $(X, \{-,-\})$, which will be a resolution of $A_{red}$ in the following sense:

* instead of forming the [[quotient]] $X/G$ we form the [[action groupoid]] or [[quotient stack]] $X//G$. More precisely we do this for the infinitesimal action and consider a quotient [[Lie algebroid]];

* instead of forming the intersecton $X|_{I = 0}$ we consider its derived locus.

Let $\{T_1, \cdots, T_N\}$ be any finite set of gnerators of the [[ideal]] $I$. Then there exists a non-positively graded [[cochain complex]] on the graded algebra

$$
  A \otimes Sym(V)
  \,,
$$

where $v$ is a [[graded vector space]] in non-positive degree and $Sym(V)$ is its symmetric [[tensor algebra]]: the [[Koszul-Tate resolution]] of $C^\infty(X)/I$.

Then on

$$
  A \otimes Sym(V) \otimes Sym(V^*)
$$

(with $V^*$ in non-negative degree)

there is an evident graded generalization of the Poisson bracket on $A$, which is on $V$ and $V^*$ just the canonical pairing.

Write $\{c^\alpha\}$ for the [[basis]] for $V^*$, called the **ghosts**. Write $\{\pi_\alpha\}$ for the dual basis on $V$, called the **ghost momenta**.

**Theorem** (Henneaux, Stasheff et al.) (**homological perturbaton theory)**

There exists an element 

$$
  \Omega \in A \otimes S(V) \otimes S(V^*)
$$

the **BRST-BV charge** such that

* $\{\Omega, \Omega\} =  0$, so that $(A\otimes S(V) \otimes S(V^*), d := \{\Omega, -\})$ is a [[cochain complex]], in fact a [[dg-algebra]];

* the [[cochain cohomology]] is

  $$
    H^0(A \otimes S(V) \otimes S(V^*), d = \{\Omega, 0\}) = A/I
    \;
  $$

  $$
    H^{\lt 0}(A \otimes S(V) \otimes S(V^*), d = \{\Omega, 0\}) = 0
    \;
  $$

  (which says that this is in non-positivbe degree a resolution of the constraint locus $A/I$)

* If $I$ is a regular ideal (meaing that $V$ can be chosen to be concentrated in degree 1) or the vanishing ideal of a coisotropic submanifold, then the cohomology in positive degree 


  $$
    H^{\bullet \geq 0}(A \otimes S(V) \otimes S(V^*), d = \{\Omega, 0\})
    \simeq
    H^\bullet(CE(A/I, I/I^2))
  $$

  is isomorphic to the [[infinity-Lie algebra cohomology|Lie algebroid cohomology]] of the [[Lie algebroid]] whose [[Lie-Rinehart algebra]] is $(A/I, I/I^2)$

  (which says that in positive degree the BRST-BV complex is a resolution of the [[action Lie algebroid]] of $\{I,-\}$ acting on $X$).


**Theorem** (Oh-Park, Cattaneo-Felder) If $C \subset X$ is coisotropic, there is an [[L-infinity algebra]]-structure on $\wedge^\bullet  \Gamma(N C)$ such that the induced bracket on $H^0 = A_{red}$ is the given one;

**Theorem** (Sch&#228;tz) The BRST-BV complex with $\{-,-\}$ as its Lie bracket is [[quasi-isomorphism|quasi-isomorphic]] to the above.


## Lagrangian BV
 {#LagrangianBV}


Under the identification of 
[[nLab:Hochschild homology]]/[[nLab:cyclic homology]] with 
the [[nLab:de Rham complex]] the product of the 
[[nLab:action functional]] 
$\exp(i S(-)) : C \to S^1$ with a formal [[nLab:measure]] $vol$
on $C$ is regarded as cycle in [[nLab:cyclic homology]]. Or rather, 
an isomorphism with [[nLab:Hochschild cohomology]] is picked,
interpreted as a choice of [[nLab:volume form]] $vol$ and 
$\exp(i S(-))$ is regarded as a cocycle in cyclic cohomology, hence
as a [[nLab:multivector field]] whose closure condition

$$
  \Delta \exp(i S(-)) = 0
$$ 

is called the _master equation_ of BV-formalis.

By the identification of [[nLab:Hochschild cohomology]]  
with functions on [[nLab:derived loop space]]s we know that 
the operator $\Delta$ encodes the rotation of loops. 
Accordingly, the resuling [[nLab:BV-algebra]] has an interpretation
as an algebra over (the homology of) the 
[[nLab:framed little disk operad]]. This we discuss 
[below](#BVAlgebra).


### The BV-Laplacian as a dualized exterior differential

We indicate how the [[BV-algebra]] appearing in Lagrangian BV-formalism is the dual of the [[de Rham complex]] of [[configuration space]] in the presence of a [[volume form]]. (This observation goes back to [Witten90](#Witten90)).

The [[path integral]] in [[quantum field theory]] is supposed to be the integral over a field [[configuration space]] $X$ using a [[measure]] $\mu_S$ which is conceived in the form

$$
  \mu_S(\phi) = \exp(\frac{i}{\hbar} S(\phi)) \mu(\phi)
  \;\;\;\;
  \phi \in X
  \,,
$$

for $\mu$ some other measure and $S : X \to \mathbb{R}$ the _[[action functional]]_.

If one thinks of $X$ as an ordinary $(d \lt \infty)$-[[dimension]]al [[smooth manifold]], $d\mu_S$ will be given by a [[volume form]], $\mu_S \in \Omega^d(X)$. By contraction of [[multivector field]]s with forms, every choice of volume form on $X$ induces an [[isomorphism]] between [[differential form]]s and [[polyvector field]]s

$$
  \mu : \Omega^\bullet(X) \stackrel{\simeq}{\to}
  \wedge^{-\bullet} \Gamma(T X)
  \,,
$$

which is usefully thought of as reversing degrees. Under this isomorphism the deRham differential maps to a divergence operator conventionally denoted

$$
  \mu : d \mapsto \Delta
$$

which interacts naturally with the canonical bracket on multivector fields: the [[Schouten bracket]]. (See [[polyvector field]] for more details.)

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



## Related concepts

* [[BRST complex]]

* [[homotopy BV algebra]]

## References

The original articles are

* I. Batalin, G. Vilkovisky,  _Gauge Algebra and Quantization_ . Phys. Lett. B 102 (1): 27&#8211;31. doi:10.1016/0370-2693(81)90205-7 (1981)
{#BV81}

* I. Batalin,G. Vilkovisky,  (1983). _Quantization of Gauge Theories with Linearly Dependent Generators_ . Phys. Rev. D 28 (10): 2567&#8211;2582. doi:10.1103/PhysRevD.28.2567.  Erratum-ibid. 30 (1984) 508 doi:10.1103/PhysRevD.30.508
{#BV83}

BRST formalism is discussed in 

* [[Glenn Barnich]], Friedemann Brandt, [[Marc Henneaux]], _Local BRST cohomology in gauge theories_, Phys. Rep. __338__ (2000), no. 5, 439&#8211;569, [hep-th/0002245](http://xxx.lanl.gov/abs/hep-th/0002245), <a href="http://dx.doi.org/10.1016/S0370-1573(00)00049-1">doi</a>

Homological Poisson reduction is discussed in 

* [[Jim Stasheff]], _Homological Reduction of Constrained Poisson Algebras_ ([arXiv](http://arxiv.org/abs/q-alg/9603021))
{#Stasheff96}

A standard textbook on the application of BRST-BV to [[gauge theory]] is

* [[Marc Henneaux]], [[Claudio Teitelboim]], _Quantization of gauge systems_, Princeton University Press 1992. xxviii+520 pp.

* [[Glenn Barnich]], Friedemann Brandt, [[Marc Henneaux]], _Local BRST cohomology in the antifield formalism. I. General theorems_, [euclid](http://projecteuclid.org/euclid.cmp/1104275094), [MR97c:81186](http://www.ams.org/mathscinet-getitem?mr=97c:81186)

Another review is

* Carlo Albert, Bea Bleile, J&#252;rg Fr&#246;hlich, _Batalin-Vilkovisky integrals in finite dimensions_, [arXiv/0812.0464](http://eprintweb.org/S/article/math-ph/0812.0464)

Geometrical aspects were pioneered in 

* [[Albert Schwarz]], _[[semiclassical approximation|Semiclassical approximation]] in Batalin-Vilkovisky formalism_, Comm. Math. Phys.  __158__ (1993), no. 2, 373--396, [euclid](http://projecteuclid.org/euclid.cmp/1104254246)
* [[Albert Schwarz]], _Semiclassical approximation in Batalin-Vilkovisky formalism_, Comm. Math. Phys.  __158__ (1993), no. 2, 373--396, [euclid](http://projecteuclid.org/euclid.cmp/1104254246)
* M. Alexandrov, [[M. Kontsevich]], A. Schwarz, O. Zaboronsky, _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A 12(7):1405&#8211;1429, 1997, [hep-th/9502010](http://arxiv.org/abs/hep-th/9502010)

Other introductions include

* [[Domenico Fiorenza]], _An introduction to the Batalin-Vilkovisky formalism_, Lecture given at the Recontres Math&#233;matiques de Glanon, July 2003, [arXiv:math/0402057](http://arxiv.org/abs/math/0402057)

*  [[A. Cattaneo]], _From topological field theory to 
deformation quantization and reduction_, ICM 2006. ([pdf](http://www.math.uzh.ch/fileadmin/math/preprints/icm.pdf))

*  M. B&auml;chtold, _On the finite dimensional BV formalism_, 2005. ([pdf](http://www.math.uzh.ch/reports/04_05.pdf))

A discussion of BV-BRST formalism in the general context of [[perturbative quantum field theory]] is in

* [[Kevin Costello]], _[[Renormalization and Effective Field Theory]]_

The interpretation of the BV quantum master equation as a description of closed differential forms acting as measures on infinite-dimensional spaces of fields is described in

* [[Edward Witten]], _A note on the antibracket formalism_, Modern Physics Letters A, __5__, n. 7, 487--494, [MR91h:81178](http://www.ams.org/mathscinet-getitem?mr=91h:81178), [doi](http://dx.doi.org/10.1142/S0217732390000561), [scan](http://ccdb4fs.kek.jp/cgi-bin/img_index?9004090)
{#Witten90}


* MO: [what is the BV formalism and its uses](http://mathoverflow.net/questions/30352/what-is-the-batalin-vilkovisky-formalism-and-what-are-its-uses-in-mathematics/32443#32443)

 * _Basics of Poisson reduction_ ([blog](http://golem.ph.utexas.edu/category/2008/07/poisson_reduction.html))

 * Alejandro Cabrera, _Homological BV-BRST methods: from QFT to Poisson reduction_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Charla_IMPA_BRST.pdf))

 * [[Jeremy Butterfield]], _On symplectic reduction in classical mechanis_ ([pdf](http://philsci-archive.pitt.edu/archive/00002373/01/ButterfieldNHSympRed.pdf))

The application in [[string theory]]/[[string field theory]] is discussed in

* B. Zwiebach, _Closed string field theory: Quantum action and the B-V master equation_, Nucl. Phys. B 390, 33-152 (1993)



Remark  on the [[homotopy theory]] interpretation of BRST-BV are in


* [[Jim Stasheff]], _The (secret?) homological algebra of the Batalin-Vilkovisky approach_ ([arXiv](http://arxiv.org/abs/hep-th/9712157))

The latter is NOT in a Poisson context, any more than Lagrangians are only for symplectic manifolds.




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
[[!redirects BRST-BV complex]]
[[!redirects BV-BRST complexes]]
[[!redirects BRST-BV complexes]]


[[!redirects BRST-BV formalism]]

[[!redirects symplectic reduction]]
[[!redirects Poisson reduction]]