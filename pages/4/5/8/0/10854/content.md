
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

### In physics

In [[physics]] and especially in [[continuum mechanics]] and [[thermodynamics]], a physical quantity associated with a [[physical system]] extended in [[space]] is called


* _intensive_ if it is a [[function]] on (the physical system extended in) space;

* _extensive_ if it is a [[density]] or [[linear distribution]] on (the physical system extended in) space.

For instance for a [[solid body]] its [[temperature]] is intensive, but its [[mass]] is extensive: there is a temperature assigned to every point of the body (in the idealization of [[classical mechanics|classical]] [[continuum mechanics]] anyway) but a mass is assigned only to every little "extended" piece of the body, not to a single point.

This terminology in [[physics]] apparently originates with [[Richard Tolman]] in 1917.

### In geometry and algebra

In ([Lawvere 86](#Lawvere86)) it is amplified that this [[duality]] is generally a fundamental one also in [[mathematics]]: given a [[topos]] $\mathbf{H}$ with a [[commutative ring|commutative]] [[ring object]] $R \in CRing(\mathbf{H})$, then 

* the space of _intensive quantities_ on an [[object]] $X \in \mathbf{H}$ is the [[mapping space]] $[X,R]_{\mathbf{H}} \in CRing(\mathbf{H})$ formed in $\mathbf{H}$;

* the space of _extensive quantities_ on $X$ is the $R$-linear dual, namely the mapping space $[X,R]^\ast \coloneqq [[X,R], R]_{R Mod}$ formed in $R$-[[modules]] in $\mathbf{H}$.

* the [[integration]] map is the canonical [[evaluation]] pairing

  $$
    \int_X \;\colon\; [X,R] \times [X,R]^\ast  \longrightarrow R
    \,.
  $$

See also at _[[Lawvere distribution]]_.

### In higher geometry and higher algebra

Viewed this way, this naturally generalizes to the case where $\mathbf{H}$ is in fact an [[(∞,1)-topos]] and $R \in CRing(\mathbf{H})$ an [[E-∞ ring]]. In this case $[X,R]$ is called the  $R$-[[cohomology]] [[spectrum]] of $X$ and $[X,R]^\ast$ is the corresponding [[generalized homology]] spectrum. In this form intensive and extensive properties appear in [[physics]] in the context of [[motivic quantization]] of [[local prequantum field theory]]. 

More generally, for $\chi$ an $R$-[[(∞,1)-line bundle]] over $X$ then the corresponding extensive object is the $\chi$-twisted [[Thom spectrum]] $R_{\bullet + \chi}(X)$ and the intensive object is the $\chi$-[[twisted cohomology]] [[spectrum]] $R^{\bullet + \chi}(X) = [R_{\bullet+ \chi}(X),R]_{R Mod}$. See at _[[motivic quantization]]_ for how this appears in [[physics]].


## References

* Wikipedia, _[Intensive and extensive properties](http://en.wikipedia.org/wiki/Intensive_and_extensive_properties)_

* [[William Lawvere]], Introduction to _[[Categories in Continuum Physics]], Lectures given at a Workshop held at SUNY, Buffalo 1982. Lecture Notes in Mathematics 1174. 1986
 {#Lawvere86}


[[!redirects intensive or extensive]]
[[!redirects intensive or extensive quantity]]
[[!redirects intensive or extensive quantities]]
[[!redirects intensive and extensive]]
[[!redirects intensive and extensive quantities]]
[[!redirects extensive or intensive]]
[[!redirects extensive or intensive quantity]]
[[!redirects extensive or intensive quantities]]
[[!redirects extensive and intensive]]
[[!redirects extensive and intensive quantities]]

[[!redirects intensive]]
[[!redirects intensive quantity]]
[[!redirects intensive quantities]]

[[!redirects extensive]]
[[!redirects extensive quantity]]
[[!redirects extensive quantities]]
