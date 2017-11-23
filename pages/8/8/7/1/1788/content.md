

A _[[distribution]]_ (def. \ref{LinearObservablesAreTheCompactlySupportedDistributions}) or _[[generalized function]]_ (prop. \ref{DistributionsAreGeneralizedFunctions}) is like a [[smooth function]] which may have "[[singularities]]", namely points at which it values or that of its [[derivative of a distribution|derivatives]] "become infinite". Conversely, [[smooth functions]] are the [[non-singular distributions]] (prop. \ref{DistributionsAreGeneralizedFunctions}). The collection of points around which a distribution is singular (i.e. not [[non-singular distribution|non-singular]]) is called its _[[singular support]]_ (def. \ref{SingularSupportOfADistribution} below).

The [[Fourier transform of distributions]] (def. \ref{FourierTransformOnTemperedDistributions}) decomposes a [[generalized function]] into the [[plane wave]] modes that it is made of (def. \ref{PlaneWaves}). The [[Paley-Wiener-Schwartz theorem]] (prop. \ref{DecayPropertyOfFourierTransformOfCompactlySupportedFunctions} below) says that the singular nature of a [[compactly supported distribution]] may be read off from this [[Fourier mode]] decomposition:  Singularities correspond to large contributions by Fourier modes of high [[frequency]] and small [[wavelength]], hence to large "[[ultraviolet divergence|ultraviolet]]" (UV) contributions. Therefore the [[singular support]] of a distribution is the set of points around which the Fourier transform does not sufficiently decay "in the UV".

But since the [[Fourier transform]] is a function of the full [[wave vector]] of the [[plane wave]] modes (def. \ref{PlaneWaves}),  not just of the [[frequency]]/[[wavelength]], but also of the [[direction of a vector|direction]] of the wave vector, this means that it contains _[[direction of a vector|directional]] information_ about the singularities: A distribution may have UV-singularities at some point and in some [[wave vector]] [[direction of a vector|direction]], but maybe not in other [[direction of a vector|directions]]. 

In particular, if the distribution in question is a [[distributional solution to a partial differential equation]] (def. \ref{DistributionalDerivatives}) on [[spacetime]] then the _[[propagation of singularities theorem]]_ (prop. \ref{PropagationOfSingularitiesTheorem} below) says that the [[singular support]] of the solution evolves in spacetime along the direction of those [[wave vectors]] in which the Fourier transform exhibits high UV constributions. This means that these directions are the "wave front" of the distributional solution. Accordingly, the [[singular support]] of a distribution together with, over each of its points, the [[direction of a vector|directions]] of [[wave vectors]] in which the Fourier transform around that point has large UV constributions is called the _[[wave front set]]_ of the distribution (def. \ref{WaveFrontSet} below). 

What is called _[[microlocal analysis]]_ is essentially the analysis of [[distributions]] with attention to their [[wave front set]], hence to the [[wave vector]]-[[direction of a vector|directions]] of [[UV divergences]].

In particular the [[product of distributions]] is well defined (only) if the [[wave front sets]] of the distributions to not "collide". And this in fact motivates the definition of the wave front set:

To see this, let $u,v \in  \mathcal{D}'(\mathbb{R}^1)$ be two [[distributions]], for simplicity of exposition taken on the [[real line]].

Since the product $u \cdot v$, is, if it exists, supposed to generalize the _pointwise_ product of smooth functions, it must be fixed locally: for every point $x \in \mathbb{R}$ there ought to be a [[compactly supported function|compactly supported]] [[smooth function]] ([[bump function]]) $b \in C^\infty_{cp}(\mathbb{R})$ with $f(x) = 1$ such that

$$
  b^2 u \cdot v = (b u) \cdot (b v)
  \,.
$$

But now $b v$ and $b u$ are both [[compactly supported distributions]] (def. \ref{PropductOfDistributionWithASmoothFunction} below), and these have the special property that their [[Fourier transform of distributions|Fourier transforms]] $\widehat{b v}$ and $\widehat{b u}$ are, in particular, [[smooth functions]] (by the [[Paley-Wiener-Schwartz theorem]], prop \ref{PaleyWienerSchwartzTheorem}).

Moreover, the operation of [[Fourier transform]] interchanges pointwise products with [[convolution products]] (prop. \ref{BasicPropertiesOfFourierTransformOverCartesianSpaces}). This means that if the [[product of distributions]] $u \cdot v$ exists, it must locally be given by the [[inverse Fourier transform]] of the [[convolution product]] of the Fourier transforms $\widehat {b u}$ and $\widehat b v$:

$$
  \widehat{ b^2 u \cdot v }(x)
  \;=\;
  \underset{\underset{k_{max} \to \infty}{\longrightarrow}}{\lim}
  \,
  \int_{- k_{max}}^{k_{max}} \widehat{(b u)}(k) \widehat{(b v)}(x - k) d k
  \,.
$$

(Notice that the converse of this formula holds as a fact by prop. \ref{FourierTransformOfDistributionsInterchangesConvolutionOfDistributionsWithPointwiseProduct})

This shows that the [[product of distributions]] exists once there is a [[bump function]] $b$ such that the [[integral]] on the right converges as $k_{max} \to \infty$.

Now the [[Paley-Wiener-Schwartz theorem]] says more, it says that the Fourier transforms $\widehat {b u}$ and $\widehat {b u}$ are polynomially bounded. On the other hand, the [[integral]] above is well defined if the [[integrand]] decreases at least quadratically with $k \to \infty$.
This means that for the convolution product to be well defined, either $\widehat {b u}$ has to polynomially decrease faster with $k \to \pm \infty$ than $\widehat {b v}$ grows in the _other_ direction, $k \to \mp \infty$ (due to the minus sign in the argument of the second factor in the [[convolution product]]), or the other way around.

Moreover, the degree of polynomial growth of the [[Fourier transform of distributions|Fourier transform]] increases by one with each [[derivative of distributions|derivative]]. Therefore if the [[product law]] for [[derivatives of distributions]] is to hold generally, we need that either $\widehat{b u}$ or $\widehat{b v}$ decays faster than _any_ polynomial in the opposite of the directions in which the respective other factor does not decay.

Here the set of directions of wave vectors in which the Fourier transform of a distribution localized around any point does not decay exponentially is the _[[wave front set]]_ of a distribution (def. \ref{WaveFrontSet} below). Hence the condition that the product of two distributions is well defined is that for each wave vector direction in the wave front set of one of the two distributions, the opposite direction must not be an element of the wave front set of the other distribution.

We now say this in detail:


+-- {: .num_defn #RestrictionOfDistributions}
###### Definition
**([[restriction of distributions]])**

For  $U \subset \mathbb{R}^n$ a [[subset]], and $u \in \mathcal{D}'(\mathbb{R}^n)$ a [[distribution]], then the _[[restriction of distributions|restriction]]_ of $u$ to $U$ is the distribution

$$
  u\vert_U \in \mathcal{D}'(U)
$$

give by restricting $u$ to test functions whose [[support]] is in $U$.

=--


+-- {: .num_defn #SingularSupportOfADistribution}
###### Definition
**([[singular support of a distribution]])**

Given a [[distribution]] $u \in \mathcal{D}'(\mathbb{R}^n)$, a point $x \in \mathbb{R}^n$ is a _singular point_ if there is no [[neighbourhood]] $U \subset \mathbb{R}^n$ of $x$ such that the [[restriction of distributions|restriction]] $u\vert_U$ (def. \ref{RestrictionOfDistributions}) is a [[non-singular distribution]] (given by a [[smooth function]]).

The set of all singular points is the _[[singular support]]_ $supp_{sing}(u) \subset \mathbb{R}^n$ of $u$.

=--

+-- {: .num_defn #PropductOfDistributionWithASmoothFunction}
###### Definition
**([[product of distributions|product of a distribution]] with a [[smooth function]])**


Let $u \in \mathcal{D}'(\mathbb{R}^n)$ be a [[distribution]], and $f \in C^\infty(\mathbb{R}^n)$ a smooth function. Then the _product_ $f u \in \mathcal{D}'(\mathbb{R}^n)$ is the evident [[distribution]] given on a test function $b \in C^\infty_{cp}(\mathbb{R}^n)$ by

$$
  f u
  \;\colon\;
  u
  \mapsto
  u(f \cdot b)
  \,
$$

=--

+-- {: .num_prop #DecayPropertyOfFourierTransformOfCompactlySupportedFunctions}
###### Proposition
**([[Paley-Wiener-Schwartz theorem]] -- decay of [[Fourier transform of distributions|Fourier transform]] of [[compactly supported functions]])**

A [[compactly supported distribution]] $u \in \mathcal{E}'(\mathbb{R}^n)$ is non-[[singular support of a distribution|singular]], hence given by a [[compactly supported function]] $b \in C^\infty_{cp}(\mathbb{R}^n)$ via $u(f) = \int b(x) f(x) dvol(x)$, precisely if its [[Fourier transform of a distribution|Fourier transform]] $\hat u$ ([this def.](compactly+supported+distribution#FourierTransformOfCompactlySupportedDistribution)) satisfies the following decay property:

For all $N \in \mathbb{N}$ there exists $C_N \in \mathbb{R}_+$ such that for all $k \in \mathbb{R}^n$ we have that the [[absolute value]] ${\vert \hat v(k)\vert}$ of the Fourier transform at that point is bounded by

$$
  \label{DecayEstimateForFourierTransformOfNonSingularDistribution}
  {\vert \hat v(k)\vert}
  \;\leq\;
  C_N \left( 1 + {\vert k\vert} \right)^{-N}
  \,.
$$

=--

([H&#246;rmander 90, around (8.1.1)](Paley-Wiener-Schwartz+theorem#Hoermander90))


+-- {: .num_defn #WaveFrontSet}
###### Definition
**([[wavefront set]])**

Let $u \in \mathcal{D}'(\mathbb{R}^n)$ be a [[distribution]]. 

For $b \in C^\infty_{cp}(\mathbb{R}^n)$ a [[compactly supported function|compactly supported]] [[smooth function]], write $b u \in \mathcal{E}'(\mathbb{R}^n)$ for the corresponding product (def. \ref{PropductOfDistributionWithASmoothFunction}), which is now a [[compactly supported distribution]].

For $x\in supp(b) \subset \mathbb{R}^n$, we say that a unit [[covector]] $k \in S((\mathbb{R}^n)^\ast)$ is _regular_ if there exists a [[neighbourhood]] $U \subset S((\mathbb{R}^n)^\ast)$ of $k$ in the [[unit sphere]] such that for all $c k' \in (\mathbb{R}^n)^\ast$ with $c \in \mathbb{R}_+$ and  $k' \in U \subset S((\mathbb{R}^n)^\ast)$ the decay estimate (eq:DecayEstimateForFourierTransformOfNonSingularDistribution) is valid for the [[Fourier transform of distributions|Fourier transform]] $\widehat{b u}$ of $b u$; at $c k'$. Otherwise $k$ is _non-regular_. Write

$$
  \Sigma(b u)
    \;\coloneqq\;
  \left\{
    k \in S((\mathbb{R}^n)^\ast)
    \;\vert\;
    k \, \text{non-regular}
  \right\}
$$

for the set of non-regular covectors of $b u$. 

The _wave front set at $x$_ is the [[intersection]] of these sets as $b$ ranges over [[bump functions]] whose [[support]] includes $x$:

$$
  \Sigma_x(u)
  \;\coloneqq\;
  \underset{ 
    { b \in C^\infty_{cp}(\mathbb{R}^n) } 
      \atop 
    { x \in supp(b) } 
  }{\cap}
  \Sigma(b u)
  \,.
$$

Finally the _[[wave front set]]_ of $u$ is the subset of the [[sphere bundle]] $S(T^\ast \mathbb{R}^n)$ which over $x \in \mathbb{R}^n$ consists of $\Sigma_x(U) \subset T^\ast_x \mathbb{R}^n$:

$$
  WF(u) 
    \;\coloneqq\;
  \underset{x \in \mathbb{R}^n}{\cup}
  \Sigma_x(u)
  \;\subset\;
  S(T^\ast \mathbb{R}^n)
$$

Often this is equivalently considered as the full [[conical set]] inside the [[cotangent bundle]] generated by the unit covectors under multiplication with [[positive number|positive]] [[real numbers]].

=--

([H&#246;rmander 90, def. 8.1.2](wavefron+set#Hoermander90))



+-- {: .num_remark #WaveFrontSetIsBundleOverSingularSupport}
###### Remark
**([[wave front set]] is the [[UV divergence]]-[[direction of a vector|direction]]-[[bundle]] over the [[singular support]])**

For $u \in \mathcal{D}'(\mathbb{R}^n)$
The [[Paley-Wiener-Schwartz theorem]] (prop. \ref{DecayPropertyOfFourierTransformOfCompactlySupportedFunctions}) implies that

1. Forgetting the [[direction of a vector|direction]] [[covectors]] in the [[wave front set]] $WF(u)$ (def. \ref{WaveFrontSet}) and remembering only the points where they are based yields the set of singlar points of $u$, hence the [[singular support]] (def. \ref{SingularSupportOfADistribution})

   $$
     \array{
       WF(u)
       \\
       \downarrow
       \\
       supp_{sing}(u) &\hookrightarrow& \mathbb{R}^n 
     }
   $$

1. the [[wave front set]] is [[empty set|empty]], precisely if the [[singular support]] is [[empty set|empty]], which is the case precisely if $u$ is a [[non-singular distribution]].

=--



+-- {: .num_example #WaveFrontOfDeltaDistribution}
###### Example
**([[wave front set]] of [[delta distribution]])**

Consider the [[delta distribution]]

$$
  \delta_0 \in \mathcal{D}'(\mathbb{R}^n)
$$

given by [[evaluation]] at the origin. Its [[wave front set]] (def. \ref{WaveFrontSet}) consists of all the [[direction of a vector|directions]] at the origin:

$$
  WF(\delta_0)
  \;=\; 
  \left\{
    (0,k)
    \;\vert\;
    k \in \mathbb{R}^n \setminus \{0\}
  \right\}
  \subset
  \mathbb{R}^n \times \mathbb{R}^n
  \simeq
  T^\ast \mathbb{R}^n 
  \,.
$$

=--

+-- {: .proof}
###### Proof

First of all the [[singular support of a distribution|singular support]] (def. \ref{SingularSupportOfADistribution}) of $\delta_$ is clearly $supp_{sing}(\delta(0)) = \{0\}$, hence by remark \ref{WaveFrontSetIsBundleOverSingularSupport} the wave front set vanishes over $\mathbb{R}^n \setminus \{0\}$. 

At the origin, any bump function $b$ supported around the origin with $b(0) = 1$ satisfies $b \cdot \delta(0) = \delta(0)$ and hence the wave front set over the origin is the set of covectors along which the [[Fourier transform of distributions|Fourier transform]] $\hat \delta(0)$ does not suitably decay. But this Fourier transform is in fact a [[constant function]] (example \ref{FourierTransformOfDeltaDistribution}) and hence does not decay in any direction.

=--

+-- {: .num_example #WaveFrontSetOfHeavisideDistribution}
###### Example
**(wave front set of [[step function]])**

Let $\Theta \in \mathcal{D}'(\mathbb{R}^1)$ be the [[Heaviside step function]] given by

$$
  \Theta(b) \coloneqq \int_0^\infty b(x)\, d x
  \,.
$$

Its [[wave front set]] (def. \ref{WaveFrontSet}) is

$$
  WF(H) = \{(0,k) \vert k \neq 0\}
  \,.
$$

=--



+-- {: .num_defn #SymbolOfADifferentialOperator}
###### Definition
**([[symbol of a differential operator]])**

Let 

$$
  D
  \;=\;
  \underset{k \leq n}{\sum}
  D^{\mu_1 \cdots \mu_k}
  \frac{\partial}{\partial x^{\mu^1}}
  \cdots
  \frac{\partial}{\partial x^{\mu^k}}
  + 
  D^0
$$

be a [[differential operator]] on $\mathbb{R}^n$ (def. \ref{DifferentialOperator}). Then its _[[symbol of a differential operator]]_ is the [[smooth function]] on the [[cotangent bundle]] $T^\ast \mathbb{R}^n \simeq \mathbb{R}^n \times \mathbb{R}^n$ (def. \ref{TangentVectorFields}) given by

$$
  \array{
    T^\ast \mathbb{R}^n
      &\overset{q}{\longrightarrow}&
    \mathbb{C}
    \\
    k &\mapsto& 
  \underset{k \leq n}{\sum}
  D^{\mu_1 \cdots \mu_k} k_{\mu_1} \cdots k_{\mu_k}
  + 
   }
  \,.
$$

The _[[principal symbol]]_ is the top degree [[homogeneous function|homogeneous]] part.

=--

+-- {: .num_defn #SymbolOrder}
###### Definition
**([[symbol order]])**

A [[smooth function]] $q$ on the [[cotangent bundle]] $T^\ast \mathbb{R}^n$ (e.g. the [[symbol of a differential operator]], def. \ref{SymbolOfADifferentialOperator} ) is of _order $m$_ (and type $1,0$, denoted $q \in S^m = S^m_{1,0}$), for $m \in \mathbb{N}$, if on each [[coordinate chart]] $((x^i), (k_i))$ we have that for every [[compact subset]] $K$ of the base space and all multi-indices $\alpha$ and $\beta$, there is a  [[real number]] $C_{\alpha, \beta,K } \in \mathbb{R}$ such that the [[absolute value]] of the [[partial derivatives]] of $q$ is bounded by


$$
  \left\vert
    \frac{\partial^\alpha}{\partial k_\alpha}
    \frac{\partial^\beta}{\partial x^\beta}
    q(x,k)
  \right\vert  
  \;\leq\;
  C_{\alpha,\beta,K}\left( 1+ {\vert k\vert}\right)^{m - {\vert \alpha\vert}}
$$

for all $x \in K$ and all cotangent vectors $k$ to $x$.

A [[Fourier integral]] operator $Q$ is of _[[symbol class]]_ $L^m = L^m_{1,0}$ if it is of the form

   $$
     Q f (x)
     \;=\;
     \int \int e^{i k \cdot (x - y)} q(x,y,k) f(y) \, d y d k
   $$

with symbol $q$ of order $m$, in the above sense.

=--

([H&#246;rmander 71, def. 1.1.1 and first sentence of section 2.1 with (1.4.1)](symbol+order#Hoermander71))

+-- {: .num_prop #PropagationOfSingularitiesTheorem}
###### Proposition
**(propagation of singularities theorem)**

Let $Q$ be a [[pseudo-differential operator]] on some [[smooth manifold]] $X$ which is [[properly supported pseudo-differential operator|properly supported]] (def. \ref{ProperlySupportedPseudoDifferentialOperator}) and of [[symbol class]] $L^m$ (def. \ref{SymbolOrder}) with real [[principal symbol]] $q$ that is [[homogeneous function|homogeneous]] of degree $m$.

For $u \in \mathcal{D}'(X)$ a [[distribution]] with $Q u = f$, then the [[complement]] of the [[wave front set]] of $u$ by that of $f$ is contained in the set of covectors on which the [[principal symbol]] $q$ vanishes:

$$
  WF(u) \setminus WF(f) \;\subset\; q^{-1}(0)
  \,.
$$

Moreover, $WF(u)$ is invariant under the [[bicharacteristic flow]] induced by the [[Hamiltonian vector field]] of $q$ with respect to the canonical [[symplectic manifold]] structure on the [[cotangent bundle]] ([here](cotangent+bundle#SymplecticStructure)).

=--

([Duistermaat-H&#246;rmander 72, theorem 6.1.1](propagation+of+singularities+theorem#DuistermaatHoermander72), recalled for instance as [Radzikowski 96, theorem 4.6](propagation+of+singularities+theorem#Radzikowski96))

