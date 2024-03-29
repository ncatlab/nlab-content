
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition

The _special orthogonal group_ or _rotation group_, denoted $SO(n)$, is the [[group]] of [[rotations]] in a  [[Cartesian space]] of [[dimension]] $n$. 

This  is one of the [[classical Lie groups]]. It is the [[connected component]] of the neutral element in the [[orthogonal group]] $O(n)$.

For instance for $n=2$ we have $SO(2)$ the [[circle group]].

It is the first step in the [[Whitehead tower]] of $O(n)$

$$
  \cdots \to Fivebrane(n) \to String(n) \to Spin(n) \to SO(n) \to \mathrm{O}(n)
  \,,
$$

the next step of which is the [[spin group]]. 

In [[physics]] the rotation group is related to [[angular momentum]].

## Properties

### Homology and cohomology 
 {#HomologyAndCohomology}

On the [[ordinary cohomology]] of the [[classifying spaces]] [[BO(n)|$B O(n)$]] and [[BSO(n)|$B SO(n)$]]

* with [[cyclic group of order 2|$\mathbb{Z}_2$]] [[coefficients]]:

  generated by the [[Stiefel-Whitney classes]]

  (e.g. [Milnor & Stasheff 74, Theorem 7.1. & Theorem 12.4.](#MilnorStasheff74))

* with [[integer]] [[coefficients]] ([[integral cohomology]]):

  generated by the [[integral Stiefel-Whitney classes]] and the [[Pontrjagin classes]]

  (e.g. [Brown 82](#Brown82), [Feshbach 83](#Feshbach83), [Pittie 91](#Pittie91), [Rudolph-Schmidt 17, Theorem 4.2.23](#RudolphSchmidt17))



### As part of the ADE pattern

[[!include ADE -- table]]


### Relation to orientation of manifolds

For $X$ an $n$-dimensional [[manifold]] a lift of [[generalized the|the]] classifying map $X \to \mathcal{B}O(n)$ of the $O(n)$-[[principal bundle]] to which the [[tangent bundle]] $T X$ is [[associated bundle|associated]] is the same as a choice of [[orientation]] of $X$.

## Examples

* For the almost degenerate case $n = 2$ there are exceptional [[isomorphisms]] of [[Lie groups]]

  $$
    SO(2) \simeq U(1) \simeq Spin(2)
  $$

  with the [[circle group]] and [[spin group]] in dimension 2.

* the case of [[SO(8)]] is special, since in the [[ADE classification]] of [[simple Lie groups]] it corresponds to [[D4]], which makes its [[representation theory]] enjoy _[[triality]]_.

\linebreak

[[!include low dimensional rotation groups -- table]]

\linebreak

## Related concepts

$\cdots \to$ [[Fivebrane group]] $\to$ [[string group]] $\to$ [[spin group]] $\to$ **special orthogonal group** $\to$ [[orthogonal group]].

[[!include table of orthogonal groups and related]]

* [[Euler angles]]

* [[finite rotation group]]

## References
 {#References}

For general references see also at _[[orthogonal group]]_.

[[ordinary cohomology]] of the [[classifying spaces]]:

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) &lbrack;[ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf)&rbrack;

* {#Brown82} [[Edgar H. Brown]], _The Cohomology of $B SO_n$ and $BO_n$ with Integer Coefficients_, Proceedings of the American Mathematical Society Vol. 85, No. 2 (Jun., 1982), pp. 283-288 ([jstor:2044298](https://www.jstor.org/stable/2044298))

* {#Feshbach83} Mark Feshbach, _The Integral Cohomology Rings of the Classifying Spaces of $\mathrm{O}(n)$ and $\mathrm{SO}(n)$,_ Indiana Univ. Math. J.  32 (1983), 511-516 ([doi:10.1512/iumj.1983.32.32036](https://doi.org/10.1512/iumj.1983.32.32036))

* {#Pittie91} [[Harsh Pittie]], _The integral homology and cohomology rings of SO(n) and Spin(n)_, Journal of Pure and Applied Algebra Volume 73, Issue 2, 19 August 1991, Pages 105&#8211;153 (<a href="https://doi.org/10.1016/0022-4049(91)90108-E">doi:10.1016/0022-4049(91)90108-E</a>)

* [[Howard Georgi]], §21 & 22 in: *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;

  > with an eye towards application to [[spinors]] in (the [[standard model of particle physics|standard model]] of) [[particle physics]]


* {#RudolphSchmidt17} [[Gerd Rudolph]], [[Matthias Schmidt]], around Theorem 4.2.23 of: _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))


See also

* {#Stasheff13} [[Jim Stasheff]], _The topology and algebra of $SO(n-1) \to SO(n) \to S^{n-1}$_, Herman's seminar July 2013 ([[StasheffSOn.pdf:file]])
 

[[!redirects special orthogonal groups]]

[[!redirects rotation group]]
[[!redirects rotation groups]]

[[!redirects SO(n)]]

