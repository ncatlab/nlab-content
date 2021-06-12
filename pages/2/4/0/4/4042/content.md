ge
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Free monads
* table of contents
{: toc}

## Definition

A **free monad** is a [[free object]] relative to a [[forgetful functor]] whose domain is a [[category]] of [[monads]].

This general concept has many different specific incarnations, since there are potentially many different such forgetful functors.  Suppose $C$ is a [[category]], and write $Mnd(C)$ for the category whose objects are monads on $C$ and whose morphisms are natural transformations commuting with the monad structure maps; i.e. it is the category of [[monoids]] in the [[monoidal category]] of endofunctors with composition.  Then we have a string of forgetful functors:
$$ Mnd(C) \to PtEnd(C) \to End(C) \to [ob(C),C] $$ 
where $End(C)$ denotes the category of [[endofunctors]] of $C$, and $PtEnd(C)$ denotes the category of [[pointed endofunctors]], i.e. endofunctors $F$ equipped with a natural transformation $Id\to F$.  A *free monad* can then be considered as a free object relative to any one of these forgetful functors.

## Free finitary monads

In general, these forgetful functors cannot be expected to have [[left adjoints]], i.e. there will not be a [[free functor|"free monad functor"]], but individual objects can often be shown to generate free monads.  One general case in which this is true is when $C$ is [[locally presentable category|locally presentable]] and we consider monads and endofunctors which are [[accessible functor|accessible]], i.e. preserve sufficiently highly [[filtered colimits]].  Suppose for the sake of argument that $C$ is locally *finitely* presentable (the higher-ary case is analogous).  Then we can restrict the above string of forgetful functors to the [[finitary monads]], i.e. those preserving filtered colimits, to obtain:
$$ Mnd_f(C) \to PtEnd_f(C) \to End_f(C) \to [ob(C)_f,C] $$ 
where the subscript $f$ denotes restriction to finitary things, and $ob(C)_f$ is the set of [[compact objects]] of $C$.  In this case, all these forgetful functors do have left adjoints, and moreover at least the functors $Mnd_f(C) \to End_f(C)$ and $Mnd_f(C) \to [ob(C)_f,C]$ are monadic.  (This is shown in the papers cited below.)  The construction is by a convergent [[transfinite composition]].

For example, the left adjoint to $Mnd_f(C) \to End_f(C)$, shows that there exists a "free finitary monad" on any finitary endofunctor.  Note, though, that this does not *automatically* imply that the "free finitary monad" on a finitary endofunctor is also a "free monad" on that endofunctor, i.e. that as a free object it satisfies the requisite universal property relative to all objects of $Mnd(C)$, not merely those lying in $Mnd_f(C)$.  It is, however, true: free finitary monads are also free monads.

## Algebraically-free monads

We say that a monad $T$ is **algebraically-free** on an endofunctor $F$ if the category $T Alg_{mnd}$ of $T$-algebras (in the sense of [[algebras for a monad]]) is equivalent to the category $F Alg_{endo}$ of $F$-algebras (in the sense of [[algebras for an endofunctor]]). **N.B.**: Any such equivalence must be an isomorphism $T Alg_{mnd} \cong F Alg_{endo}$, because the underlying functors from the categories of algebras in each case are [[amnestic functor|amnestic]] [[isofibrations]]. See remarks at the article [[monadicity theorem]] on monadicity _vis-&#224;-vis_ strict monadicity. 

*A priori*, being algebraically free is different from being free.  However, one can show the following.

+-- {: .num_theorem}
###### Theorem
Any algebraically-free monad is free.
=--
+-- {: .proof}
###### Proof
First observe that for a (perhaps pointed) endofunctor $F$ and a monad $T$, to give a functor $T Alg_{mnd} \to F Alg_{endo}$ over $C$ is equivalent to giving a (pointed) transformation $F\to T$, and if $F$ is a monad then such a functor takes values in $F Alg_{mnd}$ iff the transformation $F\to T$ is a monad morphism.  Thus, if $F Alg_{endo} \cong T Alg_{mnd}$, then for any other monad $S$, (pointed) transformations $F\to S$ correspond to maps $S Alg_{mnd} \to F Alg_{endo} \cong T Alg_{mnd}$ and hence to monad morphisms $T\to S$, i.e. $T$ is free on $F$.
=--

+-- {: .num_theorem}
###### Theorem
If $C$ is [[locally small category|locally small]] and [[complete category|complete]], then any free monad is algebraically-free.
=--
+-- {: .proof}
###### Proof
For any object $x\in C$, the assumptions ensure that the [[codensity monad]] of $x$ exists.  This is the right [[Kan extension]] of $x\colon 1\to C$ along itself, which we write as $\langle x,x\rangle$.  The universal property of Kan extensions means that for any endofunctor $F$, to give a map $F x \to x$ (i.e. to make $x$ into an $F$-algebra) is the same as to give a natural transformation $F\to \langle x,x\rangle$.  Moreover, one can check that if $F$ is a pointed endofunctor (resp. a monad), then the map $F x \to x$ is a pointed (resp. monad) algebra iff the corresponding transformation $F\to \langle x,x\rangle$ is a morphism of pointed endofunctors (resp. of monads).  Therefore, if $T$ is the free monad on $F$, then applying its universal property in $Mnd(C)$ to the monad $\langle x,x\rangle$, we see that it is also algebraically-free.
=--

Notice that this second proof relies crucially on the fact that free monads have a universal property relative to a forgetful functor whose domain is all of $Mnd(C)$, not just some subcategory of finitary or accessible monads, since $\langle x,x\rangle$ will not in general be finitary or accessible.

## Constructions

Perhaps the most general [[set theory|set-theoretically]] based construction of (algebraically) free monads is the [[transfinite construction of free algebras]].  (In [[type theory]], it is natural to use instead [[higher inductive types]].)

## Examples

* The monadicity of the above adjunctions can be used to give [[presentation]]s of monads in terms of [[generators and relations]].  This has close connections with [[Lawvere theories]] and related ideas.

* Free monads on pointed endofunctors play an important role in the construction of cofibrantly generated [[algebraic weak factorization systems]].

## Related concepts

* The [[algebra over a monad]] over a free monad on an endofunctor is an _[[algebra over an endofunctor]]_.

## References

* [[Max Kelly]], ["A unified treatment of transfinite constructions for free algebras, free monoids, colimits, associated sheaves, and so on"](http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=4759448)

* [[Max Kelly]] and [[John Power]], ["Adjunctions whose counits are coequalizers, and presentations of finitary enriched monads"](http://www.sciencedirect.com/science/article/pii/0022404993900928)

* [[Steve Lack]], ["On the monadicity of finitary monads"](http://www.maths.usyd.edu.au/res/Catecomb/Lack/1997-29.html)

* [[Nicola Gambino]], [[Martin Hyland]], section 6 of _Wellfounded trees and dependent polynomial functors_. In Types for proofs and programs, volume 3085 of Lecture Notes in Comput. Sci., pages 210&#8211;225. Springer-Verlag, Berlin, 2004 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.98.4534))
 {#GambinoHyland04}


[[!redirects free monads]]
[[!redirects algebraically-free monad]]
[[!redirects algebraically-free monads]]
[[!redirects algebraically free monad]]
[[!redirects algebraically free monads]]
