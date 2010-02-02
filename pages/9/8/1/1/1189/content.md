# Definition

In material [[set theory]], a [[pure set]] $S$ is called __transitive__ if $a\in b\in S$ implies that $a\in S$.  Note that this does _not_ mean that $\in$ is a transitive binary relation on $S$ itself.  (In fact, assuming the [[axiom of foundation]], $\in$ is a transitive relation on $S$ precisely when $S$ is a von Neumann [[ordinal number]].)

Transitive sets are a natural place to look for [[inner model]]s of material set theory: that is, sets $S$ such that $S$ together with the restriction of $\in$ to $S$ satisfies some or all of the axioms of set theory.  This is especially so because of [[Mostowski's collapsing lemma]] that any [[extensional relation|extensional]] [[well-founded relation]] is isomorphic to a transitive set.

# Transitive closures

In [[ZFC]], one can prove that every pure set $x$ is contained in a least transitive pure set, called its **transitive closure**.  This can be defined as the set of all $y$ such that there is a chain $y = x_n \in \cdots \in x_0 = x$ for some [[natural number]] $n$.  The proof that this set exists requires the [[axiom of replacement]] and the property of [[induction]] for unbounded formulas (which follows from the [[axiom of separation]]).  In set theories that are too weak to prove the existence of transitive closures in this way, their existence is sometimes assumed explicitly.

# Modeling pure sets  

Given the existence of transitive closures, pure sets can be identified with subsets of transitive sets, and hence (given Mostowski's lemma) with subsets of extensional well-founded relations.  This latter characterization is complete structural, and thus can be used to model [[pure set]]s in [[structural set theory]].

category: foundational axiom

[[!redirects transitive sets]]
[[!redirects transitive closure]]
[[!redirects transitive closures]]
