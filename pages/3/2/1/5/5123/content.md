
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

## Idea

The *Eilenberg-Zilber map* is a [[natural transformation]] intertwining the [[tensor products]] of [[chain complexes]] with that of their corresponding [[simplicial abelian groups]], which is part of the [[monoidal Dold-Kan correspondence]].

Its explicit relation by the *Eilenberg-MacLane formula* expresses it in terms of sums of non-degenerate [[simplices]] inside a [[product of simplices]].


## Definition

Denote by 

* $(sAb, \otimes)$ the [[monoidal category]] of [[simplicial abelian groups]] with [[tensor product]] given degreewise by the [[tensor product of abelian groups]];

* $(Ch_\bullet^+, \otimes)$ the [[monoidal category|monoidal]] [[category of chain complexes]] with its [[tensor product of chain complexes]].

* $C \colon sAb \to Ch_\bullet^+$ the chains/[[Moore complex]] [[functor]] of the [[Dold-Kan correspondence]];

+-- {: .num_defn #TheEilenbergZilberMap}
###### Definition

For $A,B \in sAb$ two [[simplicial abelian group]], the **Eilenberg-MacLane formula** for the **Eilenberg-Zilber map** is the [[natural transformation]] of [[chain complexes]]

$$
  \nabla_{A,B} 
  \;\colon\;  
  C(A) \otimes C(B) 
   \longrightarrow 
  C(A \otimes B) 
$$

defined on a [[pair]] of [[n-simplices|$n$-simplices]] $a \in A_p$ and $b \in B_q$ by

\[
  \label{ShuffleSumFormula}
  \begin{aligned}
  \nabla_{A,B} 
  \;\colon\; 
  a \otimes b 
    \;\mapsto\; 
   &
   \sum_{(\mu,\nu) \in Sh(p,q)} 
   sgn(\mu,\nu) 
   \cdot
   \big(s_\nu(a)\big) 
     \otimes 
   \big(s_\mu(b)\big)
   \\
   &
   \in
   C_{p+q}(A \otimes B)
   =
   A_{p+q} \otimes B_{p+q}
   \,,
  \end{aligned}
\]

where (see [here](product+of+simplices#NonDegenerateCellsInAProductOfSimplices) at *[[products of simplices]]* for the geometric interpretation):

* the [[sum]] is over all $(p,q)$-[[shuffles]]

  $$
    (\mu,\nu) = (\mu_1, \cdots, \mu_p, \nu_1, \cdots, \nu_q)
    \,,
  $$

* $sgn(\mu,\nu)$ is the [[signature of a permutation|signature]] of the corresponding [[permutation]],

* the maps $s_{\mu}$ and $s_\nu$ are iterated [[degeneracy maps]]:
  
  \[
    \label{IteratedDegeneracies} 
    s_{\mu}   
      \coloneqq 
    s_{\mu_p - 1} 
     \circ 
    \cdots 
      \circ 
    s_{\mu_2 - 1} 
      \circ 
    s_{\mu_1 - 1}
    \,,
    \phantom{----}\text{and}\phantom{----}
    s_{\nu} 
      \coloneqq 
    s_{\nu_q - 1} 
      \circ 
    \cdots 
      \circ
    s_{\nu_2 - 1} 
      \circ 
    s_{\nu_1 - 1}
    \,.
  \]

=--

\begin{remark}\label{Attribution} 
The explicit formula (eq:ShuffleSumFormula) is due to [Eilenberg & MacLane (1953), eq. (5.3)](#EilenbergMacLane53), there called the "*$\nabla$-product*";  review includes [MacLane (1963), eq. (8.9)](#MacLane63); [May (1967)](#May67), [p. 133](https://ncatlab.org/nlab/files/May_SimplicialObjectsInAlgebraicTopology.pdf#page=76); [Quillen (1969), eq. (4.2)](#Quillen69); [Loday (1992), Def. 1.6.11](#Loday92); [Gonzalez-Diaz & Real (1999)](EZAW+deformation+retraction#GonzalezDiazReal99), [p. 7](https://arxiv.org/pdf/math/0110308.pdf#page=7). 

The map that is expressed by this formula was previously shown to exist, more abstractly, by [Eilenberg & Zilber (1953)](#EilenbergZilber53); cf. also [[Kerodon]], [Rem. 2.5.7.16](https://kerodon.net/tag/00RX).
\end{remark}

\begin{remark}
The shift in the indices in (eq:IteratedDegeneracies) is to be consistent with the convention that the [[shuffle]] $(\mu, \nu)$ is a [[permutation]] of $\{1, \dots, p+q\}$. In many references the shift disappears (here) by making it a permutation of $\{0, \dots, p+q-1\}$, instead.
\end{remark}

+-- {: .num_remark}
###### Remark

The [[sum]] in (eq:ShuffleSumFormula) may be understood as being over all non-degenerate simplices in the [[Cartesian product]] $\Delta[p] \times \Delta[q]$ of [[simplices]]. See at *[[products of simplices]]* ([here](product+of+simplices#NonDegenerateCellsInAProductOfSimplices)) for more on this.

=--

+-- {: .num_prop}
###### Proposition

This Eilenberg-Zilber map (Def. \ref{TheEilenbergZilberMap}) [[corestriction|co]]/[[restriction|restricts]] on the [[normalized chain complex]] inside the [[Moore complex]], to a [[chain map]] of the form:

$$
  \nabla_{A,B} 
    \;\colon\;  
  N(A) \otimes N(B) 
    \longrightarrow 
  N(A \otimes B) 
  \,.
$$

=--

(cf. e.g. [[Kerodon]], [Exp. 2.5.7.12.](https://kerodon.net/tag/00RT))


## Properties

### Monoidal properties

+-- {: .num_prop}
###### Proposition

The Eilenberg-Zilber map (Def. \ref{TheEilenbergZilberMap}) is a [[lax monoidal transformation]] that makes $C$ and $N$ into [[lax monoidal functors]]. 

=--

See at *[[monoidal Dold-Kan correspondence]]* for details.

For the next statement notice that both $sAb$ and $Ch_\bullet^+$ are in fact [[symmetric monoidal categories]].

+-- {: .num_prop}
###### Proposition
 
The EZ map (Def. \ref{TheEilenbergZilberMap}) is [[symmetric monoidal functor|symmetric]] in that for all $A,B \in sAb$ the square

$$
  \array{
    C A \otimes C B &\stackrel{\sigma}{\to}& C B \otimes C A
    \\
    {}^{\mathllap{\nabla_{A,B}}}
    \big\downarrow 
    && 
    \big\downarrow^{\mathrlap{\nabla_{B,A}}}
    \\
    C(A\otimes B) &\stackrel{C(\sigma)}{\to}& C(B \otimes A)
  }
$$

[[commuting diagram|commutes]], where $\sigma$ denotes the [[braiding|symmetry isomorphism]] in $sAb$ and $Ch_\bullet^+$.

=--

### Eilenberg-Zilber theorem

\begin{proposition}\label{EZAWDeformationRetract}
**([[Eilenberg-Zilber/Alexander-Whitney deformation retraction]])** \linebreak

Let 

* $A, B \,\in\, sAb = $ [[SimplicialAbelianGroups]]

and denote 

* by $N(A), N(B) \,\in\, Ch^+_\bullet $ (=[[ConnectiveChainComplexes]]) their [[normalized chain complexes]], 

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

For unnormalized chain complexes, where we have a [[homotopy equivalence]], this is the original [[Eilenberg-Zilber theorem]] ([Eilenberg & Zilber 1953](EZAW+deformation+retraction#EilenbergZilber53), [Eilenberg & MacLane 1954, Thm. 2.1](EZAW+deformation+retraction#EilenbergMacLane54)). The above [[deformation retraction]] for normalized chain complexes is [Eilenberg & MacLane 1954, Thm. 2.1a](EZAW+deformation+retraction#EilenbergMacLane54). Both are reviewed in [May 1967, Cor. 29.10](EZAW+deformation+retraction#May67). Explicit description of the [[homotopy operator]] is given in [Gonzalez-Diaz & Real 1999](EZAW+deformation+retraction#GonzalezDiazReal99).




## Applications

* The Eilenberg-Zilber map induces a functor from [[simplicial Lie algebras]] to [[dg-Lie algebras]] (see [here](dgLieAlgebraOfASimplicialLieAlgebra)).

* The Eilenberg-Zilber map controls the formula for [[transgression in group cohomology]], see there fore more.

* In the context of filtered spaces $X_*, Y_*$ and their associated fundamental [[crossed complexes]] $\Pi X_*, \Pi Y_*$ there is a natural  Eilenberg-Zilber morphism  
$$\eta: \Pi X_* \otimes \Pi Y_* \to \Pi (X_* \otimes Y_*)$$
which is difficult to define directly because of the complications of the tensor product of crossed complexes,  but has a direct definition in terms of the associated cubical homotopy $\omega$--groupoids. This morphism is an isomorphism of free crossed complexes if $X_*, Y_*$ are the skeletal filtrations of CW-complexes. For more on all  this, see the book *[[Nonabelian Algebraic Topology]]* p. 533. 


## Related concepts

* [[Alexander-Whitney map]]

* [[Eilenberg-Zilber theorem]]

* [[product of simplices]]

* [[cap product]], [[cup product]]

* [[transgression in group cohomology]]


## References

The Eilenberg-MacLane formula was made explicit in:

* {#EilenbergMacLane53} [[Samuel Eilenberg]], [[Saunders MacLane]], (5.3) of: *On the groups $H(\Pi,n)$, I*, Ann. of Math. **58** 1 (1953) 55-106. &lbrack;[jstor:1969820](https://www.jstor.org/stable/1969820)&rbrack;

realizing a transformation that was shown more indirectly to exist in the proof of the [[Eilenberg-Zilber theorem]]:

* {#EilenbergZilber53} [[Samuel Eilenberg]], [[Joseph A. Zilber]], *On Products of Complexes*, American Journal of Mathematics **75** 1 (1953) 200-204 &lbrack;[jstor:2372629](https://www.jstor.org/stable/2372629), [doi:10.2307/2372629](https://doi.org/10.2307/2372629)&rbrack;

Review and further discussion:

* {#MacLane63} [[Saunders MacLane]], Thm. 8.8 in: *Homology*, Grundlehren der Mathematischen Wissenschaften **114**, Springer (1963, 1974), reprinted as: Classics in Mathematics, Springer (1995)  &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/maclane_homology.pdf), [doi:10.1007/978-3-642-62029-4](https://doi.org/10.1007/978-3-642-62029-4)&rbrack;

* {#May67} [[Peter May]], Section 29.7 of _Simplicial objects in algebraic topology_ , Chicago Lectures in Mathematics, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])

* {#Quillen69} [[Dan Quillen]], part I, section 4 of: _Rational homotopy theory_, The Annals of Mathematics, Second Series **90** 2 (1969) 205-295 &lbrack;[jstor:1970725](http://www.jstor.org/stable/1970725)&rbrack;

* {#Loday92} [[Jean-Louis Loday]], Section 1.6 of: *Cyclic Homology*, Grund. Math. Wiss. **301** Springer (1992) &lbrack;[doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9)&rbrack;

* {#SchwedeShipley03} [[Stefan Schwede]], [[Brooke Shipley]], §2.3 in: _Equivalences of monoidal model categories_, Algebr. Geom. Topol. **3** (2003) 287-334 &lbrack;[arXiv:math.AT/0209342](http://arxiv.org/abs/math.AT/0209342), [euclid:euclid.agt/1513882376](https://projecteuclid.org/euclid.agt/1513882376)&rbrack;


* [[Kerodon]], 2.5.7 *The Shuffle Product* ([00RF](https://kerodon.net/tag/00RF))

  *The Eilenberg-Zilber Homomorphism* ([00RS](https://kerodon.net/tag/00RS))


See also:

* [[Andy Tonks|A.P. Tonks]], _On the Eilenberg-Zilber Theorem for crossed complexes_. J. Pure Appl. Algebra, 179 (1-2) (2003) 199-220

* [[Tim Porter]], Section 11.2 of: _[[Crossed Menagerie]]_,

* [[Ronnie Brown]], _The twisted Eilenberg-Zilber theorem_. Simposio di Topologia (Messina, 1964), Edizioni Oderisi, Gubbio (1965), 33--37. [pdf](http://pages.bangor.ac.uk/~mas010/pdffiles/twistedez.pdf)

[[!redirects Eilenberg-MacLane forumla]]

[[!redirects shuffle map]]


