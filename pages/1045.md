#Idea#

The _Yoneda extenion_ of a [[functor]] $F : C \to D$ is extension along the [[Yoneda embedding]] $Y : C \to [C^{op},Set]$ of its domain category to a functor
$$
  \tilde F : [C^{op}, Set] \to D
  \,.
$$


#Definition#

For $C$ a [[small category]] and $F : C \to D$ a [[functor]], its **Yoneda extension**

$$
  \tilde F : [C^{op},Set] \to D
$$

is the left [[Kan extension]]  $Lan_Y F : [C^{op}, Set] \to D$ of $F$ along the [[Yoneda embedding]] $Y$:

$$
  \tilde F := Lan_Y F
  \,.
$$

## Formula ##

Recalling the general formula for the left [[Kan extension]] of a functor $F : C \to D$ through a functor $p : C  \to C'$ 

$$
  (Lan F)(c') \simeq co\lim_{(p(c) \to c') \in (p,c')} F(c)
$$

one finds for the Yoneda extension the formula

$$
  \hat F (A)(U) = ...
$$


# Properties #

* The restriction of the Yoneda extension to $C$ coincides with the original functor:
$
  \tilde F \circ Y \simeq F
$.

* The Yoneda extension commutes with small colimits in $C$ in that for $\alpha : A \to C$ a [[diagram]], we have $\tilde F (\hat colim \alpha) \simeq colim F \circ \alpha$ (where $\hat colim$ is as defined at [[limit]]).

* Moreover, $\tilde F$ is defined up to [[isomorphism]] by these two properties.

