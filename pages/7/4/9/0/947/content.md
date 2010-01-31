The __complement__ of a [[subset]] $S$ of a set $X$ is the set
$$
\tilde{S} = \{ a: X \;|\; a \notin S \}
.$$
(Besides $\tilde{S}$, there are many other notations, such as $X - S$, $\bar{S}$, $\neg{S}$, and so forth.)

Notice that $S \cap \tilde{S} = \empty$, while $S \cup \tilde{S} = X$ by the principle of [[excluded middle]].  

The __complement__ of an element $S$ of a [[lattice]] is (if it exists) the unique element $\tilde{S}$ such that $S \wedge \tilde{S} = \bot$ and $S \vee \tilde{S} = \top$.  Such complements always exist in a [[Boolean algebra]].

More generally, the __pseudocomplement__ of an element $S$ of a [[Heyting algebra]] is given by $\tilde{S} = S \Rightarrow \bot$.  This satisfies $S \wedge \tilde{S} = \bot$ but not $S \vee \tilde{S} = \top$ in general.  This case includes the complement of a subset even in [[constructive mathematics]].

In another direction, the __complement__ of a [[complemented subobject]] $S$ of an object $X$ in a [[coherent category]] is the unique subobject $\tilde{S}$ such that $S \cap \tilde{S}$ is the [[initial object]] and $S \cup \tilde{S} = X$.

The complement of a [[truth value]] (seen as a subset of the [[point]]) is called its _[[negation]]_.


[[!redirects complement]]
[[!redirects complements]]
[[!redirects complementation]]

[[!redirects pseudocomplement]]
[[!redirects pseudocomplements]]
