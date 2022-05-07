
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

## Properties

### Quillen equivalence between simplicial groups and reduced simplicial sets

\begin{proposition}\label{QuillenEquivalenceBetweenSimplicialGroupsAndReducedSimplicialSets}
**([[Quillen equivalence between simplicial groups and reduced simplicial sets]])** \linebreak
  The [[simplicial classifying space]]-construction $\overline{W}(-)$ (Def. \ref{BarWGInComponents}) is the [[right adjoint]] in a [[Quillen equivalence]] between the projective [[model structure on simplicial groups]] and the injective [[model structure on reduced simplicial sets]]. 

$$
  Groups(sSet)_{proj}
  \underoverset
    {\underset{\overline{W}}{\longrightarrow}}
    {\overset{ \Omega }{\longleftarrow}}
    {\;\;\;\;\; \simeq_{\mathrlap{Qu}} \;\;\;\;\;}
  (sSet_{\geq 0})_{inj}
  \,.
$$

The [[left adjoint]] $\Omega$ is the [[simplicial loop space]]-construction. 
\end{proposition}

(e.g. [Goerss & Jardine 09, V Prop. 6.3](#GoerssJardine09))



## Related concepts

* [[simplicial delooping functor]]

## References

For a more complete list of references, see the article [[simplicial delooping functor]].

* {#Kan58} [[Daniel Kan]], _On homotopy theory and c.s.s. groups_, Ann. of Math. 68 (1958), 38-53 ([jstor:1970042](https://www.jstor.org/stable/1970042)) (Sections 10–11.)

* [[Peter May]], chapter VI of _Simplicial objects in algebraic topology_, Van Nostrand, Princeton (1967) ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu))

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.4 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))


More details and relation to [[décalage]]:

* [[Danny Stevenson]], _Décalage and Kan's simplicial loop group functor_, Theory and Applications of Categories, Vol. 26, 2012, No. 28, pp 768-787 ([arXiv:1112.0474](https://arxiv.org/abs/1112.0474), [tac:26-28](http://www.tac.mta.ca/tac/volumes/26/28/26-28abs.html))


[[!redirects simplicial loop spaces]]
[[!redirects simplicial loop group]]
[[!redirects simplicial loop groups]]
[[!redirects simplicial loop functor]]
[[!redirects simplicial loop functors]]
[[!redirects simplicial loop space functor]]
[[!redirects simplicial loop space functors]]