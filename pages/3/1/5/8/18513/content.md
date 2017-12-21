

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

A _Wick algebra_ is an [[algebra of quantum observables]] of [[free fields|free]] [[quantum field theory|quantum fields]].

In the [[quantum mechanics]] of [[harmonic oscillators]] or in [[quantum field theory]] of [[free fields]] on [[Minkowski spacetime]] one encounters [[linear operators]] $\{a_k, a^\ast_k\}_{k \in K}$ that satisfy the [[canonical commutation relation]] $[a_i, a^\ast_j] = diag((c_k))_{i j}$.
Then by a _normal ordered polynomial_ or _Wick polynomial_ ([Wick 50](#Wick50)) one means a [[polynomial]], denoted $:P:$, which is obtained from a polynomial $P((a_k, a^\ast_k))$ in these operators  by ordering all "creation operators" $a_k^\ast$ to the left of all "annihiliation operators". For example focusing on a single mode $k$ we have:

$$
  \array{
    :a^\ast: = a^\ast
    \\
    :a: = a
    \\
    :a^\ast a: = a^\ast a
    \\
    :a a^\ast: = a^\ast a
    \\
    :a a^\ast a: = a^\ast a a
    \\
    etc.
  }
  \,
$$

The intuitive idea is that these operators span a [[Hilbert space]] $\mathcal{H}$ of [[quantum states]] from a [[vacuum state]] $\vert vac \rangle \in \mathcal{H}$ characterized by the condition

$$
  a_k \vert vac \rangle = 0
  \phantom{AAA}
  \text{for all} \,\, k
$$

hence (if we think of $a_k$ as acting by "removing a quantum in mode $k$") by the condition that it contains no quanta. So the normal ordered Wick polynomials represent the [[quantum observables]] with vanishing [[vacuum expectation value]]. In [[quantum field theory]] they model [[scattering]] processes where quanta enter a reaction process (the modes corresponding to the "annihilation" operators $a_k$) and other particles come out of the reaction (the modes corresppnding to the "creation" operators $a^\ast_k$).

The product of two Wick polynomials, computed in the ambient operator algebra and 
then re-expressed as a Wick polynomial, is given by computing the relevant sequence of [[commutators]] by [[Wick's lemma]], for example

$$
  {:a^\ast a:} \, {:a^\ast a:}
  =
  :a^\ast a^\ast a a: + \hbar \, :a^\ast a:
  \,,
$$

where $\hbar = [a, a^\ast]$ is the value of the [[canonical commutation relations|canonical commutator]].

The [[associative algebra]] thus obtained is hence called the _algebra of normal ordered operators_ or _Wick polynomial algebra_ or just _Wick algebra_.

This plays a central role in [[perturbative quantum field theory]], where the [[quantization]] of [[quantum observables]] of [[free fields]] is traditionally _defined_ as the corresponding Wick algebra.

But the Wick algebra in [[quantum field theory]] may also be understood more systematically from first principles of [[quantization]]. It turns out that it is [[Moyal deformation quantization]] of the canonical [[Poisson bracket]] on the [[covariant phase space]] of the [[free field]], which is the [[Peierls bracket]] modified to an [[almost Kähler structure]] by the [[2-point function]] of a [[quasi-free Hadamard state]] ([Dito 90](#Dito90), [D&#252;tsch-Fredenhagen 01](#DutschFredenhagen01)). See example \ref{WickAlgebraOfASingleMode} and def. \ref{WickAlgebraOfFreeQuantumField} below.

Understood in this form the construction directly generalized to [[quantum field theory on curved spacetimes]] ([Brunetti-Fredenhagen 95](#BrunettiFredenhagen95), [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00), [Hollands-Wald 01](#HollandsWald01)).

Finally, the shift by the [[quasi-free Hadamard state]], which is the very source of the "normal ordering", was understood as an example of the almost-K&#228;hler version of the quantization recipe of [[Fedosov deformation quantization]] ([Collini 16](#Collini16)). For more on this see at _[[locally covariant perturbative quantum field theory]]_.

$\,$


[[!include Wick algebra -- table]]



## Definition

### For finite-dimensional linear phase spaces
 {#ForFiniteDimensionalLinearPhaseSpaces}


+-- {: .num_defn #AlmostKaehlerVectorSpace}
###### Definition
**([[Kähler vector space]])**

An _[[Kähler vector space]]_ is a [[real vector space]] $V$ equipped with a [[linear complex structure]] $J$ as well as two [[bilinear forms]] $\omega, g \;\colon\; V \otimes_{\mathbb{R}} V \longrightarrow \mathbb{R}$ such that the following equivalent conditions hold:

1. $\omega(J v, J w) = \omega(v,w)$ and $g(v,w) = \omega(v,J w)$;

1. with $V$ regarded as a [[smooth manifold]] and with $\omega, g$ regarded as constant [[tensors]], then $(V, \omega, g)$ is an [[almost Kähler manifold]].

=--

+-- {: .num_example #StandardAlmostKaehlerVectorSpaces}
###### Example
**(standard [[Kähler vector spaces]])**

Let $V \coloneqq \mathbb{R}^2$ equipped with the [[complex structure]] $J$ which is given by the canonical identification $\mathbb{R}^2 \simeq \mathbb{C}$, hence, in terms of the canonical [[linear basis]] $(e_i)$ of $\mathbb{R}^2$, this is

$$
  J = (J^i{}_j) 
  \coloneqq 
  \left( 
    \array{
      0 & -1
      \\
      1 & 0
    }
  \right)
  \,.
$$

Moreover let 

$$
  \omega = (\omega_{i j}) \coloneqq \left( \array{0 & 1 \\ -1 & 0} \right)
$$ 

and 

$$
  g = (g_{i j}) \coloneqq \left( \array{ 1 & 0 \\ 0 & 1}  \right)
  \,.
$$ 

Then $(V, J, \omega, g)$ is a [[Kähler vector space]] (def. \ref{AlmostKaehlerVectorSpace}).

The corresponding [[Kähler manifold]] is $\mathbb{R}^2$ regarded as a [[smooth manifold]] in the standard way and equipped with the [[bilinear forms]] $J, \omega g$ extended as constant rank-2 [[tensors]] over this manifold.

If we write 

$$
  x,y \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
$$

for the standard [[coordinate functions]] on $\mathbb{R}^2$ with 

$$
  z \coloneqq x + i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

and

$$
 \overline{z} \coloneqq x - i y \;\coloneqq\; \mathbb{R}^2 \to \mathbb{C}
$$

for the corresponding complex coordinates, then this translates to 

$$
  \omega
  \in
  \Omega^2(\mathbb{R}^2)
$$ 

being the [[differential 2-form]] given by

$$
  \begin{aligned}
    \omega
    & =
    d x \wedge d y
    \\
    & =
    \tfrac{1}{2i} d z \wedge d \overline{z}
  \end{aligned}
$$

and with [[Riemannian metric]] [[tensor]] given by

$$
  g = d x \otimes d x + d y \otimes d y
  \,.
$$

The [[Hermitian form]] is given by

$$
  \begin{aligned}
    h 
    & = 
    g - i \omega
    \\
    & = 
    d z \otimes d \overline{z}
  \end{aligned}
$$


=--

(for more see at _[[Kähler vector space]]_ [this example](Kähler+vector+space#StandardAlmostKaehlerVectorSpaces)).

+-- {: .num_defn #WickAlgebraOfAlmostKaehlerVectorSpace}
###### Definition
**([[Wick algebra]] of a [[Kähler vector space]])**

Let $(\mathbb{R}^{2n},\sigma, g)$ be a [[Kähler vector space]] (def. \ref{AlmostKaehlerVectorSpace}). Then its _Wick algebra_ is the [[formal power series]] vector space $\mathbb{C}[ [ a_1, a^\ast_1, \cdots, a_n, a^\ast_n  ] ] [ [ \hbar ] ]$ equipped with the [[star product]]

$$
  \begin{aligned}
    P_1 \star_\pi P_2
    & \coloneqq
    prod \circ \exp \left( \hbar\underoverset{k_1, k_2 = 1}{2 n}{\sum}\pi^{a b} \partial_a \otimes  \partial_b \right)  (P_1 \otimes P_2)
    \\
    & =
    P_1 \cdot P_2 + \hbar \underoverset{k_1, k_2 = 1}{2n}{\sum}\pi^{k_1 k_2}(\partial_{k_1} P_1) \cdot (\partial_{k_2} P_2)
    + \cdots
  \end{aligned}
$$

given by the bilinear form

$$
  \label{InStarProductTensorInvertingHermitianForm}
  \pi \coloneqq \tfrac{i}{2} \omega^{-1} + \tfrac{1}{2} g^{-1}
  \,.
$$

Here

$$
  prod \;\colon\; \mathbb{C}[ [ a_1, a^\ast_1, \cdots, a_n, a^\ast_n  ] ] [ [ \hbar ] ]
  \otimes_{\mathbb{R}}
  \mathbb{C}[ [ a_1, a^\ast_1, \cdots, a_n, a^\ast_n  ] ] [ [ \hbar ] ]
   \longrightarrow
   \mathbb{C}[ [ a_1, a^\ast_1, \cdots, a_n, a^\ast_n  ] ] [ [ \hbar ] ]
$$

is the ordinary (commutative) product in the [[formal power series algebra]].

To make contact with the traditional notation we decorate the elements $P$ in the formal power series algebra with colons and declare the notation

$$
  : P_1 : \, :P_2:
  \;\coloneqq\;
  : P_1 \star_\pi P_2 :
$$

=--

+-- {: .num_example #WickAlgebraOfASingleMode}
###### Example
**([[Wick algebra]] of a single mode)**

Let $V \coloneqq \mathbb{R}^2 \simeq Span(\{x,y\})$ be the standard [[Kähler vector space]] according to example \ref{StandardAlmostKaehlerVectorSpaces}, with canonical coordinates denoted $x$ and $y$. We discuss its Wick algebra according to def. \ref{WickAlgebraOfAlmostKaehlerVectorSpace} and show that this reproduces the traditional definition of products of "normal ordered" operators as [above](#Idea).

To that end, consider the complex linear combination of the coordinates to the canonical complex coordinates 

$$
  z \;\coloneqq\; x + i y
  \phantom{AAA} 
    \text{and} 
  \phantom{AAA}
  \overline{z} \coloneqq x - i y
$$ 

which we use in the form

$$
  a^\ast \;\coloneqq\; \tfrac{1}{\sqrt{2}}(x + i y)
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  a \;\coloneqq\; \tfrac{1}{\sqrt{2}}(x - i y)
$$

(with "$a$" the traditional symbol for the _amplitude_ of a field mode).

Now

$$
  \omega^{-1}
  =
  \frac{\partial}{\partial y} \otimes \frac{\partial}{\partial x}  
  -
  \frac{\partial}{\partial x} \otimes \frac{\partial}{\partial y}
$$

$$
  g^{-1} 
  =
  \frac{\partial}{\partial x} 
  \otimes
  \frac{\partial}{\partial x} 
  +
  \frac{\partial}{\partial y} 
  \otimes
  \frac{\partial}{\partial y} 
$$

so that with

$$
  \frac{\partial}{\partial z}
  =
  \tfrac{1}{2}
  \left(
     \frac{\partial}{\partial x}
     -i
     \frac{\partial}{\partial y}
  \right)
  \phantom{AAAA}
  \frac{\partial}{\partial \overline{z}}
  =
  \frac{1}{2}
  \left(
    \frac{\partial}{\partial x}
    +
    i
    \frac{\partial}{\partial y}
  \right)
$$

we get

$$
  \begin{aligned}
    \tfrac{i \hbar}{2}\omega^{-1} + \tfrac{\hbar}{2} g^{-1}
    & =
    2 \hbar
    \frac{\partial}{\partial \overline{z}}
      \otimes 
    \frac{\partial}{\partial z}
    \\
    & =
    \hbar \frac{\partial}{\partial a} \otimes \frac{\partial }{\partial a^\ast}
  \end{aligned}
$$

Using this, we find the [[star product]] 

$$
  A \star_\pi B
  \;=\;
  prod \circ \exp\left( \hbar \frac{\partial}{\partial a} \otimes \frac{\partial }{\partial a^\ast}  \right)
$$

to be as follows (where we write $(-)\cdot (-)$ for the plain commutative product in the [[formal power series algebra]]):

$$
  \begin{aligned}
    a \star_\pi a & = a \cdot a
    \\
    a^\ast \star_\pi a^\ast & = a^\ast \cdot a^\ast
    \\
    a^\ast \star_\pi a & = a^\ast \cdot a
    \\
    a \star_\pi a^\ast
    & =
    a \cdot a^\ast + \hbar
  \end{aligned}
$$

and so forth, for instance

$$
  \array{
    (a a ) \star_\pi (a^\ast a^\ast)
    & =
    a^\ast \cdot a^\ast \cdot a \cdot a
    +
    4 \hbar a^\ast \cdot a
    +   
    \hbar^2
  }
$$

If we instead indicate the commutative pointwise product by 

$$
  :f g: \;\coloneqq\; f \cdot g
$$

and indicate the star-product by juxtaposition, then this reads

$$
  \array{
    :a a: \, :a^\ast a^\ast:
    & =
    : a^\ast a^\ast a  a :
    +
    4 \hbar \, : a^\ast a :
    +   
    \hbar^2
  }
$$

=--



### Wick algebra in field theory
 {#WickAlgebraInFieldTheory}

In [[free field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations]] of motion, then analog of (eq:InStarProductTensorInvertingHermitianForm)

$$
  \pi \;=\; \tfrac{i}{2}\omega^{-1} + \tfrac{1}{2}g^{-1}
$$

is the [[Wightman propagator]] according to [this equation](Hadamard+distribution#eq:DeompositionOfHadamardPropagatorOnMinkowkski)

$$
  \Delta_H
  \;=\;
  \tfrac{i}{2}\Delta_S + H
  \,.
$$



+-- {: .num_prop #MoyalStarProductOnMicrocausal}
###### Proposition
**(Hadamard-Moyal star product on [[microcausal observables]])

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] and let $\Delta_H$ be a corresponding [[Hadamard distribution]] ([[Wightman propagator]]).

Then the [[star product]]

$$
  P_1 \star_{\Delta_H} P_2
  \;\coloneqq\;
  prod
   \circ
  \exp\left(
    \int_{X^2} \hbar \Delta_H^{a b}(x_1, x_2) \frac{\delta}{\delta \Phi^a(x_1)}
    \otimes \frac{\delta}{\delta \Phi^b(x_2)} dvol_g
  \right)
  (P_1 \otimes P_2)
$$

on [[microcausal observables]] $P_1, P_2 \in \mathcal{F}_{mc}$ is well defined in that the [[products of distributions]] that appear in expanding out the [[exponential]] are such that the sum of the [[wave front sets]] of the factors does not intersect the zero section.

=--

(e.g. [Collini 16, p. 25-26](#Collini16))

+-- {: .proof}
###### Proof

By definition of [[Hadamard distribution]], the [[wave front set]] of powers of $\pi$ has all cotangents on the first variables future pointing, and all those on the second variables past pointing. The first variables are integrated against those of $P_1$ and the second against $P_2$. By definition of microcausal functionals, the wave front sets of $P_1$ and $P_2$ are disjoint from the subsets where all components are future pointing or all components are past-pointing. Therefore the relevant sum of of the wave front covectors never vanishes.

=--

+-- {: .num_defn #WickAlgebraOfFreeQuantumField}
###### Definition
**(Wick algebra of free quantum field)**

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] and let $\Delta_H$ be a corresponding [[Hadamard distribution]] ([[Wightman propagator]]).

Then the _Wick algebra_ of [[quantum observables]] of the [[free field|free]] [[scalar field]] on $(X,g)$ is the space of [[microcausal functionals]] $\mathcal{F}_{mc}$ equipped with the Hadamard-Moyal [[star product]] from prop. \ref{MoyalStarProductOnMicrocausal}:

$$
  \mathcal{W}(X,\Delta_H)
  \;\coloneqq\;
  \left(
    \mathcal{F}_{mc}, \star_{\Delta_H}
  \right)
  \,.
$$

> (this is [[off-shell]])

=--


In [[Minkowski spacetime]] the [[Hadamard state]] is simply the usual [[vacuum state]] $\vert vac \rangle$, hence the [[Hadamard distribution]] is, as a [[generalized function]]

$$
  \pi(x,y) = \langle vac \vert \Phi(x) \Phi(y) \vert vac \rangle
  \,.
$$

[[!include propagators - table]]

Therefore the abstractly defined Wick algebra as in def. \ref{WickAlgebraOfFreeQuantumField} in this case satisfies the relation

$$
  \int_{X} f(x,y)  \;  :\Phi(x): \,  :\Phi(y): \; dvol_g
  \;=\;
  \int_X f(x,y) \left( :\Phi(x) \Phi(y): -  \langle vac \vert \Phi(x) \Phi(y) \vert vac \rangle \right)  \; dvol_g
  \,.
$$

This is the traditional expression for the normal ordered Wick product on Minkowski spacetime (e.g. [here](https://en.wikipedia.org/wiki/Normal_order#Free_fields)).

## Related concepts

[[!include products in pQFT -- table]]


## References

The construction goes back to

* {#Wick50} [[Gian-Carlo Wick]], _The evaluation of the collision matrix_, Phys. Rev. 80, 268-272 (1950)

Its realization as the [[Moyal deformation quantization]] of the [[Peierls bracket]] shifted by a [[quasi-free Hadamard state]] is due to

* {#Dito90} J. Dito, _Star-product approach to quantum field theory: The free scalar field_. Letters in Mathematical Physics, 20(2):125&#8211;134, 1990 ([spire](https://inspirehep.net/record/303898/))

further amplified in

* {#DutschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic field theory, and deformation quantization_, in [[Roberto Longo]] (ed.), _Mathematical Physics in Mathematics and Physics, Quantum and Operator Algebraic Aspects_, volume 30 of Fields Institute Communications, pages 151&#8211;160. American Mathematical Society, 2001 ([arXiv:hep-th/0101079](https://arxiv.org/abs/hep-th/0101079))


and the generalization to [[quantum field theory on curved spacetime]] is discussed in

* {#BrunettiFredenhagen95} [[Romeo Brunetti]], [[Klaus Fredenhagen]], M. K&#246;hler, _The microlocal spectrum condition and Wick polynomials on curved spacetimes_, Commun. Math. Phys. 180, 633-652, 1996 ([arXiv:gr-qc/9510056](https://arxiv.org/abs/gr-qc/9510056))


* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

* {#HollandsWald01} [[Stefan Hollands]], [[Robert Wald]], _Local Wick Polynomials and Time Ordered Products of Quantum Fields in Curved Spacetime_, Commun. Math. Phys. 223:289-326, 2001 ([arXiv:gr-qc/0103074](https://arxiv.org/abs/gr-qc/0103074))

The conceptual explanation of the shift by the Hadamard state as a step in the almost-K&#228;hler version of [[Fedosov deformation quantization]] is due to

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))


[[!redirects Wick algebras]]


[[!redirects Wick polynomial]]
[[!redirects Wick polynomials]]

[[!redirects normal ordering]]

[[!redirects normal-ordered product]]
[[!redirects normal-ordered products]]

[[!redirects normal ordered product]]
[[!redirects normal ordered products]]

