
## Idea

The __prime [[spectrum of a ring]]__  (associative, but not necessarily commutative or unital) is the set of [[prime ideal]]s of the ring. For noncommutative rings however sometimes spectra of [[primitive ideal]]s are more interesting. 

The prime spectrum of a commutative unital ring extends to a contravariant functor $Spec : CRing\to Set$. 

The prime spectrum $Spec R$ of a commutative unital ring $R$ has a natural Zariski topology $\tau_{Zar}$,  given by the basis of open sets $D_f = Spec R[f^{-1}]\subset Spec R$ where $R\ni f\neq 0$. The prime spectrum considered as a topological space is  also called __Zariski spectrum__. A ring map $h:R\to S$ induces a continuous map $Spec h: Spec S \to Spec R$, so there is a  contravariant functor $Spec : CRing\to Top$.

The correspondence $D_f\mapsto R[f^{-1}]$ for all $f\neq 0$ extends to a unique sheaf $\mathcal{O}=\mathcal{O}_{Spec R}$ of commutative local rings on the Zariski topology on $Spec R$. The ringed space $(Spec R,\tau_{Zar},\mathcal{O})$ so constructed is also called the prime spectrum of the commutative ring $R$. An __affine scheme__ as a locally ringed space is any ringed space which is isomorphic to the prime spectrum of a commutative ring. 

Any morphism of commutative rings $h:R\to S$ also induces the comorphism of structure sheaves on spectra, hence a morphism in locally ringed spaces. This way one obtains a contravariant functor $Spec : CRing\to lRingedSpace$ which is fully faithful (and its essential image is the strictly full subcategory whose objects are affine schemes).

## Related concepts

* [[prime spectrum of a monoidal stable (∞,1)-category]]

* [[Stone spectrum]]

* [[Gelfand spectrum]]

* [[Gelfand duality]]


[[!redirects Zariski spectrum]]
