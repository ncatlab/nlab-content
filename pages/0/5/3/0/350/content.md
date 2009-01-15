# Idea

A Lawvere&#8211;Tierney topology (or operator, or modality, also called _geometric modality_) is a way of saying that something is 'locally' true. Unlike a [[Grothendieck topology]], this is done directly at the stage of [[logic]], defining a _geometric logic_.

# Definition

Let $E$ be a [[topos]], with [[subobject classifier]] $\Omega$. A __Lawvere&#8211;Tierney topology__ in $E$ is a map $j: \Omega \to \Omega$ that satisfies certain axioms. If $C$ is any [[category]], a __Lawvere&#8211;Tierney topology__ on $C$ is a Lawvere&#8211;Tierney topology in the topos $\Set^{C^\op}$ of [[presheaf|presheaves]] on $C$.

+--{.query}
Am I using the prepositions correctly? These are both things that one may want to say, but I\'m not sure how one is meant to distinguish them.
=--

The axioms say that $j$ is ([[internalization|internally]]) a [[left exact functor|left exact]] [[monad]] on the internal meet-semi[[lattice]] $\Omega$. To be explicit:
* $\id_\Omega \leq j: \Omega \to \Omega$ ('if $p$ is true, then $p$ is locally true');
* $j \circ j = j: \Omega \to \Omega$ ('$p$ is locally locally true iff $p$ is locally true');
* $j \circ \wedge = \wedge \circ j \times j: \Omega \times \Omega \to \Omega$ ('$p \wedge q$ is locally true iff $p$ and $q$ are each locally true').

Here $\leq$ is the internal [[partial order]] on $\Omega$, and $\wedge: \Omega \times \Omega \to \Omega$ is the internal [[meet]].

Given any [[subobject]] inclusion $X \hookrightarrow Y$ in $E$, consider its [[characteristic morphism]] $\chi_X: Y \to \Omega$. Then $\chi_X \circ j$ is another morphism $Y \to \Omega$, which defines another subobject $j_*(X)$ of $Y$. The elements of $j_*(X)$ are those elements of $Y$ that are 'locally' in $X$.

# Sheaves

... how to tell if an object of $E$ (or a presheaf on $C$) is a sheaf ... iff it is uniquely defined when consistently 'locally' defined ...

# Remarks

A special case of a Lawvere&#8211;Tierney topology on a category $C$ is a [[Grothendieck topology]] on $C$. Given a [[subpresheaf]] inclusion $F \hookrightarrow G$ in $\Set^{C^\op}$, an object $X$ of $C$, and an element $f$ of $G(X)$, $f$ is locally in $F$ (that is, $f \in j_*(F)(X)$) if and only if, for some [[cover]] $c = (c_i: U_i \to X)_i$ of $X$, the restriction $c^*(f)$ of $f$ to $c$ is in $F$ (that is, each $c_i^*(f) \in F(U_i)$).

+--{.query}
Is this always right? Or does it only work when $F, G$ are actually sheaves?
=--

As a specific example, take the usual Grothendieck topology on [[Top]], given by the usual notion of open cover. Taking real-valued functions on a space defines a presheaf (in fact a sheaf) $G: X \mapsto [X,R]$ on $\Top$; the constant functions form a subpresheaf $F$ of $G$. A real-valued function $f: X \to R$ belongs to $j_*(F)$ iff it is *locally* constant; that is, for some open cover $(U_i)_i$ of the domain $X$, each restriction $f|U_i$ is constant.