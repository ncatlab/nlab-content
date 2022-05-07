
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The analogs in [[(∞,1)-category]] theory of the [[adjoint functor theorems]] in ordinary [[category theory]].

## Statement

+-- {: .num_defn} 
###### Definition 
* Let $G:\mathcal{D} \to \mathcal{C}$ be a functor between $(\infty, 1)$-categories. We say that $G$ satisfies the **solution set condition** if the $(\infty, 1)$-category $c/G$ admits a small weakly initial set for any $c$ in $\mathcal{C}$.
 
* $G$ satisfies the **$h$-initial object condition** if $c/G$ admits an [[h-initial object]] for any $c$ in $\mathcal{C}$.

* $\mathcal{C}$ is said to be **2-locally small** if for every pair of objects, $x$,$y$, of $\mathcal{C}$, the mapping space $map_{\mathcal{C}}(x,y)$ is [[locally small]].
=--

+-- {: .num_theorem #GeneralAdjointFunctorTheorem}
###### Theorem

* Let $G:\mathcal{D} \to \mathcal{C}$ be a [[continuous functor]]. Suppose that $\mathcal{D}$ is locally small and complete and $\mathcal{C}$ is 2-locally small. Then $G$ admits a left adjoint if and only if it satisfies the solution set condition.

* Let $G:\mathcal{D} \to \mathcal{C}$ be a [[finitely continuous functor]]. Suppose that $\mathcal{D}$ is finitely complete. Then $G$ admits a left adjoint if and only if it satisfies the $h$-initial object condition.

=--

+-- {: .proof}
###### Proof


See Section 3 of ([NRS18](#NRS18)).

=--

The following result is a consequence.  

+-- {: .num_theorem}
###### Theorem

Let $F : C \to D$ be an [[(∞,1)-functor]] between [[locally presentable (∞,1)-categories]] then

1. it has a right [[adjoint (∞,1)-functor]] precisely if it preserves small [[limit in a quasi-category|colimits]];

1. it has a left [[adjoint (∞,1)-functor]] precisely if it is an [[accessible (∞,1)-functor]] and preserves small [[limit in a quasi-category|limits]].

=--

+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, cor. 5.5.2.9]].

=--


+-- {: .num_remark}
###### Remark

For the existence of right adjoints, we can weaken the hypotheses to merely requiring $D$ to be a [[locally small (infinity,1)-category]].
([[Higher Topos Theory|HTT, rem. 5.5.2.10]])

=--

## Related concepts

* [[adjoint functor theorem]]



## References

* {#NRS18} Hoang Kim Nguyen, [[George Raptis]], Christoph Schrade, _Adjoint functor theorems for ∞-categories_, Journal of the London Mathematical Society **101** 2 (2019) 659-681
([arXiv:1803.01664](https://arxiv.org/abs/1803.01664))

Section 5.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects adjoint (∞,1)-functor theorem]]
[[!redirects adjoint (∞,1)-functor theorems]]