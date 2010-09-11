
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[object]]

* [[morphism]]

* [[2-morphism]]

* [[3-morphism]]

* **k-morphism**

***


# Higher morphisms ($k$-morphisms)
* table of contents
{: toc}

## Idea

In an $n$-[[n-category|category]], or most generally an $\infty$-[[infinity-category|category]], there are many levels of [[morphism]], parametrised by [[natural numbers]].  Those at level $k$ are called __$k$-morphisms__ or __$k$-cells__.

* a 0-morphism is an [[object]]

* a 1-morphism is a [[morphism]]

* next are [[2-morphism]]s

* and so on


## Definition

All notions of higher category have $k$-morphisms, but the [[geometric shape for higher categories|shapes]] may depend on the model (or theory) employed. 

For a simplicially based [[geometric model of higher categories]], i.e., simplicial sets subject to some filler conditions, the $k$-morphisms are literally $k$-cells in the sense of a [[simplicial set]]. This applies for example to [[quasi-category|quasi-categories]], weak $n$-categories in the sense of Street, and the weak complicial sets of Verity. In other geometric models, based not on simplices but on other shapes such as [[opetope|opetopes]] (Baez-Dolan), [[multitope|multitopes]] (Hermida-Makkai-Power), or $n$-[[Theta category|disks]] (Joyal), a higher category is a presheaf 

$$X: Shapes^{op} \to Set$$ 

again subject to some filler conditions, and in each case $k$-morphisms are elements of $X(\sigma)$ where $\sigma$ is a shape of dimension $k$. Still other shapes (e.g., [[cubical category|cubes]]) are possible (see also [[n-fold category]]). 

Many notions of algebraic higher category, such as those due to Batanin, Leinster, Penon, and Trimble, are algebras over certain monads acting on globular sets (such as those induced by [[globular operad|globular operads]]), so that each higher category $X$ has an underlying [[globular set]] $U(X)$. In that case, the $k$-morphisms are the $k$-cells of $U(X)$. In such globularly based definitions, every $k$-morphism $f$ has a $(k-1)$-morphism $\sigma f$ as its [[source]] and a $(k-1)$-morphism $\tau f$ as its [[target]], and the source $(k-2)$-morphisms $\sigma \sigma f$ and $\sigma \tau f$ must be the same, as must the target $(k-2)$-morphisms $\tau \sigma f$ and $\tau \tau f$.

A $1$-morphism may simply be called a [[morphism]]; a $0$-morphism is an [[object]].

For the purposes of [[negative thinking]], it may be useful to recognise that every $\infty$-category has a $(-1)$-morphism, which is the source and target of every object.  (In the geometric picture, this comes as the $(-1)$-simplex of an [[augmented simplicial set]].)

+-- {: .query}
>every (non-empty? -David R) $\infty$-category

I think every.  Up to equivalence, a $k$-morphism in $C$ is given by a functor from the oriented $k$-simplex to $C$.  As the $(-1)$-simplex is empty, there is a unique such functor for every $C$; thus every $C$ has a unique $(-1)$-morphism.

Also note that every $k$-morphism has $k + 1$ identity $(k+1)$-morphisms, which just happen to all be the same (which can be made a result of the [[Eckmann–Hilton argument]]).  Thus, the $(-1)$-morphism has $0$ identity $0$-morphisms, so we don\'t need any object.  (This confused me once.)

---[[Toby Bartels]]
=--


[[!redirects higher morphism]]
[[!redirects higher morphisms]]
[[!redirects k-morphism]]
[[!redirects k-morphisms]]
[[!redirects j-morphism]]
[[!redirects j-morphisms]]
[[!redirects n-morphism]]
[[!redirects n-morphisms]]
[[!redirects m-morphism]]
[[!redirects m-morphisms]]
[[!redirects r-morphism]]
[[!redirects r-morphisms]]
[[!redirects s-morphism]]
[[!redirects s-morphisms]]
