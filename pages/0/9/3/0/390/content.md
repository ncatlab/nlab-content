
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{: toc}


##Definition#

An **orthogonal factorization system** can be defined as a [[weak factorization system]] in which solutions to lifting problems are unique.  It can also be defined more directly as a pair $(E,M)$ of classes of maps in a category $C$ such that

* Every morphism in $C$ factors as an $E$-morphism followed by an $M$-morphism, and
* $E$ is precisely the class of morphisms that are left [[orthogonality|orthogonal]] to every morphism in $M$.
* $M$ is precisely the class of morphisms that are right [[orthogonality|orthogonal]] to every morphism in $E$.

OFS's are traditionally called just **factorization systems**.
See the _[[joyalscatlab:Factorization systems|Catlab]]_ for more of the theory.

An orthogonal factorization system is called **proper** if every morphism in $E$ is an [[epimorphism]] and every morphism in $M$ is a [[monomorphism]].


## Prefactorization systems

For any class $E$ of morphisms in $C$, we write $E^\perp$ for the class of all morphisms that are right orthogonal to every morphism in $E$.  Dually, given $M$ we write ${}^\perp M$ for the class of all morphisms that are  left orthogonal to every morphism in $M$.  The second condition in the definition of an OFS then says that $E= {}^\perp M$ and $M= E^\perp$.

In general, $(-)^\perp$ and ${}^\perp(-)$ form a [[Galois connection]] on the [[poset]] of classes of morphisms in $C$.  A pair $(E,M)$ such that $E= {}^\perp M$ and $M= E^\perp$ is sometimes called a **prefactorization system**.  Note that by generalities about Galois connections, for any class $A$ of maps we have prefactorization systems $({}^\perp(A^\perp),A^\perp)$ and $({}^\perp A, ({}^\perp A)^\perp)$.  We call these *generated* and *cogenerated* by $A$, respectively.

If $C$ is a [[locally presentable category]], then for any *small set* of maps $A$, the prefactorization system $({}^\perp(A^\perp),A^\perp)$ is actually a factorization system.  The argument is by a transfinite construction similar to the [[small object argument]].


## Examples #

Several classical examples of OFS $(E,M)$:

* in any [[topos]], $E$ = class of all epis, $M$ = class of all monos

* more generally, in any [[regular category]], $E$ = class of all [[regular epimorphisms]], $M$ = class of all monos

* (Street) in [[Cat]], $E$ = 0-[[final functors]], $M$ = [[discrete fibration]]s 

* (Street) in $\mathrm{Cat}$,  $M$ = 0-[[initial functors]], $M$ = [[discrete opfibration]]s

* in $\mathrm{Cat}$, $M$ = [[conservative functor]]s, $E$ = left orthogonal of $M$ ("iterated strict localizations" after A. Joyal)

* in the category of small categories where morphisms are functors which are [[exact functor|left exact]] and have [[right adjoint]]s, $E$ = class of all such functors which are also localizations, $M$ = class of all such functors which are also conservative

* if $F\to C$ is a [[fibered category]] in the sense of Grothendieck, then $F$ admits a factorization system $(E,M)$ where $E$ = arrows whose projection to $C$ is invertible, $M$ = cartesian arrows in $F$


* See the _[[joyalscatlab:Factorization systems|Catlab]]_ for more examples. 

[[!redirects orthogonal factorization system]]
[[!redirects orthogonal factorization systems]]
[[!redirects orthogonal factorisation system]]
[[!redirects orthogonal factorisation systems]]
[[!redirects unique factorization system]]
[[!redirects unique factorization systems]]
[[!redirects unique factorisation system]]
[[!redirects unique factorisation systems]]
