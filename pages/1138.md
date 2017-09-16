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

on [[presheaf|presheaves]] is the [[adjoint functor|left adjoint]] to the direct image operation on presheaves, hence the left [[Kan extension]]

$$
  f^{-1} F := Lan_{f^t} F
$$

of a [[presheaf]] $F$ along $f^t$. 

The **inverse image** operation on [[sheaf|sheaves]] is the 
[[adjoint functor|left adjoint]] to the direct image operation on sheaves. This is _not_ simply the left Kan extension of the sheaf regarded as a presheaf, but the Kan extension followed by [[sheafification]] $\bar{(-)} : PSh(X) \to Sh(X)$:

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

See [[restriction and extension of sheaves]].

More generally, the left adjoint part of any [[geometric morphism]] is called its **inverse image functor**.

#Remarks#

* The other adjoint to the [[direct image]], the [[adjoint functor|right adjoint]], is (if it exists) the [[restriction and extension of sheaves|extension]] of sheaves.


#Examples#

The standard example is that where $X$ and $Y$ are [[topological space]]s and $S_X = Op(X)$, $S_Y = Op(Y)$ are their [[category of open subsets|categories of open subsets.]]

A continuous map $f : X \to Y$ induces the obvious functor $f^{-1} : Op(Y) \to Op(X)$, since preimages of open subsets under continuous maps are open. 

Hence presheaves canonically push-forward

$$
  f^{-1}_* : PSh(X) \to PSh(Y)
$$

They do not in the same simple way pull back, since images of open subsets need not be open. The Kan extension  computes the best possible approximation:

The inverse image $(f^{-1})^\dagger : PSh(Y) \to PSh(X)$ sends $F \in PSh(Y)$ to

$$
  f^\dagger F : U \mapsto colim_{(U \to f^{-1}(V)) \in (const_U, f^{-1})} F(V)
  \,.
$$

This approximates the possibly non-open subset $f^{-1}(V)$ by all open subsets $U$ _inside_ it.

On the other hand, the extension

$(f^{-1})^\ddagger : PSh(Y) \to PSh(X)$ sends $F \in PSh(Y)$ to

$$
  f^\dagger F : U \mapsto colim_{(f^{-1}(V) \to U) \in (f^{-1},const_U)} F(V)
  \,.
$$

This approximates the possibly non-open subset $f^{-1}(V)$ by all open subsets $U$  _containing_ it.

