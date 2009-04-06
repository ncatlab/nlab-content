#Idea#

Recall that for [[presheaf|presheaves]] with values in categories $A$ that admit small limits and small colimits, $PSh(X, A) = [S_X^{op}, A]$, (so in particular for $A =$  [[Set]]) every functor $f^t : S_Y \to S_X$ induces three functors of presheaf catgeories:

$$
  \array{
    (f^t)_* : PSh(X,A) \to PSh(Y,A) & direct image
    \\
    (f^t)^\dagger : PSh(Y,A) \to PSh(X,A) & left adjoint to direct image
   \\
    (f^t)^\ddagger : PSh(Y,A) \to PSh(X,A) 
   & right adjoint to direct image
  }
  \,.
$$

Recall moreover that for $f : X \to Y$ any [[site|morphism of sites]], the  right adjoint to [[direct image]] followed by [[sheafification]] $\var {{-}}$ is the [[inverse image]] map of sheaves:

$$
  f^{-1} : Sh(Y,A) \to Sh(X,A)
  \,.
$$

Now, it the morphism of sites $f$ happens to be restriction to a sub-site  $f : X \to U$ with $U \in PSh(X,A)$ with $U$ carrying the induced [[Grothendieck topology|topology]], then 

* the direct image is called **restriction** of sheaves;

* the left adjoint takes sheaves to sheaves and is called **extension** of sheaves.


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
whose action may suggestively be denoted
$$
  (j_{U \to X})_* : F \mapsto F|_U
$$

happens to take sheaves to sheaves
(when $U$ is equipped with the canonical induced topology as described at [[site]]):

one calls
$$
  j^{\ddagger}_{U \to X} : Sh(U) \to Sh(X)
$$

the **extension** of sheaves on $U$ to sheaves on $X$.

To summarize notation and terminology:

$$
  \array{
    morphism of sites & 
    j_{U \to X} : X \to U
    \\ 
    underlying functor & 
    j^t_{U \to X} : (Y_{S_X}/U) \to S_X
    \\
    sheaf restriction 
    & 
    (j_{U \to X})_* : Sh(X) \to Sh(U)
    & (= direct image)
    \\
    sheaf extension
    &
    j^{\ddagger}_{U \to X} : Sh(U) \to Sh(X)  
    & (= right adjoint to direct image)
    \\
    sheaf inverse image
    &
    \bar ({-})
    \circ (j^t)^{\dagger}_{U \to X} : Sh(U) \to Sh(X)  
    &
    (= left adjoint to direct image followed by sheafification)
  }
$$




#Remarks#

Notice the difference to the [[inverse image]] operation
$$
  j^{-1}_{U \to X} : Sh(U) \to Sh(X)
  \,.
$$


#References#

For instance section 17.6 of 

* Kashiwara, Schapira, [[Categories and Sheaves]]