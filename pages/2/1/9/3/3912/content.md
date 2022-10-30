
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
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

For $H$ a [[multiplicative cohomology theory]], and $V \to X$ a [[vector bundle]] of rank $n$, which is $H$-[[orientation in generalized cohomology|orientable]], the **Thom isomorphism** is the morphism
 
$$
  (-) \cdot u 
    \;\colon\; 
  H^\bullet(X) 
     \stackrel{\simeq}{\to} 
  \tilde H^{\bullet + n}(Th(V))
  \,.
$$

from the [[cohomology]] of $X$ to the [[reduced cohomology]] of the [[Thom space]] $Th(V)$, induced by [[cup product]] with a [[Thom class]] $u \in H^n(Th(V))$. That this is indeed an [[isomorphism]] follows from the nature of [[Thom classes]], for instance via the [[Leray-Hirsch theorem]] (see e.g. [Ebert 12, 2.3,2.4](#Ebert12)) or from running a [[Serre spectral sequence]] (e.g. [Kochmann 96, section 2.6](#Kochmann96)).

One may think of the Thom isomorphism from left to right as cupping with a generalized [[volume form]] on the fibers, and from right to left as performing [[fiber integration]].

## Definition

### Concretely

(...)

### General abstractly

A fully general abstract discussion is around page 30, 31 of ([ABGHR](#ABGHR)).

(...)

## Applications

* The Thom isomorphism is used to define [[fiber integration]] of multiplicative cohomology theories.

## Related concepts

* [[cobordism theory]]

* [[Thom space]], [[Thom spectrum]]

* [[fiber integration]]

* [[Pontrjagin-Thom collapse map]]

## References

The original proof that the Thom isomorphism is indeed an [[isomorphism]] is due to

* [[René Thom]],   _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_  Comm. Math. Helv. , 28  (1954)  pp. 17&#8211;86

Textbook accounts include

* {#Kochmann96} [[Stanley Kochmann]], section 2.6 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

See also

* W. Cockcroft, _On the Thom isomorphism Theorem_, Mathematical Proceedings of the Cambridge Philosophical Society (1962), 58 ([pdf](http://journals.cambridge.org/action/displayFulltext?type=1&fid=2056796&jid=PSP&volumeId=58&issueId=02&aid=2056788&bodyId=&membershipNumber=&societyETOCSession=))

Lecture notes include

* {#Francis3} [[John Francis]], _Topology of manifolds_, course notes (2010) ([web](http://math.northwestern.edu/~jnkf/classes/mflds/)), Lecture 3 _Thom's theorem_ (notes by A. Smith) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/3thom.pdf))

* [[Akhil Mathew]], _[The Thom isomorphism theorem](https://amathew.wordpress.com/2010/12/11/the-thom-isomorphism-theorem/)_, 2010

* {#Ebert12} [[Johannes Ebert]], sections 2.3, 2.4 of _A lecture course on Cobordism Theory_, 2012 ([pdf](http://wwwmath.uni-muenster.de/u/jeber_02/skripten/bordism-skript.pdf))

* {#Freed13} [[Dan Freed]], lecture 8 of _Bordism: old and new_, 2013 ([pdf](http://www.ma.utexas.edu/users/dafr/bordism.pdf))


A discussion in [[differential geometry]] with fiberwise compactly supported differential forms is around theorem 6.17 of 

* [[Raoul Bott]], [[Loring Tu]], _[[Differential Forms in Algebraic Topology]]_ 

A comprehensive general abstract account for [[multiplicative cohomology theories]] in terms of [[E-infinity ring]] [[spectra]] is in

* {#ABGHR} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 

An alternative simple formulation in terms of geometric cycles as in [[bivariant cohomology theory]] is in 

* Martin Jakob, _A note on the Thom isomorphism in geometric (co)homology_ ([arXiv:math/0403540](http://arxiv.org/abs/math/0403540))


See also

* [[Albrecht Dold]], _Relations between ordinary and extraordinary homology_ , Colloq. Algebraic Topology, August 1&#8211;10, 1962 , Inst. Math. Aarhus Univ.  (1962)  pp. 2&#8211;9

* [[Yuli Rudyak]], _On the Thom&#8211;Dold isomorphism for nonorientable bundles_  Soviet Math. Dokl. , 22  (1980)  pp. 842&#8211;844  Dokl. Akad. Nauk. SSSR , 255 : 6  (1980)  pp. 1323&#8211;1325

* R. M. Switzer,   _Algebraic topology - homotopy and homology_ , Springer  (1975)

* myyn.org (Planetmath) [Thom space](http://myyn.org/m/article/thom-space), [Thom class](http://myyn.org/m/article/thom-class), [Thom isomorphism theorem](http://myyn.org/m/article/thom-isomorphism-theorem)

