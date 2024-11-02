
# Implicit function theorems
* table of contents
{: toc}

## Idea

Implicit function theorems give sufficient conditions for the existence of a [[differentiable map|differentiable]] [[inverse]] of a [[germ]] $f_p$ of a [[differentiable map]] $f\colon M \to N$ of [[smooth manifold]]s at a point $p$. The invertibility is trivially equivalent to the statement that the germ is a [[local diffeomorphism]] of some [[neighborhood]] of $p$ to some neighborhood of $f(p)$. If it is invertible, then we can consider the [[tangent map]] $T_p f\colon T_p M \to T_{f(p)}N$. If $f$ is locally invertible with differentiable inverse, then for all $y$ in some neighborhood of $y$ the [[functor]]iality of $T$ implies that $Id_{T_y} = T_y (f^{-1} \circ f) = T_{f(y)} f^{-1} \circ T_y f$ and alike for $f \circ f^{-1}$ at $f(y)$, demonstrating that $T_y f$ must then be invertible. The [[inverse function theorem]] says that the invertibility of $T_p f$ is in fact sufficient for the invertibility of the germ, which is then automatically differentiable. 


## In $\mathbf{R}^n$

Let $U \subset \mathbf{R}^n$ be an [[open set]] in a [[cartesian space]], $a\in U$, $f\colon U \to \mathbf{R}^n$ a [[continuously differentiable map|map]] of class $C^1$ and $det\left(\frac{\partial f_i}{\partial x_j}(a)\right)\neq 0$. Then there are open sets $V \ni a$, $W \ni f(a)$, $V \subset U$ such that $f|_V\colon V \to W$ is a [[diffeomorphism]] and for all $y \in W$ and $(f^{-1})'(y) = (f'[f^{-1}(y)])^{-1}$. 


## Local statement on manifolds

This is the theorem stated in the Idea section; the differentiable germ is assumed to be of class $C^1$ ([[continuously differentiable map|continuously differentiable]]). The statement is local, so one can consider it in [[chart]]s, hence the proof reduces to the case of $\mathbf{R}^n$.


## Global statement on manifolds

Let $f\colon M \to N$ be a [[smooth map]] of smooth manifolds. A point $q \in N$ is a __regular value__ of $f$ if for every point $p \in f^{-1}(q)$ the [[differential]] $T_p f\colon T_p M \to T_q N$ is an [[epimorphism]]. The implicit function theorem asserts that $Q = f^{-1}(p)$ is a smooth [[submanifold]] of $M$ and the [[tangent bundle]] $T M|_N$ globally splits as $T M|_N \cong T N \oplus \mathbf{R}^n$ where $n = dim N$.

More generally, if $W \subset N$ is a submanifold, we say that the map $f$ is __transversal along__ $W$ if for every point $x\in f^{-1}(W)$ there is an equality
$$
T_{f(x)} N = T_{f(x)}W + (T_x f)(T_x M)
.$$ 
In particular, $f$ is transveral along every regular value $p \in N$. The implicit function theorem asserts that the [[preimage]] $f^{-1}(W)$ is a smooth submanifold of $M$, the [[normal bundle]] $\nu(f^{-1}(W) \subset M)$ is isomorphic to $f^*(\nu(W\subset N))$, and the differential $T f$ exhibits the fiberwise isomorphism $\nu(f^{-1}(W)\subset M)\to \nu(W\subset N)$.


## References

* L. H. Loomis, [[S. Sternberg]], _Advanced calculus_, 1968, 1990 (3.11 in 1990 edition)

* S. Lang, _Analysis I_

Various applications and related theorems can be found in chapter 5: _Local and tangential properties_ of

* T. Br&#246;cker, K. J&#228;nich, C. B. Thomas, M. J. Thomas, _Introduction to differentiable topology_, 1982 (translated from German 1973 edition; $\exists$ also 1990 German 2nd edition)

An invariant global statement on manifolds is at page 44 of 

* &#1040;. &#1057;. &#1052;&#1080;&#1097;&#1077;&#1085;&#1082;&#1086;, &#1042;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1077; &#1088;&#1072;&#1089;&#1089;&#1083;&#1086;&#1077;&#1085;&#1085;&#1080;&#1103; &#1080; &#1080;&#1093; &#1087;&#1088;&#1080;&#1084;&#1077;&#1085;&#1077;&#1085;&#1080;&#1103;, Moscow, Nauka 1984

Elementary course notes of the case in $\mathbf{R}^n$ (mainly lots of examples):

* Frank Jones, _Implicit function theorem_, [pdf](http://www.owlnet.rice.edu/~fjones/chap6.pdf)


On the implicit function theorem in the generality of [[Fréchet manifolds]]:

* [[Richard S. Hamilton]], *The inverse function theorem of Nash and Moser*, Bull. Amer. Math. Soc. **7** (1982) 65-222 &lbrack;[doi:1982-07-01/S0273-0979-1982-15004-2](https://www.ams.org/journals/bull/1982-07-01/S0273-0979-1982-15004-2)&rbrack;



[[!redirects implicit function theorem]]
[[!redirects implicit function theorems]]
