## Free quantum fields
 {#FreeQuantumFields}

We discuss here the [[quantum observables]] for the special case of
[[free field theories]] (def. \ref{FreeFieldTheory}). In [[perturbative quantum field theory]] this is the
basis of the construction of all [[interaction|interacting]] theories in the [[infinitesimal neighbourhood]]
of the [[free field theories]].


$\,$

[[!include Wick algebra -- table]]

$\,$

We now discuss these topics

* _[Wick algebra and normal ordered products](#WickAlgebraAndNormalOrderedProducts)_




$\,$



$\,$

**[[Wick algebra]] and [[normal ordered products]]**
 {#WickAlgebraAndNormalOrderedProducts}




+-- {: .num_defn #MicrocausalObservable}
###### Definition
**([[microcausal observable]])**

For $\Sigma$ a [[spacetime]], hence a [[Lorentzian manifold]] with [[time orientation]], then a _[[microcausal observable]]_ is a [[polynomial observable]] (def. \ref{PolynomialObservable}) such that each [[coefficient]] $\alpha^{(k)}$ has [[wave front set]] excluding those points  where all $k$ [[wave vectors]] are in the [[future cone]] or all in the [[past cone]].

=--

(After [[deformation quantization]] below, the [[distributions]] appearing in def. \ref{MicrocausalFunctionals} are the origin of "[[operator-valued distributions]]" in [[perturbative quantum field theory]]).


+-- {: .num_example }
###### Example
**(regular functionals are microcausal)**

Every regular functional is a [[microcausal functional]] (def. \ref{MicrocausalFunctionals}), since the [[wave front set]] of a distribution that is given by an ordinary function is empty:

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

This shows that microcausality in this case is related to conservation of momentum in th point interaction.

More generally:



+-- {: .num_prop #MoyalStarProductOnMicrocausal}
###### Proposition
**(Hadamard-Moyal star product on microcausal functionals)**

Let $(X,g)$ be a [[globally hyperbolic spacetime]], and let $\omega \in \mathcal{D}'(X \times X)$ be a [[Hadamard distribution]] (def. \ref{HadamardDistribution}) which is guaranteed to exist by prop. \ref{ExistenceOfHadamardDistributions}.

Then the [[star product]]

$$
  P_1 \star_\omega P_2
  \;\coloneqq\;
  prod
   \circ
  \exp\left(
    \int_{X^2} \hbar \omega(x_1, x_2) \frac{\delta}{\delta \phi(x_1)}
    \otimes \frac{\delta}{\delta \phi(x_2)} dvol_g
  \right)
  (P_1 \otimes P_2)
$$

on microcausal functionals $P_1, P_2 \in \mathcal{F}_{mc}$ is well defined in that the [[products of distributions]] that appear in expanding out the [[exponential]] are such that the sum of the [[wave front sets]] of the factors does not intersect the zero section.

=--

+-- {: .proof}
###### Proof

By definition of [[Hadamard distribution]], the [[wave front set]] of powers of $\omega$ has all cotangents on the first variables future pointing, and all those on the second variables past pointing. The first variables are integrated against those of $P_1$ and the second against $P_2$. By definition of microcausal functionals, the wave front sets of $P_1$ and $P_2$ are disjoint from the subsets where all components are future pointing or all components are past-pointing. Therefore the relevant sum of of the wave front covectors never vanishes.

See [Collini 16, p. 25-26](Hadamard+distribution#Collini16)

=--

+-- {: .num_defn #WickAlgebraOfFreeQuantumField}
###### Definition
**([[Wick algebra]] of [[free quantum field]])**

Let $(X,g)$ be a [[globally hyperbolic spacetime]] and let $\omega \in \mathcal{D}'(X \times X)$ be a [[Hadamard distribution]] (def. \ref{HadamardDistribution}) which is guaranteed to exist by prop. \ref{ExistenceOfHadamardDistributions}.

Then the _Wick algebra_ of [[quantum observables]] of the [[free field|free]] [[scalar field]] on $(X,g)$ is the space of [[microcausal functionals]] $\mathcal{F}_{mc}$ (def. \ref{MicrocausalFunctionals}) equipped with the Hadamard-Moyal [[star product]] from prop. \ref{MoyalStarProductOnMicrocausal}:

$$
  \mathcal{W}(X,\omega)
  \;\coloneqq\;
  \left(
    \mathcal{F}_{mc}, \star_\omega
  \right)
  \,.
$$

> need to quotient out ideal of elements in the image of $\Box_g + m^2$ to go on [[shell]]

=--


In [[Minkowski spacetime]] the [[Hadamard state]] is simply the usual [[vacuum state]] $\vert vac \rangle$, hence the [[Hadamard distribution]] is, as a [[generalized function]]

$$
  \omega(x,y) = \langle vac \vert \Phi(x) \Phi(y) \vert vac \rangle
  \,.
$$


Therefore the abstractly defined Wick algebra as in def. \ref{WickAlgebraOfFreeQuantumField} in this case satisfies the relation

$$
  \int_{X} f(x,y)  \;  :\Phi(x): \,  :\Phi(y): \; dvol_g
  \;=\;
  \int_X f(x,y) \left( :\Phi(x) \Phi(y): -  \langle vac \vert \Phi(x) \Phi(y) \vert vac \rangle \right)  \; dvol_g
  \,.
$$

This is the traditional expression for the normal ordered Wick product on Minkowski spacetime (e.g. [here](https://en.wikipedia.org/wiki/Normal_order#Free_fields)).

(...)

$\,$
