
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential-graded objects
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

A [[differential graded algebra]] over some [[ground field]] (or [[ground ring]]) is called __semi-free__ if the [[underlying]] [[graded algebra]] is free: if after forgetting the [[differential]], it is [[isomorphism|isomorphic]] as a graded algebra to a (polynomial) [[tensor algebra]] over the [[ground field]] ([[ground ring]]) of some ([[super vector space|super]])[[graded vector space]] (or graded [[module]], or [[bimodule]] if the [[ground ring]] is not [[commutative ring|commutative]] -- in this generality see [Roiter 1980 p 296](#Roiter80)).

A [[differential graded-commutative algebra]] is __semifree__ (or semi-free) if the underlying graded-commutative algebra is free: if after forgetting the differential, it is isomorphic as a graded-commutative algebra to a [[Grassmann algebra]] of some [[graded vector space]] . 


Sometimes semi-free DGAs are called _quasi-free_, but this clashes with the terminology about formal smoothness of noncommutative algebras, i.e. quasi-free algebras in the sense of Cuntz and Quillen (and with extensions to homological smootheness of dg-algebras by Kontsevich). 

## Properties


### Relation to Lie $\infty$-algebroids 

One may identify semifree [[differential graded algebras]] with [[Chevalley-Eilenberg algebras]] of ([[finite type|degreewise finite dimensional]]) [[L-infinity algebroids]] ([Sc08](#Sc08), [SSS12](#SSS12)), generalizing a corresponding statement for [[L-infinity algebras]] (see [there](L-infinity-algebra#ReformulationInTermsOfSemifreeDGAlgebra)).

At least when the algebra in degree $0$ is of the form $C^\infty(X)$ for some space $X$, which then is the space of objects of the [[Lie infinity-algebroid]]. But if it is a more general algebra in degree $0$ one can think of a suitably generalized $L_\infty$-algebroid, for instance with a noncommutative space of objects. This generalizes the step from [[Lie algebroids]] to [[Lie-Rinehart pairs]].


### Roiter's theorem 

The main theorem of [Roiter 1980](#Roiter80)
says that semi-free differential graded algebras are in bijective correspondence with [[corings]] with a [[grouplike element]]:

to an $A$-coring $(C,\Delta, A)$ with a grouplike element $g$ associate its [[Amitsur complex]] with underlying graded module $T_A(\Omega^1 A)=\oplus_{n=0}^\infty (\Omega^1 A)^{\otimes_A n}$ where $\Omega^1=ker\,\epsilon$
and differential linearly extending the formulas $d a = g a - a g$ for $a\in A$ and 
$$
d c = g\otimes c + (-1)^n c\otimes g +\sum_{i=1}^n (-1)^i c_1\otimes\ldots\otimes c_{i-1}\otimes\Delta(c_i)\otimes c_{i+1}\otimes\ldots\otimes c_n
$$
for $c=c_1\otimes_A\ldots\otimes_A c_n\in (ker\,\epsilon)^{\otimes_A n}$; 

conversely, to a semi-free dga $\Omega^\bullet A$ one associates the $A$-coring $A g\oplus\Omega^1 A$ where $g$ isa new group-like indeterminate; this is by definition a direct sum of left $A$-modules with a right $A$-module structure given by
$$
(a g +\omega)a' \coloneqq a a' g + a d a'+\omega a'.
$$
In other words, we want the commutator $[g,a']=d\omega'$.
We obtain an $A$-bimodule. The coproduct on $Ag\oplus\Omega^1 A$ is $\Delta(a g)=a g\otimes g$ and $\Delta(\omega)=
g\otimes\omega+\omega\otimes g- d\omega$.
The two operations are mutual inverses (see [lectures](http://www.newton.ac.uk/programmes/NCG/seminars/080411301.pdf) by Brzezinski or the arxiv version [math/0608170](http://arxiv.org/abs/math/0608170)).

Moreover [[connection for coring|flat connections]] for a semi-free dga are in $1$-$1$ correspondence with the comodules over the corresponding coring with a group-like element.




## Related concepts

* [[Sullivan algebra]]

* [[L-infinity algebra]], [[super L-infinity algebra]], "[[FDA]]"

## References

Roiter's theorem:

* {#Roiter80} A. V. Roiter: _Matrix problems and representations of BOCS's_, in Lec. Notes. Math. **831** (1980) 288-324 &lbrack;[doi:10.1007/BFb0089782](https://doi.org/10.1007/BFb0089782)&rbrack;


In relation to [[L-infinity algebroids]] (and specifically of [[L-infinity algebras]], see [there](L-infinity-algebra#ReformulationInTermsOfSemifreeDGAlgebra)):

* {#Sc08} [[Urs Schreiber]]: *On $\infty$-Lie* (2008) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schreiber/action.pdf), [[Schreiber-InfinityLie.pdf:file]]&rbrack;

* {#SSS12} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]] Section A.1 of: _[[schreiber:Twisted Differential String and Fivebrane Structures]]_, Communications in Mathematical Physics **315** 1 (2012) 169-213 &lbrack;[arXiv:0910.4001](http://arxiv.org/abs/0910.4001), [doi:10.1007/s00220-012-1510-3](https://link.springer.com/article/10.1007/s00220-012-1510-3)&rbrack;
 



[[!redirects semifree dgas]]
[[!redirects semi-free dga]]
[[!redirects semi-free dgas]]
[[!redirects semi-free differential graded algebra]]
[[!redirects semi-free differential graded algebras]]
[[!redirects semifree differential graded algebra]]
[[!redirects semifree differential graded algebras]]

[[!redirects quasifree dgas]]
[[!redirects quasi-free dga]]
[[!redirects quasi-free dgas]]
[[!redirects quasi-free differential graded algebra]]
[[!redirects quasi-free differential graded algebras]]
[[!redirects quasifree differential graded algebra]]
[[!redirects quasifree differential graded algebras]]

[[!redirects semifree dg-algebra]]
[[!redirects semifree dg-algebras]]

[[!redirects semifree dgc-algebra]]
[[!redirects semifree dgc-algebras]]

[[!redirects semi-free dg-algebra]]
[[!redirects semi-free dg-algebras]]

[[!redirects semi-free dgc-algebra]]
[[!redirects semi-free dgc-algebras]]


[[!redirects semifree differential graded-commutative algebra]]
[[!redirects semifree differential graded-commutative algebras]]


