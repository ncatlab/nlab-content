
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Perfectoid spaces_ are a variant of [[Huber spaces]] in [[analytic geometry]]. The concept  was introduced ([Scholze 11](#Scholze11)) in order to generalize the classical theorem of ([Fontaine-Winterberger 79](#FontaineWinterberger79)) (see also at _[[function field analogy]]_). 

This theorem establishes an [[isomorphism]] between the [[absolute Galois groups]] of the extension $L:=\cup_{n}\mathbb{Q}_{p}[p^{1/p^{n}}]$ of the [[p-adic numbers]] and of the [[perfect field|perfection]] $L^{\flat}:=\cup_{n}\mathbb{F}_{p}((t^{1/p^{n}}))$ of the field of [[Laurent series]] of the [[finite field]] $\mathbb{F}_p$ (the isomorphism between Galois groups continues to hold after passing to the completions of these fields - it is these completions that are more properly called _perfectoid_). The field $L^{\flat}$ is called the _tilt_ of $L$. In ([Scholze 11](#Scholze11)) this is generalized by the statement that the perfectoid spaces over fields related this way are equivalent. (See [Bhatt 14](#Bhatt14) for a review).

## Definitions

The reference for these definitions are [Weinstein17](#Weinstein17).

### Perfectoid fields

* A nonarchimedean field $K$ of residue characteristic $p$ is _perfectoid_ if its value group is nondiscrete and the $p$-th power Frobenius map on $K^{\circ}/p$ is surjective (here $K^{\circ}$ is the subset of power bounded elements).

### Perfectoid rings

* A _Huber ring_ is a topological ring $A$ which contains an open subring $A_{0}$ which is adic with respect to a finitely generated ideal of definition $I\subseteq A_{0}$.

* A Huber ring $A$ is _Tate_ if it contains a topologically nilpotent unit $\varpi$ (also called a _pseudouniformizer_).

* A Tate Huber ring is _perfectoid_ if it is complete, uniform (the subset of power-bounded elements is bounded), and contains a pseudo-uniformizer $\varpi$ such that $\varpi^{p}\vert p$ and the p-th power map $A/\varpi\to A/\varpi^{p}$ is an isomorphism.

### Perfectoid space

* A _perfectoid space_ is an [[adic space]] which can be covered by affinoids $Spa(A,A^{+})$, where $A$ is a perfectoid ring.

## Related concepts

* [[Berkovich space]]

* [[global analytic geometry]]

* [[p-adic Hodge theory]]

* [[perfectoid field]]


## References

Exposition includes

* Michael Harris, _The perfectoid concept: Test case for an absent theory_ ([pdf](http://www.math.columbia.edu/~harris/otherarticles_files/perfectoid.pdf))

The concept is due to 

* {#Scholze11} [[Peter Scholze]], _Perfectoid spaces_ ([arXiv:1111.4914](http://arxiv.org/abs/1111.4914))

motivated by

* {#FontaineWinterberger79} [[Jean-Marc Fontaine]], [[Jean-Pierre Wintenberger]], _Extensions alg&#233;brique et corps des normes des extensions APF des corps locaux_, C. R. Acad. Sci. Paris S&#233;r. A&#8211;B 288(8) (1979), A441&#8211;A444

Review includes

* {#Bhatt14} [[Bhargav Bhatt]], _What is... a perfectoid space?_, Notices of the AMS, volume 61, number 9 ([[BhattPerfectoidSpace.pdf:file]])

* [[Bhargav Bhatt]], _Lecture notes for a class on perfectoid spaces_, ([pdf](http://www-personal.umich.edu/~bhattb/teaching/mat679w17/lectures.pdf))

* [[Peter Scholze]], _Perfectoid spaces: a survey_ ([arXiv:1303.5948](http://arxiv.org/abs/1303.5948))

* {#Weinstein17}Jared Weinstein, _Adic spaces_, lecture notes for the 2017 Arizona Winter School [pdf](https://swc-math.github.io/aws/2017/2017WeinsteinNotes.pdf)

See also 

* Wikipedia, _[Perfectoid space](https://en.wikipedia.org/wiki/Perfectoid_space)_

Formalization in [[type theory]] (in [[Lean]]):

* {#BCM} [[Kevin Buzzard]], Johan Commelin, Patrick Massot, _[lean-perfectoid-spaces](https://github.com/leanprover-community/lean-perfectoid-spaces)_

[[!redirects perfectoid spaces]]
