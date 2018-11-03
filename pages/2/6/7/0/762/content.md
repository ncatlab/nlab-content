
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A **filtered topological space** $X_*$ is a [[filtered object]] in [[Top]], hence

1. a [[topological space]] $X=X_\infty$ 

2. equipped with a [[sequence]] of [[subspaces]] 

   $$X_*:= \quad X_0 \subseteq X_1 \subseteq \cdots \subseteq X_n \subseteq \cdots \subseteq X_\infty. $$

A filtered space $X_*$ is called a **[[connected filtered space]]** if it satisfies the following condition:

$(\phi)_0$: The function $\pi_0X_0  \to \pi_0 X_r$ induced by  inclusion is surjective for all $r \geq 0$; and, for all $i \geq 1$, $(\phi_i): \pi_i(X_r,X_i,v)=0$   for all $r \gt i$  and $ v \in X_0$.

There are two other forms of this condition which are useful under different circumstances. 


## Examples

1. A [[CW-complex]] $X$ with its filtration by [[simplicial skeleton|skeleta]] $X^n$.

1. A [[configuration space of points]] is filtered by number of points.

2. The [[free construction|free]] [[topological monoid]] $F X$ on a [[topological space]] $X$ filtered by the length of words. Given a [[pointed topological space]] $(X,x)$, there is also a reduced version by taking $F X$ and identifying $x$ with the identity of $F X$. This latter filtered space is known as the _[[James construction]]_ $J(X,x)$ ([James 55](#James55)). 

   The [[James construction]] $J(X,x)$ may be constructed [[homotopy theory|homotopy-theoretically]] ([Brunerie 13](#Brunerie13), [Brunerie 17](#Brunerie17)). Recall that, for $K$ a finite [[simplicial complex]], for $(X,A)$ a pair of spaces, its _polyhedral product_ $(X,A)^K$ is defined as the union $\bigcup_{\sigma\in S(K)}(X,A)^\sigma$ as a subspace of the Cartesian product $X^{V(K)}$. Here, for $\sigma\in S(K)$ a simplex of $K$, the subspace $(X,A)^\sigma$ consist of those $x\in X^{V(K)}$ such that, for each vertex $v$ in the complement of $\sigma$, the coordinate projection $\proj_v x$ lies in $A$. Equivalently, the polyhedral product $(X,A)^K$ can be considered as a homotopy colimit of these $(X,A)^\sigma$ over the poset $S(K)$ of simplexes $\sigma$ of $K$, where the maps are the respective inclusions.

   +-- {: .num_defn}
   ###### Definition
   For $X$ a space equipped with a basepoint $x$, define a filtered space $fil_\bullet$ as follows. 
   Set $\fil_0$ as $\{x\}$.
   For $k\ge 1$, require that the following square is homotopy pushout:
   $$
     \array{
    &&&&
        (X,x)^{\partial \Delta[k-1]}
        &&&&
         \\
         & 
         && inc \swarrow
          &
          & \searrow 
         && 
        \\
   && X^k &&&& fil_{k-1}
   \\
         & 
         && {}_{p_k}\searrow
          &
          & \swarrow_{j_k}
         && 
        \\
   &&&&
        fil_k
        &&&&
     }
   $$
   where the unlabeled arrow is the homotopy colimit of a morphism of diagrams over $S(\partial \Delta[k-1])$ given by the maps 
   $$(X,x)^\sigma \xrightarrow{\sim} X^{\dim(\sigma)+1} \xrightarrow{p_{\dim(\sigma)+1}} fil_{\dim(\sigma)+1}$$
   for each simplex $\sigma$ of the boundary simplicial complex $\partial \Delta[k-1]$ of the standard $(k-1)$-simplex.  
   =-- 

   +-- {: .num_prop #TypeOfJames}
   ###### Proposition
    For $(X,x)$ a pointed space, if $(X,x)$ is path-connected, then $fil_\infty \simeq \Omega\Sigma X$.
   =--

3. A similar example to the last using free groups instead of free monoids. 

4. A similar example to the last using free groupoids on topological graphs. 

5. A similar example to the last using the universal topological groupoid $U_\sigma(G)$ induced from a topological groupoid $G$ by a continuous function $f: Ob(G) \to Y$ to a space $Y$. 


Examples of [[connected filtered spaces]] are:

1. The skeletal filtration of a CW-complex. 

2. The word length filtration of the James construction for a space with base point such that $\{x\} \to X$ is a closed cofibration. 

3. The filtration $(B C)_*$ of the classifying space of a crossed complex, filtered using skeleta of $C$. 

This condition occurs in the [[higher homotopy van Kampen theorem]] for [[crossed complex]]es.


## Properties

We thus see that filtered spaces arise from many geometric and algebraic situations, and see also [[stratified space]]s). 
It is  therefore interesting that one can define strict higher homotopy groupoids for filtered spaces more easily than for spaces themselves. 

Note also that it is standard to be able to replace, using mapping cylinders, a sequence of maps $Y_n \to Y_{n+1}$ by a sequence of inclusions. 


## References

The [[James construction]] is due to 

* {#James55} [[Ioan James]], _Reduced product spaces_, Annals of Mathematics, Second Series, 62: 170–197 (1955)

Review of the [[James construction]] includes

* [[Dylan Wilson]], _James construction_, 2017 ([pdf](http://www.math.uchicago.edu/~dwilson/pretalbot2017/james-construction.pdf))

* Wikipedia, _[James reduced product](https://en.wikipedia.org/wiki/James_reduced_product)_

Discussion of the [[James construction]] via [[homotopy type theory]] includes the following

* {#Brunerie13} [[Guillaume Brunerie]], _The James Construction and $\pi_4(S^3)$_, talk at the Institute of Advanced Studies on March 27, 2013 ([recording](https://video.ias.edu/univalent/1213/0327-GuillaumeBrunerie))

* {#Brunerie17} [[Guillaume Brunerie]], _The James construction and $\pi_4(S^3)$ in homotopy type theory_ ([arXiv:1710.10307](https://arxiv.org/abs/1710.10307))

[[!redirects filtered topological space]]
[[!redirects filtered topological spaces]]
[[!redirects filtered space]]
[[!redirects filtered spaces]]
