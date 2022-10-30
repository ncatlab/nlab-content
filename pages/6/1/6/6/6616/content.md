
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _symplectic $\infty$-groupoid_ is a [[smooth ∞-groupoid]] equipped with a [[symplectic form]], or, more generally, with an [[n-plectic form]].

This is the generalization of the notion of [[symplectic manifold]] to [[higher symplectic geometry]]. It is also the image under [[Lie integration]] of the notion of [[symplectic Lie n-algebroid|symplectic L-∞ algebroid]], which is also a higher analog of symplectic manifolds, but in an [[infinitesimal object|infinitesimal]] way.

Notice that every symplectic manifold is in particular a [[Poisson manifold]] and that the structure of a Poisson manifold is equivalently encoded in the corresponding [[Poisson Lie algebroid]]. A _[[symplectic groupoid]]_ is the [[Lie integration]] of such a Poisson Lie algebroid. Therefore, strictly speaking, already "ordinary" symplectic geometry secretly involves [[Lie groupoid]]s. This insight is exploited in the refinement of [[geometric quantization of symplectic groupoids]]. 


## By Lie integration of symplectic $L_\infty$-algebroids

The [[symplectic form]] $\omega$ on a [[symplectic Lie n-algebroid]] $\mathfrak{a}$ is Lie theoretically an [[invariant polynomial]]. Therefore by [[infinity-Chern-Weil theory]] it induces a moprhism

$$
  \exp(\omega) 
    :  
  \tau_n\exp(\mathfrak{a}) 
    \to 
  \mathbf{\flat}_{dR} \mathbf{B}^{n+2} \mathbb{R}
$$

from the [[Lie integration]] of $\mathfrak{a}$ to the de Rham coefficient object: this is an $(n+2)$-form on a [[smooth ∞-groupoid]] (as discussed at [smooth ∞-groupoid -- structures -- de Rham cohomology](http://ncatlab.org/nlab/show/smooth+infinity-groupoid+--+structures#StrucDeRham)) and hence equips $\exp(\mathfrak{a})$ with the structure of a symplectic $\infty$-groupoid. 

We spell this out in some special cases.



### $n = 1$ -- Symplectic groupoids from Poisson Lie algebroids


Let $\mathfrak{P}$ be the [[Poisson Lie algebroid]] corresponding to a [[Poisson manifold]] that comes from a [[symplectic manifold]] $(X,\omega)$.

The [[symplectic groupoid]] associated to this is (by the discussion there) supposed to be the [[fundamental groupoid]] 
$\Pi_1(X)$ of $X$ equipped on its space of morphisms with the differential form $p_1^* \omega - p_2^* \omega$, where $p_1,p_2$ are the two endpoint projections from paths in $X$ to $X$.

We demonstrate in the following how this is indeed the result of applying the [[∞-Chern-Weil homomorphism]] to this situation.

For simplicity we shall start with the simple situation where $(X,\omega)$ has a global [[Darboux coordinate chart]] $\{x^i\}$. Write $\{\omega_{i j}\}$ for the components of the [[symplectic form]] in these coordinates, and $\{\omega^{i j}\}$ for the components of the [[inverse]].


Then the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{P})$ is generated from $\{x^i\}$ in degree 0 and $\{\partial_i\}$ in degree 1, with differential given by

$$
  d_{CE} x^i = - \omega^{i j} \partial_j
$$

$$
  d_{CE} \partial_i = \frac{\partial \pi^{j k}}{\partial x^i} \partial_j \wedge \partial_k = 0
  \,.
$$

The differential in the corresponding [[Weil algebra]] is hence

$$
  d_{W} x^i = - \omega^{i j} \partial_j + \mathbf{d}x^i
$$

$$
  d_{W} \partial_i = \mathbf{d} \partial_i
  \,.
$$


By the discussion at [[Poisson Lie algebroid]], the symplectic [[invariant polynomial]] is

$$
  \mathbf{\omega} = \mathbf{d} x^i \wedge \mathbf{d} \partial_i \in W(\mathfrak{P})
  \,.
$$

Clearly it is useful to introduce a new basis of generators with

$$
  \partial^i := -\omega^{i j} \partial_j
  \,.
$$

In this new basis we have a manifest isomorphism

$$
  CE(\mathfrak{P}) = CE(\mathfrak{T}X)
$$

with the [[Chevalley-Eilenberg algebra]] of the [[tangent Lie algebroid]] of $X$. 

Therefore the [[Lie integration]] of $\mathfrak{P}$ is the [[fundamental groupoid]] of $X$, which, since we have assumed global Darboux oordinates and hence [[contractible]] $X$, is just the [[pair groupoid]]:

$$
  \tau_1 \exp(\mathfrak{P}) = \Pi_1(X) = (X \times X \stackrel{\overset{p_2}{\to}}{\underset{p_1}{\to}} X)
  \,.
$$

It remains to show that the symplectic form on $\mathfrak{P}$ makes this a [[symplectic groupoid]].

Notice that in the new basis the invariant polynomial reads

$$
  \begin{aligned}
    \mathbf{\omega} 
      &= 
     - \omega_{i j} \mathbf{d}x^i \wedge \mathbf{d} \partial^j 
     \\
      & = \mathbf{d}( \omega_{i j} \partial^i \wedge \mathbf{d}x^j)
   \end{aligned}
$$

and that we may regard this as a morphism of $L_\infty$-algebroids

$$
  \mathbf{\omega}
   : 
  \mathfrak{T}\mathfrak{P} \to \mathfrak{T}b^3 \mathbb{R}
$$

The corresponding [[infinity-Chern-Weil theory|infinity-Chern-Weil homomorphism]] that we need to compute is given by the [[∞-anafunctor]]

$$
  \array{
    \exp(\mathfrak{P})_{diff}
     &\stackrel{\exp(\mathbf{\omega})}{\to}&
    \exp(b \mathbb{R})_{dR}
    &\stackrel{\int_{\Delta^\bullet}}{\to}&
    \mathbf{\flat}_{dR}\mathbf{B}^3 \mathbb{R} 
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{P})
  }
  \,.
$$


Over a test space $U$ in degree 1 an element in $\exp(\mathfrak{P})_{diff}$ is a pair
$(X^i, \eta^i)$

$$
  X^i \in C^\infty(U \times \Delta^1)
$$

$$
  \eta^i \in \Omega^1_{vert}(U \times \Delta^1)
$$

subject to the verticality constraint, which says that along $\Delta^1$ we have

$$
  d_{\Delta^1} X^i + \eta^i_{\Delta^1} = 0
  \,.
$$

The vertical morphism $\exp(\mathfrak{P})_{diff} \to \exp(\mathfrak{P})$ has in fact a [[section]] whose image is given by those pairs for which $\eta^i$ has no leg along $U$. We therefore find the desired form on $\exp(\mathfrak{P})$ by evaluating the top morphism on pairs of this form. 

Such a pair is taken by the top morphism to

$$
  \begin{aligned}
    (X^i, \eta^j) 
     & \mapsto 
   \int_{\Delta^1}
    \omega_{i j} F_{X^i} \wedge F_{\partial^j}
   \\
    & =
  \int_{\Delta^1}
    \omega_{i j} (d_{dR} X^i + \eta^i) \wedge d_{dR} \eta^j
  \in 
  \Omega^3(U)
  \end{aligned}
  \,.
$$

Using the above verticality constraint and the condition that $\eta^i$ has no leg along $U$, this becomes

$$
  \cdots = 
  \int_{\Delta^1}
  \omega_{i j}
    d_U X^i 
  \wedge
    d_U d_{\Delta^1} X^j 
  \,.
$$

By the [[Stokes theorem]] the integration over $\Delta^1$ yields

$$
  \cdots 
    =
  \omega_{i j} d_{dR} x^i \wedge \eta^j|_{0}
   -
  \omega_{i j} d_{dR} x^i \wedge \eta^j|_{1}
  \,.
$$

This completes the proof.

## Related concepts

* [[higher symplectic geometry]]

  * [[symplectic Lie n-algebroid]] 

  * [[symplectic groupoid]]

* [[smooth ∞-groupoid]]


## References

A bit of discussion is in section 4.3 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .


[[!redirects symplectic ∞-groupoid]]
[[!redirects symplectic ∞-groupoids]]
[[!redirects symplectic infinity-groupoids]]