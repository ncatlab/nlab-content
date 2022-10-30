
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

Recall that a [[TQFT]] is an [[FQFT]] defined on the $(\infty,n)$-[[(infinity,n)-category of cobordisms|category of cobordisms]] whose morphisms are plain cobordisms and diffeomorphisms between these.

In a _conformal_ quantum field theory the cobordisms are equipped with a [[conformal structure]] (a [[Riemannian metric]] structure modulo pointwise rescaling): _[[conformal cobordisms]]_.

A conformal field theory (CFT) is accordingly a functor on such a richer category of conformal [[cobordism]]s.

See the discussion at [[FQFT]] for more details.

The conformally invariant quantum field theories have fields for whom the correlation functions have a specific behaviour accounting for the so called conformal dimension of the fields. This kind of constraints coming from conformal invariance, leads to constraints on the possible shapes of correlation functions; this has being formulated in 1971 by Polyakov as a **bootstrap program**: the conformal invariance should be sufficient to classify consistent conformal QFTs directly from the analysis of symmetries, rather than computing the Feynman integrals from possible actions; this avoids the usual problems with regularization and renormalization. 

Precisely in 2-dimensions is the representation theory of the conformal group exceptionally interesting. In $d \gt 2$, the global transformations, i.e. the elements of the [[conformal group]], are given by the [[Poincare group|Poincare algebra]], dilations and special conformal transformations. In $2$ dimensions, there are additionaly infinitely many local generators of conformal transformations whose commutation relations are given by the [[Virasoro algebra]]. This circumstance enables Belavin, Polyakov and Zamolodchikov to make a breakthrough in the bootstrap program in 1984 (what also helped a 1984-1985 revolution in string theory). 
 There are well-developed tools for handling the theory locally ([[conformal net]]s, [[vertex operator algebra]]s) and at least in the [[rational conformal field theory]] case there are complete classification results for the full theories (defined on cobordisms of all genera).

For this reason often in the literature the term "CFT" often implicitly refers to 2d CFT.

$2$-dimensional conformal field theories have two major applications:

* they describe critical phenomena on surfaces in condensed matter physics;

* they are the building blocks used in [[string theory]]

In the former application it is mostly the _local_ behaviour of the CFT that is relevant. This is encoded in [[vertex operator algebra]]s.

In the [[string theory|string theoretic]] applications the extension of the local theory to a full representation of the 2d [[conformal cobordism category]] is crucial. This extension is called _solving the [[sewing constraints]]_ .

## Abstract ##

In the definition paragraph we will show how to define a conformal field theory using the axiomatic approach of Wightman resp. Osterwalder-Schrader. There are several approaches to axiomatically define conformal field theory, the said approach is not the most "popular" or "elegant" one. There are two reasons to consider the Wightman approach however: If one is already familiar with the Wightman approach, it helps to put conformal field theories into context. The second reason is that several notions often used by physicists can be easily and rigorously defined and explained using this approach. Therefore, it may serve as a bridge between mathematicians and physics literature.    

## 2d CFT on the plane ##

### Definition in Terms of the Osterwalder-Schrader Axioms ###

A definition of conformal field theories can be formulated using the appropriate version of the [[Osterwalder--Schrader axioms]], that is by a system of axioms of the [[correlation functions]]. From the correlation functions it is then possible to deduce the existence of field operators in the sense of the [[Wightman axioms]], that is fields aka field operators are operator valued distributions. Both the Hilbert space and the field operators are therefore not defined in the axioms, but reconstructed from the correlations functions defined in the first three axioms.

Let
$$
M_n := \{(z_1, ..., z_n) \in \mathbb{C}^n : z_i \neq z_j \; \text{for} \; i \neq j  \}
$$
be the **space of configuration points**.
Let $B_0$ be a countable index set and $B := \bigcup_{n \in \mathbb{N}} B_0^{n}$.

The correlation functions are a family $(G_i)_{i \in B}$ of continuous and polynomially bound functions
$$
   G_{i_1, ..., i_n}: M_n \to \mathbb{C} 
$$

+-- {: .un_defn}
###### Axiom 1
**locality**

For all indexes $(i_1, ..., i_n)$, configuration points $(z_1, ..., z_n)$ and permutations $\pi: \{1,..., n \} \to \{1,..., n \}$ one has
$$
G_{(i_1,..., i_n)}(z_1,..., z_n) = G_{(\pi(i_1),..., \pi(i_n))}(\pi(z_1),..., \pi(z_n))
$$
=--

In this context, covariance is meant with respect to the [[Euclidean group]] $E = E_2$.

+-- {: .un_defn}
###### Axiom 2
**covariance**

For every index $i \in B_0$ there are **conformal weights** $h_i, \overline{h_i} \in \mathbb{R}$ ($\overline{h_i}$ is completly independent from $h_i$, it is _not_ the complex conjugate, this notation is widly used in the physics literature so we use it here, too) such that for $n \ge 1$, $w \in E$ and $w_i := w(z_i)$, $h_j := h_{i_j}$ one has
$$
G_{(i_1,..., i_n)}(z_1, \overline{z_i}, ..., z_n, \overline{z_n}) = \prod (\frac{dw}{dz} (z_j))^{h_j} (\overline{\frac{dw}{dz}(z_j)})^{\overline{h_j}}   G_{(i_1,..., i_n)}(w_1, \overline{w_1}..., w_n, \overline{w_n})
$$

=--

The $s_i := h_i - \overline{h_i}$ are called **conformal spin** (for the index $i$) and $d_i := h_i + \overline{h_i}$ is the **scaling dimension**. As an axiom 2.2 we assume that all conformal spins and scaling dimensions are integers.

For the next axiom, which is about reflection positivity, we need some notation:

We write $z \in \mathbb{C}$ as $z = t + iy$ and identify $y$ as the space coordinate and $t$ as (imaginary) time.
So, time reflection $\theta$ is simply:
$$
\theta: \mathbb{C} \to \mathbb{C}
$$

$$
\theta:  z = t + iy \mapsto -t + iy = - \overline{z}
$$

Let $\mathcal{S}(\mathbb{C}^n)$ be the space of [[Schwartz functions]] and

$$
M_n^+ := \{ (z_1, ..., z_n) \in M_n: \operatorname{Re}(z_i) \gt 0 \}
$$

$$
\mathcal{S}_0^+ := \mathbb{C}
$$

$$
\mathcal{S}_n^+ := \{f \in \mathcal{S}(\mathbb{C}^n): \operatorname{Supp}(f) \subset M_n^+ \}
$$

Finally let $\underline{ \mathcal{S}^+ }$ the space of all sequences $\underline{f} = (f_i)_{i \in B}$ with $f_i \in \mathcal{S}_n^+$ fpr $i \in B_0^n$ with only finitely many entries $\ne 0$.

+-- {: .un_defn}
###### Axiom 3
**reflection positivity**

There is a map
$$
*: B_0 \to B_0
$$
with $*^2 = id_{B_0}$ that extends to a map

$$
*: B \to B
$$


$$
*: i \mapsto i^*
$$
so that

1. $G_i(z) = G_{i^*}(\theta(z)) = G_{i^*}(- \overline{z})$

2. $\langle \underline{f}, \underline{f} \rangle \ge 0$ for all $\underline{f} \in \underline{\mathcal{S}^+}$

The scalar product $\langle \underline{f}, \underline{f} \rangle$ is defined as

$$
\sum_{i, j \in B, m, n \in \mathbb{N} } \int_{M_{n+m}} G_{i^* j} (\theta(z_1), ...,\theta(z_n), w_1, ..., w_n) \overline{f_i(z)} f_j(w) d^n z d^m w
$$

=--

+-- {: .un_prop}
###### Proposition
Both a Hilbert space and the field operators of the theory can be (re-) constructed from axioms 1, 2 and 3.

TODO: Details
=--

+-- {: .un_defn}
###### Axiom 4
**scaling covariance**

The correlation functions satisfy the covariance condition also for dilatations $w(z) = e^t (t), t \in \mathbb{R}$.
=--

Explicitly, the last condition says that
$$
G_i(z_1, ..., z_n) = (e^t)^{h_1 + \overline{h_1} +...+ h_n + \overline{h_n}} G_i(e^t(z_1), ..., e^t(z_n))
$$

Given axioms 1-4, the 2-point functions can be fully classified, see below.

+-- {: .un_defn}
###### Axiom 5
**existence of the energy-momentum tensor**

There are four fields $T_{\mu, \nu}, \mu. \nu \in \{0, 1\}$ with the following properties:

Symmetry:
$$
T_{\mu, \nu} = T_{\nu, \mu}, \; T_{\mu, \nu}(z)^* = T_{\nu, \mu}(\theta (z))
$$

$$
\partial_t T_{\mu, 0} + \partial_y T_{\mu, 1} = 0
$$

$T_{\mu, \nu}$ has scaling dimension 2 and the conformal spin $s$ is restricted by
$$
s(T_{00} - T_{11} \pm 2i \; T_{01}) = \pm 2
$$
=--

The energy momentum tensor allows us to define two densly defined operators $L_{-n}, \overline{L_{-n}}$ that both define unitary representations of the [[Virasoro algebra]].

+-- {: .un_prop}
###### Proposition
**L&#252;scher-Mack**

T is holomorphic. Therefore, the operators
$$
L_{-n} := \frac{1}{2 \pi i} \oint_{| \zeta | = 1} \frac{T(\zeta)}{\zeta^{n+1}} d\zeta
$$
and
$$
\overline{L_{-n}} := \frac{1}{2 \pi i} \oint_{| \zeta | = 1} \frac{\overline{T}(\zeta)}{\zeta^{n+1}} d\zeta
$$
are well defined and satisfy the commutation relations of two commuting [[Virasoro algebra|Virasoro algebras]] with the same central charge.
=--

+-- {: .un_defn}
###### Definition
**primary field**

A conformal field $\psi_i, i \in B_0$, is called a primary field if
$$
[L_n, \psi_i] =  z^{n+1} \partial_z \psi_i(z) + h_i (n+1) z^n \psi_i(z)
$$
and likewise for $\overline{z}$.
=--

So, primary fields are the fields whose correlation functions are covariant "infinitesimally" with respect to all holomorphic functions, the "infinitesimal symmetry" expressed in the definition.

The fields are operator valued distributions and cannot be multiplied in general. The possibility of multiplication of fields evaluated at different points and some control of the singularities of this product are part of the axioms of conformal field theory:

+-- {: .un_defn}
###### Pseudodefinition
**operator product expansion**

An operator product expansion (**OPE**) for a family of fields means that there is for all fields and all $z_1 \neq \z_2$ a relation of the form
$$
\psi_i(z_1) \psi_j(z_2) \sim \sum_{k \in B_0} C_{ijk} (z_1 - z_2)^{h_k - h_i - h_j} \psi_k(z_2)
$$

Here $\sim$ means modulo regular functions.
=--

A rigorous interpretation of an OPE would interpret the given relation as a relation of e.g. matrix elements or vacuum expectation values.

An OPE is called **associative** if the expansion of a product of more than two fields does not depend on the order of the expansion of the products of two factors. 
Since the OPE has no interpretation as defining products of operators, or more generally the product in a ring, the notion of associativity does not refer to the associativity of a product in a ring, as the term may suggest.

+-- {: .un_defn}
###### Axiom 6
**existence of associative operator product expansion**

The primary fields have an associative OPE.
=--

Many _formal_ calculations of physicists in CFT involving OPE can be justified by using [[vertex operator algebra]]s, so that [[vertex operator algebra]]s have become a standard way to formulate CFT.

### Properties ###

+-- {: .un_prop}
###### Proposition
Any 2-point function satisfying axioms 1-4 has the following form:
$$
G_{ij}(z_1, z_2) = C_{ij} (z_1 - z_2)^{-(h_i + h_j)} (\overline{z_1} - \overline{z_2})^{-(\overline{h_i} + \overline{h_j})}
$$
with some constant $C_{ij} \in \mathbb{C}$.
=--


## 2d CFT on surfaces or arbitrary genus

...

## Conformal anomaly

The [[Liouville cocycle]] appears when one moves from genuine [[representation]]s of 2-dimensional [[conformal cobordisms]] to [[projective representation|projective representations]]. The obstruction for such a projective representation to be a genuine representation is precisely given by the central charge $c$; when $c\neq 0$, one says that the conformal field theory has a _conformal [[quantum anomaly|anomaly]]_.

...


## CFT in AQFT language

In [[AQFT]] conformal field theory is modeled in terms of [[local net]]s that are [[conformal net]]s.

## Full versus chiral CFT {#FullAndChiral}


> some discussion of full vs. chiral CFT goes here... then:

The following result establishes which pairs of [[vertex operator algebras]] can appear as the left and right chiral parts of a full field algebra in the sense of Huang, Lepowski, [[Liang Kong|Kong]], etc. (see [[vertex operator algebra]]).

+-- {: .un_def}
###### Definition

Two [[modular tensor categories]] are said to have the same **Witt class**
if there exist two [[spherical categories]] $S$ and $T$ such that
we have an [[equivalence of categories|equivalence]] of [[ribbon categories]]

$$
  C \boxtimes \mathcal{Z}(S) \simeq D \boxtimes \mathcal{Z}(T)
$$

=--

Here $\mathcal{Z}(S)$ is the category whose objects are pairs $(Z, z)$ consisting of an
object $Z \in S$ and a [[natural isomorphism]] 
$z_X : Z \otimes X \stackrel{\simeq}{\to} X \otimes Z$, such that for al
objects $X, Y \in S$ we have

$$
  \array{
    Z \otimes X \otimes Y &&\stackrel{z_{X \otimes Y}}{\to}&& 
    X \otimes Y \otimes Z
    \\
    & {}_{\mathllap{z_x \otimes Id}}\searrow && \nearrow_{Id \otimes \mathrlap{z_y^{-1}}}
    \\
    && X \otimes Z \otimes Y
  }
$$

This becomes a monoidal category itself by setting

$$
  (Z,z) \otimes (W,w) := (Z \otimes W, z \otimes w)
  \,.
$$

+-- {: .un_theorem}
###### Theorem
**([[Michael Müger]])**

If $S$ is a [[spherical category]] then $\mathcal{Z}(S)$ is a [[modular tensor category]].

=--

+-- {: .un_theorem}
###### Theorem
**([[Michael Müger]])**


If $C$ is a [[modular tensor category]] then there is an equivalence of 
[[ribbon categories]]

$$
  \mathcal{Z}
  \stackrel{\simeq}{\leftarrow}
  C \boxtimes \bar C
$$

=--


+-- {: .un_theorem}
###### Theorem

Two [[vertex operator algebra]]s $V$ may appear as the left and right chiral 
halfs of a full conformal field theory precisely if their [[modular tensor categories]] of representations have the same
Witt class.

=--


## Examples

* [[Ising model]]

* [[WZW model]]

* [[logarithmic CFT]]

* [[6d (2,0)-supersymmetric QFT]]

## Related concepts

* [[sewing constraints]]

  * [[modular invariance]]

  * [[Cardy condition]]

* [[conformal structure]], [[moduli space of conformal structures]], [[Teichmüller theory]]

* [[conformal transformation]], [[Möbius transformation]]

* [[vertex operator algebra]]

* [[conformal anomaly]]

* [[rational conformal field theory]]

* [[conformal net]]

* [[Liouville cocycle]]

* [[Yangian]]

* [[WZW model]]

  * [[current algebra]], [[affine Lie algebra]]

  * [[Knizhnik-Zamolodchikov connection]]

* [[Liouville theory]]

* [[SCFT]]

  * [[2d SCFT]]

## References ##

### General

The first comprehensive physics textbook on CFT was maybe

* Philippe Di Francesco,Pierre Mathieu,David S&#233;n&#233;chal, _Conformal field theory_, Springer 1997

Introduction and surveys include

* {#Gawedzki99} [[Krzysztof Gaw?dzki]], _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))

* [[Ingo Runkel]], _Boundary problems in conformal field theory_ ([pdf](http://www.math.uni-hamburg.de/home/runkel/PDF/phd.pdf))

* Yu Nakayama, _A lecture note on scale invariance vs conformal invariance_ ([arXiv:1302.0884](http://arxiv.org/abs/1302.0884))

For a survey of perspectives in CFT with an eye towards [[string theory]] see various contributions in 

* [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_


### CFT on the plane

A textbook directed at mathematicians and explaining the "classical" concept of a CFT, i.e. without reference to categories, is this:

* Martin Schottenloher: _A mathematical introduction to conformal field theory_ (2nd edition, [ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1161.17014&format=complete))

A survey of some of the basic manipulationsin chiral CFT, motivated from a [[path integral]] perspective is at

* [[Domenico Fiorenza]], _[[domenicofiorenza:Vertex algebras avant Borcherds]]_

See also the references at [[vertex operator algebra]].


### CFT on complex curves/surfaces of arbitrary genus

For chiral part see

* Edward Frenkel, David Ben-Zvi: _Vertex algebras and algebraic curves_, Math. Surveys and Monographs __88__, AMS 2001,
xii+348 pp. (Bull. AMS. [review](http://www.ams.org/journals/bull/2002-39-04/S0273-0979-02-00955-2/S0273-0979-02-00955-2.pdf), [ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1106.17035&format=complete))

* [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_, Colloqium Publications __51__,  Amer. Math. Soc. 2004, [gbooks](http://books.google.hr/books?id=yHZh3p-kFqQC&lpg=PP1&vq=%22Two-dimensional%20conformal%20geometry%20and%20vertex%20operator%20algebras%22&dq=isbn%3A0817638296&pg=PP1#v=onepage&q=%22Two-dimensional%20conformal%20geometry%20and%20vertex%20operator%20algebras%22&f=false)

### Formulaton by conformal nets

* [[Chris Douglas]], [[André Henriques]], _Topological modular forms and conformal nets_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_

For further references see [[conformal net]].

### Formulation by functors on conformal cobordisms
 {#FQFTReferences}

The idea that CFT should have an axiomatization
as [[FQFT]] -- representations of [[conformal cobordism categories]] for cobordisms equipped with [[conformal structure]] -- was promoted in

* [[Graeme Segal]], 

  _The definition of conformal field theory_, in _Differential geometrical methods in theoretical physics_ (Como, 1987), NATO Adv. Sci. Inst. Ser. C Math. Phys. Sci., 250, Kluwer Acad. Publ., Dordrecht, (1988), 165-171 

  _Two-dimensional conformal field theories and modular functors_ , in _Proceedings of the IXth International Congress on Mathematical Physics_ , Swansea, 1988, Hilger, Bristol (1989) 22-37.

  _The definition of conformal field theory_ , preprint, 1988; also in [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_ , London Math. Soc. Lect. Note Ser., Vol. 308. Cambridge University Press, Cambridge (2004) 421-577. ([pdf](https://people.maths.ox.ac.uk/segalg/0521540496txt.pdf)) 

See also

* [[Richard Blute]], [[Prakash Panangaden]], [[Dorette Pronk]], _Conformal field theory as a nuclear functor_ GDP Festschrift ([pdf](http://aix1.uottawa.ca/~rblute/conf.pdf))

Tentative ideas about a refinement of this to _extended_ ([[2-functor|2-functorial]] CFT) have famously been sketched in 

* [[Stefan Stolz]], [[Peter Teichner]], _[[What is an elliptic object?]]_

Useful related seminar notes are 

* Daniel Evans, _Conformal field theory seminar notes_ ([pdf](http://math.berkeley.edu/~devans/CFT.pdf))


### Formulation by algebra in modular tensor categories
 {#FRSFormalism}

For full CFT, The special case of _rational_ CFT has been essentially entirely formalized and classified. The classification result for full rational 2d CFT was given by Fjelstad--Fuchs--[[Ingo Runkel|Runkel]]--[[Christoph Schweigert|Schweigert]]

* [FRS reviews](http://golem.ph.utexas.edu/string/archives/000747.html)

* [The FRS theorem of RCFT](http://golem.ph.utexas.edu/string/archives/000813.html)



* [[Anton Kapustin]], [[nLab:Natalia Saulina]] _Surface operators in 3d TFT and 2d Rational CFT
_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ ([arXiv:1012.0911](http://arxiv.org/abs/1012.0911))
 {#KapustinSaulina}

* [[Liang Kong]] _Conformal field theory and a new geometry_ , in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ ([arXiv:1107.3649](http://arxiv.org/abs/1107.3649))
 {#Kong}


...

[[!redirects CFT]]
[[!redirects CFTs]]

[[!redirects conformal field theories]]

[[!redirects 2d CFT]]
[[!redirects 2d CFTs]]

[[!redirects 2-dimensional conformal field theory]]
[[!redirects 2-dimensional conformal field theories]]

[[!redirects 2d conformal field theory]]
[[!redirects 2d conformal field theories]]
