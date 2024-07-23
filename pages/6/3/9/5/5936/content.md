
## Idea

The __prime spectrum of a ring__  (associative, but not necessarily commutative or unital) is the set of [[prime ideal]]s of the ring; thus it generalizes the (underlying topological space of) [[spectrum of a commutative ring]]. For noncommutative rings s (and noncommutative [[C-star-algebras]]) however sometimes spectra of [[primitive ideal]]s are more interesting. This entry should eventually be more about the noncommutative case.


## Commutative case

See more at [[spectrum of a commutative ring]].

The prime spectrum of a commutative unital ring extends to a contravariant functor $Spec : CRing\to Set$. 

The prime spectrum $Spec R$ of a commutative unital ring $R$ has a natural Zariski topology $\tau_{Zar}$,  given by the basis of open sets $D_f = Spec R[f^{-1}]\subset Spec R$ where $R\ni f\neq 0$. The prime spectrum considered as a topological space is  also called __Zariski spectrum__. A ring map $h:R\to S$ induces a continuous map $Spec h: Spec S \to Spec R$, so there is a  contravariant functor $Spec : CRing\to Top$.

The correspondence $D_f\mapsto R[f^{-1}]$ for all $f\neq 0$ extends to a unique sheaf $\mathcal{O}=\mathcal{O}_{Spec R}$ of commutative local rings on the Zariski topology on $Spec R$. The ringed space $(Spec R,\tau_{Zar},\mathcal{O})$ so constructed is also called the prime spectrum of the commutative ring $R$. An __affine scheme__ as a locally ringed space is any ringed space which is isomorphic to the prime spectrum of a commutative ring. 

Any morphism of commutative rings $h:R\to S$ also induces the comorphism of structure sheaves on spectra, hence a morphism in locally ringed spaces. This way one obtains a contravariant functor $Spec : CRing\to lRingedSpace$ which is fully faithful (and its essential image is the strictly full subcategory whose objects are affine schemes).

## Related concepts

* [[prime spectrum of a monoidal stable (∞,1)-category]]

* [[Stone spectrum]]

* [[Gelfand spectrum]]

* [[Gelfand duality]]

## Literature

### Noncommutative case

* [[P. M. Cohn]], _Skew fields of fractions, and the prime spectrum of a general ring_, In: Lectures on Rings and Modules. Springer Lecture Notes in Mathematics __246__. [doi](https://doi.org/10.1007/BFb0059563)
* [[Fred van Oystaeyen]], Prime spectra in non-commutative algebra, 
* [[Anthony Joseph]], _A preparation theorem for the prime spectrum of a semisimple Lie algebra_, J. Algebra __48__:2 (1977) 241--289 <a href="https://doi.org/10.1016/0021-8693(77)90306-4">doi</a>

### Spectra of quantum algebras

* [[Anthony Joseph]], _Quantum groups and their primitive ideals_, Springer (1995)

* [[Milen Yakimov]], _Spectra and catenarity of quantum Schubert cells_, Glasgow Mathematical Journal, 55(A), 169--194 (2013) [doi](https://doi.org/10.1017/S0017089513000578)

* Jason Bell,, Karel Casteels, [[Stéphane Launois]], _Primitive ideals in quantum Schubert cells: Dimension of the strata_, Forum Mathematicum 26(3), 703--721 (2014)[doi:10.1515/forum-2011-0155](https://doi.org/10.1515/forum-2011-0155)

* [[S. Launois]], T. H. Lenagan, L. Rigal, _Prime ideals in the quantum grassmannian_, Sel. math., New ser. 13, 697 (2008) [doi](https://doi.org/10.1007/s00029-008-0054-z)
* Thomas H. Lenagan, Milen T. Yakimov, _Prime factors of quantum Schubert cell algebras and clusters for quantum Richardson varieties_, Journal für die reine und angewandte Mathematik (Crelles Journal) [doi](https://doi.org/10.1515/crelle-2016-0046)
* [[S. Launois]], T. H. Lenagan, B. M. Nolan, _Total positivity is a quantum phenomenon: the Grassmannian case_, Memoirs of the Amer. Math. Soc. _1448_ (2023) 123 p.


[[!redirects prime spectra]]
[[!redirects prime spectrum of a ring]]
