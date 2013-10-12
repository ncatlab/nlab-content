
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Quantum physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _Jordan-Lie-Banach algebra_ (or _JLB-algebra_ for short) is a [[topology|topological]] [[algebra]] that behaves like a [[Poisson algebra]], only that the commutative product is not required to form an [[associative algebra]], but just a [[Jordan algebra]]. Hence a _JLB-algebra_ is a _nonassociative Poisson algebra_ with topology.

JLB-algebras are the outcome of [[quantization]] of [[Poisson algebra]]s. Often that outcome is regarded to be a non-commutative but associative [[C-star-algebra]]. But any such induces a JLB-algebra by letting the Jordan product be the symmetrized product and the Lie bracket the [[commutator]]. There is a condition relating the [[associator]] of the JLB-algebra to the Lie bracket, that characterizes those JLB-algebras that come from non-commutative associative algebras, and in the usual definition of JLB-algebra this condition is required. In that case JLB-algebras are effectively the same as $C^*$-algebras, the only difference being that the single assocative product is explcitly regarded as inducing the two products of a non-associative Poisson algebra.


## Definition

A __JLB-algebra__ (over the [[real numbers]]) consists of a [[Banach space]] $A$ equipped with two [[short linear operator|short]] [[bilinear operator]]s $(-)\circ(-)$ and $(-)\bullet(-)$, called the _Jordan product_ and the _Lie product_, satisfying the following identities:

* Jordan commutativity: $x \circ y = y \circ x$;
* Lie anticommutativity: $x \bullet x = 0$, or equivalently (given bilinearity) $x \bullet y = -y \bullet x$;
* the Jacobi identity (Lie self-derivation): $x \bullet (y \bullet z) = (x \bullet y) \bullet z + y \bullet (x \bullet z)$, or equivalently (given anticommutativity) $x \bullet (y \bullet z) + y \bullet (z \bullet x) + z \bullet (x \bullet y) = 0$;
* Jordan derivation: $x \bullet (y \circ z) = (x \bullet y) \circ z + y \circ (x \bullet z)$;
* the associator identity: $(x \circ y) \circ z - x \circ (y \circ z) = ((x \bullet z) \bullet y)$;
* the $B$-identity: ${\|x \circ x\|} = {\|x\|^2}$ (compare the $B^*$-identity or $C^*$-identity of a $C^*$-[[C-star-algebra|algebra]]);
* positivity: ${\|x \circ x \|} \leq {\|x \circ x + y \circ y\|}$.

This definition is adapted from Section 1.1 of [Halvorson, 1999](#Halvorson1999).  Halvorson does not include the statement that the Lie multiplication is short, and it includes a nonnegative real constant factor $r$ on the right-hand side of the associator identity.  However, Halvorson claims to construct an equivalence between real JLB-algebras and complex $C^*$-[[C*-algebra|algebras]], and this construction produces a short Lie product that satisfies $r = 1$.

Another consequence of this definition is that the Jordan product makes $A$ into a [[Jordan algebra]] (and hence into a [[JB-algebra]]).


## References

A careful definition is in section 1.1 of 

* [[Hans Halvorson]], _Maximal Beable Subalgebras of
Quantum-Mechanical Observables_ ([pdf](http://philsci-archive.pitt.edu/65/1/beables.pdf))
  {#Halvorson1999}

A brief remark is on p. 80 of

* Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)
 {#BatesWeinstein}


[[!redirects Jordan-Lie-Banach algebra]]
[[!redirects Jordan-Lie-Banach algebras]]
[[!redirects Jordan–Lie–Banach algebra]]
[[!redirects Jordan–Lie–Banach algebras]]
[[!redirects Jordan--Lie--Banach algebra]]
[[!redirects Jordan--Lie--Banach algebras]]
[[!redirects JLB algebra]]
[[!redirects JLB algebras]]
[[!redirects JLB-algebra]]
[[!redirects JLB-algebras]]

[[!redirects Jordan-Lie algebra]]
[[!redirects Jordan-Lie algebras]]
[[!redirects Jordan–Lie algebra]]
[[!redirects Jordan–Lie algebras]]
[[!redirects Jordan--Lie algebra]]
[[!redirects Jordan--Lie algebras]]
[[!redirects JL algebra]]
[[!redirects JL algebras]]
[[!redirects JL-algebra]]
[[!redirects JL-algebras]]
