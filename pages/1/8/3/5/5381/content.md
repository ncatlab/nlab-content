+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _perfect complex_ over a [[commutative ring]] $A$ is a [[perfect module]] over the [[Eilenberg-Mac Lane spectrum]] $H(A)$.
Under the [[stable Dold-Kan correspondence]], perfect complexes correspond to [[bounded chain complexes]] of [[finitely generated module|finitely generated]] [[projective modules]].

Viewing [[commutative rings]] as [[affine schemes]], this definition generalizes to arbitrary [[stacks]].
In this generality, perfect modules still coincide with the [[dualizable object|dualizable objects]], but not always with the [[compact object in an (infinity,1)-category|compact objects]].
The latter does hold for quasi-compact quasi-separated [[schemes]] by work of [[Robert Thomason|Thomason]], [[Amnon Neeman|Neeman]], [[Alexei Bondal|Bondal]]-[[Michel Van den Bergh|Van den Bergh]].

## Properties

### Relation to compact objects

+-- {: .num_prop}
###### Proposition

Let $A$ be a [[commutative ring]] and let $D(A)$ denote the [[derived category]] of $A$-[[modules]].  A [[chain complex]] $M_\bullet$ of $A$-modules is perfect if and only if it is a [compact object](compact+object#CompactnessInAdditiveCategories) of $D(A)$.

=--

For instance [(Stacks Project, 07LT)](http://stacks.math.columbia.edu/tag/07LT).



### Perfect complexes on a ringed space

Let $(X, \mathcal{O}_X)$ be a [[ringed space]].  A [[chain complex]] of $\mathcal{O}_X$-[[sheaf of modules|modules]] is called **perfect** if it is locally [[quasi-isomorphism|quasi-isomorphic]] to a [[bounded complex]] of [[free sheaf|free]] $\mathcal{O}_X$-modules of [[coherent sheaf|finite type]].

Let $D(Mod(\mathcal{O}_X))$ be the [[derived category]] of $\mathcal{O}_X$-modules.  Let $Pf(X) \subset D(Mod(\mathcal{O}_X))$ denote the [[full subcategory]] of perfect complexes.
This is a [[triangulated category|triangulated subcategory]], see [[triangulated categories of sheaves]].

## Related concepts

* [[perfect module]]

* [[perfect dg-module]]

* [[triangulated categories of sheaves]]

* [[determinant of a perfect complex]]

[[!include finite objects -- table]]

## References

* [[R. Thomason]], T. Trobaugh, _Higher algebraic K-theory of schemes and of derived categories_, in The Grothendieck Festschrift, Vol. III (1990), pp. 247-436.

* [[Alexei Bondal]], [[Michel Van den Bergh]], _Generators and representability of functors in commutative and  noncommutative geometry_, Moscow Math. Vol. 3, no. 1 (2003), pp. 1-36, [arXiv:math/0204218](http://arxiv.org/abs/math/0204218), [pdf](http://www.ams.org/distribution/mmj/vol3-1-2003/bondal-vandenbergh.pdf).

* [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, J. Amer. Math. Soc., vol. 9, no. 1, 1996, pp. 205-236.

* [[Raphaël Rouquier]], _Dimensions of triangulated categories_, Journal of K-theory, 1 (2008), pp. 1-36, [arXiv:math/0310134](http://arxiv.org/abs/math/0310134), [pdf](http://people.maths.ox.ac.uk/rouquier/papers/dimension.pdf).

* [[The Stacks Project]], _[Characterizing perfect objects](http://stacks.math.columbia.edu/tag/07LQ)_

* [[Jack Hall]], [[David Rydh]], _Perfect complexes on algebraic stacks_, [arXiv:1405.1887](http://arxiv.org/abs/1405.1887).

[[!redirects perfect complex]]
[[!redirects perfect complexes]]
[[!redirects perfect chain complexes]]
[[!redirects perfect complex of sheaves]]
[[!redirects perfect complexes of sheaves]]
