
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[topology]] a _universal vector bundle_ of some [[rank of a vector bundle|rank]] $n$ is a [[vector bundle]] $\zeta_n \to B GL(n)$ (over a base space to be called a _[[classifying space]]_) such that every other [[vector bundle]] $E \to X$ of rank $n$ over a suitably [[nice topological space]] ([[paracompact topological space]]) arises as the [[pullback bundle]] $E \simeq f^\ast \zeta_n$ of the universal bundle, along some morphisms ([[continuous function]]) $f \colon X \to B GL(n)$ which is unique up to [[homotopy]]:

$$
  \array{
    \zeta_n &\longrightarrow& E GL(n)
    \\
    \downarrow &(pb)& \downarrow
    \\
    X &\underset{f}{\longrightarrow}& B GL(n)
  }
  \,.
$$


The _universal real vector_ $\zeta_n$ of rank $n$ is the [[vector bundle]] which is [[associated bundle|associated]] to the [[universal principal bundle]] $E GL(n) \to B GL(n)$ (with [[structure group]] the [[general linear group]]) over the given [[classifying space]], equivalently to $E O(n) \to B O(n)$:

$$
  \zeta_n \coloneqq (E O(n))\underset{O(n)}{\times} \mathbb{R}^n
  \,.
$$

Similarly for [[complex vector bundles]]

$$
  \zeta^{\mathbb{C}}_n \coloneqq (E U(n))\underset{U(n)}{\times} \mathbb{R}^{2n}
  \,.
$$

etc.

## Constructions 

### Via Grassmannians and Stiefel manifolds

For $n, k \in \mathbb{N}$, and $n \leq k$, there is the _[[Grassmannian manifold]]_ given as the [[coset]] [[topological space]]

$$
  Gr_n(k)
    \coloneqq
  O(k)/(O(n)\times O(k-n))
  \,.
$$


Similarly, the _[[Stiefel manifold]]_ is the [[coset]]

$$
  V_n(k) \coloneqq O(k)/O(n)
  \,.
$$

The [[quotient]] [[projection]]

$$
  V_{k-n}(k)\longrightarrow Gr_n(k)
$$

is an $O(n)$-[[principal bundle]], with [[associated bundle]] $V_n(k)\times_{O(n)} \mathbb{R}^n$ a [[vector bundle]] of [[rank]] $n$. In the limit ([[colimit]]) that $k \to \infty$ is this gives a presentation of the $O(n)$-[[universal principal bundle]] and of the [[universal vector bundle]] of rank $n$, respectively.. The base space $Gr_n(\infty)\simeq_{whe} B O(n)$ is the [[classifying space]] for $O(n)$-[[principal bundles]] and rank $n$ vector bundles.

## Examples

* [[universal complex line bundle]]

* [[tautological line bundle]]

## References

Textbook accounts include

* {#Kochmann96} [[Stanley Kochmann]], section 1.3 of of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-Theory_, (partly finished book) [web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html)


[[!redirects universal vector bundles]]

[[!redirects universal complex vector bundle]]
[[!redirects universal complex vector bundles]]

