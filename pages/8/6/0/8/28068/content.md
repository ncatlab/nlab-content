

{:slogan: .un_remark style="border:solid #0000cc;background: #cbe6ef;border-width:1pt;padding:4pt 25pt;margin:5pt 10pt;border-radius:10pt;"}

### Quantum commutators are time-ordered ordinary products of observables
 {#QuantumCommutatorsAreTimeOrderedOrdinaryProducts}
 

{#RelationToOperatorProductAndTimeOrder} The [[path integral]] formulation (and generally the notion of [[time-ordered products]] satisfying the [[Schwinger-Dyson equation]]) reveals the following foundational fact of [[quantum physics]], which is "well known" but not widely appreciated (most textbooks don't mention it).

As slogans, in slightly increasing order of accuracy:

+-- {: slogan}
**Slogan:**
The [[quantum observable|quantum]] ([[linear operator|operator]]) product of [[observables]] is their ordinary product after slightly shifting their [[time]] domains into operator order.

=--

Or more technically:


+-- {: slogan}
**Slogan:**
The operator product $O_2(t) \star O_1(t)$ of observables at equal time $t$ is their ordinary product after slightly shifting the observation $O_2$ to after $O_1$, hence is $\underset{\underset{\epsilon \to_+ 0}{\longrightarrow}}{\lim} O_2(t + \epsilon)  O_1(t)$.

=--

Or rather: 

+-- {: slogan}
**Slogan:**
The non-commutativity of quantum observables (such as witnessed by the [[canonical commutation relation|canonical]] [[commutator]] between [[field observables]] and their [[canonical momenta]]) reflects that the temporal order of observation matters, hence reflects the difference $\underset{\underset{\epsilon \to_+ 0}{\longrightarrow}}{\lim} \big( O_2(t + \epsilon)  O_1(t)  - O_1(t + \epsilon)  O_2(t)\big)$.

=--

Here these (limits of) ordinary products of ordinary observables (on $\mathbb{C}$-valued functions of physical configurations) are to be understood as expectation values as produced by a [[path integral]] with respect to some (arbitrary) state. We proceed to say this in more technical detail. 

This insight goes back to [Feynman 1948 p. 381](path+integral#Feynman48), who considered it in the context of [[non-relativistic particle|non-relativistic]] [[quantum mechanics]], reviewed below in:

* *[In Quantum Mechanics](#CCRFromPathIntegralInQM)*

But this generalizes to [[relativistic quantum field theory|relativistic]] [[quantum field theory|quantum]] [[field theory]], discussed below in:

* *[In Quantum Field Theory](#CCRFromPathIntegralInQFT)*.

In fact, the analogous statement remains true also in [[light-front quantization]] (cf. Rem. \ref{SDCCRDerivationInLightFrontForm} below), where it says that the canonical commutators are given by ordinary products of observables after shifting their *light-front-parameter* domain into operator order.


#### In Quantum Mechanics
 {#CCRFromPathIntegralInQM}

The following is the original observation of [Feynman 1948, p. 381](path+integral#Feynman48). 

(This has been recalled by [Feynman, Hibbs & Styer 2010 (7.45)](path+integral#FeynmanHibbsStyer2010); [Schulman 1981, Ch. 8](path+integral#Shulman1981); [Nagaosa 1999, pp. 33](path+integral#Nagaosa99); [Ong 2012](path+integral#Ong2012); [Rischke 2021 Section 5.6](path+integral#Rischke21
), but all these authors follow Feynman 1948 essentially verbatim. In particular, none actively recognizes the [[Schwinger-Dyson equation]] in the argument nor comments on generalization beyond the 1d discretized nonrelativistic path integral that Feynman considered and which we recall now.)

\linebreak

Consider the [[path integral]] for a [[particle]] propagating on a [[circle]] $S^1$, and approximated by an ordinary [[integral]] over positions $x_t$ at $N$ discrete time steps $t \in \mathbf{N} \coloneqq \{0, 1, \cdots, N-1\}$, hence over discretized trajectories 
$$
  x \colon \mathbf{N} \longrightarrow S^1
  \mathrlap\,.
$$

To recall that the [[quantum probability theory|quantum expectation value]] of an [[observable]] $O \colon (S^1) ^{\mathbf{N}} \longrightarrow \mathbb{C}$ with respect to a [[pure quantum state]] $\psi \colon S^1 \longrightarrow \mathbb{C}$ is expressed as the following (discretized) path integral:
\[
  \label{ExpectationValuesForParticleOnS1ViaDiscretized}
  \big\langle
    O
  \big\rangle
  \;\coloneqq\;
  \tfrac{1}{\mathcal{N}}
  \int   
    O(x) 
   \,
   \exp\big(\tfrac{\mathrm{i}}{\hbar} S(x)\big)
   \,
   \psi^\ast(x_N)
   \psi(x_0)
   \,
   D x
   \mathrlap{\,,}
\]
where 
$$
  \mathcal{N} 
    \coloneqq   
  \int   
   \exp\big(\tfrac{\mathrm{i}}{\hbar} S(x)\big)
   \,
   \psi^\ast(x_N)
   \psi(x_0)
   \,
   D x
$$
is the normalization factor (the "[[partition function]]"), and where
$$
  \int D x 
    \,\coloneqq\,
  \int_{S^1} \cdots \int_{S^1} 
  \mathrm{d}x_0 \cdots \mathrm{d}x_{\mathbf{N}-1}
  \mathrlap{\,.}
$$

With that simple setup, ordinary [[integration by parts]] gives for an observable which is a [[partial derivative]],
$$
  O(x) 
    \,=\, 
  \tfrac{\partial F}{\partial x_t} (x)
  \,,
  \phantom{--}
  1 \lt t \lt N
  \mathrlap{\,,}
$$
that its [[expectation value]] is equivalently expressed as:
\[
  \label{PartialIntegrationInDiscretizedPathIntegral}
  \begin{aligned}
    \big\langle
      O
    \big\rangle
    & \equiv
    \big\langle
      \tfrac{\partial F}{\partial x_t}
    \big\rangle
    \\   
    & 
    -\tfrac{\mathrm{i}}{\hbar}
    \big\langle
      F
      \tfrac{\partial S}{\partial x_t} 
    \big\rangle
  \end{aligned}
\]
(which we may recognize as the 1d discretized form of what is now called the *[[Schwinger-Dyson equation]]* in [[quantum field theory]] more generally).

Specializing this to the [[free field theory|free]] [[non-relativistic particle]] of [[mass]] $m \gt 0$, for which the discretized [[action functional]] is
$$
  S(x) 
   \,=\,  
  \sum_{1 \leq t \lt N}
  \tfrac{m}{2}
  (
     x_{t+1} 
     - 
     x_{t}
  )^2 
  \tfrac{1}{N}
  \mathrlap{\,,}
$$
the key point to observe is  that 
$$
  \tfrac{\partial S}{\partial x_t}
  \,=\,
  m
  \tfrac{
    (x_{t} - x_{t-1})
  }{1/N}
  -
  m
  \tfrac{
    (x_{t+1} - t_n)
  }{1/N}
  \mathrlap{\,.}
$$

Using this when entering equation (eq:PartialIntegrationInDiscretizedPathIntegral) with the choice
$$
  F 
    \coloneqq 
  x_t
$$ 
 gives:
$$
  \mathrm{i}\hbar
  = 
  \big\langle
    x_t 
    \, 
    m
    \tfrac{
      (x_{t} - x_{t-1})
    }{1/N}
  \big\rangle
  -
  \big\langle
    m
    \tfrac{
      (x_{t+1} - x_{t})
    }{1/N}
    \,
    x_t
  \big\rangle
  \mathrlap{\,.}
$$

Here we recognize
$$
  p_{t+1/2} 
    \coloneqq 
    m
    \tfrac{
      (x_{t+1} - x_{t})
    }
    {1/N}
$$
as the discrete approximation to the [[momentum]] observable at time $t + 1/2$, in terms of which we have found that:
\[
  \label{FeynmanCCRViaTimeShiftedProduct}
  \begin{aligned}
  \mathrm{i}\hbar
  & = 
  \big\langle
    x_t 
    \cdot
    p_{t - 1/2}
    \,-\,
    p_{t + 1/2}
    \cdot
    x_t 
  \big\rangle
  \,.
  \end{aligned}
\]
In the time continuum limit, this becomes
$$
  \mathrm{i}\hbar
  \,=\, 
  \big\langle
    x_t 
    \cdot
    p_{t - \epsilon}
    \,-\,
    p_{t + \epsilon}
    \cdot
    x_t 
  \big\rangle
$$
for $\epsilon \to 0$.

But this is clearly the path integral expression for what in operator formalism is the [[canonical commutation relation]]
$$
  \mathrm{i}\hbar
  =
  \hat x \cdot \hat p - \hat p \cdot \hat x
  \,.
$$

In conclusion, the observable corresponding to a quantum operator product $B \cdot A$ of observables at times $t$ may be thought of as the result of first shifting the temporal supports of the observables so that  $B$ is observation at a time just a little *after* that of $A$, and then forming the ordinary product of observed values. 

As Feynman 1948 also noticed, the same conclusion holds with an ordinary [[potential energy]] term included in the [[action functional]], since its contribution is non-singular and hence vanishes in the final $\epsilon\to 0$ limit.


#### In Quantum Field Theory
 {#CCRFromPathIntegralInQFT}

In fact, by using the [[Schwinger-Dyson equation]], this argument generalizes (cf. [physics.SE:685812](https://physics.stackexchange.com/a/685812/5603)) from the [[quantum mechanics]] of a [[nonrelativistic particle]] to general [[quantum field theories]] with ordinary [[potential energy]] terms, as follows.

> (Conversely, the product of [[observable]]-values in the path integral corresponds to the [[time-ordered product]] of the corresponding [[linear operators]] (eg. [Polchinski 1998 (A.1.17)](path+integral#Polchinski98); [Rischke 2021 (5.63)](path+integral#Rischke21).)


Imagine a [[path integral]]-formulation exists of some $1+d$-dimensional [[quantum field theory]] determined by a [[Lagrangian density]] $L$ with an ordinary [[potential energy]] term and denote the corresponding [[expectation values]] in some state by $\langle-\rangle$ --- or else regard $\langle-\rangle$ as denoting the [[time-ordered product]] of its arguments, that's all we need.

Let $\phi$ be one of the [[field (physics)|field]] species. (It could be a [[scalar field]] but it may just as well be a component of any more complex field.)

Assuming we are on cylindrical [[Minkowski spacetime]] $\mathbb{R}^{1,d} / \mathbb{Z}^{d}$ --- just for notational simplicity --- then the [[Schwinger-Dyson equation]] for field insertion $\phi(y)$ says that

\[
  \label{SchwingerDysonForComputingCCRs}
  \bigg\langle
    \underset
    { 
      \delta S / \delta \phi(x) 
    }{
      \underbrace{
        \Big(
        \frac{ \partial L }{ \partial \phi }
        (x)
        -
        \partial_\mu 
        \frac{ \partial L }{ \partial (\partial_\mu \phi) }
        \Big)
      }
    }
    \,
    \phi(y)
  \bigg\rangle
  \;=\;
  \mathrm{i}\hbar
  \left\langle
    \frac{ \partial \phi(y) }{ \partial \phi}(x)
  \right\rangle
  \;=\;
  \mathrm{i}\hbar
  \,
  \delta^{1+d}(x-y)
  \mathrlap{\,.}
\]

> This is the field theoretic version of Feynman's equation (eq:PartialIntegrationInDiscretizedPathIntegral) above.

Now consider the [[integration]] of this expression in the variable $x$ over the spacetime region in a small time interval $(y^0- \epsilon, y^0 + \epsilon) \times \mathbb{R}^{d}/\mathbb{Z}^{d}$ and let $\epsilon \to 0$. Then: 

1. the first summand on the left of (eq:SchwingerDysonForComputingCCRs) vanishes (being asymptotically proportional to $\epsilon$ since we are assuming that the potential term and hence the $\phi$-dependence of $L$ is that of an ordinary smooth function), 

1. by [[Stokes's theorem]] the spatial integral over the spatial components of the second summand vanishes and

1. the remaining temporal integral of its temporal component gives two boundary terms (where we now decompose $x = (x^0, \vec x)$):

\[
  \label{IntegratedSchwingerDysonForComputingCCRs}
  \underset{\underset{\epsilon\to 0}{\longrightarrow}}{\lim}
  \int_{\mathbb{R}^{d}/\mathbb{Z}^{d}}
  \mathrm{d}^d \vec x
  \,
  \left\langle
    \frac{ \partial L }{ \partial (\partial_0 \phi) }
    (y^0 + \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
    \;-\;
    \frac{ \partial L }{ \partial (\partial_0 \phi) }
    (y^0 - \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
  \right\rangle
  \;=\;
  -\mathrm{i}\hbar
  \mathrlap{\,.}
\]

Here we recognize the [[canonical momentum]] $\pi$ to the field $\phi$:

$$
  \pi(x)
  \;\coloneqq\;
  \frac{ \partial L }{ \partial (\partial_0 \phi) }(x)
  \mathrlap{\,,}
$$

so that

\[
  \label{IntegratedSchwingerDysonForComputingCCRsViaMomenta}
  \underset{\underset{\epsilon\to 0}{\longrightarrow}}{\lim}
  \int_{\mathbb{R}^{d}/\mathbb{Z}^{d}}
  \mathrm{d}^d x
  \,
  \Big\langle
    \pi(y^0 + \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
    \;-\;
    \pi(y^0 - \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
  \Big\rangle
  \;=\;
  -\mathrm{i}\hbar
  \mathrlap{\,.}
\]

> This is the field-theoretic version of Feynman's equation (eq:FeynmanCCRViaTimeShiftedProduct) above.

We may redo this derivation  after multiplication of the original Schwinger-Dyson equation (eq:SchwingerDysonForComputingCCRs) with any "smearing function" $f(\vec x)$ (a spatial [[bump function]]). Then where we used [[Stokes' theorem]] above we are now faced with an [[integration by parts]] that picks up terms proportional to the [[gradient]] of $f$ --- but if the dependence of $L$ on spatial derivatives of $\phi$ does not have unusual singularities (i.e. if the [[kinetic energy]] term in $L$ is a standard one) then these terms vanish with $\epsilon$ just as the [[potential energy]] term does, and hence we end up with

\[
  \label{IntegratedSchwingerDysonForComputingCCRsViaMomenta}
  \underset{\underset{\epsilon\to 0}{\longrightarrow}}{\lim}
  \int_{\mathbb{R}^{d}/\mathbb{Z}^{d}}
  \int \mathrm{d}^d \vec x
  \,
  f(\vec x)
  \,
  \Big\langle
    \pi(y^0 + \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
    \;-\;
    \pi(y^0 - \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
  \Big\rangle
  \;=\;
  -\mathrm{i}\hbar f(\vec y)
  \mathrlap{\,.}
\]

But since this holds for all smearing functions $f$, this is equivalent to the [[distribution|distributional]] equation
\[
  \label{UnIntegratedSchwingerDysonForComputingCCRsViaMomenta}
  \underset{\underset{\epsilon\to 0}{\longrightarrow}}{\lim}
  \Big\langle
    \pi(y^0 + \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
    \;-\;
    \pi(y^0 - \epsilon, \vec x)
    \,
    \phi(y^0, \vec y)
  \Big\rangle
  \;=\;
  -\mathrm{i}\hbar 
  \,
  \delta^d(\vec x - \vec y)
  \mathrlap{\,,}
\]
which is the claimed incarnation of the [[canonical commutation relation]] of field operators at equal times,
$$
  \big[
    \widehat{\pi}(\vec x), \widehat{\phi}(\vec x)
  \big]
  \,=\, 
  -\mathrm{i}\hbar 
  \,
  \delta^d(\vec x - \vec y)
  \mathrlap{\,,}
$$
now re-expressed as an expectation value of ordinary products of observables after shifting their temporal domains into operator order.


\begin{remark}\label{SDCCRDerivationInLightFrontForm}
The analogous conclusion holds also for **[[light front quantization]]**, with the role of the time coordinate $x^0$ now played by the light front parameter $x^+$, for 
$$
  x^\pm \coloneqq (x^0 \pm x^d)/\sqrt{2}
  \,.
$$

Here the light-front [[canonical momentum]] to a field $\phi$ is (cf. [Burkardt 1996 table 2.1](light+front+quantization#Burkardt96) for the following equations):
$$
  \pi 
    \,=\, 
  \frac
    { \partial L }
    { \partial (\partial_+ \phi) }
  \mathrlap{\,,}
$$
which for [[Lagrangian densities]] with standard [[kinetic energy]] term 
$$
  L 
    \,=\, 
  \partial_+ \phi \, \partial_- \phi 
    \,-\, 
  \tfrac{1}{2} (\vec \nabla_\perp \phi)^2 - V(\phi)
$$
comes out as
$$
  \pi 
    \,=\, 
  \partial_- \phi
  \mathrlap{\,.}
$$
While the nature of this light front momentum in [[canonical quantization]] (where it is a [[second class constraint]]) is quite different from the nature of the [[canonical momentum]] in instant form, at the end the equal-LF-parameter commutation relation has the same form as the usual equal-time commutator:
$$
  \Big[
     \widehat{\pi}\big(x^+, x^-, \vec x_\perp\big)
     ,\,
     \widehat{\phi}\big(x^+, y^-, \vec y_\perp\big)
  \Big]
  \,=\,
  -\mathrm{i}\hbar
  \tfrac{1}{2}
  \delta\big(x^- - y^-\big)
  \delta^{d-1}\big(\vec x_\perp - \vec y_\perp\big)
  \mathrlap{\,.}
$$
And so the above Schwinger-Dyson argument, just with the time coordinate $x^0$ replaced by the light front parameter $x^+$, reproduces this in the form:
\[
  \label{LightFrontUnIntegratedSchwingerDysonForComputingCCRsViaMomenta}
  \begin{array}{l}
  \underset{\underset{\epsilon\to 0}{\longrightarrow}}{\lim}
  \Big\langle
    \pi\big(y^+ + \epsilon, x^-, \vec x_\perp\big)
    \,
    \phi\big(y^+, y^-, \vec y_\perp\big)
    \;-\;
    \pi\big(y^+ - \epsilon, x^-, \vec x_\perp\big)
    \,
    \phi\big(y^+, y^-, \vec y_\perp\big)
  \Big\rangle
  \\
  \;=\;
  -\mathrm{i}\hbar 
  \,
  \tfrac{1}{2}
  \delta(x^- - y^-)
  \delta^{d-1}(\vec x_\perp - \vec y_{\perp})
  \mathrlap{\,.}
  \end{array}
\]

(Just beware the somewhat subtle factor of $1/2$ on the right of (eq:LightFrontUnIntegratedSchwingerDysonForComputingCCRsViaMomenta). In the constrained canonical quantization this factor may be found discussed carefully in [Burkardt 1996 §A p. 76](light+front+quantization#Burkardt96). In the path integral picture the factor arises more transparently as a factor of $2$ on the left, originating in: 
$
  \delta(\partial_+ \phi \partial_- \phi)/\delta\phi
  =
  -\partial_+ \partial_- \phi - \partial_- \partial_+ \phi
  =
  -2 \partial_+ \partial_- \phi
$.)

\end{remark}


\linebreak




\linebreak
