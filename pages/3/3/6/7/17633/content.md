
# (Semi)definiteness
* table of contents
{: toc}

## Idea

There are many contexts where terms such as 'positive definite', 'negative semidefinite', and 'indefinite' appear.  This is an attempt to describe a general framework in which these may be used.  Warning: this may be [[centipede mathematics]].


## Definitions

Let $A$ be a [[set]] equipped with both a [[partial order]] $\leq$ (whose [[opposite relation|opposite]] is denoted $\geq$), a [[symmetric relation]] $#$, and a [[basepoint]] $0$.  (The notation $#$ is to put one in mind of [[inequality]], but it is nontrivial even in [[classical mathematics]], and it is rarely [[tight relation|tight]].  It\'s not even always [[irreflexive|irreflexive]], although that is very common.)

We write $\lt$ for the conjunction of $\leq$ and $#$ (and $\gt$ for its opposite, the conjunction of $\geq$ and $#$).

An element $x$ of $A$ is:

* __positive__ (or _positive semidefinite_) if $x \geq 0$,
* __negative__ (or _negative semidefinite_) if $x \leq 0$,
* __semidefinite__ if $x$ is positive or negative,
* __indefinite__ if $x$ is not semidefinite,
* __nonsingular__ (or _nondegenerate_) if $x # 0$,
* __definite__ if $x$ is semidefinite and nonsingular,
* __positive definite__ if $x \gt 0$ (that is if $x$ is both positive and nonsingular),
* __negative definite__ if $x \lt 0$ (that is if $x$ is both negative and nonsingular).

Note that a positive or negative element must be semidefinite, so 'positive semidefinite' and 'negative semidefinite' are redundant; in many contexts, however, this redundancy is useful, since 'positive' and 'negative' are so widely used in other contexts.  Also, since a semidefinite element is definite iff it\'s nonsingular, 'positive definite' and 'negative definite' really mean what they say.

In [[constructive mathematics]], it is not the partial order $\leq$ that is most relevant but rather the relation $\nleq$, which classically is the [[negation]] of $\leq$ but which constructively is generally stronger.  This relation $\nleq$ is required to satisfy properties [[de Morgan duality|dual]] to those of a partial order ([[irreflexive relation|irreflexivity]], [[comparison]], and [[connected relation|connectedness]]), and $\leq$ is then defined as the negation of $\nleq$ (and can be proved to be a partial order).  Constructively, we say that $x$ is __indefinite__ if $x \nleq 0$ and $x \ngeq 0$, and that $x$ is __semidefinite__ if it is not indefinite; these are equivalent to the above in [[classical logic]], and all of the other definitions read the same.  In particular, &#8249;semidefinite&#8250; is not &#8249;positive or negative&#8250; but rather the [[double negation]] of that.  (All that said, if one is willing to give up &#8249;indefinite&#8250;, then there is no need for $\nleq$, although &#8249;semidefinite&#8250; should still be a double negation.)

We will also say that $A$ (or rather, the structure $(A,\leq,#)$) is __nontrivial__ if $#$ is [[irreflexive|irreflexive]].

Suppose that $A$ has the structure of a [[group]], which we will write additively (but without assuming commutativity).  We will say that the group structure is _right-compatible_ with other structure ($\leq$, $#$, and $0$) if

* $0$ is the [[identity element]] of the group,
* $x \leq y$ iff $y - x \geq 0$, and
* $x # y$ iff $y - x # 0$.

Thus $\leq$ and $#$ are entirely recoverable from the positive and nonsingular elements, respectively.  (Constructively, we require that $x \nleq y$ iff $y - x \nleq 0$.)  Note that in this case, $A$ is nontrivial iff $0 # 0$ is false.

We can similarly say when $A$ is _left-compatible_.  (By symmetry of $#$, this half of the compatibility condition is the same.)  Of course, if $A$ is [[abelian group|commutative]], then left- and right-compatibility are the same entirely.


## Examples

If $A$ is the set of [[real numbers]], then give $\leq$, $#$, and $0$ their usual meanings.  (The usual meaning of $#$ is [[apartness]], which classically is the same as [[denial inequality|ordinary inequality]].)  Then $\lt$ and $\gt$ also have their usual meanings.  (We also have that $\nleq$ is the same as $\gt$, and $\ngeq$ is the same as $\lt$.)  The positive-semidefinite elements are the nonnegative ones, but the positive definite elements are the (strictly) [[positive numbers]]; every real number is semidefinite, and none is indefinite.  The (commutative) additive group structure is compatible, and $A$ is nontrivial.

The previous example (except for the final sentence) can be used with any [[pointed set|pointed]] [[linear order]].  (Constructively, define $\nleq$ to be $\gt$ and go from there.)  Assuming that $A$ is [[inhabited|inhabited]] (nonempty), this is nontrivial.

If $A$ is the set of [[upper real number|upper]], [[lower real number|lower]], or [[MacNeille real number|MacNeille]] real numbers, then there is really nothing new classically; $\infty$ is positive definite, $-\infty$ is negative definite, and that is all.  Constructively, however, neither $\leq$ and $\lt$ (with their usual meanings in the relevant context) is the negation of the other.  Nevertheless, if we define $x # y$ to mean that $x \lt y$ or $x \gt y$, then everything goes through.  If we restrict to the bounded numbers, then the additive group structure is compatible too.

If $A$ is the set of [[complex numbers]], then let $x \leq y$ mean that $y - x$ is a nonnegative real, and give $#$ its usual meaning (apartness, which classically is ordinary inequality).  Then the positive-semidefinite elements are the nonnegative real numbers, the positive-definite elements are the strictly positive real numbers, the semidefinite elements are the real numbers, and the indefinite elements are the (not necessarily purely) [[imaginary numbers]].  The additive group structure is compatible, and this $A$ is nontrivial.

The previous example generalizes to any algebra of [[hypercomplex numbers]].  (Even the [[trivial algebra]] is nontrivial, for once.)

If $A$ is the set of sets of real or complex numbers (so a [[power set]]), then let $x \leq y$ mean that every element of $x$ is $\leq$ every element of $y$, $x # y$ mean that $x$ and $y$ are [[disjoint sets|disjoint]], and $0$ be the [[singleton subset|singleton]] $\{0\}$.  (Constructively, let $x \nleq y$ mean that some element of $x$ is $\nleq$ some element of $y$.)  Then $x \lt y$ mean that every element of $x$ is $\lt$ every element of $y$.  The positive-semidefinite elements are those sets whose members are all nonnegative reals, the positive-definite ones are those whose members are all strictly positive reals, the indefinite ones are those that have at least one imaginary member *or* at least one positive member and at least one negative member, and the nonsingular elements are those whose members are all nonzero.  (In particular, the [[empty subset|empty set]] is nondegenerate, for once.)  There is no compatible group structure, and this example is *not* nontrivial (since $\emptyset # \emptyset$).

The power-set construction above can be applied to any example to produce a new example.  This new example never has a compatible group structure and is never nontrivial.

If $A$ is any real&#8209; or complex-valued [[function set]], then let $x \leq y$ mean that $x_n \leq y_n$ for every $n$ in the [[domain]] of the functions, let $x # y$ mean that $x_n # y_n$ for every $n$, and let $0$ be the [[constant function]] with value zero.  (Constructively, let $x \nleq y$ if $x_n \nleq y_n$ for *some* $n$.)  Then $x \lt y$ means that $x_n \lt y_n$ for every $n$.  The positive semidefinite elements are those functions that take only nonnegative real values, the positive definite elements are those that take only strictly positive real values, the indefinite elements are those that take at least one imaginary value *or* at least one positive value and at least one negative value, and the nonsingular elements are those that take only nonzero values.  The piecewise-defined additive group structure is compatible, and $A$ is nontrivial iff the domain of the functions is [[inhabited set|inhabited]].  Every function has a [[range]], and a function is positive definite, etc, if and only if its range is (in the sense of the power-set example above).

The function-set construction above can be applied to any example to produce a new example.  If the original example had a compatible group structure, so does the new example; if the original example was nontrivial, then so is the new example iff the domain is inhabited.

If $A$ is the set of symmetric [[bilinear forms]] on some real [[vector space]] $V$ or the set of conjugate-symmetric [[sesquilinear forms]] on some complex vector space $V$, then 'semidefinite' etc have the meanings given at [[inner product space]].  (Constructively, we require $V$ to have a compatible [[apartness relation]], or else we cannot define 'indefinite'.)  The obvious additive group structure is compatible (which explains what $\leq$, $#$, and $0$ mean), and $A$ is nontrivial iff $V$ is nonzero.

If $A$ is the set of $n$-by-$n$ real or complex [[matrices]] for some [[natural number]] $n$, then 'positive definite' and the rest have all of their usual meanings.  The additive group structure is compatible, and $A$ is nontrivial iff $n \gt 0$.  In [[classical mathematics]] (and more generally, assuming [[weak countable choice]]), every matrix gives rise to a set of complex numbers, its set of complex [[eigenvalues]], and then a matrix is positive definite, etc, exactly when its set of complex eigenvalues is (in the sense of the power-set example above).

Generalizing the previous example, if $A$ is a real or complex $*$-[[star-algebra|algebra]] (with apartness, constructively, if we wish to define 'indefinite'), then all of the terms have their usual meanings there too.  (Note that $x \leq y$ means that $y - x = u^* u$ for some $u$, and $x # y$ means that $y - x$ is invertible.  Constructively, $x \nleq y$ means that $y - x$ is apart from $u^* u$ for all $u$.)  The additive group structure is compatible, and $A$ is nontrivial in our sense iff it is [[trivial algebra|nontrivial as a real algebra]].

From any example, we may form another example by restricting to a [[subset]] of $A$, as long as $0$ belongs.  If the original example has a compatible group structure, then so does the subset if it is a [[subgroup]].  If the original example is nontrivial, then so is the subset iff it is [[inhabited subset|inhabited]].


[[!redirects semidefinite]]
[[!redirects semidefiniteness]]
[[!redirects semidefinite element]]
[[!redirects semidefinite elements]]

[[!redirects positive semidefinite]]
[[!redirects positive semidefiniteness]]
[[!redirects positive semidefinite element]]
[[!redirects positive semidefinite elements]]
[[!redirects positive-semidefinite]]
[[!redirects positive-semidefiniteness]]
[[!redirects positive-semidefinite element]]
[[!redirects positive-semidefinite elements]]

[[!redirects negative semidefinite]]
[[!redirects negative semidefiniteness]]
[[!redirects negative semidefinite element]]
[[!redirects negative semidefinite elements]]
[[!redirects negative-semidefinite]]
[[!redirects negative-semidefiniteness]]
[[!redirects negative-semidefinite element]]
[[!redirects negative-semidefinite elements]]

[[!redirects definite]]
[[!redirects definiteness]]
[[!redirects definite element]]
[[!redirects definite elements]]

[[!redirects positive definite]]
[[!redirects positive definiteness]]
[[!redirects positive definite element]]
[[!redirects positive definite elements]]
[[!redirects positive-definite]]
[[!redirects positive-definiteness]]
[[!redirects positive-definite element]]
[[!redirects positive-definite elements]]

[[!redirects negative definite]]
[[!redirects negative definiteness]]
[[!redirects negative definite element]]
[[!redirects negative definite elements]]
[[!redirects negative-definite]]
[[!redirects negative-definiteness]]
[[!redirects negative-definite element]]
[[!redirects negative-definite elements]]

[[!redirects indefinite]]
[[!redirects indefiniteness]]
[[!redirects indefinite element]]
[[!redirects indefinite elements]]
