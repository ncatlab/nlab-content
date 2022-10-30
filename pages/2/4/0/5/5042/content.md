
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
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

The [[model category]] structure on the category $dgLie_k$ of [[dg-Lie algebra]]s over a commutative [[ring]] $k \supset \mathbb{Q}$ has

* [[fibrations]] the [[surjective maps]]

* [[weak equivalences]] the [[quasi-isomorphisms]] on the underlying [[chain complexes]].

This is a [[simplicial model category]] with respect to the [[sSet]]-[[hom functor]]

$$
  dgLie(\mathfrak{g}, \mathfrak{h})
  :=
  ([k] \mapsto Hom_{dgLie}(\mathfrak{g} , \Omega^\bullet(\Delta^k) \otimes\mathfrak{h}))
  \,,
$$

where 

* $\Omega^\bullet(\Delta^k)$ is the [[dg-algebra]] of [[polynomial differential forms]] on the $k$-[[simplex]];

* $\Omega^\bullet(\Delta^k)\otimes \mathfrak{h}$ is the canonical dg-Lie algebra structure on the [[tensor product]].

## Properties
 {#Properties}

### Rectification resolution for $L_\infty$-algebras
 {#RectificationResolution}

dg-Lie algebras with this model structure are a _rectification_ of [[L-∞ algebras]]: for $Lie$ the [[Lie operad]] and $\widehat Lie$ its standard [[cofibrant resolution]], [[algebras over an operad]] over $Lie$ in chain complexes are [[dg-Lie algebras]] and algebras over $\widehat Lie$ are [[L-∞ algebras]] and by the rectification result discussed at _[[model structure on dg-algebras over an operad]]_ there is an induced [[Quillen equivalence]]

$$
  Alg(\widehat Lie) \stackrel{\simeq}{\to} Alg(Lie)
$$

between the [[model structure for L-∞ algebras]] which is [[transferred model structure|transferred]] from the  [[model structure on chain complexes]] (unbounded propjective) to the above model structure on chain complexes.

There is also a [[Quillen equivalence]] from the model structure on dg-Lie algebras to the [[model structure on dg-coalgebras]]. This is part of a web of Quillen equivalences that identifies dg-Lie algebra/$L_\infty$-algebras with [[infinitesimal object|infinitesimal]] [[derived stack|derived]] [[∞-stacks]] ("[[formal moduli problems]]"). More on this is at _[[model structure for L-∞ algebras]]_.

Specifically, there is ([Quillen 69](#Quillen)) an [[adjunction]]

$$
  (\mathcal{R} \dashv i) \;\colon\;
  dgLie \stackrel{\overset{\mathcal{R}}{\leftarrow}}{\underset{i}{\to}} dgCoCAlg 
$$

between [[dg-coalgebras]] and dg-Lie algebras, where the [[right adjoint]] is the (non-full) inclusion that regards a dg-Lie algebra as a [[differential graded coalgebra]] with co-binary differential, and where the [[left adjoint]] $\mathcal{R}$ ("rectification") sends a dg-coalgebra to a dg-Lie algebra whose underlying graded [[Lie algebra]] is the [[free Lie algebra]] on the underlying [[chain complex]]. Over a [[field]] of [[characteristic]] 0, this adjunction is a [[Quillen equivalence]] between the [[model structure for L-∞ algebras]] on $dgCoCAlg$ and the model structure on $dgLie$ ([Hinich 98, theorem 3.2](#Hinich98)).

In particular, therefore the composite $i \circ \mathcal{R}$ is a [[resolution]] functor for $L_\infty$-algebras.

## Related concepts

* [[model structure on dg-coalgebras]]

* [[model structure on simplicial Lie algebras]]

* [[model structure for L-∞ algebras]]

## References

The model structure on dg-Lie algebras goes back to appendix B of

* [[Dan Quillen]], _Rational homotopy theory_ , Annals of Math., 90(1969), 205&#8211;295.
 {#Quillen69}

For more discussion see

* [[Vladimir Hinich]], _Homological algebra of homotopy algebras_ , Comm. in algebra, 25(10)(1997), 3291&#8211;3323.

* [[Vladimir Hinich]], _DG coalgebras as formal stacks_ ([arXiv:math/9812034](http://arxiv.org/abs/math/9812034))
 {#Hinich98}

and section 2.1 of 

* [[Jacob Lurie]], _[[Formal moduli problems]]_

Review with discussion of [[homotopy limits]] and [[homotopy colimits]] is in 

* {#Walter06} [[Ben Walter]], section 4 of _Rational Homotopy Calculus of Functors_ ([arXiv:math/0603336](http://arxiv.org/abs/math/0603336))


