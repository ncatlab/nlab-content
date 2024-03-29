Let $\mathcal{P}$ be a [[strictly full subcategory]] of a [[Grothendieck category]] $\mathcal{C}$ and $S$ a set. A __predecomposition theory__ is a function which to each $M$ in $\mathcal{P}$ gives a subset $\Gamma(M)\subset S$ such that 

(i) $\Gamma(M) = 0$ iff $M = 0$

(ii) For any exact sequence

$$ 0\to M' \to M\to M'' \to 0 $$

in $\mathcal{C}$, with $M\in \mathcal{P}$, 
$\Gamma(M')\subset \Gamma(M) \subset \Gamma(M')\cup\Gamma(M'')$.

(iii) If $M = \sum_i M_i$ then $\Gamma(M)=\cup_i \Gamma(M_i)$. 

(iv) If $M'$ is an essential subobject of $M\in Ob(\mathcal{P})$, then $\Gamma(M') = \Gamma(M)$. One often writes, by abuse of notation, $\Gamma : \mathcal{P}\to S$.
For any $M\in\mathcal{P}$, the elements of $\Gamma(M)$ are called $\Gamma$-associates of $M$. 

A class of examples are spectral predecomposition theories.

An object $M\in Ob(\mathcal{P})$ is said to be __$\Gamma$-coirreducible__ 
if $\Gamma(M)$ contains exactly one element. 

A subobject $M'\subset M$ is __$\Gamma$-irreducible__ if
$M'/M$ is $\Gamma$-coirreducible. 

A predecomposition theory $\Gamma:\mathcal{P}\to M$ is caleld a __decomposition theory__ if any subobject $M'$ of an object $M\in\mathcal{P}$ has a $\Gamma$-decomposition, that is the set of subobjects $\{M_i\}_{i\in I}$, $M_i\subset M$ such that 

(D1) $\cap_{i\in I} M_i = M'$

(D2) for each $i$, $M_i$ is a $\Gamma$-irreducible subobject

(D3) $\Gamma(M/M_i) \cap \Gamma(M/M_j) = \emptyset$ if $i\neq j$

(D4) $\Gamma(M_i/M') = \Gamma(M/M')-\Gamma(M/M_i)$

(D5) $\Gamma(M/M') = \cup_i \Gamma(M/M_i)$

Examples include primary decomposition theory, Lesieur-Croisot [[tertiary decomposition theory]], Bourbaki's $\mathcal{P}$-primary decomposition theories...

* Nicolae Popescu, _An introduction to Abelian categories with applications to rings and modules_, Acad. Press 1973
* Joe W. Fisher, Harvey Wolff, _Decomposition theories for abelian categories_, Trans. Amer. Math. Soc. __182__ (1973), 61&#8211;69 [MR327870](http://www.ams.org/mathscinet-getitem?mr=327870) [doi](http://dx.doi.org/10.2307/1996520) 

An earlier axiomatics in terms of pairs of objects is in

* John A. Riley, _Axiomatic primary and tertiary decomposition theory_, Trans. Amer. Math. Soc. 105 (1962), 177-201, [doi](http://dx.doi.org/10.1090/S0002-9947-1962-0141683-4 )
[[!redirects predecomposition theory]]
[[!redirects decomposition theories]]
[[!redirects predecomposition theories]]