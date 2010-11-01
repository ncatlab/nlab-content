# Contents

* tic
{: toc}

## Idea

A **Conduch&#233; functor** is a [[functor]] which is an [[exponentiable morphism]] in [[Cat]].  This turns out to be equivalent to a certain "factorization lifting" property which includes both [[Grothendieck fibrations]] and opfibrations.


## Failure of local cartesian closedness in Cat

As is evident from the fact that such functors have a name, not every functor is exponentiable in $Cat$.  In particular, although $Cat$ is [[cartesian closed category|cartesian closed]], it is not [[locally cartesian closed category|locally cartesian closed]].

It is easy to write down examples of colimits in $Cat$ that are not preserved by pullback (as they would be if pullback had a right adjoint).  For instance, let $\mathbf{2}$ denote the [[walking arrow]], i.e. the ordinal $2$ regarded as a category, $1$ the terminal category, and $\mathbf{3} = \mathbf{2} \sqcup_1 \mathbf{2}$ the ordinal $3 = (a \to b \to c)$ regarded as a category.  Then the pushout square
$$\array{1 & \overset{}{\to} & \mathbf{2}\\
  \downarrow && \downarrow\\
  \mathbf{2}& \underset{}{\to} & \mathbf{3}}$$
in $Cat/\mathbf{3}$ pulls back along the inclusion $\mathbf{2}\to \mathbf{3}$ of the arrow $(a\to c)$ to the square
$$\array{0 & \overset{}{\to} & 1\\
  \downarrow && \downarrow\\
  1& \underset{}{\to} & \mathbf{2}}$$
which is certainly not a pushout.

One way to describe the problem is that the pushout has "created new morphisms" that didn't exist before.  But another way to describe the problem is that the inclusion $\mathbf{2}\to\mathbf{3}$ fails to notice that the morphism $(a\to c)$ acquires a new factorization in $\mathbf{3}$ which it didn't have in $\mathbf{2}$.  Conduch&#233;'s observation was that this latter failure is really the only problem that can prevent a functor from being exponentiable.

## Definition

A functor $p\colon E\to B$ is a **strict Conduch&#233; functor** if for any morphism $\alpha\colon a\to b$ in $E$ and any factorization $p a \overset{\beta}{\to} c \overset{\gamma}{\to} p b$ of $p \alpha$ in $B$, we have:

1. there exists a factorization $a \overset{\tilde{\beta}}{\to} d \overset{\tilde{\gamma}}{\to} b$ of $\alpha$ in $E$ such that $p \tilde{\beta} = \beta$ and $p \tilde{\gamma} = \gamma$, and

1. any two such factorizations in $E$ are connected by a zigzag of commuting morphisms which map to $id_c$ in $B$.

The theorem is then that the following are equivalent:

* $p$ is a Conduch&#233; functor.
* $p$ is exponentiable in the 1-category $Cat$.
* $p$ is exponentiable in the [[strict 2-category]] $Cat$.

By "exponentiable in the strict 2-category $Cat$" we mean that pullback along $p$ has a strict right 2-adjoint (i.e.&#160;a $Cat$-enriched right adjoint).  Of course, this implies ordinary exponentiability in the 1-category $Cat$, while the converse follows via an argument involving [[cotensors]] with $\mathbf{2}$ in $Cat$.

For exponentiability in the weak [[2-category]] $Cat$, in the sense of pullback having a weak/pseudo 2-adjoint, we can simply weaken the condition.  We say that $p\colon E\to B$ is a **(weak) Conduch&#233; functor** if for any morphism $\alpha\colon a\to b$ in $E$ and any factorization $p a \overset{\beta}{\to} c \overset{\gamma}{\to} p b$ of $p \alpha$ in $B$, we have:

1. there exists a factorization $a \overset{\tilde{\beta}}{\to} d \overset{\tilde{\gamma}}{\to} b$ of $\alpha$ in $E$, and an isomorphism $p d \cong c$, such that modulo this isomorphism $p \tilde{\beta} = \beta$ and $p \tilde{\gamma} = \gamma$, and

1. any two such factorizations in $E$ are connected by a zigzag of commuting morphisms which map to isomorphisms in $B$.

A functor can then be shown to be a weak Conduch&#233; functor if and only if it is exponentiable in the weak sense in $Cat$.


## Conduch&#233; functors and fibrations

The main examples of Conduch&#233; functors are [[Grothendieck fibrations]].  Specifically, it is easy to show that any Grothendieck fibration *or* opfibration is a strict Conduch&#233; functor, while any fibration or opfibration in the weakened sense of Street is a weak Conduch&#233; functor.

The Conduch&#233; criterion can also be reformulated in a more conceptual way by analogy with fibrations.  Observe that to give a functor $p\colon E\to B$ is essentially the same as to give a normal [[lax 2-functor]] $B\to Prof$ from $B$ to the 2-category of [[profunctors]].  Given a functor $p$, we define $B\to Prof$ as follows.  Each object $b\in B$ is sent to the fiber category $p^{-1}(b)$ of objects lying over $b$ and morphism lying over $1_b$.  And each morphism $f\colon a\to b$ in $B$ to the profunctor $H_f\colon p^{-1}(a) &#8696; p^{-1}(b)$ for which $H_f(x,y)$ is the set of arrows $x\to y$ in $E$ lying over $f$.  The lax structure maps $H_f \otimes H_g \to H_{g f}$ are given by composition in $E$.  The converse construction of a functor $p$ from a normal lax 2-functor into $Prof$ is an evident generalization of the [[Grothendieck construction]].  Now we can say that:

* $p$ is a fibration iff the corresponding functor $B\to Prof$ factors through a pseudo 2-functor landing in $Cat^{op}$, via the contravariant inclusion $Cat^{op}\to Prof$.
* Similarly, $p$ is an opfibration iff $B\to Prof$ factors through a pseudo 2-functor landing in $Cat$ via the covariant inclusion $Cat \to Prof$.
* The functor $B\to Prof$ factors through a *lax* 2-functor landing in $Cat^{op}$ iff $p$ admits all "weakly cartesian" liftings, and dually.
* Finally, $p$ is a Conduch&#233; functor iff the functor $B\to Prof$ is itself a pseudo 2-functor (though it may not land in $Cat$ or $Cat^{op}$).  This can be seen by comparing the definition of the tensor product of profunctors with the explicit description in terms of unique factorizations above.

+--{: .query}
[[Mike Shulman]]: Does this point of view provide any intuition for why Conduch&#233; functors should be the exponentiable morphisms in $Cat$?
=--


## References

* F. Conduch&#233;, \'Au sujet de l'existence d'adjoints &#224; droite aux foncteurs "image r&#233;ciproque" dans la cat&#233;gorie des cat&#233;gories\', *C.R. Acad. Sci. Paris* 275 (1972), A891--894.

* J. Giraud, \'M&#233;thode de la descente\', *Bull. Math. Soc. Memoire* 2 (1964)

The definitions and proofs of the above theorems, along with the 2-categorical generalization (Conduch&#233; considered only the 1-categorical case) can also be found in

* [[Peter Johnstone]], "Fibrations and partial products in a 2-category", *Appl. Categ. Structures* 1 (1993), 141--179

A description of the characterization in terms of lax normal functors can be found in

* [[Ross Street], \'Powerful functors\', [pdf](http://www.math.mq.edu.au/~street/Pow.fun.pdf)

[[!redirects Conduche functors]]
[[!redirects Conduché functor]]
[[!redirects Conduché functors]]
[[!redirects exponentiable functor]]
[[!redirects exponentiable functors]]
[[!redirects strict Conduche functors]]
[[!redirects strict Conduche functors]]
[[!redirects strict Conduché functor]]
[[!redirects strict Conduché functors]]
[[!redirects strictly exponentiable functor]]
[[!redirects strictly exponentiable functors]]
[[!redirects powerful functor]]
[[!redirects powerful functors]]
[[!redirects strictly powerful functor]]
[[!redirects strictly powerful functors]]
