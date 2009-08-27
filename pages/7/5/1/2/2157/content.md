# Definitions #

An __affine space__ is a [[vector space]] that has forgotten its origin.

This can be understood in various (equivalent) ways:
*  An affine space is simply a vector space, but we accept as [[morphisms]] of affine spaces any function which is the difference between a linear map (a morphism of vector spaces) and a [[constant function]].
*  An affine space is a [[set]] equipped with an equivalence class of vector space structures, where two vector space structures are considered equivalent if the [[identity function]] is the difference between a linear map and a constant function.
*  An affine space is a set $A$ together with a vector space $V$ and an [[action]] of (the additive group of) $V$ on $A$ that makes $A$ into a $V$-[[torsor]] (over the point). For this point of view, see also [[zoranskoda:affine space]].
*  An affine space is a [[heap]] whose automorphism group is the additive group of a vector space.
*  An affine space is a set $A$ together with a vector space $V$ and a function $A \times A \to V$ (thought of as subtraction) that satisfies some equations.
*  An affine space over the [[ground field]] $k$ is an [[inhabited set]] $A$ together with functions $A \times A \times A \to A$ (thought of as $x,y,z \mapsto x - y + z$) and $k \times A \times A \to A$ (thought of as $r,x,y \mapsto r x + (1-r) y$) that satisfy some equations.
   +--{: .query}
   [[Mike Shulman]]: I changed $r x - r y + y$ to $r x + (1-r) y$ because I think the latter conveys a better intuition (a weighted average).  Speak up if you object.
   =--
*  Assuming that $2$ is invertible in the field $k$ (i.e. the [[characteristic]] of $k$ is not $2$), an affine space over $k$ is an inhabited set $A$ together with a function $k \times A \times A \to A$ that satisfies some equations.
* An affine space over the field $k$ is an inhabited set $A$ together with, for every integer $n\ge 0$ and every $(n+1)$-tuple $(r_0,\dots,r_n)$ of elements of $k$ such that $r_0+\dots+r_n=1$, a function $A^{n+1}\to A$, satisfying some equations.  We think of (and write) the function corresponding to $(r_0,\dots,r_n)$ as $(x_0,\dots,x_n)\mapsto r_0x_0+\dots+r_n x_n$.

Clearly every vector space has an underlying affine space, giving a [[forgetful functor]] $U:Vect \to Aff$.  Conversely any affine space gives rise to a canonical vector space, sometimes called its space of _displacements_.  This is obvious from the definitions that involve a vector space as part of the structure, but a vector space can also be reconstructed from the other definitions as well, analogously to how a group can be reconstructed from a [[heap]].  This gives a functor $D:Aff\to Vect$ in the other direction.  One can verify that $D(U(V))\cong V$ and $U(D(A))\cong A$, but the first isomorphism is natural and the second is not (otherwise $Vect$ and $Aff$ would be [[equivalence of categories|equivalent]]).


# Comparing definitions

Of the definitions not explicitly involving a vector space (the last three), the first is an affine version of the usual definition of a vector space in terms of addition and scalar multiplication.  Note that in each case the affine operation needs to take an extra parameter.  However, in the affine case, it turns out that (if $2$ is invertible) the "addition" $(x,y,z)\mapsto x-y+z$ can be recovered from the "scalar multiplication" $(r,x,y)\mapsto r x + (1-r)y$ by
$$ x - y + z = 2 \left(\frac{1}{2} x + \frac{1}{2} z\right) + (-1)y.$$
This leads to the next definition, in which we omit the operation $A^3\to A$ in favor of the operation $k\times A^2\to A$.

The last, "unbiased," definition is analogous to defining a vector space as a set $V$ equipped with, for every integer $n\ge 0$ and $n$-tuple $(r_1,\dots,r_n)$ of elements of $k$, a function $V^n\to V$ (thought of as $(v_1,\dots,v_n)\mapsto r_1 v_1+\dots r_n v_n$), satisfying some axioms.  Just as we call a general expression $r_1 v_1+\dots r_n v_n$ a "linear combination" of elements of $V$, when $r_0+\dots+r_n=1$ we call $r_0x_0+\dots+r_n x_n$ an _affine combination_ of elements of $A$.

The axioms for the unbiased definition are most straightforward to see by writing out the operations as a [[Lawvere theory]].  In particular, this includes "substitution" axioms of the form
$$
r_0(s_{00} x_{00} + \dots + s_{0m_0} x_{0m_0}) + \dots + r_n (s_{n0} x_{n0} + \dots + s_{n m_n} x_{n m_n}) = r_0 s_{00} x_{00} + \dots + r_n s_{n m_n} x_{n m_n}.
$$
However, it also includes "permutation" axioms of the form
$$
r_0 x_0 + \dots + r_n x_n = r_{\sigma 0} x_{\sigma 0} + \dots + r_{\sigma n} x_{\sigma n}
$$
and also "duplication" and "omission" axioms.  This Lawvere theory can be defined concisely as follows.  The Lawvere theory of vector spaces is the opposite of the category of finite-dimensional vector spaces; its operations are all linear combinations.  The Lawvere theory for affine spaces is the sub-theory of this consisting of only the affine combinations.  (The Lawvere theory of vector spaces also has other interesting sub-theories, such as that consisting of _convex combinations_ whose algebras are abstract [[convex spaces]].)

Note, however, that not all the algebras for this Lawvere theory are affine spaces (as usually considered), only the _inhabited_ ones.  Thus, the category $Aff$ is not a [[variety of algebras]].  To rectify this, sometimes one allows the [[empty set]] to be an affine space (of dimension $-1$), although it does not have an associated vector space of displacements.

Given the unbiased definition in terms of a Lawvere theory, the previous two "biased" vector-space-free definitions can then be recovered from the observation that this Lawvere theory is generated by 2-ary operations if $char(k)\neq 2$, and by 3-ary ones if $char(k)=2$.  To wit, suppose given $(r_0,\dots,r_n)\in k^{n+1}$ with $n\ge 3$ such that $r_0+\dots+r_n=1$.  Suppose for the moment that the $r_i$ are not all $1$, and WLOG suppose that $r_0\neq 1$.  (Note that here we use the invariance under permutations.)  Then we have
$$
r_0 x_0 + \dots + r_n x_n = r_0 x_0 + (1-r_0)\left(\frac{1}{1-r_0} r_1 x_1 + \dots + \frac{1}{1-r_0}r_n x_n\right)
$$
so we have expressed the given $(n+1)$-ary operation in terms of a 2-ary one and an $n$-ary one.  By induction, in this way we can express any $(n+1)$-ary operation in terms of 2-ary ones (note that there is only one 1-ary operation, namely the identity, and no 0-ary ones) --- as long as we never hit a tuple where every $r_i=1$.  But since we always have the requirement $r_0+\dots+r_n=1$, this badness can only happen if the characteristic of $k$ is $n$.  Moreover, we still have
$$
x_0 + \dots + x_n = x_0 - x_1 + (2x_1 + x_2 + \dots + x_n)
$$
so we can still write this $(n+1)$-ary operation in terms of a 3-ary one and an $n$-ary one.  So only if $n+1=3$ (i.e. $n=char(k)=2$) are we prevented from getting down to 2-ary operations only, and in this case we can still get down to 3-ary ones.  Finally, we observe that any 3-ary operation can be written in terms of 2-ary ones and the particular 3-ary operation $x_0 - x_1 + x_2$:
$$
r_0 x_0 + r_1 x_1 + r_2 x_2 = \big(r_0 x_0 + (1-r_0) x_2\big) - x_2 + \big(r_1 x_1 + (1-r_1) x_2\big).
$$

Comparing these three definitions with those that stipulate a vector space can be done in essentially the same way that one compares the various definitions of [[heap]].


# Further Remarks

Every finitely-generated affine space is isomorphic to the $n$-fold [[direct sum]] $k^n$, where $k$ is the [[base field]] and $n$ is a [[natural number]] (possibly $0$, possibly $-1$ if the empty set is allowed---by convention $k^{-1}=\emptyset$).  In [[algebraic geometry]], an $n$-dimensional affine space is often denoted $\mathbb{A}^n$ and identified with $k^n$.

The notion of affine space may be generalised to __affine module__ by replacing the vector space above by a [[module]] and the base field $k$ by a [[commutative ring]].  Then an affine module over the ring $\mathbb{Z}$ of [[integer]]s is precisely a commutative [[heap]], just like a module over $\mathbb{Z}$ is an [[abelian group]].

+--{: .query}
[[Mike Shulman]]: I haven't thought much about affine modules, but it seems likely to me that the "biased" module-free definitions won't be right any more, since the Lawvere theory needn't be generated by 2-ary or 3-ary operations (as far as I can see).  More explicitly, I don't immediately see how to write an operation like
$$(x_0,x_1,x_2,x_3) \mapsto 4x_0 - 6x_1 - 2x_2 + 5x_3$$
in terms of $A^3\to A$ and $\mathbb{Z}\times A^2\to A$, but it seems to me that this operation should still exist in an affine $\mathbb{Z}$-module.
=--


[[!redirects affine module]]
[[!redirects affine modules]]
[[!redirects affine spaces]]
