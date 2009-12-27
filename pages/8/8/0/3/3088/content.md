The [[Kan complex]] definition of [[∞-groupoid]] may be [[internalization|internalized]] to more general categories. Namely:

*  We can define a [[simplicial object]] $X$ in any [[category]] $C$;
*  If $C$ has enough [[limits]], then we can define the object $X^{\Lambda^n_k}$ of $k$-horns of $n$-simplices of $X$ as a certain limit of the $X_m$ for $m \lt n$.
*  If we have a distinguished class of 'surjections', then we require that each morphism $X_n \to X^{\Lambda^n_k}$ is surjective.

In particular, if $C$ is a [[left exact category]] equipped with a [[Grothendieck pretopology]], then we define a __Kan object__ in $C$ to be a simplicial object in $C$ satisfying the Kan conditions (3), and define an __$\infty$-groupoid in $C$__ to be a Kan object in $C$.  (Recall that one way to define an ordinary $\infty$-groupoid is as a [[Kan complex]], that is a Kan object in [[Set]].)

+--{: .query}
[[Mike Shulman]]: I think in an "arbitrary category" it's not at all clear what the Kan conditions mean.  In $Set$ the Kan conditions can be interpreted by saying that the map of sets $X_n \to X^{\Lambda^n_k}$ is surjective for all $n$ and $k$, where $X^{\Lambda^n_k}$ is a certain limit of the $X_m$ for $m\lt n$---I think in fact it's the [[weighted limit]] of $X\colon \Delta^{op}\to Set$ weighted by $\Lambda^n_k \colon \Delta^{op}\to Set$.  If $C$ has enough limits (probably finite limits are enough), you can define $X^{\Lambda^n_k}$ for a simplicial object in $C$, but then you need to say what kind of "surjective" you want.  An [[epimorphism]]?  A [[regular epimorphism]]?  For sufficiently good behavior, I'd guess you'd want $C$ to be a [[regular category]] and ask the maps $X_n \to X^{\Lambda^n_k}$ to be regular epimorphisms.

Alternately, you could ask that $X$ be "representably" a Kan complex, i.e. for each $Z\in C$ the simplicial set $C(Z,X_\bullet)$ is a Kan complex.  But I think this is just the same as asking each $X_n \to X^{\Lambda^n_k}$ to be [[split epimorphism|split epic]], which is probably stronger than you want.

[[Domenico Fiorenza]]: I agree: an "arbitray category" makes no sense, just as it would make no sense talking of group objects in an arbitrary category. So two things need to be specified. First we need to say what is a [[horn]] for a simplicial object in $C$, and here I agree that it could be defined as the weighted limit of $X\colon \Delta^{op}\to Set$ weighted by $\Lambda^n_k \colon \Delta^{op}\to Set$. So the highest generality one can speak of horns is tautologically a "category with horns", i.e., a category where precisely these limits exist. I find this, however, an almost useless level of generality, and asking for all finite limits seems a better idea. Next one should specify what the Kan condition is, namely what one requires from the morphisms $X_n \to X^{\Lambda^n_k}$. Only hints here are that for [[Set]] one asks surjectivity and for [[Diff]] one asks the morphism to be a surjective submersion (at least it is so at the [[Kan complex]] entry). So a possibility would be to consider a [[pretopology]] on $C$ and ask $X_n \to X^{\Lambda^n_k}$ to be a cover. 

_Toby_:  That sounds right, so I put it in.  But we still need to check that finite limits and a Grothendieck pretopology are sufficient for the entire construction, yes?  (So if anybody moves or removes this query box, keep the previous sentence up here.)
=--

A classical example consists of the __topological $\infty$-groupoids__. The [[nerve]] construction makes a topological $\infty$-groupoid from a [[topological groupoid]]. This is actually a characterization of topological groupoids among topological categories.

In particular, if $G$ is a [[topological group]], then $N(\mathbf{B}G)$ is a topological $\infty$-groupoid. This is relevant to the construction of the [[classifying spaces]] for continuous [[principal bundles]].

Another classical example consists of the [[∞-Lie groupoids]].


[[!redirects Internal infinity-groupoid]]
[[!redirects Internal ∞-groupoid]]
[[!redirects internal ∞-groupoid]]
[[!redirects infinity-groupoid object]]
[[!redirects ∞-groupoid object]]
