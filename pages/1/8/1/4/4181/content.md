# Pre-Lie algebras
* table of contents
{: toc}


## Definition

A **pre-Lie algebra** is a [[vector space]] $A$ equipped with a bilinear operation $\cdot: A \times A \to A$ such that
\[      [L_a, L_b] = L_{[a,b]}  \label{basic_identity} \]
for all $a, b\in A$, where $L_a$ is the operation of left multiplication by $a$:
$$ L_a b = a \cdot b $$
and $[L_a, L_b]$ is the usual commutator of operators using [[composition]]:
$$ [L_a, L_b] = L_a L_b - L_b L_a $$
while $[a,b]$ is the commutator defined using the $\cdot$ operation:
$$ [a,b] = a \cdot b - b \cdot a$$

Unravelling this, we see a pre-Lie algebra is vector space $A$ equipped with a bilinear operation $\cdot: A \times A \to A$ such that
\[ a \cdot (b \cdot c) - b \cdot (a \cdot c) = 
(a \cdot b) \cdot c - (b \cdot a) \cdot c  \label{identity} \]
More precisely, this is a **left** pre-Lie algebra.  We can also define right pre-Lie algebras.

Every [[associative algebra]] is a pre-Lie algebra, but not conversely.  The reason pre-Lie algebras have the name they do is that this weakening of the concept of associative algebra is still enough to give a [[Lie algebra]]!  In other words: it is well-known that if $A$ is an associative algebra, the operation
$$  [a,b] = a \cdot b - b \cdot a $$
makes $A$ into a Lie algebra.  But this is also true for pre-Lie algebras!  It is a fun exercise to derive the Jacobi identity from equation \eqref{identity}.


## Examples

First, given a [[manifold]] with a torsion-free [[connection]] $\nabla$ on its [[tangent bundle]], we can make the space of [[tangent vector fields]] into a pre-Lie algebra by defining
$$  v \cdot w = \nabla_v w $$
The definition of 'torsion-free' is precisely \eqref{basic_identity}.  The Lie algebra arising from this pre-Lie algebra is just the usual Lie algebra of vector fields.

Second, suppose $O$ is a linear [[operad]] whose space of unary operations is $1$-dimensional, and let $A$ be the free $O$-[[algebra of an operad|algebra]] on one generator.  As a vector space we have
$$  A = \bigoplus_{n \ge 0} O_n $$
Moreover, $A$ becomes a pre-Lie algebra in a manner described here:

* Dominique Manchon, [A short survey on pre-Lie algebras](http://math.univ-bpclermont.fr/~manchon/biblio/ESI-prelie2009.pdf)

+-- {: .query}
Is the condition on the space of unary operations really necessary???
=--

Third, the Hochschild [[chain complex]] of any space, with grading shifted down by one, can be given the structure of a '[[graded object|graded]] pre-Lie algebra', as discovered by Gerstenhaber and described here:

* Justin Thomas, [Graduate Student Seminar: Hochschild Cohomology](http://www.math.northwestern.edu/~jdthomas/Talk%20Notes/Hoch%20Cohomology.pdf)

In fact it was Gerstenhaber who coined the term 'pre-Lie algebra', for this reason.

## Relation to the work of Connes and Kreimer

The Connes--Kreimer Hopf algebra (or maybe its dual???) is a connected cocommutative [[Hopf algebra]], and thus by a theorem of Milnor and Moore it is the [[universal enveloping algebra]] of a Lie algebra.  This Lie algebra comes from a pre-Lie algebra, and this pre-Lie algebra is simply the free pre-Lie algebra on one generator.

Pre-Lie algebras are algebras of a [[linear operad]] called $PL$.  As usual, then, the free pre-Lie algebra on one generator is, as a vector space, the direct sum 

$$\bigoplus_{n \ge 0} PL_n $$

The space $PL_n$ has a basis given by labelled rooted [[trees]] with $n$ vertices, and the $i$th partial composite $s \circ_i t$ is given by summing all the possible ways of inserting the tree $t$ inside the tree $s$ at the vertex labelled $i$.  For details see:

* Fr&#233;d&#233;ric Chapoton, Muriel Livernet, Pre-Lie algebras and the rooted trees operad, _Int. Math. Res. Not._ 2001 (2001), 395-&#8211;408.

This gives a kind of 'explanation' of the relation between the Connes--Kreimer Hopf algebra and rooted trees.

## Self-referential mysteries ##

Note the following strange self-referential features of the pre-Lie operad, which raise some interesting puzzles:

As we have seen above, any linear operad $O$ with a 1d space of unary operations gives a pre-Lie algebra $\bigoplus O_n$.  But the operad for pre-Lie algebras, $PL$, is an operad of this type!  So, $\bigoplus PL_n$ is a pre-Lie algebra.   This in turn gives a Lie algebra.  What is this Lie algebra?

Also, since $\bigoplus PL_n$ is a pre-Lie algebra, there is action of $PL$ on $\bigoplus PL_n$.  How does this look, explicitly?