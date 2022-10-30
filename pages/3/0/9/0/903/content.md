
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

The _homotopy groups_ $\pi_n(X,x)$ of a [[pointed object|pointed]] 
[[topological space]] $(X,x)$ are a sequence of [[groups]] that generalise the [[fundamental group]] $\pi_1(X,x)$ to higher [[homotopy (as a transformation)|homotopies]].

The $n$th homotopy group $\pi_n(X,x)$ has as elements [[equivalence classes]] of [[spheres]] $\gamma : S_*^n \to X_*$ in $X$ where two such are regarded as equivalent if there is a [[left homotopy]] $\gamma \Rightarrow \gamma'$ between them, fixing the base point. The group operation is given by gluing of two spheres at their basepoint.

In degree 0, $\pi_0(X,x)$ is not a group but merely a [[pointed set]].  In degree $n \geq 2$ all homotopy groups are [[abelian groups]].  Only $\pi_1(X,x)$ may be an arbitrary group.  In general, $\pi_n(X,x)$ is an $n$-[[k-tuply groupal n-groupoid|tuply groupal]] set.

Lower homotopy groups [[action|act]] on higher homotopy groups; the nonabelian group cohomology of this gives the Postnikov invariants of the space.  All of this data put together allows one to reconstruct the original space, at least up to weak [[homotopy type]], through its [[Postnikov system]].

These definitions only depend on the [[homotopy type]] of $X$, by definition: a [[weak homotopy equivalence]] between topological spaces is a [[continuous map]] that induces an [[isomorphism]] on all homotopy groups.

Accordingly, homotopy groups are defined for all other models of [[homotopy types]], notably for [[simplicial sets]]. See at _[[simplicial homotopy group]]_ for more. 

## Definition 
 {#Definition}

### For topological spaces
 {#ForTopologicalSpaces}

Let $X$ be a [[topological space]], let $x : * \to X$ be a point, to be called the _base point_.

For $n \in \mathbb{N}$, write $S^n$ be the pointed $n$-[[sphere]].

+-- {: .num_defn}
###### Definition

The underlying set of $\pi_n(X,x)$ is the set of 
[[equivalence classes]] of basepoint-preserving [[continuous functions]] 

$$
  \gamma : S^n \to X
$$

where two such are regarded as equivalent if there is a basepoint-preserving [[left homotopy]] between them.  

=--

Now we will put some structure on that set.

+-- {: .num_defn}
###### Definition

There are $n$ independent equators through the basepoint of $S^n$.  Given two maps $f, g: S^n \to (X,x)$, form their [[coproduct|copairing]] in the category of pointed spaces to get a map 

$$
  S^n \vee S^n \to (X,x)
$$ 

(where $\vee$ indicates the [[wedge sum]]); then combine this with a map $S^n \to S^n \vee S^n$ that maps the $i$th equator to the basepoint and each hemisphere to one copy of the sphere.  The result is a map $S^n \to (X,x)$, called the $i$th __concatenation__ of $f$ and $g$:

$$
  S^n \to_i S^n \vee S^n \stackrel{[f,g]}{\to} (X,x)
  \,.
$$

One can check that each of these operations respects homotopy equivalence and hence equips $\pi_n(X,x)$ with the structure of a [[magma]].

=--

+-- {: .num_prop}
###### Proposition

These magmas are in fact [[groups]]; in particular:

* the [[constant function]] that maps all of $S^n$ to $x$ represents the __null element__ of $\pi_n(X,x)$, which is an identity for every concatenation.

=--

+-- {: .num_defn}
###### Definition

This may seem like quite a complicated kind of structure, but it is actually quite simple up to homotopy.  First of all, all $n$ concatenations of given maps $f$ and $g$ are homotopic, so we speak of simply a single __concatenation__ for $n \geq 1$ (and none for $n = 0$).  By the [[Eckmann?Hilton argument]], this concatenation will be commutative up to homotopy for $n \geq 2$.  In any case, it is [[associativity|associative]] and [[inverse|invertible]] up to homotopy, and the null element is an identity up to homotopy.

=--

+-- {: .num_prop}
###### Proposition

The result is that the set $\pi_n(X,x)$ of equivalence classes is an abelian group for $n \geq 2$, a group for $n = 1$, and a pointed set for $n = 0$ (when the null element is the only structure).

=--

+-- {: .num_prop}
###### Proposition

If $X$ is [[connected space|path-connected]], then all of the $\pi_n(X,a)$ are [[iomomorphism|isomorphic]].  Accordingly, it\'s traditional to just write $\pi_n(X)$ in that case.  (This is why we must use $\Pi_n(X)$ for the homotopy $n$-groupoid.)  However, there may be many different isomorphisms between $\pi_n(X,a)$ and $\pi_n(X,b)$ (given by $\pi_{n+1}(X)$), so a more careful treatment requires keeping track of the basepoint even in the connected case.

=--


### For simplicial sets 

See [[simplicial homotopy group]].


### For Lie groupoids

* [[homotopy groups of a Lie groupoid]]


### For objects in a general $\infty$-stack $(\infty,1)$-topos 

[[Top]] is the archetypical [[(∞,1)-topos]].
The definition of homotopy groups for objects in [[Top]]
is just a special case of a general definition of
homotopy groups of objects of [[∞-stack]] [[(∞,1)-topos]]es.

This is described in detail at

* [[homotopy groups in an (∞,1)-topos]].


## Truncated and connected spaces {#truncconn}

Often it is useful to talk about spaces whose homotopy groups are all trivial above or below a certain degree, for instance in the context of [[Postnikov towers]] and [[Whitehead towers]].

For $n = -1, 0, 1, 2, \ldots, \infty$:

* a space is **$n$-[[truncated space|truncated]]** if all homotopy groups _above_ degree $n$ are trivial.

* a space is **$n$-[[n-connected space|connected]]** (or **$n$-simply connected**) if it is [[inhabited space|inhabited]] and all homotopy groups _at or below_ degree $n$ are trivial.

Vacuously, every space is $\infty$-truncated, and precisely the inhabited spaces are $(-1)$-connected.  On the other end, precisely the weakly [[contractible spaces]] are $\infty$-connected, and a space is $(-1)$-truncated iff it is weakly contractible if inhabited.  (So [[classical mathematics|classically]], using [[excluded middle]], a space is $(-1)$-truncated iff it is either [[empty space|empty]] or weakly contractible.)

To extend one step further in [[negative thinking]], every space (even the empty space) is $(-2)$-connected, and precisely a weakly contractible space (but not the empty space) is $(-2)$-truncated.

* A [[pointed space]] is a **degree-$n$ [[Eilenberg?MacLane space]]** if it is both $n$-truncated as well as $(n-1)$-connected, i.e. if its only nontrivial homotopy group is in degree $n$.

A weakly contractible space is an Eilenberg&#8211;MacLane space in every degree, and these are the only Eilenberg&#8211;MacLane spaces in degree $\infty$ or $-1$.  In degree $0$, they are the pointed [[discrete space]]s (and those weakly homotopy equivalent to such).  In degree $1$, they are (up to weak homotopy equivalence) precisely the [[classifying spaces]] of [[groups]].  And so on.


## Examples

### In low dimensions

The $0$th homotopy 'group' $\pi_0(X,a)$ can be identified with the set of all [[path component]]s of $X$, with the component containing $a$ as the basepoint.  Similarly, the [[fundamental infinity-groupoid|fundamental 0-groupoid]] $\Pi_0(X)$ is the set of all path components without a chosen basepoint.  Note that $\Pi_0(X)$ is traditionally written $\pi_0(X)$, even without a basepoint.

The $1$st homotopy group $\pi_1(X,a)$ is precisely the [[fundamental group]] of $X$ at $a$.  This is the original example from which all others derived.  It was once written simply $\pi(X,a)$ with the $\pi$ standing for Poincar&#233;, who invented it.

+--{.query}
At least, that\'s where I *think* that it comes from ...  ---Toby
=--


### Of the circle

The first homotopy group of the [[circle]] $S^1$ is the group of [[integer]]s.

$$
  \pi_1(S^1) \simeq \mathbb{Z}
  \,.
$$

A formalization of a proof of this in [[homotopy type theory]] is in ([Shulman](#ShulmanPi1S1)).


### Of spheres

See [[homotopy groups of spheres]].


## History 

In the early years of the 20th century it was known that the nonabelian fundamental group $\pi_1(X,a)$ of a space $X$ with base point $a$ was useful in geometry and complex analysis. It was also known that the abelian [[homology group]]s $H_n(X)$ existed for all $n \geq 0$ and that if $X$ is connected then $H_1(X)$ is isomorphic to the abelianisation of any $\pi_1(X,a)$. 

Consequently it was hoped to generalise the fundamental group to higher dimensions, producing nonabelian groups whose abelianisations would be the homology groups.

In 1932, E. &#268;ech proposed a definition of higher homotopy groups using maps of spheres, but the paper was rejected for the Zurich ICM since it was found that these groups $\pi_n(X,a)$ were abelian for $n \geq 2$, and so do not generalise the fundamental group in the way that was originally desired.  Nonetheless, they have proved to be extremely important in homotopy theory, although more difficult to compute in general than homology groups.  See [[weak homotopy equivalence]].


## Properties 

It was early realised that the fundamental groupoid $\Pi_1(X)$ operates on the family of groups $\{\pi_n(X,a) | a \in X\}$ which should thus together be regarded as a module over $\pi_1(X,a)$.

A key property of homotopy groups is the _Whitehead theorem_: if $f:X \to Y$ is a map of connected [[m-cofibrant spaces]] (spaces each of the homotopy type of a [[CW complex]]), and $f$ induces isomorphisms $\pi_n(X,a) \to \pi_n(Y,f(a))$ for some $a$ and all $n \geq 1$, then $f$ is a [[homotopy equivalence]].

However, the homotopy groups by themselves, even considering the operations of $\pi_1$, do not characterise homotopy types. See also [[algebraic homotopy|algebraic homotopy theory]].

See also the _[[Freudenthal suspension theorem]]_.


## Some general nonsense 

Using the [[Eckmann?Hilton duality]] between
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


## Related concepts

* [[weak homotopy equivalence]]

* [[p-localization]]

* [[Goodwillie calculus]]

* [[homotopy groups in an (infinity,1)-topos]]

## References

### General

* [[Michael Hutchings]], _Introduction to higher homotopy groups and obstruction theory_ ([pdf](http://math.berkeley.edu/~hutching/teach/215b-2011/homotopy.pdf))
 {#Hutchings}


### Formalization in HoTT

Homotopy groups and their properties can naturally be formalized in [[homotopy type theory]]. In this context a proof that $\pi_1(S^1)\simeq \mathbb{Z}$ is in

* [[Mike Shulman]], _[P1S1.v](https://github.com/HoTT/HoTT/blob/master/Coq/HIT/Pi1S1.v)_
{#ShulmanPi1S1}

* [[Dan Licata]], [[Mike Shulman]], _Calculating the fundamental group of the circle in homotopy type theory_ ([pdf](http://www.cs.cmu.edu/~drl/pubs/ls13pi1s1/ls13pi1s1.pdf))

and a proof that 

$\pi_k(S^n) \simeq \left\{ \array{ 0 & for \;k \lt n \\ \mathbb{Z} & for\; k = n} \right.$ 

is in 

* [[Dan Licata]], [[Guillaume Brunerie]], _[PiNSN.agda](https://github.com/dlicata335/hott-agda/blob/master/homotopy/PiNSN.agda)_

[[!redirects homotopy group]]
[[!redirects homotopy groups]]
[[!redirects homotopy n-tuply groupal set]]
[[!redirects homotopy n-tuply groupal sets]]
[[!redirects homotopy groupal set]]
[[!redirects homotopy groupal sets]]
[[!redirects homotopy pointed set]]
[[!redirects homotopy pointed sets]]
[[!redirects homotopy abelian group]]
[[!redirects homotopy abelian groups]]
