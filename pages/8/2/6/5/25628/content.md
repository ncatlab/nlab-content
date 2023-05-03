# Contents
* table of contents
{: toc}

## Idea 

A Scott-complete category is a categorical generalization of the notion of Scott domain from [[domain theory]], and hence a model of the [[lambda calculus]]. 

A Scott domain is a [[directed colimit|directed-complete]] [[partial order]] ([[dcpo]]) that is 

* [[algebraic lattice|algebraic]], in that every element is a directed join of [[compact]] elements, and there is a [[bottom]] element;

* consistently complete, i.e., every nonempty set with an upper bound has a [[least upper bound]].

The suitable notion of morphism between Scott domains is a directed-join-preserving monotone functions. This is the same as a [[continuous function]] with respect to the [[Scott topology]]. 

Scott domains forms a [[cartesian closed category]] that supports the solution of recursive domain equations. 

Scott domains admit a simple description in terms of "information systems", which can help to calculate Scott domains and to cement the computation / information-based intuitions.

## Definition {#Def}

+-- {: .num_defn}
###### Definition

A category is **Scott-complete** if it is

* [[accessible category|finitely accessible]];

* every diagram with a [[cocone]] has a [[colimit]].

=--

Scott-complete categories and [[directed colimit]] preserving functors form a category SCC. 

This category, SCC, is [[cartesian closed]] and supports the solution of recursive domain equations. 

## See also ##

* [[Scott topos]]

## References ##

* [A categorical generalization of Scott domains](https://doi.org/10.1017/S0960129597002351), [[Jiri Adamek]]. Mathematical Structures in Computer Science , Volume 7 , Issue 5 , October 1997 , pp. 419 - 443. 



