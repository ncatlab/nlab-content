#Contents#
* Contents
{:toc}

## Idea

Systems of iterated inductive definitions are important formal systems introduced by Feferman (1970), especially of use in proof-theoretic investigations. They are obviously related as well to [[inductive types]] in [[type theory]].

Below we record the main definitions and proof-theoretic results about these systems. See also the table at [[ordinal analysis]].

## Definition

### Non-iterated case

Let us begin by the case of a non-iterated inductive definition, as incarnated in the system ID$_1$, which axiomatizes the least fixed point of an arithmetically definable positive inductive definition.

A subset $I \subseteq \mathbb{N}$ is called inductively defined if it is the least fixed point of a monotone operator $\Gamma : \mathcal{P}(\mathbb{N}) \to \mathcal{P}(\mathbb{N})$. In order to formalize this situation relative to first-order number theory, we consider operators $\Gamma_A$ defined by positive operator forms.

The language of $ID_1$, $\mathcal{L}_{ID_1}$, is obtained from that of first-order number theory, $\mathcal{L}_{\mathbb{N}}$, by the addition of a set (or predicate) constant $I_A$ for every $X$-positive formula $A(X,x)$ in $\mathcal{L}_{\mathbb{N}}[X]$ that only contains $X$ (a new set variable) and $x$ (a number variable) as free variables. The term _$X$-positive_ means that $X$ only occurs positively in $A$. If we take the background logic to be constructive, it is common to require that $X$ only occurs _strictly_ positively (never to the left of an implication).

We allow ourselves a bit of set-theoretic notation, and we consider formulas $F(x)$ in a distinguished free variable $x$ to represent the subclass $\{ x\in\mathbb{N} \mid F(x) \}$. We write $s\in F$ to mean $F(s)$, and if $F$ and $G$ are two such formulas, we write $F \subseteq G$ to mean $\forall x. F(x) \to G(x)$.

Then $ID_1$ contains the axioms of first-order number theory with the induction scheme extended to the new language as well as the axiom
\[
  (ID_1)^1\qquad
  A(I_A) \subseteq I_A
\]
and the scheme
\[
  (ID_1)^2\qquad
  A(F) \subseteq F \to I_A \subseteq F
\]
where $F(x)$ ranges over all $\mathcal{L}_{ID_1}$-formulas.

Note that $(ID_1)^1$ expresses that $I_A$ is closed under the arithmetically definable set operator $\Gamma_A(S) = \{ x\in\mathbb{N} \mid \mathbb{N} \vDash A(S,x) \}$, while $(ID_1)^2$ expresses that $I_A$ is the least such (at least among sets definable in $\mathcal{L}_{ID_1}$).

Thus, $I_A$ is meant to be the least pre-fixed-point, and hence the least fixed point of the operator $\Gamma_A$.

### Iterated inductive definitions

It is possible to define systems of finitely iterated inductive definitions by simply repeating the process of adding a level of inductive definitions and extending the existing schemas to the new language. It's important that the constants $I_A$ for the previous levels may occur negatively in the operators for the later levels. So these systems can be defined in stages by (metamathematical) induction on $\mathbb{N}$. However, to define the transfinitely iterated variants another approach is needed.

To define the system of $\nu$-times iterated inductive definitions, where $\nu$ is an [[ordinal]], let ${\prec}$ be a primitive recursive well-ordering of order type $\nu$. We use Greek letters to denote elements of the field of ${\prec}$.

The language of $ID_\nu$, $\mathcal{L}_{ID_\nu}$ is obtained from $\mathcal{L}_{\mathbb{N}}$ by the addition of a binary predicate constant $J_A$ for every $X$-positive $\mathcal{L}_{\mathbb{N}}$[X,Y] formula $A(X,Y,\mu,x)$ that contains at most the shown free variables, where $X$ is again a unary (set) variable, and $Y$ is a fresh binary predicate variable. We write $x\in J_A^\mu$ instead of $J_A(\mu,x)$, thinking of $x$ as a distinguished variable in the latter formula.

The system $ID_\nu$ is now obtained from the system of first-order number theory by expanding the induction scheme to the new language and adding
the scheme
\[
  (TI_\nu)\qquad
  TI({\prec},F)
\]
expressing transfinite induction along ${\prec}$ for an arbitrary $\mathcal{L}_{ID_\nu}$ formula $F$ as well as the axiom
\[
  (ID_\nu)^1\qquad
  \forall\mu\prec\nu. A^\mu(J_A^\mu) \subseteq J_A^\mu
\]
and the scheme
\[
  (ID_\nu)^2\qquad
  \forall\mu\prec\nu.
  A^\mu(F) \subseteq F \to J_A^\mu \subseteq F
\]
where $F(x)$ is an arbitary $\mathcal{L}_{ID_\nu}$ formula. In $(ID_\nu)^1$ and $(ID_\nu)^2$ we used the abbreviation $A^\mu(F)$ for the formula $A(F, (\lambda\gamma y. \gamma\prec\mu \wedge y\in J_A^\gamma), \mu, x)$, where $x$ is the distinguished variable. We see that these express that each $J_A^\mu$, for $\mu\prec\nu$, is the least fixed point (among definable sets) for the operator $\Gamma_A^\mu(S) = \{ n\in\mathbb{N} \mid (\mathbb{N},(J_A^\gamma)_{\gamma\prec\mu}) \vDash A(S,(J_A^\gamma)_{\gamma\prec\mu},\mu,n) \}$. Note how all the previous sets $J_A^\gamma$, for $\gamma\prec\mu$, are used as parameters.

We define $ID_{\prec\nu} = \bigcup_{\xi\prec\nu} ID_\xi$.

## Examples

It is for instance possible to define the constructive ordinal number classes $\mathcal{O}_\mu$ for $\mu\le\nu$ in $ID_\nu$. Here we describe the simpler example of the constructive tree classes.

The first tree class $\mathcal{T}_0$ is a non-iterated inductive definition, which informally states that

* $0 \in \mathcal{T}_0$, and
* if $e$ is (the code of) a total recursive function enumerating elements of $\mathcal{T}_0$, then $e+1 \in \mathcal{T}_0$.

Elements of $\mathcal{T}_0$ represent $\mathbb{N}$-branching trees. Formally, $\mathcal{T}_0$ is represented by $I_A$ for the operator $A(X,x)$ defined by
\[
  x = 0 \vee (x \ne 0 \wedge \forall n. \{x-1\}(n) \in X).
\]

The higher tree classes $\mathcal{T}_\mu$, for $\mu\prec\nu$, are given by an iterated inductive definition, which informally states that

* $0 \in \mathcal{T}_\mu$, and
* if $e$ is (the code of) a total recursive function enumerating elements of $\mathcal{T}_\mu$, then $\langle 0,e\rangle \in \mathcal{T}_\mu$, and
* if $\gamma\prec\mu$ and $e$ is (the code of) a partial recursive function whose domain includes $\mathcal{T}_\gamma$ and whose values thereon are in in $\mathcal{T}_\mu$, then $\langle 1+\gamma,e\rangle \in \mathcal{T}_\mu$.

Now the elements represent infinite trees branching at each internal node over either $\mathbb{N}$ or one of the previous tree classes $\mathcal{T}_\gamma$, for $\gamma\prec\mu$.

To define these higher tree classes, consider the operator form $A(X,Y,\mu,x)$ defined by the disjunction of the corresponding three clauses:

* $x = 0$,
* $\exists e. x = \langle 0,e\rangle \wedge \forall n. \{e\}(n) \in X$,
* $\exists \gamma, e. \gamma \prec \mu \wedge x = \langle 1+\gamma,e\rangle \wedge \forall y \in Y^\gamma. \{e\}(y) \in X$.

In the last clause we used the class term $Y^\gamma$, thinking of $y$ in $Y(\gamma,y)$ as the distinguished variable.

## Proof-theoretic results

The book by Buchholz, Feferman, Pohlers and Sieg (1981) contains most proof-theoretic results concerning these systems. For example, the [[proof-theoretic ordinal]] of $ID_\nu$ is $\psi_\Omega(\varepsilon_{\Omega_\nu+1})$ for $\nu$ a limit ordinal, and that of $ID_{\prec\nu}$ is $\psi_\Omega(\Omega_\nu)$ when $\nu=\omega^\rho$ for $\rho$ a limit ordinal.

Girard (1982) gave another analysis of the $ID_\nu$ systems using what he calls $\Pi^1_2$-logic, making heavy use of [[dilators]].

See [[ordinal analysis]] for the relations between some of the $ID_\nu$ and $ID_{\prec\nu}$ systems and other systems.

## References

* Buchholz, Feferman, Pohlers and Sieg: Iterated inductive definitions and subsystems of analysis: recent proof-theoretical studies, Lecture Notes in Mathematics 897 (1981).

* Feferman: Formal theories for transfinite iterations of generalized inductive definitions and some subsystems of analysis. In: Intuitionism and Proof Theory (Proc. Conf., Buffalo, N.Y., 1968). 1970.

* Feferman: The proof theory of classical and constructive inductive definitions, a 40 year saga, 1968-2008. In: Ways of Proof Theory. 2013. [pdf](https://math.stanford.edu/~feferman/papers/id-saga.pdf)

* Girard: Proof-theoretic investigations of inductive definitions, I. In: Logic and algorithmic (Proc. Conf., Zurich, 1980). 1982.

* Pohlers: Subsystems of Set Theory and Second Order Number Theory. In: Handbook of Proof Theory. 1998.
