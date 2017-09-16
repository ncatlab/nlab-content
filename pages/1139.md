#Definition#

Given a [[site]] $X$ with underlying [[category]] $S_X$ and given a [[presheaf]] $U \in PSh(X)$ with the induced sub-site $j_{U \to X} : X \to U$ 
corresponding to the [[stuff, structure, property|forgetful]] functor 
$j^t_{U \to X} : (Y_{S_X}/U) \to S_X$
from the [[comma category]] $S_U = (Y_{S_X}/U) \to S_X$ underlying the [[site]] $U$ 
(as discussed at [[site]]) the [[right adjoint]] functor

$$
  j^{\ddagger}_{U \to X} : PSh(U) \to PSh(X)
$$

to the [[direct image]] or, in this case, **restriction** functor

$$
  (j_{U \to X})_* : Sh(X) \to Sh(U)
$$

happens to take sheaves to sheaves
(when $U$ is equipped with the canonical induced topology as described at [[site]]):

one calls
$$
  j^{\ddagger}_{U \to X} : Sh(U) \to Sh(X)
$$

the **extension** of sheaves on $U$ to sheaves on $X$.

#Remarks#

Notice the difference to the [[inverse image]] operation
$$
  j^{-1}_{U \to X} : Sh(U) \to Sh(X)
  \,.
$$
