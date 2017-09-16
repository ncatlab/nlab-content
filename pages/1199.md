A (binary) [[relation]] $\prec$ on a [[set]] $S$ is called _well-founded_ if it is valid to do [[induction]] on $\prec$ over $S$.

# Definition #

Given a [[subset]] $A$ of $S$, suppose that $A$ has the property that, given any element $x$ of $S$, if
$$ \forall (t: S),\; t \prec x \Rightarrow t \in A ,$$
then $x \in A$.  Such an $A$ may be called a _$\prec$-inductive subset_ of $S$.  The relation $\prec$ is __well-founded__ if the only $\prec$-inductive subset of $S$ is $S$ itself.

# Examples #

Let $S$ be the set of [[natural number]]s, and let $x \prec y$ if $y$ is the [[successor]] of $x$: $y = x + 1$.  That this relation is well-founded is the usual principle of _mathematical induction_.

Again let $S$ be the set of natural numbers, but now let $x \prec y$ if $x \lt y$ in the usual order.  That this relation is well-founded is the principle of _strong induction_.

More generally, let $S$ be a set of [[ordinal number]]s (or even the proper class of all ordinal numbers), and let $x \prec y$ if $x \lt y$ in the usual order.  That this relation is well-founded is the principle of _transfinite induction_.

Let $S$ be the set of positive integers, and let $x \prec y$ mean that $x$ divides $y$: $x \mid y$, or $y/x$ is an integer.  This relation is also well-founded, so one can prove properties of integers by induction on their divisors.

# Alternative formulations #

While the definition above follows how a well-founded relation is generally *used* ---to prove properties of elements of $S$ by induction---, it is complicated.  Two alternative formulations are given by the following lemmas:

1. The relation $\prec$ is well-founded if and only if there exists no infinite descending [[sequence]] $\cdots \prec x_2 \prec x_1 \prec x_0$.

1. The relation $\prec$ is well-founded if and only if every [[inhabited set|inhabited]] subset $A$ of $S$ has a member $x \in A$ such no $t \in A$ satisfies $t \prec x$.  (Such an $x$ is called a _$\prec$-minimal_ element of $A$.)

Lemma (1) is essentially Fermat\'s method of _infinite descent_.  Lemma (2) is favoured as a definition by set theorists (particularly when stating the [[axiom of foundation]]), since it uses neither higher-order reasoning (as our first definition does) or infinity (as infinite descent does).

However, neither of these is acceptable in [[constructive mathematics]].  This is because both lemmas require the principle of [[excluded middle]] to prove one direction.  Thus the nonexistence of infinite descending sequences is too weak to allow proofs by induction (except for special forms of $A$), while the requirement that every inhabited subset have a minimal element is too strong to ever be established (except for degenerate cases of $S$).

# Remarks #

Every well-founded relation is [[irreflexive relation|irreflexive]]; that is, $x \nprec x$.  Sometimes one wants a reflexive version $\preceq$ of a well-founded relation; let $x \preceq y$ if and only $x \prec y$ or $x = y$.  Then the requirement that $x$ be a minimal element of a subset $A$ states that $t \preceq x$ only if $t = x$.  But infinite descent or direct proof by induction still require $\prec$ rather than $\preceq$.

A [[well-order|well order]] may be defined as a well-founded [[linear order]], or alternatively as a [[transitive relation|transitive]], [[extensional relation|extensional]], well-founded relation.

The [[axiom of foundation]] in material [[set theory]] states precisely that the membership relation $\in$ on the proper class of all [[pure set]]s is well-founded.  In structural set theory, accordingly, one uses well-founded relations in building structural models of well-founded pure sets.