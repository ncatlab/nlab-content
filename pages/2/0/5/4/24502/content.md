[[!redirects recursion schemes]]

#Contents#
* table of contents
{:toc}

## Idea

It is a well-known fact in [[computability]] that it is not possible to write a decision procedure that tells whether another program is terminating or not. This fact is known as the [[halting theorem]].

For this reason most [[functional programming]] languages are endowed with an unrestricted [[fixed-point operator]] at all [[types]], which simplifies the implementation of the language, but allows the user to write functions that are not-well defined mathematically. 

Inspired by [[category theory]], a _recursion scheme_ is a structured [[recursion]] operator that ensures that the definitions of [[recursive]] functions are well-defined. 

For example, 

1. A [[catamorphism]] (a.k.a. a fold) is the unique $F$-algebra homomorphism from an [[initial algebra]] for the functor $F$.

2. An [[anamorphism]] (a.k.a.  unfold) is the unique $G$-coalgebra homomorphism into the [[final coalgebra]] for the functor $G$.

3. An [[hylomorphism]] corresponds to the idea of a recursive coalgebra or [[well-founded coalgebra]]. In words, a recursive $F$-coalgebra $(c, X)$ has a unique mapping $f : X \to Y$ into any other $F$-algebra $(Y, a)$ such that $f = a \circ F(f) \circ c$.

A hylomorphism gives a simple example of an opportunity for optimization: an anamorphism builds up a tree structure and a catamorphism consumes it, so if this hylomorphism structure is recognized in the program, then an implementation need not build the intermediate tree, and so the [[computational complexity|space usage]] of the program can be reduced.

## Recursion Schemes via Adjunctions

Catamorphisms and their variants are basic and rather restricted forms of recursion, i.e. where the recursive call is called on smaller input. 

Many other patterns of recursion exist that are equally well-defined, but they cannot be expressed *directly* in terms of catamorphisms. However, most recursion schemes are adjoint folds ([Hinze, Wu and Gibbons, 2013](#HinzeWG13)), i.e. every complex recursion scheme can be reduced to a basic one via an adjunction. Moreover,  *every* recursion scheme is an instance of a conjugate hylomorphism ([Hinze, Wu and Gibbons, 2015](#HinzeWG15)) .

A comprehensive list of recursion schemes can be found in [Yang and Wu, 2022](#YangW22)

## References

* Erik Meijer, Maarten M. Fokkinga, Ross Paterson, _Functional Programming with Bananas, Lenses, Envelopes and Barbed Wire_, FPCA 1991, ([doi](https://doi.org/10.1007/3540543961_7))

* {#HinzeWG13} Ralf Hinze, Nicolas Wu and Jeremy Gibbons, _Unifying structured recursion schemes, ACM SIGPLAN International Conference on Functional Programming, ICFP'13, [doi](https://doi.org/10.1145/2500365.2500578)

* {#HinzeW16} Ralf Hinze, Nicolas Wu, _ Unifying structured recursion schemes - An Extended Study, J. Funct. Program., 2016, [doi](https://doi.org/10.1017/S0956796815000258)

* {#HinzeWG15} Ralf Hinze, Nicolas Wu and Jeremy Gibbons, Conjugate Hylomorphisms - Or: The Mother of All Structured Recursion Schemes, Symposium on Principles of Programming Languages, POPL 2015, [doi](https://doi.org/10.1145/2676726.2676989)

* {#YangW22} Zhixuan Yang and Nicolas Wu, Fantastic Morphisms and Where to Find Them - A Guide to Recursion Schemes, Mathematics of Program Construction, MPC 2022, [doi](https://doi.org/10.1007/978-3-031-16912-0_9)

