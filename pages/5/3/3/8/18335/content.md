> This entry is about the term of "class function" as it is used in set-theoretical contexts. For the notion of the same name in [[algebra]] see at _[[class function]]_.

#Contents#
* table of contents
{:toc}

## Idea

Recall that in [[set theory]] a [[function]] $f$ from a [[set]] $S_1$ to a set $S_2$ may be encoded in terms of a [[relation]] on the [[Cartesian product]] $S_1 \times S_2$ of the two sets, namely the subset $ R \subset S^1 \times S^2$ with $R = \{  (x,y) \vert y = f(x)\}$ (the [[graph]] of the function). 

This concept has an evident generalization to the case where $S_1$ and $S_2$ are allowed to be proper classes. In this case one speaks of _class functions_.

## Definition

A class function is a [[class]] $R$  which is a [[relation]] with the property that if $(x,y)\in R$ and $(x,y')\in R$, then $y=y'$. 

A class function need not be a [[set]].

Class functions are an important concept when formalizing [[category theory]] on [[set theory|set-theoretic]] [[foundations]] without using [[universes]], especially when 

* constructing functors step by step, e.g. by first constructing an assignment between two classes of objects, and then compatibly augmenting this assignment to make it a functor,

* most especially when constructing _functors on [[functor categories]]_, whose classes of objects tend to be proper classes.



## Example in Category Theory

An example is Mac Lane's discussion  [p. 23](#MacLane1998) of the category of all [[classes]] in his chapter on [[Foundations]]. There, the class of [[arrow]]s is defined by writing "its arrows [are] all functions $f\colon C\rightarrow C'$ between classes".

Class functions are the [[morphism]]s in a [[category with class structure]]. 

## Example in Set Theory 

Arguably the prototypical example of an essential use of the concept of class functions in [[set theory]] is [[Easton's theorem]] [Theorem 15.18](#Jech2002).
on the behaviour of the class function $x\mapsto 2^x$ on the class of all cardinals. (In Easton's theorem, the domain of the class function in question is the proper class of all [[regular cardinals]].) 




Often, authors resort to synonyms like [[operation]] or [[assignment]] when writing about proper classes, with [p. 23](#MacLane1998) being a counterexample.


## References

* {#MacLane1998} [[Saunders Mac Lane]]. _[[Categories for the Working Mathematician]]_ Second Edition. Springer (1998)

* {#Jech2002} T. Jech. Set theory. Third Edition. Springer (2002) 