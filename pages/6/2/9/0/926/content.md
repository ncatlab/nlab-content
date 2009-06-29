

A __Postnikov system__ or __Postnikov tower__ is a sequence of path connected, pointed spaces
$X^{(n)}$, $n \geq 1$,
such that $\pi_r(X^{(n)})=0$ for $r \gt n$,
together with a sequence $\pi_n$ of [[module]]s of the [[fundamental group]] $\pi_1(X^{(1)})$ of $X^{(1)}$ and
[[fibration]]s $p_n : X^{(n+1)} \to X^{(n)}$ classified up to [[homotopy type]] by a cohomology class $k^{n+1} \in H^{n+1}(X^{(n)}, \pi_n)$.

It is known that Postnikov systems classify all weak, pointed
connected homotopy types. In particular, if $X$ satisfies
$\pi_r(X)=0 $ for $1 \lt r \lt n$ then the first non trivial
Postnikov invariant is an  element $k^{n+1}$ of [[group cohomology]]
(with twisted coefficients of course). Such elements are also
determined by $n$-fold crossed extensions of $\pi_n$ by $\pi_1$,
which are exact [[crossed complex]]es of the form
$$ 0 \to \pi_n \to C_n \to C_{n-1} \to \cdots \to C_2 \to C_1 $$
together with an isomorphism $Coker(C_2 \to C_1) \cong \pi_1$. This
gives an algebraic model of such an $n$-[[homotopy n-type|type]]. Advantages of
algebraic models are that algebraic constructions can be made on
them, such as forming [[limit]]s or colimits. The various [[higher
homotopy van Kampen theorem]]s are useful in the latter case. For
example, it may be difficult or well nigh impossible to write down a
determination of the Postnikov invariant of a pushout of crossed
modules, even if the pushout consists of finite groups.

A Postnikov system is easiest to understand in the 2-stage case,
i.e. two non vanishing homotopy groups, and focuses attention on the
cohomology of [[Eilenberg-Mac Lane space]]s, which also determine all
cohomology operations. Basic work on this area was done by Eilenberg
and Mac Lane, and by H. Cartan, while the theory of cohomology
operations, including Steenrod operations, is itself a large area.

The reference below shows the problems in the 3-stage systems. 

For homotopy 3-types, the algebraic model of [[crossed square]]s is more explicit than the corresponding Postnikov system, and more calculable. However, not much work has been done on, say, cohomology operations using the algebraic model of $n$-fold groupoids, and it is not clear if that would help. 


##References##

* Booth P.I.   "An Explicit Classification of Three-stage Postnikov Towers", Homology, homotopy and applications, 8 (2006), No. 2, 133--155
* G. Ellis and R. Mikhailov, "A colimit of classifying spaces", arXiv:0804.3581.


[[!redirects Postnikov tower]]