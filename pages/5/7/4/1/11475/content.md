## Idea

This notion is a variant of a notion of a compact space (every cover has a finite subcover) and more specifically a special case of [[compact element]] for orders.
However this entry is written in parallel and with a view toward another generalization -- compact elements in [[quantale]]s. 

## Definition

Let $L$ be a [[complete lattice]]. An element $c\in L$ is __compact__ iff any of the following equivalent conditions hold:

(i) for every $S\subset L$, such that $c\leq sup(S)$, there is a finite subset $F\subset S$ such that $c\leq sup(F)$

(ii) for every [[directed set|directed subset]] $S\subset L$ such that $c\leq S$
there is $s\in S$ with $c\leq s$.

## Frames with properties concerning compact elements

A [[frame]] $L$ is __algebraic__ if every element of $L$ is the sup of some set of compact elements. (Cf. also entry [[algebraic lattice]]). 
In that case, one can take the set of all elements below or equal the given element.  The latter definition is accepted also for [[quantale]]s.

$L$ is __coherent__ if it is algebraic and the finite inf of a set of compact elements
is compact. 

__Theorem.__ A frame $L$ is coherent iff $L$ is isomorphic to the frame of ideals in some [[distributive lattice]].

## Literature

A [[quantale]] is __precoherent__ if it is algebraic and binary products of compact elements are compact. Precoherent quantale is __coherent__ if the truth is a compact element. 

* [[Kimmo Rosenthal|K. I. Rosenthal]], _Quantales and their applications_, Longman 1990

* [[Peter Johnstone]], [[Stone spaces]]

[[!redirects coherent frame]]
[[!redirects algebraic frame]]
[[!redirects coherent quantale]]
[[!redirects compact element in a complete lattice]]