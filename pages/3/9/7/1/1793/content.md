
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

Model structures on chain complexes are [[model category]] structures on [[categories of chain complexes]] whose weak equivalences are [[quasi-isomorphism]]s. 

Via these model structures, all of the standard techniques in [[homological algebra]], such as injective and projective resolutions, are special cases of constructions in [[homotopy theory]], such as cofibrant and fibrant [[resolution]]s.

The existence of these model structures depends subtly on whether the chain complexes in question are bounded or not. 

### In non-negative degree

Chain complexes in non-negative degree in an [[abelian category]] $A$ are special in that they may be identified via the [[Dold?Kan correspondence]] as [[simplicial object]]s in $A$.

$$
  Ch_+(A) \simeq A^{\Delta^{op}}
  \,.
$$

At least if $A$ is the category of [[abelian groups]], so that $A^{\Delta^{op}}$ is the category of abelian [[simplicial group]]s it inherits naturally a model category structure from the [[model structure on simplicial sets]], which [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[∞-groupoid]]s.

The model structure on chain complexes transports this presentation  of the special $\infty$-groupoids given by abelian simplicial groups along the Dold-Kan correspondence to chain complexes.

Analogous statements apply to the category of unbounded chain complexes and the canonical [[stable (infinity,1)-category]] [[Spec]] of [[spectrum|spectra]]. 

### For unbounded chain complexes

See the references by Spaltenstein and Hinich below



## History and references

Of course the above description of categories of chain complexes as ([[presentable (infinity,1)-category|presentations]] of) special cases of (stable) $(\infty,1)$-categories is exactly opposite to the historical development of these ideas. 

While the homotopical treatment of weak equivalences of chain complexes ([[quasi-isomorphism]]s) in [[homological algebra]] is at the beginning of all studies of higher categories and a "folk theorem" ever since

* [[Andre Joyal]], Letter to Alexander Grothendieck. April 11, 1984

it seems that the injective model structure on chain complexes has been made fully explicit in print only in proposition 3.13 of

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math/0102087), [pdf](http://arxiv.org/PS_cache/math/pdf/0102/0102087v1.pdf))

(at least according to the remark below that).

The projective model structure is discussed after that in 

* [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. 353, 6 ([pdf](http://www.mathaware.org/tran/2001-353-06/S0002-9947-01-02721-0/S0002-9947-01-02721-0.pdf))


Variant model structures on chain complexes are discussed in

* [[Dan Christensen]], [[Mark Hovey]], _Quillen model structures for relative homological algebra_ ([pdf](http://jdc.math.uwo.ca/papers/relative.pdf))

Work specifically on model structures on unbounded complexes includes the following.

Spaltenstein wrote a famous paper 

* N. Spaltenstein, _Resoutions of unbounded complexes_, Compositio Mathematica, 65 no. 2 (1988), p. 121-154 ([numdam](http://www.numdam.org/item?id=CM_1988__65_2_121_0))

on how to do homological algebra with unbounded complexes (in both sides) where he introduced notions like K-projective and K-injective complexes. Later, 

* V. Hinich, _Homological algebra of homotopy algebras_, Comm. Algebra, vol. 25 (1997), no. 10, 3291-3323
([pdf at author's page](http://math.haifa.ac.il/hinich/WEB/mypapers/haha.pdf)) 

shown that there is a model category structure on the category of unbounded chain complexes, reproduced Spaltenstein's results from that perspective and extended them widely. See also

* J. D. Christensen, Derived categories and projective classes, 2005 ([hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Christensen/derived))


[[!redirects model structures on chain complexes]]