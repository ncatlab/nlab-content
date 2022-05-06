

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}



## Definition

Let $X_1, X_2$ be two [[open subsets]] of [[Cartesian spaces]]. Then a [[smooth function]] $K \in C^\infty(X_1 \times X_2)$ on the [[Cartesian product]] of these two manifolds defines a [[linear function]] 

$$
  \array{
    C^\infty_{cp}(X_2) &\overset{}{\longrightarrow}& C^\infty(X_1)
    \\
    \phi &\mapsto& \mathcal{K}(\phi)
  }
  \,,
$$

by the "[[integral transform]]":

$$
  \mathcal{K}(\phi) \;\colon\; x_1 \mapsto \int_{X_2} K(x_1, x_2) \phi(x_2) \, dvol(x_2) 
$$

More generally, this expression makes sense for

$$
  K
  \;\in\;
  \mathcal{D}'(X_1 \times X_2) 
$$

a [[distribution]] on $X_1 \times X_2$ (a "distribution of two variables"), which makes the result itself in general be a distribution

$$
  \array{
    C^\infty_{cp}(X_2) &\overset{}{\longrightarrow}& \mathcal{D}'(X_1)
    \\
    \phi &\mapsto& \mathcal{K}(\phi)
  }
  \,.
$$

Here $K$ is called the _[[integral kernel]]_ and $\mathcal{K}(\phi)$ the corresponding _[[integral transform]]_.

## Properties

### Schwartz kernel theorem

The _Schwarz kernel theorem_ states that this construction constitutes a [[linear isomorphism]] between Schwartz [[integral kernels]] and "distribution-valued distributions"

$$
  \array{
    \mathcal{D}'(X_1 \times X_2)
    &\overset{\simeq}{\longrightarrow}&
    \mathcal{D}'( X_2, \mathcal{D}'(X_1) )
    \\
    K &\mapsto& \mathcal{K}
  }
$$

$\,$


+-- {: .num_prop #PartialProductOfDistributionsOfSeveralVariables}
###### Proposition
**(partial [[product of distributions|product of]] [[distributions of several variables]])**

Let 

$$
  K_1 \in \mathcal{D}'(X \times Y)
  \phantom{AAA}
  K_2 \in \mathcal{D}'(Y \times Z)
$$

be two [[distributions of two variables]]. For their [[product of distributions]] to be defined over $Y$, [[Hörmander's criterion]] on the [[pair]] of [[wave front sets]] $WF(K_1), WF(K_2)$  needs to hold for the [[wave front set|wave front]] [[wave vectors]] along $X$ and $Y$ taken to be zero.

If this is satisfied, then composition of [[integral kernels]] (if it exists)

$$
  (K_1 \circ K_2)(-,-)
  \;\coloneqq\;
  \underset{Y}{\int}
    K_1(-,y) K_2(y,-)
  dvol_Y(y)
  \;\in\;
  \mathcal{D}'(X \times Z)
$$

has [[wave front set]] constrained by

$$
  WF(K_1 \circ K_2)
  \;\subset\;
  WF(K_1) \circ WF(K_2)
  \;\cup\;
  (X \times \{0\}) \times WF(K_2)
  \;\cup\;
  WF(K_1) \times (Z \times \{0\})
  \,,
$$

where on the left the composition symbol means composition of [[relations]] of [[wave vectors]] over points in $Y$.

=--

([Hörmander 90, theorem 8.2.14](product+of+distributions#Hoermander90))



## Related concepts

* [[tensor product of distributions]]

* [[polynomial observable]], [[microcausal observable]]

* [[correlators as differential forms on configuration spaces of points]]

## References

* {#Hoermander90} [[Lars Hörmander]], section 5.2 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990 ([pdf](http://www.ctr.maths.lu.se/media/MATP11/2014vt2014/distho.pdf))

See also

* Wikipedia, _[Schwartz kernel theorem](http://en.wikipedia.org/wiki/Schwartz_kernel_theorem)_

[[!redirects Schwartz kernels]]

[[!redirects Schwartz kernel theorem]]
[[!redirects Schwartz kernel theorems]]

[[!redirects distribution of two variables]]
[[!redirects distributions of two variables]]

[[!redirects distribution in two variables]]
[[!redirects distributions in two variables]]


[[!redirects distribution of several variables]]
[[!redirects distributions of several variables]]


