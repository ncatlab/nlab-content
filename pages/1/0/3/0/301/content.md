
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Classically, a __truth value__ is either $\top$ (True) or $\bot$ (False). (In [[constructive mathematics]], this is not so simple, although it still holds that any truth value that is not true is false.)

More generally, a __truth value__ in a [[topos]] $T$ is a morphism $1 \to \Omega$ (where $1$ is the [[terminal object]] and $\Omega$ is the [[subobject classifier]]) in $T$.  By definition of $\Omega$, this is equivalent to an (equivalence class of) monomorphisms $U\hookrightarrow 1$.  In a [[two-valued topos]], it is again true that every truth value is either $\top$ or $\bottom$, while in a [[Boolean topos]] this is true in the [[internal logic]].

Truth values form a [[partial order|poset]] (the __poset of truth values__) by declaring that $p$ precedes $q$ iff the [[conditional]] $p \to q$ is true.  In a topos $T$, $p$ precedes $q$ if the corresponding subobject $P\hookrightarrow 1$ is contained in $Q\hookrightarrow 1$.  Classically (or in a two-valued topos), one can write this poset as $\{\bot \to \top\}$.

The poset of truth values is a [[Heyting algebra]]. Classically (or internal to a Boolean topos), this poset is even a [[Boolean algebra]]. It is also a [[complete lattice]]; in fact, it can be characterised as the [[initial object|initial]] complete lattice. As a complete Heyting algebra, it is a [[frame]], corresponding to the one-point [[locale]].

When the set of truth values is equipped with the [[specialization topology]], the result is [[Sierpinski space]].

A truth value may be interpreted as a $0$-[[0-poset|poset]] or as a $(-1)$-[[(-1)-groupoid|groupoid]]. It is also the best interpretation of the term '$(-1)$-[[(-1)-category|category]]', although this doesn\'t fit all the patterns of the [[periodic table]].


## Related concepts

[[!include homotopy n-types - table]]

* Special properties of truth values:
  * In [[synthetic topology]] with a [[dominance]], some truth values are [[open truth value|open]].


[[!redirects truth value]]
[[!redirects truth values]]
[[!redirects truth-value]]
[[!redirects truth-values]]

[[!redirects proset of truth values]]
[[!redirects poset of truth values]]
[[!redirects lattice of truth values]]
[[!redirects algebra of truth values]]

[[!redirects boolean]]
[[!redirects booleans]]
