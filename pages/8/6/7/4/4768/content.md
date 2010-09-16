We give two constructions of the simplicial localization of a [[homotopical category]].  

We first need the following preparations:

Let $\mathbf{T}$ be the [[zigzag category]].  We define the _categorical realization_ of a zigzag $t=(n,t_+,t_-)$ to be the category $[t]$ generated freely by the following [[quiver]] data:

* $[t]$ has $n+1$ vertices $t_0,...,t_n$
* If $i\in t_+$, there is an edge $g_i:t_{i-1}\to t_i$
* If $i\in t_-$, there is an edge $g_i:t_i\to t_{i-1}$

Let $C$ be a [[homotopical category]] with class of weak equivalences $W$.  Consider the functor category $Hom_{Cat}([t],C)$.  We define the category of _restricted_ $t$-zigzags $C^{t}$ to be the subcategory whose objects are zigzags $F$ such that all maps $F(t_i)\to F(t_{i-1})\in W$, and where morphisms are given by object-wise weak equivalences (natural weak equivalences).  Finally, we define $C^t(X,Y)$ to be the full subcategory of $C^t$ spanned by those objects $F$ such that $F(t_0)=X$ and $F(t_n=Y)$.  

Let $f:t\to t'$ be a morphism of $\mathbf{T}$.  Then we define the functor $f_*:C^t(X,Y)\to C^{t'}(X,Y)$ to be the functor sending a zigzag $F:[t]\to C$ with connecting maps $g_i$ lying between $t_{i-1}$ and $t_i$ (not necessarily $t_{i-1}\to t_i$) to the zigzag $f_*F:[t']\to C$ with connecting maps $h_j$ such that when $j=fi$ for some $i\in t$, $h_j=f_j$ and if not, let $h_j$ be the appropriate identity map.  It's clear that the assignment $C^{(-)}(X,Y):\mathbf{T} \to Cat$ is functorial.  With this data in hand, we may proceed to actual constructions of the simplicial categories that we want.

Before that, a short note on terminology:  Traditionally, only the second construction is called the hammock localization, but this name comes from the shape of a natural transformation between two $t$-zigzags with the same initial and terminal vertices (see figure), but as we will see, this features in both constructions.  We could say that both constructions are "hammock localizations", and indeed, they produce weakly equivalent results.

$$\begin{matrix}
&&A_1&\to&A_2&\leftarrow&A_3&\to&\ldots&\to &A_{n-3}&\leftarrow &A_{n-2}&\to& A_{n-1}&&\\
&\nearrow&\downarrow&&\downarrow&&\downarrow&&&&\downarrow&&\downarrow&&\downarrow&\searrow&\\
X&&\downarrow&&\downarrow&&\downarrow&&&&\downarrow&&\downarrow&&\downarrow&&Y\\
&\searrow&\downarrow&&\downarrow&&\downarrow&&&&\downarrow&&\downarrow&&\downarrow&\nearrow&\\
&&B_1&\to&B_2&\leftarrow&B_3&\to&\ldots&\to &B_{n-3}&\leftarrow &B_{n-2}&\to& B_{n-1}&&\end{matrix}$$

(Figure: See, it looks like a hammock!  Note that the downward arrows should in fact be single arrows, but I don't know how to TeX that without real commutative diagram software.)


####Simplicial localization via the Grothendieck Construction####

Then by the [[Grothendieck construction]], we may present this functor as a [[fibered category]] $GrC^\mathbf{T}(X,Y)$ over $\mathbf{T}$.  We will define $GrC$ to be the strict 2-category with the same objects as $C$ and with morphism categories $GrC^\mathbf{T}(X,Y)$.  

(Editor's note: the composition functor is induced by concatenation of zigzags (which sends a $t$-zigzag $X\to Y$ and a $t'$-zigzag $Y\to Z$ to a $t''$-zigzag $X\to Z$ where $t''$ is given by concatenating $t$ and $t'$ end to end), but I'm not sure how to explicitly induce this on the Grothendieck category)

**Theorem**: The categorical nerve $N(GrC)$ sending objects to objects and hom-categories to simplicial sets $N(GrC^\mathbf{T}(X,Y))$ equips $N(GrC)$ with the structure of a simplicial category.  Further, the morphisms of the homotopy category of this simplicial category coincide with those of the homotopy category arising from the ordinary construction using equivalence relations.  That is, $Ho_C(X,Y)\cong \pi_0 (N(GrC(X,Y)))$ naturally in $X$ and $Y$, where $\pi_0(-):=Hom_{Ho(SSet)}(Ho(\Delta^0), Ho(-))$.  

####Hammock Localization####

