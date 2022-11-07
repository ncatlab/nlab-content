
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

+-- {: .num_prop #FrobMonadsHaveAmbidextrousEMAdjunctions} 
###### Proposition 
If $M$ is a Frobenius monad on a category $C$, then the usual [[free-forgetful adjunction]] $F \dashv U \colon Alg_M \to C$ on its [[Eilenberg-Moore category]] is an ambidextrous adjunction whose associated Frobenius monad is isomorphic to $M$. 

=-- 

+-- {: .proof} 
###### Proof 
In general, if a monad $M$ admits a [[right adjoint]] $K$, then $K$ carries a [[comonad]] structure [[mate]]d to the monad structure of $M$, and there is an [[adjoint equivalence]] $Alg_M \simeq CoAlg_K$ between their [[Eilenberg-Moore categories]] (considered as categories over $C$, via the usual [[forgetful functors]]). If $M$ is Frobenius, then $M \dashv M$ and the comonad structure mated to the monad is indeed the given comonad structure of $M$ (a proof is given [here](Frobenius+algebra#general)). Hence the [[left adjoint]] $C \to Alg_M$ to the forgetful functor may be identified with the [[right adjoint]] $C \to CoAlg_M$ of the forgetful functor, each being unique (up to isomorphism) lifts of $M \colon C \to C$ through the forgetful functors. 
=-- 


## Related concepts

* [[Wirthmüller context]]

* [[infinitesimal cohesion]]

## References

* [[Ross Street]], *Frobenius monads and pseudomonoids*, J. Math. Phys. **45** 3930 (2004) &lbrack;[doi:10.1063/1.1788852](https://doi.org/10.1063/1.1788852)&rbrack;


[[!redirects Frobenius monads]]