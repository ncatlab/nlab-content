
#Contents#

* automatic table of contents goes here
{:toc}

#Definition#

A [[differential graded algebra]] is __semifree__ (or semi-free) if, after forgetting the differential, it is isomorphic as a graded algebra to a tensor (polynomial) algebra of some (super)vector space. 

A differential **graded-commutative** algebra is __semifree__ (or semi-free) if, after forgetting the differential, it is isomorphic as a graded-commutative algebra to a [[Grassmann algebra]] of some [[graded vector space]] . 


# Roiter's theorem #

Roiter's theorem

* A. V. Roiter, _Matrix problems and representations of BOCS's_; in Lec. Notes. Math. 831, 288--324 (1980)

says: semi-free differential graded algebras are in bijective correspondence with [[coring]]s with a [[grouplike element]]:

to an $A$-coring $(C,\Delta, A)$ with a grouplike element $g$ associate its [[Amitsur complex]] with underlying graded module $T_A(\Omega^1 A)=\oplus_{n=0}^\infty (\Omega^1 A)^{\otimes_A n}$ where $\Omega^1=ker\,\epsilon$
and differential linearly extending the formulas $d a = g a - a g$ for $a\in A$ and 
$$
d c = g\otimes c + (-1)^n c\otimes g +\sum_{i=1}^n (-1)^i c_1\otimes\ldots\otimes c_{i-1}\otimes\Delta(c_i)\otimes c_{i+1}\otimes\ldots\otimes c_n
$$
for $c=c_1\otimes_A\ldots\otimes_A c_n\in (ker\,\epsilon)^{\otimes_A n}$; 

conversely, to a semi-free dga $\Omega^\bullet A$ one associates the $A$-coring $A g\oplus\Omega^1 A$ where $g$ isa new group-like indeterminate; this is by definition a direct sum of left $A$-modules with a right $A$-module structure given by
$$
(a g +\omega)a' := a a' g + a d a'+\omega a'.
$$
In other words, we want the commutator $[g,a']=d\omega'$.
We obtain an $A$-bimodule. The coproduct on $Ag\oplus\Omega^1 A$ is $\Delta(a g)=a g\otimes g$ and $\Delta(\omega)=
g\otimes\omega+\omega\otimes g- d\omega$.
The two operations are mutual inverses (see [lectures](http://www.newton.ac.uk/programmes/NCG/seminars/080411301.pdf) by Brzezinski).

Moreover [[connection for coring|flat connections]] for a semi-free dga are in $1$-$1$ correspondence with the comodules over the corresponding coring with a group-like element.

# Relation to Lie $\infty$-algebroids #

One can identify semifree [[differential graded algebra]]s in non-negative degree with Chevalley--Eilenberg algebras of (degreewise finite dimensional) [[Lie infinity-algebroid]]s

At least when the algebra in degree $0$ is of the form $C^\infty(X)$ for some space $X$, which then is the space of objects of the [[Lie infinity-algebroid]]. But if it is a more general algebra in degree $0$ one can think of a suitably generalized $L_\infty$-algebroid, for instance with a noncommutative space of objects. This generalizes the step from [[Lie algebroid]]s to Lie--Rinehart pairs.

# Terminology #

Sometimes semi-free DGAs are called _quasi-free_, but this is in collision with the terminology about formal smoothness of noncommutative algebras, i.e. quasi-free algebras in the sense of Cuntz and Quillen (and with extensions to homological smootheness of dg-algebras by Kontsevich). 

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