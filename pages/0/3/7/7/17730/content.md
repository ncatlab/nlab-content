#Contents#
* Contents
{:toc}

## Idea

Systems of iterated inductive definitions are important formal systems introduced by Feferman, especially in regards to proof-theoretic investigation. They are obviously related as well to [[inductive types]] in [[type theory]].

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

Note that $(ID_1)^1$ expresses that $I_A$ is closed under the arithmetically definable set operator $\Gamma_A(S) = \{ x\in\mathbb{N} \mid \mathbb{N} \vDash A(S,x) \}$, while $(ID_1)^2$ expresses that $I_A$ is the least such (at least among sets definable in $\mathcal{L}_{ID_1}$.

### Iterated inductive definitions

It is possible to define systems of finitely iterated inductive definitions by simply repeating the process of adding a level of inductive definitions and extending the existing schemas to the new language. However, to define the transfinitely iterated variants another approach is needed.

To define the system of $\nu$-times iterated inductive definitions, where $\nu$ is an [[ordinal]], let ${\prec$} be a well-ordering of order type $\nu$. The language of $ID_\nu$, $\mathcal{L}_{ID_\nu}$ is obtained from $\mathcal{L}_{\mathbb{N}}$ by the addition of a constant for ${\prec$} and a binary predicate constant $J_A$ for every $X$-positive $\mathcal{L}_{\mathbb{N}}$ formula $A(X,Y,x,y)$ that contains at most the shown free variables. We write $a\in J_A^b$ instead of $J_A(a,b)$ and $a\in J_A^{\prec b}$ for the formula $\exists y\prec b. a\in J_A^y$.

The system $ID_\nu$ is now obtained from the system of first-order number theory by expanding the induction scheme to the new language and adding
the scheme
\[
  (TI_\nu)\qquad
  LO({\prec}) \wedge TI({\prec},F)
\]
expressing transfinite induction along ${\prec}$ for an arbitrary $\mathcal{L}_{ID_\nu}$ formula $F$ as well as
\[
  (ID_\nu)^1\qquad
  \forall y\in field({\prec}). \forall x.
  A(J_A^y,J_A^{\prec y},x,y) \to x\in J_A^y
\]
and
\[
  (ID_\nu)^2\qquad
  \forall y\in field({\prec}).
  (\forall x. A(B,J_A^{\prec y},x,y) \to B(x))
  \to \forall x. x\in J_A^y \to B(x)
\]
where $B(x)$ is an arbitary $\mathcal{L}_{ID_\nu}$ formula.

(work in progress)