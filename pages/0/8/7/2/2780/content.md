#Contents#

* automatic table of contents goes here
{:toc}

## Idea

On this page, we work work through several of the key examples of **[[colimits]]** in the category [[Set]]. This is part of a bigger project: [[Understanding Constructions in Categories]].

Recall that a colimit, or universal cocone, over a [[diagram]] $F:J\to Set$ is a [[cocone]] $T$ over $J$ such that, given any cocone $T'$, there is a unique [[cone function]] from $T$ to $T'$.

## Initial Object

An [[initial object]] is a universal cocone over the empty diagram. In this section, we demonstrate how this leads us to the statement:

+-- {: .standout}
The empty set $\varnothing$ is the [[initial object]] in $Set$.
=--

To demonstrate, first note that a cocone over an empty diagram is just a set and a corresponding cocone function is just a function. Therefore, we are looking for a "universal set" $\bullet$ such that for an other set $C$, there is a unique function 

$$f:\bullet\to C.$$

The empty set fills the bill because we have the [[empty function]] from $\varnothing$ to $C$ for all $C$.

Therefore the empty set is an initial object in $Set$.

## Binary Coproducts

Binary [[coproducts]] correspond to disjoint unions in $Set$.

**Under Construction**

## Arbitrary Small Coproducts

arbitrary (but small) [[coproducts]]

## Coequalizers
 
[[coequalizers]]

## Pushouts

[[pushouts]]

## Cofibred Products

[[cofibered coproduct|cofibred coproducts]]

[[!redirects Understanding Colimits in Set]]
