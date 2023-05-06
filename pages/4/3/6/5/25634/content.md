
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categories of categories
+--{: .hide}
[[!include categories of categories - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

There are several versions of a ([[very large category|very large]]) [[2-category]] of [[model categories]], depending on which notion of [[transformation of adjoints]] one takes to be the [[2-morphisms]] between [[1-morphisms]] given by [[Quillen functors]].

One choice is to consider [[2-morphisms]] to be [[conjugate transformations of adjoints]] between [[Quillen adjunctions]] &lbrack;[Hovey (1999), p. 24](#Hovey99), cf. also [Harpaz & Prasma (2015), Def. 2.5.3](#HarpazPrasma15)&rbrack;, such that forgetting the [[model category]]-[[structure]] is a [[forgetful functor|forgetful]] [[2-functor]] to [[CatAdj|$Cat_{Adj}$]]:
$$
  ModCat \longrightarrow Cat_{Adj} \longrightarrow Cat
  \,.
$$
[Therefore](CatAdj#RelationToBifibrations) a [[pseudofunctor]] $\mathcal{B} \longrightarrow Cat$ which factors through $ModCat$ this way has as [[Grothendieck construction]] a [[bifibration]] of [[model categories]]. Under good conditions, the [[domain]] of this bifibration carries itself an induced [[model category structure]], see at *[[model structure on Grothendieck constructions]]*.


## Related concepts

* [[double category of model categories]]

* [[Ho(CombModCat)]]

* [[Grothendieck construction for model categories]]


## References

The [[2-category]] of [[model categories]], left-pointing [[Quillen adjunctions]] and [[conjugate transformations of adjoints]] is considered in:

* {#Hovey99} [[Mark Hovey]], p. 24 of: *[[Model Categories]]*, Mathematical Surveys and Monographs, **63** AMS (1999) &lbrack;[ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover)&rbrack;


* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], Def. 2.5.3 in: _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

[[!redirects 2-category of model categories]]