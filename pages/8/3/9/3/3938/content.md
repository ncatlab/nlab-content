_Under Construction - The following material needs the blessing of an expert._

## Idea

Given a smooth morphism $f:M\to N\in Diff$ in , an $n$-dimensional connected open subset $U \subseteq M$ and a differential $n$-form $\omega\in\Omega^n(N)$, we have the pullback $f^*\omega\in\Omega^n(M)$ and the pushforward $f_*U$ that satisfy

$$\int_U f^*\omega = \int_{f_*U} \omega.$$

_Transgression_ can be thought of as a generalization of this situation. For instance, given a smooth manifold $M$, let $LM$ denote the [[loop space]] of $M$, that is, $Hom(S^1,M)$.
+-- {: .query}
_Harry_: It's not obvious whether or not you mean the space of smooth loops or continuous loops, nor how you equip this space, which presumably has the compact-open topology, with a smooth manifold structure at all.  This is important for the next part.

Note: I changed what it originally said, but it's still not clear to me what is correct.
=--
A $0$-form $f:LM\to \mathbb{R}$ induces a $1$-form $L^*f\in \Omega^1(M)$ and a loop $\gamma: S^1\to M$ in $M$ determines a point $L_*\gamma$ in $LM$. Then we give the condition that for any $0$-form $f: LM\to \mathbb{R}$ and any loop $\gamma: S^1\to M$,

$$\int_\gamma L^*f = \int_{L_*\gamma} f.$$

The right-hand side is simply evaluation of the $0$-form at the point determined by $\gamma$, from which it follows that the integral of a 1-form $L^*f$ over a loop $\gamma: S^1 \to M$ can be computed simply by evaluation.
