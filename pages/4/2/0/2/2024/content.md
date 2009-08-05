## Idea

An overt space is a space that satisfies a condition [[de Morgan duality|logically dual]] to that satisfied by a [[compact space]].  An overt space is also called _open_ (in French, there is only one word, 'ouvert').


## Motivation

Recall that a [[topological space]] $X$ is _compact_ if and only if, for every other space $Y$ and any open subset $U$ of $X \times Y$, the subset
$$ \forall_X U = \{ b : Y \;|\; \forall\; a: X,\; (a, b) \in U \} $$
is open in $Y$.

Dually, a space is _overt_ if and only if, for every other space $Y$ and any open subset $U$ of $X \times Y$, the subset
$$ \exists_X U = \{ b : Y \;|\; \exists\; a: X,\; (a, b) \in U \} $$
is open in $Y$.  (Note that the duality here is only in the logical connectives, not within the category of spaces.)

Of course, *every* topological space satisfies this condition; $\exists_X U$ is the [[union]] over $a$ of the open subsets $\{ b \;|\; (a,b) \in U \}$.  However, the condition is not trivial in some frameworks, such as [[locale]] theory and [[Abstract Stone Duality]].


## Definition

To remove it from dependence on points, we write the definition like this:

A space (locale, etc) $X$ is __overt__ if, given any space $Y$ and any open $U$ in $X \times Y$, there exists an open $\exists_X U$ in $Y$ that satisfies the [[universal property]] of existential [[quantification]]:
$$ \exists_X U \subseteq V \;\Leftrightarrow\; U \subseteq X \times V $$
for every open $V$ in $Y$.


## Remarks

As compact spaces go with proper maps, so overt spaces go with open maps.  Indeed, $X$ is compact if and only if the unique map $X \to pt$ to the [[point]] is proper, while $X$ is overt if and only if the unique map $X \to pt$ is open.


[[!redirects overt locale]]
[[!redirects open locale]]