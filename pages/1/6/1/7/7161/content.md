## Idea

The notion of groupoid object is a horizontal categorification of a [[group object]].  Equivalently, it is an [[internal category]] which is a [[groupoid]] (in the appropriate internal sense.

## Definitions

Let $C$ be a [[category with finite limits]], and let $\Grpd$ be the category of small [[groupoids]].   We can define groupoid objects representably:

+-- {: .un_defn}
###### Definition

A **groupoid object in** $C$ is a functor $F\colon C\to \Grpd$ such that

1. there is an object $g_0\in C_0$ such that there is a [[natural isomorphism]] $F(c)_0\simeq C(c,g_0)$

1. there is an object $g_1\in C_0$ such that there is a natural isomorphism $F(c)_1\simeq C(c,g_1)$
=--

We can also define them more explicitly:

+-- {: .un_defn}
###### Definition
A **groupoid object in** $C$ is an [[internal category]] $A$ such that there is an "inverse-assigning morphism" $i\colon A_1 \to A_1$ satisfying certain axioms...
=--

## Examples

* A groupoid in $\Top$ is a [[topological groupoid]].

* A groupoid in $\Diff$ is a [[Lie groupoid]].  (Note that $\Diff$ does not have all pullbacks, but by suitable conditions on the source and target map we can ensure that the requisite pullbacks do exist.)


## Related concepts

* [[monoid]], [[monoid object]], [[monoid object in an (∞,1)-category]]

* [[group]], **group object**, [[group object in an (∞,1)-category]]

* [[groupoid]], [[groupoid object]], [[groupoid object in an (∞,1)-category]]

* [[infinity-groupoid]], [[infinity-groupoid object]], [[groupoid object in an (∞,1)-category]]

* [[ring]], [[ring object]]
