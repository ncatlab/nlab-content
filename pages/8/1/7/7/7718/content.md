[[!redirects III.9, Dieudonné modules (connected formal groups of finite type)]]

This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

By a similar discussion (replacing $p$ by $F$) as in &#167; 8, we have:
 
+-- {: .num_remark}
###### Remark
If $G$ is is a connected finite type formal group, define

$$M(G):= lim M(ker F^n_G)$$

This is a module over the $F$-completion $\hat D_k$ of $D_k$.
=--

+-- {: .num_theorem}
###### Theorem
The Dieudonn&#233;-functor is an equivalence

$$\begin{cases}
Fftc\to \hat D_k-Mod_{fin.len.quot}
\\
G\mapsto M(G)
\end{cases}$$

between the category of connected formal groups of finite type and the category of $\hat D_k$-modules $M$ such that $M/FM$ has finite length. Moreover we have:

1. $G$ is finite iff $M(G)$ has finite length iff $F^n M(G)=0$ for large $n$.

1. $G$ is smooth iff $F:M(G)\to M(G)$ is injective. In that case $dim(G)= length(M(G)/ FM(G))$.
=--


