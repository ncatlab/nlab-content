[[!redirects I.8, constant- and étale schemes]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

$Sch_k$ is [[copower|copowered (= tensored)]] over $Set$. We define the _constant $k$-scheme_ on a set $E$ by

$$E_k:=E\otimes Sp_k k=\coprod_{e\in E}Sp_k k$$

For a scheme $X$ we compute $M_k(E_k,E)=Set(Sp_k k,X)^E=X(k)^E=Set(E,X(k))$ and see that there is an adjunction

$$((-)_k\dashv (-)(k)):Sch_k\to Set$$

A _constant formal scheme_ is defined to be a completion of constant scheme. The completion functor induces an equivalence between the category of constant schemes and the category of constant formal schemes.

An _&#233;tale $k$-scheme_ is defined to be a directed colimit of $k$-spectra $Sp_k k^\prime$ of finite separable field-extensions $k^\prime$ of $k$.


An _&#233;tale formal $k$-scheme_ is defined to be a directed colimit of formal $k$-spectra $Spf_k k^\prime$ of finite separable field-extensions $k^\prime$ of $k$.

+-- {: .num_remark}
###### Remark
Let $X$ be a $k$-scheme or a formal $k$-scheme. Then the following statements are equivalent:

1. $X$ is &#233;tale.

1. $X\otimes_k cl(k)$ is constant.

1. $X\otimes_k k_s$ is constant.

where $cl(k)$ denotes an algebraic closure of $k$, $k_s$ denotes the subextension of $cl(k)$ consisting of all separable elements of $cl(k)$ and $\otimes_k$ denotes skalar extension.
=--

+-- {: .num_prop}
###### Proposition
Let $X$ be a $k$-formal scheme (resp. a [[locally algebraic scheme]]) then $X$ is [[etale scheme|étale]] iff the [[Frobenius morphism]] $F_X:X\to X^{(p)}$is a monomorphism (resp. an isomorphism).
=--

+-- {: .num_theorem}
###### Theorem
([[the fundamental theorem of Galois theory|fundamental theorem of Galois theory]])

The functor

$$\begin{cases}
Sch_{et}\to Gal(k_s / k)- Mod
\\
X\mapsto X(k_s)
\end{cases}$$

from [[etale scheme|étale schemes]] to the category of [[Galois module|Galois modules]] $Gal(k_s/s)-Mod$ is an equivalence of categories.
=--

+-- {: .num_remark}
###### Remark
The completion functor

$$\begin{cases}
Sch_{et}\to fSch_{et}
\\
X\mapsto \hat X
\end{cases}$$
 is an equivalence of categories.
=--


[[!redirects étale scheme]]

[[!redirects etale scheme]]
