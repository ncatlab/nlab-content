
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##


For $V$ a sufficiently nice ([[monoidal model category|monoidal]]) [[model category]] and $C$ a [[small category]] equipped with a [[Grothendieck topology]] $\tau$, there are left [[Bousfield localization]]s of the [[global model structure on functors]] $[C^{op}, V]$ whose fibrant objects satisfy [[descent]] with respect to [[Čech cover]]s or even [[hypercover]]s with respect to $\tau$. 

These model structures are expected to model $V$-valued [[∞-stack]]s on $C$. This is well understood for the case $V = $ [[SSet]] equipped with the standard [[model structure on simplicial sets]] modelling [[∞-groupoid]]s. In this case the resulting [[local model structure on simplicial presheaves]] is known to be one of the  [[models for ∞-stack (∞,1)-toposes]].

But the general localization procedure works for choices of $V$ different from and more general than [[SSet]] with its standard model structure. In particular it should work for 

* $V = $ [[SSet]] equipped with its [[model structure on simplicial sets|Joyal model structure]], modelling [[(∞,1)-category|(∞,1)-categories]]

* $V = (n,r)\Theta Spaces$, the model structure on [[Theta space]]s modelling weak [[(n,r)-category|(n,r)-categories]];

* $V = dSet$, the [[model structure on dendroidal sets]] modelling [[(∞,1)-operad]]s.

For these cases the local model structure on $V$-valued presheaves should model, respectively, $(n,r)$-category valued sheaves/stacks and $(\infty,1)$-operad valued sheaves/stacks.

## References ##

The general localization result is apparently due to

* [[Clark Barwick]], _On left and right model categories and left and right Bousfield localization_ Homology, Homotopy and Applications, vol. 12(2), 2010, pp.245&#8211;320 ([pdf](http://www.intlpress.com/HHA/v12/n2/a9/v12n2a9.pdf))

which considers the [[Čech cover]]-localization assuming $V$ to be [[monoidal category|monoidal]] and

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique_ ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF)) 

which apparently does the [[hypercover]] [[descent]] and without assuming $V$ to be monoidal.

Much of this was kindly pointed out by [[Denis-Charles Cisinski]] in discussion [here](http://mathoverflow.net/questions/5808/local-joyal-simplicial-presheaves).

## Related concepts

* [[enriched Reedy category]]

* [[model structure on sSet-presheaves]]

[[!redirects model structures on homotopical presheaves]]