We give two constructions of the simplicial localization of a [[homotopical category]].  

We first need the following preparations:

Let $\mathbf{T}$ be the [[zigzag category]].  We define the _categorical realization_ of a zigzag $t=(n,t_+,t_-)$ to be the category $[t]$ generated freely by the following [[quiver]] data:

* $[t]$ has $n+1$ vertices $t_0,...,t_n$
* If $i\in t_+$, there is an edge $g_i:t_{i-1}\to t_i$
* If $i\in t_-$, there is an edge $g_i:t_i\to t_{i-1}$

Let $C$ be a [[homotopical category]] with class of weak equivalences $W$.  Consider the functor category $Hom_{Cat}([t],C)$.  We define the category of _restricted_ $t$-zigzags $C^{t}$ to be the subcategory whose objects are zigzags $F$ such that all maps $F(t_i)\to F(t_{i-1})\in W$, and where morphisms are given by object-wise weak equivalences (natural weak equivalences) such that the maps on the initial and terminal vertices are identities.  Finally, we define $C^t(X,Y)$ to be the full subcategory of $C^t$ spanned by those objects $F$ such that $F(t_0)=X$ and $F(t_n=Y)$.  

Let $f:t\to t'$ be a morphism of $\mathbf{T}$.  Then we define the functor $f_*:C^t(X,Y)\to C^{t'}(X,Y)$ to be the functor sending a zigzag $F:[t]\to C$ with connecting maps $g_i$ lying between $t_{i-1}$ and $t_i$ (not necessarily $t_{i-1}\to t_i$) to the zigzag $f_*F:[t']\to C$ with connecting maps $h_j$ defined to be the ordered composite of the maps $g_i$ such that $i\in f^{-1}(j)$ (Note: There should be a better combinatorial way to precisely specify this, but I'm having trouble doing so).  Notice that if $f^{-1}(j)$ is empty, this procedure yields the identity map.  On morphisms, everything remains well-defined by the naturality condition (implying that the diagrams do in fact commute).   This proves that the assignment $C^{(t)}(X,Y):\mathbf{T} \to Cat$ is functorial in $t$.  

Notice that this is not actually functorial in $X$ and $Y$, but for a map $Z\to X$, we can give a functor $C^t(X,Y)\to C^{1\vee t}(Z,Y)$.  Similarly, for a map $Y\to Z$, we can give a map $C^{t}(X,Y)\to C^{t \vee 1}(X,Z)$.  This is a special case of concatenation, which we will describe as follows:

We may concatenate two combinatorial zigzags $t=(n,t_+,t_-)$ and $t'=(m,t'_+,t'_-)$ in the obvious way by taking $t\vee t'$ to be the combinatorial zigzag $(n+m, t_+ \cup n(t'_+), t_- \cup n(t'_-))$ where $n(S):=\{n+i: i\in S\}$ is the map adding $n$ to each index.  This is clearly functorial in both coordinates and defines a monoidal product $\vee:\mathbf{T}\times \mathbf{T}\to \mathbf{T}$.  

We will lift this to a functor $\vee^{t,t'}_{XYZ}:C^t(X,Y)\times C^{t'}(Y,Z)\to C^{t\vee t'}(X,Z)$.  We send a pair of zigzags to their concatenation in the obvious way.  On morphisms, we concatenate natural transformation diagrams, the result of which remains natural by the hammock-shape of our natural transformation diagrams (see below), so $\vee^{t,t'}_{XYZ}$ is a functor in both coordinates.  

$$\begin{matrix}
&&A_1&\to&A_2&\leftarrow&A_3&\to&\ldots&\to &A_{n-3}&\leftarrow &A_{n-2}&\to& A_{n-1}&&\\
&\nearrow&\downarrow&&\downarrow&&\downarrow&&&&\downarrow&&\downarrow&&\downarrow&\searrow&\\
X&&\downarrow&&\downarrow&&\downarrow&&&&\downarrow&&\downarrow&&\downarrow&&Y\\
&\searrow&\downarrow&&\downarrow&&\downarrow&&&&\downarrow&&\downarrow&&\downarrow&\nearrow&\\
&&B_1&\to&B_2&\leftarrow&B_3&\to&\ldots&\to &B_{n-3}&\leftarrow &B_{n-2}&\to& B_{n-1}&&\end{matrix}$$

(Note that this picture is technically hiding the identity morphisms $X\to X$ and $Y\to Y$.  We omit them to show the hammock-shape, as noted below).

We note that we must define everything pointwise for the moment, but it's reasonable expect all of this data to lift to an actual composition functor in the colimit over $\mathbf{T}$, perhaps after some effort.  

With this data in hand, we may proceed to actual constructions of the simplicial categories that we want.

Before that, a short note on terminology:  Traditionally, only the second construction is called the hammock localization, but this name comes from the shape of a natural transformation between two $t$-zigzags with the same initial and terminal vertices (notice how much the figure above looks like a hammock!), but as we will see, this features in both constructions.  We could say that both constructions are "hammock localizations", and indeed, they produce weakly equivalent results.


####Simplicial localization via the Grothendieck Construction####

By the [[Grothendieck construction]], we may present the functor $C^t(X,Y):\mathbf{T}\to Cat$ as a [[fibered category]] $GrC^\mathbf{T}(X,Y)$ over $\mathbf{T}$.  

We describe the resulting category $GrC^\mathbf{T}(X,Y)$ explicitly as follows:

*The objects are pairs $(t,F)$ with $t\in \mathbf{T}$ and $F\in C^t(X,Y)
*The morphisms are pairs $(f,g):(t,F)\to (t',G)$ where $f:t\to t'$ and $g:f_*F\to G$.
*Composition is given by the rule $(f',g')\circ (f,g)=(f'\circ f,g'\circ f_* g)$.

In the sequel, we will construct the strict 2-category $GrC$, called the Grothendieck enrichment with the same objects as $C$ and with morphism categories $GrC^\mathbf{T}(X,Y)$. 

The first order of business is to show that the $\vee^{t,t'}_{XYZ}$ assemble first to a functor $\vee_{XYZ}:GrC^\mathbf{T}(X,Y)\times GrC^\mathbf{T}(Y,Z)\to GrC^\mathbf{T}(X,Z)$.  After that, we must show that all $\vee_{XYZ}$ assemble to an actual law of composition.

We define the functor $\vee_{XYZ}:GrC^\mathbf{T}(X,Y)\times GrC^\mathbf{T}(Y,Z)\to GrC^\mathbf{T}(X,Z)$ as follows: On objects (suppressing subscripts), we have $(t,F)\vee (t',F'):= (t\vee t', F\vee^{t,t'} F').  This is clearly functorial by way of the results from our earlier preparations. 

We now define the strict $2$-category GrC by specifying the following data:

*The objects are simply the objects of $C$
*The hom-categories are given by $GrC^\mathbf{T}(X,Y)$
*The identity morphism $id_X\in GrC^\mathbf{T}(X,X)$ is the unique empty zigzag.  
*We define the law of composition to be $\vee$.  

It's clear from the definitions that $\vee$ is associative and that $id_X\vee F=F$ whenever the composition makes sense.  Then $GrC$ is a $2$-category.

We define the categorical nerve: $N:2\text{-}Cat\to Set_\Delta\text{-}Cat$ to be the canonical functor arising from the ordinary nerve.  That is, $N$ is the identity on objects, and sends $GrC^\mathbf{T}(X,Y)\to \nu(GrC^\mathbf{T}(X,Y))$ where $\nu$ denotes the ordinary nerve.  This is well defined since $\nu$ is a right adjoint and therefore commutes with products.  

We call the simplicial category $N(GrC)$ the simplicial localization of $C$. 

**Theorem**: The categorical nerve $N(GrC)$ sending objects to objects and hom-categories to simplicial sets $N(GrC^\mathbf{T}(X,Y))$ equips $N(GrC)$ with the structure of a simplicial category.  Further, the morphisms of the homotopy category of this simplicial category coincide with those of the homotopy category arising from the ordinary construction using equivalence relations.  That is, $Ho_C(X,Y)\cong \pi_0 (N(GrC(X,Y)))$ naturally in $X$ and $Y$, where $\pi_0(-):=Hom_{Ho(SSet)}(Ho(\Delta^0), Ho(-))$.  

####Hammock Localization####

