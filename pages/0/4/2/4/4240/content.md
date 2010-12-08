# Quandles
* table of contents
{: toc}


##The Idea##

A quandle is a set equipped with a binary operation satisfying axioms analogous to the three [[Reidemeister moves]] in knot theory.  A quandle is a special case of a [[rack]].  

While mainly used to obtain invariants of [[knot|knots]], quandles are interesting algebraic structures in their own right. In particular, the definition of a quandle axiomatizes the properties of conjugation in a group.  More abstractly, we can say that a quandle is an algebraic structure where every element acts as an automorphism of that structure, fixing that element.


##Definition##

A **quandle** is a [[rack]] obeying the law

$$ a \triangleright a = a $$

or equivalently

$$a \triangleleft a = a \, .$$

In other words, a quandle is a set $Q$ equipped with two binary operations, $\triangleright$ and $\triangleleft$, obeying the laws:

\[ a \triangleright (b \triangleright c) = (a \triangleright b)\triangleright (a \triangleright  c)   \]

\[ (c \triangleleft b) \triangleleft a = (c \triangleleft a)\triangleleft (b \triangleleft a)  \]

\[ (a \triangleright b)\triangleleft a = b \]

\[ a \triangleright (b \triangleleft a) = a \]

\[    a \triangleright a = a \]

\[  a \triangleleft a = a  \]

Given laws 3 and 4, the operation $\triangleright$ determines the operation $\triangleleft$, and vice versa, and then law 1 is equivalent to law 2, while law 5 is equivalent to law 6.  So, this definition has a certain redundancy built in.  See [[rack]] for more discussion of related points.

##Examples##

Every [[group]] gives a quandle where the operations come from conjugation:

$$ a \triangleright b = a b a^{-1}$$
$$ b \triangleleft a = a^{-1} b a $$

In fact, every equational law satisfied by [[conjugation]] in a group follows from the quandle axioms.  So, one can think of a quandle as what is left of a group when we forget multiplication, the identity, and inverses, and only remember the operation of conjugation.

Every tame knot in $\mathbb{R}^3$ has a "fundamental quandle".  To define this, one can note that the [[fundamental group]] of the knot complement, or [[knot group]], has a presentation (the [[Wirtinger presentation]]) in which the relations only involve conjugation.  So, this presentation can also be used as a presentation of a quandle.  The fundamental quandle is a very powerful invariant of knots.  In particular, if two knots have [[isomorphism|isomorphic]] fundamental quandles then there is a [[homeomorphism]] of $\mathbb{R}^3$, possibly orientation reversing, taking one knot to the other.   

Less powerful but more easily computable invariants of knots may be obtained by counting the homomorphisms from the knot quandle to a fixed quandle $Q$.  Since the Wirtinger presentation has one generator for each strand in a [[knot diagram]], these invariants can be computed by counting ways of labelling each strand by an element of $Q$, subject to certain constraints easily read off from a diagram of the knot.  More sophisticated invariants of this sort can be constructed with the help of quandle [[cohomology]].

The Alexander quandles are also important, since they can be used to compute the [[Alexander polynomial]] of a knot.  Let $A$ be a module over the ring  $\mathbb{Z}[t, t^{-1}]$ of [[Laurent polynomial|Laurent polynomials]] in one variable. Then the **Alexander quandle** consists of $A$ made into a quandle with the left action given by

$$a \triangleright b = t a + (1-t)b $$

[[rack|Racks]] are a useful generalization of quandles in topology, since while quandles can represent knots on a round linear object (such as rope or a thread), racks can represent ribbons, which may be twisted as well as knotted.

A quandle $Q$ is said to be **involutory** if it obeys the law

$$ a \triangleright (a \triangleright b) = b $$

or equivalently

$$ (b \triangleleft a) \triangleleft a = b$$

Any [[symmetric space]] gives an involutory quandle, where $a \triangleright b$ is the result of 'reflecting $b$ through $a$'.
In fact this leads to an elegant definition of symmetric spaces.  Note that involutory quandles are algebras of a certain [[Lawvere theory]], since [[rack|racks]] are already algebras of a Lawvere theory, and involutory quandles are racks obeying some extra equational laws.  We may thus define involutory quandle objects in any [[category]] with finite [[products]], such as the category of [[smooth manifolds]].  Loos has shown that a connected symmetric space is the the same as an involutory quandle object $Q$ in the category of smooth manifolds with the additional properties that:

* each point $a$ is an _isolated_ fixed point of the operation $a \triangleright -$.  

* $Q$ is connected.  

This fact is Theorem I.4.3. in:

* Wolgang Bertram, _The Geometry of Jordan and Lie Structures_, Lecture Notes in Mathematics **1754**, Springer, Berlin, 2000.

He attributes this result to:

* Ottmar Loos, _Symmetric Spaces I_, Chapter II, Benjamin, New York, 1969.

[[!redirects quandles]]




## References ##

* Gavin Wraith, [A personal story about knots](http://www.wra1th.plus.com/gcw/rants/math/Rack.html).

* Sam Nelson, [Quandle theory](http://www.esotericka.org/pomona/quandles.html).

* J. Scott Carter, [A survey of quandle ideas](http://arxiv.org/abs/1002.4429).

* Seiichi Kamada, [Knot invariants derived from quandles and racks](http://arxiv.org/abs/math/0211096).

* J. Scott Carter and Masahico Saito, [Quandle homology theory and cocycle knot invariants](http://arxiv.org/abs/math/0112026).

* Alissa Crans, [Shelves, racks, spindles and quandles](http://arxiv.org/PS_cache/math/pdf/0409/0409602v1.pdf#page=56), in _Lie 2-Algebras_.

The last reference makes it clear that quandles are algebras of a [[Lawvere theory]], so that quandles may be defined in any [[cartesian monoidal category]] (a category with finite [[products]]).  It also shows that any Lie algebra gives a quandle in the category of cocommutative [[coalgebra|coalgebras]].


[[!redirects quandle]]
[[!redirects quandles]]
