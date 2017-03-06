
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Frobenius monad_ is a _[[monad]]_ which as a [[monoid]] in [[endofunctors]] is a [[Frobenius monoid]].

## Examples

The monad induced from an [[ambidextrous adjunction]] is Frobenius. The converse is also true: 

+-- {: .num_prop} 
###### Proposition 
If $M$ is a Frobenius monad on a category $C$, then the usual free-forgetful adjunction $F \dashv U: Alg_M \to C$ is an ambidextrous adjunction whose associated Frobenius monad is isomorphic to $M$. 
=-- 

+-- {: .proof} 
###### Proof 
In general, if a monad $M$ admits a [[right adjoint]] $K$, then $K$ carries a comonad structure [[mate]]d to the monad structure of $M$, and there is an adjoint equivalence $Alg_M \simeq CoAlg_K$ (considered as categories over $C$, via the usual forgetful functors). If $M$ is Frobenius, then $M \dashv M$ and the comonad structure mated to the monad is indeed the given comonad structure of $M$ (a proof is given [here](https://ncatlab.org/nlab/show/Frobenius+algebra#general)). Hence the left adjoint to the forgetful functor $Alg_M \to C$ may be identified with the right adjoint of the forgetful functor $CoAlg_M \to C$. 
=-- 

## Related concepts

* [[Wirthmüller context]]

* [[infinitesimal cohesion]]

## References

* [[Ross Street]], _Frobenius monads and pseudomonoids_, J. Math. Phys. 45.(2004) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.91.2686))


[[!redirects Frobenius monads]]