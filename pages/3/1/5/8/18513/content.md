

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
  A \start_\pi B
  \;=\;
  prod \circ \exp\left( \hbar \frac{\partial}{\partial a} \otimes \frac{\partial }{\partial a^\ast}  \right)
$$

as follows (where we write $(-)\cdot (-)$ for the plain commutative product in the [[formal power series algebra]]):

$$
  \begin{aligned}
    a \star_\pi a & = a \cdot a
    \\
    a^\ast \star_\pi a^\ast & = a^\ast \cdot a^\ast
    \\
    a^\ast \star_\pi a & = a^\ast \star_\pi a
    \\
    a \star_\pi a^\ast
    & =
    a \cdot a^\ast + \hbar
  \end{aligned}
$$

These four cases are sufficient to see that in the star-product $P_1 \star_\pi P_2$ of general elements, we obtain correction term $\hbar$ to the ordinary commutative product precisely for every pair consisting  of a factor of $a$ in $P_1$ and a factor $a^\ast$ in $P_2$. This is exactly the "normal ordering" prescription.

=--

### For free fields on curved spacetimes
 {#ForFreeFieldsOnCurvedSpacetime}

The genuine Wick algebras in [[quantum field theory]] are
the analogues to those induced by finite-dimensional almost K&#228;hler vector spaces as [above](#ForFiniteDimensionalLinearPhaseSpaces), where now the underlying vector space is a space of ("[[microcausal functional|microcausal]]") [[functionals]] on the space of [[smooth functions]] on a [[spacetime]], and where the [[symplectic form]] is given by the [[causal propagator]] of the [[wave equation]]/[[Klein-Gordon equation]].

We give the definition [below](#WickAlgebraInFieldTheory).
First we briefly recall the relevant ingredients:

#### Covariant phase space of the free scalar field


+-- {: .num_defn #PointEvaluationObservable}
###### Definition
**(point evaluation observable)**

Let $X$ be a [[smooth manifold]]. Then the [[mapping space]] $C^\infty(X, \mathbb{R})$ is naturally a [[smooth space]].

For $x \in X$ there is the [[smooth function]]

$$
  \array{
     C^\infty(X) &\overset{\Phi(x)}{\longrightarrow}& \mathbb{R}
     \\
     \phi &\mapsto& \phi(x)
  }
$$

evaluating at $x \in X$.

=--

More generally:

+-- {: .num_defn #SmoothFunctionalsOnSmoothFunctions}
###### Definition
**(smooth functionals on smooth functions)


For $f \in C_c^\infty(X)$ a [[bump function]], it induces the function given by [[integration]]

$$
  \array{
    C^\infty(X) &\overset{\Phi(f)}{\longrightarrow}& \mathbb{R}
    \\
    \phi &\mapsto& \int_X f \cdot \phi dvol_g
  }
  \,,
$$

where $dvol_g$ denotes the [[volume form]] of the given [[pseudo-Riemannian metric]], and similarly if $f \in C_c^\infty(X^n)$ is a bump function on the $n$-fold [[Cartesian product]] manifold $X^n$, then there is

$$
  \array{
    C^\infty(X^n) &\overset{\Phi(f)}{\longrightarrow}& \mathbb{R}
    \\
    \phi &\mapsto& \int_{X^n} f \cdot \phi^n dvol_g^n
  }
  \,,
$$

Write $\mathcal{F}_{reg}$ for the sub-algebra of smooth functions on the smooth space $C^\infty(X)$ which is generated from the functions $\Phi(f)$ for $n \in \mathbb{N}$ and $f \in C^\infty_c(X^n)$.

A further evident generalization of this takes $f \in \mathcal{E}'(X^n)$ to be a [[compactly supported distribution]] and induces the function

$$
  \array{
    C^\infty(X^n) &\overset{\Phi(f)}{\longrightarrow}& \mathbb{R}
    \\
    \phi &\mapsto& \langle f, \phi^{\otimes^n} \rangle_g
  }
  \,.
$$

Write $\mathcal{F}_{dist}$ for the subalgebra generated by these functionals.
(After [[deformation quantization]] below, this is the origin of "[[operator-valued distributions]]" in [[perturbative quantum field theory]]).

=--

Recall the following general facts about the [[wave equation]]/[[Klein-Gordon equation]]:

+-- {: .num_prop #PropertiesOfTheCausalPropagator}
###### Proposition
**([[causal propagator]])**

Let $(X,g)$ be a [[time orientation|time-oriented]] [[globally hyperbolic spacetime]] and let $m \in \mathbb{R}_{\geq 0}$ (the "[[mass]]"). Then the [[Klein-Gordon equation]]

$$
  (\Box_g + m^2) \phi = 0
$$

(a [[partial differential equation]] on [[smooth functions]] $f \in C^\infty(X,\mathbb{R})$ ) has unique advanced and retarded [[Green functions]] $E^{R/A}$, namely [[continuous linear functionals]]

$$
  E^{A/R}
   \;\colon\;
  C^\infty_c(X)
   \longrightarrow
  C^\infty(X)
$$

(from [[bump functions]] to general [[smooth functions]]) which are [[fundamental solutions]] in that

$$
  (\Box_g + m^2) \circ E^{A/R} = \delta
  \phantom{AAAA}
  E^{A/R} \circ (\Box_g + m^2) = \delta
$$

and which have advanced/retarded [[support of a distribution]] when viewed (via the [[Schwartz kernel theorem]]) as [[distributions]] on the [[Cartesian product]] manifold $X \times X$

$$
  supp( E^{A/R}) \subset \{ (x_1, x_2) \in X \times X  \;\vert\; x_1 \in J^{\mp} (x_2) \}
 \,.
$$

In fact these two fundamental solutions are related by switching their arguments

$$
  E^{A/R}(x_1, x_2) = E^{R/A}(x_2, x_1)
  \,.
$$

Finally their [[wave front set]] is

$$
  WF(E^{A/R})
  \;=\;
  \left\{
   ((x_1, x_2), (k_1, -k_2))
   \;\vert\;
   x_1 \in J^{\mp}(x_2)
   \;\text{and}\;
   \left(
     (x_1, k_1) \sim (x_2, k_2)
   \right)
   \;\text{or}\;
   \left(
     (x_1 = x_2)
     \,\text{and}\,
     k_1 = -k_2
   \right)
  \right\}
  \,.
$$

Here the [[relation]] $(x_1, k_1) \sim (x_2, k_2)$ means that there exists a [[lightlike]] [[geodesic]] from $x_1$ to $x_2$ with cotangent vector $k_1$ at $x_1$ and $k_2$ at $x_2$.

It follows that the [[wave front set]] of their difference (the [[causal propagator]])

$$
  E \;\coloneqq\; E^A - E^R
$$

is

$$
  WF(E)
  \;=\;
  \left\{
    ((x_1 x_2), (k_1, -k_2))
    \;\vert\;
    (x_1, k_1) \sim (x_2, k_2)
  \right\}
  \,.
$$

This causal propagator gives the [[Poisson bracket]] on the [[covariant phase space]] of the [[free field|free]] [[scalar field]] in that, as [[distributions]]

$$
  \left\{
    \Phi(x_1)
    ,
    \Phi(x_2)
  \right\}
  \;=\;
  E(x_1, x_2)
  \,,
$$

where on the left $\{-,-\}$ is the Poisson bracket and $\Phi(x)$ is the point evaluation function from def. \ref{PointEvaluationObservable}. This means that on the algebra $\mathcal{F}_{reg}$ of regular functionals from def. \ref{SmoothFunctionalsOnSmoothFunctions} the bracket is given by

$$
  \{\Phi(f_1), \Phi(f_2)\}
  \;=\;
  \langle E, f_1 \cdot f_2 \rangle
  \,.
$$

=--

The point now is that:

+-- {: .num_remark}
###### Remark

The algebra $\mathcal{F}_{reg}$ of regular functionals (def. \ref{SmoothFunctionalsOnSmoothFunctions}) is too small a subalgebra of all smooth functionals on $C^\infty(X)$ to be of interest (for instance the point [[interaction]] terms such as $g\Phi(x)^n \colon \phi \mapsto \int_X g(x) (\phi(x))^x dvol$ (for $g$ an [[adiabatic switching]] [[coupling constant]]) needed for [[phi^4 theory]] etc. are not contained). On the other hand $\mathcal{F}_{dist}$ is too large: extending the above Poisson bracket to this algebra would mean to form a [[product of distributions]] with $E$, and in general this is not defined.

But the obstruction to this product being defined is well characterized: One may multiply with $E$ all those distributions $f$ such that the sum of the [[wave front sets]] $WF(E) + WF(f)$ does not intersect the zero-section.

Therefore if $E$ could be modified such that its wave front set shrinks, then this variant may be applied to larger subalgebras of smooth functionals. Now def. \ref{WickAlgebraOfAlmostKaehlerVectorSpace} suggests that sensible modifications of the [[causal propagator]] are those by adding distributions $H$ on $X^2$ that are _symmetric_ in their two arguments.

=--

Such distributions are quasi-free Hadamard states:

+-- {: .num_defn #HadamardDistribution}
###### Definition
**([[quasi-free Hadamard state]])

Let $(X,g)$ be a [[time orientation|time oriented]] [[globally hyperbolic spacetime]].

A _[[Hadamard 2-point function]]_ for the [[free field|free]] [[scalar field]] on $(X,g)$ is a [[distribution]]

$$
  \pi \in \mathcal{D}'(X \times X)
$$

on the [[Cartesian product]] manifold such that


1. the anti-symmetric part of $\pi$ is the [[causal propagator]] $E$ (from prop. \ref{PropertiesOfTheCausalPropagator})

   $$
     \pi(x_1, x_2) - \pi(x_2, x_1)
     \;=\;
     i E(x_1, x_2)
   $$

1. the [[wave front set]] is one causal half that of the causal propagator:

   $$
     WF(\pi)
     \;=\;
     \left\{
       ((x_1, x_2), (k_1, -k_2))
       \;\vert\;
       (x_1, k_1) \simeq (x_2, k_2)
       \;\;\text{and}\;\;
       k_1 \in V_{x_1}^+
     \right\}
   $$

1. (Klein-Gordon bi-solution) $(\Box_g - m^2) \pi(-,x) = 0$ and $(\Box_g - m^2)\pi(x,-) = 0$, for all $x \in X$;

1. (positive semi-definiteness) For any complex-valued [[bump function]] $b$ we have that

   $$
     \int_{X \times X} b^\ast(x) \pi(x,y) b(y) \, dvol(x) dvol(y)
     \;\coloneqq\;
     \langle \pi, b^\ast \otimes b \rangle
     \;\geq\; 0
   $$

=--

+-- {: .num_prop #ExistenceOfHadamardDistributions}
###### Proposition
**(existence of Hadamard distributions)

Let $(X,g)$ be a [[globally hyperbolic spacetime]]. Then a [[Hadamard distribution]] $\pi$ according to def. \ref{HadamardDistribution} does exist.

=--

([Radzikowski 96](Hadamard+distribution#Radzikowski96))



#### Wick algebra in field theory
 {#WickAlgebraInFieldTheory}

+-- {: .num_defn #MicrocausalFunctionals}
###### Definition
**([[microcausal functionals]])**

Let $(X,g)$ be a [[globally hyperbolic spacetime]].

Write $\mathcal{F}_{mc} \subset \mathcal{F}_{dist}$ for the subalgebra of smooth functionals

$$
  C^\infty(X) \longrightarrow \mathbb{R}
$$

on the [[smooth space]] of smooth functions on $X$ which is generated from those [[distributions]] on some Cartesian product $X^n$ (as in def. \ref{SmoothFunctionalsOnSmoothFunctions}) whose [[wave front set]] excludes those covectors to a point in $X^n$ all whose components are in the [[future cone]] or all whose components are in the [[past cone]].

=--

(After [[deformation quantization]] below, the [[distributions]] appearing in def. \ref{MicrocausalFunctionals} are the origin of "[[operator-valued distributions]]" in [[perturbative quantum field theory]]).


+-- {: .num_example }
###### Example
**(regular functionals are microcausal)**

Every regular functional (def. \ref{SmoothFunctionalsOnSmoothFunctions}) is a [[microcausal functional]] (def. \ref{MicrocausalFunctionals}), since the [[wave front set]] of a distribution that is given by an ordinary function is empty:

$$
  \mathcal{F}_{reg} \subset \mathcal{F}_{mc}
  \,.
$$

=--

+-- {: .num_example}
###### Example
**([[adiabatic switching|adiabtaically switched]] point interactions are microcausal)**

Let $g \in C^\infty_c(X)$ be a [[bump function]], then for $n \in \mathbb{N}$ the smooth functional

$$
  \array{
    C^\infty(X) &\overset{}{\longrightarrow}& \mathbb{R}
    \\
    \phi &\mapsto& \int_X g(x) (\phi(x))^n dvol(x)
  }
$$

is a [[microcausal functional]] (def. \ref{MicrocausalFunctionals}).

If here we think of $\phi(x)^n$ as a point-[[interaction]] term (as for instance in [[phi^4 theory]]) then $g$ is to be thought of as an "[[adiabatic switching|adiabatically switched]]" [[coupling constant]]. These are the relevant interaction terms to be quantized via [[causal perturbation theory]].

=--

+-- {: .proof}
###### Proof

For notational convenience, consider the case $n = 2$, the other cases are directly analogous. The distribution in question is the [[delta distribution]]

$$
  \int_X g(x) \phi(x)^2 dvol(x)
  \;=\;
  \int_{X \times X} g(x_1) \phi(x_1) \phi(x_2) dvol(x_1) dvol(x_2)
  =
  \langle g \cdot \delta(-,-) , (\phi \circ pr_1)\cdot (\phi \circ pr_2)  \rangle_g
  \,.
$$

Now for $(x_1, x_2) \in X \times X$ and $\mathbb{R}^{2n} \simeq U \subset X \times X$ a [[chart]] around this point,  the [[Fourier transform]] of $g \cdot \delta(-,-)$ restricted to this chart is proportional to the Fourier transform $\hat g$ of $g$ evaluated at the sum of the two covectors:

$$
  \begin{aligned}
    (k_1, k_2)
      & \mapsto
     \int_{\mathbb{R}^{2n}} g(x_1) \delta(x_1, x_2) \exp( k_1 \cdot x_1 + k_2 \cdot x_2 ) dvol(x_1) dvol(x_2)
    \\
    & \propto \hat g(k_1 + k_2)
   \end{aligned}
  \,.
$$


Since $g$ is a plain [[bump function]], its Fourier transform $\hat g$ is quickly decaying (in the sense of wave front sets)  with $k_1 + k_2$ ([this prop.](wavefront+set#EmptyWaveFronSetCorrespondsToOrdinaryFunction)). Thus only on the cone $k_1 + k_2 = 0$ that function is in fact constant and in particular not decaying.


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/WaveFrontSetOfDeltaDistributionInTwoVariables.png" width="200"/>
</div>

{#WaveFrontOfdeltaxy} This means that the wave front set consists of the element of the form $(x, (k, -k))$ with $k \neq 0$. Since $k$ and $-k$ are both in the [[future cone]] or both in the past cone precisely if $k = 0$, this situation is excluded in the wave front set and hence the distribution $g \cdot \delta(-,-)$ is microcausal.

> (graphics grabbed from [Khavkine-Moretti 14, p. 45](quasi-free+quantum+state#KhavkineMoretti14))

=--

This shows that microcausality in this case is related to conservation of momentum in the point interaction.

More generally:


+-- {: .num_example #CompactlySupportedPolynomialLocalDensities}
###### Example
**(compactly supported polynomial [[local observables]])**

Write

$$
  \Pi_{poly}^{h,v}(E)
$$

for the space of differential forms on the [[jet bundle]] of $E$ which locally are [[polynomials]]
in the field variables.

$$
  \mathcal{F}_{loc}
    \; \subset \;
  C^\infty_c(\Sigma) \underset{\Pi_{poly}^{0,0}(E)}{\otimes} \Pi_{poly}^{d,0}(E)
$$

for the subspace of [[horizontal differential forms]] of degree $d$ on the [[jet bundle]] ([[local Lagrangian densities]])
of those which are [[compact support|compactly supported]] with respect to $\Sigma$ and [[polynomial]] with respect to the
field variables ([[local observables]]).

Every $L \in \mathcal{F}_{loc}$ induces a functional

$$
   \Gamma_\Sigma(E) \longrightarrow \mathbb{R}
$$

by [[integration of differential forms|integration]] of the [[pullback of differential forms|pullback]]
of $L$ along the [[jet prolongation]] of a given [[section]]:

$$
  \phi \mapsto \int_{\Sigma} j^\infty(\phi)^\ast L
  \,.
$$

These functionals happen to be [[microcausal functional|microcausal]], so that there is an inclusion

$$
  \mathcal{F}_{loc} \hookrightarrow \mathcal{F}_{mc}
$$

into the space of [[microcausal functionals]]. (See [this example](microcausal+functional#CompactlySupportedPolynomialLocalDensities) at _[[microcausal functional]]_).

=--



+-- {: .num_prop #MoyalStarProductOnMicrocausal}
###### Proposition
**(Hadamard-Moyal star product on microcausal functionals)

Let $(X,g)$ be a [[globally hyperbolic spacetime]], and let $\pi \in \mathcal{D}'(X \times X)$ be a [[Hadamard distribution]] (def. \ref{HadamardDistribution}) which is guaranteed to exist by prop. \ref{ExistenceOfHadamardDistributions}.

Then the [[star product]]

$$
  P_1 \star_\pi P_2
  \;\coloneqq\;
  prod
   \circ
  \exp\left(
    \int_{X^2} \hbar \pi(x_1, x_2) \frac{\delta}{\delta \phi(x_1)}
    \otimes \frac{\delta}{\delta \phi(x_2)} dvol_g
  \right)
  (P_1 \otimes P_2)
$$

on microcausal functionals $P_1, P_2 \in \mathcal{F}_{mc}$ is well defined in that the [[products of distributions]] that appear in expanding out the [[exponential]] are such that the sum of the [[wave front sets]] of the factors does not intersect the zero section.

=--

+-- {: .proof}
###### Proof

By definition of [[Hadamard distribution]], the [[wave front set]] of powers of $\pi$ has all cotangents on the first variables future pointing, and all those on the second variables past pointing. The first variables are integrated against those of $P_1$ and the second against $P_2$. By definition of microcausal functionals, the wave front sets of $P_1$ and $P_2$ are disjoint from the subsets where all components are future pointing or all components are past-pointing. Therefore the relevant sum of of the wave front covectors never vanishes.

See [Collini 16, p. 25-26](#Collini16)

=--

+-- {: .num_defn #WickAlgebraOfFreeQuantumField}
###### Definition
**(Wick algebra of free quantum field)**

Let $(X,g)$ be a [[globally hyperbolic spacetime]] and let $\pi \in \mathcal{D}'(X \times X)$ be a [[Hadamard distribution]] (def. \ref{HadamardDistribution}) which is guaranteed to exist by prop. \ref{ExistenceOfHadamardDistributions}.

Then the _Wick algebra_ of [[quantum observables]] of the [[free field|free]] [[scalar field]] on $(X,g)$ is the space of [[microcausal functionals]] $\mathcal{F}_{mc}$ (def. \ref{MicrocausalFunctionals}) equipped with the Hadamard-Moyal [[star product]] from prop. \ref{MoyalStarProductOnMicrocausal}:

$$
  \mathcal{W}(X,\pi)
  \;\coloneqq\;
  \left(
    \mathcal{F}_{mc}, \star_\pi
  \right)
  \,.
$$

> need to quotient out ideal of elements in the image of $\Box_g - m^2$ to go on [[shell]]

=--

#### In Minkowski spacetime

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

