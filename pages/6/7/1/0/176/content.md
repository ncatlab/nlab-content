+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic QFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functorial QFT
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

A conformal field theory (CFT) is accordingly a functor on such a richer category of conformal [[cobordisms]]. See the discussion at [[FQFT]] for more details.

The conformally invariant quantum field theories have fields for whom the [[correlation functions]] have a specific behaviour accounting for the _conformal dimension_ of the [[field (physics)|fields]]. This kind of constraints coming from conformal invariance, leads to constraints on the possible behaviour of correlation functions; this has being formulated in 1971 by Polyakov as a **[[conformal bootstrap]]** program: the conformal invariance should be sufficient to classify consistent conformal QFTs directly from the analysis of symmetries, rather than computing the [[Feynman diagram]] [[perturbation series]] from some [[action functional]]; this avoids the usual problems with regularization and [[renormalization]]. 

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

+-- {: .num_defn}
###### Axiom 1
**locality**

For all indexes $(i_1, ..., i_n)$, configuration points $(z_1, ..., z_n)$ and permutations $\pi: \{1,..., n \} \to \{1,..., n \}$ one has
$$
G_{(i_1,..., i_n)}(z_1,..., z_n) = G_{(\pi(i_1),..., \pi(i_n))}(\pi(z_1),..., \pi(z_n))
$$
=--

In this context, covariance is meant with respect to the [[Euclidean group]] $E = E_2$.

+-- {: .num_defn}
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

+-- {: .num_defn}
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

+-- {: .num_prop}
###### Proposition
Both a Hilbert space and the field operators of the theory can be (re-) constructed from axioms 1, 2 and 3.

TODO: Details
=--

+-- {: .num_defn}
###### Axiom 4
**scaling covariance**

The correlation functions satisfy the covariance condition also for dilatations $w(z) = e^t (t), t \in \mathbb{R}$.
=--

Explicitly, the last condition says that
$$
G_i(z_1, ..., z_n) = (e^t)^{h_1 + \overline{h_1} +...+ h_n + \overline{h_n}} G_i(e^t(z_1), ..., e^t(z_n))
$$

Given axioms 1-4, the 2-point functions can be fully classified, see below.

+-- {: .num_defn}
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

+-- {: .num_prop}
###### Proposition
**[Lüscher & Mack 1975](#LüscherMack75)**

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

+-- {: .num_defn}
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

+-- {: .num_defn}
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

+-- {: .num_defn}
###### Axiom 6
**existence of associative operator product expansion**

The primary fields have an associative OPE.
=--

Many _formal_ calculations of physicists in CFT involving OPE can be justified by using [[vertex operator algebra]]s, so that [[vertex operator algebra]]s have become a standard way to formulate CFT.

### Properties ###

+-- {: .num_prop}
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


## Full versus chiral CFT 
 {#FullAndChiral}


> some discussion of full vs. chiral CFT goes here... then:

The following result establishes which pairs of [[vertex operator algebras]] can appear as the left and right chiral parts of a _[[full field algebra]]_ in the sense of ([Huang-Kong 05](#HuangKong05)), etc. (see [[vertex operator algebra]]).

+-- {: .num_defn}
###### Definition

Two [[modular tensor categories]] $C$ and $D$ are said to have the same **Witt class** if there exist two [[spherical categories]] $S$ and $T$ such that we have an [[equivalence of categories|equivalence]] of [[ribbon categories]]

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

+-- {: .num_theorem}
###### Theorem
**([[Michael Müger]])**

If $S$ is a [[spherical category]] then $\mathcal{Z}(S)$ is a [[modular tensor category]].

=--

\begin{theorem}
**([[Michael Müger]])**

If $C$ is a [[modular tensor category]] then there is an [[equivalence of categories|equivalence]] of [[ribbon categories]]

\[
  \label{IdentifyingTheDrinfeldCenter}
  \mathcal{Z}
  \stackrel{\simeq}{\leftarrow}
  C \boxtimes \bar C
\]

\end{theorem}

\begin{remark}\label{IdentifyingTheDrinfeldCenter}

1. An explicit [[inverse functor]] for (eq:IdentifyingTheDrinfeldCenter) is given by [Guu & Tham 2021](modular+tensor+category#GuuTham21) using [[string diagram|graphical calculus]]. 

1. The functor (eq:IdentifyingTheDrinfeldCenter) exists also for the non-modular case, but it is then just an [[ambidextrous adjunctions|ambidextrous adjoint]].

\end{remark}


## Examples

* [[Ising model]]

* [[WZW model]]

* [[parafermion]]

* [[logarithmic CFT]]

* [[Brownian loop soup]]

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

* [[minimal model CFT]]

* [[Gepner model]], [[WZW model]]

* [[conformal net]]

* [[Liouville cocycle]]

* [[Yangian]]

* [[WZW model]]

  * [[current algebra]], [[affine Lie algebra]]

  * [[Knizhnik-Zamolodchikov connection]]

* [[Liouville theory]]

* [[SCFT]]

  * [[2d SCFT]]

* [[boundary conformal field theory]]

* [[automorphism of a 2d conformal field theory]]

* [[TT deformation]]



## References ##

### General

The mathematical axioms of CFT, as well as its relevance for surface phenomena goes back to

* [[Alexander Belavin]], [[Alexander Polyakov]], [[Alexander Zamolodchikov]], _Infinite conformal symmetry in two–dimensional quantum field theory_, Nuclear Physics B Volume 241, Issue 2, 23 July 1984, Pages 333-380 (<a href="https://doi.org/10.1016/0550-3213(84)90052-X">doi:10.1016/0550-3213(84)90052-X</a>)

Monographs:

* [[Philippe Di Francesco]], Pierre Mathieu, David Sénéchal: *Conformal field theory*, Springer (1997) &lbrack;[doi:10.1007/978-1-4612-2256-9](https://doi.org/10.1007/978-1-4612-2256-9)&rbrack;

* [[Martin Schottenloher]]: *A Mathematical Introduction to Conformal Field Theory*, Lecture Notes in Physics **759**, Springer (2008) &lbrack;[doi:10.1007/978-3-540-68628-6](https://link.springer.com/book/10.1007/978-3-540-68628-6), [web](https://www.mathematik.uni-muenchen.de/~schotten/LNP-cft-pdf/)&rbrack;

See also:

* {#LüscherMack75} [[Martin Lüscher]], [[Gerhard Mack]]: *Global Conformal Invariance in Quantum Field Theory*, Comm. Math. Phys. **41** 3  (1975) 203-234 &lbrack;[doi:10.1007/BF01608988](https://doi.org/10.1007/BF01608988), [jstor:cmp/1103898909](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-41/issue-3/Global-conformal-invariance-in-quantum-field-theory/cmp/1103898909.full), [inspire:90687](https://inspirehep.net/literature/90687)&rbrack;



With emphases on [[braid group representations]] constituted by [[conformal blocks]] via the [[Knizhnik-Zamolodchikov equation]]:

* [[Toshitake Kohno]], *Conformal field theory and topology*, transl. from the 1998 Japanese original by the author. Translations of Mathematical Monographs __210__. Iwanami Series in Modern Mathematics. Amer. Math. Soc. (2002) &lbrack;[AMS:mmono-210](https://bookstore.ams.org/mmono-210)&rbrack;


Introduction and surveys:

* [[Paul Ginsparg]], *Applied Conformal Field Theory*, lectures at: *[Fields, strings, critical phenomena, Les Houche Summer School 1988](https://inis.iaea.org/search/search.aspx?orig_q=RN:21047524)([arXiv:hep-th/9108028](https://arxiv.org/abs/hep-th/9108028))

* {#Gawedzki99} [[Krzysztof Gawedzki]], _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))

* [[Ingo Runkel]], _Boundary problems in conformal field theory_ ([pdf](http://www.math.uni-hamburg.de/home/runkel/PDF/phd.pdf))

* [[Ralph Blumenhagen]], [[Erik Plauschinn]], *Introduction to Conformal Field Theory -- With Applications to String Theory*, Lecture Notes in Physics **779**, Springer (2009) &lbrack;[doi:10.1007/978-3-642-00450-6](https://doi.org/10.1007/978-3-642-00450-6)&rbrack;

* Yu Nakayama, _A lecture note on scale invariance vs conformal invariance_, [arXiv:1302.0884](http://arxiv.org/abs/1302.0884)

* [[Christoph Schweigert]]: *Introduction to conformal field theory*, lecture notes (2013/14) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schweigert/skripten/cftskript.pdf)&rbrack;

* [[Katrin Wendland]], _Snapshots of Conformal Field Theory_, in: *Mathematical Aspects of Quantum Field Theories*, Mathematical Physics Studies, Springer (2015)  &lbrack;[arXiv:1404.3108](http://de.arxiv.org/abs/1404.3108), [doi:10.1007/978-3-319-09949-1_4](https://doi.org/10.1007/978-3-319-09949-1_4)&rbrack;

* [[Hans Jockers]] (notes by Walker Stern): *Conformal Field Theory*, lecture notes (2016) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/stern/Notes/CFT/Notes_CFT.pdf)&rbrack;

* [[Bert Schellekens]]: *Conformal Field Theory*, lecture notes (2017) &lbrack;[pdf](https://www.nikhef.nl/~t58/CFT.pdf)&rbrack;

* [[Jörg Teschner]], _A guide to two-dimensional conformal field theory_ &lbrack;[arXiv:1708.00680](http://arxiv.org/abs/1708.00680)&rbrack;

* Joaquin Liniado, *Two Dimensional Conformal Field Theory and a Primer to Chiral Algebras* ([arXiv:2110.15164](https://arxiv.org/abs/2110.15164))

* Marc Gillioz, *Conformal field theory for particle physicists* &lbrack;[arXiv:2207.09474](https://arxiv.org/abs/2207.09474)&rbrack;

* Satoshi Nawata, Runkai Tao, Daisuke Yokoyama, *Fudan lectures on 2d conformal field theory* &lbrack;[arXiv2208.05180](https://arxiv.org/abs/2208.05180)&rbrack;

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Simon Wood]], [[Yang Yang]], *Algebraic structures in two-dimensional conformal field theory*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2305.02773](https://arxiv.org/abs/2305.02773)&rbrack;

* Andrew M. Evans, Alexandra Miller, Aaron Russell, *A Conformal Field Theory Primer in $D \geq 3$* &lbrack;[arXiv:2309.10107](https://arxiv.org/abs/2309.10107)&rbrack;

* Christian Northe: *Young Researchers School 2024 Maynooth: Lectures on CFT, BCFT and DCFT* &lbrack;[arXiv:2411.03381](https://arxiv.org/abs/2411.03381)&rbrack;


* [[Pavel Mnev]]: *Lecture notes on conformal field theory* &lbrack;[arXiv:2501.06616](https://arxiv.org/abs/2501.06616)&rbrack;



Discussion of mathematical formalization ([[vertex operator algebras]], [[conformal nets]], [[functorial QFT]]) see

* {#Tener18} James E. Tener, _Representation theory in chiral conformal field theory: from fields to observables_ ([arXiv:1810.08168](https://arxiv.org/abs/1810.08168))

* {#HuangKong05} [[Yi-Zhi Huang]], [[Liang Kong]], _Full field algebras_, Commun.Math.Phys.272:345-396,2007 ([arXiv:0511328](http://arxiv.org/abs/math/0511328))

* [[Liang Kong]], _Full field algebras, operads and tensor categories_, Adv. Math.213:271-340, 2007 ([arXiv:0603065](http://arxiv.org/abs/math/0603065))


For a survey of perspectives in CFT with an eye towards [[string theory]] see various contributions in 

* [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_

Discussion in relation to the [[AdS-CFT correspondence]]:

* Matteo Broccoli, *Aspects of Conformal Field Theory* &lbrack;[arXiv:2212.11829](https://arxiv.org/abs/2212.11829)&rbrack;

* Yuya Kusuki: *Modern Approach to 2D Conformal Field Theory* &lbrack;[arXiv:2412.18307](https://arxiv.org/abs/2412.18307)&rbrack;

See also:

* [[Sylvain Ribault]]: *Exactly solvable conformal field theories* &lbrack;[arXiv:2411.17262](https://arxiv.org/abs/2411.17262)&rbrack;



### CFT on complex curves/surfaces of arbitrary genus

For chiral 2d CFT:

* [[Edward Frenkel]], [[David Ben-Zvi]]: _Vertex algebras and algebraic curves_, Math. Surveys and Monographs __88__, AMS (2001) (Bull. AMS. [review](http://www.ams.org/journals/bull/2002-39-04/S0273-0979-02-00955-2/S0273-0979-02-00955-2.pdf), [ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1106.17035&format=complete))

* [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_, Colloqium Publications __51__,  Amer. Math. Soc. 2004, [gbooks](http://books.google.hr/books?id=yHZh3p-kFqQC&lpg=PP1&vq=%22Two-dimensional%20conformal%20geometry%20and%20vertex%20operator%20algebras%22&dq=isbn%3A0817638296&pg=PP1#v=onepage&q=%22Two-dimensional%20conformal%20geometry%20and%20vertex%20operator%20algebras%22&f=false)

### Formulation by conformal nets

* [[Chris Douglas]], [[André Henriques]], _Topological modular forms and conformal nets_, in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_

For further references see [[conformal net]].


### Formulation in full AQFT

Formulation in full [[AQFT on curved spacetimes]]:

* [[Marco Benini]], [[Luca Giorgetti]], [[Alexander Schenkel]], *A skeletal model for 2d conformal AQFTs* ([arXiv:2111.01837](https://arxiv.org/abs/2111.01837))



[[!include D=2 CFT a functorial field theory -- references]]





### Formulation by algebra in modular tensor categories
 {#FRSFormalism}

For full CFT, The special case of _rational_ CFT has been essentially entirely formalized and classified. The classification result for full rational 2d CFT was given by Fjelstad--Fuchs--[[Ingo Runkel|Runkel]]--[[Christoph Schweigert|Schweigert]]

* [FRS reviews](http://golem.ph.utexas.edu/string/archives/000747.html)

* [The FRS theorem of RCFT](http://golem.ph.utexas.edu/string/archives/000813.html)

* {#KapustinSaulina} [[Anton Kapustin]], [[Natalia Saulina]]: *Surface operators in 3d TFT and 2d Rational CFT*, in: [[Hisham Sati]], [[Urs Schreiber]] (eds.), *[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]*, Proceedings of Symposia in Pure Mathematics **83**, AMS (2011) &lbrack;[arXiv:1012.0911](http://arxiv.org/abs/1012.0911), [ams:pspum-83](https://bookstore.ams.org/pspum-83)&rbrack;
 
* {#Kong} [[Liang Kong]]: *Conformal field theory and a new geometry*, in: [[Hisham Sati]], [[Urs Schreiber]] (eds.), *[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]*, Proceedings of Symposia in Pure Mathematics **83**, AMS (2011) &lbrack;[arXiv:1107.3649](http://arxiv.org/abs/1107.3649), [ams:pspum-83](https://bookstore.ams.org/pspum-83)&rbrack;
 


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

[[!redirects 2D conformal field theory]]
[[!redirects 2D conformal field theories]]


[[!redirects D=2 conformal field theory]]
[[!redirects D=2 conformal field theories]]

[[!redirects D=2 CFT]]
[[!redirects D=2 CFT]]


[[!redirects D=2 CFT]]


[[!redirects conformal weight]]
[[!redirects conformal weights]]


