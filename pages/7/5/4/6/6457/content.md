
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _simplicial Lie algebra_ is a [[simplicial object]] in the [[category]] of [[Lie algebra]]s.

## Properties
 {#Properties}

+-- {: .num_theorem}
###### Theorem

There is an [[adjunction]]

$$
  (N^* \dashv N) : LieAlg_k^\Delta \stackrel{\overset{N^*}{\leftarrow}}{\underset{N}{\to}}
  dgLieAlg_k
$$

between simplicial Lie algebras (over a [[field]] $k$) and [[dg-Lie algebra]]s, where $N$ acts on the underlying simplicial vector spaces as the [[Moore complex]] functor.

=--

This is ([Quillen 69, prop. 4.4](#Quillen69)).

+-- {: .num_remark}
###### Remark

There is a standard structure of a [[category with weak equivalences]] on both these categories, hence there are corresponding [[homotopy categories]]. (See also at _[[model structure on simplicial Lie algebras]]_ and _[[model structure on dg-Lie algebras]]_.) The following asserts that the above adjunction is compatible with this structure.

=--

+-- {: .num_theorem}
###### Theorem

For $k$ a [[field]] of [[characteristic zero]] the corresponding [[derived functors]] constitute an [[equivalence of categories]] between the corresponding [[homotopy categories]]

$$
  (L N^* \dashv \tilde N) 
   \;\colon\;
  Ho(LieAlg^\Delta)_1 
   \stackrel{\overset{L N^*}{\leftarrow}}{\underset{\tilde N}{\to}} Ho(dgLieAlg)_1
$$

of [[1-connected]] objects on both sides.

=--

This is in the proof of ([Quillen, theorem. 4.4](#Quillen)).


## Related concepts

* [[model structure on simplicial Lie algebras]]

* [[simplicial group]]


## References

An early account is in 

* {#Quillen69} [[Dan Quillen]], part I, section 4 of _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([JSTOR](http://www.jstor.org/stable/1970725))
 

See also

* Christian R&#252;schoff, section 8.3 of _relative algebraic $K$-theory and algebraic cyclic homology_ ([pdf](http://archiv.ub.uni-heidelberg.de/volltextserver/22305/1/Dissertation%20-%20Rueschoff.pdf))

* &#304;. Ak&#231;a and Z. Arvasi, _Simplicial and crossed Lie algebras_ Homology Homotopy Appl. Volume 4, Number 1 (2002), 43-57. 

On the [[homotopy theory]] of simplicial Lie algebras see also

* [[Stewart Priddy]], _On the homotopy theory of simplicial Lie algebras_, ([pdf](http://www.ams.org/journals/proc/1970-025-03/S0002-9939-1970-0270371-9/S0002-9939-1970-0270371-9.pdf))

* [[Graham Ellis]], _Homotopical aspects of Lie algebras_ Austral. Math. Soc. (Series A) 54 (1993), 393-419 ([web](http://anziamj.austms.org.au/JAMSA/V54/Part3/Ellis.html))





[[!redirects simplicial Lie algebras]]