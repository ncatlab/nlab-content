
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categories of categories
+--{: .hide}
[[!include categories of categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

There are different versions of what one may mean by a [[2-category]] of [[categories]] with [[adjoint functors]] as [[1-morphisms]], namely depending on which notion of [[transformation of adjoints]] one considers.

For example, the ([[very large category|very large]]) [[wide subcategory|wide]] [[locally full sub-2-category]] of [[Cat]]
\[
  \label{CatAdjInsideCat}
  Cat_{Adj} \longrightarrow Cat
\]
whose 

* [[objects]] are categories,

* [[1-morphisms]] are [[left adjoint]] [[functors]]

* [[2-morphisms]] are [[natural transformations]] which are [[conjugate transformations of adjoints]].

## Properties

### Relation to bifibrations
 {#RelationToBifibrations}

\begin{proposition}
  Under the [[Grothendieck construction]], the [[Grothendieck fibrations]] which arise from [[pseudofunctors]] $\mathcal{B} \longrightarrow Cat$ that factor through $Cat_{Adj}$ (eq:CatAdjInsideCat) are equivalently the [[bifibrations]].
\end{proposition}
\begin{proof}
Notice, by [this Prop.](transformation+of+adjoints#UniqueConjugateMate), that such a factorization exists (and then essentially uniquely) iff the component functors of the given [[pseudofunctor]] all have an [[adjoint functor|adjoint]] (on the appropriate side).
Hence it now suffices to show that a Grothendieck fibration is a bifibration iff all its base change functors have an adjoint on the appropriate side. 
This may be [[category theory]] [[folklore]]; one place where this proof is spelled out is [Jacobs (1998), Lem. 9.1.2](bifibration#Jacobs98), see also [Harpaz & Prasma (2015), Prop. 2.2.1](#HarpazPrasma15).\end{proof}

## Related concepts

* [[2-category of adjunctions]]

* [[ModCat|2-category of model categories]]

* [[bifibration]]

* [[adjoint (infinity,1)-functor#category_of_adjunctions|
∞-category of adjunctions]]

## References

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], Section 2.2. of: _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

  > (in the context of [[model structures on Grothendieck constructions]])
