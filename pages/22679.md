+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}



## Definitions

Classically:
 +-- {: .num_defn #classical}
###### Definition

A **division rig** is a [[rig]] in which every nonzero element has a multiplicative [[inverse]] and $0 \neq 1$ (which may be combined as: an element is invertible if and only if it is nonzero).
=--

### Constructive notions
{#constructive}

Division rigs are (arguably) not a purely [[algebra|algebraic]] notion in that they don\'t form an [[algebraic category]] (see [discussion below](#category)).  For this reason, it should be unsurprising that in [[constructive mathematics]] (including the [[internal logic]] of a [[topos]]) there are different inequivalent ways to define a division rig.  In this case the classical definition is not usually the best one; for instance, the non-negative real numbers do not satisfy it. There are several potential replacements with their own advantages and disadvantages.

+-- {: .num_defn #discrete}
###### Definition

If we replace "an element is invertible iff it is nonzero" in Definition \ref{classical} by "an element is invertible [[xor]] it equals zero" (which is equivalent in [[classical logic]] but stronger in [[constructive logic]]), then we obtain the notion of **discrete division rig**.  This condition means that every element is either $0$ or invertible, and it also implies that $0\neq 1$.
=--

Such a division rig $R$ is 'discrete' in that it decomposes as a coproduct $R = \{0\} \sqcup R^\times$ (where $R^\times$ is the subset of invertible elements).  An advantage is that this is a [[coherent logic|coherent theory]] and hence also a [[geometric theory]].  A disadvantage is that this axiom is not satisfied (constructively) by the rig of non-negative [[real numbers]] (however these are defined), although it is satisfied by the rig of non-negative [[rational number|rational]].

+-- {: .num_defn #heyting}
###### Definition

If we interpret 'nonzero' in Definition \ref{classical} as a reference to a [[tight apartness relation]], thus defining the apartness relation $\#$ by $x # y$ iff $x - y$ is invertible, then we obtain the notion of **Heyting division rig**, where the rig operations become strongly extensional functions.  In addition to $0\# 1$, the condition then means that every element apart from $0$ is invertible.
=--

This is how 'practising' constructive analysts of the Bishop school usually define the simple word 'division rig'.  An advantage is that the (located Dedekind) non-negative [[real numbers]] form a Heyting division rig, although (for example) the (less located) non-negative [[MacNeille real number]]s need not form a Heyting division rig; another disadvantage is that this is not a coherent axiom and so cannot be [[internalization|internalized]] in as many categories.

Every discrete division rig is also a Heyting division rig. A Heyting division rig is a discrete division rig if and only if [[decidable equality|equality is decidable]]; it is in this sense that a discrete division rig is 'discrete'.

## Examples
 {#Examples}

+-- {: .num_example}
###### Example

There are the division rigs of:

* non-negative [[rational numbers]],

* non-negative [[real numbers]],

* all [[division rings]], such as [[fields]]

* for a division rig $R$, all $R$-[[division algebras]]

=--

## Related concepts

* [[rig]], [[integral cancellable rig]]

* [[division ring]]

* [[field]]

[[!redirects division rig]]
[[!redirects division rigs]]

[[!redirects commutative division rig]]
[[!redirects commutative division rigs]]