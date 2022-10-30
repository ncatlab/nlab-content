## Reminder

Let $G$ be a commutative $k$-group functor (in cases of interest this is a finite flat commutative [[group scheme]]). Then the *Cartier dual* $D(G)$ of $G$ is defined by

$$D(G)(R):=Gr_R(G\otimes_k R,\mu_R)$$

where $\mu_k$ denotes the group scheme assigning to a ring its multiplicative group $R^\times$ consisting of the invertible elements of $R$.

This definition deserves the name [[duality]] since we have

$$hom(G,D(H))=hom(H,D(G))=hom(G\times H,\mu_k)$$

## Discussion

The notion of a *multipliciative group scheme* generalizes 

+-- {: .num_defn}
###### Definition and Remmark
A group scheme is called *multiplicative group scheme* if the following equivalent conditions are satisfied:

1. $G\otimes_k k_s$ is [[diagonalizable group scheme|diagonalizable]].

1. $G\otimes_k K$ is diagonalizable for a field $K\in M_k$.

1. $G$ is the Cartier dual of an &#233;tale $k$-group.

1. $\hat D(G)$ is an &#233;tale $k$-formal group.

1. $Gr_k(G,\alpha_k)=0$

1. (If $p\neq 0)$, $V_G$ is an epimorphism

1. (If $p\neq 0)$, $V_G$ is an isomorphism
=--

+-- {: .num_remark}
###### Remark
Let $G_const$ dnote a [[constant group scheme]], let $E$ be an [[étale group scheme]]. Then we have the following [[Cartier duality|cartier duals]]:

1. $D(G_const)$ is [[diagonalizable group scheme|diagonalizable]].

1. $D(E)$ is [[multiplicative group scheme|multiplicative]]
=--