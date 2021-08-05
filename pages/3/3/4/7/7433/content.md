
# Contents
* table of contents
{: toc}

## Idea

The Reidemeister trace, developed by Reidemeister and Wecken, is an algebraic invariant of a self-map of a "finite" topological space.  It gives information about the existence or nonexistence of fixed points, and refines both the [[Lefschetz number]] and [[Nielsen number]].

## Definition

Suppose $M$ is a [[closed manifold]] and $f\colon M\to M$ a [[self-map]].  Deform $f$ so that it has isolated fixed points.  We say that two fixed points $x$ and $y$ are in the same [[fixed-point class]] if there is a path $\gamma$ from $x$ to $y$ such that $f(\gamma)$ is [[homotopy|homotopic]] to $\gamma$ rel the endpoints ($x$ and $y$).  Let $\mathbb{Z}[\pi_1(M)_f]$ denote the free abelian group on the set of fixed-point classes.  Then the **Reidemeister trace** of $f$ is the formal sum

$$ R(f) \coloneqq \sum_{f(x)=x} ind_f(x) \cdot [x] \in \mathbb{Z}[\pi_1(M)_f] $$

where $ind_f(x)$ is the [[index]] of the fixed point $x$ of $f$.  This definition is homotopy invariant.

An equivalent definition can be obtained algebraically, or category-theoretically using the [[bicategorical trace]].

## Properties

* The sum of all the coefficients in the Reidemeister trace is the [[Lefschetz number]] $L(f)$.

* The number of nonzero coefficients in the Reidemeister trace is the [[Nielsen number]] $N(f)$.

* If $M$ is a closed manifold of dimension at least 3, and $R(f)=0$, then $f$ is homotopic to a map without fixed points.  Thus, the Reidemeister trace supports a converse to the [[Lefschetz fixed-point theorem]].

## References

The Reidemeister trace was introduced in 

* [[Kurt Reidemeister]], _Automorphismen von Homotopiekettenringen_, Mathematische
Annalen, 112:586&#8211;593 (1936)

A modern treatment is in

* S. Husseini, _Generalized Lefschetz numbers_, Transactions of the American
Mathematical Society, 272:247&#8211;274 (1982)

See also

* Peter Staecker, _The Reidemeister trace: computation by nilpotentization and extension to coincidence theory_ (PhD thesis)

* Peter Staecker, _Axioms for a local Reidemeister trace in fixed point and coincidence theory on differentiable manifolds_, ([arXiv:0704.1891v2](http://arxiv.org/abs/0704.1891v2))

A reformulation of the Reidemeister trace in terms of [[bicategorical trace]] is in 

* [[Kate Ponto]], [[Michael Shulman]], _The multiplicativity of fixed point invariants_ ([arXiv:1203.0950](http://arxiv.org/abs/1203.0950))
