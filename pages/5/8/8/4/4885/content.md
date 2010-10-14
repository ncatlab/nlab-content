
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The _Reidemeister moves_ are local changes to [[knot]] or [[link]] [[knot diagram|diagrams]].  

These moves were given in the book by [Reidemeister](#Reidemeister).


## Definition

We define the Reidemeister moves in terms of link diagrams

The conventions are that part of the diagram is shown with the 'move' indicated, but that outside that, the diagram of the link is unchanged and that no other part of the diagram appears at the crossings that are changed by that move. 


+-- {: .un_remark}
###### Note
In manipulating a link diagram, the changes obtained by elongating part of the diagram, rotating it, deforming the plane, etc., are not counted as changing the structure of the diagram provided they do not change any crossing,and so they may be done without comment.  The 'moves' outlined here do change things locally near crossings.
=--


### First Reidemeister moves

The local configurations (R3)

[[!include Reidemeister move 1 - SVG]]


are interchangable;

### Second Reidemeister move (R2)
The configurations

[[!include Reidemeister move 2 - SVG]]



are interchangeable;

### Third Reidemeister move (R3)
The configurations

[[!include Reidemeister move 3 - SVG]]

are interchangeable.

Often the terminology is used that two link diagrams, $D$ and $D'$ are  _isotopic_ or _isotopic by moves_ if $D$ can be transforemd into $D'$ by some sequence of the three Reidemeister moves, R1, R2 and R3. They are called _regularly isotopic_ if the transformation can be done without using R1.  It is clear that both isotopy and regular isotopy give equivalence relations on link diagrams.

The following theorem is a form of Reidemeister's theorem:

## Properties
##Reidemeister's Theorem
+-- {: .un_theorem}
###### Theorem
Two [[knot diagram]]s correspond to isotopic knots precisely if they can be connected by a sequence of applications of the three Reidemeister moves.
=--
The corresponding statement for [[links]] and link diagram is also true.



Because of this, we can hope to use the Reidemeister moves to verify invariance of a potential [[link invariant]]. For instance, as none of the moves alters the number of components of a link diagram, the number of components is an isotopy invariant (which is not at all surprising!) We can conclude that the [[Hopf link]] and the [[Borromean rings]] are not isotopic. 

A deeper observation is that the [[linking number]] is a link invariant, for which see that entry.

(Other instances of this sort of argument will get put here later on.)


   




## References
One of the original sources is:

* Reidemeister, _Knotentheorie,_ Ergebnisse der Mathematik (1932)
{#Reidemeister}

Many modern texts on Knot Theory contain discussions of the Reidemeister Moves.


[[!redirects Reidemeister move]]
[[!redirects Reidemeister moves]]
