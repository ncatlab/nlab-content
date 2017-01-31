
# One-sided real numbers
* table of contents
{: toc}

## Summary

There are really two notions of one-sided real number: lower reals and upper reals.  But there is a nearly perfect symmetry between them (although the lower reals seem to get slightly more use).

These are largely concepts in [[constructive mathematics]].  Using [[excluded middle]], a bounded one-sided real number is simply a [[real number]], but constructively they are more general (and less well behaved).  Lower reals are particularly important in constructive [[measure theory]] as the values taken by [[positive measures]] (and more generally are used to define [[extended positive cones]]).

However, even in [[classical mathematics]], there are some differences, at least in emphasis and application.  First, it is most natural to include $\infty$ as a lower real and include $-\infty$ as an upper real.  (However, you can restrict to _bounded_ lower/upper reals to avoid that, or alternatively genralise to _extended_ lower/upper reals if you want to include both $\pm\infty$ at once.)  Also, the natural [[topological structure|topology]] on the lower reals is the _lower [[semicontinuous topology]]_ (and the natural topology on the upper reals is the _upper semicontinuous topology_).

One-sided numbers are sometimes called (upper or lower) *semicontinuous* numbers.  To see why, consider a [[locale]] (or [[topological space]]) $L$, and consider the (upper or lower) [[semicontinuous functions]] (real-valued) on $L$.  On the one hand, these are the same as the [[continuous functions]] from $L$ to (classically) the set of real numbers equipped with the semicontinuous topology or to (constructively) a locale whose [[point of a locale|points]] are the one-sided real numbers.  On the other hand, these semicontinuous functions are precisely the [[internal logic|internal]] one-sided real numbers in the [[topos of sheaves]] over $L$.

Lower and upper reals don\'t interact well together.  Their "intersection" is the set of [[MacNeille real numbers]], which is moderately well-behaved; it also contains the set of [[located real numbers]], which is better-behaved algebraically (but not, constructively, a complete lattice).  But it seems hard, constructively, to find any reasonably behaved notion of "real number" than contains both upper and lower reals.


## Idea

(In the following, 'number' without qualification may be taken to mean either a [[real number]] or a [[rational number]]; the result is the same either way.  Indeed, we could take any [[dense subset|dense set]] of real numbers.)

A __lower real number__ is the [[supremum]] of an [[inhabited set|inhabited]] set of numbers.  A __bounded lower real__ is the supremum of an inhabited set of numbers that has a finite upper bound.  An __extended lower real__ is the supremum of an arbitrary set of numbers.

An __upper real number__ is the [[infimum]] of an inhabited set of numbers.  A __bounded upper real__ is the infimum of an inhabited set of numbers that has a finite lower bound.  An __extended lower real__ is the infimum of an arbitrary set of numbers.

We cannot generalize further by taking more extrema of the same sort.  Explicitly, the supremum of any inhabited set of lower reals is a lower real and the infimum of any inhabited set of upper reals is an upper real.  Similar results obtain if we use either bounded or extended reals, so long as we also either require the set to bounded or allow it to be [[empty subset|empty]].


## Definitions

There are some choices as to how exactly to represent one-sided real numbers; we will define them here as certain [[subsets]] of the set $\mathbb{Q}$ of [[rational numbers]].  If we replaced $\mathbb{Q}$ with any other [[dense subset]] of the [[real line]], then the definitions would end up being equivalent.


### Lower reals

An __extended lower real number__ is any subset $L$ of $\mathbb{Q}$ such that

*  if $a \in L$, then $a \lt b$ for some $b \in L$; and
*  if $a \lt b$ and $b \in L$, then $a \in L$.

We can actually combine these into a single rule:

*  $a \in L$ if and only if $a \lt b$ for some $b \in L$.

A __lower real number__ is an extended lower real $L$ such that:

*  some $a \in L$.

A __bounded lower real number__ is a lower real $L$ such that

*  some $b \notin L$.

When treated explicitly as a subset of $\mathbb{Q}$, we call $L$ a __[[lower set]]__.  When we interpret $L$ as a one-sided real number $x$, we write $a \lt x$ to mean that $a \in L$.  Conversely, we can interpret any rational number, or even any real number, $x$ as a bounded lower real, specifically as the set of all rational numbers less than $x$.  (A bounded lower real is __located__ if it is the lower real obtained in this way from a real number; classically, every bounded lower real number is located.)  We interpret $\infty$ as the lower real whose lower set is all of $\mathbb{Q}$; we interpret $-\infty$ as the extended lower real whose lower set is empty.


### Upper reals

An __extended upper real number__ is any subset $U$ of $\mathbb{Q}$ such that

*  if $b \in U$, then $a \lt b$ for some $a \in U$; and
*  if $a \lt b$ and $a \in U$, then $b \in U$.

We can actually combine these into a single rule:

*  $b \in U$ if and only if $a \lt b$ for some $a \in U$.

An __upper real number__ is an extended upper real $U$ such that:

*  some $b \in U$.

A __bounded upper real number__ is an upper real $U$ such that

*  some $a \notin U$.

When treated explicitly as a subset of $\mathbb{Q}$, we call $U$ an __[[upper set]]__.  When we interpret $U$ as a one-sided real number $x$, we write $x \lt b$ to mean that $b \in U$.  Conversely, we can interpret any rational number, or even any real number, $x$ as a bounded upper real, specifically as the set of all rational numbers greater than $x$.  (A bounded upper real is __located__ if it is the upper real obtained in this way from a real number; classically, every bounded upper real number is located.)  We interpret $-\infty$ as the upper real whose upper set is all of $\mathbb{Q}$; we interpret $\infty$ as the extended upper real whose upper set is empty.


## Order relations

We define [[order]] relations between extended lower reals $x$ and $y$ as follows:

*  $x \lt y$ if and only if there exists a rational number $a$ such that $a \lt y$ but not $a \lt x$;
*  $x \leq y$ if and only if $a \lt y$ for every rational number $a$ such that $a \lt x$.

In other words, $\leq$ is $\subseteq$ on lower sets, and $\lt$ is $\subsetneq$ (in an appropriate sense).

We define order relations between extended upper reals $x$ and $y$ as follows:

*  $x \lt y$ if and only if there exists a rational number $b$ such that $x \lt b$ but not $y \lt b$;
*  $x \leq y$ if and only if $x \lt b$ for every rational number $b$ such that $y \lt b$.

In other words, $\leq$ is $\supseteq$ on upper sets, and $\lt$ is $\supsetneq$.

We now have multiple meanings for $x \lt y$ or $x \leq y$ if one or both of these is already a rational number or a real number, but it is a theorem that the meanings are all consistent.  We also have $-\infty \leq x \leq \infty$ for every extended number $x$, and $-\infty \lt x \lt \infty$ for every bounded number $x$.  Finally, $x \leq y$ if $x \lt y$ or $x = y$; the converse holds classically.

Each version of $\leq$ is a [[partial order]] and each version of $\lt$ is a [[quasiorder]].  By [[excluded middle]], $\leq$ is a [[total order]] and $\lt$ is the corresponding [[linear order]], but neither of these results holds constructively.  In particular, the [[comparison]] law for $\lt$ is invalid, which is why one-sided reals are not as well behaved as ordinary (located) [[real numbers]].


## Suprema and infima

Given any collection of extended lower reals, their __supremum__ is an extended lower real which is found by taking the [[union]] of lower sets.  The supremum of an inhabited set of lower reals is a lower real, and the supremum of an inhabited set of bounded lower reals is bounded iff the set has a bounded lower real as an upper bound.  In any case, this supremum really is the [[supremum]] under $\leq$.  This agrees with the notion of supremum of real numbers in the real number system, when that exists.  Every extended lower real is also the supremum in this sense of its corresponding lower set, interpreted as a set of lower reals that happen to all be rational numbers.

Given any collection of extended upper reals, their __infimum__ is an extended upper real which is found by taking the union of upper sets.  The infimum of an inhabited set of upper reals is an upper real, and the infimum of an inhabited set of bounded upper reals is bounded iff the set has a bounded upper real as a lower bound.  In any case, this infimum really is the [[infimum]] under $\leq$.  This agrees with the notion of infimum of real numbers in the real number system, when that exists.  Every extended upper real is also the infimum in this sense of its corresponding upper set, interpreted as a set of upper reals that happen to all be rational numbers.

By the [[adjoint functor theorem]], suprema of upper reals and infima of lower reals also exist, but they are not constructed as set-theoretic intersections but rather as the [[interior]] of an intersection.  (This construction makes sense even in [[predicative mathematics|predicative]] constructive mathematics, though the adjoint functor theorem does not.)  However, these may not be what we really want; an obvious example of this is if we take the infimum of a set of lower reals that happen to all be located, in which case what we really want is the corresponding *upper* real infimum (for instance, when defining [[located subspaces]]).  (In the [[MacNeille real numbers]], contained in both the lower and upper reals, both infima and suprema are constructed using interiors, and hence neither may be what we want.)

An [[inferior limit]] is ...


## Arithmetic {#arithmetic}

In general, you can extend [[order-preserving functions]] of rational numbers to lower reals and to upper reals; you simply take the [[image]] of the lower or upper set and close it downward or upwards, as appropriate.  If you have an order-reversing function of rational numbers, then you can apply it to a lower real to get an upper real and conversely; this is about the only interaction that I know of between the two kinds of one-sided real.

Since addition is order-preserving, it works nicely, at least to make a [[monoid]]; but [[subtraction]] doesn\'t work in general.  Multiplication has trouble with negative numbers but produces good results if you restrict to $[0,\infty]$.  Notice that we get $0 \cdot \infty = 0$ with lower reals but $0 \cdot \infty = \infty$ with extended upper reals; thus, ${[{0,\infty}[}$ is a [[rig]] for either lower or upper reals, while $[0,\infty]$ is a rig only for lower reals.  (This doesn\'t so much mean that upper reals behave worse than lower reals, as that extended reals on either side behave worse.)  We can also use [[logarithms]] to translate between addition and multiplication.  (In particular, $-\infty + \infty = -\infty$ with extended lower reals but $-\infty + \infty = \infty$ with extended upper reals.)

Of course, arithmetic with one-sided real numbers is much easier than this in [[classical mathematics]], where the bounded or extended versions may be identified; but even there, the natural operations involving $\pm\infty$ may differ.  Accordingly, the conventions for arithmetic with infinities can signal which sort of number is appropriate for a [[constructive mathematics|constructive]] development.

If you want to do arbitrary arithmetic operations constructively on something more general than [[located real numbers]], you can try the [[MacNeille real number|MacNeille reals]], which are contained in both the upper and the lower reals.


## Topology

Let\'s put this on a separate page: [[semicontinuous topology]].  For one thing, it\'s more advanced than the elementary stuff above; for another thing, it\'s more interesting in classical mathematics; and finally, it\'s more complicated in constructive mathematics.  The main point is that each type of one-sided real number has its own natural topology, and these differ (both classically and constructively) from the usual topology on the [[real line]].


## In topos theory

There is a bijective correspondence of [[internalization|internal]] extended lower real numbers in a sheaf topos $\mathrm{Sh}(X)$ of a [[topological space]] $X$ and [[semicontinuous map|lower semicontinuous]] functions $X \to \mathbb{R} \cup \{ +\infty \}$, or equivalently a [[continuous map|continuous]] function $X \to \mathbb{R} \cup \{ +\infty \}$, when the latter is equipped with the [[lower semicontinuous topology]].  (We will work classically in the external logic.)

Let $\Delta(\mathbb{Q})$ denote the [[constant sheaf]] of rational numbers on $X$. A _lower real number_ $U$ in $\mathrm{Sh}(X)$ is then defined as a subsheaf of $\Delta(\mathbb{Q})$ satisfying the axioms above (interpreted in the [[internal language]]). Such a lower real number induces a lower semicontinuous function $x \mapsto \sup U_x$, where $U_x$ denotes the [[stalk]] of $U$ at $x$ (taken as a subset of $\mathbb{Q}$).

Conversely, a lower semicontinuous function $f : X \to \mathbb{R} \cup \{ +\infty \}$ defines an internal lower real number $U$ with sections
$$U(A) \coloneqq \{ \varphi : A \to \mathbb{Q} | \forall x \in A: \varphi(x) \lt f(x) \} \subseteq \Delta(\mathbb{Q})(A)$$
over open sets $A \subseteq X$.

See [Mulvey (1974, page 28)](#Mulvey1974) for details.

For the externally constructive version of this, it is best to take $X$ to be a [[locale]]; we need to use the (external) locale $L$ of lower real numbers in place of $\mathbb{R} \cup \{\infty\}$, and the notion of semicontinuous map is replaced with a continuous map (in the sense of locales) to $L$.


## References

* D. Lesnik, _Synthetic Topology and Constructive
Metric Spaces_ , PhD University of Ljubljana 2010. ([pdf](http://www.fmf.uni-lj.si/storage/19160/PhD_Davorin.pdf))

* [[Chris Mulvey|C. Mulvey]] (1974): _Intuitionistic Algebra and Representations of Rings_. In Hofmann, Liukkonen: _Recent Advances in the Representation Theory of Rings and C\*-Algebras by Continuous Sections_, AMS 1974.
  {#Mulvey1974}

* J. Z. Reichman, _Semicontinuous Real Numbers in a Topos_ , JPAA **28** (1983) pp.81-91.

See also the following MO-discussion: ([link](http://mathoverflow.net/questions/108029/simplification-in-semi-continuous-real?rq=1))

[[!redirects one-sided real]]
[[!redirects one-sided reals]]
[[!redirects one-sided real number]]
[[!redirects one-sided real numbers]]
[[!redirects semicontinuous real]]
[[!redirects semicontinuous reals]]
[[!redirects semicontinuous real number]]
[[!redirects semicontinuous real numbers]]

[[!redirects lower real]]
[[!redirects lower reals]]
[[!redirects lower real number]]
[[!redirects lower real numbers]]
[[!redirects bounded lower real]]
[[!redirects bounded lower reals]]
[[!redirects bounded lower real number]]
[[!redirects bounded lower real numbers]]
[[!redirects extended lower real]]
[[!redirects extended lower reals]]
[[!redirects extended lower real number]]
[[!redirects extended lower real numbers]]
[[!redirects lower semicontinuous real]]
[[!redirects lower semicontinuous reals]]
[[!redirects lower semicontinuous real number]]
[[!redirects lower semicontinuous real numbers]]

[[!redirects upper real]]
[[!redirects upper reals]]
[[!redirects upper real number]]
[[!redirects upper real numbers]]
[[!redirects bounded upper real]]
[[!redirects bounded upper reals]]
[[!redirects bounded upper real number]]
[[!redirects bounded upper real numbers]]
[[!redirects extended upper real]]
[[!redirects extended upper reals]]
[[!redirects extended upper real number]]
[[!redirects extended upper real numbers]]
[[!redirects upper semicontinuous real]]
[[!redirects upper semicontinuous reals]]
[[!redirects upper semicontinuous real number]]
[[!redirects upper semicontinuous real numbers]]
