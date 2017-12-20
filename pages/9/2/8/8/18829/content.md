## Quantization
 {#Quantization}

Given any [[space]] with [[infinitesimal symmetries]] acting on it, there is the corresponding [[homotopy quotient]]
by these infinitesimal symmetries. For the [[covariant phase space]] of a [[Lagrangian field theory]], as [above](#PhaseSpace) with its [[Poisson Lie algebra]] of infinitesimal symmetries (def. \ref{PoissonBracketOnHamiltonianLocalObservables}),
this infinitesimal [[homotopy quotient]] is known as the _[[Poisson Lie algebroid]]_ and the corresponding genuine
[[homotopy quotient]] is known as the _[[symplectic groupoid]]_. As one passes from [[phase space]] to its [[symplectic groupoid]],
the [[algebra of functions]] on phase space -- hence the [[algebra of observables]] $Obs$ (def. \ref{LocalObservables}) -- which is always a [[commutative algebra]] _[[deformation quantization|deforms]]_ to the corresponding algebra of functions on a [[Lie groupoid]]
called the ([[polarization|polarized]]) [[convolution algebra of a Lie groupoid]]. This is now a [[non-commutative algebra]]
called the _[[algebra of quantum observables]]_ $Obs_{\hbar}$; and this passage from
[[phase space]] to its [[symplectic groupoid]] [[homotopy quotient]] by  Hamiltonian symmetries is called _[[quantization]]_
(specifically: "[[geometric quantization of symplectic groupoids]]").
Here the strength of the non-commutativity is measured by a [[deformation]] parameter called _[[Planck's constant]]_ $\hbar$.

Since the product in the [[algebra of quantum observables]] $Obs_\hbar$ differs from that in $Obs$, the
positivity condition $\langle A^\ast A\rangle \geq 0$ in the definition of  _[[states]]_ $\langle - \rangle$
of a field theory (def. \ref{States}) acquires a different meaning. The states after [[quantization]] are called
_[[quantum states]]_ and their difference witnesses that after [[quantization]] the [[Lagrangian field theory]] is of a different nature:
one says that it is no longer a _[[classical field theory]]_, but a _[[quantum field theory]]_
and that the objects whose states are expressed by these new [[quantum states]] are _[[quantum fields]]_.

Unfortunately, explicitly constructing the [[algebra of quantum observables]] of a [[Lagrangian field theory]] and hence "constructing the [[quantum field theory]]" turns out to be extremely hard, unless some simplifying assumptions are made.

One kind of simplification occurs when the  [[spacetime]] [[dimension]] is very low. For instance if the spacetime dimension is taken to be $p+1 = 1$ -- modelling the approximation where one completely ignores the variation of fields in space
and retains just their time evolution -- then one speaks of [[quantum mechanics]], which is well understood.
Another simplification occurs when the field theory is a _[[free field theory]]_, meaning that its [[equation of motion]]
is a [[normally hyperbolic differential operator|normally hyperbolic]] [[linear differential operator]].
In this case the [[quantum field theory]] is fully understood as long as the underlying [[spacetime]] is a
[[time orientation|time-orientable]] and [[globally hyperbolic spacetime|globally hyperbolic]]. But, as the
name indicates, this captures only the case where there is no [[interaction]] among the [[field (physics)|fields]].

Since the [[algebra of quantum observables]] $Obs_\hbar$ is a _[[deformation]]_ with strength $\hbar$ of the commutative algebra of classical
observables $Obs$ controlled by the [[Poisson Lie algebra]], another simplification occurs if one
gives up on the demand to understand the full deformation at finite value of [[Planck's constant]] $\hbar$
and considers just [[infinitesimal]] values of $\hbar$. Since this means that the resulting [[quantum observables]]
are no longer actual [[smooth functions]] of $\hbar$, but just _[[formal power series]]_, this is called
_[[formal deformation quantization]]_. The resulting "infinitesimally quantized" [[field theory]] is called
_[[perturbative quantum field theory]]_.

For [[interaction|interacting]] [[field theories]] in [[spacetime]] dimension $p+1 \geq 3+1$
their quantization has been constructed to date only in [[perturbation theory]] this way.
The construction of full [[non-perturbative quantum field theory]] (in dimension $\geq 3+1$ with
non-vanishing [[interaction]]) is, at the time of this writing, a wide open problem.

But [[perturbative quantum field theory]] is well understood. This we turn to in the following chapters.

$\,$

We now discuss these topics:

* _[Geometric quantization](#GeometricQuantization)_

* _[Star products](#StarProducts)_

* _[Moyal star product via Geometric quantization](#MoyalStarProductViaGeometricQuantization)_

$\,$


**[[geometric quantization]]**
  {#GeometricQuantization}

(...)

Consider the [[phase space]] given by $\mathbb{R}^2$ with canonical [[coordinate functions]] $\{q,p\}$ and equipped with the [[symplectic form]] given by

$$
  \omega = d p \wedge d q
  \,.
$$

A _[[prequantum line bundle]]_ for this is given by the
[[trivial vector bundle|trivial]] [[complex line bundle]] over $\mathbb{R}^2$ which is equipped with the [[connection on a bundle|connection]] that is given
by the globally defined [[differential 1-form]]

$$
  \label{CanonicalSymplecticPotentialOnR2}
  \theta \;\coloneqq\; q \, d p
  \,.
$$

(Other choices of connection are possible, notably $\theta = - p \, d q$).

A [[section]] of this complex line bundle is canonically identified simply with a $\mathbb{C}$-valued [[smooth function]] on $\mathbb{R}^2$.

A choice of [[foliation]] and hence of [[real polarization]] of this phase space is given by constant-$q$-slices

$$
  \label{ConstantqSlicesOnR2}
  \Lambda_q = \subset \mathbb{R}^2
  \,.
$$

(Other choices of [[polarization]] are possible, notably the constant $p$-slices as well as the canonical [[Kähler polarization]] on $\mathbb{R}^2 \simeq \mathbb{C}$.)

The [[polarization]] condition on [[sections]] $\psi$ is that their [[covariant derivative]] along the [[leaves]] vanishes, which for the choice of polarization in (eq:ConstantqSlicesOnR2) means that

$$
  \nabla_{\partial/\partial p} \psi = 0
  \,,
$$

which in turn for the choice of connection in (eq:CanonicalSymplecticPotentialOnR2) means that

$$
  \frac{\partial}{\partial p} \psi + i q \psi = 0
  \,.
$$

The solutions to this [[differential equation]] are of the form

$$
  \psi(q,p) = \psi(q,0) \exp(i p q)
  \,.
$$

The space of these "[[wave functions]]" is (noncanonically) identified with the space of complex-valued [[smooth functions]] on the line by evaluating at $p = 0$.

Since we have the [[hamiltonian vector fields]]

$$
  v_q = \frac{\partial}{\partial p}
$$ 

$$
  v_p = -\frac{\partial}{\partial q}  
$$

the action of the [[quantum operator (in geometric quantization)|quantum operators]] $\hat q$ and $\hat p$ on these states is

$$
  \hat q \psi = - i \nabla_{\partial/\partial p}\psi + q \psi
  = q \psi
$$

and

$$
  \hat p \psi =  i \nabla_{\partial/ \partial q} \psi + p \psi
  = i \frac{\partial}{\partial q} \psi
  \,.
$$


$\,$


**[[star products]]**
  {#StarProducts}

Let $V$ be a [[vector space]] of [[finite number|finite]] [[dimension]] and let $\pi \in V \otimes V$ be an element of the [[tensor product]] (not necessarily skew symmetric at the moment).

We may canonically regard $V$ as a [[smooth manifold]], in which case $\pi$ is canonically regarded as a constant rank-2 [[tensor]]. As such it has a canonical [[action]] by forming [[derivatives]] on the tensor product of the space of [[smooth functions]]:

$$
  \pi
  \;\colon\;
  C^\infty(V) \otimes C^\infty(V)
  \longrightarrow
  C^\infty(V) \otimes C^\infty(V)
  \,.
$$

If $\{\partial_i\}$ is a [[linear basis]] for $V$, identified, as before, with a basis for $\Gamma(T V)$, then in this basis this operation reads

$$
  \pi(f \otimes g)
  \;=\;
  \pi^{i j}
  (\partial_i f) \otimes (\partial_j g)
  \,,
$$

where $\partial_i f \coloneqq \frac{\partial f}{\partial x^i}$ denotes the [[partial derivative]] of the [[smooth function]] $f$ along the $i$th [[coordinate]], and where we use the [[Einstein summation convention]].

For emphasis we write

$$
  \array{
    C^\infty(V) \otimes C^\infty(V)
      &\overset{prod}{\longrightarrow}&
    C^\infty(V)
    \\
    f \otimes g &\mapsto& f \cdot g
  }
$$

for the pointwise product of smooth functions.


+-- {: .num_defn #StarPoduct}
###### Definition
**([[star product]] induced by constant rank-2 [[tensor]])**

Given $(V,\pi)$ as above, then the _[[star product]]_ induced by $\pi$ on the [[formal power series algebra]] $C^\infty(V) [ [\hbar] ]$ in a formal variable $\hbar$ ("[[Planck's constant]]") with [[coefficients]] in the [[smooth functions]] on $V$ is the linear map

$$
  (-) \star_\pi (-)
  \;\colon\;
  C^\infty(V)[ [ \hbar ] ] \otimes C^\infty(V)[ [ \hbar ] ]
    \longrightarrow
  C^\infty(V)[ [\hbar] ]
$$

given by

$$
  (-) \star_\pi (-)
  \;\coloneqq\;
  prod
    \circ \exp\left(
       \hbar \pi^{i j} \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}
  \right)
$$

Hence

$$
  f \star_\pi g
  \;\coloneqq\;
  1
  +
  \hbar \pi^{i j}
  \frac{\partial f}{\partial x^i} \cdot \frac{\partial g}{\partial x^j}
  +
  \hbar^2
  \tfrac{ 1 }{2}
  \pi^{i j}
  \pi^{k l}
  \frac{\partial^2 f}{\partial x^{i} \partial x^{k}}
    \cdot
  \frac{\partial^2 g}{\partial x^{j} \partial x^{l}}
  +
  \cdots
  \,.
$$

=--


+-- {: .num_example }
###### Example
**([[star product]] degenerating to pointwise product)**

If $\pi = 0$ in def. \ref{StarPoduct}, then the star product $\star_0 = \cdot$ is the plain pointwise product of functions.

=--


+-- {: .num_prop #MoyalStarProduct}
###### Example
**([[Moyal star product]])**

If the tensor $\pi$ in def. \ref{StarPoduct} is skew-symmetric, it may be regarded as a constant [[Poisson tensor]] on the smooth manifold $V$. In this case $\star_{\tfrac{1}{2}\pi}$ is called a _[[Moyal star product]]_ and the star-product algebra $C^\infty(V)[ [\hbar] ], \star_\pi)$ is called the _[[Moyal deformation quantization]]_ of the [[Poisson manifold]] $(V,\pi)$.

=--



+-- {: .num_prop #AssociativeAndUnitalStarProduct}
###### Proposition
**([[star product]] is [[associativity|associative]] and [[unitality|unital]])**

Given $(V,\pi)$ as above, then the star product
$(-) \star_\pi (-)$ from def. \ref{StarPoduct}
is [[associativity|associative]] and [[unitality|unital]]
with unit the [[constant function]] $1 \in C^\infty(V) \hookrightarrow C^\infty(V)[ [ \hbar ] ]$.

Hence the [[vector space]] $C^\infty(V)$ equipped with the star product $\pi$ is a [[unital algebra|unital]] [[associative algebra]].

=--


+-- {: .proof}
###### Proof

Observe that the [[product rule]] of [[differentiation]] says that

$$
  \partial_i \circ prod
    =
   prod \circ ( \partial_i \otimes id \;+\; id \otimes \partial_i  )
  \,.
$$

Using this we compute as follows:

$$
  \begin{aligned}
  (f \star_\pi  g) \star_\pi h
  & =
  prod \circ
  \exp( \pi^{i j} \partial_i \otimes \partial_j )  \circ
  \left(
    \left( prod \circ \exp( \pi^{k l} \partial_k \otimes \partial_l ) \right) \otimes id
  \right)
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  \exp( \pi^{i j} \partial_i \otimes \partial_j ) \circ
  (prod \otimes id)
  \circ
  \left(
    \exp( \pi^{k l} \partial_k \otimes \partial_l )  \otimes id
  \right)
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  (prod \otimes id) \circ
  \exp( \pi^{i j}  ( \partial_i \otimes id \otimes \partial_j +id \otimes \partial_i \otimes \partial_j   )
  \circ
  \exp( \pi^{k l} \partial_k \otimes \partial_l )  \otimes id
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  (prod \otimes id) \circ
  \exp( \pi^{i j}   \partial_i \otimes id \otimes \partial_j   )
  \circ
  \exp( \pi^{i j}  id \otimes \partial_i \otimes \partial_j )
  \circ
  \exp( \pi^{k l} \partial_k \otimes \partial_l \otimes id )
  (f \otimes g \otimes g)
  \\
  & =
  prod_3
  \circ
  \exp( \pi^{i j} ( \partial_i \otimes \partial_j \otimes id  +  \partial_i \otimes id \otimes \partial_j + id \otimes \partial_i \otimes \partial_j)   )
  \end{aligned}
$$

In the last line we used that the ordinary pointwise product of functions is associative, and wrote $prod_3 \colon C^\infty(V) \otimes C^\infty(V) \otimes C^\infty(V) \to C^\infty(V)$ for the unique pointwise product of three functions.

The last expression above is manifestly independent of the choice of order of the arguments in the triple star product, and hence it is clear that an analogous computation yields

$$
  \cdots = f \star_\pi (g \star_\pi h)
  \,.
$$

=--

+-- {: .num_prop #SymmetricContribution}
###### Proposition
**(shift by symmetric contribution is [[isomorphism]] of [[star products]])**

Let $V$ be a vector space, $\pi \in V \otimes V$ a rank-2 [[tensor]] and $\alpha \in Sym(V \otimes V)$ a _symmetric_ rank-2 tensor.

Then the linear map

$$
  \array{
    C^\infty(V)
     &\overset{\exp\left(-\hbar\tfrac{1}{2}\alpha \right)}{\longrightarrow}&
    C^\infty(V)
    \\
    f &\mapsto& \exp\left( -\hbar\tfrac{1}{2}\alpha^{i j} \partial_i \partial_j \right) f
  }
$$

constitutes an [[isomorphism]] of star product algebras (prop. \ref{AssociativeAndUnitalStarProduct}) of the form

$$
  \exp\left(-\hbar\tfrac{1}{2}\alpha \right)
   \;\colon\;
  (C^\infty(V)[ [\hbar] ], \star_\pi)
    \overset{\simeq}{\longrightarrow}
  (C^\infty(V))[ [\hbar] ], \star_{\pi + \alpha})
  \,,
$$

hence identifying the star product induced from $\pi$ with that induced from $\pi + \alpha$.

In particular every star product algebra $(C^\infty(V)[ [\hbar] ],\star_\pi)$ is isomorphic to a Moyal star product algebra $\star_{\tfrac{1}{2}\pi}$ (example \ref{MoyalStarProduct}) with $\tfrac{1}{2}\pi_{skew}^{i j} = \tfrac{1}{2}(\pi^{i j} - \pi^{j i})$ the skew-symmetric part of $\pi$, this isomorphism being exhibited by $\alpha^{i j} = - \tfrac{1}{2}(\pi^{i j} + \pi^{j i})$ (minus) the symmetric part.

=--


+-- {: .proof}
###### Proof

We need to show that

$$
  prod \circ
  \exp( \pi )
  \circ
  \left(
    \exp\left( -\tfrac{1}{2}\alpha\right)
    \otimes
    \exp\left( -\tfrac{1}{2}\alpha \right)
  \right)
  \;=\;
  \exp\left( -\tfrac{1}{2}\alpha \right)
  \circ
   prod \circ \exp( \pi )
  \,.
$$


To this end, observe that the [[product rule]] of [[differentiation]] applied twice in a row implies that

$$
  \partial_i \partial_j \circ prod
  \;=\;
  prod \circ
  \left(
     (\partial_i \partial_j)  \otimes id
     +
     id \otimes (\partial_i \partial_j)
     +
     \partial_i \otimes \partial_j
     +
     \partial_j \otimes \partial_i
  \right)
  \,.
$$

Using this we compute

$$
  \begin{aligned}
    \exp\left( - \hbar\tfrac{1}{2}\alpha^{i j} \partial_i \partial_j \right)
    \circ
    prod
    \circ
    \exp( \hbar \pi^{i j} \partial_{k} \otimes \partial_l )
    & =
    prod
      \circ
      \exp\left( - \hbar \tfrac{1}{2}\alpha^{i j}
         (\partial_i \partial_j) \otimes id
         +
         id \otimes (\partial_i \partial_j)
         +
         \partial_i \otimes \partial_j
         +
         \partial_j \otimes \partial_i
      \right)
      \circ
    \exp( \hbar \pi^{i j} \partial_{k} \otimes \partial_l )
    \\
    &
    =
    prod
    \circ
    \exp\left(
       \hbar (\pi^{i j} + \alpha^{i j}) \partial_i \otimes \partial_j
    \right)
    \circ
    \exp\left(
      - \hbar \tfrac{1}{2} \alpha^{i j} (\partial_i \partial_j) \otimes id
      - \hbar \tfrac{1}{2} \alpha^{i j} id \otimes (\partial_i \partial_j)
    \right)
    \\
    & =
    prod
    \circ
    \exp\left(
       \hbar (\pi^{i j} + \alpha^{i j}) \partial_i \otimes \partial_j
    \right)
    \circ
    \left(
      \exp(-\hbar \tfrac{1}{2}\alpha)
        \otimes
      \exp(-\hbar \tfrac{1}{2}\alpha)
    \right)
  \end{aligned}
$$

=--




$\,$


**[[Moyal star product]] via [[geometric quantization]]**
  {#MoyalStarProductViaGeometricQuantization}


+-- {: .num_prop #IntegralRepresentationOfStarProduct}
###### Proposition
**([[integral]] representation of [[star product]])**

If $\pi$ skew-symmetric and invertible, in that there exists $\omega \in V^\ast \otimes V^\ast$ with $\pi^{i j}\omega_{j k} = \delta^i_k$, and if the functions $f,g$ admit [[Fourier analysis]] (are [[functions with rapidly decreasing partial derivatives]]), then  their [[star product]] (def. \ref{StarPoduct}) is equivalently given by the following [[integral]] expression:

$$
  \begin{aligned}
  \left(f \star_\pi g\right)(x)
   &=
  \frac{(det(\omega)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{ \tfrac{1}{i \hbar} \omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

=--

([Baker 58](Moyal+deformation+quantization#Baker58))

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
  \left(f \star_\pi g\right)(x)
  & \coloneqq
  prod
    \circ \exp\left(
       \hbar \pi^{i j} \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}
  \right)(f, g)
  \\
  & =
  \frac{1}{(2 \pi)^{2n}}
  \frac{1}{(2 \pi)^{2n}}
  \int
  \int
    \underbrace{
      e^{ i \hbar \pi(k,q) }
    }
    \underbrace{
      e^{i k \cdot (x-y)}
      f(y)
    }
    \underbrace{
      e^{i q \cdot (x- \tilde y)}
      g(\tilde y)
    }
   \,
   d^{2 n} k
   \,
   d^{2 n} q
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
   \\
   & =
  \frac{1}{(2 \pi)^{2n}}
  \int
    \delta\left( x - \tilde y + \hbar \pi \cdot k \right)
    e^{i k \cdot (x-y)}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} k
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
   \\
   & = 
  \frac{1}{(2 \pi)^{2n}}
  \int
    \delta\left( x - \tilde y + z \right)
    e^{ \tfrac{i}{\hbar} \omega(z, (x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} z
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \\
  & =
  \frac{(det(\pi)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{\tfrac{1}{i \hbar}\omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

Here in the first step we expressed $f$ and $g$ both by their [[Fourier transform]] (inserting the Fourier expression of the [[delta distribution]] from [this example](Dirac+distribution#FourierTransformOfDeltaDistribution)) and used that under this transformation the [[partial derivative]] $\pi^{a b} \frac{\partial}{\partial\phi^a}{\frac{\partial}{\phi^b}}$ turns into the product with $i \pi^{i j} k_i k_j$ ([this prop.](Fourier+transform#BasicPropertiesOfFourierTransformOverCartesianSpaces)).
Then we identified again the Fourier-expansion of a [[delta distribution]]
and finally we applied the [[change of integration variables]] $k = \tfrac{1}{\hbar}\omega \cdot z$ and then evaluated the [[delta distribution]].

=--

Next we express this as the [[groupoid convolution product]] of polarized sections of the [[symplectic groupoid]]. To this end, we first need the following definnition:


+-- {: .num_defn #SymplecticGroupoidOfSymplecticVectorSpace}
###### Definition
**([[symplectic groupoid]] of [[symplectic vector space]])**

Assume that $\pi$ is the inverse of a [[symplectic form]] $\omega$ on $\mathbb{R}^{2n}$. Then the [[Cartesian product]] 

$$
  \array{
    && \mathbb{R}^{2n} \times \mathbb{R}^{2n}
    \\
    & {}^{\mathllap{pr_1}}\swarrow && \searrow^{\mathrlap{pr_2}}
    \\
    \mathbb{R}^{2n} && && \mathbb{R}^{2n}
  }
$$

inherits the symplectic structure

$$
  \Omega
  \;\coloneqq\;
  \left(
    pr_1^\ast \omega - pr_2^\ast \omega
  \right)
$$

given by

$$
  \begin{aligned}
    \Omega 
    & = 
    \omega_{i j} d x^i \wedge d x^j - \omega_{i j} d y^i \wedge d y^j
    \\
    & =
    \omega_{i j} ( d x^i - d y^i ) \wedge ( d x^j +  d y^j )
  \end{aligned}
  \,.
$$

The [[pair groupoid]] on $\mathbb{R}^{2n}$ equipped with this [[symplectic form]] on its space of [[morphisms]] is a [[symplectic groupoid]].

A choice of potential form $\Theta$ for $\Omega$, hence with $\Omega = d \Theta$, is given by

$$
  \Theta 
   \coloneqq
   -\omega_{i j} ( x^i + y^i ) d (x^j - y^j) )  
$$

Choosing the [[real polarization]] spanned by $\partial_{x^i} - \partial_{y^i}$ a polarized section is function $F = F(x,y)$ such that

$$
  \iota_{\partial_{x^j} - \partial_{y^j}}(d F - \tfrac{1}{i \hbar} \tfrac{1}{4} \Theta F) = 0
$$

hence

$$
  \label{PolarizedSectionOnMorphismsOfSymplecticGroupoid}
  F(x,y) 
   = 
  f\left( \tfrac{x + y}{2} \right) e^{ \tfrac{1}{i \hbar} \omega\left(  \tfrac{x - y}{2} , \tfrac{x + y}{2} \right)}
  \,.
$$

=--

+-- {: .num_prop #PolarizedSymplecticGroupoidConvolutionProductOfSymplecticVectorSpaceIsMoyalStarProduct}
###### Proposition
**(polarized [[symplectic groupoid|symplectic]] [[groupoid convolution product]] of [[symplectic vector space]] is give by [[Moyal star product]])**

Given a [[symplectic vector space]] $(\mathbb{R}^{2n}, \omega)$, then 
the [[groupoid convolution product]] on polarized sections (eq:PolarizedSectionOnMorphismsOfSymplecticGroupoid) on its [[symplectic groupoid]] (def. \ref{SymplecticGroupoidOfSymplecticVectorSpace}), given by [[convolution product]] followed by averaging ([[integration]]) over the polarization [[fiber]], is given by the [[star product]] (def. \ref{StarPoduct}) for the corresponding [[Poisson tensor]] $\pi \coloneqq \omega^{-1}$, in that

$$
  \begin{aligned}
    \int \int 
      F(x,t) G(t,y) \, d^{2n} t \, d^{2n} (x-y)
    & = 
    (f \star_\pi g)((x+y)/2)
  \end{aligned} 
  \,.
$$

=--

([Weinstein 91, p. 446](Moyal+deformation+quantization#Weinstein91), [Garcia-Bondia & Varilly 94, section V](Moyal+deformation+quantization#GBV))

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
    \int \int 
      F(x,t) G(t,y) \, d^{2n} t \, d^{2n} (x-y)
    & \coloneqq
    \int \int f((x + t)/2) g( (t + y)/2 ) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( x-t, x+t ) + \tfrac{1}{i \hbar} \tfrac{1}{4} \omega(t-y, t + y)  }
    \, d^{2n} t
    \, d^{2n} (x-y)
    \\
    & = 
    \int \int 
      f(t/2) g( (t - (x - y))/2 ) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( (x+y) + (x - y) - t, t ) + \tfrac{1}{i \hbar} \tfrac{1}{4} \omega(t-(x+y), t - (x-y))  }
    \, d^{2n} t
    \, d^{2n} (x-y)   
    \\
    & =  
    \int \int 
      f(t/2) g( \tilde t / 2) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( (x+y) - \tilde t, t ) - \tfrac{1}{i \hbar} \tfrac{1}{4} \omega((x+y)-t, \tilde t)  }
    \, d^{2n} t
    \, d^{2n} \tilde t
    \\
    & = 
    \int \int 
      f(t) g( \tilde t ) 
      e^{ \tfrac{1}{i \hbar} \tfrac{1}{4} \omega( (x+y) - 2 \tilde t, 2 t ) - \tfrac{1}{ii \hbar} \tfrac{1}{4} \omega((x+y)- 2 t, 2 \tilde t)  }
    \, d^{2n} t
    \, d^{2n} \tilde t
    \\
    \\
    & = 
    \int \int
       f(t) g(\tilde t )
      e^{ \tfrac{1}{i \hbar} \omega\left( \tfrac{1}{2}(x+y) - \tilde t, \tfrac{1}{2}(x + y) - t  \right)}   
     \, d^{2n} t
     \, d^{2n} \tilde t
    \\
    & = 
    (f \star_\omega g)((x+y)/2)
  \end{aligned} 
$$

The first line just unwinds the definition of polarized sections from def. \ref{SymplecticGroupoidOfSymplecticVectorSpace}, the following lines each implement a [[change of integration variables]] and 
fnally in the last line we used prop. \ref{IntegralRepresentationOfStarProduct}.

=--

(...)

