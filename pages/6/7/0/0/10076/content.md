
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Near-rings
* table of contents
{: toc}

## Idea

A near-ring is a sort of [[ring]] in which [[addition]] need not be commutative.  However, if we simply remove the commutativity of addition from the usual definition of a ring, then nothing changes, because we can prove commutativity from the other axioms: we have
$$ (x+y)(1+1) = x(1+1) + y(1+1) = x + x + y + y $$
and also
$$ (x+y)(1+1) = (x+y)1 + (x+y)1 = x + y + x + y. $$
Canceling $x$ on the left and $y$ on the right, we have $x+y=y+x$.

Thus, in order for the notion of near-ring to be different from that of a ring, we need to relax the [[distributivity law]] as well; we impose it only on one side.


## Definition

A **near-ring** is a set $R$ equipped with

1. A [[group]] structure $(R,+,0)$,

2. A [[monoid]] structure $(R,\cdot,1)$,

3. such that for any $x,y,z\in R$ we have $(x+y)\cdot z = (x\cdot z) + (y\cdot z)$, and for any $x\in R$ we have $0\cdot x = 0$.

If $(R,+,0)$ is only a monoid or semigroup, we say instead that $R$ is a **near-rig** or a **near-semiring**.  (Of course, now it is possible to have distributivity on both sides without making addition commutative, since addition need not always cancel.)

There is also a weaker notion, of __loop near ring__, where in the 
axioms above the group structure on $(R,+,0)$ is weakened to a [[loop (algebra)|loop]]
algebraic structure (i.e. left and right additive inverses no longer coincide and the associativity of addition is dropped).

## Internalization

Of course, near-rings can be defined [[internalization|internally]] to any [[cartesian monoidal category]].  More generally, they can be defined internally to a braided [[duoidal category]].

## References

* [wikipedia](en.wikipedia.org/wiki/Nearring)

For loop near rings see

* D. Ramakotaiah, C. Santhakumari. On loop near-rings.
Bull. Austral. Math. Soc. 19(3):417{435, 1978.

Loop near rings appear in topology:

* Damir Franeti&#269;, Petar Pave&#353;i&#263;, _Loop near-rings and unique decompositions of H-spaces_, [arxiv/1511.06168](http://arxiv.org/abs/1511.06168)


category: algebra

[[!redirects near-ring]]
[[!redirects near-rings]]
[[!redirects nearring]]
[[!redirects nearrings]]

[[!redirects near-rig]]
[[!redirects near-rigs]]
[[!redirects nearrig]]
[[!redirects nearrigs]]
