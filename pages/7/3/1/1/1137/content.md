#Definition#

Given a [[site|morphism of sites]] $f : X \to Y$ coming from a [[functor]] $f^t : S_Y \to S_X$, the **direct image** operation on [[presheaf|presheaves]] is the functor

$$
  f_* : PSh(X) \to PSh(Y)
$$
$$
  f_* F : S_Y^{op} \stackrel{f^t}{\to} S_X^{op} \stackrel{F}{\to} Set
  \,.
$$

The restriction of this operation to [[sheaf|sheaves]], which respects sheaves, is the **direct image of sheaves**

$$
  f_* : Sh(X) \to Sh(Y)
  \,.
$$

More generally, the right adjoint part of any [[geometric morphism]] is called its **direct image functor**.

#Remarks#

* The [[left adjoint]] to the direct image is the [[inverse image]] functor.

* The [[right adjoint]] to the direct image functor, if it exists, is the [[restriction and extension of sheaves|extension]] operation on (pre)sheaves.
