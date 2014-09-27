
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

A _Jordan--Lie--Banach algebra_ (or _$JLB$-algebra_ for short) is a [[topological vector space|topological]] [[nonassociative algebra|algebra]] that behaves like a [[Poisson algebra]], only that the commutative product is not required to form an [[associative algebra]], but just a [[Jordan algebra]]. Hence a _$JLB$-algebra_ is a _nonassociative Poisson algebra_ with [[topological structure|topology]].

JLB-algebras are the outcome of [[quantization]] of [[Poisson algebras]]. In traditional [[strict deformation quantization]] that outcome is regarded to be a non-commutative but associative [[C-star-algebra]]. But any such induces a JLB-algebra by letting the Jordan product be the symmetrized product and the [[Lie bracket|Lie product]] the [[commutator]] (times $\mathrm{i}/2$). There is a condition relating the [[associator]] of the JLB-algebra to the Lie bracket, that characterizes those JLB-algebras that come from non-commutative associative algebras, and in the usual definition of JLB-algebra this condition is required. In that case JLB-algebras are effectively the same as $C^*$-algebras, the only difference being that the single assocative product is explcitly regarded as inducing the two products of a non-associative Poisson algebra. For more on this separation of the Lie-algebra and the Jordan algebra aspect of quantization see at _[[order-theoretic structure in quantum mechanics]]_.


## Definition

A __JLB-algebra__ (over the [[real numbers]]) consists of a [[Banach space]] $A$ equipped with two [[short linear operator|short]] [[bilinear operator]]s $(-)\circ(-)$ and $(-)\bullet(-)$, respectively called the _Jordan product_ and the _Lie product_, satisfying the following identities:

* Jordan commutativity: $x \circ y = y \circ x$;
* Lie anticommutativity: $x \bullet x = 0$, or equivalently (given bilinearity) $x \bullet y = -y \bullet x$;
* the Jacobi identity (Lie self-derivation): $x \bullet (y \bullet z) = (x \bullet y) \bullet z + y \bullet (x \bullet z)$, or equivalently (given anticommutativity) $x \bullet (y \bullet z) + y \bullet (z \bullet x) + z \bullet (x \bullet y) = 0$;
* Jordan derivation: $x \bullet (y \circ z) = (x \bullet y) \circ z + y \circ (x \bullet z)$;
* the associator identity: $x \circ (y \circ z) = (x \circ y) \circ z + y \bullet (x \bullet z)$, or equivalently (given anticommutativity) $(x \circ y) \circ z - x \circ (y \circ z) = (x \bullet z) \bullet y$;
* the $B$-identity: ${\|x \circ x\|} = {\|x\|^2}$ (compare the $B^*$-identity or $C^*$-identity of a $C^*$-[[C-star-algebra|algebra]]);
* positivity: ${\|x \circ x \|} \leq {\|x \circ x + y \circ y\|}$.

This definition is adapted from Section 1.1 of [Halvorson, 1999](#Halvorson1999).  Halvorson does not include the statement that the Lie multiplication is short, and it includes a nonnegative real constant factor $r$ on the right-hand side of the associator identity (second version).  However, Halvorson claims to construct an equivalence between real $JLB$-algebras and complex $C^*$-[[C*-algebra|algebras]], and this construction produces a short Lie product that satisfies $r = 1$.

Another consequence of this definition is that the Jordan product makes $A$ into a [[Jordan algebra]] (and hence into a [[JB-algebra]]).

While we\'re at it let\'s define a __$JLBW$-algebra__ to be a $JLB$-algebra whose underlying Banach space is equipped with a [[predual]].


## Equivalence to $C^*$-algebras

The Jordan product and Lie product are respectively the real-symmetrized and imaginary-antisymmetrized parts of an associative operation on the [[complexification]] of $A$, defining a complex $C^*$-[[C-star-algebra|algebra]]; and every $C^*$-algebra likewise defines a JLB-algebra consisting of its [[Hermitian operator|Hermitian]] elements.

Specifically, starting with a JLB-algebra $A$, we write $A \oplus A$ formally as $A + \mathrm{i} A$, on which we define the following operations:

* norm: ${\|a + \mathrm{i} b\|} \coloneqq \sqrt{{\|a\|^2} + {\|b\|^2}}$,
* addition: $(a + \mathrm{i} b) + (c + \mathrm{i} d) \coloneqq (a + c) + \mathrm{i} (b + d)$,
* opposite: $-(a + \mathrm{i} b) \coloneqq (-a) + \mathrm{i} (-b)$,
* zero: $0 \coloneqq 0 + \mathrm{i} 0$,
* scalar multiplication: $(x + \mathrm{i} y) (a + \mathrm{i} b) = (x a - y b) + \mathrm{i} (x b + y a)$ (for $x + \mathrm{i} y$ a [[complex number]]),
* involution: $(a + \mathrm{i} b)^* \coloneqq a + \mathrm{i} (-b)$,
* multiplication: $(a + \mathrm{i} b) (c + \mathrm{i} d) \coloneqq (a \circ c + a \bullet d + b \bullet c - b \circ d) + \mathrm{i} (-a \bullet c + a \circ d + b \circ c + b \bullet d)$.

If the Jordan product of the JLB-algebra has an identity $1$, then so does the $C^*$-algebra:

* $1 \coloneqq 1 + \mathrm{i} 0$.

Conversely, starting with a $C^*$-algebra $A$, we form the subspace $sa(A) = \{x\colon A \;|\; x^* = x\}$, on which we define the following operations (under each of which $sa(A)$ is closed):

* norm, addition, opposite, zero, scalar multiplication (by [[real numbers]] only): by [[restriction]],
* Jordan product: $a \circ b \coloneqq \frac{1}{2} a b + \frac{1}{2} b a$,
* Lie product: $a \bullet b \coloneqq \frac{1}{2} \mathrm{i} a b - \frac{1}{2} \mathrm{i} b a$.

If the $C^*$-algebra has an identity, then this is also an identity for the Jordan product (so $1$ is also defined by restriction).

This all defines a [[functor]] each way between the [[groupoids]] of $C^*$-algebras and $JLB$-algebras, which in fact (I hope!) form an [[equivalence of categories|adjoint equivalence]].  Since we have a notion of [[morphism]] (not just [[isomorphism]]) of $C^*$-algebras, we can transport this along the equivalence to get a notion of morphism of $JLB$-algebras (which I would expect to be a short linear map that preserves both products) and thus a [[category]] $JLB Alg$ equivalent to $C^* Alg$.

Then real $JLBW$-algebras are equivalent to complex $W^*$-[[W-star-algebra|algebras]].


## References

A definition is in section 1.1 of 

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

[[!redirects JLBW algebra]]
[[!redirects JLBW algebras]]
[[!redirects JLBW-algebra]]
[[!redirects JLBW-algebras]]
