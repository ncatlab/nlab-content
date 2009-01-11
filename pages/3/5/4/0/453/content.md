A _regular category_ is a [[finitely complete category]] which admits a good notion of [[image]] factorization. A primary _raison d'etre_ behind regular categories $C$ is to have a decently behaved _calculus of [[relation]]s_ in $C$. 

## Definition

A category $C$ is **regular** if 

* It is finitely complete; 

* The [[kernel pair]] $p_1, p_2: e \,\rightrightarrows\, d$ of any $f: d \to c$ admits a [[coequalizer]];  and

* The pullback of a [[regular epimorphism]] along any map is again a regular epi.

The last condition may equivalently be stated as "coequalizers of kernel pairs are stable under pullback".  However, it is not generally true in a regular category that pullbacks preserve all coequalizer _diagrams_.


## Image factorization

To form the image factorization of a map $f: d \to c$, let $q: d \to k$ be the coequalizer of the kernel pair of $f$. Since $f$ coequalizes its kernel pair, there is a unique map $i: k \to c$ such that $f = i q$. It may be shown from the regular category axioms that $i$ is monic and in fact represents the [[image]] of $f$, i.e., the smallest subobject through which $f$ factors.  Moreover, the class of regular epis and monos forms a [[orthogonal factorization system|factorization system]], and therefore the regular epimorphisms coincide with the [[extremal epimorphism]]s.

Conversely, one can show that a finitely complete category in which the extremal epimorphisms and monomorphisms form a factorization system and extremal epis are preserved by pullbacks is necessarily regular, and the extremal and regular epis coincide.


## Examples

* [[Set]] is a regular category. In fact, any [[topos]] is regular. 

* The category of models of any finitary algebraic theory (i.e., [[Lawvere theory]]) $T$ is regular. This applies in particular to the category [[Ab]] of abelian groups. 

* Any [[abelian category]] is regular (and, in fact, [[exact category|exact]].

* If $C$ is regular, then so is $C^D$ for any category $D$.

* From any category $C$ with finite limits, or even [[weak limit|weak finite limits]], one can construct a "free" regular category $C_{reg/lex}$ by adjoining formal images of morphisms in $C$.  The regular categories of the form $C_{reg/lex}$ for some category $C$ with weak finite limits are precisely those which have [[projective object|enough (regular) projectives]] and in which every object admits a monomorphism into a finite product of projectives; in this case the projectives are the retracts of objects of $C$ (Carboni-Vitale 1998).


## Remarks

* If $C$ is regular, then its [[subobject]] preorders $Sub(X)$ (which have finite meets, since $C$ has finite limits) have the property that for any map $f:X\to Y$, the pullback functor $f^*:Sub(Y)\to Sub(X)$ has a left adjoint $\exists_f$, and the [[Beck-Chevalley condition]] is satisfied for any pullback square.

* Every regular category has an [[internal logic]] which is [[regular logic]].

## References

Carboni, A. and Vitale, E. M. Regular and exact completions, _JPAA_ 125, 1998.