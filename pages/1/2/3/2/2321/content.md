
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
#### Integration theory
+-- {: .hide}
[[!include integration theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

The basic concept is for [[vector spaces]], and the remainder are defined in terms of that.

+-- {: .num_defn #basis}
###### Definition

**_(orientation of a vector space)_**
Given an [[ordered field]] $K$ and a [[vector space]] $V$ over $K$ of dimension $n$ (a [[natural number]]), an __orientation__ of $V$ is a choice of one of the two [[equivalence classes]] of [[linear order|ordered]] [[linear bases]] of $V$, where two bases are considered equivalent if the transformation matrix from one to the other has [[positive number|positive]] [[determinant]].
=--

In the case $n = 0$, the only ordered basis is the [[empty list]], but we still declare there to be two orientations by fiat, usually called positive and negative.  We can make the definition seamless by taking the elements of the equivalence class to be pairs consisting of an ordered basis and a nonzero [[sign]] (positive or negative), with $(B_1, s_1) \sim (B_2, s_2)$ iff $\sgn \det I^{B_1}_{B_2} = s_1/s_2$.  This is redundant except in dimension $0$, where now each equivalence class has a single element, $(*, +)$ for the positive orientation and $(*, -)$ for the negative orientation (where $*$ is the empty list).

In any case, this ensures that if $\omega$ is an orientation, then there is also an __opposite orientation__ $-\omega$.


Another way to say the same is
+-- {: .num_defn #bigwedge}
###### Definition

**_(orientation of a vector space)_**
For $V$ a vector space of dimension $n$, an __orientation__ of $V$ is an equivalence class of nonzero elements of the [[line]] $\bigwedge^n V$, the $n$th [[alternating power]] of $V$, where two such elements are considered equivalent when either (hence each) is a positive multiple of the other.
=--

Note that by both definitions, an orientation of a [[line]] (with $n = 1$) is an equivalence class of nonzero elements.

Assuming that $K$ is the field of [[real numbers]] or something like it, we can generalize from vector spaces to vector bundles:

+-- {: .num_defn #bundle}
###### Definition

**_(orientation of a vector bundle)_**
For $X$ a [[manifold]] and $V \to X$ a [[vector bundle]] of [[rank]] $k$, an __orientation__ on $V$ is an [[equivalence class]] of [[trivialization|trivializations]] of the [[line bundle]] $\bigwedge^k V$ that is obtained by associating to each [[fiber]] of $V$ its $k$th [[alternating power]].
=--

Equivalently for a [[smooth manifold]] this is an equivalence class of an everywhere non-vanishing element of $\bigwedge^k_{C^\infty(X)} \Gamma(V)$, which may be considered the [[sign]] of the element.

+-- {: .num_defn #manifold}
###### Definition

**_(orientation of a manifold)_**
For $X$ a [[manifold]] of dimension $n$, an __orientation__ of $X$ is an orientation of the [[tangent bundle]] $T X$ (or [[cotangent bundle]] $T^* X$).
=--

This is equivalently a choice of everywhere non-vanishing [[differential form]] on $X$ of degree $n$; the orientation may be considered the [[sign]] of the $n$-form (and the $n$-form\'s [[absolute value]] is a [[pseudoform|pseudo]]-$n$-form).

A vector space always has an orientation, but a manifold or bundle may not.  If an orientation exists, $V$ (or $X$) is called __orientable__.  If $X$ is a [[connected space]] and $V$ (or $X$) is orientable, then there are exactly $2$ orientations; more generally, the entire bundle is orientable iff the restriction to each [[connected component]] is orientable, and then the number of orientations is $2^k$, where $k$ is the number of orientable components.  (Or we can always say that the number of orientations is $2^k 0^m$, where now $m$ is also the number of nonorientable components.)


## Properties

### In terms of lifting through Whitehead tower 

An orientation on a [[Riemannian manifold]] $X$ is equivalently a lift $\hat g$ of the classifying map $g : X \to \mathcal{B}O(n)$ of its [[tangent bundle]] through the fist step $S O(n) \to O(n)$ in the [[Whitehead tower]] of $X$:

$$
  \array{
    && \mathcal{B}S O(n)
    \\
    & {}^{\hat g}\nearrow & \downarrow
    \\
    X &\stackrel{g}{\to}& \mathcal{B} O(n)
  }
  \,.
$$

From this perspective a choice of orientation is the first in a series of special structures on $X$ that continue with

* **orientation**

* [[spin structure]]

* [[string structure]], [[differential string structure]]

* [[fivebrane structure]], [[differential fivebrane structure]]


### In terms of orientation in generalized cohomology

For $R$ an [[E-∞ ring]] spectrum, there is a general notion of $R$-orientation of vector bundles. This is described at

* [[orientation in generalized cohomology]].

For $R = H(\mathbb{R})$ be the [[Eilenberg-MacLane spectrum]]
for the [[discrete group|discrete]] [[abelian group]] $\mathbb{R}$
of [[real number]]s, orientation in $R$-cohomology is equivalent to the 
ordinary notion of orientation described above.


## Related concepts

* [[orientation double cover]]

[[!include higher spin structure - table]]


[[!redirects orientation]]
[[!redirects orientations]]

[[!redirects oriented]]
[[!redirects orientedness]]

[[!redirects orientable]]
[[!redirects orientability]]
[[!redirects nonorientable]]
[[!redirects nonorientability]]
[[!redirects non-orientable]]
[[!redirects non-orientability]]

[[!redirects orientation structure]]
[[!redirects orientation structures]]

[[!redirects oriented manifold]]
[[!redirects orientable manifold]]
[[!redirects nonorientable manifold]]
[[!redirects non-orientable manifold]]
