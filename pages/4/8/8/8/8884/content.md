
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Zermelo--Fraenkel set theory with atoms
* table of contents
{: toc}

## Idea

**ZFA** is a variant of the [[material set theory]] [[ZF]] which allows for objects, called _atoms_ or _[[urelements]]_ (hence the alternative name ZFU), which may be members of [[sets]], but are not made up of other elements. ZFA featured in early independence proofs, notably [[Fraenkel-Mostowski permutation models]], for example showing AC is independent of the rest of the axioms of ZFA.

[[Zermelo|Zermelo's]] original 1908 axiomatisation of set theory included atoms, but they were soon discarded as a foundational approach as they could be modeled inside of atomless set theory.

## Definition

There are two possible approaches to formulating ZFA. In both cases, we can further require that the [[axiom of choice]] is satisfied, and obtain ZFCA.

### Empty atoms
In this approach, atoms are empty. We start by adding an additional unary predicate $A$, where we interpret $A(x)$ as saying "$x$ is an atom". We write $(\forall set x)$ to mean $\forall x, \neg A(x) \Rightarrow$, and similarly write $(\forall atom x)$ to mean $\forall x, A(x) \Rightarrow$.

Then the [[axiom of extensionality]] says
$$
  (\forall set x) (\forall set y) (\forall z, z \in x \Leftrightarrow z \in y)  \Rightarrow x = y,
$$
and the [[axiom of empty set]] says
$$
  (\exists set x) (\forall y) (y \notin x).
$$
We also add the axiom that says atoms are empty:
$$
  (\forall atom a) (\forall x) x \notin a.
$$
Sometimes it is also convenient to assume that we have a set of atoms:
$$
  (\exists X) (\forall x) (A(x) \Leftrightarrow x \in X),
$$
but in some cases, we might also like to consider models with a proper class of atoms.

### Reflexive/Quine atoms
We can give up on the [[axiom of foundation]], and introduce the urelements as [[reflexive sets]], ie. sets $x$ such that $x = \{x\}$. In place of the axiom of foundation, we can have an axiom of _weak_ foundation, where we require the existence of a set A such that every element of A is reflexive, and the [[cumulative hierarchy]] built up from $A$ is the whole universe. In other words, if we define

 * $R(0) = A$,

 * $R(\alpha + 1) = P(R(\alpha))$ for any ordinal $\alpha$,

 * $R(\lambda) = \bigcup_{\gamma \lt \lambda} R(\gamma)$ for $\lambda$ a limit ordinal,

then $V = \bigcup_\alpha R(\alpha)$.

## Models

### Fraenkel--Mostowski models
By allowing atoms in our models, we lend ourselves to the method of [[Fraenkel-Mostowski models]], where we can obtain models in which the [[axiom of choice]] fails by imposing some symmetry on the atoms (so that we cannot uniformly pick an atom out of many). Such models are closely related to [[categories of G-sets]].

## Related concepts

 * [[ZFC]]
 * [[Fraenkel-Mostowski models]]
 * [[permutation model]]
 * [[urelements]]

[[!redirects ZFA]]
[[!redirects ZFU]]
[[!redirects ZFCA]]
[[!redirects ZFAC]]
