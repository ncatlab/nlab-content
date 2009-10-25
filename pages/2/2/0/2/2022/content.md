**Warning: This page is tentative and may contain errors.**

## Idea ##

Given a [[finite category|locally finite]] [[partially ordered set]] $C$, its _Hasse diagram_ encodes the minimal amount of information necessary to reproduce the ordering relation.

## Definition ##

A **Hasse diagram** $H$ is a [[directed graph]] such that the [[graph|adjacency relation]] equals the [[covering relation]].

In other words, a Hasse diagram is a directed graph in which for each edge $x\to y$ there is no other path from $x$ to $y$. There are no intermediate edges.

In particular, given a [[proset]] $C$, its Hasse diagram $H(C)$ is obtained by "forgetting all composite morphisms". The proset $C$ may then be recovered as the free poset on that Hasse diagram.

More formally, there is a [[forgetful functor]]

$$U: Ord \to Hasse,$$

where $Ord$ is the category of [[preordered sets]] and $Hasse$ is the category of Hasse diagrams, that forgets composite morphisms.

The corresponding [[free functor]]

$$F:Hasse\to Ord$$

allows us to identify a Hasse diagram with each proset.

## References ##

* See also [[Hasse n-graph]]
* [Wikipedia](http://en.wikipedia.org/wiki/Hasse_diagram)