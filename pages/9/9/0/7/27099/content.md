[[!redirects category with extra structure]]
[[!redirects category with extra structure]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[subcategory]] $\mathcal{D}$ of a [[category]] $\mathcal{C}$ can be defined as a subset $\mathrm{Ob}_D$ of $\mathrm{Ob}_\mathcal{C}$ and for all $X,Y \in \mathrm{Ob}_\mathcal{C}$, a subset $\mathcal{D}[X,Y]$ such that:

* for every $X \in \mathrm{Ob}_\mathcal{D}$, we have $\mathrm{id}_X \in \mathcal{D}[X,X]$,
* for all objects $X,Y,Z \in \mathrm{Ob}_\mathcal{D}$ and for all morphisms $f \in \mathcal{D}[X,Y]$, $g \in \mathcal{D}[Y,Z]$, we have $f;g \in \mathcal{D}[X,Z]$.

The structure of category on $\mathcal{C}$ then induces a structure of category on $\mathcal{D}$.

A structure of category can also be induced on a set of objects and morphisms which will not form a subcategory of the base category. The idea is that instead of selecting subsets of [[objects]] and [[morphisms]], we add some structure on the objects. We can add different structures to the same starting object, ending up with different objects with extra structure. The set of morphisms between two objects with extra structure can be seen as a subset of the morphisms between the underling objects in the initial category. We try to give an abstract account of how a structure of category can be induced from the original category on candidate objects with extra structure and morphisms between them. We don't explicitly introduce extra structure but the framework is meant to abstract what's going on in purely categorical terms. 

Given a category with extra structure on objects $\mathcal{D}$ with base category $\mathcal{C}$, we obtain a faitfhful [[forgetful functor]] $U:\mathcal{D} \rightarrow \mathcal{C}$. We can't really see $\mathcal{D}$ as a subcategory of $\mathcal{C}$ since the [[image]] of a functor is properly defined only if this functor is [[injective-on-objects functor|injective on objects]]. And most of the time $U$ will not be injective on objects. However, we can use the [[full image]] of $U$. The full image of $U$ is not properly a subcategory of $\mathcal{D}$ since the morphisms live in $\mathcal{D}$ but the objects live in $\mathcal{C}$. This full image can be  intuitively identified with the category $\mathcal{D}$ here. This is because although the objects of $\mathcal{D}$ can't be reduced to objects of $\mathcal{C}$, the morphisms of $\mathcal{D}$ can be seen as morphisms of $\mathcal{C}$.

## Definition and proposition

Let $\mathcal{C}$ be a category. We call *category with extra structure on objects* $\mathcal{D}$ with base category $\mathcal{C}$ the data of:

* a set $\mathrm{Ob}_\mathcal{D}$ together with a function
$$
U:\mathrm{Ob}_\mathcal{D} \rightarrow \mathrm{Ob}_\mathcal{C},
$$
* for all $X,Y \in \mathrm{Ob}_\mathcal{D}$, a set $\mathcal{D}[X,Y]$,
* for all $X,Y \in \mathrm{Ob}_\mathcal{D}$, an injection
$$
U_{X,Y}:\mathcal{D}[X,Y] \rightarrow \mathcal{C}[U(X),U(Y)],
$$

such that:

* $\mathrm{id}_{U(X)} \in U_{X,X}(\mathcal{D}[X,X])$ for every $X \in \mathrm{Ob}_\mathcal{D}$,
* $f_{X,Y}(u);f_{Y,Z}(v) \in U_{X,Z}(\mathcal{D}[X,Z])$ for all $X,Y,Z \in \mathrm{Ob}_\mathcal{D}$, $u \in \mathcal{D}[X,Y]$, $v \in \mathcal{D}[Y,Z]$.

\begin{proposition}
The set $\mathrm{Ob}_\mathcal{D}$ together with the sets $\mathcal{D}[X,Y]$ for all $X,Y \in \mathrm{Ob}_\mathcal{D}$ form a category $\mathcal{D}$ with identities and composition defined as follows:

* $u;v\,:= U_{X,Z}^{-1}(U_{X,Y}(u);U_{Y,Z}(v))$ for all $X,Y,Z \in \mathrm{Ob}_\mathcal{D}$, $u \in \mathcal{D}[X,Y]$ and $v \in \mathcal{D}[Y,Z]$,
* $\mathrm{id}_X=U_{X,X}^{-1}(\mathrm{id}_{U(X)})$.

Moreover the functions $U$ and $U_{X,Y}$ for all $X,Y \in \mathrm{Ob}_\mathcal{D}$ define a faithful functor $U$ from $\mathcal{D}$ to $\mathcal{C}$.
\end{proposition} 


