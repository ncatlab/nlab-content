**Warning: This page is tentative and may contain errors.**

## Idea ##

Given a [[finite category|locally finite]] [[partially ordered set]] $C$, its _Hasse diagram_ encodes the minimal amount of information necessary to reproduce the ordering relation.

## Definition ##

A **Hasse diagram** $H$ is a [[directed graph]] whose edges satisfy the [[covering relation]].

+-- {: .query}
I don\'t understand that sentence as phrased; I think that you mean that the adjacency relation equals the covering relation?  (Of course, maybe I rewrote [[covering relation]] badly; Wikipedia\'s article on covering relations wasn\'t very clear.  But it didn\'t seem to be a relation the way that you wrote it.)  ---Toby
=--

There is a [[forgetful functor]]

$$U: Ord \to Hasse,$$

where $Ord$ is the category of [[preordered sets]] and $Hasse$ is the category of Hasse diagrams, that forgets composite morphisms.

The corresponding [[free functor]]

$$F:Hasse\to Ord$$

allows us to identify a Hasse diagram with each proset.

## References ##

* See also [[Hasse n-graph]]
* [Wikipedia](http://en.wikipedia.org/wiki/Hasse_diagram)