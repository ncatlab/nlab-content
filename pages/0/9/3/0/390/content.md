#Definition#

An **orthogonal factorization system** can be defined as a [[weak factorization system]] in which solutions to lifting problems are unique.  It can also be defined more directly as a pair $(E,M)$ of classes of maps in a category $C$ such that

* Every morphism in $C$ factors as an $E$-morphism followed by an $M$-morphism, and
* Every morphism in $E$ is left [[orthogonality|orthogonal]] to every morphism in $M$.

In particular, if $(E,M)$ is an OFS then classes $E$ and $M$ determine each other.
OFS's are traditionally called just **factorization systems**.  Our use of the adjective "orthogonal" is to avoid the [[red herring principle]] when comparing with [[weak factorization system]]s.

Several classical examples of OFS $(E,M)$:

* in any topos, $E$ = class of all epis, $M$ = class of all monos

* (Street) in $\mathrm{Cat}$, $E$ = 0-final functors, $M$ = [[discrete fibration]]s 

* (Street) in $\mathrm{Cat}$,  $M$ = 0-initial functors, $M$ = [[discrete opfibration]]s

* in $\mathrm{Cat}$, $M$= class of all [[conservative functor]]s, $E$ = left orthogonal of $M$ ("iterated strict localizations" after A. Joyal)

* in the category of small categories where morphisms are functors which are exact and having right adjoint, $E$ = class of all such functors which are also localizations, $M$ = class of all such functors which are also conservative

* if $F\to C$ is a fibered category in the sense of Grothendieck, then $F$ admits a factorization system $(E,M)$ where $E$ = arrows whose projection to $C$ is invertible, $M$ = cartesian arrows in $F$