
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[deformation quantization]] of [[Poisson manifolds]] the commutative product $\cdot$ of the [[commutative algebra|commutative]] [[algebra of functions]] is replaced by a noncommutative associative product. This is often called a **star product** and denoted "$\star$".

An [[archetypal example]] is the _[[Moyal star product]]_ (example \ref{MoyalStarProduct} below) that deforms the function algebra on a Poisson vector space, and often "star product" is by default understood to be a Moyal star product. Indeed every star product induced from a constant rank-2 tensor on a vector space is [[isomorphism|isomorphic]] to a Moyal star product (prop. \ref{SymmetricContribution} below).

More recently also nonassociative "star products" have been proposed to be of interest.

## Definition


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


## Properties

### Equivalences of star products

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

### Integral representations

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



## Examples


Some examples of star products as in def. \ref{StarPoduct}:

+-- {: .num_example}
###### Example

If $\pi = 0$ in def. \ref{StarPoduct}, then the star product $\star_0 = \cdot$ is the plain pointwise product.

=--


+-- {: .num_prop #MoyalStarProduct}
###### Example
**([[Moyal star product]])**


If the tensor $\pi$ in def. \ref{StarPoduct} is skew-symmetric, it may be regarded as a constant [[Poisson tensor]] on the smooth manifold $V$. In this case $\star_{\tfrac{1}{2}\pi}$ is called a _[[Moyal star product]]_ and the star-product algebra $C^\infty(V)[ [\hbar] ], \star_\pi)$ is called the _[[Moyal deformation quantization]]_ of the [[Poisson manifold]] $(V,\pi)$.

=--


+-- {: .num_example #WickAlgebras}
###### Example
**([[normal-ordered products]] and [[time-ordered products]])**

In cases where $V$ is _not_ [[finite number|finite]] [[dimension|dimensional]], but for instance a [[space of sections]] of a linear [[field bundle]], the expression involved in the definition of the star product in def. \ref{StarPoduct} still may be interpreted as [[products of distributions]], but these only exist if the [[wavefront sets]] satisfy [[Hörmander's criterion]].

In these situations it happens that the star product for some Poisson tensor $\tfrac{1}{2}\pi$ is not defined due to [[wavefront set]] collision (violation of [[Hörmander's criterion]]), but the star product $\star_{\tfrac{1}{2}\pi + \alpha}$ for the tensor $\tfrac{1}{2}\pi + \alpha$ shifted by a symmetric contribition $\alpha$ as in prop. \ref{SymmetricContribution} is defined, and serves as the proper stand-in for the non-existing $\star_{\tfrac{1}{2}\pi}$.

This is the case notably for [[Wick algebras]] ([[algebras of quantum observables]] of [[free fields]]): here $\tfrac{1}{2}\pi$ is the [[causal propagator]] for which $\star_\pi$ does not exist, and $\pi = \tfrac{1}{2}\pi + \alpha$ is a [[Hadamard propagator]], so that $\star_{\pi}$ does exist on [[microcausal functionals]]: it is the "[[normal-ordered product]]" of quantum observables.

=--

[[!include Wick algebra -- table]]


## Related concepts

* [[deformation theory]]


[[!redirects star products]]

[[!redirects star-product]]


