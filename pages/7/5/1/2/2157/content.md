
# Contents
* table of contents
{: toc}

## Idea

An __affine space__ or __affine linear space__ is a [[vector space]] that has forgotten its origin.  An __affine linear map__ (a morphism of affine spaces) is a linear map (a morphism of vector spaces) that need not preserve the origin.

Note that the 'linear functions' of elementary algebra ---the total functions whose graphs are lines--- are in fact (precisely) *affine* $\mathbb{R}$-linear maps from $\mathbb{R}$ to itself.  (Similarly, the 'linear relations' ---the relations whose graphs are lines--- are precisely the *[[projective space|projective]]* $\mathbb{R}$-linear maps.) 

Alternatively, in [[algebraic geometry]], the terminology "$n$-dimensional affine space" $\mathbb{A}^n k$ (affine line, affine plane, etc.) over a [[field]] $k$ refers to, depending on context, the set $k^n$, or the set of maximal ideals of the [[polynomial algebra]] $k[x_1, \ldots, x_n]$ -- these definitions coinciding if $k$ is an [[algebraically closed field]] -- and typically considered as equipped with relevant extra structure such as a [[Zariski topology]] or, going even further, the [[locally ringed space]] structure adhering to the [[affine variety]] or [[affine scheme]] corresponding to the polynomial algebra $k[x_1, \ldots, x_n]$. Whatever the precise sense chosen, the idea is that an affine space $\mathbb{A}^n k$ is a setting in which the study of loci of polynomial equations, i.e. definable sets in the theory of [[commutative algebras]] over $k$, is carried out. 

Most of this article concerns affine spaces in the sense of vector spaces that have forgotten their origins or identities; the algebraic geometry sense is very briefly touched upon in the section *Affine spaces as model spaces*. 


## Definitions

### Summary

The definition of affine space can be made precise in various (equivalent) ways.  We give a name to some of the definitions for later reference.

*  An affine space is simply a vector space, but with different morphisms; an affine linear map is a function that is the difference between a linear map and a [[constant function]].

*  An affine space is a [[set]] equipped with an equivalence class of vector space structures, where two vector space structures are considered equivalent if the [[identity function]] is affine linear as a map from one structure to the other; whether a map between affine spaces is affine linear is independent of the representative vector space structures.

*  An affine space is a set $A$ together with a vector space $V$ and an [[action]] of (the additive group or _[[translation group]]_ of) $V$ on $A$ that makes $A$ into a $V$-[[torsor]] (over the point); an affine linear map is a $V$-equivariant map. For this point of view, see also [[zoranskoda:affine space]].

*  An affine space is a [[heap]] whose [[automorphism group]] is equipped with structure making it the additive group of a vector space; an affine linear map is a heap morphism.

*  An affine space is an [[inhabited set]] $A$ together with a vector space $V$ and a function $\Lambda\colon A \times A \to V$ (thought of $\Lambda(x,y) \coloneqq x - y$) that satisfies some equations; an affine linear map $A \to A'$ is a function equipped with a linear map $V \to V'$ relative to which it preserves subtraction (the "vector-valued difference" definition).

*  An affine space over the [[ground field]] $k$ is an [[inhabited set]] $A$ together with functions $\mu\colon A \times A \times A \to A$ (thought of as $\mu(x,y,z) \coloneqq x - y + z$) and $\Lambda_*\colon k \times A \times A \to A$ (thought of as $\Lambda_r(x,y) \coloneqq x - r x + r y$) that satisfy some equations; an affine linear map is a function that preserves these operations (the "two ternary operations" definition).

*  An affine space over $k$ is an inhabited set $A$ together with a function $\mu_*\colon k\times A\times A\times A\to A$ (thought of as $\mu_r(x,y,z) \coloneqq r x - r y + z$) that satisfies some equations; an affine linear map is a function that preserves this operation (the "one quaternary operation") definition.

*  Assuming that $2$ is invertible in the field $k$ (i.e. the [[characteristic]] of $k$ is not $2$), an affine space over $k$ is an inhabited set $A$ together with a function $\Lambda_*\colon k \times A \times A \to A$ that satisfies some equations; an affine linear map is a function that preserves this operation (the "one ternary operation" definition).

*  An affine space over the field $k$ is an inhabited set $A$ together with, for every [[natural number]] $n \geq 0$ and every $(n+1)$-tuple $(r_0,\dots,r_n)$ of elements of $k$ such that $r_0 + \dots + r_n = 1$, a function $\gamma_{r_0,\ldots,r_n}\colon A^{n+1}\to A$ (thought of as $\gamma_{r_0,\ldots,r_n}(x_0,\ldots,x_n) \coloneqq r_0 x_0 + \cdots + r_n x_n$), satisfying some equations; an affine linear map is a function that preserves these operations (the "[[unbiased]]" definition).

+-- {: .query}
[[Mike Shulman]]: I think there should also be a definition of the form "an affine space is a [[projective space]]" with a distinguished line called "infinity", which should also be equivalent to a "synthetic" description involving points and lines and incidence axioms.  This definition would not fix the field $k$ at the outset, but rather recover it synthetically using cross-ratios.  Accordingly, it ought to define an equivalent groupoid to the groupoid of pairs $(k,A)$ where $k$ is a field and $A$ is an affine space over $A$.  I don't know how one could recover the non-invertible affine transformations from it directly.
=--

+-- {: .query}
There should be another characterisation, which I don\'t quite see how to phrase, at least when $k = \mathbb{R}$, which is that an affine space is a manifold (perhaps Riemannian) that is sufficiently flat and unbounded in some sense.  ---Toby

[[Mike Shulman]]: It'd have to be at least Riemannian, otherwise you don't have enough structure.  I don't suppose it's enough to say that a (finitely generated) affine space is a Riemannian manifold isometric to some $\mathbb{R}^n$?

_Toby_:  I intended 'that is [...] in some sense' to include the possibility of structure that should be preserved by the morphisms.  Note that a Riemannian manifold is *too much* structure, although it allows a definition like the first one above.  (A Riemannian manifold isometric to some $\mathbb{R}^n$ is precisely a [[Euclidean space]].)  But really, I\'m hoping for some phrasing such that &#8249;isomorphic to some $\mathbb{R}^n$&#8250; actually becomes a (not too obvious) *theorem*.  I\'ll keep thinking about it.

[[Mike Shulman]]: Shouldn't a Riemannian manifold isometric to some $\mathbb{R}^n$ be a "Euclidean affine space" (a torsor over a Euclidean space)?  Seems that a Euclidean space would be a Riemannian manifold _equipped with_ an isometry to some $\mathbb{R}^n$.  It does seem like there should be a natural way to say this, but I don't know what it is.

_Toby_:  I guess that this depends on what you think 'Euclidean space' means; I\'ve known people to define it to *be* $\mathbb{R}^n$, but that seems quite ahistorical to me; I like that Urs calls such a thing [[Cartesian space]] instead.  Euclid did not have coordinates; he did not even have an origin, so a Euclidean space should be a heap rather than a group.  For my comment above, I would define a [[Euclidean space]] to be an affine inner product space; FWIW [Wikipedia agrees](https://secure.wikimedia.org/wikipedia/en/affine_space).  (However, Wikipedia doesn\'t go as far as I do when I claim that the inner product should be valued in an $\mathbb{R}$-line rather than in $\mathbb{R}$ itself; then again, I ignored that subtlety myself in my previous comment.)
=--

Clearly every vector space has an underlying affine space (and every linear map is affine linear), giving a [[forgetful functor]] $U:Vect \to Aff$.  Conversely, any affine space gives rise to a canonical vector space, sometimes called its space of _displacements_.  This is obvious from the definitions that involve a vector space as part of the structure, but a vector space can also be reconstructed from the other definitions as well, analogously to how a group can be reconstructed from a [[heap]].  This gives a functor $D:Aff\to Vect$ in the other direction.  One can verify that $D(U(V))\cong V$ and $U(D(A))\cong A$; the first isomorphism is [[natural isomorphism|natural]], but the second is not (otherwise $Vect$ and $Aff$ would be [[equivalent categories]], which they are not).

The category of affine spaces is almost a [[variety of algebras]], as can be seen from the last few definitions, except for the requirement that an affine space be inhabited.  To rectify this, sometimes one allows the [[empty set]] to be an affine space, although it does not have any particular vector space of displacements.  (See [heap#empty](heap#empty) for discussion.)

Note that there are a few different ways to think about the operations involved in the final three definitions (those not explicitly involving a vector space).  The operation $\mu\colon x,y,z \mapsto x - y + z$ is the same as the [[Mal'cev operation]] (i.e. [[heap]] structure) of the [[translation group|additive group]] of a vector space.  It can be viewed as the point completing a parallelogram with given vertices $x,y,z$, or equivalently as the result of adding $x$ and $z$, relative to a choice of $y$ as the origin.  The operation $\Lambda_*\colon r,x,y \mapsto x - r x + r y$ can be viewed as either a weighted average of $x$ and $y$ (i.e. as $(1-r)x + r y$) or as the result of multiplying the "displacement vector" $y-x$ by $r$, relative to the origin $x$ (i.e. as $x + r(y-x)$).


### Details and comparisons

The first few definitions, which explicitly involve a vector space, make no especial use of the fact that the vector space is a vector space rather than merely an abelian [[group]].  Thus, they are valid (and equivalent) in the more general context of [[torsors]] and [[heaps]].  They are also mostly complete as stated, except for the final one.


#### Vector-valued differences

In this definition, an affine space over a vector space $V$ is a set $A$ together with a "subtraction" function $\Lambda\colon A\times A\to V$, written $\Lambda\colon x,y \mapsto x-y$, such that:

* $\Lambda(x,x) = 0$, or $x-x = 0$, for any $x$ in $A$.
* $\Lambda(x,y) + \Lambda(y,z) = \Lambda(x,z)$, or $(x-y) + (y-z) = (x-z)$, for any $x,y,z$ in $A$.
* For any $x$ in $A$ and $v$ in $V$ there exists a unique $y$ in $A$ such that $\Lambda(y,x) = v$, or $y - x = v$.

If $y - x = v$, then we write $y = x + v$, which we can regard as an operation on $x$ and $v$ by the third axiom.  Hence we have $(x + v) - x = v$ and (by uniqueness) $x + (y - x) = y$, and also $x + 0 = x$ and $(x + v) + w = x + (v + w)$ by the first two axioms.  Thus, these axioms suffice to make $A$ into a [[torsor]] over the additive group of $V$ with the action $+$, which is one of the previous definitions given.

Note again that this would makes sense if $V$ is any group, not just the additive group of a vector space.


#### Two ternary operations

This definition is an affine version of the usual definition of a vector space in terms of addition and scalar multiplication.  However, in each case the affine operation needs to take an extra parameter.  In reading the following axioms it helps to think of $\mu(x,y,z)$ as "the sum of $x$ and $z$ relative to the basepoint $y$" and likewise $\Lambda_r(x,y)$ as "the product $r\cdot y$ relative to the basepoint $x$".

* $\mu(x,x,y) = y$ (identity for addition)
* $\mu(x,y,\mu(z,w,v)) = \mu(\mu(x,y,z),w,v)$ (associativity of addition)
* $\mu(x,y,z) = \mu(z,y,x)$ (commutativity of addition)
* $\Lambda_{r s}(x,y) = \Lambda_r(x, \Lambda_s(x,y))$ (associativity of scalar multiplication)
* $\Lambda_1(x,y) = y$ (identity for scalar multiplication)
* $\Lambda_{r+s}(x,y) = \mu(\Lambda_r(x,y), x, \Lambda_s(x,y))$ (left distributivity of scalar multiplication)
* $\Lambda_r(w, \mu(x,y,z)) = \mu(\Lambda_r(w,x), \Lambda_r(w,y), \Lambda_r(w,z))$ (right distributivity of scalar multiplication)


#### One quaternary operation

This definition is an affine version of the less standard definition of a vector space in terms of a single operation $r,x,y\mapsto r\cdot x + y$.  Here an affine space over $k$ is a set $A$ together with a single operation $\mu\colon k\times A\times A\times A\to A$, written as $(r,x,y,z)\mapsto \mu_r(x,y,z)$ and thought of as the sum "$r\cdot x + z$ relative to the basepoint $y$," such that:

* $\mu_1(x,y,y) = x$
* $\mu_r(x,x,y) = y$
* $\mu_1(x,y,z) = \mu_1(z,y,x)$
* $\mu_r(\mu_s(x,y,z),w,v) = \mu_{r s}(x,y,\mu_r(z,w,v))$
* $\mu_{r+s}(x,y,z) = \mu_r(x,y,\mu_s(x,y,z))$


#### One ternary operation

In the affine case (in contrast to the vector space case), it turns out that if $2$ is invertible the "addition" $(x,y,z)\mapsto x-y+z$ can be recovered from the "scalar multiplication" $(r,x,y)\mapsto r x + (1-r)y$ by $\mu(x,y,z) = \Lambda_2(y,\Lambda_{1/2}(x,y))$.  Thus, in this case we can define an affine space over $k$ to be a set $A$ together with a single operation $\Lambda\colon k\times A\times A\to A$ such that the axioms for the two-ternary-operations definition are satisfied with this definition of $\mu$.

However, we can also simplify the requisite axioms in this presentation.  The following axioms are easier to state if we write $\Lambda_r(x,y)$ as $(1-r) x + r y$, or equivalently as $r x + s y$, where we require $r+s=1$ for the expression to be defined.

* Idempotence: $r x + s x = x$ whenever $r+s=1$.
* Commutativity: $r x + s y = s y + r x$ whenever $r+s=1$.
* Associativity: whenever $r+s+t=1$, whichever of the following three expressions are defined are equal:
  $$
  \array{
  r x + (1-r)\left(\frac{s}{1-r} y + \frac{t}{1-r} z\right)\\
  (1-s)\left(\frac{r}{1-s} x + \frac{t}{1-s} z\right) + s y\\
  (1-t)\left(\frac{r}{1-t} x + \frac{s}{1-t} y\right) + t z
  }
  $$
  The first is defined whenever $r\neq 1$, the second whenever $s\neq 1$, and the third whenever $t\neq 1$.  Since $k$ has characteristic $\neq 2$, we cannot have $r=s=t=1$ and $r+s+t=1$ at the same time, so at least one of these expressions is always defined.  We write $r x + s y + t z$ for the common value of whichever of them are defined.
* Cancellation: for any $r\in k$ and $x,y\in A$, we have $x + a y - a y = x$.


#### Unbiased definition

Let $Th_{vect}$ denote the [[Lawvere theory]] of $k$-vector spaces.  For any $n$, its $n$-ary operations are $n$-tuples $(r_1,\dots,r_n)\in k^n$ representing the [[linear combination]] operation $(x_1,\dots,x_n)\mapsto r_1 x_1 +\dots+ r_n x_n$.  Composition of operations is by substitution in the obvious way, and the identity operation is $(1)$.  A model of this theory is simply a vector space.  With this 'unbiased' definition, a vector space comes equipped with, for every integer $n\ge 0$ and $n$-tuple $(r_1,\dots,r_n)$ of elements of $k$, a function $V^n\to V$ (thought of as $(v_1,\dots,v_n)\mapsto r_1 v_1+\dots r_n v_n$), satisfying some axioms.

Let $Th_{aff}$ denote the subtheory of $Th_{vect}$ containing only those operations $(r_1,\dots,r_n)$ such that $r_1+\dots+r_n=1$; an **affine space** is a nonempty model of $Th_{aff}$.  (We have to observe that these are closed under the theory operations and thus define a subtheory.  Note that this excludes all zero-ary operations, so an affine space has no distinguished constants, and it also excludes all nonidentity unary operations.)  The basic operations $r_0x_0+\dots+r_n x_n$, when $r_0+\dots+r_n=1$, are called __affine (linear) combinations__ of elements of $A$.

The axioms for the unbiased definition are most straightforward to see by writing out the operations of $Th_{aff}$.  In particular, this includes "substitution" axioms of the form
$$
r_0(s_{00} x_{00} + \dots + s_{0m_0} x_{0m_0}) + \dots + r_n (s_{n0} x_{n0} + \dots + s_{n m_n} x_{n m_n}) = r_0 s_{00} x_{00} + \dots + r_n s_{n m_n} x_{n m_n}.
$$
However, it also includes "permutation" axioms of the form
$$
r_0 x_0 + \dots + r_n x_n = r_{\sigma 0} x_{\sigma 0} + \dots + r_{\sigma n} x_{\sigma n}
$$
and also "duplication" and "omission" axioms.  This Lawvere theory can be defined concisely as follows.  The Lawvere theory of vector spaces is the opposite of the category of finite-dimensional vector spaces; its operations are all [[linear combinations]].  The Lawvere theory for affine spaces is the sub-theory of this consisting of only the affine combinations.  (The Lawvere theory of vector spaces also has other interesting sub-theories, such as that consisting of _[[convex combinations]]_ whose algebras are abstract [[convex space]]s in one sense of the term.)  Note that the empty set is a model (algebra) of this Lawvere theory; an affine space is an *inhabited* model.

Given the unbiased definition in terms of a Lawvere theory, the previous three "biased" vector-space-free definitions can then be recovered by finding particular generating operations for the theory.  In particular, this Lawvere theory is generated by $2$-ary operations if $char(k)\neq 2$, and by $3$-ary ones if $char(k)=2$.  To wit, suppose given $(r_0,\dots,r_n)\in k^{n+1}$ with $n\ge 3$ such that $r_0+\dots+r_n=1$.  Suppose for the moment that the $r_i$ are not all $1$, and WLOG suppose that $r_0\neq 1$.  (Note that here we use the invariance under permutations.)  Then we have
$$
r_0 x_0 + \dots + r_n x_n = r_0 x_0 + (1-r_0)\left(\frac{1}{1-r_0} r_1 x_1 + \dots + \frac{1}{1-r_0}r_n x_n\right)
$$
so we have expressed the given $(n+1)$-ary operation in terms of a $2$-ary one and an $n$-ary one.  By induction, in this way we can express any $(n+1)$-ary operation in terms of $2$-ary ones (note that there is only one $1$-ary operation, namely the identity, and no $0$-ary ones) --- as long as we never hit a tuple where every $r_i=1$.  But since we always have the requirement $r_0+\dots+r_n=1$, this badness can only happen if the characteristic of $k$ is $n$.  Moreover, we still have
$$
x_0 + \dots + x_n = x_0 - x_1 + (2x_1 + x_2 + \dots + x_n)
$$
so we can still write this $(n+1)$-ary operation in terms of a $3$-ary one and an $n$-ary one.  So only if $n+1=3$ (i.e. $n=char(k)=2$) are we prevented from getting down to $2$-ary operations only, and in this case we can still get down to $3$-ary ones.  Finally, we observe that any $3$-ary operation can be written in terms of $2$-ary ones and the particular $3$-ary operation $x_0 - x_1 + x_2$:
$$
r_0 x_0 + r_1 x_1 + r_2 x_2 = \big(r_0 x_0 + (1-r_0) x_2\big) - x_2 + \big(r_1 x_1 + (1-r_1) x_2\big).
$$


## Further Remarks

Every finitely-generated affine space is isomorphic to the $n$-fold [[direct sum]] $k^n$, where $k$ is the [[base field]] and $n$ is a [[natural number]] (possibly $0$).  In [[algebraic geometry]], an $n$-dimensional affine space is often denoted $\mathbb{A}^n$ and identified with $k^n$.  If one accepts the empty set as an affine space, then this is considered to have dimension $-1$ by convention (so $k^{-1} = \empty$).

The notion of affine space may be generalised to __affine module__ by replacing the vector space above by a [[module]] and the base field $k$ by a [[commutative ring]].  Then an affine module over the ring $\mathbb{Z}$ of [[integer]]s is precisely a commutative [[heap]], just like a module over $\mathbb{Z}$ is an [[abelian group]].  Note that the definition involving only one "scalar multiplication" operation works if and only if $2$ is invertible in $k$; it\'s not enough that $2 \ne 0$ in $k$.

+-- {: .query}
[[Mike Shulman]]: I haven't thought much about affine modules, but it seems likely to me that the "biased" module-free definitions won't be right any more, since the Lawvere theory needn't be generated by 2-ary or 3-ary operations (as far as I can see).  More explicitly, I don't immediately see how to write an operation like
$$(x_0,x_1,x_2,x_3) \mapsto 4x_0 - 6x_1 - 2x_2 + 5x_3$$
in terms of $A^3\to A$ and $\mathbb{Z}\times A^2\to A$, but it seems to me that this operation should still exist in an affine $\mathbb{Z}$-module.

[[Mike Shulman]]: Well that's rubbish isn't it.  The operation $A^3\to A$ is enough to give you a heap, hence an additive group, and then $\mathbb{Z}\times A^2\to A$ gives you the scalar multiplication.  And so
$$4x_0 - 6x_1 - 2x_2 + 5x_3 = \big((4x_0 - 3y) - y + (-6x_1+7y)\big) - y + \big((-2x_2+3y) - y + (5x_3 - 4y)\big)$$
for any $y$ at all.

_Toby_:  Right.  But I find an affine module of a *rig* to be a trickier concept.

[[Mike Shulman]]: Quite so.  Perhaps first one should look for a version of a [[heap]] corresponding to a [[monoid]]?

_Toby_:  Yes, that would be an affine $\mathbb{N}$-module.
=--


## Affine spaces as model spaces

Affine spaces typically serve as local models for more general kinds of spaces. 

For instance a [[manifold]] is a [[topological space]] that is locally isomorphic to an affine space over the [[real numbers]].  

Similarly, in [[algebraic geometry]] a [[scheme]] is locally isomorphic to an [[affine scheme]].

Therefore there are attempts to axiomatize properties of categories of affine spaces for the purpose of using these as model spaces for more complicated geometries. One such axiomatization is the notion of [[geometry (for structured (∞,1)-toposes)]]. and in particular that of [pregeometry](/nlab/show/geometry+(for+structured+(infinity%2C1%29-toposes%29#Pregeometry).


## Related concepts

* the [[automorphism group]] of an affine space is an _[[affine group]]_

* [[Cartesian space]]

* [[polydisk]]

## References

* [[Aurelio Carboni]], _Categories of Affine Spaces_ , JPAA **61** (1989) pp.243-250.

* [[Aurelio Carboni]], [[George Janelidze]], _Modularity and Descent_ , JPAA **99** (1995) pp.255-265.

* Michel Thi&#233;baud, _Modular Categories_ , pp.386-400 in _Proc. Como conference - Category Theory_ , LNM **1488** Springer Heidelberg 1991.

[[!redirects affine space]]
[[!redirects affine spaces]]
[[!redirects affine vector space]]
[[!redirects affine vector spaces]]
[[!redirects affine linear space]]
[[!redirects affine linear spaces]]
[[!redirects affine-linear space]]
[[!redirects affine-linear spaces]]

[[!redirects affine function]]
[[!redirects affine functions]]
[[!redirects affine linear function]]
[[!redirects affine linear functions]]
[[!redirects affine-linear function]]
[[!redirects affine-linear functions]]
[[!redirects affine map]]
[[!redirects affine maps]]
[[!redirects affine linear map]]
[[!redirects affine linear maps]]
[[!redirects affine-linear map]]
[[!redirects affine-linear maps]]

[[!redirects affine combination]]
[[!redirects affine combinations]]
[[!redirects affine linear combination]]
[[!redirects affine linear combinations]]
[[!redirects affine-linear combination]]
[[!redirects affine-linear combinations]]

[[!redirects affine module]]
[[!redirects affine modules]]
