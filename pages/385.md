The _Crans-Gray tensor product_ is a [[tensor product]] on the category of [[strict omega-category|strict omega-categories]] which reduces to the (lax version of the) [[Gray tensor product]] when restricted to [[strict 2-category|strict 2-categories]]. It provides the category of [[strict omega-category|strict omega-categories]] with a [[closed monoidal category|biclosed monoidal structure]] whose internal hom-objects are strict $\omega$-categories of _strict_ functors, _lax_ natural transformations between these, lax modifications between these, and so on.

+--{: .query}
[[Mike Shulman|Mike]]: Is it really true that the Crans-Gray tensor product reduces to the (lax) Gray tensor product when applied to 2-categories?  It seems to me that if the "lax transformations" involved are lax in all dimensions, which the informal discussion below suggests that they are, then the Crans-Gray tensor product of two 2-categories will not, in general, even be a 2-category any more.  Then the most you could expect is that the reflection from strict $\omega$-categories to strict 2-categories would take the Crans-Gray tensor product to the Gray tensor product.
=--

The Crans-Gray tensor product can be understood as arising as follows:

There is an obvious [[monoidal category|monoidal structure]] on the [[cube category]] obtained from the obvious product of cellular [[geometric shapes for higher structures|cubes]] which is analogous to the cartesian product of the topological cubes $[0,1]^n$. By [[Day convolution]] this naturally indces a [[monoidal category|monoidal structure]] on [[cubical set|cubical sets]]. Strict $\omega$-categories, being [[globular set|globular sets]] with extra structure, can also be regarded as [[cubical set|cubical sets]] with extra structure and extra property. The Crans-Gray tensor product thus extends the tensor product on cubical sets to $\omega$-categories.

#Remarks#

 The Crans-Gray tensor product extends the tensor product  on strict $\omega$-groupoids given by R. Brown and P.J. Higgins (see below); they construct a symmetric monoidal closed structure on these $\omega$-groupoids. 

The third  paper below sets up an equivalence between globular $\omega$-categories and certain cubical $\omega$-categories with connections, to which the monoidal closed structure in the previous paper is easily extended. 

#References#

A detailed discussion is in

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([ftp, gzipped PostScript](ftp://ftp.math.mcgill.ca/pub/crans/thten.ps.gz))

* R. Brown and P.J. Higgins, Tensor products and homotopies for $\omega$-groupoids and crossed complexes,  J. Pure Appl. Alg. 47 (1987) 1-33.

* F.A. Al-Agl, R. Brown and R. Steiner,  Multiple categories: the equivalence between a globular and cubical approach, Advances in Mathematics, 170 (2002) 71-118.

