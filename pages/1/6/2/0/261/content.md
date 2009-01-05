#Definition#

A **simplicial set**  is a [[presheaf]] on the [[simplicial category]] $\Delta$.

#Remarks#

* The definition is to be understood from the point of view of [[space and quantity]]: a **simplicial set** is a space characterized by the fact that and how it may be _probed_ by mapping standard simplices into it: the set $S_n$ assigned by a simplicial set to the standard $n$-simplex $[n]$ is the set of $n$-simplicies in this space, hence the way of mapping a standard $n$-simplex into this spaces.

* Simplicial sets generalize the idea of [[simplicial complex]]: a simplicial set can be thought of as something consisting of a set of $n$-simplices for all $n \in \mathbb{N}$ together with face and degeneracy functions. More precisely, if $X$ is a simplicial set, we write $X_n$ to denote the set of $n$-simplices. The **face** maps (also called **boundary** maps) are functions $\delta_i : X_n \rightarrow X_{n-1}$ for each $0\leq i \leq n$, which associate to each $n$-simplex one of its $n+1$ faces, themselves $n-1$-simplices. The **degeneracy** maps are functions $\sigma_i : X_n \rightarrow X_{n+1}$ for each $0\leq i \leq n$, which allow one to regard and $n$-simplex as a degenerate $n+1$-simplex. 

* The face map $\delta_i : X_n \rightarrow X_{n-1}$ is dual to the unique injection $d^i : [n-1] \rightarrow [n]$ in the category $\Delta$ whose image omits the element $i \in [n]$. Similarly, the degeneracy map $\sigma_i : X_n \rightarrow X_{n+1}$ is dual to the unique surjection $s^i : [n+1] \rightarrow [n]$ in $\Delta$ such that $i \in [n]$ has two elements in its preimage. The maps $d^i$ and $s^i$ satisfy certain obvious relations; the face are degeneracy maps satisfy relations dual to these.

#Examples#

* Let $[n]$ denote the object of $\Delta$ corresponding to the totally ordered set $\{ 0, 1, 2,\ldots, n\}$. Then the represented presheaf $\Delta(-, [n])$, which we typically write as $\Delta[n]$ is an example of a simplicial set. By the Yoneda lemma, the $n$-simplices of a simplicial set $X$ are in natural bijective correspondence to maps $\Delta[n] \rightarrow X$ of simplicial sets.

* If $C$ is a small category, the **nerve** of $C$ is a simplicial set which we denote $NC$. If we write **n** for the category corresponding to the poset $[n]$ defined above, we define the $n$-simplices of $NC$ to be the set of functors **n**$\rightarrow C$. Equivalently, the $0$-simplices of $NC$ are the objects of $C$, the $1$-simplices are the morphisms, and the $n$-simplices are strings of $n$ composable arrows in $C$. Face maps are given by composition (or omission, in the case of $\delta_0$ and $\delta_n$) and degeneracy maps are given by inserting identity arrows.

* If $Z$ is a topological space, the **total singular complex** of $Z$ is a simplicial set, which we denote $SZ$. Let ${\Delta}n$ denote the standard _topological_ $n$-simplex $\{ (x_0, \ldots, x_n) : 0\leq x_i \leq n, \sum x_i =1\}$. The $n$-simplices of $SZ$ are defined to be the continuous functions ${\Delta}n \rightarrow Z$. The face map $\delta_i$ is given by precomposition by the continuous injection $d^i$ of ${\Delta}_{n-1}$ as the $i$-th face of ${\Delta}_n$ (with a 0 in the $x_i$ coordinate). The degeneracy map $\sigma_i$ is given by the continuous function ${\Delta}_{n+1} \rightarrow {\Delta}_n$ that adds the $x_i$ and $x_{i+1}$ coordinates. 

#The Category of Simplicial Sets#

Like all categories of presheafs on a small category, the category $sS$ of simplicial sets is complete and cocomplete (with limits and colimits constructed levelwise) and cartesian closed. We write $[X,Y]$ for the internal-hom of simplicial sets $X$ and $Y$. By the Yoneda lemma, the $n$-simplices of $[X,Y]$ correspond to maps $\Delta[n] \rightarrow [X,Y]$, or equivalently, maps $X \times \Delta[n] \rightarrow Y$ (by the defining adjunction). So we may _define_ the simplicial set $[X,Y]$ to have these $n$-simplices. The face and degeneracy maps are given by precomposition by the dual maps in $\Delta$.

# Adjunctions #

The maps $N:$ **Cat** $\rightarrow sS$ and $S:$ **Top** $\rightarrow sS$ described in the examples are actually functors, both of which have left adjoints. These adjoint pairs are examples of a very general sort of adjunction involving simplicial sets, of which there are many examples.

Let $E$ be any cocomplete category and let $F: \Delta \rightarrow E$ be a functor. We define the right adjoint $R : E \rightarrow sS$ as follows. Given an object $e \in E$ the $n$-simplices of $Re$ are defined to be the set $E(F[n],e)$ of morphisms in $E$ from $F[n]$ to $e$. Face and degeneracy maps are given by precomposition by the appropriate (dual) maps in the image of $F$. $R$ is defined on morphisms by postcomposition. 

The left adjoint $L$ is defined to be the left [[Kan extension]] of $F$ along the Yoneda embedding $y: \Delta \rightarrow sS$. Because the $y$ is full and faithful, we will have $Ly = F$, i.e., $L (\Delta[n]) = F[n]$. By specifying $F$, we have already defined a functor to $E$ on the represented simplicial sets; $L$ is the unique cocontinuous extension of this functor to $sS$. It can be described explicitly on objects as a coend.

(Easy) abstract nonsense shows that $L$ and $R$ form an adjoint pair $L \dashv R$.

Here are some examples:

* Let $E=$**Cat** and $F$ be the functor $[n] \mapsto$ **n**. The right adjoint is the nerve functor $N$ described above. The left adjoint ${\tau}1$ takes a simplicial set to its **fundamental category**. 

* Let $E=$**Top** and $F$ be the functor $[n] \mapsto {\Delta}n$. The right adjoint is the total singular complex functor $S$ described above. The left adjoint $|-|$ is called **geometric realization**.  As a consequence of the Kan extension construction, the geometric realization of the represented simplicial set $\Delta[n]$ is the standard $n$-simplex ${\Delta}n$.

* Subdivision and extension $sd: sS \leftrightarrow sS : ex$.

* The simplicial nerve functor and its left adjoint $sS \leftrightarrow sC$ where $sC$ denotes the category of [[simplicial category|simplicial categories]], i.e., categories enriched in $sS$.

* The adjunction $- \times X : sS \leftrightarrow sS : [X,-]$ between the product with a simplicial set $X$ and the internal-hom, which makes $sS$ cartesian closed.