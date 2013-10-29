
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $G$ a suitable ([[compact Lie group|compact]]) [[Lie group]], the  $G$-[[equivariant K-theory]] of the point is the [[representation ring]] of the group $G$:

$$
  K_G(\ast) \simeq Rep(G)
  \,.
$$

Accordingly the construction of an [[index]] ([[push-forward in generalized cohomology|push-forward]] to the point) in equivariant K-theory is a way of producing $G$-[[representations]] from [[equivariant vector bundles]]. Specifically with $K \hookrightarrow G$ a suitable subgroup for the push-forward from $K$-equivariant to $G$-equivariant K-theory/representations, this method is also called _Dirac induction_ since it is analogous to the construction of _[[induced representations]]_.

Applied to equivariant [[complex line bundles]] on [[coadjoint orbits]] of $G$, Dirac induction is a [[K-theory|K-theoretic]] formulation of the [[orbit method]].

## Properties

### Relation to the orbit method
 {#RelationToTheOrbitMethod}

+-- {: .num_prop}
###### Proposition

For $G$ a [[compact Lie group]] with [[Lie algebra]] $\mathfrak{g}^\ast$, the [[push-forward in generalized cohomology|push-forward]] in compactly supported [[twisted K-theory|twisted]] $G$-[[equivariant K-theory]] to the point (the $G$-equivariant [[index]]) produces the [[Thom isomorphism]]

$$
  ind_{\mathfrak{g}^\ast} 
    \;\colon\; 
  K_G^{\sigma + dim G}(\mathfrak{g}^\ast)_{cpt} 
   \stackrel{\simeq}{\to} 
  K_G^0(\ast) \simeq Rep(G)
  \,.
$$

Moreover, for $i \colon \mathcal{O} \hookrightarrow \mathfrak{g}^\ast$ a regular [[coadjoint orbit]], [[push-forward in generalized cohomology|push-forward]] involves a [[twisted K-theory|twist]] $\sigma$ of the form

$$
  Rep(G) \simeq K_G^0(\ast)
  \stackrel{ind_{\mathcal{O}}}{\leftarrow}
  K_G^{\sigma(\mathcal{O}) + dim(\mathcal{O})}(\mathcal{O})
  \stackrel{i_!}{\to}
  K_G^{\sigma + dim G}(\mathfrak{g}^\ast)_{cpt}
$$

and 

1. $i_!$ is surjective 

1. $ind_{\mathcal{O}} = ind_{\mathfrak{g}^\ast} \circ i_!$.

=--

This is ([FHT II, (1.27), theorem 1.28](#FHT)). Related results are in ([Hochs 12, section 2.2](#Hochs12)). For more background see at _[[orbit method]]_.


## Related concepts

* [[Schubert calculus]]

## References

The idea of Dirac induction goes back to [[Raoul Bott]]'s formulation in the 1960s of [[index theory]] in the [[equivariant cohomology|equivariant]] context.

* [[Raoul Bott]], _The index theorem for homogeneous differential operators_, In: _Differential and combinatorial topology_ (A symposium in honor of Marston Morse), 1965, Princeton Univ. Press, Princeton, NJ, 167&#8211;186
 {#Bott65}

* [[Michael Atiyah]], [[Raoul Bott]], _A Lefschetz fixed point formula for
elliptic complexes. II_. Applications. Ann. of Math. (2), 88:451&#8211;
491, 1968.
 {#AtiyahBott68}

A generalization to [[super Lie groups]] is discussed in 

* [[Gregory Landweber]], _Twisted representation rings and Dirac induction_, J. Pure Appl. Algebra 206 (2006), no. 1-2, 21-54 ([arXiv:math/0403524](http://arxiv.org/abs/math/0403524))

An inverse to Dirac induction, hence a construction of good equivariant vector bundles that push to a given representation, is discussed in 

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], part II, section 1 of _[[Loop Groups and Twisted K-Theory]]_
 {#FHT}

* [[Peter Hochs]], section 2.2 of _Quantisation of presymplectic manifolds, K-theory and group representations_ ([arXiv:1211.0107](http://arxiv.org/abs/1211.0107))
 {#Hochs12}

The analog of Dirac induction for K-theory replaced by [[elliptic cohomology]] is discussed in 

* [[Nora Ganter]], _The elliptic Weyl character formula_ ([arXiv:1206.0528](http://arxiv.org/abs/1206.0528))

[[!redirects Dirac inductions]]
