
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[deformation quantization]] of [[Poisson manifolds]] the commutative product $\cdot$ of the [[commutative algebra|commutative]] [[algebra of functions]] is replaced by a noncommutative associative product. This is often called a **star product** and denoted "$\star$". 

An archetypical example is the _[[Moyal star product]]_ (example \ref{MoyalStarProduct} below) that deforms the function algebra on a Poisson vector space, and often "star product" is by default understood to be a Moyal star product. Indeed every star product induced from a constant rank-2 tensor on a vector space is [[isomorphism|isomorphic]] to a Moyal star product (prop. \ref{SymmetricContribution} below).

More recently also nonassociative "star products" have been proposed to be of interest.

## Definition


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
**(star product induced by constant rank-2 tensor)**

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
       \hbar \omega^{i j} \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}
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
**(star product is [[associativity|associative]] and [[unitality|unital]])**

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


## Properties


+-- {: .num_prop #IntegralRepresentationOfStarProduct}
###### Proposition
**([[integral]] representation of [[star product]])**

If the functions $f,g$ admit [[Fourier analysis]] (are [[functions with rapidly decreasing partial derivatives]]), then  their [[star product]] (def. \ref{StarPoduct}) is equivalently given by the following [[integral]] expression:

$$
  \begin{aligned}
  \left(f \star_\omega g\right)(x)
   &= 
  \frac{(det(\omega)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{ - \tfrac{1}{i \hbar} \omega((x - \tilde y),(x-y))}
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
  \left(f \star_\omega g\right)(x)
  & \coloneqq
  prod 
    \circ \exp\left(
       \hbar \omega^{i j} \frac{\partial}{\partial x^i} \otimes \frac{\partial}{\partial x^j}
  \right)(f, g)
  \\
  & =
  \frac{1}{(2 \pi)^{2n}}
  \frac{1}{(2 \pi)^{2n}}
  \int
  \int
    \underbrace{
      e^{ i \hbar \omega^{-1}(k,q) }
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
    \delta\left( x - \tilde y + \hbar \omega^{-1}(k) \right)
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
  \frac{(det(\omega)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{i \tfrac{1}{\hbar}\omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

Here in the first step we expressed $f$ and $g$ both by their [[Fourier transform]] (inserting the Fourier expression of the [[delta distribution]] from [this example](Dirac+distribution#FourierTransformOfDeltaDistribution)) and used that under this transformation the [[partial derivative]] $\omega^{a b} \frac{\partial}{\partial\phi^a}{\frac{\partial}{\phi^b}}$ turns into the product with $i \omega^{i j} k_i k_j$ ([this prop.](Fourier+transform#BasicPropertiesOfFourierTransformOverCartesianSpaces)). 
Then we identified again the Fourier-expansion of a [[delta distribution]]
and finally we applied the [[change of integration variables]] $k = \tfrac{1}{\hbar} \omega(z)$ and evaluated the [[delta distribution]].

=--


+-- {: .num_prop #SymmetricContribution}
###### Proposition
**(shift by symmetric contribution is isomorphism of star product)**

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

## Examples



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


+-- {: .num_example #WickAlgebras}
###### Example
**([[normal-ordered products]] and [[time-ordered products]])**

In cases where $V$ is _not_ [[finite number|finite]] [[dimension|dimensional]], but for instance a [[space of sections]] of a linear [[field bundle]], the expression involved in the definition of the star product in def. \ref{StarPoduct} still may be interpreted as [[products of distributions]], but these only exist if certain [[wavefront set]]-conditions are met. 

In these situations it happens that the star product for some Poisson tensor $\tfrac{1}{2}\pi$ is not defined due to [[wavefront set]] collision, but the star product $\star_{\tfrac{1}{2}\pi + \alpha}$ for the tensor $\tfrac{1}{2}\pi + \alpha$ shifted by a symmetric contribition $\alpha$ as in prop. \ref{SymmetricContribution} is defined, and serves as the proper stand-in for the non-existing $\star_{\tfrac{1}{2}\pi}$. 

This is the case notably for [[Wick algebras]] ([[algebras of quantum observables]] of [[free fields]]): here $\tfrac{1}{2}\pi$ is the [[causal propagator]] for which $\star_\omega$ does not exist, and $\omega = \tfrac{1}{2}\pi + \alpha$ is a [[Hadamard propagator]], so that $\star_{\omega}$ does exist on [[microcausal functionals]]: it is the "[[normal-ordered product]]" of quantum observables.

 

=--


## Related concepts

* [[deformation theory]]


[[!redirects star products]]

[[!redirects star-product]]
