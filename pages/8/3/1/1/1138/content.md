#Definition#

Given a [[site|morphisms of sites]] $f : X \to Y$ coming from a [[functor]] $f^t : S_Y \to S_X$ of the underlying [[category|categories]], the [[direct image]] operation on [[presheaf|presheaves]] and [[sheaf|sheaves]] 
$F \mapsto f_* F$
is just precomposition with $f^t$

$$
  \array{
    S_Y^{op}
    &\stackrel{f_* F}{\to}&
    Set
    \\
    \downarrow^{f^t} & \nearrow_{F}
    \\
    S_X^{op}
  }
  \,.
$$

The **inverse image** operation 

$$
  f^{-1} : PSh(Y) \to PSh(X)
$$

on [[presheaf|presheaves]] is the [[left adjoint]] to the direct image operation on presheaves, hence the left [[Kan extension]]

$$
  f^{-1} F := Lan_{f^t} F
$$

of a [[presheaf]] $F$ along $f^t$. 

The **inverse image** operation on [[sheaf|sheaves]] is the 
[[left adjoint]] to the direct image operation on sheaves. This is _not_ simply the left Kan extension of the sheaf regarded as a presheaf, but the Kan extension followed by [[sheafification]] $\bar{(-)} : PSh(X) \to Sh(X)$:

$$
  f^{-1} : Sh(Y) \to Sh(X)
$$
$$
  f^{-1} : Sh(Y) \hookrightarrow PSh(Y)
  \stackrel{f^{-1}}{\to}
  PSh(X)
  \stackrel{\bar {(-)}}{\to}
  Sh(X)
  \,.
$$

#Remarks#

* The other adjoint to the [[direct image]], the [[right adjoint]], is the [[restriction and extension of sheaves|extension]] of sheaves.