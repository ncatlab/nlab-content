#Contents#
* Contents
{:toc}

## Idea

Systems of iterated inductive definitions are important formal systems introduced by Feferman (1970), especially of use in proof-theoretic investigations. They are obviously related as well to [[inductive types]] in [[type theory]].

Below we record the main definitions and proof-theoretic results about these systems. See also the table at [[ordinal analysis]].

## Definition

### Non-iterated case

Let us begin by the case of a non-iterated inductive definition, as incarnated in the system ID$_1$, which axiomatizes the least fixed point of an arithmetically definable positive inductive definition.

The language of $ID_1$, $\mathcal{L}_{ID_1}$, is obtained from that of first-order number theory, $\mathcal{L}_{\mathbb{N}}$, by the addition of a set (or predicate) constant $I_A$ for every $X$-positive formula $A(X,x)$ in $\mathcal{L}_{\mathbb{N}}$ that only contains $X$ (a set variable) and $x$ (a number variable) as free variables.

Then $ID_1$ contains the axioms of first-order number theory with the induction scheme extended to the new language as well as the axiom
\[
  (ID_1)^1\qquad
  \forall x. A(I_A, x) \to x \in I_A
\]
and the scheme
\[
  (ID_1)^2\qquad
  (\forall x. A(B,x) \to B(x)) \to \forall x. x\in I_A \to B(x)
\]
where $B(x)$ ranges over all $\mathcal{L}_{ID_1}$-formulas.

Note that $(ID_1)^1$ expresses that $I_A$ is closed under the arithmetically definable set operator $\Gamma_A(S) = \{ x\in\mathbb{N} \mid \mathbb{N} \vDash A(S,x) \}$, while $(ID_1)^2$ expresses that $I_A$ is the least such (at least among sets definable in $\mathcal{L}_{ID_1}$).

### Iterated inductive definitions

It is possible to define systems of finitely iterated inductive definitions by simply repeating the process of adding a level of inductive definitions and extending the existing schemas to the new language. It's important that the constants $I_A$ for the previous levels may occur negatively in the operators for the later levels. So these systems can be defined in stages by (metamathematical) induction on $\mathbb{N}$. However, to define the transfinitely iterated variants another approach is needed.

To define the system of $\nu$-times iterated inductive definitions, where $\nu$ is an [[ordinal]], let ${\prec}$ be a well-ordering of order type $\nu$. The language of $ID_\nu$, $\mathcal{L}_{ID_\nu}$ is obtained from $\mathcal{L}_{\mathbb{N}}$ by the addition of a binary predicate constant $J_A$ for every $X$-positive $\mathcal{L}_{\mathbb{N}}$ formula $A(X,Y,x,y)$ that contains at most the shown free variables. We write $a\in J_A^b$ instead of $J_A(a,b)$ and $a\in J_A^{\prec b}$ for the formula $\exists y\prec b. a\in J_A^y$.

The system $ID_\nu$ is now obtained from the system of first-order number theory by expanding the induction scheme to the new language and adding
the scheme
\[
  (TI_\nu)\qquad
  TI({\prec},F)
\]
expressing transfinite induction along ${\prec}$ for an arbitrary $\mathcal{L}_{ID_\nu}$ formula $F$ as well as the axiom
\[
  (ID_\nu)^1\qquad
  \forall y\in field({\prec}). \forall x.
  A(J_A^y,J_A^{\prec y},x,y) \to x\in J_A^y
\]
and the scheme
\[
  (ID_\nu)^2\qquad
  \forall y\in field({\prec}).
  (\forall x. A(B,J_A^{\prec y},x,y) \to B(x))
  \to \forall x. x\in J_A^y \to B(x)
\]
where $B(x)$ is an arbitary $\mathcal{L}_{ID_\nu}$ formula.

Intuitively, $(ID_\nu)^1$ and $(ID_\nu)^2$ express that each $J_A^y$, for $y\in field({\prec})$, is the least fixed point (among definable sets) for the operator $\Gamma_y(X) = \{ n\in\mathbb{N} \mid \mathbb{N} \vDash A(X,J_A^{\prec y},n,y) \}$.

It is for instance possible to define the constructive number classes $\mathcal{O}_\mu$ for $\mu\le\nu$ in $ID_\nu$.

We define $ID_{\prec\nu} = \bigcup_{\xi\prec\nu} ID_\xi$.

## Proof-theoretic results

See [[ordinal analysis]] for the proof-theoretic results concerning the $ID_\nu$ and $ID_{\prec\nu}$ systems.

## References

* Buchholz, Feferman, Pohlers and Sieg: Iterated inductive definitions and subsystems of analysis: recent proof-theoretical studies, Lecture Notes in Mathematics 897 (1981).

* Feferman: Formal theories for transfinite iterations of generalized inductive definitions and some subsystems of analysis. In: Intuitionism and Proof Theory (Proc. Conf., Buffalo, N.Y., 1968). 1970.

* Feferman: The proof theory of classical and constructive inductive definitions, a 40 year saga, 1968-2008. In: Ways of Proof Theory. 2013. [pdf](https://math.stanford.edu/~feferman/papers/id-saga.pdf)

* Pohlers: Subsystems of Set Theory and Second Order Number Theory. In: Handbook of Proof Theory. 1998.
