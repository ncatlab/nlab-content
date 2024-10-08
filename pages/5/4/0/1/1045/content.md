
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea##

The _Yoneda extension_ of a [[functor]] $F : C \to D$ is a universal [[extension]] ([[Kan extension]]) along the [[Yoneda embedding]] $Y \colon C \to [C^{op},Set]$ of its [[domain]] category to a functor
$$
  \tilde F \colon [C^{op}, Set] \to D
  \,.
$$

The Yoneda extension exhibits the [[presheaf]] category $PSh(C)$ as the [[free cocompletion]] of $C$.


##Definition##

For $C$ a [[small category]] and $F \colon C \to D$ a [[functor]], its **Yoneda extension**

$$
  \tilde F \;\colon\; [C^{op},Set] \to D
$$

is the left [[Kan extension]]  $Lan_Y F \;\colon\; [C^{op}, Set] \to D$ of $F$ along the [[Yoneda embedding]] $Y$:

$$
  \tilde F \;\coloneqq\; Lan_Y F
  \,.
$$

### Remarks ###

Often it is of interest to Yoneda extend not $F \;\colon\; C \to D$ 
itself, but the composition $Y \circ F \;\colon\; C \to [D^{op}, Set]$ to get a functor entirely between presheaf categories

$$
  \hat F \;\coloneqq\; \tilde{Y \circ F} 
  \;\colon\; 
  [C^{op},Set] \to [D^{op}, Set]
  \,.
$$

This is in fact a [[left adjoint]] to the restriction functor $F^\ast \;\colon \; [D^{op}, Set] \to [C^{op}, Set]$ which maps $H \mapsto H \circ F$.  This is relevant, for instance, to [[restriction and extension of sheaves]].

### Formula ###

Recalling the general formula for the left [[Kan extension]] of a functor $F \;\colon\; C \to D$ through a functor $p : C  \to C'$ 

$$
  (Lan_p F)(c') \simeq \colim_{(p(c) \to c') \in (p,c')} F(c)
$$

one finds for the Yoneda extension the formula

$$
  \begin{aligned}
    \tilde F (A) 
    & \;\coloneqq\; (Lan_Y F)(A) 
    \\
    & \simeq
    \colim_{(Y(U) \to A) \in (Y,A) } F(U)
  \end{aligned}
  \,.
$$

(Recall the notation for the [[comma category]] $(Y,A) \;\coloneqq\; (Y, const_A)$ whose objects are pairs $(U \in C, (Y(U) \to A) \in [C^{op}, Set] )$.

For the full extension $\hat F : [C^{op}, Set] \to [D^{op}, Set]$ this yields

$$
  \begin{aligned}
    \hat F(A)(V)
    &=
    (\colim_{(Y(U) \to A) \in (Y,A) } F(U))(V)
    \\
    &\simeq
    \colim_{(Y(U) \to A) \in (Y,A) } F(U)(V)    
    \\
    &\simeq
    \colim_{(Y(U) \to A) \in (Y,A) } Hom_{D}(V,F(U))    
  \end{aligned}
  \,.
$$

Here the first step is from above, the second uses that colimits in presheaf categories are computed objectwise and the last one is again using the [[Yoneda lemma]].


## Properties ##

* The restriction of the Yoneda extension to $C$ coincides with the original functor:
$
  \tilde F \circ Y \simeq F
$.

* The Yoneda extension commutes with small colimits in $C$, i.e. for $\alpha : A \to C$ a [[diagram]], we have $\tilde F (colim (Y \circ \alpha)) \simeq colim F \circ \alpha$ .

* Moreover, $\tilde F$ is defined up to [[isomorphism]] by these two properties.

## Generalizations ##

* [[(infinity,1)-Yoneda extension]] 
