


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of *formal deformation quantization* (often taken to be the default notion of *[[deformation quantization]]*) is one formalization of the general idea of [[quantization]] of a [[classical mechanical system]]/[[classical field theory]] to a [[quantum mechanical system]]/[[quantum field theory]], at least [[perturbative quantum field theory|perturbatively]] in small (really: [[infinitesimal]]) values of [[Planck's constant]] $\hbar$.

Formal deformation quantization focuses on the [[algebras of observables]] of a physical system (hence on the [[Heisenberg picture]]): it provides rules for how to [[deformation theory|deform]] the commutative algebra of classical observables to a non-commutative algebra of quantum observables. (This is in contrast to [[geometric quantization]], which focuses on the [[spaces of states]] and hence on the [[Schrödinger picture]].)

Usually and traditionally, _[[deformation quantization]]_ refers to (just) _formal_ deformations, in the sense that it produces [[formal power series]] expansions in a formal parameter $\hbar$ (physically: [[Planck's constant]]) of the product in the deformed algebra of observables.

| [[classical mechanics]] | [[semiclassical approximation]] |  ... | [[formal deformation quantization]] | [[quantum mechanics]] |
|--|--|--|--|--|
| $\mathcal{O}(\hbar^0)$ | $\mathcal{O}(\hbar^1)$ | $\mathcal{O}(\hbar^n)$ | $\mathcal{O}(\hbar^\infty)$  |  |

(This is related to [[perturbation theory]], which is about [[formal power series]] in [[coupling constants]], instead of in [[Planck's constant]].)


But there are refinements of this to [[C-star algebraic deformation quantization]] which studies the proper deformation to a genuine [[C-star algebra]] of observables. (This in turn is related to genuine [[geometric quantization]] via the notion of [[geometric quantization of symplectic groupoids]].)

One can, therefore, argue that only [[C-star algebraic deformation quantization|strict deformation quantization]] is genuine [[quantization]]. For instance in ([Gukov-Witten 09, section 1.4](#GukovWitten09)) it says

> Generally speaking, [[physics]] is based on $[$ strict $]$ quantization, rather than $[$ formal $]$ deformation quantization, although conventional quantization sometimes leads to problems that can be treated by deformation quantization.


As other methods of quantization, deformation quantization has as input a description of a [[classical mechanical system]], which is in this case most often a smooth [[Poisson manifold]]. The deformation quantization replaces the algebra of [[smooth functions]] on the Poisson manifold with the same [[vector space]], but equipped with new noncommutative [[associative algebra|associative unital product]] whose [[commutator]] agrees, up to order $\hbar$, with the underlying [[Poisson bracket]]. Of course the proper study of quantization of Poisson manifolds studied the appropriate notion at the level of [[sheaves]] of algebras. Gluing local solutions to the quantization problem furthermore involves [[stacks]] and specifically [[gerbes]].

## Definition

If the result of deformation quantization is an algebra over the [[power series]] [[ring]] $\mathbb{R}[ [ \hbar ] ]$ of a formal parameter $\hbar$ (thought of as [[Planck's constant]]) such that the limit $\hbar \to 0$ reproduces the starting point of the deformation, then one speaks of

* [Formal deformation quantization](#FormalDeformationQuantization)

In much of the literature this is regarded as the default meaning of "deformation quantization". But this is really the case corresponding to [[perturbation theory]] in [[quantum field theory]]. A "genuine" or "strict" deformation quantization

* [Strict deformation quantization](#StrictDeformationQuantization)

is supposed to result in a non-formal deformation, which in terms of the above formal power series at least means that one can set $\hbar = 1$ such that all expressions in $\hbar$ converge, but which in general is taken to mean something stronger, such as that there is a continuous field of [[C-star algebraic deformation quantization]].


### Formal deformation quantization
 {#FormalDeformationQuantization}

We first give the traditional

* [Explicit definition of traditional deformation quantization](#ExplicitDefinitionOfTraditionalDeformationQuantization)

of a [[Poisson manifold]]/[[Poisson algebra]]. Thought of in terms of [[physics]] this describes a [[quantization]] of a [[physical system|system]] of [[quantum mechanics]], as opposed to full [[quantum field theory]].

More abstractly, this may be formulated and generalized in terms of lifts of [[algebras over an operad]] over a [[P-n operad]] to a [[BD-n operad]] and hence an [[E-n operad]], for $n = 1$. This we discuss in

* [Formulation as lifts from P-n algebras to BD-n algebras](#FormulationAsLiftsFromPnAlgebrasToBDAlgebras)

In this formulation one sees that for genral $n$ the construction applies  to $n$-dimensional [[quantum field theory]] (with [[quantum mechanics]] for $n = 1$ be 1-dimensional quantum field theory, for instance the [[sigma-model]] "on the [[worldline]]" of a [[particle]]). A formulation of deformation quantization to _[[local quantum field theory|local]]_ quantum field theory formulated in terms of [[factorization algebras of observables]] over [[spacetime]]/[[worldvolume]] is indicated in ([Costello-Gwilliam, chapter 5](#CostelloGwilliam)).


#### Explicit definition of deformation of Poisson manifolds/Poisson algebras
 {#ExplicitDefinitionOfTraditionalDeformationQuantization}

Let $M$ be a [[Poisson manifold]] and let $A = C^\infty(M)$ be the [[Poisson algebra]] of smooth functions.

+-- {: .num_defn}
###### Definition
A **$\ast$-product** ([[star product]]) on $A$ is a product on the
[[power series]] $A [ [ t ] ]$ that is (1) bilinear over $\mathbb{R}[ [ t ] ]$, (2) associative, and (3) for $a,b \in A$ it can be written out as a [[formal power series]]
\[ a \ast b = \sum_{n=0}^\infty B_n(a,b) t^n \]
where $B_n$ are bilinear maps on $A$ such that $B_0(a,b) = ab$.
=--

+-- {: .num_defn}
###### Definition
A (formal) **deformation quantization** of $M$ is a [[star product]] on $A = C^\infty(M)$ such that the [[Poisson bracket]] $\{a,b\} = B_1(a,b) - B_1(b,a)$ for $a,b \in A$; by bilinearity over $\mathbb{R}[ [ t ] ]$, this characterizes it.
=--


#### Formulation as lifts from $P_n$-algebras to $BD_n$-algebras and $E_n$-algebras
 {#FormulationAsLiftsFromPnAlgebrasToBDAlgebras}

(...)

([Costello-Gwilliam, section 2.3, 2.4](#CostelloGwilliam))

(...)

[[!include deformation quantization - table]]

#### Deformation quantization in perturbative quantum field theory
 {#InPerturbativeQuantumFieldTheory}

Deformation quantization in [[perturbative quantum field theory]] is discussed for [[free field theory]] via [[Moyal deformation quantization]] yielding [[Wick algebras]] in ([D&#252;tsch-Fredenhagen 00](#DuetschFredenhagen00), [Hirschfeld-Henselder 02](#HirschfeldHenselder02)), 
and for interacting [[perturbative quantum field theory]] ([[perturbative AQFT]]) via [[Fedosov deformation quantization]]
in ([Collini 16](#Collini16)), see also ([Hawkins-Rejzner 16](#HawkinsRejzner16)).



### Strict deformation quantization
 {#StrictDeformationQuantization}

(...)
[[C-star algebraic deformation quantization]]
(...)

## Properties

### Existence results

[[Vladimir Drinfel'd]] has sketched a proof (and gave main ingredients) to show that every [[Poisson Lie group]] can be deformation quantized to a [[Hopf algebra]]; this proof has been completed by Etingof and Kazhdan. [[Maxim Kontsevich]] proved a certain *[[Kontsevich formality|formality theorem]]* (formality is here in the sense of _[[formal dg-algebra]]_ in [[rational homotopy theory]]) whose main corollary (and motivation) was the statement that every [[Poisson manifold]] has a deformation quantization ([Kontsevich 97](#Kontsevich97)).

For [[symplectic manifolds]] and those [[Poisson manifolds]] that have a [[regular foliation]] by [[symplectic leafs]], the theory of deformation quantization is much simpler; [[Boris Fedosov]] gave a construction of [[star products]] on symplectic manifolds using [[symplectic connections]] on [[smooth manifolds]] ([Fedosov 94](#Fedosov94)), see at _[[Fedosov's deformation quantization]]_.  An analogous argument was given by [[Roman Bezrukavnikov]] and [[Dmitry Kaledin]] in the context of an algebraic symplectic form ([BK 04](#BK)).

+-- {: .standout}
Caution: the following are rough notes from a talk by [[J.D.S. Jones]] (Cambridge, 8.1.2013); there are probably many typos and sign errors.
=--

#### Deformation of Poisson manifolds


+-- {: .num_theorem #Kontsevich}
###### Theorem
**(Kontsevich)**.  Every [[Poisson manifold]] has a (formal) deformation quantization.

=--

This was shown in ([Kontsevich 97](#Kontsevich97)). There the deformed product is constructed by a kind of [[Feynman diagram]] [[perturbation series]]. Later this was identified as the perturbation series of the [[Poisson sigma-model]] for the given Poisson manifold. See there for more details.






#### Deformation of Algebraic Varieties ####

(Not from the notes of J.D.S. Jones)

Let $X$ be a smooth algebraic variety over a field $\mathbb{k}$ of characteristic $0$. The analogue of the HKR Theorem here is this:

+-- {: .num_theorem #SwYe}
###### Theorem
**(Swan, [Yekutieli](http://dx.doi.org/10.4153/CJM-2002-051-8)).**
There is a canonical isomorphism
\[ \operatorname{Ext}^i_{X^2}(\mathcal{O}_X, \mathcal{O}_X) \cong
\bigoplus_q \operatorname{H}^{i - q}(X, \bigwedge^q (\mathcal{T}_X)) . \]
=--

Here $\mathcal{T}_X$ is the tangent sheaf of $X$, and $X$ is embedded diagonally in $X^2$.

This is a consequence of the following result. Let $\mathcal{C}_{cd, X}$ be the sheaf of continuous Hochschild cochains of $X$. It is a bounded below complex of quasi-coherent $\mathcal{O}_{X^2}$-modules.

+-- {: .num_theorem #Yek1}
###### Theorem
**([Yekutieli](http://dx.doi.org/10.4153/CJM-2002-051-8)).**

1. There is a canonical isomorphism
\[ \operatorname{R} \mathcal{Hom}_{X^2}(\mathcal{O}_X, \mathcal{O}_X) \cong
\mathcal{C}_{cd, X} \]
in the derived category of $\mathcal{O}_{X^2}$-modules.

2. There is a canonical quasi-isomorphism of complexes of $\mathcal{O}_{X^2}$-modules
\[  \bigoplus_q \bigwedge^q (\mathcal{T}_X)[-q] \to \mathcal{C}_{cd, X}  . \]

3. Therefore there is a  canonical isomorphism
\[ \operatorname{R} \mathcal{Hom}_{X^2}(\mathcal{O}_X, \mathcal{O}_X) \cong
\bigoplus_q \bigwedge^q (\mathcal{T}_X)[-q] \]
in the derived category of $\mathcal{O}_{X^2}$-modules.
=--


The relation to deformation quantization is this: $\mathcal{C}_{cd, X}$ is a shift by $1$ of the sheaf of $\mathcal{D}_{poly, X}$ of polydifferential operators (viewed only as a complex of quasi-coherent $\mathcal{O}_{X^2}$-modules). Similarly,
$\bigoplus_q \bigwedge^q (\mathcal{T}_X)[-q]$
is the shift by $1$ of the sheaf $\mathcal{T}_{poly, X}$ of polyvector fields. Thus item 2 in the theorem above says that there is a canonical $\mathcal{O}_{X^2}$-linear quasi-isomorphism
\[ \mathcal{T}_{poly, X} \to \mathcal{D}_{poly, X} . \]
Trying to replicate the global formality theorem of Kontsevich, one would like to upgrade this to an $\mathrm{L}_{\infty}$ quasi-isomorphism.
However, it seems that in general this cannot be done directly, but only after a suitable resolution.

Here is the result. (See also [Van den Bergh](http://dx.doi.org/10.1016/j.jalgebra.2007.02.012).)
Any quasi-coherent sheaf $\mathcal{M}$ on $X$ admits a canonical flasque resolution called the mixed resolution:
\[ \mathcal{M} \to \operatorname{Mix}(\mathcal{M}) . \]
This "mixes" the jet resolution with the Cech resolution (corresponding to an affine open covering of $X$ that we suppress).
In particular there are quasi-isomorphisms of sheaves of DG Lie algebras
\[ \mathcal{T}_{poly, X} \to \operatorname{Mix}(\mathcal{T}_{poly, X}) \]
and
\[ \mathcal{D}_{poly, X} \to \operatorname{Mix}(\mathcal{D}_{poly, X}) . \]

+-- {: .num_theorem #Yek2}
###### Theorem
**([Yekutieli](http://www.math.bgu.ac.il/~amyekut/publications/def-quant/def-quant.html)).**
There is an  $\mathrm{L}_{\infty}$ quasi-isomorphism
\[ \Psi : \operatorname{Mix}(\mathcal{T}_{poly, X}) \to
\operatorname{Mix}(\mathcal{D}_{poly, X}) \]
whose $1$-st order term commutes with the HKR quasi-isomorphism above. It is independent of choices up to quasi-isomorphism.
=--

A Poisson deformation of $\mathcal{O}_X$ is a sheaf $\mathcal{A}$ of Poisson
$\mathbb{k}[[\hbar]]$-algebras on $X$, with an isomorphism
$\mathbb{k} \otimes_{\mathbb{k}[[\hbar]]} \mathcal{A} \cong \mathcal{O}_X$
called an augmentation. Likewise an associative deformation of $\mathcal{O}_X$ is a sheaf $\mathcal{A}$ of associative unital (but noncommutative)
$\mathbb{k}[[\hbar]]$-algebras on $X$, with an augmentation to $\mathcal{O}_X$.

[Theorem 4](#Yek2) implies:

+-- {: .num_theorem #Yek3}
###### Theorem
**(Yekutieli).**
Assume that the cohomology groups
$\operatorname{H}^{1}(X, \mathcal{O}_X)$ and
$\operatorname{H}^{2}(X, \mathcal{O}_X)$ vanish. Then there is a canonical bijection
\[ \mathrm{quant} : \quad
\frac{ \{ \text{ Poisson deformations of} \; \mathcal{O}_X \} }{\text{isomorphism}} \quad \xrightarrow{\, \simeq \,} \quad
\frac{ \{ \text{ associative deformations of} \; \mathcal{O}_X \} }{\text{isomorphism}}  \]
called quantization. It preserves first order brackets.
=--

When $X$ is affine this is Theorem 0.1 of
[this paper](http://www.math.bgu.ac.il/~amyekut/publications/def-quant/def-quant.html).
For the full statement see Corollary 11.2 of
[this paper](http://www.math.bgu.ac.il/~amyekut/publications/twisted-defs/twisted-defs.html).

For twisted (or stacky) deformations there is a corresponding (but much more difficult to state and prove). See the
[paper](http://www.math.bgu.ac.il/~amyekut/publications/twisted-defs/twisted-defs.html)
and the
[survey](http://www.math.bgu.ac.il/~amyekut/publications/tw-defs-surv/tw-defs-surv.html).






#### Gerstenhaber's deformation theory by Hochschild (co)homology

Let $V$ be a $k$-vector space and consider $C^p(V,V) = \Hom(V^{\otimes p}, V)$.  We define a "circle operator" $\circ$ as follows: for $f \in C^p(V,V)$ and $g \in C^q(V,V)$, we define $f \circ g \in C^{p+q-1}(V,V)$ as the map
\[ (f \circ g)(v_1, \ldots v_{p+q-1}) = f(v_1, \ldots, v_{i-1}, g(v_i, \ldots, v_{i+q-1}), v_{i+q}, \ldots, v_{p+q-1}). \]

For $f \in C^\ast(V,V)$, let $A_f(g,h) = (f \circ g) \circ h - f \circ (g \circ h)$.  (This is graded symmetric.)  It follows that the commutator of $\circ$ is given by
\[ [f,g] = f \circ g - (-1)^{(|f| - 1)(|g|-1)} g \circ f \]
where $|f| = p$ when $f \in C^p(V,V)$.  This defines a _graded [[Lie bracket]]_ of degree -1.

+-- {: .num_example}
###### Example
Let $\mu \in C^2(V,V)$ ($\mu : V \otimes V \to V$).  Note that $\mu$ is associative iff $\mu \circ \mu = 0$ iff $[\mu, \mu] = 0$.  Let $d_\mu : C^{p}(V,V) \to C^{p+1}(V,V)$ be defined by $d_\mu(x) = \mu \otimes x \pm x \otimes \mu = [\mu, x]$.  We have $d_\mu \circ d_\mu = 0$ so $(C^\ast(V,V), d_\mu)$ becomes a [[differential graded algebra]].  In fact this is the [[Hochschild cochain complex]] of the [[associative algebra]] $A = (V, \mu)$.
=--

Apply this example to the construction of deformation quantization.  The star product is uniquely determined by $\theta : A \otimes A \to A[ [ t ] ]$ given by $\theta(a,b) = ab + c(a,b)$.  What we want is that
\[ (\mu + c) \otimes (\mu + c) = 0; \]
write this out and we get the equation
\[ d_\mu c + c \circ c = 0, \]
or $d_\mu c + \frac{1}{2}[c,c] = 0$; this is the [[Maurer-Cartan equation]].  Hence we are looking for solutions of the M-C equation but in the Hochschild complex $C^\ast(A,A)[ [ t ] ]$.  One should note that $d_\mu$ is actually a [[derivation]] of the [[Lie bracket]], hence we have a [[dg-Lie algebra]].

+-- {: .num_theorem #HKR}
###### Theorem
**([[HKR theorem]])**. $HH^p(A,A) = \Gamma(M, \Lambda^p TM)$.
=--

(Note that $C^p(C^\infty(M),C^\infty(M))$ should be interpreted as $\Hom_{diff}(C^\infty(M), C^\infty(M))$.)  Under this isomorphism the Poisson bracket is mapped to the [[Poisson tensor]]:
\[ \{ \cdot , \cdot \} \in HH^2(A,A) \quad \mapsto \quad P \in \Gamma(M, \Lambda^2 TM). \]
The bracket in Hochschild cohomology ([[Gerstenhaber bracket]]) goes to the [[Schouten bracket]]:
\[ [ \cdot , \cdot ]_G \quad \mapsto \quad [ \cdot, \cdot ]_S. \]

For vector fields $\xi$ and $\eta$, the [[Schouten bracket]] satisfies (1) $[\xi,\eta]_S = [\xi,\eta]$ (the Lie bracket), and (2) $[\alpha, \beta \wedge \gamma] = [\alpha,\beta] \wedge \gamma \pm [\alpha,\gamma] \wedge \beta$; note that this completely determines it (everything is locally given by wedges...).

In the Hochschild cohomology $HH^\ast(A,A)$ of $A$, $d_\mu P \mapsto 0$ and $[P,P]_S = 0$, so _we have a solution to M-C in $H^\ast(A,A)[ [ t ] ]$_.

#### In terms of differential graded Lie algebras

+-- {: .num_defn}
###### Definition
Let $L_1$ and $L_2$ be [[differential graded Lie algebras]] (dgL).  A **[[quasi-isomorphism]]** $f : L_1 \to L_2$ is a homomorphism of dgLs that induces an isomorphism on homology.  $L_1$ and $L_2$ are **quasi-isomorphic** if there exists $M$ with quasi-isomorphisms $L_1 \leftarrow M \rightarrow L_2$.  It can be verified that this is an equivalence relation.
=--

+-- {: .num_theorem #KontsevichDeformationTheorem}
###### Theorem
**([[Kontsevich]])**.  If $L_1$ is quasi-isomorphic to $L_2$ then there is a solution to the M-C equation in $L_1$ iff there is a solution to the M-C equation in $L_2$.
=--

+-- {: .num_theorem #KontsevichFormality}
###### Theorem
**([[Kontsevich formality]])**.  $C^\ast(A,A)[ [ t ] ]$ is quasi-isomorphic to $H^\ast(A,A)[ [ t ] ]$.  ($A = C^\infty(M)$)
=--

Hence there is a solution to M-C in $C^\ast(A,A)[ [ t ] ]$, and hence there is a deformation quantization (!).

#### The Deligne conjecture

We have $(C^*(A,A), d_\mu)$, the [[Gerstenhaber bracket]], and we also have a [[cup product]]
\[ (f \cup g) (a_1, \ldots, a_{p+q}) = \mu(f(a_1,\ldots,a_p), g(a_{p+1},\ldots,a_{p+q})) \]
for $f : A^{\otimes p} \to A$, $g : A^{\otimes q} \to A$; this satisfies also $d_\mu(f \cup g) = (d_\mu f) \cup g \pm f \cup d_\mu g$.
The [[Deligne conjecture]] gives a relationship between these things.

In $HH^*(A,A)$, we have:

1. $[\cdot, \cdot]$ is a graded Lie bracket of degree -1.
1. The cup product $\cup$ is graded commutative.
1. The [[Jacobi identity]] for $[\cdot,\cdot]$.
1. $[a, b \cup c] = [a,b] \cup c \pm [a,c] \cup b$.

Such a thing is called a [[Gerstenhaber algebra]].  Note that we do not have these relations in $C^*(A,A)$, they are only true modulo boundaries.

+-- {: .num_theorem #Deligne}
###### Theorem
**([[Deligne conjecture]])**.  $C^*(A,A)$ is a $G_\infty$-algebra, which is a Gerstenhaber algebra _up to coherent homotopy_.
=--



#### Deformation by universal enveloping algebras
 {#RelationToUniversalEnvelopingAlgebras}

It is a classical fact that
the [[universal enveloping algebra]] of a [[Lie algebra]] provides
a deformation quantization of the corresponding [[Lie-Poisson structure]]
(example \ref{DeformationQuantizationOfLiePoissonStructuresByUniversalEnvelopingAlgebras} below).
Remarkably, this statement generalizes to more general [[polynomial Poisson algebras]] (def. \ref{PolynomialPoissonAlgebra} below)
for a suitable generalized concept of universal enveloping algebra (def. \ref{DeformationQuantizationOfLiePoissonStructuresByUniversalEnvelopingAlgebras} below):
it is _always_ true up to third order in $\hbar$, and sometimes to higher order ([Penkava-Vanhaecke 00, theorem 3.2](#PenkavaVanhaecke00), prop. \ref{UniversalEnvelopingAlgebraProvidesDeformationQuantizationAtLeastToOrder3} below).
In particular it also holds true for restrictions of [[Poisson bracket Lie algebras]] to their [[Heisenberg Lie algebras]]
(example \ref{DeformationQuantizationOfLiePoissonStructuresByUniversalEnvelopingAlgebras} below).

+-- {: .num_defn #PolynomialPoissonAlgebra}
###### Definition
**([[polynomial]] [[Poisson algebra]])**

A [[Poisson algebra]]  $((A,\cdot), \{-,-\})$
is called a _[[polynomial Poisson algebra]]_ if the underlying [[commutative algebra]] $(A,\cdot)$
is a [[polynomial algebra]], hence a [[symmetric algebra]]

$$
  Sym(V) \coloneqq T(V)/(x \otimes y - y \otimes x \vert x,y \in V)
$$

on some [[vector space]] $V$. Here

$$
  T(V) \coloneqq \underset{n \in \mathbb{N}}{\oplus} V^{\otimes^n}
$$

denotes the [[tensor algebra]] of $V$. We write

$$
  \mu \;\colon\; T(V) \longrightarrow Sym(V)
$$

for the canonical [[projection]] map (which is an algebra [[homomorphism]]) and

$$
  \sigma \;\colon\; Sym(V) \longrightarrow T(V)
$$

for its [[linear map|linear]] inverse (symmetrization, which is not in general an algebra [[homomorphism]]).

Notice that by its bi-[[derivation]] property the Poisson bracket
on a polynomial Poisson algebra is fixed by its restriction to linear elements

$$
  \{-,-\} \;\colon\; V \otimes V \longrightarrow Sym(V)
  \,.
$$

=--

+-- {: .num_example #PolynomialLiePoissonStructure}
###### Example
**(polynomial [[Lie-Poisson structure]])**

Let $(C^\infty(\mathbb{R}^n), \pi)$ be a [[Poisson manifold]] whose
underlying manifold is a [[Cartesian space]] $\mathbb{R}^n$. Then the restriction
of its Poisson algebra $( C^\infty(\mathbb{R}^n, \cdot), \pi^{i j} \partial_i(-) \cdot \partial_j(-)  )$
to the [[polynomial functions]] $\mathbb{R}[x^1, \cdots, x^n ] \ookrightarrow C^\infty(\mathbb{R}^n)$
is a polynomial Poisson algebra according to def. \ref{PolynomialPoissonAlgebra}.

In particular if $(\mathfrak{g}, [-,-])$ is a [[Lie algebra]] and
$(\mathfrak{g}^\ast, \{-,-\})$ the corresponding [[Lie-Poisson structure|Lie-Poisson manifold]],
then the corresponding polynomial Poisson algebra is $(Sym(\mathfrak{g}), \{-,-\})$
where the restriction of the Poisson bracket to linear polynomial elements coincides with the [[Lie bracket]]:

$$
  \{x,y\} = [x,y]
  \,.
$$

=--

+-- {: .num_defn #UniversalEnvelopingAlgebraOfPolynomialPoissonAlgebra}
###### Definition
**(universal enveloping algebra of polynomial Poisson algebra)**

Given a polynomial Poisson algebra $(Sym(V), \{-,-\})$ (def. \ref{PolynomialPoissonAlgebra}),
say that its _universal enveloping algebra_ $\mathcal{U}(V,\{-,-\})$ is the [[associative algebra]] which is the [[quotient]] of
the [[tensor algebra]] of $V$ with a [[power series|formal variable]] $\hbar$ adjoined
by the two-sided ideal which is generated by the the $\hbar$-Poisson bracket relation on linear elements:

$$
  \mathcal{U}(V,\{-,-\})
  \;\coloneqq\;
  T(V)/( x \otimes y - y \otimes x - \hbar \{x,y\} \vert x,y \in V )
  \,.
$$

This comes with the quotient projection linear map which we denote by

$$
  \rho \;\colon\; T(V)[ [ \hbar ] ] \longrightarrow \mathcal{U}(V,\hbar\{-,-\})
  \,.
$$


=--

([Penkava-Vanhaecke 00, def. 3.1](#PenkavaVanhaecke00))

+-- {: .num_example #UniversalEnvelopingAlgebraOfLieAlgebra}
###### Example
**([[universal enveloping algebra]] of [[Lie algebra]])**

In the case of a polynomial [[Lie-Poisson structure]] $(Sym(\mathfrak{g}), [-,-])$ (example \ref{PolynomialLiePoissonStructure})
the universal enveloping algebra $\mathcal{U}(\mathfrak{g},[-,-])$ from def. \ref{UniversalEnvelopingAlgebraOfPolynomialPoissonAlgebra}
(for $\hbar = 1$) coincides with the standard [[universal enveloping algebra]] of the [[Lie algebra]] $(\mathfrak{g}, [-,-])$.

=--

The combined linear projection maps from def. \ref{PolynomialPoissonAlgebra} and def. \ref{UniversalEnvelopingAlgebraOfPolynomialPoissonAlgebra}
we denote by

$$
  \tau \coloneqq \rho \circ (\sigma/[ [ \hbar ] ]) \;\colon\; Sym(V)[ [ \hbar ] ] \longrightarrow \mathcal{U}(V,\{-,-\})
  \,.
$$


+-- {: .num_prop #UniversalEnvelopingAlgebraProvidesDeformationQuantizationAtLeastToOrder3}
###### Proposition
**(universal enveloping algebra provides [[formal deformation quantization]] at least up to order 3)**

Let $( Sym(V), \{-,-\} )$ be a polynomial Poisson algebra (def. \ref{PolynomialPoissonAlgebra})
such that the canonical linear map to its universal enveloping algebra (def. \ref{UniversalEnvelopingAlgebraOfPolynomialPoissonAlgebra})
is [[injective function|injective]] up to order $n \in \mathbb{N}\cup \{\infty\}$

$$
  \tau/(\hbar^{n+1}) \;\colon\; Sym(V)[ [ \hbar ] ]/(\hbar^{n+1}) \hookrightarrow \mathcal{U}(V,\hbar\{-,-\})/(\hbar^{n+1})
  \,.
$$

Then the restriction of the product on $\mathcal{U}(V,\hbar\{-,-\})/(\hbar^{n+1})$ to $Sym(V)/(\hbar^{n+1})$
is a [[formal deformation quantization]] of $(Sym(V), \{-,-\})$ to order $n$ (hence a genuine deformation quantization in the case that $n = \infty$).

Moreover, this is _always_ the case for $n = 3$, hence for every polynomial Poisson algebra its universal enveloping algebra
always provides a deformation quantization of order $3$ in $\hbar$.

=--

([Penkava-Vanhaecke 00, theorem 3.2 with section 2](#PenkavaVanhaecke00))


+-- {: .num_example #DeformationQuantizationOfLiePoissonStructuresByUniversalEnvelopingAlgebras}
###### Example
**([[formal deformation quantization]] of [[Lie-Poisson structures]] by universal enveloping algebras)**

In the following cases the map $\tau$ in prop. \ref{UniversalEnvelopingAlgebraProvidesDeformationQuantizationAtLeastToOrder3}
is injective to arbitrary order, hence in these cases the universal enveloping algebra provides a genuine [[formal deformation quantization]]:

1. the case that the Poisson bracket is [[linear Poisson structure|linear]] in that restricts as

   $$
     \{-,-\} \;\colon\; V \otimes V \longrightarrow V \hookrightarrow Sym(V)
     \,.
   $$

   This is the case of the [[Lie-Poisson structure]] from example \ref{PolynomialLiePoissonStructure}
   and the universal enveloping algebra that provides it deformation quantization is the
   standard one (example \ref{UniversalEnvelopingAlgebraOfLieAlgebra}).


1. more generally, the case that the Poisson bracket restricted to linear elements has linear and
   constant contribution in that it restricts as

   $$
     \{-,-\} \;\colon\; V \otimes V \longrightarrow \mathbb{R} \oplus V \hookrightarrow Sym(V)
     \,.
   $$

   This includes notably the Poisson structures induced by [[symplectic vector spaces]],
   in which case the restriction

   $$
     \{-,-\} \;\colon\; (\mathbb{R} \oplus V) \otimes (\mathbb{R} \oplus V) \longrightarrow (\mathbb{R} \oplus V)
   $$

   is the [[Lie bracket]] of the associated [[Heisenberg Lie algebra]].



=--

This is ([Penkava-Vanhaecke 00, p. 26](#PenkavaVanhaecke00))
The first statement in itself is a classical fact (reviewed e.g. in [Gutt 11](#Gutt11)).



### Motivic Galois group action on the space of quantizations
 {#MotivicGaloisGroup}

In ([Kontsevich 99](Kontsevich99)) it was indicated that a [[quotient group]] of the [[motivic Galois group]] apparently equivalent to the [[Grothendieck-Teichmüller group]] naturally [[action|acts]] on the space of formal deformation quantizations of a finite dimensional manifold. See also at _[[cosmic Galois group]]_.

This has been formalized as follows. The formal deformation quantization of ([Kontsevich 97](#Kontsevich97)) is all induced by the [[Kontsevich formality]] theorem, which states that over suitable [[manifolds]]/[[varieties]] $X$ there is an [[equivalence]] of [[L-∞ algebras]]


$$
  \mathcal{X}(X) \stackrel{\simeq}{\to} C^\bullet(X)
$$

identifying the [[multivector fields]] on $X$ with the [[Hochschild cohomology]] complex (of its [[function algebra]]).  Every choice of such an equivalence induces one formal deformation quantization of a [[Poisson manifold]] $X$, and the two quantizations induced by two equivalent (homotopic) equivalences are in turn equivalent.

Therefore one may regard the [[∞-groupoid]] $Maps^{L_\infty}_{equiv}(\mathcal{X}(X), C^\bullet(X))$ as the "space of formal deformation quantizations" of $X$.

In ([Dolgushev 1109, theorem 6.2](#Dolgushev1109), [Dolgushev 1111, theorem 3.1](#Dolgushev1111)) it is shown that the set $\pi_0 Maps^{L_\infty}_{equiv}(\mathcal{X}(X), C^\bullet(X))$ of connected components of this space is, up to a choice of basepoint, the [[Grothendieck-Teichmüller group]], hence is a [[torsor]] over that group.

(This is based on identifications of the GRT Lie algebra with the degree-0 [[chain cohomology]] of the [[graph complex]], due to [[Thomas Willwacher]]. See at _[Grothendieck-Teichm&#252;ller group -- relation to the graph complex](Grothendieck-Teichm%C3%BCller+tower#RelationToTheGraphComplex)_.

Aspects of the generalization of this statement to more general spaces then $\mathbb{R}^n$ are discussed in [Dolgushev-Rogers-Willwacher 12](#DolgushevRogersWillwacher12).

For discussion of [[motive|motivic structures]] in [[geometric quantization]] see at _[[motivic quantization]]_.

## Examples

* [[Moyal deformation quantization]]

* [[Fedosov deformation quantization]]

## Related concepts

* [[reductions deformations resolutions in physics]]

* [[quantization]]

  * **deformation quantization**, [[geometric quantization]]

  * [[path integral]]

  * [[semiclassical approximation]]

* [[Jordan algebra]]

[[!include Isbell duality - table]]

[[!include infinitesimal and local - table]]

## References

Monographs:

* {#Waldmann07} [[Stefan Waldmann]], _Poisson-Geometrie und Deformationsquantisierung_, Springer (2007) &lbrack;[doi:10.1007/978-3-540-72518-3](https://doi.org/10.1007/978-3-540-72518-3)&rbrack;

* {#Gutt11} [[Simone Gutt]], _Deformation quantization of Poisson manifolds_, Geometry and Topology Monographs **17** (2011) 171-220 &lbrack;[gtm:17](https://msp.org/gtm/2011/17/p003.xhtml), [pdf](http://msp.org/gtm/2011/17/gtm-2011-17-003p.pdf)&rbrack;


The concept of algebraic deformation quantization originates around

* {#BayenFlatoFronsdalLichnerowiczSternheimer78} F. Bayen, [[Moshé Flato]], C. Fronsdal, , [[André Lichnerowicz]], [[Daniel Sternheimer]], _Deformation theory and quantization. I. Deformations of symplectic structures._, Annals of Physics (N.Y.) 111, 61, 111 (1978) ([publisher](http://www.sciencedirect.com/science/article/pii/0003491678902245))

* {#BayenFlatoFronsdalLichnerowiczSternheimer78b} F. Bayen, [[Moshé Flato]], C. Fronsdal, , [[André Lichnerowicz]], [[Daniel Sternheimer]], _Deformation theory and quantization. II. Physical applications_, Annals of Physics 111, 111-151 (1978)  ([publisher](http://www.sciencedirect.com/science/article/pii/0003491678902257))

Review is in 

* [[Daniel Sternheimer]], _Deformation Quantization: Twenty Years After_, AIP Conf.Proc.453:107-145,1998 ([arXiv:math/9809056](https://arxiv.org/abs/math/9809056))

The [[Fedosov deformation quantization]] prescription for deformation quantization of [[symplectic manifolds]] and varieties and also of [[Poisson manifolds]] that have a [[regular foliation]] by [[symplectic leaves]] is discussed in

* [[Boris Fedosov]], _Formal quantization_, Some Topics of Modern Mathematics and their Applications to Problems of Mathematical Physics (in Russian), Moscow (1985), 129-136.

* [[Boris Fedosov]], _Index theorem in the algebra of quantum observables_, Sov. Phys. Dokl. 34 (1989), 318-321.

* {#Fedosov94} [[Boris Fedosov]], _A simple geometrical construction of deformation quantization_  J. Differential Geom. Volume 40, Number 2 (1994), 213-238. ([EUCLID](http://projecteuclid.org/euclid.jdg/1214455536))


For algebraic forms this is discussed in

* {#BK09} [[Roman Bezrukavnikov]], [[Dmitry Kaledin]], _Fedosov quantization in algebraic context_ Mosc. Math. J., Volume 4, Number 3, (2004) 559&#8211;592 ([AMS pdf](http://www.ams.org/distribution/mmj/vol4-3-2004/bezrukavnikov-kaledin.pdf))

More discussion of this approach is in

* Claudio Emmrich, [[Alan Weinstein]], _The differential geometry of Fedosov's quantization_ ([arXiv:hep-th/9311094](http://arxiv.org/abs/hep-th/9311094))

A direct and general formula for the deformation quantization of any Poisson manifold was given in

* {#Kontsevich97} [[Maxim Kontsevich]], _Deformation quantization of Poisson manifolds_,  Lett. Math. Phys. __66__ (2003),  no. 3, 157--216, ([arXiv:q-alg/9709040](http://arxiv.org/abs/q-alg/9709040)).

see also

* Peter Banks, Erik Panzer, Brent Pym, _Multiple zeta values in deformation quantization_ ([arXiv:1812.11649](https://arxiv.org/abs/1812.11649))

This secretly uses the [[Poisson sigma-model]] (see there for more details) induced by the given target [[Poisson Lie algebroid]].

A popular exposition of this is in

* [[Anton Kapustin]], _Quantum geometry: The reunion of math and physics_ ([online slides](https://dl.dropboxusercontent.com/u/12796267/kapustin-talk.swf) [Powerpoint](http://www.theory.caltech.edu/~kapustin/talk.ppt))

The classification of the space of such formal deformation quantization is discussed in

* {#Dolgushev1109} [[Vasily Dolgushev]], _Stable Formality Quasi-isomorphisms for Hochschild Cochains I_ ([arXiv:1109.6031](http://arxiv.org/abs/1109.6031))


* {#Dolgushev1111} [[Vasily Dolgushev]], _Exhausting formal quantization procedures_ ([arXiv:1111.2797](http://arxiv.org/abs/1111.2797))


* {#DolgushevRogersWillwacher12} [[Vasily Dolgushev]], [[Christopher Rogers]], [[Thomas Willwacher]], _Kontsevich's graph complex, GRT, and the deformation complex of the sheaf of polyvector fields_ ([arXiv:1211.4230](http://arxiv.org/abs/1211.4230))


Deformation quantization of [[polynomial Poisson algebras]] via [[universal enveloping algebra]] (generalizing that of [[Lie-Poisson structures]]) is discussed in

* {#PenkavaVanhaecke00} [[Michael Penkava]], [[Pol Vanhaecke]], _Deformation Quantization of Polynomial Poisson Algebras_, Journal of Algebra
227, 365&#241;393 (2000) ([arXiv:math/9804022](https://arxiv.org/abs/math/9804022))


Deformation quantization of algebraic varieties is in

*  [[Amnon Yekutieli]], Deformation Quantization in Algebraic Geometry,
Advances in Mathematics 198 (2005), 383-432.
Erratum: Advances in Mathematics  217 (2008), 2897-2906.

See also

* MO discussion , _[Kontsevich's conjectures on the Grothendieck-Teichm&#252;ller group?](http://mathoverflow.net/questions/42148/kontsevichs-conjectures-on-the-grothendieck-teichmuller-group)_


Deformation quantization in [[perturbative quantum field theory]] is discussed for [[free field theory]] is due to

* {#Dito90} Joseph Dito, _Star-product approach to quantum field theory: The free scalar field_. Letters in Mathematical Physics, 20(2):125&#8211;134, 1990 ([spire](https://inspirehep.net/record/303898/))

and further expanded on in

* {#DuetschFredenhagen00} [[Michael Dütsch]], [[Klaus Fredenhagen]], section 5.1 of _Algebraic Quantum Field Theory, Perturbation Theory, and the Loop Expansion_, Commun.Math.Phys. 219 (2001) 5-30 ([arXiv:hep-th/0001129](https://arxiv.org/abs/hep-th/0001129))

* {#DuetschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic quantum field theory and deformation quantization_, Proceedings of the Conference on Mathematical Physics in Mathematics and Physics, Siena June 20-25 (2000) ([arXiv:hep-th/0101079](http://xxx.uni-augsburg.de/abs/hep-th/0101079))

* {#HirschfeldHenselder02} A. C. Hirshfeld, P. Henselder, _Star Products and Perturbative Quantum Field Theory_, Annals Phys. 298 (2002) 382-393 ([arXiv:hep-th/0208194](https://arxiv.org/abs/hep-th/0208194))


and for interacting [[perturbative quantum field theory]] ([[perturbative AQFT]]) in

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))

* {#HawkinsRejzner16} [[Eli Hawkins]], [[Kasia Rejzner]], _The Star Product in Interacting Quantum Field Theory_ ([arXiv:1612.09157](https://arxiv.org/abs/1612.09157))


The relation to [[geometric quantization]] is discussed in

* [[Eli Hawkins]], _The Correspondence between Geometric Quantization and Formal Deformation Quantization_ ([arXiv:math/9811049](http://arxiv.org/abs/math/9811049))

* Christoph N&#246;lle, _Geometric and deformation quantization_ ([arXiv:0903.5336](http://arxiv.org/abs/0903.5336))

and some remarks on the relation are also in section 1.4 of

* {#GukovWitten09} [[Sergei Gukov]], [[Edward Witten]], _Branes and Quantization_, Adv. Theor. Math. Phys. 13 (2009) 1&#8211;73, ([arXiv:0809.0305](http://arxiv.org/abs/0809.0305), [euclid](http://projecteuclid.org/euclid.atmp/1282054099))


which is about [[quantization via the A-model]].

The formulation of deformation quantization as lifts from [[P-n operads]] over [[BD-n operads]] to [[E-n operads]] is discussed in section 2.3 and 2.4 of

* {#CostelloGwilliam} [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html), early/partial draft [pdf](http://math.northwestern.edu/~gwilliam/factorization.pdf))




See also

* [wikipedia](http://en.wikipedia.org/wiki/Weyl_quantization#Deformation_quantization)
* F. Bayen, M. Flato, C. Fronsdal, A. Lichnerowicz, D. Sternheimer, _Quantum mechanics as a deformation of classical mechanics_, Lett. Math. Phys. 1 (1975/77), [MR674337](http://www.ams.org/mathscinet-getitem?mr=674337), [doi](http://dx.doi.org/10.1007/BF00399745);  _Deformation theory and quantization. I. Deformations of symplectic structures_, Ann. Physics 111 (1978), no. 1, 61&#8211;110, [MR496157](http://www.ams.org/mathscinet-getitem?mr=496157); _Deformation theory and quantization. II. Physical applications_, Ann. Physics 111 (1978), no. 1, 111&#8211;151, [MR496158](http://www.ams.org/mathscinet-getitem?mr=496158)
* M. Flato, A. Lichnerowicz, D. Sternheimer, _Deformations of Poisson brackets, Dirac brackets and applications_, J. Math. Phys. __17__ (1976), no. 9, 1754&#8211;1762, [MR420723](http://www.ams.org/mathscinet-getitem?mr=420723), [doi](http://dx.doi.org/10.1063/1.523104)
* D. Arnal, J.-C. Cortet, _$\ast$-products in the method
of orbits for nilpotent groups_, J. Geom. Phys. 2 (1985), no. 2,
83&#8211;116, <a href="http://dx.doi.org/10.1016/0393-0440(85)90010-5">doi</a>

On the [[stack]] of deformation quantizations:

* [[Maxim Kontsevich]], _Deformation quantization of algebraic varieties_ ([arXiv:math/0106006](http://arxiv.org/abs/math/0106006))

* Pietro Polesello, [[Pierre Schapira]], _Stacks of quantization-deformation modules on complex symplectic manifolds_ ([arXiv:math/0305171](http://arxiv.org/abs/math/0305171))

* [[Amnon Yekutieli]], _Twisted Deformation Quantization of Algebraic Varieties_ ,
[ arxiv:0905.0488 ](http://arxiv.org/abs/0905.0488)

The action of a [[motivic Galois group]] ("[[cosmic Galois group]]") on the space of deformation quantization was observed in

* {#Kontsevich99} [[Maxim Kontsevich]], _Operads and Motives in Deformation Quantization_, Lett. Math. Phys.48:35-72,1999 ([arXiv:math/9904055](http://arxiv.org/abs/math/9904055))

See also at _[[motives in physics]]_.


[[!redirects algebraic deformation quantization]]

[[!redirects formal deformation quantization]]
[[!redirects formal deformation quantizations]] 


[[!redirects formal algebraic deformation quantization]]
[[!redirects formal algebraic deformation quantizations]]
