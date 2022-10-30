
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

For $X$ a [[compact space|compact]], [[connected]], [[orientation|oriented]] 3-[[dimension]]al [[manifold]], write 

$$
  2 T X := T X \oplus T X
$$

for the fiberwise [[direct sum]] of the [[tangent bundle]] with itself. Via the [[diagonal]] embedding

$$
  SO(3) \to SO(3) \times SO(3) \hookrightarrow SO(6)
$$

this naturally induces a [[special orthogonal group|SO(6)]]-[[principal bundle]]. Due to the low dimension, this always lifts to a [[spin group|spin(6)]]-[[principal bundle]].

A **2-framing** on $X$ is a [[homotopy]] class of trivializations of this Spin-bundle.


## Properties

### Relation to bounding 4-manifolds

In ([Atiyah](#Atiyah1990)) it is shown how a framing on a compact connected oriented 3-manifold $X$ is induced a 4-manifold $Z$ with [[boundary]] $\partial Z \simeq X$. In fact, a framing is equivalently a choice of [[cobordism]] class of bounding 4-manifolds ([Kerler](#Kerler)).

Discussion of 2-framing entirely in terms of bounding 4-manifolds is for instance in ([Sawin](#Sawin)).

### Relation to String-structures

By ([Atiyah 2.1](#Atiyah)) a 2-framing of a 3-manifold $X$ is equivalently a  
$p_1$-[[twisted differential c-structures|structure]], where $p_1$ is the first [[Pontryagin class]], hence a homotopy class of a trivialization of

$$
  p_1(X) \colon X \to B SO(3) \stackrel{p_1}{\to} K(\mathbb{Z},4)
  \,.
$$

This perspective on framings is made explicit in ([Bunke-Naumann, section 2.3](#BunkeNaumann)). It is mentioned for instance also in ([Freed, slide 5](#Freed)).

## Related concepts

* [[framed manifold]]

* [[string structure]].

## References

The notion of "2-framing" is due to

* [[Michael Atiyah]], _On framings of 3-manifolds_ , Topology, Vol. 29, No 1, pp. 1-7 (1990) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/atiyahfr.pdf))
  {#Atiyah1990}

making explicit a structure which slightly implicit in the discussion of the [[path integral]] of [[Chern-Simons theory]] in 

* [[Edward Witten]], _Quantum field theory and the Jones Polynomial_ , Comm. Math. Phys.  121 (1989)

(see [Atiyah, page 6](#Atiyah)). For more on the role of 2-framings in [[Chern-Simons theory]] see also

* [[Dan Freed]], Robert Gompf, _Computer calculation of Witten's 3-Manifold invariant_, Commun. Math. Phys. 141,79-117 (1991) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/freedgompf.pdf))

* [[Dan Freed]], _Remarks on Chern-Simons theory_ ([pdf slides])
 {#Freed}

and for discussion in the context of the [[M2-brane]] from p. 7 on in 

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]] II: Twisted $String$ and $String^c$-structures_  ([arXiv:1007.5419](http://arxiv.org/abs/1007.5419)).

The relation to [[string structures]] is made explicit in section 2.3 of 

* [[Ulrich Bunke]], [[Niko Naumann]], _Secondary Invariants for String Bordism and tmf_ ([arXiv:0912.4875](http://arxiv.org/abs/0912.4875))
 {#BunkeNaumann}

Discussion in terms of bounding 4-manifolds is in 

* Thomas Kerler, _Bridged links and tangle presentations of cobordism categories_. Adv. Math., 141(2):207&#8211;281, (1999) ([arXiv:math/9806114](http://arxiv.org/abs/math/9806114))
 {#Kerler}

* Stephen F. Sawin, _Three-dimensional 2-framed TQFTS and surgery_ (2004) ([pdf](http://digitalcommons.fairfield.edu/cgi/viewcontent.cgi?article=1020&context=mathandcomputerscience-facultypubs))
 {#Sawin}

page 9 of 

* Stephen Sawin, _Invariants of Spin Three-Manifolds From Chern-Simons Theory and Finite-Dimensional Hopf Algebras_ ([arXiv:math/9910106](http://arxiv.org/abs/math/9910106))

[[!redirects 2-framing]]
[[!redirects 2-framings]]
