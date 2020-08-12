
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

A Jordan--Lie algebra is a [[quantum deformation]] of a [[Poisson algebra]], consisting of a single [[vector space]] with compatible structures of both a [[Jordan algebra]] and a [[Lie algebra]].  If we add an appropriate [[topological structure]], then we get a Jordan--Lie--[[Banach algebra]], of which the $JLB$-algebras (corresponding to $C^*$-[[C-star algebra|algebras]]) and $JLBW$-algebras (corresponding to [[von Neumann algebras]]) are important special cases.

In traditional [[strict deformation quantization]] the outcome of [[quantization]] of [[Poisson algebras]] is regarded to be a non-commutative but associative complex $*$-[[star-algebra|algebra]] (such as a $C^*$-[[C-star-algebra|algebra]]). But any such induces a Jordan--Lie algebra (consisting of its [[self-adjoint elements]]) by letting the Jordan product be the symmetrized product and the [[Lie bracket|Lie product]] the [[commutator]] (times $\mathrm{i}/2$). There is a condition relating the [[associator]] of the Jordan product to the Lie product, which makes $JLB$-algebras effectively the same as $C^*$-algebras, the only difference being that the single associative product is explicitly regarded as inducing the two products of a $JLB$-algebra. For more on this separation of the Lie-algebra and the Jordan-algebra aspect of quantization see at _[[order-theoretic structure in quantum mechanics]]_.


## Definitions

Given a [[field]] $K$ and a scalar $h \in K$, a __Jordan--Lie algebra__ (over $K$ and $h$) consists of a [[vector space]] $A$ equipped with two [[bilinear operators]] $(-)\circ(-)$ and $(-)\bullet(-)$, respectively called the _Jordan product_ and the _Lie product_, satisfying the following identities:

* Jordan commutativity: $x \circ y = y \circ x$;
* the Jordan identity: $(x \circ y) \circ (x \circ x) = x \circ (y \circ (x \circ x))$;
* Lie anticommutativity: $x \bullet x = 0$, or equivalently (given bilinearity) $x \bullet y = -y \bullet x$;
* the Jacobi identity (Lie self-derivation): $x \bullet (y \bullet z) = (x \bullet y) \bullet z + y \bullet (x \bullet z)$, or equivalently (given anticommutativity) $x \bullet (y \bullet z) + y \bullet (z \bullet x) + z \bullet (x \bullet y) = 0$;
* Jordan derivation: $x \bullet (y \circ z) = (x \bullet y) \circ z + y \circ (x \bullet z)$;
* the associator identity: $x \circ (y \circ z) = (x \circ y) \circ z + h^2 y \bullet (x \bullet z)$, or equivalently (given anticommutativity) $(x \circ y) \circ z - x \circ (y \circ z) = h^2 (x \bullet z) \bullet y$.

If $K$ is a [[topological field]] (usually taken to be the field of [[real numbers]]), then a __Jordan--Lie--Banach algebra__ consists of a [[Banach space]] $A$ equipped with two [[bounded linear operator|bounded]] [[bilinear operators]] making $A$ into a Jordan--Lie algebra as above.

A __$JLB$-algebra__ is a Jordan--Lie--Banach algebra satisfying the following additional identities:

* the $B$-identity: ${\|x \circ x\|} = {\|x\|^2}$ (compare the $B^*$-identity or $C^*$-identity of a $C^*$-[[C-star-algebra|algebra]]);
* positivity: ${\|x \circ x \|} \leq {\|x \circ x + y \circ y\|}$.

A consequence of this definition is that the Jordan product makes $A$ into a [[JB-algebra]].  As with $JB$-algebras generally, the Jordan identity follows from the other axioms of a $JLB$-algebra and so may be left out of a direct definition.

Following the established terminology for $JB$-algebras, a _$JLC$-algebra_ may be defined as a *concrete* $JLB$-algebra, that is one equipped with a faithful representation (see [below](#representations)) on a [[Hilbert space]], or equivalently a real [[subalgebra]] of $SA(H)$ (see [below](#examples)) that is closed in the [[operator topology]].  However, like $C^*$-algebras (but unlike general $JB$-algebras), every $JLB$-algebra may be so represented and this term seems not to be used.

Finally, a __$JLBW$-algebra__ is a $JLB$-algebra with an [[identity element]] whose underlying Banach space is equipped with a (necessarily unique) [[predual]], and _$JLW$-algebra_ is further equipped with a faithful representation (or equivalently is a $JC$-algebra which includes the identity and is closed in the [[weak operator topology]]).  Again, every abstract algebra may be made concrete, although neither term seems to be established in the literature yet.


## Relation to Poisson algebras {#poisson}

If $h = 0$, then the Jordan product becomes associative, and the Jordan--Lie algebra becomes a [[Poisson algebra]].  Conversely, if $h \ne 0$, then dividing the Lie product by $h$ gives a Jordan--Lie algebra with $h = 1$.  In this way, a Jordan--Lie algebra may be seen as a [[quantum deformation]] of a Poisson algebra.  (In the [[physics|physical]] interpretation, $h$ here is the [[Dirac constant]] $\hbar$.)

Similarly, a Jordan--Banach algebra is a quantum deformation of a Poisson--Banach algebra (a Poisson algebra equipped with a Poisson bracket), and similarly for the more specialized versions.


## Relation to $C^*$-algebras {#cstar}

For a $JLB$-algebra with $h = 1$, the Jordan product and Lie product are respectively the real-symmetrized and imaginary-antisymmetrized parts of an associative operation on the [[complexification]] of $A$, defining a complex $C^*$-[[C-star-algebra|algebra]]; and every $C^*$-algebra likewise defines a $JLB$-algebra with $h = 1$ consisting of its [[Hermitian operator|Hermitian]] elements.

Specifically, starting with a $JLB$-algebra $A$, we write $A \oplus A$ formally as $A + \mathrm{i} A$, on which we define the following operations:

* norm: ${\|a + \mathrm{i} b\|} \coloneqq \sqrt{{\|a\|^2} + {\|b\|^2}}$,
* addition: $(a + \mathrm{i} b) + (c + \mathrm{i} d) \coloneqq (a + c) + \mathrm{i} (b + d)$,
* opposite: $-(a + \mathrm{i} b) \coloneqq (-a) + \mathrm{i} (-b)$,
* zero: $0 \coloneqq 0 + \mathrm{i} 0$,
* scalar multiplication: $(x + \mathrm{i} y) (a + \mathrm{i} b) = (x a - y b) + \mathrm{i} (x b + y a)$ (for $x + \mathrm{i} y$ a [[complex number]]),
* involution: $(a + \mathrm{i} b)^* \coloneqq a + \mathrm{i} (-b)$,
* multiplication: $(a + \mathrm{i} b) (c + \mathrm{i} d) \coloneqq (a \circ c + a \bullet d + b \bullet c - b \circ d) + \mathrm{i} (-a \bullet c + a \circ d + b \circ c + b \bullet d)$.

If the Jordan product of the $JLB$-algebra has an identity $1$, then so does the $C^*$-algebra:

* $1 \coloneqq 1 + \mathrm{i} 0$.

Conversely, starting with a $C^*$-algebra $A$, we form the subspace $sa(A) = \{x\colon A \;|\; x^* = x\}$, on which we define the following operations (under each of which $sa(A)$ is closed):

* norm, addition, opposite, zero, scalar multiplication (by [[real numbers]] only): by [[restriction]],
* Jordan product: $a \circ b \coloneqq \frac{1}{2} a b + \frac{1}{2} b a$,
* Lie product: $a \bullet b \coloneqq \frac{1}{2} \mathrm{i} a b - \frac{1}{2} \mathrm{i} b a$.

If the $C^*$-algebra has an identity, then this is also an identity for the Jordan product (so $1$ is also defined by restriction).

This all defines a [[functor]] each way between the [[groupoids]] of $C^*$-algebras and $JLB$-algebras with $h = 1$, which in fact (I hope!) form an [[equivalence of categories|adjoint equivalence]].  Since we have a notion of [[morphism]] (not just [[isomorphism]]) of $C^*$-algebras, we can transport this along the equivalence to get a notion of morphism of $JLB$-algebras (which I would expect to be a short linear map that preserves both products) and thus a [[category]] $JLB Alg$ equivalent to $C^* Alg$.

Then real $JLBW$-algebras are equivalent to complex $W^*$-[[W-star-algebra|algebras]].

If you start with a $JLB$-algebra with $h \ne 1$ (including $h = 0$, that is a Poisson $B$-algebra), then you can still get a complex $C^*$-algebra by modifying the definition of multiplication:
$$ (a + \mathrm{i} b) (c + \mathrm{i} d) \coloneqq (a \circ c + h a \bullet d + h b \bullet c - b \circ d) + \mathrm{i} (-h a \bullet c + a \circ d + b \circ c + h b \bullet d) .$$
Then if $h \ne 0$, you can recover the original $JLB$-algebra with a modified definition of the Lie product:
$$ a \bullet b \coloneqq \frac{1}{2h} \mathrm{i} a b - \frac{1}{2h} \mathrm{i} b a .$$

In particular, for a fixed $h \ne 0$, the category of $JLB$-algebras with one value of $h$ is equivalent to the category of $JLB$-algebras with another value of $h$ (since both are equivalent to complex $C^*$-algebras), but we have only a functor from $JLB$-algebras with $h = 0$ to any other category.


## Examples {#examples}

Any commutative [[associative algebra]] is a trivial example of a Jordan--Lie algebra with the Lie product set to [[zero]].  Similarly, any commutative [[Banach algebra]] is a Jordan--Lie--Banach algebra, any commutative $C^*$-[[C-star-algebra|algebra]] with trivial involution is a $JLB$-algebra, and any commutative $W^*$-[[W-star-algebra|algebra]] with trivial involution is a $JLBW$-algebra.  Note that the value of $h$ is irrelevant in these examples.

More interestingly, given any $C^*$-[[C-star-algebra|algebra]] (*not* assumed commutative or with trivial involution), the [[self-adjoint elements]] form a $JLB$-algebra with $h = 1$; if the original $C^*$-algebra is a $W^*$-[[W-star-algebra|algebra]], then the self-adjoint elements form a $JLBW$-algebra.  In fact, *every* $JLB$-algebra (including every $JLBW$-algebra) with $h = 1$ has this form (see [above](#cstar)).

More generally, given a $C^*$-[[C-star-algebra|algebra]] and $h \gt 0$, the self-adjoint elements form a $JLB$-algebra with this value of $h$ if we divide the Lie product by $h$.  In fact, every $JLB$-algebra with $h \gt 0$ has this form.

More specifically, given a [[Hilbert space]] $H$, the [[self-adjoint operators]] form a $JLBW$-algebra $SA(H)$ with $h = 1$.  In fact, *every* $JLB$-algebra (including every $JLBW$-algebra) with $h = 1$ is a subalgebra of some $SA(H)$; more generally, every $JLB$-algebra with $h \ne 0$ has this form upon dividing the Lie product by $h$.

As for $h = 0$, every [[Poisson algebra]] is a Jordan--Lie algebra with $h = 0$, and every Jordan--Lie algebra (including Jordan--Lie--Banach algebras etc) with $h = 0$ has this form.

Let $V$ be a (real) [[vector space]] of finite dimension $n$, which we will think of as the [[configuration space]] of a [[classical system]], and let $A$ be the [[symmetric algebra]] on the dual [[phase space]] $V \otimes V^* \cong \mathbb{R}^{2n}$.  We normally think of $A$ as consisting of (commutative) [[polynomials]] in the variables $q^1, \ldots, q^n, p_1, \ldots, p^n$, but let us now think of them as *noncommutative* polynomials consisting only of terms in which the variables come in order.  Fixing a scalar $h$, define the Jordan product on $A$ so that $q_i \circ q_j = q_{\min(i,j)} q_{\max(i,j)}$, $p^i \circ p^j = p^{\min(i,j)} p^{\max(i,j)}$, and $q_i \circ p^j = q_i p^j + h \delta_i^j$; in other words, to remove $\circ$ from a product, we must add a term with a factor of $h$ whenever $q_i$ and $p^i$ appear on opposite sides of $\circ$.  Also, define the Lie product so that $q_i \bullet q_j = 0$, $p^i \bullet p^j = 0$, and $q_i \bullet p^j = -h \delta_i^j$.  Then when $h = 0$, we get the usual symmetric algebra of commutative polynomials, while for $h = 1$, we get the (real) [[Weyl algebra]].


## Representations

In general, a [[representation]] of Jordan--Lie algebra $A$ in a Jordan--Lie algebra $B$ is simply a [[homomorphism]] (in the usual sense of [[universal algebra]]) from $A$ to $B$.  But when $h \gt 0$, we often take $B$ to be an associative $*$-[[*-algebra]] and represent $A$ in it with a homomorphism to $sa(B)$, the Jordan--Lie algebra of self-adjoint elements of $B$ (see [above](#examples)).  When $A$ is a Jordan--Lie--Banach algebra, then we generally want $B$ to be the same, or to be a [[Banach *-algebra|Banach algebra]], and for the homomorphism to be [[short map|short]].  Similarly, when $A$ is unital, we generally want $B$ to be the same, and to have the homomorphism preserve the unit.  When $A$ is a $JLB$-algebra, then we generally want $B$ to be the same, or to be a $C^*$-[[C-star-algebra|algebra]]; and when $A$ is a $JLBW$-algebra, then we generally want $B$ to be the same or to be a $W^*$-[[W-star-algebra|algebra]].  (In these cases, the homomorphism is automatically short and automatically preserves any unit.)

Instead of a representation *in* $B$, we can also consider a representation *on* $H$, where $H$ is an [[inner product space]] over the [[complex numbers]] (or the complexification of $K$ more generally).  This is a representation in the $*$-algebra of [[linear operators]] on $H$, or equivalently a representation in the Jordan--Lie algebra of self-adjoint operators on $H$.  When $B$ is a Jordan--Lie--Banach algebra (especially a $JLB$-algebra or even a $JLBW$-algebra), then we may take $H$ to be a [[Hilbert space]] and look only at the [[bounded operators]].


## References

A definition is in section 1.1 of 

* [[Hans Halvorson]] and [[Rob Clifton]] (1999). _Maximal Beable Subalgebras of Quantum-Mechanical Observables_. [PDF](http://philsci-archive.pitt.edu/65/1/beables.pdf).
  {#HC1999}

A brief remark is on page 80 of

* [[Sean Bates]] and [[Alan Weinstein]] (1995?). _Lectures on the geometry of quantization_. [PDF](http://www.math.berkeley.edu/~alanw/GofQ.pdf).
  {#BW1995}


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
[[!redirects JLC algebra]]
[[!redirects JLC algebras]]
[[!redirects JLC-algebra]]
[[!redirects JLC-algebras]]

[[!redirects JLBW algebra]]
[[!redirects JLBW algebras]]
[[!redirects JLBW-algebra]]
[[!redirects JLBW-algebras]]
[[!redirects JLW algebra]]
[[!redirects JLW algebras]]
[[!redirects JLW-algebra]]
[[!redirects JLW-algebras]]
