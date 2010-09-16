We give two constructions of the simplicial localization of a [[homotopical category]].  

We first need the following preparations:

Let $\mathbf{T}$ be the [[zigzag category]].  We define the _categorical realization_ of a zigzag $t=(n,t_+,t_-)$ to be the category $[t]$ generated freely by the following [[quiver]] data:

* $[t]$ has $n+1$ vertices $t_0,...,t_n$
* If $i\in t_+$, there is an edge $t_{i-1}\to t_i$
* If $i\in t_-$, there is an edge $t_i\to t_{i-1}$

Let $C$ be a [[homotopical category]] with class of weak equivalences $W$.  Consider the functor category $Hom_{Cat}([t],C)$.  We define the category of _restricted_ $t$-zigzags $C^{t}$ to be the subcategory whose objects are zigzags $F$ such that all maps $F(t_i)\to F(t_{i-1})\in W$, and where morphisms are given by object-wise weak equivalences.  Finally, we define $C^t(X,Y)$ to be the full subcategory of $C^t$ spanned by those objects $F$ such that $F(t_0)=X$ and $F(t_n=Y)$.  

Let $f:t\to t'$ be a morphism of $\mathbf{T}$.  Then we define the functor $f_*:C^t(X,Y)\to C^{t'}(X,Y)$ to be the functor sending a zigzag $F:[t]\to C$ with connecting maps $g_i$ lying between $t_{i-1}$ and $t_i$ (not necessarily $t_{i-1}\to t_i$) to the zigzag $f_*F:[t']\to C$ with connecting maps $h_j$ such that when $j=fi$ for some $i\in t$, $h_j=f_j$ and if not, let $h_j$ be the appropriate identity map.

It's clear that the assignment $C^{(-)}(X,Y):\mathbf{T} \to Cat$ is functorial.  Then by the [[Grothendieck construction]], we may present this functor as a [[fibered category]] $GrC^\mathbf{T}(X,Y)$ over $\mathbf{T}$.  We will define $GrC$ to be the strict 2-category with the same objects as $C$ and with morphism categories $GrC^\mathbf{T}(X,Y)$.  

**Theorem**: The nerve $N(GrC)$ sending objects to objects and hom-categories to simplicial sets $N(GrC^\mathbf{T}(X,Y))$ equips $N(GrC)$ with the structure of a simplicial category.  Further, the homotopy category of this simplicial category coincides with the classical homotopy category.  That is, $Ho_C(X,Y)\cong \pi_0 (N(GrC))$