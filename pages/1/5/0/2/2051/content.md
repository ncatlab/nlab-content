A discrete [[group]] $G$ is a __Hopfian group__ if every [[surjection|surjective]] [[endomorphism]] $\phi : G\to G$ is an [[isomorphism]]. Dually, a discrete group is called __coHopfian__ if any [[injection|injective]] endomorphism of $G$ is an isomorphism.

As the [[epimorphism]]s and [[monomorphism]]s in [[Grp]] are precisely the surjections and injections (see [[epimorphisms of groups are surjective]]), the definition generalises immediately to that of a [[Hopfian object]] in any [[category]]. In other words, we *could* define an object $X$ to be Hopfian if every epic endomorphism is an isomorphism (see [[Dedekind finite object]]). 

Whatever that generalization is worth, much of the literature (such as [V](#V) below) adopts the more concrete notion: given a [[concrete category]] $U: C \to Set$ with $U$ a [[faithful functor]], say that an object $X$ of $C$ is *Hopfian* if every morphism $\phi: X \to X$ in $C$ with $U(\phi)$ surjective is an isomorphism. (In the presence of faithfulness of $U$, $\phi$ is epic if $U(\phi)$ is surjective.) For [[monadic functors]] $U: C \to Set$, this surjectivity assumption is the same as the assumption that $\phi$ is a [[regular epimorphism]]. Of course there is a dual notion of being co-Hopfian; here the hypothesis that $U(\phi)$ is injective frequently coincides simply with $\phi$ being monic -- certainly that is true if $U$ preserves [[finite limits]] (which is frequently the case "in nature"). 

Clearly all [[finite group]]s are both Hopfian and coHopfian.
Using Nielsen's method, one can show that every finitely generated [[free group]] and the union of any ascending chain of such free groups (for example, $\mathbb{Q}$) are Hopfian. It is also known that every [[torsion-free group|torsion-free]] [[hyperbolic group]] is Hopfian.

## References 

* K. Varadarajan, _Hopfian and Co-Hopfian Objects_, Publicacions Matem&#225;tiques, Vol. 36 (1992), 293-317. ([web](http://www.raco.cat/index.php/PublicacionsMatematiques/article/viewFile/37700/37574)) 
 {#V} 


[[!redirects Hopf group]]
[[!redirects coHopfian group]]
[[!redirects co-Hopfian group]]