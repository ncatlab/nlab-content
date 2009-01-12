A **local ring** is a ring (with unit, usually also assumed commutative) such that:
* $0 \ne 1$; and
* whenever $a + b = 1$, $a$ or $b$ is invertible.

Here are a few equivalent ways to phrase the combined condition:
* Whenever a (finite) sum equals $1$, at least one of the summands is invertible.
* Whenever a sum is invertible, at least one of the summands is invertible.
* The invertible elements form an anti-[[ideal]] (which means that whenever a sum of products is invertible, for at least one of the summands, all of its multiplicands are invertible).

+--{.query}
The last equivalent phrase doesn\'t seem to follow in a noncommutative ring. Is there an accepted definition of noncommutative local ring, and if so, which (if either) of these is equivalent to it?

Reply to [[Toby Bartels|myself]]: Both Wikipedia and Planet Math say that it *does* follow, but they don\'t give proofs. I should at least check if the proof is constructive, so I can say something if it\'s not. (But I bet that it is.)
=--

As the invertible elements form an anti-ideal of a (commutative) local ring, the non-invertible elements form an ideal (since an ideal is simply the complement of an anti-ideal). This is in fact a maximal ideal, so the [[quotient object|quotient ring]] is a field.

Local rings are often more useful than fields when doing mathematics [[internalization|internally]]. For one thing, the definition make sense in any [[coherent category]]. But unlike the definition of discrete field (see [[field]]), which is also coherent, it is satisfied by rings such as the ring of (located Dedekind) real numbers. Rather than mod out by the ideal of non-invertible elements, you take care to use only properties that are invariant under multiplication by an invertible element.

In [[constructivism|constructive mathematics]], one could do the same thing, but it\'s more common to use the notion of Heyting field (again, see [[field]]). This is closely related, however; the quotients of local rings are precisely the Heyting fields (which are themselves local rings). In fact, one can define an [[apartness relation]] (like that on a Heyting field) in any local ring: $x \# y$ iff $x - y$ is invertible. Then the local ring is a Heyting field if and only if this apartness relation is tight.