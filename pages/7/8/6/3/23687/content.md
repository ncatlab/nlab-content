[[!redirects coherent dagger 2-posets]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

## Contents ##
* table of contents
{:toc}

## Idea ##

A coherent dagger 2-poset is a dagger 2-poset whose [[category of maps]] is a [[coherent category]].

## Definition ##

A **coherent dagger 2-poset** is a [[dagger 2-poset]] $C$ such that 

* There is an object $0 \in Ob(C)$ such that for each object $A \in Ob(C)$, there is a [[monic map in a dagger 2-poset|monic map]] $i_{0,A} \in Hom(0,A)$ such that for each object $B \in Ob(C)$ with a monic map $i_{B,A} \in Hom(B,A)$, there is a monic map $i_{0,B} \in Hom(0,B)$ such that $i_{B,A} \circ i_{0,B} = i_{0,A}$. 

* For each object $A \in Ob(C)$, $B \in Ob(C)$, $E \in Ob(C)$ with monic maps $i_{B,A} \in Hom(B,A)$, $i_{E,A} \in Hom(E,A)$, there is an object $B \cup E \in Ob(C)$ with monic maps $i_{B \cup E,A} \in Hom(B \cup E,A)$, $i_{B,B \cup E} \in Hom(B,B \cup E)$, $i_{E,B \cup E} \in Hom(E,B \cup E)$, such that $i_{B \cap E,A} \circ i_{B,B \cap E} = i_{B,A}$ and $i_{B \cap E,A} \circ i_{E,B \cap E} = i_{E,A}$,and for every object $D \in Ob(C)$ with monic maps $i_{D,A} \in Hom(D,A)$ $i_{B,D} \in Hom(B,D)$, $i_{E,D} \in Hom(E,D)$ such that $i_{D,A} \circ i_{B,D} = i_{B,A}$ and $i_{D,A} \circ i_{E,D} = i_{E,A}$, there is a monic map $i_{B \cup E,D} \in Hom(B \cup E,D)$ such that $i_{D,A} \circ i_{B \cup E,D} = i_{B \cup E,A}$

* For each object $A \in Ob(C)$, $B \in Ob(C)$, $E \in Ob(C)$ with monic maps $i_{B,A} \in Hom(B,A)$, $i_{E,A} \in Hom(E,A)$, there is an object $B \cap E \in Ob(C)$ with monic maps $i_{B \cap E,A} \in Hom(B \cap E,A)$, $i_{B \cap E,B} \in Hom(B \cap E,B)$, $i_{B \cap E,E} \in Hom(B \cap E,E)$, such that $i_{B,A} \circ i_{B \cap E,B} = i_{B \cap E,A}$ and $i_{E,A} \circ i_{B \cap E,E} = i_{B \cap E,A}$, and for every object $D \in Ob(C)$ with monic maps $i_{D,A} \in Hom(D,A)$ $i_{D,B} \in Hom(D,B)$, $i_{D,E} \in Hom(D,E)$ such that $i_{B,A} \circ i_{D,B} = i_{D,A}$ and $i_{E,A} \circ i_{D,E} = i_{D,A}$, there is a monic map $i_{D,B \cap E} \in Hom(D,B \cap E)$ such that $i_{B \cap E,A} \circ i_{D,B \cap E} = i_{D,A}$. 

* For each object $A \in Ob(C)$, $B \in Ob(C)$, $D \in Ob(C)$, $E \in Ob(C)$ with monic maps $i_{B,A} \in Hom(B,A)$, $i_{D,A} \in Hom(D,A)$, $i_{E,A} \in Hom(E,A)$, there is a [[unitary isomorphism]] 
$$j_{B,C,E} \in E \cap (B \cup C) \cong^\dagger (E \cap B) \cup (E \cap C)$$

## Properties ##

* For each object $A \in Ob(C)$, the identity function $1_A \in Hom(A,A)$ is a monic map, and for each object $B \in Ob(C)$ with a monic map $i_{B,A} \in Hom(B,A)$, $1_A \circ i_{B,A} = i_{B,A}$. 

* The [[isomorphism classes]] of monic maps is a [[distributive lattice]]. Since every monic map is a map, the [[category of maps]] is a [[coherent category]]. 

## Examples ##

The dagger 2-poset [[Rel]] of [[sets]] and [[relations]] is a coherent dagger 2-poset. 

## See also ##

* [[dagger 2-poset]]
* [[coherent dagger 2-poset]] 
* [[geometric dagger 2-poset]]
* [[Heyting dagger 2-poset]]
* [[Boolean dagger 2-poset]]
* [[elementarily topical dagger 2-poset]]