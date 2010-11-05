

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
  s_{\mu} = s_{\mu_p} \circ \cdots s_{\mu_2} \circ s_{\mu_1}
$$

and

$$
  s_{\nu} = s_{\nu_q} \circ \cdots s_{\nu_2} \circ s_{\nu_1}
  \,.
$$

The sign $sign(\mu,\nu) \in \{-1,1\}$ is the [[signature of a permutation|signature]] of the corresponding [[permutation]].

=--

+-- {: .un_remark}
###### Remark

The sum may be understood as being over all non-degenerate simplices in the product $\Delta[p] \times \Delta[q]$. See [[products of simplices]] for more on this.

=--

+-- {: .un_prop}
###### Proposition


This map restricts to the normalized chains complex

$$
  \nabla_{A,B} :  N(A) \otimes N(B) \to N(A \otimes B) 
  \,.
$$

=--


## Properties

+-- {: .un_prop}
###### Proposition

The Eilenberg-Zilber map is a [[lax monoidal transformation]] that makes $C$ and $N$ into [[lax monoidal functor]]s. 

=--

See [[monoidal Dold-Kan correspondence]] for details.

+-- {: .un_prop}
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

+-- {: .un_prop}
###### Proposition

For all $X,Y$ the EZ map $\nabla_{X,Y}$ is a [[quasi-isomorphism]] and in fact a chain [[homotopy equivalence]].

=--

This is in 29.10 of ([May](#May)).


For the next statement notice that both $sAb$ and $Ch_\bullet^+$ are in fact [[symmetric monoidal categories]].

+-- {: .un_prop}
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


## Related concepts

* [[Alexander-Whitney map]]

* **Eilenberg-Zilber map**

## References

The Eilenberg-Zilber map was introduced in (5.3) of 

* [[Samuel Eilenberg]], [[Saunders MacLane]], On the groups $H(\Pi,n)$, I, Ann. of Math. (2) 58, (1953), 55&#8211;106.

See also 29.7 of 

* [[Peter May]], _Simplicial objects in algebraic topology_ , Chicago Lectures in Mathematics, Chicago, (1967) ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu))
{#May}

and section 11.2 of

* [[Tim Porter]], _[[Crossed Menagerie]]_

[[!redirects shuffle map]]