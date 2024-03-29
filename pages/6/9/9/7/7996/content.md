
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A _metalinear structure_ on a [[smooth manifold]] of [[dimension]] $n$ is a [[lift of the structure group]] of the [[tangent bundle]] along the [[group extension]] $Ml(n) \to GL(n)$ of the [[general linear group]] by the [[metalinear group]].

## Properties


### Obstruction and existence

A metalinear structure on a manifold $Q$ of [[dimension]] $n$ exists precisely if the [[Chern class]] of the [[canonical bundle]] $\wedge^n T^*Q$ is divisible by 2. So a metalinear structure is equivalent to the existence of a [[square root]] [[line bundle]] $\sqrt{\wedge^n T^* Q}$ ( _[[Theta characteristic]]_ ).

This means that for $E \to Q$ any hermitean [[line bundle]], [[sections]] of the tensor product $E \otimes \sqrt{\wedge^n T^* Q}$ have a canonical [[inner product]] (if $Q$ is compact and orientable). This is the use of metalinear structure in [[metaplectic correction]].

### Relation to metaplectic structure

+-- {: .num_theorem}
###### Theorem

Let $(X,\omega)$ be a [[symplectic manifold]] and $L \subset T X$ a subbundle of [[Lagrangian subspaces]] of the [[tangent bundle]]. Then $T X$ admits a [[metaplectic structure]] precisely if $L$ admits a metalinear structure. 

=--

([Bates-Weinstein, theorem 7.16](#BatesWeinstein))


## Related concepts

* [[metaplectic structure]], [[metaplectic correction]]

* [[spin structure]]

[[!include square roots of line bundles - table]]


## References

Lecture notes include

* {#BatesWeinstein} Sean Bates, [[Alan Weinstein]], _[[Lectures on the geometry of quantization]]_, ([pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf))


Discussion with an eye towards [[Theta characteristics]] is in 

* [[Andrei Tyurin]], _Quantization, classical and quantum field theory and Theta-functions_ ([arXiv:math/0210466v1](http://arxiv.org/abs/math/0210466v1))



[[!redirects metalinear structures]]
