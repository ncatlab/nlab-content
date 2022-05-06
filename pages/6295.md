
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

A Jordan--Lie algebra is a [[quantum deformation]] of a [[Poisson algebra]], consisting of a single [[vector space]] with compatible structures of both a [[Jordan algebra]] and a [[Lie algebra]].  Secretly, this is the same thing as a [[complexification|complexified]] $*$-[[star-algebras]].  If we add an appropriate [[topological structure]], then we get a Jordan--Lie--[[Banach algebra]] (corresponding to complex Banach $*$-algebras), of which the $JLB$-algebras (corresponding to $C^*$-[[C-star algebra|algebras]]) and $JLBW$-algebras (corresponding to [[von Neumann algebras]]) are important special cases.

In traditional [[strict deformation quantization]], the outcome of [[quantization]] of [[Poisson algebras]] is regarded to be a non-commutative but associative complex $*$-[[star-algebra|algebra]] (such as a $C^*$-[[C-star-algebra|algebra]]).  But any such induces a Jordan--Lie algebra (consisting of its [[self-adjoint elements]]) by letting the Jordan product be the symmetrized product and the [[Lie bracket]] the [[commutator]] (times $\mathrm{i}/2$). There is a condition relating the [[associator]] of the Jordan product to the Lie bracket, which makes $JLB$-algebras effectively the same as $C^*$-algebras, the difference being that the single associative product is explicitly regarded as inducing the two products of a $JLB$-algebra. For more on this separation of the Lie-algebra and the Jordan-algebra aspect of quantization see at _[[order-theoretic structure in quantum mechanics]]_.


## Definitions and elementary properties

Let $K$ be a [[formally real field]] (in particular, $1/2 \in K$), and let $q \in K$ be a scalar.  (Most of what we say here works over more general fields or even [[commutative rings]], but there are arguments that the usual notion of [[Jordan algebra]] is inappropriate already for fields of characteristic $2$, so I don\'t want to pretend to more generality than we can justify.  Indeed, there does not yet seem to be any published literature on Jordan--Lie algebras that doesn\'t set $K$ to the field $\mathbb{R}$ of [[real numbers]].)  Since $K$ is a [[field]], $q$ is either zero or invertible, and some things will depend on which it is.

A __Jordan--Lie algebra__ (over $K$ with deformation constant $q$) consists of a $K$-[[vector space]] $A$ equipped with two [[bilinear operators]] $(-)\circ(-)$ and $[{-},{-}]$, respectively called the _[[Jordan product]]_ and the _[[Lie bracket]]_, satisfying the following identities:

* commutativity of the Jordan product: $x \circ y = y \circ x$;
* alternation (anticommutativity) of the Lie bracket: $[x, x] = 0$, or equivalently (using bilinearity and that $1/2 \in K$) $[x, y] = -[y, x]$;
* the Jacobi identity (self-derivation of the Lie bracket): $[x, [y, z]] = [[x, y], z] + [y, [x, z]]$, or equivalently (using anticommutativity) $[x, [y, z]] + [y, [z, x]] + [z, [x, y]] = 0$;
* derivation of the Lie bracket over the Jordan product: $[x, y \circ z] = [x, y] \circ z + y \circ [x, z]$;
* the associator identity: $x \circ (y \circ z) = (x \circ y) \circ z + q^2 [y, [x, z]]$, or equivalently (using anticommutativity) $(x \circ y) \circ z - x \circ (y \circ z) = q^2 [[x, z], y]$.

Note that the last two axioms (and alternation) prove the Jordan identity: first,
$$ [x, x \circ x] = [x, x] \circ x + x \circ [x, x] = 0 ;$$
then (writing $x^2$ for $x \circ x$),
$$ x \circ (y \circ x^2) - (x \circ y) \circ x^2 = q^2 [y, [x, x^2]] = 0 .$$
Thus, $A$ is a [[Jordan algebra]] under the Jordan product, and of course $A$ is a [[Lie algebra]] under the Lie bracket.  (In a similar way, we can prove the Jacobi identity from the associator identity if $q$ is cancellable; but we state the Jacobi identity separately to cover when $q = 0$ as well.)

As usual for Jordan algebras, we write $x^n$ for an $n$-fold product of $x$ under the Jordan product; this is unambiguous since Jordan algebras are always power-associative.  (And of course, an $n$-fold Lie bracket is always zero for $n \gt 1$.)  Even more generally the un[[bias]]ed form of the Jordan identity is that multiplication by $x^m$ and by $x^n$ commute:
$$ (x^m \circ y) \circ x^n = x^m \circ (y \circ x^n) $$
(which may be proved by [[induction]] using only the usual Jordan identity).  We similarly have that powers of $x$ commute with each other under the bracket:
$$ [x^m, x^n] = 0 .$$
The proof is similar to the proof above that $[x, x^2] = 0$, by induction.  (Then you can use this to get a faster proof of the unbiased Jordan identity.)

A Jordan--Lie algebra is __unital__ if the Jordan product has   an [[identity element]] $1$:

* multiplicative identity: $1 \circ x = x$.

Then we may also interpret $x^0$ as $1$.  Note that $[x, 1] = 0$ too (a special case of $[x^m, x^n] = 0$), proved by examining $[x, 1 \circ 1]$.

If $K$ is a [[normed field]], then a __Jordan--Lie--Banach algebra__ consists of a $K$-[[Banach space]] $A$ equipped with a [[short linear operator|short]] [[bilinear operator]] (as the Jordan product) and a [[densely defined linear operator|densely defined]] bilinear operator (as the Lie bracket) making the domain of the Lie bracket into a Jordan--Lie algebra as above.

Typically, although the Lie bracket is allowed to be unbounded, it will be bounded when $q \gt 0$.  (This is a theorem for $JLB$-algebras below.)  Using continuity to prove all of the axioms, $A$ is also a [[Jordan–Banach algebra]] under the Jordan product.  A Jordan--Lie--Banach algebra is __unital__ if the Jordan algebra has a unit and ${\|1\|} \leq 1$ (in which case ${\|1\|} = 1$ if $A$ is nontrivial).  Note that Jordan--Lie--Banach algebras (besides the $JLB$-algebras below) don\'t seem to appear in the literature; this terminology is analogous to that of Jordan--Banach algebras.

A __$JLB$-algebra__ is a Jordan--Lie--Banach algebra satisfying the following additional identities:

* the $B$-identity: ${\|x\|^2} = {\|x^2\|}$ (compare the $B^*$-identity or $C^*$-identity of a $C^*$-[[C-star-algebra|algebra]]);
* positivity: ${\|x^2\|} \leq {\|x^2 + y^2\|}$.

Then $A$ is a [[JB-algebra]] under the Jordan product.

As with any $JB$-algebra, we don\'t need to explicitly state that the Jordan product is short (nor that ${\|1\|} \leq 1$ in the unital case), as this can be proved using the $B$-identity and the [[polarization identities]].  (Conversely, if we do state that the product is short, then we only need the $\leq$ half of the $B$-identity in addition, or we can even combine it with positivity as ${\|x\|^2} \leq {\|x^2 + y^2\|}$.)  We can also prove (by induction on $\lceil\log_2 n\rceil$) that ${\|x^n\|} = {\|x\|^n}$ (except for $n = 0$ in the trivial algebra).

When $q \gt 0$, we should also be able to prove that Lie bracket is bounded by $1/q$, but I don\'t see the proof.  (A naive look at the associator identity suggests a bound of $\sqrt{2}/q$, but it\'s not clear to me whether $[[x,z],y]$ is sufficently general to prove this.)  Then extending by continuity, we may assume that the Lie bracket is defined everywhere.

Positivity generalizes to any number of terms on either side (as long as the right-hand side has more, of course).  (However, I don\'t see how to prove this without going through the [[functional calculus]] to prove that every sum of squares has a [[square root]].)  Thus, a $JB$-algebra is [[formally real algebra|formally real]]: if $\sum_i x_i^2 = 0$, then each $x_i = 0$ (because the norms lie in a formally real field).

Following the established terminology for $JB$-algebras, a __$JLC$-algebra__ may be defined as a *concrete* $JLB$-algebra, that is one equipped with a faithful representation (see [below](#representations)) on a [[Hilbert space]], or equivalently a real [[subalgebra]] of $SA(H)$ (see [below](#examples)) that is closed in the [[operator topology]].  However, like $C^*$-algebras (but unlike general $JB$-algebras), every $JLB$-algebra may be so represented and this term seems not to be used.

Finally, a __$JLBW$-algebra__ is a unital $JLB$-algebra whose underlying Banach space is equipped with a (necessarily unique) [[predual]], and a __$JLW$-algebra__ is further equipped with a faithful representation (or equivalently is a $JC$-algebra which includes the identity and is closed in the [[weak operator topology]]).  Again, every abstract $JLBW$-algebra may be made concrete, so we really only need one term in practice, although neither seems to be established in the literature yet.


## Relation to Poisson algebras {#poisson}

If $q = 0$, then the Jordan product becomes associative; in fact, a Jordan--Lie algebra with $q = 0$ is precisely a commutative [[Poisson algebra]].  On the other hand, if $q$ is invertible, then dividing the Lie bracket by $q$ gives a Jordan--Lie algebra with $q = 1$, so the only thing that really matters about $q$ (at least over a field) is whether or not it is zero.  In this way, a Jordan--Lie algebra may be seen as a [[quantum deformation]] of a Poisson algebra.  (In the [[physics|physical]] interpretation, $q$ here is the [[Dirac constant]] $\hbar$.)

Similarly, a Jordan--Banach algebra with $q = 0$ is a commutative Banach algebra equipped with a Poisson bracket (typically unbounded), and similarly for the more specialized versions; then the $q \ne 0$ case is a quantum deformation of such Poisson--Banach algebras.  We can see from this why the Lie bracket cannot be expected to be defined on an entire $JLB$-algebra when $q = 0$, since Poisson brackets in typical examples of Poisson algebras are unbounded in the obvious norms.


## Relation to $C^*$-algebras {#cstar}

For a $JLB$-algebra with $q \gt 0$, the Jordan product and Lie bracket are respectively the real-symmetrized and imaginary-antisymmetrized parts of an associative operation on the [[complexification]] of $A$, defining a complex $C^*$-[[C-star-algebra|algebra]]; and every $C^*$-algebra likewise defines a $JLB$-algebra for any $q \gt 0$ consisting of its [[Hermitian operator|Hermitian]] elements.  (With $q = 0$, we can still get a $C^*$-algebra out of the $JLB$-algebra, and we can still recover the original $JB$-algebra as the self-adjoint elements, but trying to recover the original Lie bracket just results in $0/0$.)  This also works on the purely algebraic level, relating Jordan--Lie algebras to complex $*$-algebras, and on the measurable level, relating $JLBW$-algebras to [[von Neumann algebras]].

Specifically, starting with a Jordan--Lie algebra or Jordan--Lie--Banach algebra $A$ (possibly unital) with deformation constant $q$ over a formally real commutative ring $K$, we write $A \oplus A$ formally as $A + \mathrm{i} A$, on which we define the following operations:

* addition: $(a + \mathrm{i} b) + (c + \mathrm{i} d) \coloneqq (a + c) + \mathrm{i} (b + d)$,
* opposite: $-(a + \mathrm{i} b) \coloneqq (-a) + \mathrm{i} (-b)$ (which we write as $-a - \mathrm{i} b$ as usual),
* zero: $0 \coloneqq 0 + \mathrm{i} 0$,
* scalar multiplication: $(x + \mathrm{i} y) (a + \mathrm{i} b) = (x a - y b) + \mathrm{i} (x b + y a)$ (for $x + \mathrm{i} y$ a scalar in $K[i]$),
* involution: $(a + \mathrm{i} b)^* \coloneqq a + \mathrm{i} (-b) = a - \mathrm{i} b$,
* multiplication: $(a + \mathrm{i} b) (c + \mathrm{i} d) \coloneqq (a \circ c + q [a, d] + q [b, c] - b \circ d) + \mathrm{i} (-q [a, c] + a \circ d + b \circ c + q [b, d])$,
* unit (in the unital case): $1 \coloneqq 1 + \mathrm{i} 0$.

This makes $A + \mathrm{i} A$ into an associative $*$-[[star-algebra|algebra]] over $K[i] := K[\mathrm{x}]/\lang\!\lang\mathrm{x}^2 + 1\rang\!\rang$ (which is a proper extension of $K$, and a field if $K$ is, because $K$ is formally real).  If $A$ is a $JLB$-algebra, then $A + \mathrm{i} A$ becomes a $C^*$-algebra; if $A$ is a $JLBW$-algebra, then $A + \mathrm{i} A$ becomes a von Neumann algebra.

The intermediate Jordan--Lie--Banach case doesn\'t quite work.  If we allow the Lie bracket to be unbounded (except when $q = 0$ so that it is irrelevant), then we might not be able to define multiplication everywhere.  It is also not clear how the norm can be defined in this case.  (For $C^*$-algebras, in contrast, there is no need to define the norm explicitly, since it is determined by the algebraic structure.)

Conversely, starting with a $*$-algebra $A$ (possibly unital, possibly a Banach $*$-algebra) over $K[i]$ and an *invertible* scalar $q$, and assuming that $2$ is invertible in $K$, we form the subspace $sa(A) = \{x\colon A \;|\; x^* = x\}$, on which we define the following operations (under each of which $sa(A)$ is closed):

* addition, opposite, zero, scalar multiplication (by scalars in $K$), unit (in the unital case): by [[restriction]],
* Jordan product: $a \circ b \coloneqq \frac{1}{2} a b + \frac{1}{2} b a$,
* Lie bracket: $[a, b] \coloneqq \frac{1} {2 \mathrm{i} q} a b - \frac{1} {2 \mathrm{i} q} b a$.

In the Banach case, we may also define the norm by restriction.  (There is no difficulty in this direction for arbitrary Banach $*$-algebras.)

We can write the resulting Jordan--Lie algebra as $sa_q(A)$ or simply $sa(A)$ if $q = 1$.  If $A$ is a Banach $*$-algebra, then $sa_q(A)$ is a Jordan--Lie--Banach algebra (with the Lie bracket defined everywhere); if $A$ is a $C^*$-algebra, then $sa_q(A)$ is a $JLB$-algebra; if $A$ is a von Neumann algebra, then $sa_q(A)$ is a $JLBW$-algebra.

(If $K$ is a formally real *field*, then it has characteristic $0$, so $2$ must be invertible; but for more general rings, if $2$ is not invertible in $K$, then the formulas for the Jordan product and Lie bracket don\'t make sense, even when $q$ is invertible.  If you leave out the divisions by $2$, then you still get a Jordan--Lie algebra with deformation constant $q$, but it won\'t necessarily be unital when $A$ is, the Jordan product could have a norm as high as $2$ in the Banach case, and the $B$-identity will fail in the $C^*$-case, gaining an unwanted factor of $2$.  In any case, a round-trip between Jordan--Lie algebras and complex $*$-algebras requires a division by $2$ somewhere.)

This all defines a [[functor]] each way between the [[groupoids]] of $C^*$-algebras and $JLB$-algebras with fixed $q \ne 0$, which in fact form an [[equivalence of categories|adjoint equivalence]].  (At least it should be; I don\'t know if this has been worked out in detail.)  Since we have a notion of [[morphism]] (not just [[isomorphism]]) of $C^*$-algebras, we can transport this along the equivalence to get a notion of morphism of $JLB$-algebras (which I would expect to be a short linear map that preserves both products, but somebody should check this) and thus a [[category]] $JLB Alg$ equivalent to $C^* Alg$.

In particular, for fixed $q \ne 0$, the category of $JLB$-algebras with one value of $q$ is equivalent to the category of $JLB$-algebras with another value of $q$ (since both are equivalent to complex $C^*$-algebras), but we have only a functor from $JLB$-algebras with $q = 0$ to any of these other categories.  (And this is not a very interesting functor, since it simply throws away the original Lie bracket and replaces it with zero.)

Similarly, real $JLBW$-algebras (with fixed $q \ne 0$) are equivalent to complex $W^*$-[[W-star-algebra|algebras]].


## Examples {#examples}

Any commutative [[associative algebra]] is a trivial example of a Jordan--Lie algebra with the Lie bracket set to [[zero]].  Similarly, any commutative [[Banach algebra]] is a Jordan--Lie--Banach algebra, any commutative $C^*$-[[C-star-algebra|algebra]] with trivial involution is a $JLB$-algebra, and any commutative $W^*$-[[W-star-algebra|algebra]] with trivial involution is a $JLBW$-algebra.  Note that the value of $q$ is irrelevant in these examples.

More interestingly, given any $C^*$-[[C-star-algebra|algebra]] (*not* assumed commutative or with trivial involution), the [[self-adjoint elements]] form a $JLB$-algebra with $q = 1$; if the original $C^*$-algebra is a $W^*$-[[W-star-algebra|algebra]], then the self-adjoint elements form a $JLBW$-algebra.  In fact, *every* $JLB$-algebra (including every $JLBW$-algebra) with $q = 1$ has this form; more generally, every $JLB$-algebra with $q \ne 0$ has this form upon dividing the Lie bracket by $q$.  (See [above](#cstar)).

More specifically, given a [[Hilbert space]] $H$, the [[self-adjoint operators]] form a $JLBW$-algebra $SA(H)$ with $q = 1$.  In fact, *every* $JLB$-algebra (including every $JLBW$-algebra) with $q = 1$ is a subalgebra of some $SA(H)$; more generally, every $JLB$-algebra with $q \ne 0$ has this form upon dividing the Lie bracket by $q$.  (This is a combination of the previous paragraph and the theorem that every $C^*$-algebra may be made concrete.)

As for $q = 0$, every commutative [[Poisson algebra]] is a Jordan--Lie algebra with $q = 0$, and every Jordan--Lie algebra with $q = 0$ has this form.  This settles the purely algebraic case.

For the topological case with $q = 0$, fix a [[symplectic manifold]] (or [[Poisson manifold]]) $X$ and take the unital Banach [[algebra of bounded continuous functions]] on $X$, equipped with the [[Poisson bracket]].  Here, the Poisson bracket is unbounded and not defined everywhere.  (You could also use the Banach space of [[smooth functions]] whose derivatives of all orders are bounded, but the Poisson bracket is still unbounded and not defined everywhere, since there are bounded smooth functions with unbounded derivatives, unless $X$ is [[closed manifold|closed]].)  This is a $JLB$-algebra with $q = 0$.  (But not *every* $JLB$-algebra with $q = 0$ has this form.)

Let $V$ be a (real) [[vector space]] of finite dimension $n$, which we will think of as the [[configuration space]] of a [[classical system]], and let $A$ be the [[symmetric algebra]] on the dual [[phase space]] $V \otimes V^* \cong \mathbb{R}^{2n}$.  We normally think of $A$ as consisting of (commutative) [[polynomials]] in the variables $x^1, \ldots, x^n, p_1, \ldots, p_n$, but let us now think of them as *noncommutative* polynomials consisting only of terms in which the variables come in order.  Fixing a scalar $q$, define the Jordan product on $A$ so that $x^i \circ x^j = x^{\min(i,j)} x^{\max(i,j)}$, $p_i \circ p_j = p_{\min(i,j)} p_{\max(i,j)}$, and $x^i \circ p_j = x^i p_j + q \delta^i_j$; in other words, to remove $\circ$ from a product, we must add a term with a factor of $q$ whenever $x^i$ and $p_i$ appear on opposite sides of $\circ$.  Also, define the Lie bracket so that $[x^i, x^j] = 0$, $[p_i, p_j] = 0$, and $[q^i, p_j] = -\frac{1}{2} \delta^i_j$.  Then when $q = 0$, $A$ is the usual symmetric algebra of commutative polynomials again, while for $q \ne 0$, $A$ becomes $sa_q(W)$, where $W$ is the [[Weyl algebra]] $A + \mathrm{i} A$.


## Representations

In general, a [[representation]] of Jordan--Lie algebra $A$ in a Jordan--Lie algebra $B$ is simply a [[homomorphism]] (in the usual sense of [[universal algebra]]) from $A$ to $B$.  But when $q \gt 0$, we often take $B$ to be an associative $*$-[[*-algebra]] and represent $A$ in it with a homomorphism to $sa(B)$, the Jordan--Lie algebra of self-adjoint elements of $B$ (see [above](#examples)).  When $A$ is a Jordan--Lie--Banach algebra, then we generally want $B$ to be the same, or to be a [[Banach *-algebra|Banach algebra]], and for the homomorphism to be [[short map|short]].  Similarly, when $A$ is unital, we generally want $B$ to be the same, and to have the homomorphism preserve the unit.  When $A$ is a $JLB$-algebra, then we generally want $B$ to be the same, or to be a $C^*$-[[C-star-algebra|algebra]]; and when $A$ is a $JLBW$-algebra, then we generally want $B$ to be the same or to be a $W^*$-[[W-star-algebra|algebra]].  (In these cases, the homomorphism is automatically short and automatically preserves any unit.)

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
