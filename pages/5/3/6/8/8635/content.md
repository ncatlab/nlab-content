
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Localization of a module is the result of application of an additive localization functor on the category of modules. 

In the case of commutative rings of functions, and under the [interpretation of modules as generalized vector bundles](module#RelationToVectorBundlesInIntroduction) the _localization_ of a module corresponds to the restriction of the bundle to a subspace of its base space.

## Definition

Consider the abelian category $\mathcal{A}$ of all $R$-modules, for $R$ a (possibly noncommutative) unital ring, or (left or right) $\mathcal{O}$-modules where $\mathcal{O}$ is a sheaf of (possibly noncommutative) rings, and a 
[[reflective localization]] functor $Q^* = Q^*_\Sigma:\mathcal{A}\to \Sigma^{-1}\mathcal{A}$ with right adjoint $Q_*$. Then the application of this functor to $M\in \mathcal{A}$ is some object $Q^*(M)$ in the localized category, which is up to isomorphism determined by its image $Q_* Q^*(M)$. The __localization map__ is the component of the unit of the adjunction (usually denoted by $i$, $j$ or $\iota$ in this setup) $\iota_M : M\to Q_* Q^*(M)$.

By [[Eilenberg-Watts theorem]] if $\mathcal{A}= {}_R Mod$ then 
$Q^*(M) = Q^*(R)\otimes_R M$. If the localization is a left [[Ore localization]] or [[commutative localization]] at a set $S\subset R$ then $Q^*(R) = S^{-1} R$, hence $Q^*(M) = S^{-1} R\otimes_R M$. In these cases there are also direct constructions of $Q^*(M)$ (not using to $Q^*(R)$) which give an isomorphic result, also denoted by $S^{-1}M$. 

Depending on an author or a context, we say that a (reflective) localization functor of category of modules is __flat__ if either $Q^*$ is also left [[exact functor]], or more strongly that the composed endofunctor $Q_* Q^*$ is exact. For example, [[Gabriel localization]] is flat in the first, weak sense, and left or right Ore localization is flat in the second, stronger, sense. 

## Related concepts and literature

* [[localization of a ring]], [[Ore localization]], [[Gabriel localization]], [[Cohn localization]]
* [[localization of a category]] (= localization functor)
* [[locally free module]]
* [[Z. Škoda]], _Noncommutative localization in noncommutative geometry_,  London Math. Society Lecture Note Series 330 ([pdf](http://www.maths.ed.ac.uk/~aar/books/nlat.pdf)), ed.  A. Ranicki; pp. 220--313, [math.QA/0403276](http://arxiv.org/abs/math.QA/0403276)

[[!redirects localizations of a module]]
[[!redirects localizations of modules]]
