
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
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

The [[model structure on simplicial algebras]] for [[simplicial Lie algebras]].

## Details
 {#Details}


+-- {: .num_defn #CategoryOfSimplicialLieAlgebras}
###### Definition

For $k$ some [[field]], write $LieAg_k$ for the [[category]] of [[Lie algebras]] over $k$, and write 

$$
  ((LieAlg)_k)^{\Delta^{op}}
  \in sSetCat
$$ 

for the category of [[simplicial objects]] in that category, naturally regarded as a [[simplicial category]]. Say a morphism in that category is a _weak equivalence_ or _fibration_, if its underlying morphism of [[simplicial sets]] is a weak equivalence or fibration, respectively, in the [[classical model structure on simplicial sets]]. Write $((LieAlg)_k)^{\Delta^{op}}_{proj}$ for the category equipped with these classes of morphism.

=--

+-- {: .num_prop }
###### Proposition

The category $((LieAlg)_k)^{\Delta^{op}}_{proj}$ from def. \ref{CategoryOfSimplicialLieAlgebras} is a [[simplicial model category]].

=--

Since [[Lie algebras]] are algebras over a [[Lawvere theory]], this is a special case of ([Reedy 74, theorem I](https://ncatlab.org/nlab/show/model+structure+on+simplicial+algebras#Reedy74)) discussed at _[[model structure on simplicial algebras]]_. Without the simplicial enrichment and on [[reduced simplicial sets|reduced]] simplicial Lie algebras this model structure is left as an exercise for the reader in ([Quillen 69, below theorem 4.7](#Quillen69)).

## Related concepts

* [[model structure on dg-Lie algebras]]

* [[model structure for L-infinity algebras]]

* [[model structure on dg-coalgebras]]

## References

The model structure for [[reduced simplicial set|reduced]] simplicial Lie algebras is originally due to

* {#Quillen69} [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([JSTOR](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf)) 

On the [[homotopy theory]] of simplicial Lie algebras see also

* [[Stewart Priddy]], _On the homotopy theory of simplicial Lie algebras_, ([pdf](http://www.ams.org/journals/proc/1970-025-03/S0002-9939-1970-0270371-9/S0002-9939-1970-0270371-9.pdf))

* [[Graham Ellis]], _Homotopical aspects of Lie algebras_ Austral. Math. Soc. (Series A) 54 (1993), 393-419 ([web](http://anziamj.austms.org.au/JAMSA/V54/Part3/Ellis.html))

[[!redirects model structures on simplicial Lie algebras]]
