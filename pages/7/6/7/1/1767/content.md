#Contents#
* automatic table of contents goes here
{:toc}


## Definition

### General definition in a coring

Given an $A$-[[coring]] $(C,\Delta,\epsilon)$ (a [[comonoid]] in the category of $A$-$A$-[[bimodule]]s for a $k$-[[algebra]] $A$)  (example: any $k$-algebra) a __semi-grouplike__ element in $A$ is any $g\in C$ such that 

$$
  \Delta(g) = g\otimes g
  \,.
$$ 

A __grouplike__ (or group-like) element is a semi-grouplike one such that $\epsilon(g) = 1$. 

### Special case: grouplike elements in coalgebras

Every [[coalgebra]] is special case of a [[coring]].

The grouplike elements in a $k$-[[Hopf algebra]] form a [[group]]. (Can this fact be [[categorification|categorified]] ??)

## Relation to differential graded algebras


For corings with a (sometimes semi-)grouplike element one can define many useful notions which do not exist for general corings.  

For example, given a semi-grouplike element $g$, the [[tensor algebra]] $\Omega C = \oplus_i \Omega^i C$ of the coring $C$, where $\Omega^i C = C\otimes_A \ldots \otimes_A C$ ($i$ times) over $A$ can be equipped with a [[differential]] $d$ of degree $+1$ in a canonical way making it a [[differential graded algebra]]: 

in degree $0$, one defines 

$$
  d a = g a - a g
$$ 

and in higher degree 

$$
  d(c_1\otimes\ldots\otimes c_n) = g\otimes c_1\otimes\ldots\otimes c_n + (-1)^{n+1}c_1\otimes\ldots\otimes c_n\otimes g + \sum_{i=1}^n c_1\otimes\ldots\otimes c_{i-1}\otimes \Delta(c_i)\otimes c_{i+1}\otimes\ldots \otimes c_n\,.
$$

In fact, by a result in

* A. V. Roiter, _Matrix problems and representations of BOCS's_; in Lec. Notes. Math. 831, 288--324 (1980)

[[semi-free differential graded algebras]] are in bijective correspondence with corings with a group-like element. Moreover flat [[connection for coring|connections]] for a semi-free dga are in $1$-$1$ correspondence with the [[comodule]]s over the corresponding coring with a group-like element.

A special case of this construction is when $g = 1\otimes_R 1$ and $C$ is the [[Sweedler coring]] for a $k$-algebra extension $R\to S$. The dga obtained is the classical Amitsur complex $\Omega(S/R)$ for that extension; for this reason the complex $\Omega C = \Omega(C,g)$ above for any coring $C$ and semi-grouplike $g$ is sometimes said to be an _[[Amitsur complex]]_. 

* [[T. Brzeziński]], R. Wisbauer, _Corings and comodules_, London Math. Soc. Lec. Note Series __309__, Cambridge 2003.

* C. Menini, D. &#350;tefan, _Descent theory and Amitsur cohomology of triples_, 
J. Algebra __266__ (2003), no. 1, 261--304. 

* [[T. Brzeziński]], _Flat connections and comodules_, [math.QA/0608170](http://arxiv.org/abs/math/0608170)

* [[T. Brzeziński]], _Galois structures_, Warszawa 2007/8 course, part III, [pdf](http://toknotes.mimuw.edu.pl/sem7/files/Brzezinski_gs.pdf), [ps](http://toknotes.mimuw.edu.pl/sem7/files/Brzezinski_gs.ps)

[[!redirects group-like element]]