
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $C : sAb \to Ch_\bullet^+$ be the chains/[[Moore complex]] functor of the [[Dold-Kan correspondence]].

Let $(sAb, \otimes)$ be the standard [[monoidal category]] structure given degreewise by the [[tensor product]] on [[Ab]] and let $(Ch_\bullet^+, \otimes)$ be the standard monoidal structure on the [[category of chain complexes]].


+-- {: .un_defn}
###### Definition

For $A,B \in sAb$ two abelian [[simplicial group]]s, the **Alexander-Whitney map** is the [[natural transformation]] on [[chain complex]]es

$$
  \Delta_{A,B} :  C(A \otimes B) \to C(A) \otimes C(B)
$$

defined on two $n$-simplices $a \in A_n$ and $b \in B_n$ by

$$
  \Delta_{A,B} : a \otimes b \mapsto \oplus_{p + q = n}  (\tilde d^p a) \otimes (d^q_0 b)
  \,,
$$

where the _front face map_ $\tilde d^p$ is that induced by

$$
  [p] \to [p+q] : i \mapsto i
$$

and the _back face_ $d^q_0$ map is that induced by

$$
  [q] \to [p+q] : i \mapsto i+p
  \,.
$$

=--

+-- {: .un_defn}
###### Definition


This AW map restricts to the normalized chains complex

$$
  \Delta_{A,B} :  N(A \otimes B) \to N(A) \otimes N(B)
  \,.
$$

=--

## Properties

\begin{proposition}
The Alexander-Whitney map is an [[oplax monoidal transformation]] that makes $C$ and $N$ into [[oplax monoidal functors]]. 
\end{proposition}

Beware that the AW map is _not_ [[symmetric monoidal category|symmetric]].
For details see *[[monoidal Dold-Kan correspondence]]*.



\begin{proposition}\label{EZAWDeformationRetract}
**([[Eilenberg-Zilber/Alexander-Whitney deformation retraction]])**
\linebreak

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

For unnormalized chain complexes, where we have a [[homotopy equivalence]], this is the original [[Eilenberg-Zilber theorem]] ([Eilenberg & Zilber 1953](#EilenbergZilber53), [Eilenberg & MacLane 1954, Thm. 2.1](#EilenbergMacLane54)). The above [[deformation retraction]] for normalized chain complexes is [Eilenberg & MacLane 1954, Thm. 2.1a](#EilenbergMacLane54). Both are reviewed in [May 1967, Cor. 29.10](#May67). Explicit description of the [[homotopy operator]] is given in [Gonzalez-Diaz & Real 1999](#GonzalezDiazReal99)).


## Related concepts

* **Alexander-Whitney map**

* [[Eilenberg-Zilber map]]

## References

The [[Eilenberg-Zilber theorem]] is due to

* {#EilenbergZilber53} [[Samuel Eilenberg]], [[Joseph Zilber]], _On Products of Complexes_, Amer. Jour. Math. 75 (1): 200&#8211;204, (1953) ([jstor:2372629](https://www.jstor.org/stable/2372629))

* {#EilenbergMacLane54} [[Samuel Eilenberg]], [[Saunders MacLane]], Section 2 of: *On the Groups $H(\Pi,n)$, II: Methods of Computation*, Annals of Mathematics, Second Series, Vol. 60, No. 1 (Jul., 1954), pp. 49-139 ([jstor:1969702](https://www.jstor.org/stable/1969702), [doi:10.2307/2372629](https://doi.org/10.2307/2372629))

using the definition of the [[Eilenberg-Zilber map]] in:

* {#EilenbergMacLane53} [[Samuel Eilenberg]], [[Saunders MacLane]], (5.3) of: *On the groups $H(\Pi,n)$*, I*, Ann. of Math. (2) 58, (1953), 55&#8211;106. ([jstor:1969820](https://www.jstor.org/stable/1969820))

Review:

* {#May67} [[Peter May]], Section 29 of: _Simplicial objects in algebraic topology_ , Chicago Lectures in Mathematics, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])

* {#GonzalezDiazReal99} Rocio Gonzalez-Diaz, Pedro Real, *A Combinatorial Method for Computing Steenrod Squares*, Journal of Pure and Applied Algebra 139 (1999) 89-108 ([arXiv:math/0110308](https://arxiv.org/abs/math/0110308))

[[!redirects Alexander-Whitney maps]]
