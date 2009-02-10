A [[coproduct]] $a+b$ in a [[category]] is **disjoint** if

1. the coprojections $a\to a+b$ and $b\to a+b$ are [[monomorphism|monic]], and 

1. their [[intersection]] is an [[initial object]].

Equivalently, this means we have [[pullback]] squares

$$
\array{ a & \to & a &&&
b & \to & b &&&
0 & \to & b\\
\downarrow && \downarrow &&&
\downarrow && \downarrow &&&
\downarrow && \downarrow \\
a & \to & a+b &&&
b & \to & a+b &&&
a & \to & a+b}
$$

An arbitrary coproduct $\coprod_i a_i$ is disjoint if each coprojection $a_i\to \coprod_i a_i$ is monic and the intersection of any two is initial.  Note that every 0-ary coproduct (that, is initial object) is disjoint.

Having disjoint (finite) coproducts is half of the condition for a category to be [[extensive category|extensive]].  Having all small disjoint coproducts is one of the conditions in Giraud's theorem characterizing [[Grothendieck topos|Grothendieck toposes]].

+--{: .query}
David Roberts says: This is probably a stupid question, but does the fact a coproduct $A\coprod B$ is disjoint imply that any map to it factors through either $A$ or $B$?  

Mike: No, it doesn't; consider the identity map of $A\coprod B$.  What is true is that if the coproduct is both disjoint and pullback-stable, then any map $X\to A\coprod B$ decomposes its domain $X$ as a coproduct $X_1\coprod X_2$, such that the given map is a coproduct of maps $X_1\to A$ and $X_2\to B$.  See [[extensive category]].

David R: Of course. And the intended application was something like a superextensive site - forming a Grothendieck pretopology with only singleton covering families from general covering families - so my question is more than answered.
=--

## Generalizations ##

A coproduct $a+b$ in a [[bicategory]] is disjoint if $a\to a+b$ and $b\to a+b$ are [[full and faithful functor|fully faithful]] and their [[comma object]] is initial.
