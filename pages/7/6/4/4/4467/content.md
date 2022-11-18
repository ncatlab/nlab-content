
>This entry is about a generalized notion of [[topology]]. For the notion of _formal space_ in the sense of [[rational homotopy theory]], see [[formal dg-algebra]].


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Formal topology
* table of contents
{: toc}

## Idea

Formal topology is a programme for doing [[topology]] in a [[finite mathematics|finite]], [[predicative mathematics|predicative]], and [[constructive mathematics|constructive]] fashion.

It is a kind of [[pointless topology]]; in the context of [[classical mathematics]], it reproduces the theory of [[locales]] rather than [[topological spaces]] (although of course one can recover topological spaces from locales).

The basic definitions can be motivated by an attempt to study locales entirely through the [[posites]] that generate them.  However, in order to recover all basic topological notions (particularly those associated with *closed* rather than *open* features) predicatively, we need to add a 'positivity' relation to the 'coverage' relation of sites.


## Definitions

A __formal topology__ or __formal space__ is a [[set]] $S$ together with

*  an [[element]] $\top$ of $S$,
*  a [[binary operation]] $\cap$ on $S$,
*  a [[binary relation]] $\lhd$ between elements of $S$ and [[subsets]] of $S$, and
*  a [[unary relation]] $\Diamond$ on $S$,

such that

1.  $a = b$ whenever $a \lhd \{b\}$ and $b \lhd \{a\}$,
2.  $a \lhd U$ whenever $a \in U$,
3.  $a \lhd V$ whenever $a \lhd U$ and $x \lhd V$ for all $x \in U$,
4.  $a \cap b \lhd U$ whenever $a \lhd U$ or $b \lhd U$,
5.  $a \lhd \{ x \cap y \;|\; x \in U,\; y \in V \}$ whenever $a \lhd U$ and $a \lhd V$,
6.  $a \lhd \{\top\}$,
7.  $\Diamond x$ for some $x \in U$ whenever $\Diamond a$ and $a \lhd U$, and
8.  $a \lhd U$ whenever $a \lhd U$ if $\Diamond a$,

for all $a$, $b$, $U$, and $V$.

We interpret the elements of $S$ as __basic opens__ in the formal space.  We call $\top$ the __[[improper subset|entire space]]__ and $a \cap b$ the __[[intersection]]__ of $a$ and $b$.  We say that $a$ is __covered__ by $U$ or that $U$ is a __[[cover]]__ of $a$ if $a \lhd U$.  We say that $a$ is __positive__ or __[[inhabited subset|inhabited]]__ if $\Diamond a$.  (For a [[topological space]] equipped with a strict [[topological base]] $S$, taking these intepretations literally does in fact define a formal space; see the Examples.)

Some immediate points to notice:

*  If we drop (1), then the hypothesis of (1) defines an [[equivalence relation]] on $S$ which is a [[congruence]] for $\top$, $\cap$, $\lhd$, and $\Diamond$, so that we may simply pass to the [[quotient set]].  In appropriate foundations, we can even allow $S$ to be a [[preset]] originally, then use (1) as a definition of equality.
*  We can prove that $(S,\cap,\top)$ is a bounded [[semilattice]]; if (as the notation suggests) we interpret this as a [[meet]]-semilattice, then $a \leq b$ if and only if $a \lhd \{b\}$.  Conversely, we could require that $(S,\cap,\top)$ be a semilattice originally, then let (1) say that $a \leq b$ whenever $a \lhd \{b\}$.
*  We can prove that $\Diamond a$ holds iff every cover of $a$ is inhabited and that $\Diamond a$ fails iff $a \lhd \empty$.  Accordingly, this predicate is uniquely definable (in two equivalent ways, one impredicative and one nonconstructive) in a classical treatment; only in a treatment that is both predicative and constructive do we need to include it in the axioms.  See [[positivity predicate]].


## Examples

Let $X$ be a [[topological space]], and let $S$ be the collection of [[open subsets]] of $X$.  Let $\top$ be $X$ itself, and let $a \cap b$ be the literal intersection of $a$ and $b$ for $a, b \in S$.  Let $a \lhd U$ if and only $U$ is literally an [[open cover]] of $a$, and let $\Diamond a$ if and only if $a$ is literally inhabited.  Then $(S,\top,\cap,\lhd,\Diamond)$ is a formal topology.

The above example is impredicative (since the collection of open subsets is generally large), but now let $S$ be a [[base for the topology]] of $X$ which is strict in the sense that it is closed under finitary [[intersection]].  Let the other definitions be as before.  Then $(S,\top,\cap,\lhd,\Diamond)$ is a formal topology.

More generally, let $B$ be a [[subbase]] for the topology of $X$, and let $S$ be the [[free monoid]] on $B$, that is the set of [[finite lists]] of elements of $B$ (so this example is not strictly finitist), modulo the [[equivalence relation]] by which two lists are identified if their [[intersections]] are equal.  Let $\top$ be the [[empty list]], let $a \cap b$ be the [[concatenation]] of $a$ and $b$, let $a \lhd U$ if the intersection of $a$ is contained in the [[union]] of the intersections of the elements of $U$, and let $\Diamond a$ if the intersection of $a$ is inhabited.  Then $(S,\top,\cap,\lhd,\Diamond)$ is a formal topology.

Let $X$ be an [[accessible locale]] generated by a [[posite]] whose underlying [[poset]] $S$ is a (meet)-[[semilattice]].  Let $\top$ and $\cap$ be as in the semilattice structure on $S$, and let $a \lhd U$ if $U$ contains a basic cover (in the posite structure on $S$) of $a$.  Then we get a formal topology, defining $\Diamond$ in the unique way.

The last example is not predicative, and this is in part *why* one studies formal topologies instead of sites, if one wishes to be strictly predicative.  (It still needs to be motivated that we want $\Diamond$ at all.)

## In dependent type theory

In [[dependent type theory]], if one doesn't have a [[type of all propositions]], then one usually cannot define a relation between a type $S$ and the type of all subtypes of $S$, which is necessary for defining the coverage $\lhd$. Instead, one has to use a [[Tarski universe]] to define the type of all locally $U$-small subtypes of $S$, and use that to define a locally $U$-small formal topology on $S$. 

Let $(U, T)$ be a [[Tarski universe]], and let $\mathrm{Prop}_U$ be the type of all propositions in $U$

$$\mathrm{Prop}_U \coloneqq \sum_{A:U} \mathrm{isProp}(T(A))$$

which comes with an [[embedding]] $\mathrm{asType}_U:\mathrm{Prop}_U \hookrightarrow U$. In addition, we define the relation $a \in_S^U A$ for $a:S$ and $A:S \to \mathrm{Prop}_U$ as

$$a \in_S^U A \coloneqq \mathrm{isContr}(T(\mathrm{asType}(A(a)))$$

The singleton subtype function is a function $\{-\}:S \to (S \to \mathrm{Prop}_U)$, such that for all elements $a:S$, $p(a):a \in_S^U \{a\}$, and for all functions $R:S \to (S \to \mathrm{Prop}_U)$ such that for all elements $a:S$, $p_R(a):a \in_S^U R(a)$, the type of functions $(b \in_S^U \{a\}) \to (b \in_S^U R(a))$ is contractible for all $a:A$ and $b:A$. 

Given a [[Tarski universe]] $(U, T)$, a **locally $U$-small formal topology** or **locally $U$-small formal space** is a [[type]] $S$ together with

*  an [[element]] $\top:S$,
*  a [[binary operation]] $\cap:S \times S \to S$,
*  a [[binary relation]] $a \lhd A$ between elements of $S$, $a:S$, and locally $U$-small [[subsets]] of $S$, $A:S \to \mathrm{Prop}_U$, and
*  a [[unary relation]] $\Diamond a$ on $S$,

such that

1. For all elements $a:S$ and $b:S$, the canonical function 
$$\mathrm{idToFormalTop}(a, b):(a =_S b) \to ((a \lhd \{b\}) \times (b \lhd \{a\}))$$
is an [[equivalence of types]]. 
$$\prod_{a:S} \prod_{b:S} \mathrm{isEquiv}(\mathrm{idToFormalTop}(a, b))$$
2. For all elements $a:S$ and subsets $A:S \to \mathrm{Prop}_U$, if $a \in_S^U A$, then $a \lhd A$
$$\prod_{a:S} \prod_{A:S \to \mathrm{Prop}_U} (a \in_S^U A) \to (a \lhd A)$$
3.  For all elements $a:S$ and subsets $A:S \to \mathrm{Prop}_U$ and $B:S \to \mathrm{Prop}_U$, if $a \lhd A$ and for all elements $x:S$, $x \lhd B$ and $x \in_S^U A$, then $a \lhd B$
$$\prod_{a:S} \prod_{A:S \to \mathrm{Prop}_U} \prod_{B:S \to \mathrm{Prop}_U} \left((a \lhd A) \times \prod_{x:S} (x \in_S^U A) \times (x \lhd B)\right) \to (a \lhd B)$$
4.  For all elements $a:S$ and $b:S$ and subsets $A:S \to \mathrm{Prop}_A$, if $a \lhd A$ or $b \lhd A$, then $a \cap b \lhd A$.
$$\prod_{a:S} \prod_{b:S} \prod_{A:S \to \mathrm{Prop}_U} ((a \lhd A) \times (b \lhd A)) \to (a \cap b \lhd A)$$
5.  For all elements $a:S$ and subsets $A:S \to \mathrm{Prop}_U$ and $B:S \to \mathrm{Prop}_U$, if $a \lhd A$ and $a \lhd B$, then
$$a \lhd \sum_{z:S} \prod_{x:S} \prod_{y:S} (x \in_S^U A) \times (y \in_S^U B) \times (z =_S x \cap u)$$
$$\prod_{a:S} \prod_{A:S \to \mathrm{Prop}_U} \prod_{B:S \to \mathrm{Prop}_U} (a \lhd A) \times (a \lhd B) \to \left(a \lhd \sum_{z:S} \prod_{x:S} \prod_{y:S} (x \in_S^U A) \times (y \in_S^U B) \times (z =_S x \cap y)\right)$$
6.  For all elements $a:S$, $a \lhd \{\top\}$,
$$\prod_{a:S} a \lhd \{\top\}$$
7.  For all elements $a:S$ and subsets $A:S \to \mathrm{Prop}_U$, if $\Diamond a$ and $a \lhd A$, there exists an element $x:S$ such that $x \in_S A$ and $\Diamond x$. 
$$\prod_{a:S} \prod_{A:S \to \mathrm{Prop}_U} (\Diamond a) \times (a \lhd A) \to \sum_{x:S} (x \in_S A) \times (\Diamond x)$$
8.  For all elements $a:S$ and subsets $A:S \to \mathrm{Prop}_U$, if $\Diamond a$ implies $a \lhd A$, then $a \lhd A$. 
$$\prod_{a:S} \prod_{A:S \to \mathrm{Prop}_U} (\Diamond a \to a \lhd A) \to (a \lhd A)$$

## References

*  [[Mike Fourman]] and Grayson (1982); _Formal Spaces_.  This is the original development, intended as an application of locale theory to logic.

*  [[Giovanni Sambin]] (1987); _Intuitionistic formal spaces_; [pdf](http://www.math.unipd.it/~sambin/txt/ifs87-97.pdf).
   *  This is the probably the main reference on the subject.
   *  Warning: you can ignore the material about [[foundations]] and [[type theory]], but if you do read any of it, the term 'category' means (roughly) [[proper class]]; this was common in type theory in the 1980s.

*  [[Giovanni Sambin]] (2001); _Some points in formal topology_; [pdf](http://www.math.unipd.it/~sambin/txt/SP.pdf).  This has newer results, alternative formulations, etc.

* {#Palmgren05} [[Erik Palmgren]], _From Intuitionistic to Point-Free Topology: On the Foundation of Homotopy Theory_, Logicism, Intuitionism, and Formalism Volume 341 of the series Synthese Library pp 237-253, 2005 ([pdf](http://www2.math.uu.se/~palmgren/homotopy_rev2.pdf))


[[!redirects formal topology]]
[[!redirects formal topologies]]

[[!redirects formal space]]
[[!redirects formal spaces]]
[[!redirects formal topological space]]
[[!redirects formal topological spaces]]
