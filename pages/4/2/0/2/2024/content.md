
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Overt spaces
* table of contents
{: toc}

## Idea

An _overt_ space is a space (of a sort studied in [[topology]]) that satisfies a condition [[de Morgan duality|logically dual]] to that satisfied by a *[[compact space]]*.  An overt space is also called _open_ (in French, there is only one word, 'ouvert') or _locally positive_.


## Motivation

Notice (see [here](closed-projection+characterization+of+compactness#StillOtherCleverConstructions)) that a [[topological space]] $X$ is _compact_ if and only if, for every other space $Y$ and any open subspace $U$ of $X \times Y$, the subspace
$$ \forall_X U = \{ b\colon Y \;|\; \forall\; a\colon X,\; (a, b) \in U \} $$
is open in $Y$.

Dually, a space is _overt_ if and only if, for every other space $Y$ and any open subspace $U$ of $X \times Y$, the subspace
$$ \exists_X U = \{ b\colon Y \;|\; \exists\; a\colon X,\; (a, b) \in U \} $$
is open in $Y$.  (Note that the duality here is only in the logical connectives, not within the category of spaces.)

Of course, *every* topological space satisfies this condition; $\exists_X U$ is the [[union]] over $a$ of the open subspaces $\{ b \;|\; (a,b) \in U \}$.  However, the condition is not trivial in some frameworks, such as [[constructive mathematics|constructive]] [[locale]] theory, [[formal topology]], and [[Abstract Stone Duality]].


## Definition

To remove it from dependence on points, we write the definition like this:

A [[space]] (topological space, locale, etc) $X$ is __overt__ (or __open__) if, given any space $Y$ and any [[open subspace]] $U$ of the [[product space]] $X \times Y$, there exists an open $\exists_X U$ in $Y$ that satisfies the [[universal property]] of [[existential quantification]]:
$$ \exists_X U \subseteq V \;\Leftrightarrow\; U \subseteq X \times V $$
for every open $V$ in $Y$.

Note that, since we quantify over all spaces $Y$ and opens $U\subseteq X\times Y$ in this definition, whether a given space is overt may depend on precisely what 'space' and 'open' mean (even if $X$ is an example for both meanings).  For example, if $X$ is a set with the [[discrete topology]], then it is always overt if 'space' means 'topological space' or 'locale' with the usual meaning of 'open'.  On the other hand, if 'space' means simply 'set', but 'open' refers to the synthetic notion induced by a [[dominance]], then overtness of $X$ is a nontrivial condition (and in fact, if all sets are overt in this sense then the dominance is trivial).


## Overt locales

In the case of [[locales]], it is sufficient to require the above definition only for the case $Y \coloneqq 1$ the [[point]] (unlike the "dual" case of compactness).  In this case, when the map $\exists_X\colon Op(X) \to Op(1) = TV$ (the set or class of [[truth values]]) exists, it is a [[positivity predicate]] on $Op(X)$.  The behavior of this predicate depends on the foundational assumptions:

*  In [[classical mathematics]], it always exists; thus classically every locale is overt.

*  In impredicative [[constructive mathematics]] (such as the [[internal logic]] of a [[topos]]), the positivity predicate can be defined, but it may not satisfy the requisite univeral property of [[adjunction|adjointness]].  Thus, constructively, not every locale is overt.  However, even constructively, every [[topological locale]] is overt (so a [[sober space]] is overt regardless of whether it is viewed as a topological space or as a locale).

*  In constructive [[predicative mathematics]], a positivity predicate cannot be defined and so must be given as a structure on (predicative data that generate) the locale, as is done with a [[formal topology]].  Once this structure is assumed, one can then ask whether a formal topology is overt, i.e. whether the axiomatic positivity predicate satisfies the requisite adjointness.

In impredicative constructive mathematics, [[overt locales]] can be characterized by the *positive covering lemma*: $X$ is overt iff every open $U\in O(X)$ can be covered by positive opens, and iff every covering of an open $U$ can be refined to a covering by positive elements.


## Examples

* At least in impredicative constructive mathematics, the [[topological locale|locale induced by a topological space]] is overt. An open subspace $U$ is positive if and only if it is inhabited.

* At least in impredicative constructive mathematics, the [[spectrum of a commutative ring]] $A$ (defined as the locale whose frame is the frame of radical ideals) is overt if and only if any element of $A$ is nilpotent or not nilpotent.


## Remarks

As compact spaces go with [[proper maps]], so overt spaces go with [[open maps]].  Indeed, $X$ is compact if and only if the unique map $X \to pt$ to the [[point]] is proper, while $X$ is overt if and only if the unique map $X \to pt$ is open.  Similarly, if $X\to pt$ is instead [[closed map|closed]], then $X$ is [[covert space|covert]].

Note that overtness is expressed only in terms of a [[left adjoint]], whereas open maps of locales must additionally satisfy a [[Frobenius reciprocity]] condition.  In the case of locale maps to the point, this latter condition is automatic.

An overt space may also be called **locally $(-1)$-connected**, since this condition is the [[(0,1)-topos]]-theoretic version of the notion of [[locally connected topos]] and [[locally n-connected (n,1)-topos]].  A similar thing happens for higher local connectivity involving the Frobenius reciprocity condition, which must be imposed on general [[geometric morphisms]] to make them locally $n$-connected, but is automatic for morphisms to the point.


## In synthetic topology

In [[synthetic topology]], we interpret 'space' to mean simply 'set' (or [[type]], i.e. the basic objects of our foundational system).  If the notion of 'open' is specified by a [[dominance]], then there is an induced nontrivial notion of "overt set", defined essentially as above.  For instance, the [[Rosolini dominance]] is the smallest dominance such that $\mathbb{N}$ is overt, whereas if all sets are overt then the dominance is trivial.

On the other hand, if by 'open' we mean an open subset [[Penon open|in the sense of Penon]], then all sets are overt.


## References

The notion of an open [[locale]] was originally introduced by Joyal and Tierney (and developed by Johnstone in [[Stone Spaces]]):

* [[Andre Joyal]], [[Myles Tierney]], _An extension of the Galois theory of Grothendieck_,  Mem. Amer. Math. Soc. 51 (1984), no. 309, vii+71 pp. 

The term "overt" is due to [[Paul Taylor]].  For example, it appears in:

* [[Paul Taylor]], _A lambda calculus for real analysis_, Journal of Logic and Analysis 2(5), pp.1-115, 2010. ([web](http://www.paultaylor.eu/ASD/lamcra/))

Some of the history is described in the introduction to:

* [[Bas Spitters]], _Locatedness and Overt Sublocales_, Annals of Pure and Applied Logic, 162:1, October 2010, Pages 36&#8211;54. ([arxiv](http://arxiv.org/abs/math/0703561))


[[!redirects overt space]]
[[!redirects overt spaces]]
[[!redirects overt]]
[[!redirects overtness]]

[[!redirects open space]]
[[!redirects open spaces]]

[[!redirects locally positive space]]
[[!redirects locally positive spaces]]
[[!redirects locally positive]]
[[!redirects local positivity]]

[[!redirects locally (-1)-connected space]]
[[!redirects locally (-1)-connected spaces]]
