
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Harmonic analysis
+-- {: .hide}
[[!include harmonic analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Idea
 {#Idea}

### Basic idea

Generally, a _Fourier transform_ is an [[isomorphism]] between the algebra of [[complex numbers|complex]]-valued [[functions]] on a suitable [[topological group]] and a [[convolution product]]-algebra structure on the [[Pontrjagin dual]] group.
The study of Fourier transforms is also called _Fourier analysis_.

Typically, such as in the case over [[Cartesian space]] (def. \ref{FourierTransformSmoothFunctionsWithRapidlyDecayingDerivativesOnCartesianSpace} below) this means to decompose
any suitable [[function]] as a [[superposition]] of _[[complex number|complex]] [[plane waves]]_, which may be thought of as the 
"harmonics" of the given function. Therefore one speaks of _[[harmonic analysis]]_. 

### Generalizations

The concept of Fourier transforms of functions generalizes in a variety of ways. Core part of the subject of Fourier analysis
is the generalization to _[[Fourier transform of distributions]]_ (def. \ref{FourierTransformOnTemperedDistributions} below).
The asymptotic growth of the [[Fourier transform of distributions]] reflects the singularity structure of the distributions,
in dependence of the [[direction of a vector|direction]] of the [[wave vector]] (the "[[wave front set]]"). The study of this behaviour is called _[[microlocal analysis]]_.

If the role of complex [[plane waves]] in the Fourier transform are replaced by [[wavelets]], one speaks of the _[[wavelet transform]]_.

For [[noncommutative topology|noncommutative topological]] groups, instead of continuous characters one should consider [[irreducible representation|irreducible]]  [[unitary representations]], which makes the subject much more difficult. There are also generalizations in [[noncommutative geometry]], see _[[quantum group Fourier transform]]_.



## General definition


Let $G$ be a [[locally compact space|locally compact]] [[Hausdorff topological space|Hausdorff]] [[abelian group|abelian]] [[topological group]] with [[Haar measure|invariant (= Haar) measure]] $\mu$. Then for each $f\in L_1(G,\mu)$, define its __Fourier transform__ $\hat{f}$ as a function on its [[Pontrjagin dual]] group $\hat{G}$ given by

$$
\hat{f}(\chi) = \int_G f(x) \widebar{\chi(x)} d\mu(x),\,\,\,\chi\in\hat{G}.
$$


The Fourier transform of $f\in L_1(G,\mu)$ is always continuous and bounded on $\hat{G}$; the transform of the [[convolution]] of two functions is the product of the transforms of each of the functions separately.



## Over the circle and the integers

In the classical case of __Fourier series__, where $G=\mathbb{Z}$ (the additive group of [[integers]]) and $\hat{G}=S^1$ (the [[circle group]]), the Fourier transform restricts to a unitary operator between the [[Hilbert spaces]] $L_2(S^1,d t)$ and $l_2(\mathbb{Z})$ and the Fourier coefficients are the numbers

$$c_n := \hat{f}(\chi_n) = \int_0^1 f(t) e^{-2\pi i n t} d t,$$

for $n\in\mathbb{Z}$, where the functions $\chi_n(t)= e^{2\pi i n t}$ form an orthonormal basis of $L_2(S^1,d t)$. The Fourier transform $\hat{\chi_n}$ is then viewed as the  $\mathbb{Z}$-series $\delta_n$ which in the $n$-th place has $1$ and elsewhere $0$. The Fourier transform replaces the operator of differentiation $d/d t$ by the operator of multiplication by the series $\{2\pi i n\}_{n\in\mathbb{Z}}$.


## Over compact abelian groups and discrete groups

In general, if $G$ is a [[compact space|compact]] abelian group (whose [[Pontrjagin dual]] is [[discrete group|discrete]]), one can normalize the invariant measure by $\mu(G)=1$ and $\hat{\mu}(X)=card(X)$ for $X\subset\hat{G}$. Then the Fourier transform restricts to a unitary operator from $L_2(X,\mu)$ to $L_2(\hat{G},\hat{\mu})$.


## Over cyclic groups (the discretized circle)

* [[discrete Fourier transform]]

## Over Cartesian spaces
 {#FourierTransformOnCartesianSpaces}

Throughout, let $n \in \mathbb{N}$ and write $\mathbb{R}^n$ for the [[Cartesian space]] of [[dimension]] $n$ and write $(-) \cdot (-)$ for the canonical [[inner product]] on $\mathbb{R}^n$:

$$
  k \cdot x \;\coloneqq\; \underoverset{a = 1}{n}{\sum} k_n x^n
  \,.
$$

In the following by a [[smooth function]] $f \in C^\infty(\mathbb{R}^n)$ on $\mathbb{R}^n$ we mean a smooth function with values in the [[complex numbers]].

For $f \in C^\infty(\mathbb{R}^n)$, we write $f^\ast \in C^\infty(\mathbb{R}^n)$ for its pointwise [[complex conjugate]]:

$$
  f^\ast(x) \coloneqq (f(x))^\ast
  \,.
$$

#### On functions with rapidly decreasing partial derivatives

+-- {: .num_defn #SchwartzSpace}
###### Definition
**([[Schwartz space]] of [[functions with rapidly decreasing partial derivatives]])**


A [[complex number|complex]]-valued [[smooth function]] $f \in C^\infty(\mathbb{R}^n)$ is said to have _[[rapidly decreasing function|rapidly decreasing]] [[partial derivatives]]_ if for all $\alpha,\beta \in \mathbb{N}^{n}$ we have

$$
  \underset{x \in \mathbb{R}^n}{sup} {\vert  x^\beta \partial^\alpha f(x) \vert}
  \;\lt\; \infty
  \,.
$$

Write

$$
  \mathcal{S}(\mathbb{R}^n) \hookrightarrow C^\infty(\mathbb{R}^n)
$$

for the sub-[[vector space]] on the functions with rapidly decreasing partial derivatives regarded as a [[topological vector space]] for the [[Frechet space]] struzcture induced by the [[seminorms]]

$$
  p_{\alpha, \beta}(f) \coloneqq \underset{x \in \mathbb{R}^n}{sup} {\vert  x^\beta \partial^\alpha f(x) \vert}
  \,.
$$

This is also called the _[[Schwartz space]]_.

=--

(e.g. [H&#246;rmander 90, def. 7.1.2](#Hoermander90))

+-- {: .num_example #CompactlySupportedSmoothFunctionsAreFunctionsWithRapidlyDecreasingDerivatives}
###### Example
**([[compactly supported function|compactly supported]] [[smooth function]] are [[functions with rapidly decreasing partial derivatives]])**

Every [[compactly supported function|compactly supported]] [[smooth function]] ([[bump function]]) $b \in C^\infty_{cp}(\mathbb{R}^n)$ rapidly decreasing partial derivatives (def. \ref{SchwartzSpace}):

$$
  C^\infty(\mathbb{R}^n)
   \hookrightarrow
  \mathcal{S}(\mathbb{R}^n)
  \,.
$$

=--



+-- {: .num_prop #ConvolutionProductOnSchwartzSpace}
###### Proposition
**(pointwise product and [[convolution product]] on [[Schwartz space]])

The [[Schwartz space]] $\mathcal{S}(\mathbb{R}^n)$ (def. \ref{SchwartzSpace}) is closed under the following operations on smooth functions $f,g \in \mathcal{S}(\mathbb{R}^n) \hookrightarrow C^\infty(\mathbb{R}^n)$

1. pointwise product:

   $$
     (f \cdot g)(x) \coloneqq f(x) \cdot g(x)
   $$

1. [[convolution product]]:

   $$
     (f \star g)(x) \coloneqq \underset{y \in \mathbb{R}^n}{\int} f(y)\cdot g(x-y) \, dvol(y)
     \,.
   $$

=--


+-- {: .proof}
###### Proof

By the [[product law]] of [[differentiation]].

=--

+-- {: .num_prop #RapidlyDecreasingFunctionsAreIntegrable}
###### Proposition
**([[rapidly decreasing functions]] are [[integrable functions|integrable]])**

Every [[rapidly decreasing function]] $f \colon \mathbb{R}^n \to \mathbb{R}$ (def. \ref{SchwartzSpace}) is an [[integrable function]] in that its [[integral]] exists:

$$
  \underset{x \in \mathbb{R}^n}{\int} f(x) \, d^n x
  \;\lt\;
  \infty
$$

In fact for each $\alpha \in \mathbb{N}^n$ the product of $f$ with the $\alpha$-power of the [[coordinate functions]] exists:

$$
  \underset{x \in \mathbb{R}^n}{\int}
    x^\alpha f(x)\, d^n x
  \;\lt\;
   \infty
  \,.
$$

=--

+-- {: .num_defn #FourierTransformSmoothFunctionsWithRapidlyDecayingDerivativesOnCartesianSpace}
###### Definition
**([[Fourier transform]] of [[functions with rapidly decreasing partial derivatives]])**

The _[[Fourier transform]]_ is the [[continuous linear functional]]

$$
  \widehat{(-)}
    \;\colon\;
  \mathcal{S}(\mathbb{R}^n)
    \longrightarrow
  \mathcal{S}(\mathbb{R}^n)
$$

on the [[Schwartz space]] of [[functions with rapidly decreasing partial derivatives]] (def. \ref{SchwartzSpace}), which is given by [[integration]] against the [[exponential function|exponential]] [[plane wave]] functions

$$
  x \mapsto e^{- i k \cdot x}
$$

times the standard [[volume form]] $d^n x$:

$$
  \label{IntegralExpressionForFourierTransform}
  \hat f(k)
    \;\colon\;
  \int_{x \in \mathbb{R}^n}
    e^{- i \, k \cdot x} f(x) \, d^n x 
  \,.
$$

Here the argument $k \in \mathbb{R}^n$ of the Fourier transform is also called the _[[wave vector]]_.

=--

(e.g. [H&#246;rmander, lemma 7.1.3](#Hoermander90))


+-- {: .num_defn #FourierInversion}
###### Proposition
**([[Fourier inversion theorem]])**

The [[Fourier transform]] $\widehat{(-)}$ (def. \ref{FourierTransformSmoothFunctionsWithRapidlyDecayingDerivativesOnCartesianSpace}) on the [[Schwartz space]] $\mathcal{S}(\mathbb{R}^n)$ (def. \ref{SchwartzSpace}) is an [[isomorphism]], with [[inverse function]] the _[[inverse Fourier transform]]_

$$
  \widecheck {(-)}
     \;\colon\;
  \mathcal{S}(\mathbb{R}^n) \longrightarrow \mathcal{S}(\mathcal{R}^n)
$$

given by

$$
  \widecheck g (x)
    \;\coloneqq\;
   \underset{k \in \mathbb{R}^n}{\int}
      g(k) e^{i k \cdot x}
   \, \frac{d^n k}{(2\pi)^n}
   \,.
$$

Hence in the language of [[harmonic analysis]] the function $\widecheck g \colon \mathbb{R}^n \to \mathbb{C}$ is the [[superposition]] of [[plane waves]] in which the plane wave with [[wave vector]] $k\in \mathbb{R}^n$
appears with [[amplitude]] $g(k)$.

=--

(e.g. [H&#246;rmander, theorem 7.1.5](#Hoermander90))


+-- {: .num_prop #BasicPropertiesOfFourierTransformOverCartesianSpaces}
###### Proposition
**(basic properties of the [[Fourier transform]])**

The [[Fourier transform]] $\widehat{(-)}$ (def. \ref{FourierTransformSmoothFunctionsWithRapidlyDecayingDerivativesOnCartesianSpace}) on the [[Schwartz space]] $\mathcal{S}(\mathbb{R}^n)$ (def. \ref{SchwartzSpace}) satisfies the following properties, for all $f,g \in \mathcal{S}(\mathbb{R}^n)$:

1. (interchanging [[coordinate]] [[multiplication]] with [[partial derivatives]])

   $$
     \label{FourierTransformInterchangesCoordinateProductWithDerivative}
     \widehat{ x^a f } =  + i \partial_a \widehat f
     \phantom{AAAAA}
     \widehat{ - i\partial_a f} = k_a \widehat f
   $$

1. (interchanging pointwise multiplication with [[convolution product]], remark \ref{ConvolutionProductOnSchwartzSpace}):

   $$
     \label{FourierTransformInterchangesPointwiseProductWithConvolution}
     \widehat {(f \star g)} = \widehat{f} \cdot \widehat{g}
      \phantom{AAAA}
      \widehat{ f \cdot g } = (2\pi)^{-n} \widehat{f} \star \widehat{g}
   $$

1. ([[unitary operator|unitarity]], [[Parseval's theorem]])

   $$
     \underset{x \in \mathbb{R}^n}{\int} f(x) g^\ast(x)\, d^n x
     \;=\;
     \underset{k \in \mathbb{R}^n}{\int} \widehat{f}(k) \widehat{g}^\ast(k) \, d^n k
   $$

1. $$
     \label{FourierTransformInIntegralOfProductMayBeShiftedToOtherFactor}
     \underset{k \in \mathbb{R}^n}{\int} \widehat{f}(k) \cdot g(k) \, d^n k
     \;=\;
     \underset{x \in \mathbb{R}^n}{\int} f(x) \cdot \widehat{g}(x) \, d^n x
   $$

=--

(e.g [H&#246;rmander 90, lemma 7.1.3, theorem 7.1.6](#Hoermander90))



#### On tempered distributions
 {#FourierTransformOnTemperedDistributionsOverCartesianSpace}

The [[Schwartz space]] of [[functions with rapidly decreasing partial derivatives]] (def. \ref{SchwartzSpace})
serves the purpose to support the [[Fourier transform]] (def. \ref{FourierTransformSmoothFunctionsWithRapidlyDecayingDerivativesOnCartesianSpace})
together with its inverse (prop. \ref{FourierInversion}), but for many applications 
one needs to apply the Fourier transform to more general functions, and in fact to _[[generalized functions]]_
in the sense of [[distributions]] (via [this prop.](non-singular+distribution#NonSingularDistributionsAreDenseInAllDistributions)).
But with the [[Schwartz space]] in hand, this generalization is readily obtained by [[formal duality]]:


+-- {: .num_defn #TemperedDistribution}
###### Definition
**([[tempered distribution]])**

A _[[tempered distribution]]_ is a [[continuous linear functional]]

$$
  u \;\colon\; \mathcal{S}(\mathbb{R}^n) \longrightarrow \mathbb{C}
$$

on the [[Schwartz space]] (def. \ref{SchwartzSpace}) of [[functions with rapidly decaying partial derivatives]]. The [[vector space]] of all tempered distributions is canonically a [[topological vector space]] as the [[dual space]] to the [[Schwartz space]], denoted

$$
  \mathcal{S}'(\mathbb{R}^n)
    \;\coloneqq\;
  \left(
     \mathcal{S}(\mathbb{R}^n)
  \right)^\ast
  \,.
$$

=--

e.g. ([H&#246;rmander 90, def. 7.1.7](#Hoermander90))


+-- {: .num_example #SomeNonSingularTemperedDistributions}
###### Example
**(some [[non-singular distribution|non-singular]] [[tempered distributions]])**

Every [[function with rapidly decreasing partial derivatives]] $f \in \mathcal{S}(\mathbb{R}^n)$ (def. \ref{SchwartzSpace}) induces a [[tempered distribution]] $u_f \in \mathcal{S}'(\mathbb{R}^n)$ (def. \ref{TemperedDistribution}) by [[integration|integrating]] against it:

$$
  u_f \;\colon\; g \mapsto \underset{x \in \mathbb{R}^n}{\int} g(x) f(x)\, d^n x
  \,.
$$

This construction is a linear inclusion

$$
  \mathcal{S}(\mathbb{R}^n) \overset{\text{dense}}{\hookrightarrow} \mathcal{S}'(\mathbb{R}^n)
$$

of the [[Schwartz space]] into its [[dual space]] of [[tempered distributions]]. This is a [[dense subspace]] inclusion.

In fact already the restriction of this inclusion to the [[compactly supported function|compactly supported]] [[smooth functions]] (example \ref{CompactlySupportedSmoothFunctionsAreFunctionsWithRapidlyDecreasingDerivatives}) is a [[dense subspace]] inclusion:

$$
  C^\infty_{cp}(\mathbb{R}^n)
    \overset{dense}{\hookrightarrow}
  \mathcal{S}'(\mathbb{R}^n)
  \,.
$$

This means that every [[tempered distribution]] is a [[limit of a sequence|limit]] of a [[sequence]] 
of ordinary [[functions with rapidly decreasing partial derivatives]], and in fact even the [[limit of a sequence|limit]]
of a [[sequence]] of [[compactly supported function|compactly supported]] [[smooth functions]] ([[bump functions]]).

It is in this sense that [[tempered distributions]] are "generalized functions".

=--

(e.g. [H&#246;rmander 90, lemma 7.1.8](#Hoermander90))

+-- {: .num_example #CompactlySupportedDistibutionsAreTemperedDistributions}
###### Example
**([[compactly supported distributions]] are [[tempered distributions]])**

Every [[compactly supported distribution]] is a [[tempered distribution]] (def. \ref{TemperedDistribution}), 
hence there is a [[linear map|linear]] [[injection|inclusion]]

$$
  \mathcal{E}'(\mathbb{R}^n)
    \hookrightarrow
  \mathcal{S}'(\mathbb{R}^n)
  \,.
$$

=--




+-- {: .num_example #DiracDeltaDistribution}
###### Example
**([[delta distribution]])

Write

$$
 \delta_0(-) \;\in\; \mathcal{E}'(\mathbb{R}^n)
$$

for the [[distribution]] given by point evaluation of functions at the origin of $\mathbb{R}^n$:

$$
  \delta_0(-) \;\colon\; f \mapsto f(0)
  \,.
$$

This is clearly a [[compactly supported distribution]]; hence a [[tempered distribution]] by example \ref{CompactlySupportedDistibutionsAreTemperedDistributions}.

We write just "$\delta(-)$" (without the subscript) for the corresponding [[generalized function]] (example \ref{SomeNonSingularTemperedDistributions}),  so that

$$
  \underset{x \in \mathbb{R}^n}{\int} \delta(x) f(x) \, d^n x
  \;\coloneqq\;
  f(0)
  \,.
$$

=--



+-- {: .num_example #SquareIntegrableFunctionsInduceTemperedDistributions}
###### Example
**([[square integrable functions]] induce [[tempered distributions]])**

Let $f \in L^p(\mathbb{R}^n)$ be a function in the $p$th [[Lebesgue space]], e.g. for $p = 2$ this means that $f$ is a [[square integrable function]]. Then the operation of [[integration]] against the [[measure]] $f dvol$

$$
  g \mapsto \underset{x \in \mathbb{R}^n}{\int} g(x) f(x) \, d^n x
$$

is a [[tempered distribution]] (def. \ref{TemperedDistribution}).

=--

(e.g. [H&#246;rmander 90, below lemma 7.1.8](#Hoermander90))

Property (eq:FourierTransformInIntegralOfProductMayBeShiftedToOtherFactor) of the ordinary [[Fourier transform]] on [[functions with rapidly decreasing partial derivatives]] motivates and justifies the fullowing generalization:


+-- {: .num_defn #FourierTransformOnTemperedDistributions}
###### Definition
**([[Fourier transform of distributions]] on [[tempered distributions]])**

The _[[Fourier transform of distributions]]_ of a [[tempered distribution]] $u \in \mathcal{S}'(\mathbb{R}^n)$ (def. \ref{TemperedDistribution}) is the [[tempered distribution]] $\widehat u$ defined on a smooth function $f \in \mathcal{S}(\mathbb{R}^n)$ in the [[Schwartz space]] (def. \ref{SchwartzSpace}) by

$$
  \widehat{u}(f) \;\coloneqq\; u\left( \widehat f\right)
  \,,
$$

where on the right $\widehat f \in \mathcal{S}(\mathbb{R}^n)$ is the [[Fourier transform]] of functions from def. \ref{FourierTransformSmoothFunctionsWithRapidlyDecayingDerivativesOnCartesianSpace}.
=--

(e.g. [H&#246;rmander 90, def. 1.7.9](#Hoermander90))



+-- {: .num_example #FourierTransformOfDistributionsIndeedGeneralizedOrdinaryFourierTransform}
###### Example
**([[Fourier transform of distributions]] indeed generalizes [[Fourier transform]] of [[functions with rapidly decreasing partial derivatives]])**

Let $u_f \in \mathcal{S}'(\mathbb{R}^n)$ be a [[non-singular distribution|non-singular]] [[tempered distribution]] induced, via example \ref{SomeNonSingularTemperedDistributions}, from a [[function with rapidly decreasing partial derivatives]] $f \in \mathcal{S}(\mathbb{R}^n)$.

Then its [[Fourier transform of distributions]] (def. \ref{FourierTransformOnTemperedDistributions}) is the [[non-singular distribution]] induced from the [[Fourier transform]] of $f$:

$$
  \widehat{u_f} \;=\; u_{\hat f}
  \,.
$$

=--


+-- {: .proof}
###### Proof

Let $g \in \mathcal{S}(\mathbb{R}^n)$. Then

$$
  \begin{aligned}
    \widehat{u_f}(g)
    & \coloneqq
    u_f\left( \widehat{g}\right)
    \\
    & =
    \underset{x \in \mathbb{R}^n}{\int} f(x) \hat g(x)\, d^n x
    \\
    & =
    \underset{x \in \mathbb{R}^n}{\int} \hat f(x) g(x) \, d^n x
    \\
    & =
    u_{\hat f}(g)
  \end{aligned}
$$

Here all equalities hold by definition, except for the third: this is property (eq:FourierTransformInIntegralOfProductMayBeShiftedToOtherFactor) from prop. \ref{BasicPropertiesOfFourierTransformOverCartesianSpaces}.

=--


+-- {: .num_example #CompactlySupportedDistributionFourierTransform}
###### Example
**([[Fourier transform of distributions|Fourier transform]] of [[compactly supported distributions]])**

Under the identification of [[smooth functions]] of bounded growth with [[non-singular distributions|non-singular]] [[tempered distributions]] (example \ref{SomeNonSingularTemperedDistributions}), the [[Fourier transform of distributions]] (def. \ref{FourierTransformOnTemperedDistributions}) of a [[tempered distribution]] that happens to be [[compactly supported distribution|compactly supported]] (example \ref{CompactlySupportedDistibutionsAreTemperedDistributions})

$$
  u \in \mathcal{E}'(\mathbb{R}^n) \hookrightarrow \mathcal{S}'(\mathbb{R}^n)
$$

is simply

$$
  \widehat{u}(k) = u\left( e^{-  i k \cdot (-)}\right)
  \,.
$$

=--

([H&#246;rmander 90, theorem 7.1.14](#Hoermander90))




+-- {: .num_defn #FourierTransformOfDeltaDistribution}
###### Example
**([[Fourier transform of distributions|Fourier transform]] of the [[delta-distribution]])**

The [[Fourier transform of distributions|Fourier transform]] (def. \ref{FourierTransformOnTemperedDistributions}) of the [[delta distribution]] (def. \ref{DiracDeltaDistribution}), via example \ref{CompactlySupportedDistributionFourierTransform}, is the [[constant function]] on 1:

$$
  \begin{aligned}
    \widehat {\delta}(k)
    & =
    \underset{x \in \mathbb{R}^n}{\int} \delta(x) e^{- i k x} \, d x
    \\
    & =
    1
  \end{aligned}
$$

This implies by the [[Fourier inversion theorem]] (prop. \ref{FourierInversionTheoremForDistributions}) that the [[delta distribution]] itself has equivalently the following expression as a [[generalized function]]

$$
  \begin{aligned}
    \delta(x)
    & =
    \widecheck{\widehat {\delta_0}}(x)
    \\
    & =
    \underset{k \in \mathbb{R}^n}{\int} e^{i k \cdot x} \, \frac{d^n k}{ (2\pi)^n }
  \end{aligned}
$$

in the sense that for every [[function with rapidly decreasing partial derivatives]] $f \in \mathcal{S}(\mathbb{R}^n)$ (def. \ref{SchwartzSpace}) we have

$$
  \begin{aligned}
    f(x)
    & =
    \underset{y \in \mathbb{R}^n}{\int}
    f(y) \delta(y-x)  \, d^n y
    \\
    & =
    \underset{y \in \mathbb{R}^n}{\int}
    \underset{k \in \mathbb{R}^n}{\int}
    f(y) e^{i k \cdot (y-x)}
    \, \frac{d^n k}{(2\pi)^n} \, d^n y
    \\
    & =
    \underset{k \in \mathbb{R}^n}{\int}
    e^{- i k \cdot x}
    \underset{= \widehat{f}(-k) }{
    \underbrace{
      \underset{y \in \mathbb{R}^n}{\int}
      f(y) e^{i k \cdot y}
      \, d^n y
    }
    }
    \,\, \frac{d^n k}{(2\pi)^n}
    \\
    & =
    +
    \underset{k \in \mathbb{R}^n}{\int}
    e^{i k \cdot x}
    \underset{= \widehat{f}(k) }{
    \underbrace{
      \underset{y \in \mathbb{R}^n}{\int}
      f(y) e^{- i k \cdot y}
      \, d^n y
    }
    }
    \,\, \frac{d^n k}{(2\pi)^n}
    \\
    & =
    \widecheck{\widehat{f}}(x)
  \end{aligned}
$$

which is the statement of the [[Fourier inversion theorem]] for smooth functions (prop. \ref{FourierInversion}).

(Here in the last step we used [[change of integration variables]] $k \mapsto -k$ which introduces one sign $(-1)^{n}$ for the new volume form,
but another sign $(-1)^n$ from the re-[[orientation]] of the integration domain. )

Equivalently, the above computation shows that the [[delta distribution]] is the [[neutral element]] for the 
[[convolution product of distributions]].

=--


+-- {: .num_prop #PaleyWienerSchwartzTheorem}
###### Proposition
**([[Paley-Wiener-Schwartz theorem]])**

Let $u \in \mathcal{E}'(\mathbb{R}^n) \hookrightarrow \mathcal{S}'(\mathbb{R}^n)$ be a [[compactly supported distribution]] regarded as a [[tempered distribution]] by example \ref{CompactlySupportedDistibutionsAreTemperedDistributions}. Then its [[Fourier transform of distributions]] (def. \ref{FourierTransformOnTemperedDistributions}) is a [[non-singular distribution]] induced from a [[smooth function]] that grows at most exponentially.

=--

+-- {: .num_prop #FourierInversionTheoremForDistributions}
###### Proposition
**([[Fourier inversion theorem]] for [[Fourier transform of distributions]])**

The operation of forming the [[Fourier transform of distributions]] $\widehat{u}$ (def. \ref{FourierTransformOnTemperedDistributions}) [[tempered distributions]] $u \in \mathcal{S}'(\mathbb{R}^n)$ (def. \ref{TemperedDistribution}) is an [[isomorphism]], 
with [[inverse]] given by 

$$
  \widecheck{ u } \;\colon\; g \mapsto u\left( \widecheck{g}\right)
  \,,
$$

where on the right $\widecheck{g}$ is the ordinary [[inverse Fourier transform]] of $g$ according to prop. \ref{FourierInversion}.

=--

+-- {: .proof}
###### Proof

By def. \ref{FourierTransformOnTemperedDistributions}
this follows immediately from the [[Fourier inversion theorem]] for smooth functions (prop. \ref{FourierInversion}).

=--

We have the following distributional generalization of the basic property (eq:FourierTransformInterchangesPointwiseProductWithConvolution) from prop. \ref{BasicPropertiesOfFourierTransformOverCartesianSpaces}:

+-- {: .num_prop #FourierTransformOfDistributionsInterchangesConvolutionOfDistributionsWithPointwiseProduct}
###### Proposition
**([[Fourier transform of distributions]] interchanges [[convolution of distributions]] with pointwise product)**

Let

$$
  u_1 \in \mathcal{S}'(\mathbb{R}^n)
$$

be a [[tempered distribution]] (def. \ref{TemperedDistribution}) and

$$
  u_2 \in \mathcal{E}'(\mathbb{R}^n) \hookrightarrow \mathcal{S}'(\mathbb{R}^n)
$$

be a [[compactly supported distribution]], regarded as a [[tempered distribution]] via example \ref{CompactlySupportedDistibutionsAreTemperedDistributions}.

Observe here that the [[Paley-Wiener-Schwartz theorem]] (prop. \ref{PaleyWienerSchwartzTheorem}) implies that the [[Fourier transform of distributions]] of $u_1$ is a [[non-singular distribution]]
$\widehat{u_1} \in C^\infty(\mathbb{R}^n)$ so that the product $\widehat{u_1} \cdot \widehat{u_2}$ is always defined.

Then the [[Fourier transform of distributions]] of the [[convolution product of distributions]] is the product of the [[Fourier transform of distributions]]:

$$
  \widehat{u_1 \star u_2}
  \;=\;
  \widehat{u_1} \cdot \widehat{u_2}
  \,.
$$


=--

(e.g. [H&#246;rmander 90, theorem 7.1.15](#Hoermander90))


+-- {: .num_remark #ProductOfDistributionsViaFourierTransformOfConvolution}
###### Remark
**([[product of distributions]] via [[Fourier transform of distributions]])**

Prop. \ref{FourierTransformOfDistributionsInterchangesConvolutionOfDistributionsWithPointwiseProduct} together with the [[Fourier inversion theorem]] (prop. \ref{FourierInversionTheoremForDistributions}) suggests to _define_ the [[product of distributions]] $u_1 \cdot u_2$ for [[compactly supported distributions]] $u_1, u_2 \in \mathcal{E}'(\mathbb{R}^n) \hookrightarrow \mathcal{S}'(\mathbb{R}^n)$ by the formula

$$
  \widehat{ u_1 \cdot u_2 }
  \;\coloneqq\;
  (2\pi)^n \widehat{u_1} \star \widehat{u_2}
$$

which would complete the generalization of of property (eq:FourierTransformInterchangesPointwiseProductWithConvolution) from prop. \ref{BasicPropertiesOfFourierTransformOverCartesianSpaces}.

For this to make sense, the [[convolution product]] of the [[smooth functions]] on the right needs to exist, which is not guaranteed (prop. \ref{ConvolutionProductOnSchwartzSpace} does not apply here!). The condition that this exists is the [[Lars Hörmander|Hörmander]]-condition on the _[[wave front set]]_ of $u_1$ and $u_2$. See at _[[product of distributions]]_ for more.


=--





## Related concepts

* [[Fourier integral operator]]

* [[Fourier transform of distributions]]

* [[pseudodifferential operator]]

* [[Poisson summation formula]]

* [[Laplace transform]], [[Fourier-Laplace transforms]]

* [[Mellin transform]]

* [[wavefront set]]

* [[wavelet transform]]

* [[Bochner's theorem]]


## References

Lecture notes include

* {#Peacock13} [[John Peacock]], _Fourier analysis_ 2013 ([part 1 pdf](http://www.roe.ac.uk/japwww/teaching/fourier/fourier_lectures_part1.pdf), [part 2 pdf](http://www.roe.ac.uk/japwww/teaching/fourier/fourier_lectures_part2.pdf), [part 3 pdf](http://www.roe.ac.uk/japwww/teaching/fourier/fourier_lectures_part3.pdf), [part 4 pdf](http://www.roe.ac.uk/japwww/teaching/fourier/fourier_lectures_part4.pdf), [part 5 pdf](http://www.roe.ac.uk/japwww/teaching/fourier/fourier_lectures_part5.pdf))

* Gerald B. Folland, _A course in abstract harmonic analysis_, Studies in Advanced Mathematics. CRC Press, Boca Raton, FL, 1995. x+276 pp. [gBooks](http://books.google.com/books?hl=en&lr=&id=0VwYZI1DypUC)

Discussion in the broader context of [[functional analysis]] and [[distribution]] theory:

* {#Hoermander90} [[Lars Hörmander]], chapter 7 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

* [[Sergiu Klainerman]], chapter 5 of of _Lecture notes in analysis_, 2011 ([pdf](https://web.math.princeton.edu/~seri/homepage/courses/Analysis2011.pdf))


category: analysis


[[!redirects Fourier transforms]]



[[!redirects Fourier series]]

[[!redirects Fourier integral]]
[[!redirects Fourier integrals]]

[[!redirects Fourier analysis]]

[[!redirects Fourier mode]]
[[!redirects Fourier modes]]

[[!redirects Fourier expansion]]
[[!redirects Fourier expansions]]
