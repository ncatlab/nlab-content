

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

+-- {: .num_defn}
###### Definition

For $A,B \in sAb$ two abelian [[simplicial group]]s, the **Eilenberg-Zilber map** or **Eilenberg-MacLane map** or **shuffle map** is the [[natural transformation]] on [[chain complex]]es

$$
  \nabla_{A,B} :  C(A) \otimes C(B) \to C(A \otimes B) 
$$

defined on two $n$-simplices $a \in A_p$ and $b \in B_q$ by

$$
  \nabla_{A,B} : a \otimes b \mapsto 
   \sum_{(\mu,\nu)} sign(\mu,\nu) (s_\nu(a)) \otimes (s_\mu(b))
   \;\;
   \in
   C_{p+q}(A \otimes B)
   =
   A_{p+q} \otimes B_{p+q}
  \,,
$$

where the sum is over all $(p,q)$-[[shuffle]]s

$$
  (\mu,\nu) = (\mu_1, \cdots, \mu_p, \nu_1, \cdots, \nu_q)
$$

and the corresponding degeneracy maps are

$$
  s_{\mu} = s_{\mu_p - 1} \circ \cdots s_{\mu_2 - 1} \circ s_{\mu_1 - 1}
$$

and

$$
  s_{\nu} = s_{\nu_q - 1} \circ \cdots s_{\nu_2 - 1} \circ s_{\nu_1 - 1}
  \,.
$$

(The shift in the indices is to be coherent with the convention that the [[shuffle]] $(\mu, \nu)$ is a [[permutation]] of $\{1, \dots, p+q\}$. In many references the shift disappears by making it a permutation of $\{0, \dots, p+q-1\}$ instead.) The sign $sign(\mu,\nu) \in \{-1,1\}$ is the [[signature of a permutation|signature]] of the corresponding [[permutation]].

=--

+-- {: .num_remark}
###### Remark

The sum may be understood as being over all non-degenerate simplices in the product $\Delta[p] \times \Delta[q]$. See [[products of simplices]] for more on this.

=--

+-- {: .num_prop}
###### Proposition


This map restricts to the normalized chain complex

$$
  \nabla_{A,B} :  N(A) \otimes N(B) \to N(A \otimes B) 
  \,.
$$

=--


## Properties


+-- {: .num_prop}
###### Proposition

The Eilenberg-Zilber map is a [[lax monoidal transformation]] that makes $C$ and $N$ into [[lax monoidal functor]]s. 

=--

See [[monoidal Dold-Kan correspondence]] for details.

+-- {: .num_prop}
###### Proposition


On normalized chain complexes the EZ map has a [[left inverse]], given by the [[Alexander-Whitney map]] $\Delta_{A,B}$:

$$
  Id 
  :
  N A \otimes N B \stackrel{\nabla_{A,B}}{\to} N(A \otimes B)
  \stackrel{\Delta_{A,B}}{\to}
  N A \otimes N B
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For all $X,Y$ the EZ map $\nabla_{X,Y}$ is a [[quasi-isomorphism]] and in fact a chain [[homotopy equivalence]].

=--

This is in 29.10 of ([May](#May)).


For the next statement notice that both $sAb$ and $Ch_\bullet^+$ are in fact [[symmetric monoidal categories]].

+-- {: .num_prop}
###### Proposition

 
The EZ map is [[symmetric monoidal functor|symmetric]] in that for all $A,B \in sAb$ the square

$$
  \array{
    C A \otimes C B &\stackrel{\sigma}{\to}& C B \otimes C A
    \\
    {}^{\mathllap{\nabla_{A,B}}}\downarrow 
    && 
    \downarrow^{\mathrlap{\nabla_{B,A}}}
    \\
    C(A\otimes B) &\stackrel{C(\sigma)}{\to}& C(B \otimes A)
  }
$$

commutes, where $\sigma$ denotes the symmetry isomorphism in $sAb$ and $Ch_\bullet^+$.

=--

## Applications

* The Eilenberg-Zilber map induces a functor from [[simplicial Lie algebras]] to [[dg-Lie algebras]] (see [here](dgLieAlgebraOfASimplicialLieAlgebra))


## Related concepts

* [[Alexander-Whitney map]]

* **Eilenberg-Zilber map**

* [[Eilenberg-Zilber theorem]]

* [[product of simplices]]

* [[cap product]], [[cup product]]

In the context of  filtered spaces $X_*, Y_*$ and their associated fundamental crossed complexes $\Pi X_*, \Pi Y_*$ there is a natural  Eilenberg-Zilber morphism  
$$\eta: \Pi X_* \otimes \Pi Y_* \to \Pi (X_* \otimes Y_*)$$
which is difficult to define directly because of the complications of the tensor product of crossed complexes,  but has a direct definition in terms of the associated cubical homotopy $\omega$--groupoids. This morphism is an isomorphism of free crossed complexes if $X_*, Y_*$ are the skeletal filtrations of CW-complexes. For more on all  this, see the book [[Nonabelian Algebraic Topology]] p. 533. 

## References

The Eilenberg-Zilber map was introduced in:

* [[Samuel Eilenberg]], [[Saunders MacLane]], (5.3) of: *On the groups $H(\Pi,n)$*, I, Ann. of Math. (2) 58, (1953), 55&#8211;106. ([jstor:1969820](https://www.jstor.org/stable/1969820))

following the [[Eilenberg-Zilber theorem]] of

* [[Samuel Eilenberg]], [[Joseph A. Zilber]], American Journal of Mathematics Vol. 75, No. 1 (Jan., 1953), pp. 200-204 ([jstor:2372629](https://www.jstor.org/stable/2372629), [doi:10.2307/2372629](https://doi.org/10.2307/2372629))

See also:

* {#May} [[Peter May]], Section 29.7 of _Simplicial objects in algebraic topology_ , Chicago Lectures in Mathematics, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])

* [[Andy Tonks|A.P. Tonks]], _On the Eilenberg-Zilber Theorem for crossed complexes_. J. Pure Appl. Algebra, 179~(1-2) (2003) 199--220, 

* [[Tim Porter]], section 11.2 of _[[Crossed Menagerie]]_,

* [[Jean-Louis Loday]], Section 1.6 of: _Cyclic Homology_, Grund. Math. Wiss. 301, Springer, 1992 ([doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9))

* {#Quillen69} [[Dan Quillen]], part I, section 4 of _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](http://www.jstor.org/stable/1970725))

The specific maps introduced by Eilenberg-Mac Lane have stronger properties which for simplicial sets $K,L$ make $C(K) \otimes C(L)$ a strong deformation retract of $C(K \times L)$. This is exploited in 

* [[Ronnie Brown]], _The twisted Eilenberg-Zilber theorem_. Simposio di Topologia (Messina, 1964), Edizioni Oderisi, Gubbio (1965), 33--37. [pdf](http://pages.bangor.ac.uk/~mas010/pdffiles/twistedez.pdf)




[[!redirects shuffle map]]