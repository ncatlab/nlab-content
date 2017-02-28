
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

+-- {: .num_prop #ProjectiveModelStructureOnSimplicialLieAlgebras}
###### Proposition

The category $((LieAlg)_k)^{\Delta^{op}}_{proj}$ from def. \ref{CategoryOfSimplicialLieAlgebras} is a [[simplicial model category]].

=--

Since [[Lie algebras]] are algebras over a [[Lawvere theory]], this is a special case of ([Reedy 74, theorem I](https://ncatlab.org/nlab/show/model+structure+on+simplicial+algebras#Reedy74)) discussed at _[[model structure on simplicial algebras]]_. Without the simplicial enrichment and on [[reduced simplicial sets|reduced]] simplicial Lie algebras this model structure is a special case of ([Quillen 67, II.4 theorem 4](#Quillen67)) and also left as an exercise for the reader in ([Quillen 69, below theorem 4.7](#Quillen69)).

## Properties

### Relation to dg-Lie algebras

+-- {: .num_defn #dgLieAlgebraOfASimplicialLieAlgebra}
###### Definition

Let $(\mathfrak{g}, [-,-]$ be a [[simplicial Lie algebra]]. Then the [[normalized chains complex]] $N \mathfrak{g}$ of the underlying [[simplicial abelian group]] becomes a [[dg-Lie algebra]] by equipping it with the [[Lie bracket]] given by the following [[composition|composite]] morphisms

$$
  [-,-]_{N \mathfrak{g}}
  \;\colon\;
  (N \mathfrak{g}) \otimes_k (N \mathfrak{g})
    \overset{\nabla}{\longrightarrow}
  N (\mathfrak{g} \otimes_k \mathfrak{g})
    \overset{N([-,-])}{\longrightarrow}
  N (\mathfrak{g})
$$

where the first morphism is the [[Eilenberg-Zilber map]].

This construction extends to a [[functor]]

$$
  N 
    \;\colon\;
  LieAlg_k^{\Delta^{op}}
    \longrightarrow
  dgLieAlg_k
$$

from simplical Lie algebras to [[dg-Lie algebras]].

=--

([Quillen 69, (4.3)](#Quillen69))


+-- {: .num_prop #NormalizedChainsFromSimplicialLieAlgtodgLieAlgHasLeftAdjoint}
###### Proposition

The functor $N$ from simplicial Lie algebras to dg-Lie algebras from def. \ref{dgLieAlgebraOfASimplicialLieAlgebra} has a [[left adjoint]] 

$$
  (N^* \dashv N) 
    \;\colon\; 
  LieAlg_k^{\Delta^{op}} 
    \underoverset
      {\underset{N}{\longrightarrow}}
      {\overset{N^*}{\longleftarrow}}
      {\bot}
  dgLieAlg_k
  \,.
$$

=--

This is ([Quillen 69, prop. 4.4](#Quillen69)).


+-- {: .num_prop #QuillenAdjunctionTodgLieAlgebras}
###### Proposition

With respect to the projective model structure on simplicial Lie algebras from prop. \ref{ProjectiveModelStructureOnSimplicialLieAlgebras} and the projective [[model structure on dg-Lie algebras]] ([this prop.](model+structure+on+dg-Lie+algebras#ProjectiveModelStructureOndgLieAlgebras)) the [[adjunction]] from prop. \ref{NormalizedChainsFromSimplicialLieAlgtodgLieAlgHasLeftAdjoint} is a [[Quillen adjunction]]

$$
  (N^* \dashv N) 
    \;\colon\; 
  (LieAlg_k^{\Delta^{op}})_{proj} 
    \underoverset
      {\underset{N}{\longrightarrow}}
      {\overset{N^*}{\longleftarrow}}
      {\bot}
  (dgLieAlg_k)_{proj}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the standard [[Dold-Kan correspondence]] $N$ preserves fibrations and weak equivalences  ([this prop.](Dold-Kan+correspondence#QuillenEquivalenceBetweensAbAndCh), [Schwede-Shipley 02, section 4.1](#SchwedeShipley), [p.17](http://www.math.uic.edu/~bshipley/monoidalequi.final.pdf#page=17)).

=--

+-- {: .num_prop }
###### Proposition

The [[adjunction]] between [[homotopy categories]] of the [[derived functors]] of the [[Quillen adjunction]] in prop. \ref{QuillenAdjunctionTodgLieAlgebras} 

$$
  Ho(LieAlg_k^{\Delta^{op}})
    \underoverset
      {\underset{\mathbb{R}N}{\longrightarrow}}
      {\overset{\mathbb{L}N^*}{\longleftarrow}}
      {\bot}
  Ho(dgLieAlg_k)
$$

restricts on connected simplicial algebras and connected [[dg-Lie algebras]] (meaning: having the trivial Lie algebra in degree 0) to an [[equivalence of categories]]:

$$
  Ho(LieAlg_k^{\Delta^{op}})_{\geq 1}
    \underoverset
      {\underset{\mathbb{R}N}{\longrightarrow}}
      {\overset{\mathbb{L}N^*}{\longleftarrow}}
      {\simeq}
  Ho(dgLieAlg_k)_{\geq 1}
  \,.
$$

=--

([Quillen 76, section II.4, see p. 224 (20 of 92)](#Quillen76), see also figure 2 on p. 211 (8 of 92))

## Related concepts

* [[model structure on dg-Lie algebras]]

* [[model structure for L-infinity algebras]]

* [[model structure on dg-coalgebras]]

## References

The model structure for for simplicial %T%Palgebras is originally due to

* {#Quillen67} [[Dan Quillen]], _Homotopical Algebra_, Lectures Notes in Mathematics 43, Springer Verlag, Berlin, (1967)

and specifically for [[reduced simplicial set|reduced]] simplicial Lie algebras due to

* {#Quillen69} [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([JSTOR](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf)) 

On the [[homotopy theory]] of simplicial Lie algebras see also

* [[Stewart Priddy]], _On the homotopy theory of simplicial Lie algebras_, ([pdf](http://www.ams.org/journals/proc/1970-025-03/S0002-9939-1970-0270371-9/S0002-9939-1970-0270371-9.pdf))

* [[Graham Ellis]], _Homotopical aspects of Lie algebras_ Austral. Math. Soc. (Series A) 54 (1993), 393-419 ([web](http://anziamj.austms.org.au/JAMSA/V54/Part3/Ellis.html))

See also

* {#SchwedeShipley02} [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_, Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv:math.AT/0209342](http://arxiv.org/abs/math.AT/0209342))


[[!redirects model structures on simplicial Lie algebras]]
