
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _category over an operad_ is the [[horizontal categorification]]
of an [[algebra over an operad|algebra]] over an [[operad]].  It is like an [[enriched category]]
in which the composition operation is not necessarily binary, but 
parameterized by the [[operad]].


## Definition

Given an [[operad]] $O$ in some [[symmetric monoidal category]]
$C$, a **category over the operad** $O$, or **$O$-category** $D$ is

* a set/class/whatever $D_0$, called the set of **objects** of $D$;

* for each pair $x,y \in D_0$ an object $D(x,y) \in C$, called the 
object of **morphisms** from $x$ to $y$ in $D$;

* for each [[natural number]] $n$ and each sequence $x_0, x_1, \cdots, x_n$
of objects of $D_0$ a morphism
$$ comp_{(x_0, \cdots, x_n)} : \left(D(x_0,x_1) \otimes D(x_1,x_2) 
\otimes \cdots \otimes D(x_{n-1},x_n) \right) \otimes O(n) \to D(x_0, x_n)$$
called the **$n$-ary composition** operation;

* such that the composition operations satisfy the obvious
compatibility conditions with the operad composition operation,
directly analogous to those for $O$-algebras.


## Examples

* Let $Associative$ be the ordinary associative operad in [[Set]].
An $Associative$-category is an ordinary [[Set]]-[[enriched category]]
i.e. a [[locally small category]].

* Let $A$ be the ordinary associative operad in vector spaces. An 
$A$-category is a [[Vect]]-[[enriched category]].

* We may regard the operad $A$ as a dg-operad i.e. an operad in 
the category of [[cochain complex]]es. As such, $A$ has a 
resolution, the [[A-infinity-operad]] operad $A_\infty$. An 
$A_\infty$-category is an [[A-infinity-category]] (see there).

* A class of definitions of [[infinity-category|infinity-categories]] is operadic in this sense, or in a generalization thereof. See

  * [[Trimble n-category]]

  * [[Eugenia Cheng]], _Comparing operadic definitions of $n$-category_ ([arXiv](http://arxiv.org/abs/0809.2070))
