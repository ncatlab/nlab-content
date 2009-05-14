A **local ring** is a ring (with unit, usually also assumed commutative) such that:
* $0 \ne 1$; and
* whenever $a + b = 1$, $a$ or $b$ is invertible.

Here are a few equivalent ways to phrase the combined condition:
* Whenever a (finite) sum equals $1$, at least one of the summands is invertible.
* Whenever a sum is invertible, at least one of the summands is invertible.
* Whenever a sum of products is invertible, for at least one of the summands, all of its multiplicands are invertible).
* The non-invertible elements form an [[ideal]].  (Unlike the previous clauses, this requires [[excluded middle]] to be equivalent.)

The ideal of non-invertible elements is in fact a [[maximal ideal]], so the [[quotient object|quotient ring]] is a field.  (This quotient can also be taken constructively, where one mods out by an anti-ideal.)

Local rings are often more useful than fields when doing mathematics [[internalization|internally]]. For one thing, the definition make sense in any [[coherent category]]. But unlike the definition of discrete field (see [[field]]), which is also coherent, it is satisfied by rings such as the ring of (located Dedekind) real numbers. Rather than mod out by the ideal of non-invertible elements, you take care to use only properties that are invariant under multiplication by an invertible element.

In [[constructive mathematics]], one could do the same thing, but it\'s more common to use the notion of Heyting field (again, see [[field]]). This is closely related, however; the quotients of local rings are precisely the Heyting fields (which are themselves local rings). In fact, one can define an [[apartness relation]] (like that on a Heyting field) in any local ring: $x \# y$ iff $x - y$ is invertible. Then the local ring is a Heyting field if and only if this apartness relation is [[tight relation|tight]].