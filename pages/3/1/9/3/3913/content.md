
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Thom space** $Th(V)$ of a [[vector bundle]] $V \to X$ over a [[topological space]] $X$ is the [[topological space]] obtained by first forming the disk bundle $D(V)$ of (unit) disks in the [[fibers]] of $V$ and then identifying to a point the [[boundaries]] of all the disks, i.e. forming the quotient by the [[sphere bundle]] $S(V)$:

$$
  Th(V) := D(V)/S(V)
  \,.
$$

(N.B.: this is a quotient of the *total* spaces of the bundles taken in $Top$, not a bundle quotient in $Top/V$.) This is equivalently the [[mapping cone]]

$$
  \array{
    S(V) &\to& *
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\to& Th(V)
  }
$$

in [[Top]] of the [[sphere]] [[bundle]] of $V$. Therefore more generally, for $P \to X$ any $S^n$-[[bundle]] over $X$, its Thom space is the the [[mapping cone]]

$$
  \array{
    P &\to& *
    \\
    \downarrow^{\mathrlap{p}} && \downarrow
    \\
    X &\to& Th(P)
  }
$$

of the bundle projection.


For $X$ a [[compact topological space]], the $Th(V)$ is a model for [[generalized the|the]] [[one-point compactification]] of the total space $V$.

The Thom space of the universal rank-$n$ vector bundle over the [[classifying space]] $B O(n)$ of the [[orthogonal group]] is usuelly denoted $M O(n)$. As $n$ ranges, these spaces form the [[Thom spectrum]].

## Properties

+-- {: .num_prop}
###### Observation

The Thom space of the rank-0 bundle over $X$ is the space $X$ with a basepoint freely adjoined:

$$
  Th(X \times \mathbb{R}^0) = Th(X) \simeq X_+
$$

=--

+-- {: .num_prop}
###### Proposition


For $V$ a vector bundle and $\mathbb{R}^n \oplus V$ its fiberwise [[direct sum]] with the trivial rank $n$ vector bundle we have

$$
  Th(V \oplus \mathbb{R}^n) \simeq S^n \wedge Th(V)
$$

is the [[smash product]] of the Thom space of $V$ with the $n$-[[sphere]] (the $n$-fold [[suspension]]).

=--

+-- {: .num_example}
###### Example

In particular, if $\mathbb{R}^n \times X \to X$ is a trivial vector bundle of [[rank]] $n$, then 

$$
  Th(X \times \mathbb{R}^n) \simeq S^n \wedge X_+
$$

is the [[smash product]] of the $n$-[[sphere]] with $X$ with one base 
point freely adjoined (the $n$-fold [[suspension]]).

=--

+-- {: .num_remark}
###### Remark

This implies that for every vector bundle $V$ the sequence of spaces
$Th(\mathbb{R}^n \oplus V)$ forms a [[suspension spectrum]]: this is called the [[Thom spectrum]] of $V$.

=--

## Related concepts

* [[cobordism theory]]

* [[one-point compactification]]

* [[Thom spectrum]]

* [[Thom isomorphism]]

## References

The [[Thom isomorphism]] for Thom spaces was originally found in

* [[René Thom]],   _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_  Comm. Math. Helv. , 28  (1954)  pp. 17&#8211;86

For general discussion see

* [[Michael Atiyah]], _Thom complexes_, Proc. London Math. Soc. __11__  (1961)  pp. 291&#8211;310

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability, and cobordism_, Springer 1998 [googB](http://books.google.hr/books?isbn=3540620435)

* [[eom]], _[Thom space](http://eom.springer.de/t/t092680.htm)_

* [[Dale Husemöller]], _Fibre bundles_ , McGraw-Hill  (1966)

* myyn.org [Thom space](http://myyn.org/m/article/thom-space), [Thom class](http://myyn.org/m/article/thom-class), [Thom isomorphism theorem](http://myyn.org/m/article/thom-isomorphism-theorem)

Also

* [[Robert Stong]], _Notes on cobordism theory_ , Princeton Univ. Press  (1968)

* W.B. Browder, _Surgery on simply-connected manifolds_ , Springer  (1972)


