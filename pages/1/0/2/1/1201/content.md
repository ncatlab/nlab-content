
# The axiom of foundation
* table of contents
{: toc}

In material [[set theory]], the __axiom of foundation__, also called the __axiom of regularity__, states that the membership relation $\in$ on the proper class of all [[pure set]]s is [[well-founded relation|well-founded]].  In structural set theory, accordingly, one uses well-founded relations in building structural models of well-founded pure sets.


## Statement

Given a proper class $A$ of [[pure set]]s, suppose that $A$ has the property that, given any pure set $x$,
$$ \forall t,\; t \in x \Rightarrow t \in A ,$$
then $x \in A$.  Such an $A$ may be called a _membership-inductive_ class.  Then the __axiom of foundation__ states that the only membership-inductive class of pure sets is the class of all pure sets.  In this form, the axiom of foundation is also called *$\in$-induction*.

Although the statement here refers to proper classes, it can also be formulated as an axiom schema that makes no mention of classes.


## Alternative formulations

While the statement above follows how the axiom of foundation is generally *used* ---to prove properties of pure sets by [[transfinite induction]]---, it is complicated.  Two alternative formulations are given by the following lemmas:

+-- {: .num_lemma #InfiniteDescent}
###### Lemma
The axiom of foundation holds if and only if there exists no infinite descending [[sequence]] $\cdots \in x_2 \in x_1 \in x_0$.
=--
+-- {: .proof}
###### Proof
First, suppose the axiom of foundation holds, and suppose there were such a sequence.  Let $A$ be the class of all sets which are not equal to $x_i$ for any $i$.  Then for any $x$, if $x$ were equal to some $x_i$, then some $t\in x$ would also be equal to some $x_j$, namely $x_{i+1}$; hence if all $t\in x$ are in $A$, so is $x$.  Thus, by the axiom of foundation, all sets are in $A$, a contradiction.

Second, suppose there are no such sequences, and let $A$ be as in the statement of foundation.  Suppose that $A$ does not contain all sets.  Then there exists an $x_0\notin A$.  By hypothesis on $A$, there must exist an $x_1\in x_0$ such that $x_1 \notin A$.  And hence an $x_2\in x_1$ such that $x_2 \notin A$, and so on, producing an infinite descending $\in$-sequence in contradiction to our hypothesis; hence $A$ must contain all sets.
=--

This is essentially a version of Fermat\'s method of [[infinite descent]] modified to apply to [[transfinite induction]] instead of only to ordinary [[induction]].  It arguably provides the most direct intuitive picture of what the axiom means.  Note that as a special case, it implies that no set can contain itself, since then $\cdots \in x\in x\in x$ would be an infinite chain.

+-- {: .num_lemma #MembershipMinimal}
###### Lemma
The axiom of foundation holds if and only if every [[inhabited set|inhabited]] pure set $x$ has a member $y \in x$ such that no $t \in x$ satisfies $t \in y$.  (Such a $y$ is called a _membership-minimal_ element of $x$.)
=--
+-- {: .proof}
###### Proof
First, suppose the axiom of foundation holds, let $x$ be a pure set without a membership-minimal element, and let $A = \{ y | y\notin x \}$.  If $z$ is a set such that all $t\in z$ are in $A$, then we cannot have $z\in x$, since then we would have some $t\in z$ with $t\in x$ and hence $t\notin A$; hence $z\in A$.  So $A$ satisfies the assumptions of the foundation axiom, and hence $x$ is empty.

Second, suppose that every inhabited pure set has a membership-minimal element, and let $A$ be as in the statement of foundation.  Since every pure set is contained in a [[transitive set]], it suffices to show that $A \cap x = x$ for any transitive $x$.  Let $y = \{ z\in x \mid z \notin A \}$.  If $y$ is inhabited, then it contains a membership-minimal element $z$, i.e. we have $z\in x$, $z\notin A$, and for every $t\in z$ we have $t\notin z$---but $t\in x$ since $x$ is transitive, hence $t\in A$.  Thus this $z$ contradicts the assumption on $A$, so $y$ must be empty, as desired.
=--

This version is favoured by [[classical mathematics|classical]] set theorists as a statement of the axiom, since it uses neither higher-order reasoning (as our first definition does) or infinity (as infinite descent does).

However, neither of these is acceptable in [[constructive mathematics]], since both lemmas require at least the principle of [[excluded middle]] to prove at least one direction.    In particular, the nonexistence of infinite descending sequences is too weak to allow proofs by transfinite induction (except for special forms of $A$), while the requirement that every inhabited pure set have a minimal element is unnecessarily strong and itself implies excluded middle.

More precisely, the necessary set-theoretic axioms for the above proofs are the following.  (Is it known, in any case, that proofs using fewer axioms don't exist?)

* The "only if" direction of Lemma \ref{InfiniteDescent} requires only the axiom of infinity (for "infinite sequence" to make sense).

* The "if" direction of Lemma \ref{InfiniteDescent} evidently requires the principle of excluded middle, the axiom of infinity, and the axiom of [[dependent choice]].  It also appears to require the [[axiom of collection]] (since dependent choice, as usually stated, only chooses elements from a sequence of nonempty *sets*, rather than nonempty classes), and a principle of [[induction]] strong enough to recursively construct functions into a [[proper class]] (which is usually proven using the [[axiom of separation]]) in order to put together these nonempty sets into a sequence we can apply dependent choice to.

* The "only if" direction of Lemma \ref{MembershipMinimal} requires only excluded middle.

* The "if" direction of Lemma \ref{MembershipMinimal} requires excluded middle, also that every set is contained in a transitive one (the [[axiom of transitive closure]], which follows from [[axiom of replacement|replacement]]), as well as the [[axiom of separation]] in the form "the intersection of any class with a set is a set."

Another version of the axiom of foundation which *is* intuitionistically acceptable, but makes no reference to proper classes is:

+-- {: .num_lemma #WFTransitive}
###### Lemma
The axiom of foundation holds if and only if the relation $\in$ on any [[transitive set]] is a [[well-founded relation]].
=--
+-- {: .proof}
###### Proof
Suppose the axiom of foundation holds, let $x$ be a transitive set, and let $S\subseteq x$ be such that for any $y\in x$, if all $t\in y$ are in $S$, then $y\in S$.  Let $A$ be the class of all sets $y$ such that if $y\in x$, then $y\in S$; then $A$ satisfies the conditions in the axiom of foundation, so it contains all sets, and hence $S=x$.

Now suppose $\in$ is well-founded on any transitive set and let $A$ satisfy the conditions in foundation.  Since every set is contained in a transitive one, it suffices to show that $A\cap x = x$ for any transitive $x$, but this follows directly from the assumption.
=--

In this case:

* The "only if" direction requires no notable axioms at all, while

* The "if" direction requires [[transitive closure]], as in Lemma \ref{MembershipMinimal}, and also the axiom of separation.

Finally, another commonly cited version of foundation, equivalent to it at least over the other axioms of [[ZF]], is:

+-- {: .num_lemma #CumulativeHierarchy}
###### Lemma
The axiom of foundation holds if and only if every pure set is an element of $V_\alpha$ for some [[ordinal]] $\alpha$.
=--

Here the $V_\alpha$ are the [[cumulative hierarchy]] defined by [[transfinite recursion]] as $V_\alpha = P(\bigcup_{\beta\lt \alpha} V_\beta)$.


## Anti-foundation

Most of set theory works without the axiom of foundation, but not the deep study of well-founded pure sets.  However, one might want to do material set theory without assuming that all sets are well-founded, then one would not assume this axiom.

Alternatively, one can adopt the __axiom of anti-foundation__, which says:

* Given any [[extensional relation|extensional]] [[binary relation]] $\prec$ on any [[set]] $S$, there exists a unique [[transitive set]] $U$ such that $(U,\in)$ is [[isomorphism|isomorphic]] (necessarily uniquely) to $(S,\prec)$.

Since any relation has an [[extensional quotient]], we may also phrase the axiom thus:

* Given any binary relation $\prec$ on any [[set]] $S$, there exists a unique [[transitive set]] $U$ and [[surjection]] $f : S \to U$ such that $f(s_1) \in f(s_2)$ if and only if $s_1 \in s_2$, for $s_1, s_2$ in $S$.  (That is, $f$ is almost an isomorphism between $(S, \prec)$ and $(U, \in)$, but needn't be [[injection|injective]].)

Just as there are several versions of an [[extensional relation]], there are several versions of this axiom.  Note that the existence part of the statement is a set-formation axiom, while the uniqueness part is a strong version of the [[axiom of extensionality]] (which is equivalent to the usual one for well-founded sets).

If you include the hypothesis that $\prec$ be [[well-founded relation|well-founded]], then the statement is a theorem ([[Mostowski's collapsing lemma]]), while the converse is the axiom of foundation.

If you adopt the axiom of anti-foundation (with the strongest notion of extensional relation) instead of foundation, then the universe of [[pure sets]] becomes the [[corecursion|corecursively]] defined ill-founded sets instead of the [[recursion|recursively]] defined well-founded sets.


## Structural meaning

Since the axiom of foundation is about pure sets, there seems little point to it in a [[structural set theory]].  However, it does have a structural consequence: every set $S$ is the underlying set of elements of a well-founded model for a pure set (in any of the ways described at [[pure set]]).  If one assumes the [[axiom of choice]], however, then this statement follows from the [[well-ordering theorem]], since in that case $S$ is the underlying set of a model for a von Neumann [[ordinal number]].  But the axiom of foundation has no stronger structural consequence, since this statement already suffices to ensure that a model of structural set theory can be reconstructed from the material set theory consisting of its well-founded pure sets.

That this statement is the correct structural version of antifoundation may be justified by appeal to the [[material-structural adjunction]].

## See also

* [[Mostowski's principle]]

## References

On [[non-wellfounded sets]] in [[homotopy type theory]]:

* [[Håkon Robbestad Gylterud]], [[Elisabeth Stenholm]], [[Niccolò Veltri]], *Terminal Coalgebras and Non-wellfounded Sets in Homotopy Type Theory* &lbrack;[arXiv:2001.06696](https://arxiv.org/abs/2001.06696)&rbrack;

category: foundational axiom, logic

[[!redirects axiom of foundation]]

[[!redirects axiom of anti-foundation]]
[[!redirects axiom of antifoundation]]
[[!redirects anti-foundation]]
[[!redirects antifoundation]]

[[!redirects axiom of regularity]]

[[!redirects membership induction]]
[[!redirects membership-induction]]

[[!redirects wellfounded set]]
[[!redirects wellfounded sets]]

[[!redirects well-founded set]]
[[!redirects well-founded sets]]

[[!redirects nonwellfounded set]]
[[!redirects nonwellfounded sets]]

[[!redirects non-wellfounded set]]
[[!redirects non-wellfounded sets]]

[[!redirects non-well-founded set]]
[[!redirects non-well-founded sets]]

[[!redirects wellfounded set theory]]
[[!redirects wellfounded set theories]]

[[!redirects well-founded set theory]]
[[!redirects well-founded set theories]]

[[!redirects nonwellfounded set theory]]
[[!redirects nonwellfounded set theories]]

[[!redirects non-wellfounded set theory]]
[[!redirects non-wellfounded set theories]]

[[!redirects non-well-founded set theory]]
[[!redirects non-well-founded set theories]]
