## Background

See the article [[Kähler C^∞-differentials of smooth functions are differential 1-forms]] for the necessary background for this article, including the notions of [[C^∞-ring]], [[C^∞-derivation]], and [[Kähler C^∞-differential]].

## Idea

In [[algebraic geometry]], (algebraic) differential forms on the [[Zariski spectrum]] of a [[commutative ring]] $R$ (or a commutative $k$-algebra $R$) can be defined as the free [[commutative differential graded algebra]] on $R$.

This definition does not quite work for [[smooth manifolds]]: as already explained in the article [[Kähler C^∞-differentials of smooth functions are differential 1-forms]], the notion of a [[Kähler differential]] must be refined in order to extract smooth differential 1-forms from the [[C^∞-ring]] of smooth functions on a [[smooth manifold]] $M$.

Thus, in order to get the algebra of smooth differential forms, the notion of a [[commutative differential graded algebra]] must likewise be adjusted.

\begin{definition}
A __commutative differential graded C^∞-ring__ is a real [[commutative differential graded algebra]] $A$ whose degree 0 component $A_0$ is equipped with a structure of a [[C^∞-ring]] in such a way that the degree 0 differential $A_0\to A_1$ is a [[C^∞-derivation]].
\end{definition}

With this definition, we can recover smooth differential forms in a manner similar to algebraic geometry, deducing the following consequence of the Dubuc–Kock theorem for Kähler C^∞-differentials.

\begin{theorem}
The free commutative differential graded C^∞-ring on the [[C^∞-ring]] of smooth functions on a smooth manifold $M$ is canonically isomorphic to the differential graded algebra of smooth [[differential forms]] on $M$.
\end{theorem}

## Application: the Poincaré lemma

The [[Poincaré lemma]] becomes a trivial consequence of the above theorem.

\begin{proposition}
For every $n\ge0$, the canonical map
$$\mathbf{R}[0]\to \Omega(\mathbf{R}^n)$$
is a [[quasi-isomorphism]] of [[differential graded algebras]]. 
\end{proposition}

\begin{proof}
(Copied from the [[MathOverflow]] [answer](https://mathoverflow.net/questions/38439/integrals-from-a-non-analytic-point-of-view/38479#38479).)
The de Rham complex of a finite-dimensional smooth manifold $M$ is the free C^∞-dg-ring on the C^∞-ring $C^\infty(M)$.
If $M$ is the underlying smooth manifold of a finite-dimensional real vector space $V$, then $C^\infty(M)$ is the free C^∞-ring on the vector space $V^*$ (the real dual of $V$).  Thus, the de Rham complex of a finite-dimensional real vector space $V$ is the free C^∞-dg-ring on the vector space $V^*$.  This free C^∞-dg-ring is the free C^∞-dg-ring on the free cochain complex on the vector space $V^*$.  The latter cochain complex is simply $V^*\to V^*$ with the identity differential.  It is cochain homotopy equivalent to the zero cochain complex, and the free functor from cochain complexes to C^∞-dg-rings preserves cochain homotopy equivalences.
Thus, the de Rham complex of the smooth manifold $V$ is cochain homotopy equivalent to the free C^∞-dg-ring on
the zero cochain complex, i.e., $\mathbf{R}$ in degree 0.
\end{proof}

## References

* [[E. J. Dubuc]], [[A. Kock]], _On 1-form classifiers_, Communications in Algebra 12:12 (1984), 1471–1531.  [doi](https://doi.org/10.1080/00927878408823064).
