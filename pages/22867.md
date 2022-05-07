

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
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

The [[Dold-Kan correspondence]] between [[connective chain complexes]] and [[simplicial abelian groups]] is not quite compatible with the [[tensor product]]-structure on both sides, but it is so up to [[homotopy]] (see at *[[monoidal Dold-Kan correspondence]]*). One aspect of this is the *[[Eilenberg-Zilber theorem]]*, saying that the [[Eilenberg-Zilber map]] from the [[tensor product of chain complexes]] of [[normalized chain complexes]] of two [[abelian groups]] to the normalized chain complex of their degree-wise [[tensor product of abelian groups]] is not quite an [[isomorphism]], but is a [[homotopy equivalence]], in fact a [[deformation retraction]], with homotopy-inverse the [[Alexander-Whitney map]]. 

## Statement

\begin{proposition}\label{EZAWDeformationRetract}
**([[Eilenberg-Zilber map|Eilenberg-Zilber]]/[[Alexander-Whitney map|Alexander-Whitney]] [[deformation retraction]])** \linebreak

Let 

* $A, B \,\in\, sAb = $ [[SimplicialAbelianGroups]]

and denote 

* by $N(A), N(B) \,\in\, Ch^+_\bullet = $ [[ConnectiveChainComplexes]] their [[normalized chain complexes]], 

* by $A \otimes B \,\in\, sAb$ the degreewise [[tensor product of abelian groups]],

* by $N(A) \otimes N(B)$ the [[tensor product of chain complexes]].

Then there is a [[deformation retraction]]

\begin{tikzcd}
  N(A) \otimes N(B)
  \ar[
    rr,
    bend right=20,
    "\mathrm{id}"{below},
    "\ "{above, name=t}
  ]
  \ar[
    rr,
    phantom,
    "\ "{name=s, yshift=-6pt}
  ]
  \ar[
    r,
    "\nabla_{A,B}"
  ]
  &
  N( A \otimes B )
  \ar[
    r,
    "\Delta_{A,B}"
  ]
  &
  N(A) \otimes N(B)
  \ar[
    from=s,
    to=t,
    -,
   shift left=1pt
  ]
  \ar[
    from=s,
    to=t,
    -,
   shift right=1pt
  ]
\end{tikzcd}

\begin{tikzcd}
  N( A \otimes B )
  \ar[
    rr,
    bend right=20,
    "\mathrm{id}"{below},
    "\ "{above, name=t}
  ]
  \ar[
    rr,
    phantom,
    "\ "{name=s, yshift=-6pt}
  ]
  \ar[
    r,
    "\Delta_{A,B}"
  ]
  &
  N(A) \otimes N(B)
  \ar[
    r,
    "\nabla_{A,B}"
  ]
  &
  N( A \otimes B )
  \ar[
    from=s,
    to=t,
    Rightarrow
  ]
\end{tikzcd}

where 

* $\nabla_{A,B}$ is the [[Eilenberg-Zilber map]];

* $\Delta_{A,B}$ is the [[Alexander-Whitney map]].

\end{proposition}

For unnormalized chain complexes, where we have a [[homotopy equivalence]], this is the original [[Eilenberg-Zilber theorem]] ([Eilenberg & Zilber 1953](#EilenbergZilber53), [Eilenberg & MacLane 1954, Thm. 2.1](#EilenbergMacLane54)), review in [MacLane 1975, VIII 8](#MacLane75), [Dold 1995, VI 12.1](#Dold95). The above [[deformation retraction]] for normalized chain complexes is [Eilenberg & MacLane 1954, Thm. 2.1a](#EilenbergMacLane54). Both are reviewed in [May 1967, Cor. 29.10](#May67), the latter at least mentioned in [MacLane 1975, VIII Cor. 8.9](#MacLane75). Explicit description of the [[homotopy operator]] is given in [Gonzalez-Diaz & Real 1999](#GonzalezDiazReal99).


## Related concepts

* **Alexander-Whitney map**

* [[Eilenberg-Zilber map]]

## References

The [[Eilenberg-Zilber theorem]] is due to

* {#EilenbergZilber53} [[Samuel Eilenberg]], [[Joseph Zilber]], _On Products of Complexes_, Amer. Jour. Math. 75 (1): 200&#8211;204, (1953) ([jstor:2372629](https://www.jstor.org/stable/2372629))

* {#EilenbergMacLane54} [[Samuel Eilenberg]], [[Saunders MacLane]], Section 2 of: *On the Groups $H(\Pi,n)$, II: Methods of Computation*, Annals of Mathematics, Second Series, Vol. 60, No. 1 (Jul., 1954), pp. 49-139 ([jstor:1969702](https://www.jstor.org/stable/1969702), [doi:10.2307/2372629](https://doi.org/10.2307/2372629))

using the definition of the [[Eilenberg-Zilber map]] in:

* {#EilenbergMacLane53} [[Samuel Eilenberg]], [[Saunders MacLane]], (5.3) of: *On the groups $H(\Pi,n)$*, I*, Ann. of Math. (2) 58, (1953), 55&#8211;106. ([jstor:1969820](https://www.jstor.org/stable/1969820))

Review and further discussion:

* {#May67} [[Peter May]], Section 29 of: _Simplicial objects in algebraic topology_ , Chicago Lectures in Mathematics, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])

* {#MacLane75} [[Saunders Mac Lane]], _Homology_ (1975) reprinted as Classics in Mathematics. Springer-Verlag, Berlin, 1995. x+422 pp. ISBN 3-540-58662-8 ([doi:10.1007/978-3-642-62029-4](https://link.springer.com/book/10.1007/978-3-642-62029-4))

* {#Dold95} [[Albrecht Dold]], Section VI 12.1 in *Lectures on Algebraic Topology*, Springer 1995 ([doi:10.1007/978-3-642-67821-9](https://www.springer.com/gp/book/9783540586609), [pdf](https://link.springer.com/content/pdf/bfm%3A978-3-642-67821-9%2F1.pdf))


* {#GonzalezDiazReal99} [[Rocio Gonzalez-Diaz]], [[Pedro Real]], *A Combinatorial Method for Computing Steenrod Squares*, Journal of Pure and Applied Algebra 139 (1999) 89-108 ([arXiv:math/0110308](https://arxiv.org/abs/math/0110308))


[[!redirects EZAW deformation retraction]]
