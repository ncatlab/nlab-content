# Pre-Lie algebras
* table of contents
{: toc}


## Definition

A **pre-Lie algebra** is a [[vector space]] $A$ equipped with a bilinear operation $\cdot: A \times A \to A$ such that
\[      [L_a, L_b] = L_{[a,b]}  \label{basic_identity} \]
for all $a, b\in A$.  Here $L_a$ is the operation of left multiplication by $a$:
$$ L_a b = a \cdot b $$
and $[L_a, L_b]$ is the usual commutator of operators using [[composition]]:
$$ [L_a, L_b] = L_a L_b - L_b L_a $$
while $[a,b]$ is the commutator defined using the $\cdot$ operation:
\[ [a,b] = a \cdot b - b \cdot a  \label{torsion_free_identity} \]

Unravelling this, we see a pre-Lie algebra is vector space $A$ equipped with a bilinear operation $\cdot: A \times A \to A$ such that
\[ a \cdot (b \cdot c) - b \cdot (a \cdot c) = 
(a \cdot b) \cdot c - (b \cdot a) \cdot c  \label{identity} \]
More precisely, this is a **left** pre-Lie algebra.  We can also define right pre-Lie algebras.

Every [[associative algebra]] is a pre-Lie algebra, but not conversely.  The reason pre-Lie algebras have the name they do is that this weakening of the concept of associative algebra is still enough to give a [[Lie algebra]]!  In other words: it is well-known that if $A$ is an associative algebra, the operation
$$  [a,b] = a \cdot b - b \cdot a $$
makes $A$ into a Lie algebra.  But this is also true for pre-Lie algebras!  It is a fun exercise to derive the Jacobi identity from equation \eqref{identity}.


## Examples

First, given a [[manifold]] with a flat torsion-free [[connection]] $\nabla$ on its [[tangent bundle]], we can make the space of [[tangent vector fields]] into a pre-Lie algebra by defining
$$  v \cdot w = \nabla_v w $$
The definition of 'flat' is precisely \eqref{basic_identity}, whereas that of 'torsion-free' is precisely \eqref{torsion_free_identity}.  The Lie algebra arising from this pre-Lie algebra is just the usual Lie algebra of vector fields.


Second, suppose $O$ is a [[linear operad]], and let $A$ be the free $O$-[[algebra of an operad|algebra]] on one generator.  As a vector space we have
$$  A = \bigoplus_{n} O_n/S_n \, .$$
Here $S_n$ is the [[symmetric group]], which acts on the space $O_n$ of $n$-ary operations of $O$.  Moreover, $A$ becomes a pre-Lie algebra in a manner described here:

* Dominique Manchon, [A short survey on pre-Lie algebras](http://math.univ-bpclermont.fr/~manchon/biblio/ESI-prelie2009.pdf)

Third, the [[Hochschild cohomology|Hochschild]] [[chain complex]] of any associative algebra, with grading shifted down by one, can be given the structure of a '[[graded object|graded]] pre-Lie algebra', as discovered by Gerstenhaber and described here:

* Justin Thomas, [Graduate student seminar: Hochschild cohomology](http://www.math.northwestern.edu/~jdthomas/Talk%20Notes/Hoch%20Cohomology.pdf)

In fact it was Gerstenhaber who coined the term 'pre-Lie algebra', for this reason.

## Relation to the work of Connes and Kreimer

Connes and Kreimer formalized the process of [renormalization](http://ncatlab.org/nlab/show/renormalization#hopfalgebraic_renormalization_3) using a certain [[Hopf algebra]] built from Feynman diagrams.  More abstractly we can understand the essence of their construction using a Hopf algebra built from rooted trees, as explained here:

* John Baez, This Week's Finds in Mathematical Physics, Week 299.  ([web](http://math.ucr.edu/home/baez/week299.html))  ([blog](http://golem.ph.utexas.edu/category/2010/06/this_weeks_finds_in_mathematic_60.html))

The key is to form the free pre-Lie algebra on one generator, then turn this into a Lie algebra as described above, and then form the universal enveloping of that, which is a cocommutative Hopf algebra.  Finally, the restricted dual of this cocommutative Hopf algebra is the commutative Hopf algebra considered by Connes and Kreimer here:

* Alain Connes and Dirk Kreimer, Hopf algebras, renormalization and noncommutative geometry, _Commun. Math. Phys._ **199** (1998), 203--242 ([arXiv](http://arxiv.org/abs/hep-th/9808042))

Pre-Lie algebras are algebras of a [[linear operad]] called $PL$.  The space $PL_n$ has a basis given by labelled rooted [[trees]] with $n$ vertices, and the $i$th partial composite $s \circ_i t$ is given by summing all the possible ways of inserting the tree $t$ inside the tree $s$ at the vertex labelled $i$.  For details see:

* Fr&#233;d&#233;ric Chapoton, Muriel Livernet, Pre-Lie algebras and the rooted trees operad, _Int. Math. Res. Not._ 2001 (2001), 395-408.

The free pre-Lie algebra on one generator is thus
$$\bigoplus_{n} PL_n /S_n  \, $$
so the description of $PL_n$ in terms of rooted trees gives a kind of 'explanation' of the relation between the Connes--Kreimer Hopf algebra and rooted trees.

## Self-referentiality ##

Pre-Lie algebras have a strange self-referential feature.  Every operad of a large class gives a pre-Lie algebra, but the operad for pre-Lie algebras is one of this class!  This raises the following interesting puzzle.

As we have seen above, for any linear operad $O$, the free $O$-algebra with one generator becomes a pre-Lie algebra.  But the operad for pre-Lie algebra is an operad of this type.  So, the free pre-Lie algebra on one generator becomes a pre-Lie algebra in this way.   But of course it already *is* a pre-Lie algebra!  Do these pre-Lie structures agree?

The answer is no.  For an explanation, see page 7 here:

* Dominique Manchon, A short survey on pre-Lie algebras.  ([pdf](http://math.univ-bpclermont.fr/~manchon/biblio/ESI-prelie2009.pdf))

## References ##

The best overall introduction to pre-Lie algebras seems to be that by Dominique Manchon, cited above.  For two more introductions, try:

* John Baez, This Week's Finds in Mathematical Physics, Week 299.  ([web](http://math.ucr.edu/home/baez/week299.html))  ([blog](http://golem.ph.utexas.edu/category/2010/06/this_weeks_finds_in_mathematic_60.html))

* Fr&#233;d&#233;ric Chapoton, Operadic point of view on the Hopf algebra of rooted trees.  ([pdf](http://www-math.unice.fr/~patras/CargeseConference/ACQFT09_FredericCHAPOTON.pdf))

