The _Crans-Gray tensor product_ is a [[tensor product]] on the category of [[strict omega-category|strict omega-categories]] which reduces to the (lax version of the) [[Gray tensor product]] when restricted to [[strict 2-category|strict 2-categories]]. It provides the category of [[strict omega-category|strict omega-categories]] with a [[closed monoidal category|biclosed monoidal structure]] whose internal hom-objects are strict $\omega$-categories of _strict_ functors, _lax_ natural transformations between these, lax modifications between these, and so on.

+--{: .query}
[[Mike Shulman|Mike]]: Is it really true that the Crans-Gray tensor product reduces to the (lax) Gray tensor product when applied to 2-categories?  It seems to me that if the "lax transformations" involved are lax in all dimensions, which the informal discussion below suggests that they are, then the Crans-Gray tensor product of two 2-categories will not, in general, even be a 2-category any more.  Then the most you could expect is that the reflection from strict $\omega$-categories to strict 2-categories would take the Crans-Gray tensor product to the Gray tensor product.

[[Ronnie Brown|Ronnie]]: The tensor product of strict globular 2-categories is really a strict globular 4-category. However there is a _cotruncation_ from dimension $n$ to lower dimension $m$ which at dimension $m$ imposes some additional relations. I know how to write this down in the crossed complex case but am not so sure in the globular and category case. 

It also seems that the monoidal closed structure on strict globular omega categories in the third paper below gives "higher order lax transformations". What else?  In the crossed complesx case, you get higher order left homotopies. 

[[Urs Schreiber|Urs]]: I had a vague recollection that Sjoerd Crans gives a detailed discussion of this somewhere, but now that I looked again as his stuff all I seem to be able to find is the remark on [pp. 14 (3 of 60)](http://www.tac.mta.ca/tac/volumes/1999/n2/n2.pdf#page=3)
of 

Sjoerd Crans, _A tensor product for $Gray$-categories_ ([tac](http://www.tac.mta.ca/tac/volumes/1999/n2/5-02abs.html))

_Mike_: Is the "cotruncation" what I would call the "reflection into $m$-categories"?

I don't see a relevant remark on p. 14 of that paper, but on p. 41 he says:

> If the $Gray$-categories $C$ and $D$ are both 2-categories, then their tensor product _as 2-categories_ is precisely the 2-category obtained from _the $Gray$-category $C \otimes D$_ by formally turning all its 3-arrows into identities.  In other words, Gray's tensor product is the 2-categorical reflection of the tensor product of $Gray$-categories given here.

I think this supports what I was saying, although the relationship between the tensor product of $Gray$-categories and the tensor product of strict $\omega$-categories is also an important question.  One might guess that on the intersection of their domains (namely, strict 3-categories) the former is the reflection of the latter into 3-categories, although it's not even obvious to me that the tensor product _qua_ $Gray$-categories of two strict 3-categories is again a strict 3-category.

=--

+--{: .query}

[[Urs Schreiber|Urs]]: Another question:

Does the $\omega$-nerve intertwine the Gray tensor product on $\omega$-categories with the cartesian product on simplicial sets?

$$
  N(C \otimes D) \simeq N(C)\times N(D)
  \;\;\;
  ??
$$

[[Mike Shulman|Mike]]: No.  Consider $C=D=\mathbf{2}$, the walking arrow $(0 \overset{f}{\to} 1)$.  Then $N C \times N D$ is a square
$$\array{(0,0) & \overset{(f,0)}{\to} & (1,0)\\
^{(0,f)}\downarrow & \searrow^{(f,f)} & \downarrow^{(1,f)}\\
(0,1) & \underset{(f,1)}{\to} & (1,1)}$$
in which both triangles contain a 2-simplex.  I don't think this is isomorphic to the nerve of any $\omega$-category, but it certainly isn't equivalent to the nerve of $C\otimes D$, since the latter only contains a 2-cell from $(1,f)(f,0)$ to $(f,1)(0,f)$.

On the other hand, I do believe that the "pseudo" version of the tensor product on $\omega$-categories (has this been written down?) gets intertwined, at least up to equivalence, with the cartesian product of _stratified_ simplicial sets.  Possibly something about this could be found in Verity's work on [[weak complicial set]]s.

[[Urs Schreiber|Urs]]: Right, thanks. It should be the pseudo version. Or else, I should have asked whether the $\omega$-nerve on strict $\omega$-groupoids intertwines the Brown-Gray tensor product with the cartesian product of Kan complexes. That should be true, right?

[[Mike Shulman|Mike]]: Seems likely.

=--



The Crans-Gray tensor product can be understood as arising as follows:

There is an obvious [[monoidal category|monoidal structure]] on the [[cube category]] obtained from the obvious product of cellular [[geometric shapes for higher structures|cubes]] which is analogous to the cartesian product of the topological cubes $[0,1]^n$. By [[Day convolution]] this naturally indces a [[monoidal category|monoidal structure]] on [[cubical set|cubical sets]]. Strict $\omega$-categories, being [[globular set|globular sets]] with extra structure, can also be regarded as [[cubical set|cubical sets]] with extra structure and extra property. The Crans-Gray tensor product thus extends the tensor product on cubical sets to $\omega$-categories.

#Remarks#

* The Crans-Gray tensor product extends the tensor product  on strict $\omega$-groupoids given by R. Brown and P.J. Higgins (see below); they construct a symmetric monoidal closed structure on these $\omega$-groupoids. 

* The article _BrHi_ below sets up an equivalence between globular $\omega$-categories and certain cubical $\omega$-categories with connections, to which the monoidal closed structure in the previous paper is easily extended. 

* There is the [[Verity-Gray tensor product]] on [[stratified simplicial set]]s (as described there). Via the [[oriental|omega-nerve]] [[strict omega-category|strict omega-categories]] form the [[complicial set]]s within all [[stratified simplicial set]]s. According to observation 60 of [Verity06](http://arxiv.org/abs/math/0604414) section 11.4 of [Verity04](http://arxiv.org/abs/math/0410412) proves that the Crans-Gray tensor product is the reflection of the Verity-Gray tensor product under this inclusion.
 
#References#

A detailed discussion is in

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([ftp, gzipped PostScript](ftp://ftp.math.mcgill.ca/pub/crans/thten.ps.gz))

* **BrHi** R. Brown and P.J. Higgins, Tensor products and homotopies for $\omega$-groupoids and crossed complexes,  J. Pure Appl. Alg. 47 (1987) 1--33.

* F.A. Al-Agl, R. Brown and R. Steiner,  Multiple categories: the equivalence between a globular and cubical approach, Advances in Mathematics, 170 (2002) 71--118.

Some helpful remarks and diagrams are in 

* Sjoerd Crans, _A tensor product for $Gray$-categories_ ([tac](http://www.tac.mta.ca/tac/volumes/1999/n2/5-02abs.html))

which is however mainly concerned with a slightly different topic.