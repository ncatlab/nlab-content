
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

The notion of *Scott-complete categories* is a [[category theory|category theoretic]] generalization of the notion of *[[Scott domains]]* from [[domain theory]], and hence a model of the [[lambda calculus]]. 

A Scott domain is a [[directed colimit|directed-complete]] [[partial order]] ([[dcpo]]) that is 

* [[algebraic lattice|algebraic]], in that every [[element]] is a [[directed colimit|directed]] [[join]] of [[compact]] elements, and there is a [[bottom]] [[element]];

* consistently complete, i.e., every [[inhabited set|nonempty]] [[subset]] with an [[upper bound]] has a [[least upper bound]].

The suitable notion of [[morphisms]] between Scott domains is that of [[directed colimit|directed]]-[[join]]-[[preserved colimit|preserving]] [[monotone functions]]. These are the same as [[continuous functions]] with respect to the [[Scott topology]]. 

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

## See also

* [[Scott topos]]

## References 

* [[Jiří Adámek]], *A categorical generalization of Scott domains*, Mathematical Structures in Computer Science **7** 5  (1997) 419 - 443 &lbrack;[doi:10.1017/S0960129597002351](https://doi.org/10.1017/S0960129597002351)&rbrack;

[[!redirects Scott-complete categories]]


