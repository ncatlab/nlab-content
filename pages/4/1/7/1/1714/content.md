In an $n$-[[n-category|category]], or most generally an $\infty$-[[infinity-category|category]], there are many levels of [[morphism]], parametrised by [[natural number]]s.  Those at level $j$ are called __$j$-morphisms__ or __$j$-cells__.

In a [[geometric model of higher categories]], the $j$-morphisms are literally $j$-cells in the sense of a [[simplicial set]].  In any case, all models of higher categories have them.

Every $j$-morphism $f$ has a $(j-1)$-morphism $\sigma f$ as its [[source]] and a $(j-1)$-morphism $\tau f$ as its [[target]].  The source $(j-2)$-morphisms $\sigma \sigma f$ and $\sigma \tau f$ must be the same, as must the target $(j-2)$-morphisms $\tau \sigma f$ and $\tau \tau f$.

A $1$-morphism may simply be called a [[morphism]]; a $0$-morphism is an [[object]].

For the purposes of [[negative thinking]], it may be useful to recognise that every $\infty$-category has a $(-1)$-morphism, which is the source and target of every object.  (In the geometric picture, this comes is the $(-1)$-simplex of an [[augmented simplicial set]].)

+-- {: .query}
(non-empty? -David R)

Reply from Toby:  I think every.  Up to equivalence, a $j$-morphism in $C$ is given by a functor from the oriented $j$-simplex to $C$.  As the $(-1)$-simplex is empty, there is a unique such functor for every $C$; thus every $C$ has a unique $(-1)$-morphism.

Also note that every $j$-morphism has $j + 1$ identity $(j+1)$-morphisms, which just happen to all be the same (which can be made part of the [[Eckmann-Hilton argument]]).  Thus, the $(-1)$-morphism has $0$ identity $0$-morphisms, so we don\'t need any object.  (This confused me once.)
=--


[[!redirects k-morphism]]
[[!redirects n-morphism]]
[[!redirects m-morphism]]
[[!redirects r-morphism]]
[[!redirects s-morphism]]