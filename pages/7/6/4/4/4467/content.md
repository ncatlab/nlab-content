# Formal topology
* table of contents
{: toc}

## Idea

Formal topology is a programme for doing [[topology]] in a [[finite mathematics|finite]], [[predicative mathematics|predicative]], and [[constructive mathematics|constructive]] fashion.

It is a kind of pointless topology; in the context of [[classical mathematics]], it reproduces the theory of [[locales]] rather than [[topological spaces]] (although of course one can recover topological spaces from locales).

The basic definitions can be motivated by an attempt to study locales entire through the [[(0,1)-site|sites]] that generate them.  However, in order to recover all basic topological notions (particularly those associated with *closed* rather than *open* features) predicatively, we need to add a 'positivity' relation to the 'coverage' relation of sites.


## Definitions

A __formal topology__ or __formal space__ is a [[set]] $S$ together with

*  an [[element]] $\top$ of $S$,
*  a [[binary operation]] $\cap$ on $S$,
*  a [[binary relation]] $\lhd$ between elements of $S$ and [[subsets]] of $S$, and
*  a [[unary relation]] $\vdash$ on $S$,

such that

1.  $a = b$ whenever $a \lhd \{b\}$ and $b \lhd \{a\}$,
2.  $a \lhd U$ whenever $a \in U$,
3.  $a \lhd V$ whenever $a \lhd U$ and $x \lhd V$ for all $x \in U$,
4.  $a \cap b \lhd U$ whenever $a \lhd U$ or $b \lhd U$,
5.  $a \lhd \{ x \cap y \;|\; x \in U,\; y \in V \}$ whenever $a \lhd U$ and $a \lhd V$,
6.  $a \lhd \{\top\}$,
7.  $\vdash x$ for some $x \in U$ whenever $\vdash a$ and $a \lhd U$, and
8.  $a \lhd U$ whenever $a \lhd U$ if $\vdash a$,

for all $a$, $b$, $U$, and $V$.

We interpret the elements of $S$ as __basic opens__ in the formal space.  We call $\top$ the __[[improper subset|entire space]]__ and $a \cap b$ and the __[[intersection]]__ of $a$ and $b$.  We say that $a$ is __covered__ by $U$ or that $U$ is a __[[cover]]__ of $a$ if $a \lhd U$.  We say that $a$ is __positive__ or __[[inhabited subset|inhabited]]__ if $\vdash a$.  (For a [[topological space]] equipped with a strict [[topological base]] $S$, taking these intepretations literally does in fact define a formal space; see the Examples.)

Some immediate points to notice:

*  If we drop (1), then the hypothesis of (1) defines an [[equivalence relation]] on $S$ which is a [[congruence]] for $\top$, $\cap$, $\lhd$, and $\vdash$, so that we may simply pass to the [[quotient set]].
*  The predicate $\vdash$ is uniquely definable in an impredicative treatment; we can prove that $a$ is [[positive element|positive]] if and only if every cover of $a$ is inhabited.
*  We can prove that $(S,\cap,\top)$ is a bounded [[semilattice]]; if (as the notation suggests) we interpret this as a [[meet]]-semilattice, then $a \leq b$ if and only if $a \lhd \{b\}$.


## Examples

Let $X$ be a [[topological space]], and let $S$ be the collection of [[open subsets]] of $X$.  Let $\top$ be $X$ itself, and let $a \cap b$ be the literal intersection of $a$ and $b$ for $a, b \in S$.  Let $a \lhd U$ if and only $U$ is literally an [[open cover]] of $a$, and let $\vdash a$ if and only if $a$ is inhabited.  Then $(S,\top,\cap,\lhd,\vdash)$ is a formal topology.

The above example is impredicative (since the collection of open subsets is generally large), but now let $S$ be a [[base for the topology]] of $X$ which is strict in the sense that it is closed under finitary [[intersection]].  Let the other definitions be as before.  Then $(S,\top,\cap,\lhd,\vdash)$ is a formal topology.

More generally, let $B$ be a [[subbase]] for the topology of $X$, and let $S$ be the [[free monoid]] on $B$, that is the set of [[finite lists]] of elements of $B$ (so this example is not strictly finitist), modulo the [[equivalence relation]] by which two lists are identified if their [[intersections]] are equal.  Let $\top$ be the [[empty list]], let $a \cap b$ be the [[concatenation]] of $a$ and $b$, let $a \lhd U$ if the intersection of $a$ is contained in the [[union]] of the intersections of the elements of $U$, and let $\vdash a$ if the intersection of $a$ is inhabited.  Then $(S,\top,\cap,\lhd,\vdash)$ is a formal topology.

Let $X$ be an [[accessible locale]], and let $S$ be a [[(0,1)-site|site]] (with a [[top element]]) that generates $X$.  Let $\top$ and $\cap$ be as in the semilattice structure on the site $S$, and let $a \lhd U$ if $U$ contains a basic cover of $a$.  Then we get a formal topology, defining $\vdash$ in the unique way.

The last example is not predicative, and this is in part *why* one studies formal topologies instead of sites, if one wishes to be strictly predicative.  (It still needs to be motivated that we want $\vdash$ at all.)


## References

*  [[Givoanni Sambin]], _Some points in formal topology_, [pdf](http://www.math.unipd.it/~sambin/txt/SP.pdf)


[[!redirects formal topology]]
[[!redirects formal topologies]]
[[!redirects formal space]]
[[!redirects formal spaces]]
