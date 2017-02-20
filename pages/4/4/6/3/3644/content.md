
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **rational homotopy equivalence** is the notion of equivalence of [[topological space]]s as used in [[rational homotopy theory]]. Where a [[weak homotopy equivalence]] in ordinary [[homotopy theory]] identifies spaces under morphisms that induce isomorphisms on all [[homotopy group]]s, rational homotopy equivalences identify spaces under morphisms that induce isomorphisms on all _rationalized_ homotopy groups.

## Definition

+-- {: .num_defn }
###### Definition


For $X$ and $Y$ be [[simply connected space|simply connected]] [[topological space]]s and $f : X \to Y$ a continuous map between them, $f$ is called a **rational homotopy equivalence** if the following equivalent conditions are satisfied:

1. it induces an isomorphism on rationalized homotopy groups: $\pi_*(f) \otimes \mathbb{Q} : \pi_*(X) \otimes \mathbb{Q} \stackrel{\simeq}{\to} \pi_*(X) \otimes \mathbb{Q}$;

1. it induces an isomorphism on [[ordinary homology]] groups with rational [[coefficients]]: $H_*(f,\mathbb{Q}) : H_*(X,\mathbb{Q}) \stackrel{\simeq}{\to} H_*(X,\mathbb{Q})$;

1. it induces an isomorphism on rational [[cohomology]] groups: $H^*(f,\mathbb{Q}) : H^*(X,\mathbb{Q}) \stackrel{\simeq}{\to} H^*(X,\mathbb{Q})$;

1. it induces a [[weak homotopy equivalence]] on the  [[rationalization]]s $X_{ra}$ and $Y_{ra}$ : $f_{ra} : X_{ra} \stackrel{\simeq_{whe}}{\to} Y_{ra}$.

=--

That (the first two of) these conditions are equivalent is due to [Serre 53](#Serre53)

## References

The concept is due to

* {#Serre53} [[Jean-Pierre Serre]], _Groupes d'homotopy et classes de groupes abelians_, Ann. of Math. 58 (1953) 258-294



Review includes 

* [[Kathryn Hess]], around definition 1.17 in _Rational homotopy theory: a brief introduction_ ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626))
