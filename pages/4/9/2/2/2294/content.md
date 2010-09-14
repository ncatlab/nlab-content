
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

There are two common ways to define a [[category]]:

1. As a [[collection]] $C_0$ of [[objects]] and a collection $C_1$ of [[morphisms]], together with [[source]] and [[target]] maps $C_1\to C_0$, a composition map $C_1\times_{C_0} C_1\to C_1$, and an [[identity assigning map]] $C_0\to C_1$, satisfying axioms.

1. As a collection $C_0$ of objects, together with for each pair $x,y$ of objects, a collection $hom_C(x,y)$ of morphisms, together with identities $1_x\in hom_C(x,x)$ and composition maps $hom_C(y,z)\times hom_C(x,y)\to hom_C(x,z)$, satisfying axioms.

In [[logic|logical]] terms, the first is formulated as a $2$-sorted theory in [[first-order logic]], while the second is a [[dependent type theory|dependently typed theory]]; the usual way of interpreting any dependently typed theory as an independently sorted theory turns the latter into the former.

However, there is a third way of defining a category which uses only one collection (representing the collection of morphisms) and thus is formulated as an untyped (or $1$-sorted) first-order theory.  Note that this is *not* the usual way of replacing sorts with predicates, but instead a slightly clever trick.  The basic idea is that an [[object]] can be identified with its [[identity morphism]].  This reformulation is occasionally useful, but mostly for technical reasons.


## Definition

A **category** (single-sorted version) is a [[collection]] $C$, whose elements are called _morphisms_, together with two functions $s,t:C\to C$ and a [[partial function]] $\circ:C\times C\dashrightarrow C$, such that:

1. $s(s(x)) = s(x) = t(s(x))$
2. $t(t(x)) = t(x) = s(t(x))$
3. $x\circ y$ is defined if and only if $s(x)=t(y)$.
4. If $x\circ y$ is defined, then $s(x\circ y) = s(y)$ and $t(x\circ y)=t(x)$.
5. $x\circ s(x)=x$ and $t(x)\circ x=x$ (both composites are always defined, because of the first two axioms)
6. $(x\circ y)\circ z = x\circ (y\circ z)$, if either is defined (in which case the other is defined by the axiom 3).

The first two axioms say that $s$ and $t$ are [[idempotent]] endofunctions on $C$ which have the same [[image]].  The elements of their common image (the $x$ such that $s(x)=x$, or equivalently $t(x)=x$) are called _identities_ or _objects_.  Once that is done, the rest of the identification is straightforward.

A **[[functor]]** between single-sorted categories is just a function $f:C\to D$ such that $f(s(x)) = s(f(x))$, $f(t(x)) = t(f(x))$, and $f(x\circ y)= f(x)\circ f(y)$ whenever $x\circ y$ is defined (which, by the first two axioms of a functor and axiom (3) of a category, implies that $f(x)\circ f(y)$ is defined).

Finally, a **[[natural transformation]]** between functors $f,g:C\to D$ of single-sorted categories is a function $\alpha:C\to D$ such that $s(\alpha(x)) = s(f(x))$, $t(\alpha(x)) = t(g(x))$, and $\alpha(x) \circ f(y) = g(x) \circ \alpha(y)$ whenever $x\circ y$ is defined (which implies that both composites in this identity are defined).  Note that while a natural transformation is ordinarily defined to consist of a component $\alpha(x)$ only when $x$ is an _object_, this definition supplies a component to each _morphism_.  In terms of the usual definition, the component of $\alpha$ at a morphism is the diagonal of the corresponding naturality square.

It can now be proved that single-sorted categories, functors, and natural transformations form a $2$-[[2-category]] which is (strictly) [[equivalence of categories|equivalent]] to the usual $2$-category [[Cat]].


## Remarks

### Specializations

A [[monoid]] is a single-sorted category in which $s$ is a constant function (hence so is $t$, and they are equal).  This works up to [[isomorphism of categories]], not merely equivalence, so single-sorted categories may seem to be a more direct [[oidification]] of monoids than the usual categories.


### Internalization

The usual definition of an [[internal category]] is two-sorted, but the one-sorted definition can also be interpreted [[internalization|internally]].  While the usual notion of internal category requires the [[ambient category]] only to have [[pullbacks]], the one-sorted version appears to require one to make sense of an "internal partial binary operation."  However, since in this case the domain of $\circ$ is specified explicitly in the definition, one can just require $\circ$ to be an ordinary morphism whose domain is the pullback of $s$ and $t$; thus only pullbacks are required for the single-sorted definition as well.

It is easy to see that any internal two-sorted category gives an internal one-sorted category (consider the object of arrows).  The converse is true as long as the ambient category has [[split idempotents]], for then given an internal one-sorted category we can split either $s$ or $t$ to obtain an object of objects.  In general, however, the two concepts are not equivalent.


### Generalizations

There exist similar single-sorted definitions of $n$-[[n-categories|categories]] and [[∞-categories]].  The single sort in the definition of $n$-category is the set of $n$-morphisms, but you can also think of this as the union (over all $k \leq n$) of the sets of $k$-morphisms, as long as you identify each $k$-morphism (for $k \lt n$) with its identity $(k+1)$-morphism.  In the the definition of $\infty$-category, there is no notion of $\infty$-morphism to take care of everything at once, but the single sort can still be understood as this union (now over all $k$).


## References

* _[[Categories Work]]_, I.1 and XII.5.


[[!redirects single-sorted definition of category]]
[[!redirects single-sorted definition of a category]]
[[!redirects single-sorted definition of categories]]
[[!redirects single-sorted definitions of category]]
[[!redirects single-sorted definitions of a category]]
[[!redirects single-sorted definitions of categories]]
