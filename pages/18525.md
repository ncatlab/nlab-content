
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


Let $X$ be a [[smooth manifold]] and let $D$ be a [[differential operator]] on (smooth [[sections]] of) the [[trivial line bundle]] over $X$ (or more generally a [[properly supported pseudo-differential operator]]). Then the [[principal symbol]] $q(D)$ of $D$ is equivalently a [[smooth function]] on the [[cotangent bundle]] $T^\ast X$ (by [this example](symbol+of+a+differential+operator#BicharacteristicFlow)). With the [[cotangent bundle]] canonically regarded as a [[symplectic manifold]], let 

$$
  v_{q(D)} \in \Gamma\left(T\left(T^\ast X\right) \right)
$$ 

be the corresponding [[Hamiltonian vector field]]. 

+-- {: .num_defn #BicharacteristicFlow}
###### Definition

The _bicharacteristic flow_ of $D$ is the [[Hamiltonian flow|Hamiltonian]] [[flow of a vector field|flow]] of the [[Hamiltonian vector field]] $v_{q(D)}$ inside the submanifold defined by $q = 0$. Moreover:

1. A single [[flow line]] in $T^\ast X$ is called a _bicharacteristic strip_ of $D$, 

1. the [[projection]] of such to a [[curve]] in $X$ is called a _bicharacteristic curve_.

1. The [[relation]] $C$ on $T^\ast X$ given by

   $$
     \left((x_1,k_1) \sim (x_2, k_2)\right)
     \;\coloneqq\;
     \left(
       q(x_i,k_i) = 0
       \;\;\text{and}\;\;
       (x_1,k_1) \,\text{is connected to}\,
       (x_2,k_2) \,\text{by a bicharacteristic strip}
     \right)
   $$

   is called the _bicharacteristic relation_.

=--

## Examples

### Of the Klein-Gordon operator
 {#OfTheKleinGordonOperator}

+-- {: .num_example #BicharachteristicFlowOfKleinGordonOperator}
###### Example
**(bicharacteristic curves of [[wave operator]]/[[Klein-Gordon operators]] are the [[lightlike]] [[geodesics]])**

Let $(X,g)$ be a [[Lorentzian manifold]] and let $D \coloneqq \Box_g - m^2$ be its [[wave operator]]/[[Klein-Gordon operator]]. 

Then the bicharacteristic curves of $D$ (def. \ref{BicharacteristicFlow}) are precisely the [[lightlike]] [[geodesics]] of $(X,e)$, and the bicharacteristic strips are precisely these geodesices with their [[cotangent vectors]].

Accordingly two cotangent vectors are bicharacteristically related $(x_1,k_1) \sim (x_2,k_2)$ precisely if there is a [[lightlike]] [[geodesic]] connecting the points, with $k_1$ and $k_2$ the corresponding cotangents, hence one the result of [[parallel transport]] of the other along the geodesic.

=--

([Radzikowski 96, prop. 4.2 and below (6)](#Radzikowski96))

Specifically on [[Minkowski spacetime]]:


+-- {: .num_example}
###### Example
**([[bicharacteristic flow]] of [[Klein-Gordon operator]] on [[Minkowski spacetime]])**

Let $\mathbb{R}^{p,1}$ be [[Minkowski spacetime]] of [[dimension]] $p+1$ consider the [[Klein-Gordon operator]]

$$
  D
  \;=\;
  \eta^{\mu \nu} \frac{\partial}{\partial x^\mu} \frac{\partial}{\partial x^\nu}
  -
  \left(\tfrac{m c}{\hbar}\right)^2
  \,.
$$

Its [[principal symbol]] is the function

$$
  \array{
    T^\ast \mathbb{R}^{p,1}
      &\overset{q}{\longrightarrow}&
    \mathbb{R}
    \\
    (x,k) &\mapsto& \eta^{\mu \nu} k_\mu k_\nu
  }
$$

Hence $q(k) = 0$ is the condition that the [[wave vector]] $k$ be [[lightlike]].

The [[Hamiltonian vector field]] corresponding to $q$ is 

$$
  \begin{aligned}
    v_q 
    & =
    -\tfrac{1}{2} \eta^{\mu \nu} k_\mu \partial_{x^\nu}
    \\
    & =
    -\tfrac{1}{2} k^\mu \partial_{x^\mu}
  \end{aligned}
$$

in that

$$
  \begin{aligned}
    \iota_{v_q} d k_\mu \wedge d x^\mu
    &=
    \tfrac{1}{2} \eta^{\mu \nu} k_\mu d k_\mu
    \\
    & =
    d q(k)
  \end{aligned}
$$

It follows that the [[bicharacteristic curves]] are precisely the [[lightlike]] [[curves]] 

$$
  \array{
    \mathbb{R} &\overset{\gamma_k}{\longrightarrow}& \mathbb{R}^{p,1}
    \\
    \tau &\mapsto& (\gamma^\mu(0) +  \tau k^\mu)
  }
$$

and the corresponding [[bicharacteristic strips]] are these with their lightlike contangent vector constantly carried along 


$$
  \array{
    \mathbb{R} &\overset{\gamma_k}{\longrightarrow}& T^\ast\mathbb{R}^{p,1}
    \\
    \tau &\mapsto& \left((\gamma^\mu(0) +  \tau k^\mu),(k_\mu)\right)
  }
$$


=--

## Properties

### Propagation of singularities

The _[[propagation of singularities theorem]]_ says that the [[wave front set]] of a [[distribution|distributional]] solution to the [[differential equation]] of a sufficiently nice [[differential operator]] (or generally of a [[properly supported pseudo-differential operator]]) is preserved by the bicharacteristic flow.


## References


* {#DuistermaatHoermander72} [[Johann Duistermaat]], [[Lars Hörmander]], _Fourier integral operators II_, Acta Mathematica 128, 183-269, 1972 ([Euclid](https://projecteuclid.org/euclid.acta/1485889724))

Review in the context of the [[free field|free]] [[scalar field]] on [[globally hyperbolic spacetimes]] (with $Q$ the [[wave operator]]/[[Klein-Gordon operator]]) is in

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

[[!redirects bicharacteristic flows]]

[[!redirects bicharacteristic strip]]
[[!redirects bicharacteristic strips]]

[[!redirects bicharacteristic curve]]
[[!redirects bicharacteristic curves]]

