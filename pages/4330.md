## Overview

The composite of [[Schur functors]] is again a Schur functor.  The process of composing Schur functors is known as **plethysm**, especially in situations where we want an explicit "formula" for how the Schur functors compose.

For example, the $n^{th}$ [[exterior power]] functor $\Lambda^n$ is a Schur functor, as is the $n^{th}$ [[symmetric power]] functor $S^n$.  So, we might want to describe the composite

$$  V \mapsto \Lambda^2 S^2(V) $$

as a direct sum of Schur functors coming from [[Young diagrams]].    This is the sort of problem people study when they talk about "plethysm".

## Plethysm product and symmetric operads

Let $S$ be the skeletal category of finite sets and bijections and $C$ a symmetric additive monoidal category with monoidal product $\otimes$ and unit object $\mathbf{1}$. Objects in the category of contravariant functors $C^{S^{op}}$ can be descibed as collections $M = \{M(n), n\geq 0\}$ of objects $M(n)$ in $C$ with action of a symmetric group $\Sigma_n$ on $n$ letters. The category $C^{S^{op}}$ acts on $C$ by the polynomial functors
$$
M : V \mapsto \oplus_{n\geq 0} M(n)\otimes_{\Sigma_n} V^{\otimes n}
$$
The composition of such functors defines a monoidal product on $C^{S^{op}}$ called the __plethysm product__. This way we obtain a monoidal category. The monoids in that category are the (symmetric) $C$-[[operads]]. 

## History and references

In Richard P. Stanley's book _Enumerative Combinatorics_, he discusses the origin of the term 'plethysm' in Volume 2, Appendix 2.  He says that the term was introduced in 

* [[D. E.  Littlewood]], _Invariant theory, tensors and group characters_, Philos. Trans. Roy. Soc. London. Ser. A. **239**, (1944), 305--365.

The term 'plethysm' was suggested to Littlewood by M. L. Clark after the Greek word _plethysmos_, or &#960;&#955;&#951;&#952;&#965;&#963;&#956;&#972;&#962;, which means 'multiplication' in modern Greek (though apparently the meaning goes back to ancient Greek).  The related term _plethys_ in Greek means 'a big number' or 'a throng', and this in turn comes from the Greek verb _plethein_, which means 'to be full', 'to increase', 'to fill', etc.  

Some aspects of plethysm appear (partly through exercises) in the textbook W. Fulton, J. Harris, _Representation theory_.

* A. M. Garsia, G. Tesler, _Plethystic formulas for Macdonald $q, t$-Kostka coefficients_, Advances in Math. __123__ (1996) 144&#8211;222, [MR1420484](http://www.ams.org/mathscinet-getitem?mr=1420484); A. M. Garsia, J. Remmel, _Plethystic formulas and positivity for $q,t$-Kostka coefficients_, Mathematical essays in honor of Gian-Carlo Rota (Cambridge, MA, 1996), 245&#8211;262, Progr. Math. __161__, Birkh&#228;user  1998, [MR99j:05189d](http://www.ams.org/mathscinet-getitem?mr=1627327)

For an application in the study of [[characteristic classes]] see

* Dragutin Svrtan, _New plethysm operation, Chern characters of exterior and symmetric powers with applications to Stiefel-Whitney classes of Grassmannians_, Conference on Formal Power Series and Algebraic Combinatorics (Bordeaux, 1991).  Theoret. Comput. Sci.  __117__ (1993),  no. 1-2, 289--301, &lt;http://dx.doi.org/10.1016/0304-3975(93)90320-S>

An application in a counting problem:

*  Thomas Kahle, Mateusz Michalek, _Plethysm and lattice point counting_ [arxiv/1408.5708](http://arxiv.org/abs/1408.5708)
     