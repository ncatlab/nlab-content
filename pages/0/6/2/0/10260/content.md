
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### On a complex vector space
 {#OnAComplexVectorSpace}

A *quatermionic structure* on a [[complex vector space]] $V$ is an [[complex numbers|complex]]-[[anti-linear map]] 

$$
  \sigma 
    \,\colon\,
  V \longrightarrow V
  \,,
  \;\;\;\;\;
  \underset{v \in V}{\forall}
  \;
  \sigma(\mathrm{i}v) = - \mathrm{i} \sigma(v)
  \,,
$$

which squares to minus the [[identity map|identity]]:

$$
  \sigma^2 = -1
  \,.
$$

(Compare this to a *[[real structure]]*, which is such a $\mathbb{C}$-[[anti-linear map]]  that instead squares to $+1$, hence that is an [[involution]].)

Given such $\sigma$ then with the [[linear operator]] $\mathrm{i}$ of multiplication by the [[imaginary unit]] one obtains three [[real numbers|real]] [[linear maps|linear]] [[endomorphisms]]

$$
  \begin{aligned} 
    \mathbf{i} & \coloneqq \mathrm{i}
    \\
    \mathbf{j} & \coloneqq \sigma
    \\
    \mathbf{k} & \coloneqq \mathrm{i} \sigma
  \end{aligned}
$$

on $V$, which evidently induce on $V$ a [[real numbers|real]] [[linear maps|linear]] [[representation]] of the [[associative algebra|algebra]] of [[quaternions]].


### On a manifold

An *almost quaternionic structure* on a [[manifold]] of [[dimension of a manifold|dimension]] a multiple of 4, is a [[reduction of the structure group]] along the inclusion 

$$
  GL_n(\mathbb{H}) 
    \hookrightarrow 
  Gl_{4 n}(\mathbb{R})
$$

of [[general linear groups]], for $\mathbb{R}$ the [[real numbers]] and $\mathbb{H}$ the [[quaternions]], hence a *[[G-structure]]* for a quaterionic-[[general linear group]].

(...)


## Related concepts

* [[quaternionic unitary group]]

* [[real structure]], [[complex structure]]

* [[real vector space]], [[complex vector space]], [[quaternionic vector space]]

* [[para-quaternionic structure]]

## References

* Wikipedia, _[Quaternionic structure](http://en.wikipedia.org/wiki/Quaternionic_structure)_

* Wikipedia, _[Reduction of the structure group -- Examples](https://en.wikipedia.org/wiki/Reduction_of_the_structure_group#Examples)_

[[!redirects quaternionic structures]]

[[!redirects almost quaternionic structure]]

