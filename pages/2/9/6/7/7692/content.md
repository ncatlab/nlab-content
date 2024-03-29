[[!redirects I.3, open- and closed subfunctors; schemes]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

For a $k$-functor $X\in coPsh(M_k)$ and $E\subseteq O(X)=M_k(X,O_k)$ a set of functions on $X$, Definition in [[k-ring]], we define

$$V(E)(R):=\{x\in X(R) | f\in E, f(x)=0\}$$

and

$$D(E)(R):=\{x\in X(R)|f\in E, \text{the} f(x) \text{generate the unit ideal of} R\}$$

(The ''unit ideal of $R$'' is just $R$ itself.) For a transformation $u:Y\to X$ of $k$-functors and $Z\subseteq X$ a subfunctor we define

$$u^{-1}(Z)(R):=\{y\in Y(R)|u(y)\in Z(R)\}$$

A subfunctor $Y\subseteq X$ is called _open subfunctor_ resp. _closed subfunctor_ if for every transformation $u:T\to X$ we have $u^{-1}(Y)$ is of the form $V(E)$ resp. $D(E)$.

+-- {: .num_defn}
###### Definition

A $k$-functor $X$ is called a $k$_-scheme_ if the following two conditions hold:

1. ($X$ is a sheaf for the Zarisky Grothendieck topology on $M_k^{op}$) For all $k$-rings and all families $(f_i)_i$ such that $R=\coprod_i R f_i$ we have: if for all $x_i\in R[f_i^{-1}]$ such that the images of $x_i$ and $x_j$ coincide in $X(R[f_i^{-1} f_j^{-1}])$ there is a unique $x\in X(R)$ mapping to the $x_i$.

1. ($X$ has a cover of Zarisky open immersions of affine $k$-schemes) There exists a family $(U_i)_i$ of open affine subfunctors of $X$ such that for all fields $K\in M_k$ we have that $X(K)=\coprod_i U_i(K)$.

=--

+-- {: .num_remark}
###### Remark
The category of $k$-schemes is closed under limits, forming open- and closed subfunctors and skalar extension.

=--
