
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
In a model $M$ of a first-order theory $T$ a definable set $G$ might have additional algebraic stucture (e.g. that of a [[group]], [[ring]], [[groupoid]], [[category]], etc.) also given by definable functions and predicates. Since this set with extra structure is given by some collection of formulas in the language of $T$, it is interpreted in every model of $T$, and is hence an invariant of the [[syntactic category]] (walking model) $\mathbf{Def}(T)$ of $T$.

## Definition
To make this precise:

* A definable group is just a [[group object]] in $\mathbf{Def}(T)$.
* A definable groupoid is just a groupoid object, i.e. an [[internal groupoid]] in $\mathbf{Def}(T)$.
* A definable ring is just a semigroup object in the category of abelian group objects of $\mathbf{Def}(T)$.
* A definable category is just a category object, i.e. an [[internal category]] in $\mathbf{Def}(T)$.

Since groups, groupoids, rings, and categories can be given by algebraic theories, a definition (modulo having [[elimination of imaginaries|EI]]) of one of these in $T$ is just an interpretation of one of those theories in $T$ is just a logical functor from the walking models of one of these to $\mathbf{Def}(T)$.

### Remarks
* Evaluating the unit of the [[Makkai duality]] adjunction at $T$ yields $\mathbf{Def}(T) \simeq \operatorname{Hom}_{\mathbf{Ult}}(\mathbf{Mod}(T), \mathbf{Set})$ the category of [[ultrafunctors]] from the category of models (logical functors $\mathbf{Def}(T) \to \mathbf{Set}$) to $\mathbf{Set}$ viewed as [[ultracategories]], so that one may identify a definable set (and definable sets with extra definable structure on them) $X \in \mathbf{Def}(T)$ with a [[functor of points]] $M \mapsto X(M)$ on the category of models.

* The fact that the [[external axiom of choice]] (all epimorphisms split) holds in $\mathbf{Set}$ if and only if every [[fully faithful]] [[essentially surjective]] [[functor]] between [[small]] categories is a true [[equivalence of categories]] can be word-for-word internalized to $\mathbf{Def}(T)$. This means: if the theory has two constants, then $T$ has definable Skolem functions if and only if every fully faithful essentially surjective definable functor between definable categories admits a [[pseudoinverse]].

* With a suitable amount of choice (definable Skolem functions, for example) Freyd's general adjoint functor theorem also carries over word-for-word to the setting of internal categories in $\mathbf{Def}(T)$.

* In particular, there is much studied case of __definable groups__, cf. e.g. ([Peterzil-Pillay](#PeterzilPillay))

## Properties


+-- {: .num_defn}
###### Theorem

There is a [[bijection|bijective]] correspondence between internal imaginary sorts of $T$ and definable concrete groupoids with a single isomorphism class, up to bi-interpretability over $T$ for the internal imaginary sorts and Hrushovski-equivalence for the definable concrete groupoids.

=--

This is ([Hrushovski 2006, Th.3.2](#Hrushovski)).


## Related concepts

* [[definability]]

## References

* Y. Peterzil, A. Pillay, _Generic sets in definably compact groups_, Fundamenta Mathematicae __193__ (2007), pp. 153--170, [MR2282713](http://www.ams.org/mathscinet-getitem?mr=2282713), [doi](http://dx.doi.org/10.4064/fm193-2-4)
 {#PeterzilPillay}

* Y. Peterzil, A. Pillay, S. Starchenko, _Linear groups definable in o-minimal structures_, J. Algebra __247__ (2002), no. 1, pp. 1--23, [MR1873380](http://www.ams.org/mathscinet-getitem?mr=1873380), [doi](http://dx.doi.org/10.1006/jabr.2001.8861)

* Alessandro Berarducci, _Definable groups in o-minimal structures_, [pdf](http://www.dm.unipi.it/~dinasso/marian2004/berarducci.pdf); _Cohomology of groups in o-minimal structures: acyclicity of the infinitesimal subgroup_, J. Symbolic Logic __74__:3 (2009), 891-900, [MR2548466](http://www.ams.org/mathscinet-getitem?mr=2548466), [euclid](http://projecteuclid.org/euclid.jsl/1245158089), [doi](http://dx.doi.org/10.2178/jsl/1245158089), _O-minimal spectra, infinitesimal subgroups and cohomology_, J. Symbolic Logic __72__ (2007), no. 4, pp. 1177--1193, [MR2371198](http://www.ams.org/mathscinet-getitem?mr=2371198), [euclid](http://projecteuclid.org/euclid.jsl/1203350779 ), [doi](http://dx.doi.org/10.2178/jsl/1203350779)

* Margarita Otero, _A survey on groups definable in o-minimal structures_, in: Model theory with applications to algebra and analysis. Vol. 2, 177&#8211;206, London Math. Soc. Lecture Note Ser. __350__, Cambridge Univ. Press 2008, [MR2010b:03042](http://www.ams.org/mathscinet-getitem?mr=2436142), [doi](http://dx.doi.org/10.1017/CBO9780511735219.006)

* [[Ehud Hrushovski]], _Groupoids, imaginaries and internal covers_ Turk. J. Math 36 (2012) 173 – 198 [doi](https://doi.org/10.3906/mat-1001-91) [arxiv/math.LO/0603413](http://arxiv.org/abs/math/0603413) (2006) {#Hrushovski06}

* [[Ehud Hrushovski]], _On finite imaginaries_, [arxiv/0902.0842](http://arxiv.org/abs/0902.0842)

* Levon Haykazyan, Rahim Moosa, _Functoriality and uniformity in Hrushovski's groupoid-cover correspondence_, [arxiv/1711.03531](https://arxiv.org/abs/1711.03531)


[[!redirects definable groupoids]]
[[!redirects definable category]]
[[!redirects definable categories]]
[[!redirects definable group]]
[[!redirects definable groups]]
