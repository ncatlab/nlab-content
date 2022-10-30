

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
Then by a _normal ordered polynomial_ or _Wick polynomial_ ([Wick 50](#Wick50)) one means a [[polynomial]], denoted $:P:$, which is obtained from a polynomial $P((a_k, a^\ast_k))$ in these operatorss  by ordering all "creation operators" $a_k^\ast$ to the left of all "annihiliation operators". For example focusing on a single mode $k$ we have:

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
  \,.
$$

The intuitive idea is that these operators span a [[Hilbert space]] $\mathcal{H}$ of [[quantum states]] from a [[vacuum state]] $\vert vac \rangle \in \mathcal{H}$ characterized by the condition

$$
  \underset{k}{\forall} \left( a_k \vert vac \rangle = 0 \right)
$$

hence (if we think of $a_k$ as acting by "removing a quantum in mode $k$") by the condition that it contains no quanta. So the normal ordered Wick polynomials represent the [[quantum observables]] with vanishing [[vacuum expectation value]]. In [[quantum field theory]] they model [[scattering]] processes where quanta enter a reaction process (the modes corresponding to the "annihilation" operators $a_k$) and other particles come out of the reaction (the modes corresppnding to the "creation" operators $a^\ast_k$).

The product of two Wick polynomials, computed in the ambient operator algebra and then re-expressed as a Wick polynomial, is given by computing the relevant sequence of [[commutators]] by [[Wick's lemma]], for example

$$
  {:a^\ast a:} \, {:a^\ast a:} 
  =
  :a^\ast a^\ast a a: + c \, :a^\ast a:
  \,,
$$

where $c \coloneqq [a, a^\ast]$ is the value of the canonical [[commutator]].

The [[associative algebra]] thus obtained is hence called the _algebra of normal ordered operators_ or _Wick polynomial algebra_ or just _Wick algebra_. 

This plays a central role in [[perturbative quantum field theory]], where the [[quantization]] of [[quantum observables]] of [[free fields]] is traditionally _defined_ as the corresponding Wick algebra. 

But the Wick algebra in [[quantum field theory]] may also be understood more systematically from first principles of [[quantization]]. It turns out that it is [[Moyal deformation quantization]] of the canonical [[Poisson bracket]] on the [[covariant phase space]] of the [[free field]], which is the [[Peierls bracket]] modified to an [[almost Kähler structure]] by the [[2-point function]] of a [[quasi-free Hadamard state]] ([Dito 90](#Dito90), [D&#252;tsch-Fredenhagen 01](#DutschFredenhagen01)). See example \ref{WickAlgebraOfASingleMode} below.

Understood in this form the construction directly generalized to [[quantum field theory on curved spacetimes]] ([Brunetti-Fredenhagen 95](#BrunettiFredenhagen95), [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00), [Hollands-Wald 01](#HollandsWald01)).

Finally the shift by the [[quasi-free Hadamard state]], which is the very source of the "normal ordering", was understood as an example of the almost-K&#228;hler version of the quantization recipe of [[Fedosov deformation quantization]] ([Collini 16](#Collini16)). For more on this see at _[[locally covariant perturbative quantum field theory]]_.

## Definition

### For finite-dimensional linear phase spaces
 {#ForFiniteDimensionalLinearPhaseSpaces}


+-- {: .num_defn #AlmostKaehlerVectorSpace}
###### Definition
**(almost K&#228;hler vector space)**

An _almost K&#228;hler vector space_ is a [[complex vector space]] $V$ equipped with two [[bilinear forms]] $\sigma, g \;\colon\; V \otimes_{\mathbb{R}} V \longrightarrow \mathbb{R}$ such that with $V$ regarded as a [[smooth manifold]] and with $\sigma, g$ regarded as constant [[tensors]], $(V,\sigma,g)$ is an [[almost Kähler manifold]].

=--

+-- {: .num_example #StandardAlmostKaehlerVectorSpaces}
###### Example
**(standard almost K&#228;hler vector spaces)**

Let $V \coloneqq \mathbb{R}^2$ equipped with the [[complex structure]] given by the canonical identification $\mathbb{R}^2 \simeq \mathbb{C}$, let $\sigma \coloneqq \left( \array{0 & -1 \\ 1 & 0} \right)$ and $g \coloneqq \left( \array{ 1 & 0 \\ 0 & 1}  \right)$. Then $(V,\sigma,g)$ is an almost K&#228;hler vector space (def. \ref{AlmostKaehlerVectorSpace}).

=--


+-- {: .num_defn #WickAlgebraOfAlmostKaehlerVectorSpace}
###### Definition
**(Wick algebra of an almost K&#228;hler vector space)**

Let $(\mathbb{R}^{2n},\sigma, g)$ be an almost K&#228;hler vector space (def. \ref{AlmostKaehlerVectorSpace}). Then its _Wick algebra_ is the [[formal power series]] vector space $\mathbb{C}[ [ a_1, a^\ast_1, \cdots, a_n, a^\ast_n  ] ] [ [ \hbar ] ]$ equipped with the [[Moyal star product]]

$$
  \begin{aligned}
    P_1 \star_\omega P_2
    & \coloneqq
    prod \circ \exp \left( \tfrac{\hbar}{2}\underoverset{k_1, k_2 = 1}{2 n}{\sum}\omega^{a b} \partial_a \otimes  \partial_b \right)  (P_1 \otimes P_2)
    \\
    & =
    P_1 \cdot P_2 + \tfrac{\hbar}{2} \underoverset{k_1, k_2 = 1}{2n}{\sum}\omega^{k_1 k_2}(\partial_{k_1} P_1) \cdot (\partial_{k_2} P_2)
    + \cdots
  \end{aligned}
$$

given by the bilinear form

$$
  \omega \coloneqq i \sigma + g
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
  : P_1 \star_\omega P_2 : 
$$

=--

+-- {: .num_example #WickAlgebraOfASingleMode}
###### Example
**(Wick algebra of a single mode)**

Let $V \coloneqq \mathbb{R}^2 \simeq Span(\{x,y\})$ be a standard almost K&#228;hler vector space according to example \ref{StandardAlmostKaehlerVectorSpaces}, with canonical coordinates denoted $x$ and $y$. We discuss its Wick algebra according to def. \ref{WickAlgebraOfAlmostKaehlerVectorSpace} and show that this reproduces the traditional definition of products of "normal ordered" operators as [above](#Idea).

To that end, consider the complex linear combination of the coordinates to the canonical complex coordinates $z \coloneqq x + i y$ and $\overline{z} \coloneqq x - i y$, which we suggestively write instead as

$$
  a \coloneqq \tfrac{1}{\sqrt{2}}(x + i y)
  \phantom{AAAA}
  a^\ast \coloneqq \tfrac{1}{\sqrt{2}}(x - i y)
$$

(with "$a$" the traditional symbol for the _amplitude_ of a field mode).

We find the value of the almost-K&#228;hler forms on these elements to be

$$
  \begin{aligned}
    \sigma(a,a^\ast)
    & = 
    \tfrac{1}{2} \sigma( (x + i y), (x - i y) )
    \\
    & = 
    \tfrac{-i}{2}( \sigma(x,y) - \sigma(y,x) )
    \\
    & =
    - i
  \end{aligned}
$$

$$
  \begin{aligned}
    g(a, a^\ast)
    & =
    \tfrac{1}{2} g( (x + i y), (x - i y) )
    \\
    & = 
    \tfrac{1}{2}(g(x,x) + g(y,y))
    \\
    & =
    1
  \end{aligned}
$$

$$
  \begin{aligned}
    \sigma(a,a)
    & = 
    \sigma(a^\ast, a^\ast)
    \\
    & =
    0
    \phantom{AAAAAA} \text{by anti-symmetry}
  \end{aligned}
$$

$$
  \begin{aligned}
    g(a,a)
    & =
    \tfrac{1}{2}( g( (x + i y), (x + i y) ) )
    \\
    & =
    \tfrac{1}{2}( g(x,x) - g(y,y))
    \\
    & = 
    0
  \end{aligned}
$$

$$
  \begin{aligned}
    g(a^\ast, a^\ast)
    & = 
    \tfrac{1}{2}( g(x,x) - g(y,y) )
    \\
    & = 0
  \end{aligned}
$$

Using this, we find the Moyal star product as follows (where we write $(-)\cdot (-)$ for the plain commutative product in the [[formal power series algebra]]):

$$
  \begin{aligned}
    a \star_\omega a^\ast
    & =
    a \cdot a^\ast
    +
    \tfrac{\hbar}{2}
    \left(
       \underset{= 1}{\underbrace{i \sigma( a, a^\ast )}}
       + 
       \underset{= 1}{\underbrace{g(a, a^\ast)}}
    \right)
    \\
    & = 
    a^\ast \cdot a + \hbar  
    \\
    \\
    a^\ast \star_\omega a
    & =
    a^\ast \cdot a
    + 
    \tfrac{\hbar}{2}
    \left(
      \underset{= -1}{\underbrace{i \sigma( a^\ast , a )}}
      + 
      \underset{ = 1}{\underbrace{g( a^\ast, a )}}
    \right)
    \\
    & =
    a^\ast \cdot a
    \\
    \\
    a \star_\omega a 
     & = 
    a \cdot a
    \\
    \\
    a^\ast \star_\omega a^\ast
    & = 
    a^\ast \cdot a^\ast
  \end{aligned}
$$

These four cases are sufficient to see that in the star-product $P_1 \star_\omega P_2$ of general elements, we obtain correction term $\hbar$ to the ordinary commutative product precisely for every pair consisting  of a factor of $a$ in $P_1$ and a factor $a^\ast$ in $P_2$. This is exactly the "normal ordering" prescription.

=--

### For free fields on curved spacetimes

(...)


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

