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

But [[perturbative quantum field theory]] is well understood. This we turn to next...


(...)

Let $V$ be a [[vector space]] of [[finite number|finite]] [[dimension]] and let $\omega \in V \otimes V$ be an element of the [[tensor product]] (not necessarily skew symmetric at the moment).

We may canonically regard $V$ as a [[smooth manifold]], in which case $\omega$ is canonically regarded as a constant rank-2 [[tensor]]. As such it has a canonical [[action]] by forming [[derivatives]] on the tensor product of the space of [[smooth functions]]:

$$
  \omega
  \;\colon\;
  C^\infty(V) \otimes C^\infty(V)
  \longrightarrow
  C^\infty(V) \otimes C^\infty(V)
  \,.
$$

If $\{\partial_i\}$ is a [[linear basis]] for $V$, identified, as before, with a basis for $\Gamma(T V)$, then in this basis this operation reads

$$
  \omega(f \otimes g)
  \;=\;
  \omega^{i j}
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
**([[star product]] induced by constant rank-2 tensor)**

Given $(V,\omega)$ as above, then the _[[star product]]_ induced by $\omega$ on the [[formal power series algebra]] $C^\infty(V) [ [\hbar] ]$ in a formal variable $\hbar$ ("[[Planck's constant]]") with [[coefficients]] in the [[smooth functions]] on $V$ is the linear map

$$
  (-) \star_\omega (-)
  \;\colon\;
  C^\infty(V)[ [ \hbar ] ] \otimes C^\infty(V)[ [ \hbar ] ]
    \longrightarrow
  C^\infty(V)[ [\hbar] ]
$$

given by

$$
  (-) \star_\omega (-)
  \;\coloneqq\;
  prod
    \circ \exp\left(
       \hbar \omega^{i j} \partial_i \otimes \partial_j
  \right)
$$

Hence

$$
  f \star_\omega g
  \;\coloneqq\;
  1
  +
  \hbar \omega^{i j}
  \frac{\partial f}{\partial x^i} \cdot \frac{\partial g}{\partial x^j}
  +
  \hbar^2
  \tfrac{ 1 }{2}
  \omega^{i j}
  \omega^{k l}
  \frac{\partial^2 f}{\partial x^{i} \partial x^{k}}
    \cdot
  \frac{\partial^2 g}{\partial x^{j} \partial x^{l}}
  +
  \cdots
  \,.
$$


=--


+-- {: .num_prop #AssociativeAndUnitalStarProduct}
###### Proposition
**([[star product]] is [[associativity|associative]] and [[unitality|unital]])**

Given $(V,\omega)$ as above, then the star product
$(-) \star_\omega (-)$ from def. \ref{StarPoduct}
is [[associativity|associative]] and [[unitality|unital]]
with unit the [[constant function]] $1 \in C^\infty(V) \hookrightarrow C^\infty(V)[ [ \hbar ] ]$.

Hence the [[vector space]] $C^\infty(V)$ equipped with the star product $\omega$ is a [[unital algebra|unital]] [[associative algebra]].

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
  (f \star_\omega  g) \star_\omega h
  & =
  prod \circ
  \exp( \omega^{i j} \partial_i \otimes \partial_j )  \circ
  \left(
    \left( prod \circ \exp( \omega^{k l} \partial_k \otimes \partial_l ) \right) \otimes id
  \right)
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  \exp( \omega^{i j} \partial_i \otimes \partial_j ) \circ
  (prod \otimes id)
  \circ
  \left(
    \exp( \omega^{k l} \partial_k \otimes \partial_l )  \otimes id
  \right)
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  (prod \otimes id) \circ
  \exp( \omega^{i j}  ( \partial_i \otimes id \otimes \partial_j +id \otimes \partial_i \otimes \partial_j   )
  \circ
  \exp( \omega^{k l} \partial_k \otimes \partial_l )  \otimes id
  (f \otimes g \otimes g)
  \\
  & =
  prod \circ
  (prod \otimes id) \circ
  \exp( \omega^{i j}   \partial_i \otimes id \otimes \partial_j   )
  \circ
  \exp( \omega^{i j}  id \otimes \partial_i \otimes \partial_j )
  \circ
  \exp( \omega^{k l} \partial_k \otimes \partial_l \otimes id )
  (f \otimes g \otimes g)
  \\
  & =
  prod_3
  \circ
  \exp( \omega^{i j} ( \partial_i \otimes \partial_j \otimes id  +  \partial_i \otimes id \otimes \partial_j + id \otimes \partial_i \otimes \partial_j)   )
  \end{aligned}
$$

In the last line we used that the ordinary pointwise product of functions is associative, and wrote $prod_3 \colon C^\infty(V) \otimes C^\infty(V) \otimes C^\infty(V) \to C^\infty(V)$ for the unique pointwise product of three functions.

The last expression above is manifestly independent of the choice of order of the arguments in the triple star product, and hence it is clear that an analogous computation yields

$$
  \cdots = f \star_\omega (g \star_\omega h)
  \,.
$$

=--



+-- {: .num_prop #SymmetricContribution}
###### Proposition
**(shift by symmetric contribution is [[isomorphism]] of [[star products]])**

Let $V$ be a vector space, $\omega \in V \otimes V$ a rank-2 [[tensor]] and $\alpha \in Sym(V \otimes V)$ a _symmetric_ rank-2 tensor.

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
  (C^\infty(V)[ [\hbar] ], \star_\omega)
    \overset{\simeq}{\longrightarrow}
  (C^\infty(V))[ [\hbar] ], \star_{\omega + \alpha})
  \,,
$$

hence identifying the star product induced from $\omega$ with that induced from $\omega + \alpha$.

In particular every star product algebra $(C^\infty(V)[ [\hbar] ],\star_\omega)$ is isomorphic to a Moyal star product algebra $\star_{\tfrac{1}{2}\pi}$ (example \ref{MoyalStarProduct}) with $\tfrac{1}{2}\pi^{i j} \tfrac{1}{2}(\omega^{i j} - \omega^{j i})$ the skew-symmetric part of $\omega$, this isomorphism being exhibited by $\alpha^{i j} = - \tfrac{1}{2}(\omega^{i j} + \omega^{j i})$ (minus) the symmetric part.

=--


+-- {: .proof}
###### Proof

We need to show that

$$
  prod \circ
  \exp( \omega )
  \circ
  \left(
    \exp\left( -\tfrac{1}{2}\alpha\right)
    \otimes
    \exp\left( -\tfrac{1}{2}\alpha \right)
  \right)
  \;=\;
  \exp\left( -\tfrac{1}{2}\alpha \right)
  \circ
   prod \circ \exp( \omega )
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
    \exp( \hbar \omega^{i j} \partial_{k} \otimes \partial_l )
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
    \exp( \hbar \omega^{i j} \partial_{k} \otimes \partial_l )
    \\
    &
    =
    prod
    \circ
    \exp\left(
       \hbar (\omega^{i j} + \alpha^{i j}) \partial_i \otimes \partial_j
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
       \hbar (\omega^{i j} + \alpha^{i j}) \partial_i \otimes \partial_j
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



Some examples of star products as in def. \ref{StarPoduct}:

+-- {: .num_example}
###### Example

If $\omega = 0$ in def. \ref{StarPoduct}, then the star product $\star_0 = \cdot$ is the plain pointwise product.

=--


+-- {: .num_prop #MoyalStarProduct}
###### Example
**([[Moyal star product]])**

If $\omega = \tfrac{1}{2}\pi$ in def. \ref{StarPoduct} is skew-symmetric, it may be regarded as a constant [[Poisson tensor]] $\pi$ on the smooth manifold $V$. In this case $\star_{\tfrac{1}{2}\pi}$ is called a _[[Moyal star product]]_ and the star-product algebra $C^\infty(V)[ [\hbar] ], \star_\pi)$ is called the _[[Moyal deformation quantization]]_ of the [[Poisson manifold]] $(V,\pi)$.

=--

(...)

