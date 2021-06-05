
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[simplicial group]], there is a [[reduced simplicial set|reduced]] [[simplicial set]], traditionally denoted $\overline W G$ and called the *[[classifying space]]* or *classifying complex* of $G$, which is a model for the [[delooping]] of $G$ and such that the [[functor]] $\overline{W}(-)$ is [[right adjoint]] to the standard [[simplicial loop space]]-construction $L$. 

This pair of [[adjoint functors]] 
$$
  SimplicialGroups
    \underoverset
      {\;\;\;\underset{\overline{W}}{\longrightarrow}\;\;\;}
      {\;\;\;\overset{L}{\longleftarrow}\;\;\;}
      {\bot}
  SimplicialSets_{red}
$$
is a [[Quillen equivalence]] between the [[model structure on simplicial groups]] and the [[model structure on reduced simplicial sets]], modelling [[looping and delooping]] of [[homotopy types]] in [[simplicial homotopy theory]].

## Related concepts

* [[simplicial homotopy theory]]

* [[Borel model structure]]


## References

The functor $\overline W$ is essentially due to:

* {#MacLane54} [[Saunders MacLane]], *Constructions simpliciales acycliques*, Colloque Henri Poincar&eacute; 1954 ([[MacLaneConstructionsSimplicialesAcycliques.pdf:file]])

* {#EilenbergMacLane53I} [[Samuel Eilenberg]], [[Saunders Mac Lane]], _On the Groups $H(\Pi,n)$, I_, Annals of Mathematics Second Series, Vol. 58, No. 1 (Jul., 1953), pp. 55-106 ([jstor:1969820](https://www.jstor.org/stable/1969820)) 

The functor $L$ (denoted there by $G$) was introduced by [[Kan]] in §7 of

* [[Daniel M. Kan]], _A combinatorial definition of homotopy groups_, Annals of Mathematics 67:2 (1958), 282–312.  [doi](https://doi.org/10.2307/1970006).

As part of a [[Quillen equivalence]]:

* {#Kan58} [[Daniel Kan]], Sections 10-11 in: _On homotopy theory and c.s.s. groups_, Ann. of Math. 68 (1958), 38-53 ([jstor:1970042](https://www.jstor.org/stable/1970042))

* {#Quillen69} [[Dan Quillen]], Section 2 of: _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](http://www.jstor.org/stable/1970725))

Textbook accounts:

* [[Peter May]], p. 87-88 in: _Simplicial objects in algebraic topology_, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])


* [[Paul Goerss]], [[J. F. Jardine]], Section V.4 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

Streamlining:

* [[Danny Stevenson]], around Lemma 15 of: *Décalage and Kan's simplicial loop group functor*, Theory and Applications of Categories, Vol. 26, 2012, No. 28, pp 768-787 ([arXiv:1112.0474](https://arxiv.org/abs/1112.0474), [tac:26-28](http://www.tac.mta.ca/tac/volumes/26/28/26-28abs.html))

Generalization to [[simplicial presheaves]]:

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Section 3.5 of: _Principal $\infty$-bundles -- _Presentations_, Journal of Homotopy and Related Structures, Volume 10, Issue 3 (2015), pages 565-622 ([doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4), [arXiv:1207.0249](http://arxiv.org/abs/1207.0249))

[[!redirects simplicial classifying spaces]]

[[!redirects simplicial classifying complex]]
[[!redirects simplicial classifying complexes]]

[[!redirects simplicial delooping]]
[[!redirects simplicial deloopings]]

