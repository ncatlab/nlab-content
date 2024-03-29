


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


+-- {: .num_defn #SymbolOrder}
###### Definition
**([[symbol order]])**

A [[smooth function]] $q$ on a [[cotangent bundle]] (e.g. the [[symbol of a differential operator]]) is of _order $m$_ (and type $1,0$, denoted $q \in S^m = S^m_{1,0}$), for $m \in \mathbb{N}$, if on each [[coordinate chart]] $((x^i), (k_i))$ we have that for every [[compact subset]] $K$ of the base space and all multi-indices $\alpha$ and $\beta$, there is a  [[real number]] $C_{\alpha, \beta,K } \in \mathbb{R}$ such that the [[absolute value]] of the [[partial derivatives]] of $q$ is bounded by


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

A [[Fourier integral]] operator $Q$ is of _[[symbol class]]_ $L^m = L^m_{1,0}$ if

1. it is of the form

   $$
     Q f (x)
     \;=\;
     \int \int e^{i k \cdot (x - y)} \hat f(x,y,k) f(y) \, d y d k
   $$

1. its [[principal symbol]] $q$ is of order $m$, in the above sense.

=--

([H&#246;rmander 71, def. 1.1.1 and first sentence of section 2.1](#Hoermander71))

## Examples

+-- {: .num_example}
###### Example

The [[wave operator]]/[[Klein-Gordon operator]] on [[Minkowski spacetime]] is of class $L^2$, according to def. \ref{SymbolOrder}.

=--


## Related concepts

* [[propagation of singularities theorem]]


## References

* {#Hoermander71} [[Lars Hörmander]], _Fourier  integral  operators I._ Acta  Mathematica  127, 79-183 (1971) ([Euclid](https://projecteuclid.org/euclid.acta/1485889699))

[[!redirects symbol orders]]

[[!redirects symbol class]]
[[!redirects symbol classes]]
