
# Overt spaces
* table of contents
{: toc}

## Idea

An _overt_ space is a space that satisfies a condition [[de Morgan duality|logically dual]] to that satisfied by a [[compact space]].  An overt space is also called _open_ (in French, there is only one word, 'ouvert').


## Motivation

Recall that a [[topological space]] $X$ is _compact_ if and only if, for every other space $Y$ and any open subset $U$ of $X \times Y$, the subset
$$ \forall_X U = \{ b : Y \;|\; \forall\; a: X,\; (a, b) \in U \} $$
is open in $Y$.

Dually, a space is _overt_ if and only if, for every other space $Y$ and any open subset $U$ of $X \times Y$, the subset
$$ \exists_X U = \{ b : Y \;|\; \exists\; a: X,\; (a, b) \in U \} $$
is open in $Y$.  (Note that the duality here is only in the logical connectives, not within the category of spaces.)

Of course, *every* topological space satisfies this condition; $\exists_X U$ is the [[union]] over $a$ of the open subsets $\{ b \;|\; (a,b) \in U \}$.  However, the condition is not trivial in some frameworks, such as [[constructive mathematics|constructive]] [[locale]] theory, [[formal topology]], and [[Abstract Stone Duality]].


## Definition

To remove it from dependence on points, we write the definition like this:

A [[space]] (topological space, locale, etc) $X$ is __overt__ if, given any space $Y$ and any open $U$ in $X \times Y$, there exists an open $\exists_X U$ in $Y$ that satisfies the [[universal property]] of existential [[quantification]]:
$$ \exists_X U \subseteq V \;\Leftrightarrow\; U \subseteq X \times V $$
for every open $V$ in $Y$.

Note that, since we quantify over all spaces $Y$, whether a given space is overt may depend on precisely what 'space' means (even if $X$ is an example for both meanings).  I don\'t know any good examples of this, however.

In particular, in the case of [[locales]], it is sufficient to require the above condition for the case $Y=1$ the [[point]] (unlike the "dual" case of compactness, below).  In this case, when the map $\exists_X:Op(X) \to Op(1)$ exists, it is a [[positivity predicate]] on $Op(X)$.  The behavior of this predicate depends on the foundational assumptions:

* In [[classical mathematics]], it always exists; thus classically every locale is overt.

* In impredicative [[constructive mathematics]] (such as the [[internal logic]] of a [[topos]]), the positivity predicate can be defined, but it may not satisfy the requisite property of adjointness.  Thus, constructively, not every locale is overt.  However, even constructively, every [[topological locale]] is overt (so a [[sober space]] is overt regardless of whether it is viewed as a topological space or as a locale).

* In [[predicative mathematics]], a positivity predicate is determined uniquely if it exists, but it cannot be defined and so must be given axiomatically, as is done with a [[formal topology]].  Once this structure is assumed, one can then ask whether a formal topology is overt, i.e. whether the axiomatic positivity predicate satisfies the requisite adjointness.


## Remarks

As compact spaces go with [[proper maps]], so overt spaces go with [[open maps]].  Indeed, $X$ is compact if and only if the unique map $X \to pt$ to the [[point]] is proper, while $X$ is overt if and only if the unique map $X \to pt$ is open.

Note that overtness is expressed only in terms of a left adjoint, whereas open maps of locales must additionally satisfy a [[Frobenius reciprocity]] condition.  In the case of locale maps to the point, this latter condition is automatic.

An overt space may also be called **locally (-1)-connected**, since this condition is the "(0,1)-topos theoretic" version of the notion of [[locally connected topos]] and [[locally n-connected (n,1)-topos]].  A similar thing happens for higher local connectivity involving the Frobenius reciprocity condition, which must be imposed on general [[geometric morphisms]] to make them locally $n$-connected, but is automatic for morphisms to the point.


[[!redirects overt space]]
[[!redirects open space]]
[[!redirects overt locale]]
[[!redirects open locale]]
[[!redirects overt spaces]]
[[!redirects open spaces]]
[[!redirects overt locales]]
[[!redirects open locales]]
[[!redirects locally (-1)-connected space]]
[[!redirects locally (-1)-connected spaces]]
[[!redirects locally (-1)-connected locale]]
[[!redirects locally (-1)-connected locales]]
