
#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

The _homotopy groups_ $\pi_n(X,a)$ of a [[pointed object|pointed]] space $(X,a)$ are a sequence of [[groups]] that generalise the [[fundamental group]] $\pi_1(X,a)$ to higher [[homotopy (as a transformation)|homotopies]].

Actually, $\pi_0(X,a)$ is not a group at all but merely a [[pointed set]].  Conversely, $\pi_2(X,a)$ and above are all [[abelian groups]].  Only $\pi_1(X,a)$ may be an arbitrary group.  In general, $\pi_n(X,a)$ is an $n$-[[k-tuply groupal n-groupoid|tuply groupal]] set.

Lower homotopy groups act on higher homotopy groups; the nonabelian group cohomology of this gives the Postnikov invariants of the space.  All of this data put together allows one to reconstruct the original space, at least up to weak [[homotopy type]], through its [[Postnikov system]].

# Definition 

## for topological spaces##

Let $S^n$ be the pointed $n$-[[sphere]], that is an $n$-dimensional real sphere equipped with any basepoint.  The underlying set of $\pi_n(X,a)$ will be the set of basepoint-preserving continuous maps from $S^n$ to $(X,a)$, with such maps identified if there is a basepoint-preserving [[homotopy]] between them.  Now we will put some structure on that set.

First, the [[constant function]] that maps all of $S^n$ to $a$ is the __null element__ of $\pi_n(X,a)$.  Now, there are $n$ independent equators through the basepoint of $S^n$.  Given two maps $f, g: S^n \to (X,a)$, form their [[coproduct|copairing]] in the category of pointed spaces to get a map $S^n \vee S^n \to (X,a)$ (where $\vee$ indicates the [[wedge sum]]); then combine this with a map $S^n \to S^n \vee S^n$ that maps the $i$th equator to the basepoint and each hemisphere to one copy of the sphere.  The result is a map $S^n \to (X,a)$, called the $i$th __concatenation__ of $f$ and $g$:
$$S^n \to_i S^n \vee S^n \to^{[f,g]} (X,a)$$
One can check that this operation respects homotopy equivalence.

This seems like quite a complicated kind of structure, but it is actually quite simple up to homotopy.  First of all, all $n$ concatenations of given maps $f$ and $g$ are homotopic, so we speak of simply a single __concatenation__ for $n \geq 1$ (and none for $n = 0$).  By the [[Eckmann-Hilton argument]], this concatenation will be commutative up to homotopy for $n \geq 2$.  In any case, it is associative and invertible up to homotopy, and the null element is an identity up to homotopy.

The result is that the set $\pi_n(X,a)$ of equivalence classes is an abelian group for $n \geq 2$, a group for $n = 1$, and a pointed set for $n = 0$ (when the null element is the only structure).

Note that if $X$ is [[connected space|path-connected]], then all of the $\pi_n(X,a)$ are isomorphic.  Accordingly, it\'s traditional to just write $\pi_n(X)$ in that case.  (This is why we must use $\Pi_n(X)$ for the homotopy $n$-groupoid.)  However, there may be many different isomorphisms between $\pi_n(X,a)$ and $\pi_n(X,b)$ (given by $\pi_{n+1}(X)$), so a more careful treatment requires keeping track of the basepoint even in the connected case.

### Low-dimensional cases ###

The $0$th homotopy 'group' $\pi_0(X,a)$ can be identified with the set of all [[path component]]s of $X$, with the component containing $a$ as the basepoint.  Similarly, the [[fundamental infinity-groupoid|fundamental 0-groupoid]] $\Pi_0(X)$ is the set of all path components without a chosen basepoint.  Note that $\Pi_0(X)$ is traditionally written $\pi_0(X)$, even without a basepoint.

The $1$st homotopy group $\pi_1(X,a)$ is precisely the [[fundamental group]] of $X$ at $a$.  This is the original example from which all others derived.  It was once written simply $\pi(X,a)$ with the $\pi$ standing for Poincar&#233;, who invented it.

+--{.query}
At least, that\'s where I *think* that it comes from ...  ---Toby
=--

## for simplicial sets ##

See [[simplicial homotopy group]].

## for objects in a general $\infty$-stack $(\infty,1)$-topos ##

[[Top]] is the archetypical [[(∞,1)-topos]].
The definition of homotopy groups for objects in [[Top]]
is just a special case of a general definition of
homotopy groups of objects of [[∞-stack]] [[(∞,1)-topos]]es.

This is described in detail at
[[homotopy group (of an ∞-stack)]].

# History #

In the early years of the 20th century it was known that the nonabelian fundamental group $\pi_1(X,a)$ of a space $X$ with base point $a$ was useful in geometry and complex analysis. It was also known that the abelian [[homology group]]s $H_n(X)$ existed for all $n \geq 0$ and that if $X$ is connected then $H_1(X)$ is isomorphic to the abelianisation of any $\pi_1(X,a)$. 

Consequently it was hoped to generalise the fundamental group to higher dimensions, producing nonabelian groups whose abelianisations would be the homology groups.

In 1932, E. &#268;ech proposed a definition of higher homotopy groups using maps of spheres, but the paper was rejected for the Zurich ICM since it was found that these groups $\pi_n(X,a)$ were abelian for $n \geq 2$, and so do not generalise the fundamental group in the way that was originally desired.  Nonetheless, they have proved to be extremely important in homotopy theory, although more difficult to compute in general than homology groups.  See [[weak homotopy equivalence]].

# Properties #

It was early realised that the fundamental groupoid $\Pi_1(X)$ operates on the family of groups $\{\pi_n(X,a) | a \in X\}$ which should thus together be regarded as a module over $\pi_1(X,a)$.

A key property of homotopy groups is the _Whitehead theorem_: if $f:X \to Y$ is a map of connected [[m-cofibrant spaces]] (spaces each of the homotopy type of a [[CW complex]]), and $f$ induces isomorphisms $\pi_n(X,a) \to \pi_n(Y,f(a))$ for some $a$ and all $n \geq 1$, then $f$ is a [[homotopy equivalence]].

However, the homotopy groups by themselves, even considering the operations of $\pi_1$, do not characterise homotopy types. See also [[algebraic homotopy|algebraic homotopy theory]].

See also the [[Freudenthal suspension theorem]].

# Some general nonsense #

Using the [[Eckmann-Hilton duality]] between
[[cohomology]] and [[homotopy (as an operation)]] one may discuss homotopy groups along the same lines as the discussion of [[cohomology groups]]  (see there).

From that perspective we might say that:

for $B, X$ any two objects in an [[(∞,1)-topos]] $\mathbf{H}$, the "homotopy of $X$ with co-coefficients $B$" is the [[hom-set]]
  $$
    \pi_H(X,B) := H(B,X) := \pi_0 \mathbf{H}(B,X)
    \,,
  $$
  where $\pi_H$ denotes the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathbf{H}$.

For the special case that the object $B$ here is a [[co-group object]], this _homotopy set_ $\pi(X,B)$ naturally inherits the structure of a [[group]].

The standard example is that where $B = S^n$ is the $n$-[[sphere]]. This naturally comes with an co-group structure up to homotopy, which is precisely the structure underlying the co-category structure of the [[interval object]] and more generally that underlying the mechanism of the [[Trimble n-category]].

As opposed to [[cohomology]] where people are used to talking about [[generalized cohomology]], "homotopy" usually just means this ordinary homotopy for $B = S^n$.

[[!redirects homotopy groups]]