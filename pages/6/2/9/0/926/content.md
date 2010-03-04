
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A __Postnikov system__ or __Postnikov tower__ ([[M M Postnikov]], 1951) is a sequence of path connected, pointed topological spaces $X^{(n)}$, $n \geq 1$,
such that $\pi_r(X^{(n)})=0$ for $r \gt n$,
together with a sequence $\pi_n$ of [[module]]s of the [[fundamental group]] $\pi_1(X^{(1)})$ of $X^{(1)}$ and
[[fibration]]s $p_n : X^{(n+1)} \to X^{(n)}$ classified up to [[homotopy type]] by a specified cohomology class $k^{n+1} \in H^{n+1}(X^{(n)}, \pi_n)$. 


## Properties

It is known that Postnikov systems classify all weak, pointed connected [[homotopy type]]s. In particular, if $X$ satisfies $\pi_r(X)=0 $ for $1 \lt r \lt n$ then the first non trivial Postnikov invariant is an  element $k^{n+1}$ of [[group cohomology]] (with twisted coefficients of course). Such elements are also determined by $n$-fold crossed extensions of $\pi_n$ by $\pi_1$,
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


## Generalizations

There are analogues in other setups, e.g. 

* [[Postnikov system in triangulated category|Postnikov systems in triangulated categories]] 

* [[motive|motivic]] homotopy theory (M. Levine, [The Postnikov tower in motivic stable homotopy theory](http://www.math.uiuc.edu/K-theory/0692)).

* [[Postnikov tower in an (∞,1)-category]]

## References

* M.M. Postnikov, _Determination of the homology groups of a space by means of the homotopy invariants_, Doklady Akad. Nauk SSSR (N.S.) 76: 359&#8211;362 (1951)
* George Whitehead, _Elements of homotopy theory_, chapter 9
* Donald W. Kahn, _The spectral sequence of a Postnikov system_, Comm. Math. Helv. 40, n.1, 169--198, 1965 [doi](http://dx.doi.org/10.1007/BF02564370)
* P. I. Booth, _An explicit classification of three-stage Postnikov towers_, Homology, homotopy and applications 8 (2006), No. 2, 133--155
* G. Ellis and R. Mikhailov, _A colimit of classifying spaces_, [arXiv:0804.3581](http://www.arxiv.org/abs/0804.3581).

A pedagogical introduction to Postnikov systems with an eye towards their $\infty$-[[infinity-groupoid|groupoid]] incarnation under the correspondence given by the [[homotopy hypothesis]] is in

* [[John Baez]], [[Mike Shulman]], _[[Lectures on n-Categories and Cohomology]]_


[[!redirects Postnikov tower]]
[[!redirects Postnikov decomposition]]