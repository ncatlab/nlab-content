
\tableofcontents

## Idea

In [[classical mathematics]], a *[[subsingleton]]* could either be defined as 

* a set $S$ such that for all elements $a \in S$ and $b \in S$, $a = b$

* a set $S$ which is either [[empty set|empty]] or a [[singleton]]. 

However, in [[constructive mathematics]], the two notions of subsingleton above are no longer the same, because the [[axiom of excluded middle]] no longer holds true. Instead, one usually defines a subsingleton as the first definition, and the second definition is then referred to as about *[[decidable subsingletons]]*. 

Similarly, in [[classical mathematics]], an *[[injection]]* between two sets $A$ and $B$ is then a function $f:A \to B$ such that for all elements $b \in B$, the [[preimage]] or [[fiber]] of $f$ at $b$ is a subsingleton. However, in [[constructive mathematics]], there are two notions of [[injections]], resulting from the two notions of subsingletons: 

* An [[injection]] between two sets $A$ and $B$ is a function $f:A \to B$ such that for all elements $b \in B$, the [[preimage]] or [[fiber]] of $f$ at $b$ is a [[subsingleton]].  

* A **decidable injection** between two sets $A$ and $B$ is a function $f:A \to B$ such that for all elements $b \in B$, the [[preimage]] or [[fiber]] of $f$ at $b$ is a [[decidable subsingleton]]; i.e. either [[empty set|empty]] or a [[singleton]]. 

## Set of decidable injections

Suppose the [[set theory]] has [[function sets]] $B^A$. Then one could define the set of decidable injections from $A$ to $B$ as the set 

$$\mathrm{Inj}_d(A, B) \coloneqq \{f \in B^A \vert \forall b \in B.(\exists!a \in A.a \in f^*(b)) \vee (\neg \exists a \in A.a \in f^*(b))\}$$

where $f^*(b)$ is the [[preimage]] or [[fiber]] of $f$ at $b$. 

## Related concepts

* [[decidable subset]]
* [[decidable subsingleton]]
* [[injection]]
* [[binomial set]]

[[!redirects decidable injection]]
[[!redirects decidable injections]]

[[!redirects set of decidable injection]]
[[!redirects set of decidable injections]]