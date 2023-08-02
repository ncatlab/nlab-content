
\tableofcontents

## Idea

In [[classical mathematics]], a [[subsingleton]] could either be defined as 

* a set $S$ such that for all elements $a \in S$ and $b \in S$, $a = b$

* a set $S$ which is either [[empty set|empty]] or a [[singleton]]. 

However, in [[constructive mathematics]], the two notions of subsingleton are no longer the same, because [[excluded middle]] no longer holds. Instead, one usually defines a subsingleton as the first definition, and the second definition then becomes a **decidable subsingleton**. 

Every subsingleton $S$ comes with an injection $i:S \to 1$ into a [[singleton]] $1$, and is thus is a (structural) [[subset]] of $1$. A subsingleton is also decidable in the subset sense: defining the relation $x \in_1 S$ as 
$$x \in_1 S \coloneqq \exists y \in 1.i(x) = y$$
for all elements $x \in 1$, $x \in_1 S$ or $\neg (x \in_1 S)$. 

## Related concepts

* [[decidable proposition]]
* [[decidable subset]]
* [[decidable injection]]
* [[subsingleton]]

[[!redirects decidable subsingleton]]
[[!redirects decidable subsingletons]]