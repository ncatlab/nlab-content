## Idea

In addition to the usual [[distributive laws]] between a [[monad]] and a monad (in a bicategory) there are many other combinations between monad and [[comonad]], comonad and [[endofunctor]], [[action of a monoidal category]] and a monad and so on.

Suppose $V$ is any [[symmetric monoidal category]] with [[coequalizers]] preserved by the tensor product, for example $V$ is the category of $k$-[[modules]] where $k$ is a [[commutative ring]]. Then for any $k$-algebra $A$, endofunctors $A\otimes -$ and $-\otimes A$ are monads on $V$; similarly if $C$ is a $k$-[[comodule|coalgebra]], then endofunctors $C\otimes -$ and $-\otimes C$ are comonads on $V$.

## Definition
A **left entwining structure** is a morphism
$\phi:A\otimes C\to C\otimes A$ in $V$ satisfying four coherence axioms so that $\phi\otimes -$ is (after postcomposing by the [[associator]]) a mixed [[distributive law]] $A\otimes(C\otimes -)\to C\otimes(A\otimes -)$. 

This amounts to ensuring $C\otimes -$ lifts to a comonad on $A\otimes -$-modules (which are the same as _left_ $A$-modules) or, equivalently, that $A\otimes -$ lifts to a monad on $C\otimes -$-comodules.

A **right entwining structure** is a morphism $\psi:C\otimes A\to A\otimes C$ such that $-\otimes\psi$ defines a [[distributive law]] ensuring a lift of the comonad $-\otimes C$ to $-\otimes A$-modules, that is _right_ $A$-modules.
Entwining structures in the monoidal category of endofunctors are the usual distributive laws.

In category of vector spaces (and $k$-modules for $k$ being a commutative ring) (right) entwining structure was introduced by [Brzeziński and Majid 1998](#BrzezinskiMajid1998) in the context of the study of [[noncommutative principal bundles]], not being aware at the time of the mixed distributive laws in category theory ([Van Osdol, 1973](#vanOsdol73)). Namely, they noticed that some examples of noncommutative principal bundles do not have a bialgebra as a structure "group", but a coalgebra together with an entwining.  Entwinings organize into a [[bicategory]]. Every entwining
induces a coring (as observed by Takeuchi; in [Škoda 2008](#Škoda2008) this correspondence is extended to a 2-functor).
To every entwining structure one associates the corresponding category of [[entwined module]]s.

## Literature

* {#BrzezinskiMajid1998} [[T. Brzeziński]], [[S. Majid]], _Coalgebra bundles_, Comm. Math. Phys.  191  (1998),  no. 2, 467--492 [arXiv version](https://arxiv.org/abs/q-alg/9602022) 
*  [[Gabriella Böhm]], _Internal bialgebroids, entwining structures and corings_, Algebraic structures and their representations, 207-226, Contemp. Math., 376, Amer. Math. Soc., Providence, RI, 2005, arXiv:[math/0311244](https://arxiv.org/abs/math/0311244)
* {#vanOsdol73} [[Donovan van Osdol]], *Bicohomology Theory*, Trans. Amer. Math. Soc. **183** (1973) 449--476 [jstor:1996479](https://www.jstor.org/stable/1996479)&rbrack;
* {#Škoda2008} [[Zoran Škoda]], _Bicategory of entwinings_, [arXiv:0805.4611](https://arxiv.org/abs/0805.4611)
* B. Mesablishvili, _Entwining structures in monoidal categories_, J. Algebra __319__:6 (2008) 2496--2517 [doi](http://dx.doi.org/10.1016/j.jalgebra.2007.08.030)
* Bachuki Mesablishvili, Robert Wisbauer, _Galois functors and entwining structures_, J. Algebra __324__:3 (2010) 464--506 [doi](https://doi.org/10.1016/j.jalgebra.2010.04.004)

[[!redirects entwining]]
[[!redirects entwinings]]
[[!redirects entwining structures]]