
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

* [[1-morphisms]] are [[left adjoint]] [[functors]],

* [[2-morphisms]] are [[natural transformations]] which are [[conjugate transformations of adjoints]].

&lbrack;[MacLane (1971), p. 103](#MacLane71)&rbrack;

## Properties

### Relation to bifibrations
 {#RelationToBifibrations}

\begin{proposition}
  Under the [[Grothendieck construction]], the [[Grothendieck fibrations]] which arise from [[pseudofunctors]] $\mathcal{B} \longrightarrow Cat$ that factor through $Cat_{Adj}$ (eq:CatAdjInsideCat) are equivalently the [[bifibrations]].
\end{proposition}
\begin{proof}
A Grothendieck construction on a pseudofunctor yielding a bifibration is fairly immediately equivalent to all base change functors having an adjoint on the respective side (e.g. [Jacobs (1998), Lem. 9.1.2](bifibration#Jacobs98)). By the fact that $Cat_{adj} \to Cat$ is a [[locally full sub-2-category]] ([this Prop.](transformation+of+adjoints#UniqueConjugateMate)) this already means that the given pseudofunctor factors through  $Cat_adj$, and essentially uniquely so.
\end{proof}
See also [Harpaz & Prasma (2015), Prop. 2.2.1](#HarpazPrasma15).

## Related concepts

* [[2-category of adjunctions]]

* [[ModCat|2-category of model categories]]

* [[bifibration]]

* [[adjoint (infinity,1)-functor#category_of_adjunctions|
∞-category of adjunctions]]

## References

* {#MacLane71} [[Saunders MacLane]], p. 102 of: _[[Categories Work|Categories for the working mathematician]]_, Graduate Text in Mathematics, Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

See also:

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], Section 2.2. of: _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

  > (in the context of [[model structures on Grothendieck constructions]])
