In material [[set theory]], the __axiom of foundation__, also called the __axiom of regularity__, states that the membership relation $\in$ on the proper class of all [[pure set]]s is [[well-founded relation|well-founded]].  In structural set theory, accordingly, one uses well-founded relations in building structural models of well-founded pure sets.

# Statement #

Given a proper class $A$ of [[pure set]]s, suppose that $A$ has the property that, given any pure set $x$,
$$ \forall t,\; t \in x \Rightarrow t \in A ,$$
then $x \in A$.  Such an $A$ may be called a _membership-inductive_ class.  Then the __axiom of foundation__ states that the only membership-inductive class of pure sets is the class of all pure sets.

Although the statement here refers to proper classes, it can also be formulated as an axiom schema that makes no mention of classes.

# Alternative formulations #

While the statement above follows how the axiom of foundation is generally *used* ---to prove properties of pure sets by [[transfinite induction]]---, it is complicated.  Two alternative formulations are given by the following lemmas:

1. The axiom of foundation holds if and only if there exists no infinite descending [[sequence]] $\cdots \in x_2 \in x_1 \in x_0$.

1. The axiom of foundation holds if and only if every [[inhabited set|inhabited]] pure set $A$ has a member $x \in A$ such no $t \in A$ satisfies $t \in x$.  (Such an $x$ is called a _membership-minimal_ element of $A$.)

Lemma (1) is essentially a transfinite version of Fermat\'s method of _infinite descent_.  Lemma (2) is favoured by set theorists as a statement of the axiom, since it uses neither higher-order reasoning (as our first definition does) or infinity (as infinite descent does).

However, neither of these is acceptable in [[constructive mathematics]].  This is because both lemmas require the principle of [[excluded middle]] to prove one direction.  Thus the nonexistence of infinite descending sequences is too weak to allow proofs by transfinite induction (except for special forms of $A$), while the requirement that every inhabited pure set have a minimal element is unnecessarily strong and itself implies excluded middle.

# Anti-foundation #

Most of set theory works without the axiom of foundation, but not the deep study of well-founded pure sets.  However, one might want to do material set theory without assuming that all sets are well-founded, then one would not assume this axiom.

Alternatively, one can adopt the __axiom of anti-foundation__, which says something like:

* Given any binary [[relation]] $\prec$ on any [[set]] $S$, there exists a unique [[transitive set]] $U$ such that $(U,\in)$ is [[isomorphism|isomorphic]] to $(S,\prec)$.

(This might be wrong, so somebody should fix it.  There might also be several versions or equivalent forms.)

Note that the converse of this is obvious.  If you include the hypothesis that $\prec$ be [[well-founded relation|well-founded]], then the statement is a theorem but the converse is the axiom of foundation.

If you adopt the axiom of anti-foundation instead of foundation, then the universe of [[pure set]]s becomes the [[corecursion|corecursively]] defined ill-founded sets instead of the [[recursion|recursively]] defined well-founded sets.

category: foundational axiom