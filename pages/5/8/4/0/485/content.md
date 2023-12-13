
> The term **exact category** has several different meanings.  This page is about exact categories *in the sense of [Barr 1971](#Barr71)*, also called "Barr-exact categories" or "effective regular categories."  This is distinct from the notion of *[[Quillen exact category]]*.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Regular and Exact categories
+-- {: .hide}
[[!include regular and exact categories - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 


## Definition ##

An **exact category** (in the sense of [Barr 1971](#Barr71)) is a [[regular category]] in which every [[congruence]] is a [[kernel pair]] (that is, every [[internalization|internal]] [[equivalence relation]] is _[[effective epimorphism|effective]]_).  These are also called **effective regular categories**.

\begin{remark}
See *[[familial regularity and exactness]]* for a generalization of exactness and its relationship to [[extensive category|extensivity]].
\end{remark}

## Properties

\begin{remark}
If $R\hookrightarrow X\times X$ is a congruence which is the kernel pair of $f:X \to Y$, then if $f = m \circ p$ is the [[image factorization]] of $f$, one can show that $p$ is a [[coequalizer]] of $R$.  Therefore, congruences have [[quotient object|quotient]]s in an exact category.  

However, not _every_ parallel pair of morphisms need have a coequalizer, and there are also regular categories having all coequalizers which are not exact.
\end{remark}


\begin{remark}
The [[codomain fibration]] of an exact category is a [[stack]] ([[2-sheaf]]) for its [[regular category|regular topology]].  However, being exact is not a necessary condition for this to hold in a regular category; all that is required is that if $R\rightrightarrows A$ is a kernel pair, then so is $f^*R \rightrightarrows B$ for any $f\colon B\to A$.
\end{remark}

## Examples ##

* Any [[topos]] is an exact category.

* Any [[regular category]] with [[van Kampen colimit|van Kampen]] [[quotients]] of [[congruences]] is exact. See at [[van Kampen colimit]] for a proof.

* Any category which is [[monad|monadic]] over a power of [[Set]] is exact. A proof may be found [here](/nlab/show/colimits+in+categories+of+algebras#exact). 

* Any [[abelian category]] is exact. In fact an abelian category is precisely an exact [[additive category]]. 

* If $C$ is exact and $T$ is a [[Lawvere theory]], then the category $Mod(T, C)$ of $T$-models in $C$ is also exact. See Theorem 5.11 of Barr's [Exact Categories](#Barr). 

* Any [[slice]] or [[co-slice]] of an exact category is also exact. (Source: [Borceux and Bourn](http://www.springer.com/us/book/9781402019616), Appendix A.) 

* One can construct, for any regular category $C$, a "free" exact category $C_{ex/reg}$ on $C$ by adjoining formal quotient objects for congruences.  One way to define $C_{ex/reg}$ is as the (locally discrete) [[2-category]] whose objects are congruences in $C$ and whose morphisms are [[anafunctor|anafunctors]].  If $C$ is already exact, then $C_{ex/reg}$ is equivalent to $C$.  See [[regular and exact completions]].

* Similarly, one can construct the "free" exact category $C_{ex/lex}$ on any category $C$ with finite limits, or even with [[weak limit|weak finite limits]].  The exact categories of the form $C_{ex/lex}$ for a category $C$ with weak finite limits are exactly those which have [[projective object|enough (regular) projectives]]; in this case the projective objects are the retracts of objects of $C$ (Carboni-Vitale 1998).  See [[regular and exact completions]].

## Related concepts

* [[exact 2-category]]

* [[Puppe exact category]]

* [[Barr embedding theorem]]

* [[regular category]]

* [[exact functor]]

## References

* {#BarrGrilletvonOsdool} [[Michael Barr]],  [[Pierre Grillet]], [[Donovan van Osdol]], *Exact Categories and Categories of Sheaves*,  Lec. Notes in Math. **236**, Springer (1971) &lbrack;[doi:10.1007/BFb0058579](https://link.springer.com/book/10.1007/BFb0058579)&rbrack;


* {#Barr71}  [[Michael Barr]], _Exact categories_, in: *Exact categories and categories of sheaves*, Springer Lec. Notes in Math. __236__ (1971) 1-120 &lbrack;[doi:10.1007/BFb0058580](http://dx.doi.org/10.1007/BFb0058580), [pdf](https://www.math.mcgill.ca/barr/papers/exact.pdf), [[Barr-ExactCategories.pdf:file]]&rbrack;  

* [[Aurelio Carboni]], [[Enrico Vitale]], _Regular and exact completions_, _JPAA_ 125, 1998.


* [[Francis Borceux]], [[Dominique Bourn]], *[[Borceux-Bourn|Mal'cev, protomodular, homological and semi-abelian categories]]*

[[!redirects exact categories]]

[[!redirects Barr-exact category]]
[[!redirects Barr-exact categories]]

[[!redirects Barr exact category]]
[[!redirects Barr exact categories]]

[[!redirects effective regular category]]
[[!redirects effective regular categories]]

[[!redirects Barr-exact]]


