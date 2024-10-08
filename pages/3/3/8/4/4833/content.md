# Suitable monads
* table of contents
{: toc}

## Idea

Given a [[cartesian monad]] $T$ on a [[locally cartesian category]] $C$ one can define a generalized graph and a [[generalized multicategory]] of type $T$ ($T$-multicategory). We want to impose a "suitability" condition on $C$ and $T$ which would ensure that one can talk about a free $T$-multicategory. In other words, the forgetful functor 
$$
U : (C,T)\text{-}Multicat \to (C,T)\text{-}Graph
$$ 
from $T$-multicategories to $T$-graphs has a left adjoint $F$; this adjunction induces hence a monad $T^+ = (UF, U\epsilon F,\eta)$ on $C^+ := (C,T)Graph$. Moreover one wants to be able to build new cartesian monads iteratively, namely to ensure the same suitability conditions on the $T^+$, $T^{++}$ and so on. This is used for example in some of the possible inductive definitions of [[opetopes]]. 


## Definition

A *category* $C$ is **suitable** (in the sense of [[Tom Leinster]]) if 

* $C$ is cartesian
* $C$ has finite [[disjoint coproducts]], which are also stable under pullback
* $C$ has colimits of all *nested sequences* (i.e. $\omega$-chains of [[monomorphisms]]); they commute with pullback and have monic injections (coprojections)

A *monad* $T = (T,\mu,\eta)$ is **suitable** if 

* $(T,\mu,\eta)$ is cartesian
* its underlying endofunctor $T$ preserves colimits of nested sequences


## Properties

Any [[presheaf topos]] is suitable. Any [[finitary monad|finitary]] [[cartesian monad]] is suitable. 

The forgetful functor from the category of $T$-multicategories to the category of $T$-graphs has a left adjoint and the adjunction is monadic; the category of $T$-graphs is then suitable and the induced monad is suitable.


## Literature 

Section 6.5 and appendix D in

* [[Tom Leinster]], _Higher operads, higher categories_, London Math. Soc. Lec. Note Series __298__, [math.CT/0305049](http://arxiv.org/abs/math.CT/0305049)
* [[Tom Leinster]], _Generalized enrichment for categories and multicategories_,  [math.CT/9901139](http://arxiv.org/abs/math.CT/9901139)

See also the appendix of:

* Brandon Shapiro, _Enrichment of Algebraic Higher Categories_, [arXiv:2205.12235](https://arxiv.org/abs/2205.12235) (2022).


[[!redirects suitable monads]]
