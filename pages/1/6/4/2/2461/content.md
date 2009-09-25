Let $B$ be a $k$-bialgebra and $E$ a right $B$-comodule algebra with coaction $\rho:E\to E\otimes B$. Let $j : E\to E_\mu$ be a biflat affine localization in the sense that it is a homomorphism of rings (affiness), and that the extension of scalars along $j$ is an exact localization functor whose right adjoint is also exact. If $B$ is a Hopf algebra of coordinate functions on an alegbraic $k$-group where $k$-is a field, and $E$ is the coordinate algebra of an affine $k$-variety with regular $G$-action, then we can not restrict the action to an arbitrary open sets, but only to the $G$-invariant open sets. In our case, this would mean that the  coaction does not necessarily extend to the localization $E_\mu$ respecting the algebra structure.  

For this reason, one introduces the class of $\rho$-compatible localizations: a localization of a comodule algebra $(E,\rho)$ is **coaction compatible localization** if the coaction extends to an algebra morphism $E_\mu\to E_\mu\otimes B$ such that the diagram

$$\array{
E&\stackrel{\rho}\to &E\otimes B\\
j \downarrow &&\downarrow j\otimes B\\
E_\mu&\stackrel{\rho_\mu}\to &E_\mu\otimes B
}$$

commmutes. If such an extension exists it is unique. 

The algebra of **localized coinvariants** is the algebra $E_mu^{co B}$ of $\rho_\mu$-[[coinvariants]] in $E_\mu$. It is important to notice that taking coinvariants and localization do not commute: there is no localization
$E^{co B}\to E^{co B}_\mu$ in general. A $B$-comodule algebra which is $\rho$-compatibly may have many new $B$-coinvariants which do not come in any sense as images under some sort of a localization from the $B$-coinvariants of $E$. This localization can be used to get more local information on the noncommutative quotient space for coactions of Hopf algebra. In some cases one can construct a cover of the quotient spaces by affine charts whose coordinate algebras are the algebras of localized coinvariant for varying compatible localizations of the original comodule algebra; this can be further generalized by replacing comodule algebra by a more general object which is also glued from the charts, but this requires consideration of the compatibility at the level of the localization functors and the actions are then globally expressed via an action of a monoidal category (which is still locally induced by a coaction). 

The notion of compatibility of coactions and Ore localizations and the localized coinvariants have been introduced in 1997 when starting working on

* Z. &#352;koda, _Coset spaces for quantum groups_, thesis, Univ. of Wisconsin 2002.
 
This work is outlined in 

* Z. &#352;koda, _Localizations for construction of quantum coset spaces_, in "Noncommutative geometry and Quantum groups", W.Pusz,  P.M. Hajac, eds. Banach Center Publications vol.61, pp. 265--298, Warszawa 2003, [math.QA/0301090](http://arxiv.org/abs/math.QA/0301090).

and generalized in 

* Z. &#352;koda, _Some equivariant constructions in noncommutative algebraic geometry_, Georgian Mathematical Journal 16 (2009), No. 1, 183--202, [arXiv:0811.4770](http://arxiv.org/abs/0811.4770).

* Z. &#352;koda, _Compatibility of (co)actions and localization_,  [arXiv:0902.1398](http://arxiv.org/abs/0902.1398).


