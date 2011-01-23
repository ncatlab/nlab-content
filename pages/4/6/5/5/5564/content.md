
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Idea

A _model structure of $(2,1)$-sheaves_ is a [[model category]] [[presentable (infinity,1)-category|presentation]] of the [[(2,1)-category of (2,1)-sheaves]] over some [[site]] or [[(2,1)-site]].


## Definition

There are several equivalent ways to set up a [[model category]] structure for $(2,1)$-sheaves. 

Suppose first that the [[(2,1)-site]] $C$ is just a 1-[[category]], hence just a [[site]].

* Write [[Grpd]] for the [[category]] of [[small category]] [[groupoid]]s and [[functor]]s between them. Write $Grpd_{nat}$ for the [[natural model structure on groupoids]].
 
  Write $[C^{op}, Grpd_{nat}]_{proj}$ for the projective [[model structure on functors]] on the [[functor category]] $[C^{op}, Grpd]$.

  Let $W = \{ S(\{U_i\})\to j(U) \}$ be the set of morphisms in $[C^{op}, Set] \hookrightarrow [C^{op}, Set]$ that are [[covering]] [[sieve]] inclusions with respect to the [[coverage]] on $C$.

  Then let finally $[C^{op}, Grpd_{folk}]_{proj,loc}$ be the [[Bousfield localization of model categories|left Bousfield localization]] at the set of morphisms $W$. This is a model for $(2,1)$-sheaves on $C$.


* Write $[C^{op}, sSet_{Quillen}]_{loc}$ for a local [[model structure on simplicial presheaves]] on $C$, the one which presents the [[(∞,1)-category of (∞,1)-sheaves]] on $C$.

  Let $W = \{\partial \Delta[n] \cdot U \to \Delta[n] \cdot U| n \geq 2 \in \mathbb{N}, U \in C\}$ be the class of generating morphisms of weak equivalences on [[homotopy n-type|homotopy 1-type]]s.

  Write $[C^{op}, sSet_{Quillen}]_{loc,W}$ for the [[Bousfield localization of model categories|left Bousfield localization]] of the model structure for [[(∞,1)-sheaves]] at the morphisms $W$. Then this is a model structure for $(2,1)$-sheaves on $C$.


The discussion in ([Hollander](#Hollander)) shows that the results of these two constructions are [[Quillen equivalence|Quillen equivalent]]. 

> Or essentially, I'll fill in details and make this precise once I have a second.


## Related concepts

* **model structure for $(2,1)$-sheaves**

* model structures for $(\infty,1)$-sheaves

  * [[model structure on simplicial presheaves]]

  * [[model structure on simplicial sheaves]]

## References

A model structure on presheaves of groupoids Quillen equivalent to the [[left Bousfield localization]] of the local [[model structure on simplicial presheaves|model structure for (∞,1)-sheaves]] at morphisms that are weak equivalences of [[homotopy n-type|homtopy 1-type]]s is in.

* [[Sharon Hollander]], _A homotopy theory for stacks_ ([arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247))
{#Hollander}

A discussion of $(2,1)$-sheaves/stacks as [[1-truncated]] objects in the full [[model structure on simplicial presheaves|model structure for (∞,1)-sheaves]] is in

* J. F. Jardine, _Stacks and the homotopy theory of simplicial sheaves_ ,  Homology Homotopy Appl. Volume 3, Number 2 (2001), 361-384. ([project euclid](http://projecteuclid.org/euclid.hha/1139840259))
{#Jardine}

[[!redirects (2,1)-sheaves]]
[[!redirects (2,1)-category of (2,1)-sheaves]]