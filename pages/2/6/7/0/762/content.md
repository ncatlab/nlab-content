##Filtered space##

A [[filtered space]] $X_*$ consists of a space $X=X_\infty$ and a [[sequence]] of subspaces 

$$X_*:= \quad X_0 \subseteq X_1 \subseteq \cdots \subseteq X_n \subseteq \cdots \subseteq X_\infty. $$

Standard examples are : 

1. A CW-complex $X$ with its filtration by skeleta $X^n$.

1. The free topological monoid $FX$ on a space $X$ filtered by the length of words. This is sometimes modified by taking a space with base point $(X,x)$ and then in $FX$ identifying $x$ with the identity of $FX$. This gives the James construction $J(X,x)$, after Ioan James. 

1. A similar example to the last using free groups instead of free monoids. 

1. A similar example to the last using free groupoids on topological graphs. 

1. A similar example to the last using the universal topological groupoid $U_\sigma(G)$ induced from a topological groupoid $G$ by a continuous function $f: Ob(G) \to Y$ to a space $Y$. 

Thus filtered spaces arise from many geometric and algebraic situations. (See also [[stratified space]]s). 
So it is  interesting that one can define strict higher homotopy groupoids for filtered spaces more easily than for spaces themselves. 

Note also that it is standard to be able to replace, using mapping cylinders, a sequence of maps $Y_n \to Y_{n+1}$ by a sequence of inclusions. 

A filtered space $X_*$ is called a [[connected filtered space]]  if it satisfies the following condition:


 $(\phi)_0$: The function $\pi_0X_0  \to \pi_0 X_r$ induced by  inclusion is surjective for all $r \geq 0$; and, for all $i \geq 1$, $(\phi_i): \pi_i(X_r,X_i,v)=0$   for all $r \gt i$  and $ v \in X_0$.

There are two other forms of this condition which are useful under different circumstances. 

Examples of connected filtered spaces are:

1. The skeletal filtration of a CW-complex. 

1. The word length filtration of the James construction for a space with base point such that $\{x\} \to X$ is a closed cofibration. 

1. The filtration $(BC)_*$ of the classifying space of a crossed complex, filtered using skeleta of $C$. 

This condition occurs in the [[higher homotopy van Kampen theorem]] for [[crossed complex]]es.

[[!redirects filtered spaces]]