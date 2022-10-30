
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


Let $X$ be a [[smooth manifold]] and let $D$ be a [[differential operator]] on (smooth [[sections]] of) the [[trivial line bundle]] over $X$. Then the [[symbol of a differential operator|symbol]] $q(D)$ of $D$ is equivalently a [[smooth function]] on the [[cotangent bundle]] $T^\ast X$ (by [this example](symbol+of+a+differential+operator#BicharacteristicFlow)). With the [[cotangent bundle]] canonically regarded as a [[symplectic manifold]], let 

$$
  v_{q(D)} \in \Gamma(T(T^\ast X))
$$ 

be the corresponding [[Hamiltonian vector field]]. 

+-- {: .num_prop #BicharacteristicFlow}
###### Definition

The _bicharacteristic flow_ of $D$ is the [[Hamiltonian flow|Hamiltonian]] [[flow of a vector field|flow]] of the [[Hamiltonian vector field]] $v_{q(D)}$. Moreover:

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

+-- {: .num_example #BicharachteristicFlowOfKleinGordonOperator}
###### Example
**(bicharacteristic curves of [[wave operator]]/[[Klein-Gordon operators]] are the [[lightlike]] [[geodesics]])**

Let $(X,e)$ be a [[Lorentzian manifold]] and let $D \coloneqq \Box_e + m^2$ be its [[wave operator]]/[[Klein-Gordon operator]]. Then the bicharacteristic curves of $D$ (def. \ref{BicharacteristicFlow}) are precisely the [[lightlike]] [[geodesics]] of $(X,e)$, and the bicharacteristic strips are precisely these geodesices with their [[cotangent vectors]].

Accordingly two cotangent vectors are bicharacteristically related $(x_1,k_1) \sim (x_2,k_2)$ precisely if there is a [[lightlike]] [[geodesic]] connecting the points, with $k_1$ and $k_2$ the corresponding cotangents, hence one the result of [[parallel transport]] of the other along the geodesic.

=--

([Radzikowski 96, prop. 4.2 and below (6)](#Radzikowski96))


## Properties

### Propagation of singularities

The _[[propagation of singularities theorem]]_ says that the [[wave front set]] of a [[distribution|distributional]] solution to the [[differential equation]] of a (suitably nice) [[differential operator]] is preserved by the bicharacteristic flow.


## References


* {#DuistermaatHoermander72} [[Johann Duistermaat]], [[Lars Hörmander]], _Fourier integral operators II_, Acta Mathematica 128, 183-269, 1972 ([Euclid](https://projecteuclid.org/euclid.acta/1485889724))

Review in the context of the [[free field|free]] [[scalar field]] on [[globally hyperbolic spacetimes]] (with $Q$ the [[wave operator]]/[[Klein-Gordon operator]]) is in

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

[[!redirects bicharacteristic flows]]

[[!redirects bicharacteristic strip]]
[[!redirects bicharacteristic strips]]

[[!redirects bicharacteristic curve]]
[[!redirects bicharacteristic curves]]

