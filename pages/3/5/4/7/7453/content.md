
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _2-Giraud theorem_ is the generalization of [[Giraud's theorem]] from [[topos theory]] to [[2-topos theory]].

## Statement

The following theorem, which generalizes the classical [[Giraud theorem]], is due to [[StreetCBS]].

+-- {: .num_theorem #Giraud}
###### Theorem
For a [[2-category]] $K$, the following are equivalent.

* $K$ is equivalent to the 2-category of [[2-sheaves]] on a small [[2-site]].
* $K$ is an infinitary [[2-pretopos]] with a small [[eso-generator]].
* $K$ is a [[reflective sub-2-category]] of a category $[C^{op},Cat]$ of [[2-presheaves]] with left-exact reflector.
=--

In fact, it is not hard to prove the same theorem for [[n-categories]], for any $1\le n\le 2$.

+-- {: .num_theorem #Giraud}
###### Theorem
For an [[n-category]] $K$, the following are equivalent.

* $K$ is equivalent to the $n$-category of [[n-sheaves]] on a small [[n-site]].
* $K$ is an infinitary [[n-pretopos]] with a small [[eso-generator]].
* $K$ is a reflective sub-$n$-category of a category $[C^{op},n Cat]$ of $n$-presheaves with left-exact reflector.
=--

For $n=2$ this is Street's theorem; for $n=1$ it is the classical theorem.  The other values included are of course $n=(1,2)$ and $n=(2,1)$.

## References

* [[Mike Shulman]], _[[michaelshulman:2-Giraud theorem]]_

