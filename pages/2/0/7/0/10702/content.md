
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The _Adams operations_ are endo-[[cohomology operations]] on [[K-theory]]. They are an example of [[power operations]].

## Definition

For $k \in \mathbb{N}$, the $k$th Adams operation 

$$
  \psi^k \;\colon\; K(X) \longrightarrow K(X)
$$

is characterized by the fact that 

1. $\psi^k$ is a [[functor|functorial]] [[ring]] [[homomorphism]];

1. applied to a [[K-theory]] class $[L]$ represented by a [[line bundle]] $L$, $\psi^k$ is the $k$th [[tensor power]] $\psi^k(L) = L^{\otimes ^k}$;


## Properties

### Adams conjecture

The [[Adams conjecture]] (a [[theorem]]) says that for all $k \in \mathbb{N}$ and $V \in K(X)$ there is $n \in \mathbb{N}$ such that the [[spherical fibration]] assigned to the [[K-theory]] class $k^n (\psi^k(V)-V)$ under the [[J-homomorphism]] is trivial, hence that


$$
  J
  \left(
     k^n \left(
       \psi^k(V) - V
     \right)
  \right)
  = 0
  \,.
$$


## Related concepts

* [[Lambda-ring]]

* [[Steenrod square]]

* [[Steenrod operation]]

* [[power operation]]

## References

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 11 of _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))

* {#Hatcher} [[Allen Hatcher]], section 2.3 of _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))


* Wikipedia, _[Adams operation](http://en.wikipedia.org/wiki/Adams_operation)_


* [[Jacob Lurie]], remark 2 in: _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 35 _The image of $J$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture35.pdf))
 


[[!redirects Adams operations]]