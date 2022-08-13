[[!redirects recursion schemes]]
#Contents#
* table of contents
{:toc}

## Idea

In [[functional programming]], _recursion schemes_ are patterns of definition for [[recursive]] functions. These are formally defined in order to study equational properties of recursive programs and to facilitate automated optimization of recursive programs.

## Examples

By convention these are given names ending in "morphism". For example:

1. A [[catamorphism]] is a fold, i.e., a homomorphism out of an [[initial algebra]].
2. An [[anamorphism]] is an unfold, i.e., a homomorphism into a [[final coalgebra]].
3. A [[hylomorphism]] is a composition of an anamorphism followed by a catamorphism (in a [[algebraically compact category|category where the initial and final algebra coincide]]).

A hylomorphism gives a simple example of an opportunity for optimization: an anamorphism builds up a tree structure and a catamorphism consumes it, so if this hylomorphism structure is recognized in the program, then an implementation need not build the intermediate tree, and so the [[computational complexity|space usage]] of the program can be reduced.

## References

* Erik Meijer, Maarten M. Fokkinga, Ross Paterson, _Functional Programming with Bananas, Lenses, Envelopes and Barbed Wire_, FPCA 1991, ([doi](https://doi.org/10.1007/3540543961_7))