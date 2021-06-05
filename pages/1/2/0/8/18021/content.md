
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

In [[simplicial homotopy theory]] there is a standard construction ([Kan 58](#Kan58)), traditionally denoted $G$, for the simplicial analog of the [[homotopy type]] of the [[loop space]] $\Omega X$ of a [[connected topological space]], now incarnated as a [[simplicial group]]: It is the [[left adjoint]] in an [[adjunction]]
$$
  (G \dashv \overline{W}) 
    \;\colon\;
  sSet_*
    \underoverset
      {\underset{\overline{W}}{\longleftarrow}}
      {\overset{G}{\longrightarrow}}
      {\bot}
  sGrp
$$

between [[pointed simplicial sets]] and [[simplicial groups]], whose [[right adjoint]] is the [[simplicial classifying space]] construction.

This adjunction is a [[Quillen adjunction]] for the [[Kan–Quillen model structure]] on [[pointed simplicial sets]] and its [[transferred model structure]] on [[simplicial groups]].

When restricted to [[reduced simplicial sets]], this [[Quillen adjunction]] becomes a [[Quillen equivalence]].

The generalization of this construction to non-reduced simplicial sets and [[simplicial groupoids]] is the [[Dwyer-Kan loop groupoid]] functor.

## Related concepts

* [[simplicial delooping functor]]

## References

For a more complete list of references, see the article [[simplicial delooping functor]].

* {#Kan58} [[Daniel Kan]], _On homotopy theory and c.s.s. groups_, Ann. of Math. 68 (1958), 38-53 ([jstor:1970042](https://www.jstor.org/stable/1970042)) (Sections 10–11.)

* [[Peter May]], chapter VI of _Simplicial objects in algebraic topology_, Van Nostrand, Princeton (1967) ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu))

More details and relation to [[décalage]]:

* [[Danny Stevenson]], _Décalage and Kan's simplicial loop group functor_, Theory and Applications of Categories, Vol. 26, 2012, No. 28, pp 768-787 ([arXiv:1112.0474](https://arxiv.org/abs/1112.0474), [tac:26-28](http://www.tac.mta.ca/tac/volumes/26/28/26-28abs.html))


[[!redirects simplicial loop spaces]]
[[!redirects simplicial loop group]]
[[!redirects simplicial loop groups]]
[[!redirects simplicial loop functor]]
[[!redirects simplicial loop functors]]
[[!redirects simplicial loop space functor]]
[[!redirects simplicial loop space functors]]