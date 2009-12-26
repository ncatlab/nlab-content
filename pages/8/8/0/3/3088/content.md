The [[Kan complex]] definition of [[∞-groupoid]] may be immediately [[internalization|internalized]] to an arbitrary category. Namely, if $C$ is a [[category]], an __$\infty$-$C$-groupoid__ (or __$\infty$-groupoid in $C$__) is a [[Kan object]] in $C$, i.e., a [[simplicial object]] in $C$ which satisfies the Kan conditions. In this sense, an $\infty$-groupoid is a $\infty$-$Set$-groupoid (an $\infty$-groupoid in [[Set]]). 

+--{: .query}
[[Mike Shulman]]: I think in an "arbitrary category" it's not at all clear what the Kan conditions mean.  In $Set$ the Kan conditions can be interpreted by saying that the map of sets $X_n \to X^{\Lambda^n_k}$ is surjective for all $n$ and $k$, where $X^{\Lambda^n_k}$ is a certain limit of the $X_m$ for $m\lt n$---I think in fact it's the [[weighted limit]] of $X\colon \Delta^{op}\to Set$ weighted by $\Lambda^n_k \colon \Delta^{op}\to Set$.  If $C$ has enough limits (probably finite limits are enough), you can define $X^{\Lambda^n_k}$ for a simplicial object in $C$, but then you need to say what kind of "surjective" you want.  An [[epimorphism]]?  A [[regular epimorphism]]?  For sufficiently good behavior, I'd guess you'd want $C$ to be a [[regular category]] and ask the maps $X_n \to X^{\Lambda^n_k}$ to be regular epimorphisms.

Alternately, you could ask that $X$ be "representably" a Kan complex, i.e. for each $Z\in C$ the simplicial set $C(Z,X_\bullet)$ is a Kan complex.  But I think this is just the same as asking each $X_n \to X^{\Lambda^n_k}$ to be [[split epimorphism|split epic]], which is probably stronger than you want.

[[Domenico Fiorenza]]: I agree: an "arbitray category" makes no sense, just as it would make no sense talking of group objects in an arbitrary category. So two things need to be specified. First we need to say what is a [[horn]] for a simplicial object in $C$, and here I agree that it could be defined as the weighted limit of $X\colon \Delta^{op}\to Set$ weighted by $\Lambda^n_k \colon \Delta^{op}\to Set$. So the highest generality one can speak of horns is tautologically a "category with horns", i.e., a category where precisely these limits exist. I find this, however, an almost useless level of generality, and asking for all finite limits seems a better idea. Next one should specify what the Kan condition is, namely what one requires from the morphisms $X_n \to X^{\Lambda^n_k}$. Only hints here are that for [[Set]] one asks surjectivity and for [[Diff]] one asks the morphism to be a surjective submersion (at least it is so at the [[Kan complex]] entry). So a possibility would be to consider a [[pretopology]] on $C$ and ask $X_n \to X^{\Lambda^n_k}$ to be a cover. 
=--

A classical example consists of the __topological $\infty$-groupoids__. The [[nerve]] construction makes a topological $\infty$-groupoid from a [[topological groupoid]]. This is actually a characterization of topological groupoids among topological categories.

In particular, if $G$ is a [[topological group]], then $N(\mathbf{B}G)$ is a topological $\infty$-groupoid. This is relevant to the construction of the [[classifying space]]s for continuous [[principal bundle]]s.

Another classical example consists of the [[∞-Lie groupoids]].


[[!redirects Internal infinity-groupoid]]
[[!redirects Internal ∞-groupoid]]
[[!redirects internal ∞-groupoid]]
[[!redirects infinity-groupoid object]]
[[!redirects ∞-groupoid object]]
