<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

Under the [[Dold–Kan correspondence]] there is an [[equivalence of categories]] relating non-negatively graded [[chain complex]]es in an [[abelian category]] $A$ to [[simplicial object]]s in $A$.

$$
  Ch_+(A) \simeq A^{\Delta^{op}}
  \,.
$$

At least if $A$ is the category of abelian groups, so that $A^{\Delta^{op}}$ is the category of abelian [[simplicial group]]s it inherits naturally a [[homotopical category|homotopical category]] from the [[model structure on simplicial sets]]. This is a very canonical model structure in that it is no less than the [[presentable (infinity,1)-category|presentation]] of the archetypical [[(infinity,1)-category]] [[Infinity-Grpd]] of [[infinity-groupoid]].

The model structure on chain complexes transports this presentation  of the special $\infty$--groupoids given by abelian simplicial groups along the Dold-Kan correspondence to chain complexes.

Analogous statements apply to the category of unbounded chain complexes and the canonical [[stable (infinity,1)-category]] [[Spec]] of [[spectrum|spectra]]. 

Spaltenstein wrote a famous paper 

* N. Spaltenstein, _Resoutions of unbounded complexes_, Compositio Mathematica, 65 no. 2 (1988), p. 121-154 ([numdam](http://www.numdam.org/item?id=CM_1988__65_2_121_0))

on how to do homological algebra with unbounded complexes (in both sides) where he introduced notions like K-projective and K-injective complexes. Later, 

* V. Hinich, _Homological algebra of homotopy algebras_, Comm. Algebra, vol. 25 (1997), no. 10, 3291-3323
([pdf at author's page](http://math.haifa.ac.il/hinich/WEB/mypapers/haha.pdf)) 

shown that there is a model category structure on the category of unbounded chain complexes, reproduced Spaltenstein's results from that perspective and extended them widely. See also

* J. D. Christensen, Derived categories and projective classes, 2005 ([hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Christensen/derived))

+-- { .query}
[[Zoran Škoda]]: It is misleading to put positive complexes in the center of this nlab entry, because this is just the easiest, cheapest part of the story. I do not think the results for positive, negative or bounded complexes were just easily generalized from unbounded as it is impression from the sentence above on "analogous results". Both Spaltenstein and Hinich wrote breakthrough papers over 20 years after Quillen's school understood the examples of one-side-unbounded and bounded cases. 

This Spaltenstein-Hinich story which I just mentioned with writing out the references, would thus be more essential to precisely cover (and will be more essentially used) than making the long story out of trivial resort to Dold-Kan argument, and modern lingo on (infty,1). 
=--


# History and references#

Of course the above description of categories of chain complexes as ([[presentable (infinity,1)-category|presentations]] of) special cases of (stable) $(\infty,1)$-categories is exactly opposite to the historical development of these ideas. 

While the homotopical treatment of weak equivalences of chain complexes ([[quasi-isomorphism]]s) in [[homological algebra]] is at the beginning of all studies of higher categories and a "folk theorem" ever since

* A. Joyal, Letter to Alexander Grothendieck. April 11, 1984

it seems that the injective model structure on chain complexes has been made fully explicit in print only in proposition 3.13 of

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math/0102087), [pdf](http://arxiv.org/PS_cache/math/pdf/0102/0102087v1.pdf))

(at least according to the remark below that).

The projective model structure is discussed after that in 

* Mark Hovey, _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. 353, 6 ([pdf](http://www.mathaware.org/tran/2001-353-06/S0002-9947-01-02721-0/S0002-9947-01-02721-0.pdf))