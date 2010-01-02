# Definition

A **generic proof** in a [[category]] $C$ is a map $\theta\colon \Theta\to\Lambda$ such that for every map $f\colon Y\to X$, there exists a (not necessarily unique) map $\nu\colon X\to \Lambda$ such that $f$ and $v^*\theta$ each factor through each other, i.e. they are equivalent in the [[preorder reflection]] of the [[slice category]] $C/X$.

The main interest of generic proofs is in the following:

+-- {: .un_theorem}
###### Theorem
If $C$ has [[finite limits]], then its [[ex/lex completion]] $C_{ex/lex}$ is a [[topos]] if and only if $C$ has [[weak dependent product]]s and a generic proof.
=--

In particular, if $C$ is a [[locally cartesian closed category]], then $C_{ex/lex}$ is a topos if and only if $C$ has a generic proof.

A counterpart of generic proofs in [[type theory]] is Russell's [[axiom of reducibility]].

# Axioms of choice

If $C$ is a [[topos]] satisfying the [[axiom of choice]], then its [[subobject classifier]] is a generic proof, since any $f\colon Y\to X$ factors through, and (assuming AC) is factored through by, its [[image]], a subobject of $X$.  In fact, for such a $C$, $C_{ex/lex}$ is equivalent to $C$.

The statement "$Set$ has a generic proof," or equivalently "$Set_{ex/lex}$ is a topos," seems, at least *a priori*, to be weaker than the full axiom of choice.

A (seemingly) even weaker statement is "$Set_{ex/lex}$ is [[well-powered category|well-powered]]."  Note that if $X$ is a set, then the subobject lattice of (the image of) $X$ in $Set_{ex/lex}$ is precisely the preorder reflection of $C/X$; thus this second statement says in particular that all such preorder reflections are essentially small.  This can be regarded as saying that although full AC may not hold, it is only violated in a "small way" at each set.  It is sufficient, for instance, to show that the category of [[anafunctors]] between two small categories is essentially small.


# References

* Mat&#237;as Menni, "Exact completions and toposes", Ph.D. Thesis
