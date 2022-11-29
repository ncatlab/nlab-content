
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

This theorem establishes an [[isomorphism]] between the [[absolute Galois groups]] of the extension $L \coloneqq \cup_{n}\mathbb{Q}_{p}[p^{1/p^{n}}]$ of the [[p-adic numbers]] and of the [[perfect field|perfection]] $L^{\flat} \coloneqq \cup_{n}\mathbb{F}_{p}((t^{1/p^{n}}))$ of the field of [[Laurent series]] of the [[finite field]] $\mathbb{F}_p$ (the isomorphism between Galois groups continues to hold after passing to the completions of these fields - it is these completions that are more properly called _perfectoid_). The field $L^{\flat}$ is called the _tilt_ of $L$. In ([Scholze 11](#Scholze11)) this is generalized by the statement that the perfectoid spaces over fields related this way are equivalent. (See [Bhatt 14](#Bhatt14) for a review).

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

## Generalizations

The concept of perfectoid space can be generalized into that of a _diamond_, which is a quotient of a perfectoid space of characteristic $p$ by a perfectoid equivalence relation ([ScholzeWeinstein20](#ScholzeWeinstein20), Definition 8.3.1). The concept of diamond can similarly be generalized into that of a _v-sheaf_, and in particular a _small v-sheaf_ is a quotient of a diamond by a diamond equivalence relation ([ScholzeWeinstein20](#ScholzeWeinstein20), Proposition 17.2.2).

## Applications

One application of perfectoid spaces is in relating [[Galois representations]] to torsion in the cohomology of [[Shimura varieties]]. In turn, using the excision sequence, one can relate this to the cohomology of arithmetic manifolds that are not Shimura varieties (for example Bianchi manifolds, which are quotients of [[hyperbolic 3-space]] by an arithmetic subgroup). This is surveyed in section 5 of [Weinstein15](#Weinstein15).

## Related concepts

* [[Berkovich space]]

* [[global analytic geometry]]

* [[p-adic Hodge theory]]

* [[perfectoid field]]

* [[prismatic cohomology]]


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

Perfectoid spaces and related concepts were the topic of a course at Berkeley in 2014, whose lecture notes have now been made into a book:

* {#ScholzeWeinstein20} [[Peter Scholze]] and Jared Weinstein, _Berkeley Lectures on p-adic Geometry_ [pdf](https://www.math.uni-bonn.de/people/scholze/Berkeley.pdf)

Some applications of perfectoid spaces are discussed in

* {#Weinstein15} Jared Weinstein, _Reciprocity Laws and Galois Representations: Recent Breakthroughs_ [pdf](https://math.bu.edu/people/jsweinst/CEB/BAMS.pdf)

See also 

* Wikipedia, _[Perfectoid space](https://en.wikipedia.org/wiki/Perfectoid_space)_

Formalization in [[type theory]] (in [[Lean]]):

* {#BCM} [[Kevin Buzzard]], Johan Commelin, Patrick Massot, _[lean-perfectoid-spaces](https://github.com/leanprover-community/lean-perfectoid-spaces)_

[[!redirects perfectoid spaces]]
