
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

A _Frobenius monad_ &lbrack;[Lawvere 1969](#Lawvere69)&rbrack; is a _[[monad]]_ which as a [[monoid]] in [[endofunctors]] is a [[Frobenius monoid]].

## Examples

The monad [induced](monad#RelationBetweenAdjunctionsAndMonads) from an [[ambidextrous adjunction]] is Frobenius. The converse is also true: 

\begin{prop}
\label{FrobMonadsHaveAmbidextrousEMAdjunctions}
If $M$ is a Frobenius monad on a category $C$, then the usual [[free-forgetful adjunction]] $F \dashv U \colon Alg_M \to C$ on its [[Eilenberg-Moore category]] is an [[ambidextrous adjunction]] whose associated Frobenius monad is isomorphic to $M$. 
\end{prop}
(cf. [Street (2004), Section II](#Street04))

\begin{proof}
In general, if a monad $M$ admits a [[right adjoint]] $K$, then $K$ carries a [[comonad]] [[structure]] [[mate|mated]] to the monad structure of $M$, and there is an [[adjoint equivalence]] $Alg_M \simeq CoAlg_K$ between their [[Eilenberg-Moore categories]] (considered as categories over $C$, via the usual [[forgetful functors]]). If $M$ is Frobenius, then $M \dashv M$ and the comonad structure mated to the monad is indeed the given comonad structure of $M$ (a proof is given at *[[Frobenius algebra]]* (see [there](Frobenius+algebra#general)). Hence the [[left adjoint]] $C \to Alg_M$ to the [[forgetful functor]] may be identified with the [[right adjoint]] $C \to CoAlg_M$ of the forgetful functor, each being unique (up to isomorphism) lifts of $M \colon C \to C$ through the forgetful functors. 
\end{proof}



## Examples 
 {#Examples}

* For $B$ a [[finite set]] and $k$ any [[ground field]], the [[reader monad]] $\bigcirc_B \;\colon\; Vect_k \to Vect_k$ on $k$-[[VectorSpaces]] is Frobenius and [[isomorphism|isomorphic]] to the [[writer monad]] corresponding to the [[Frobenius algebra]] $k^{\oplus^B}$ (see [there](function+monad#QuantumReaderMonadIsSpecialFrobeniusWriterMonad) for details), this reflecting the existence of [[biproducts]] (namely [[direct sums]]) of [[vector spaces]].


## Related concepts

* [[Wirthmüller context]]

* [[infinitesimal cohesion]]

## References

The notion of Frobenius monads appears briefly in

* {#Lawvere69} [[William Lawvere]], pp. 151 of: *Ordinal sums and equational doctrines*, in *[[Seminar on Triples and Categorical Homology Theory]]* LNM **80** (1969) 141-155 &lbrack;[doi:10.1007/BFb0083085](https://doi.org/10.1007/BFb0083085)&rbrack;


The relation of Frobenius monads to [[ambidextrous adjunctions]]:

in [[Cat]]

* {#Street04} [[Ross Street]], *Frobenius monads and pseudomonoids*, J. Math. Phys. **45** 3930 (2004) &lbrack;[doi:10.1063/1.1788852](https://doi.org/10.1063/1.1788852)&rbrack;

and in general [[2-categories]]:

* {#Lauda05} [[Aaron Lauda]], *Frobenius algebras and ambidextrous adjunctions*, Theory and Applications of Categories **16** 4 (2006) 84-122 &lbrack;[arXiv:math/0502550](http://arxiv.org/abs/math/0502550), [tac:16-04](http://www.tac.mta.ca/tac/volumes/16/4/16-04abs.html)&rbrack;

  > (motivated by [[2d TQFT]])

See also:

* F. Castaño Iglesias, [[José Gómez Torrecillas]], C. Nastasescu, _Frobenius functors: applications_, Comm. Alg. __27__ 10  (1998) 4879-4900 &lbrack;[doi:10.1080/00927879908826735](https://doi.org/10.1080/00927879908826735)&rbrack;



[[!redirects Frobenius monads]]