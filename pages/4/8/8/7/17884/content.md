

Both [[BV-algebras]] and [[BD-algebras]] have a superficial similarity and are both related to [[BV-BRST formalism]] in [[physics]]. Indeed the "[[BV-operad]]" was named such because its algebras resemble the structure seen on the [[BV-complexes]] in physics. However in the [[formal deformation quantization]] picture of BV-formalism used in [Costello-Gwilliam](#CostelloGwilliam), the quantum BV-complexes crucially are [[BD-algebras]] and _not_ [[BV-algebras]]. On the other hand, if one does not insist on a formal deformation parameter, one may also formalize quantum BV complexes using actual BV-algebras.

This page here means to indicate how all these structures are similar and yet different.

$\,$

Write all [[chain complexes]] in the following with [[differential]] $d$ of degree +1.

Write $E_2$ for the [[little disk operad]] and $E_2^{fr}$ for the [[framed little disk operad]]. The [[chain homology]] of these is the [[BV-operad]] $BV$ and the operad $P_2$ for [[Poisson 2-algebras]], respectively:

$$
  \array{
    BV &\simeq& H_\bullet(E_2^{fr})
    \\
    \uparrow && \uparrow
    \\
    P_2 &\simeq& H_\bullet(E_2)
  }
  \,.
$$


An [[algebra over an operad|algebra over]] these in chain complexes  -- a [[homotopy BV-algebra]] or [[Poisson 2-algebra]], respectively -- is a chain complex $(V^\bullet, d)$ equipped with the following operations of the degree shown:

$$
  \array{
     operation && d && (-,-) & &  \{-,-\} && \Delta
     \\
     degree && +1 && 0 && -1 && +1
  }
  \,,
$$

where the [[BV-operator]] $\Delta$ exists on [[homotopy BV-algebra]]s but not on [[Poisson 2-algebras]], satisfying the relation

$$
  \Delta (a \cdot b) = (\Delta a) \cdot b + (-1)^{\vert a \vert} a \cdot \Delta b - \{a,b\}
  \,. 
$$

If $A$ is a commutative smooth Poincare duality algebra so that its [[Hochschild cohomology]] $HH^\bullet(A)$ is identified by the [[HKR theorem]] with the multi-derivations, then $HH^\bullet(A)$ carries a [[BV-algebra]] structure and under this identification the above [[Gerstenhaber bracket]] $\{-,-\}$ is the [[Schouten bracket]] and the [[BV-operator]] $\Delta_{BV}$ is the image of the [[de Rham differential]] dualized. Hence this is then indeed the standard BV-complex as discussed there in the section _[Multivector fields dual to differential forms](https://ncatlab.org/nlab/show/BV-BRST+formalism#MultivectorFieldsDualToDifferentialForms)_.


If we disregard the [[BV-operator]] $\Delta$, then more generally there are [[Poisson n-algebras]] for all $n$, which are as above but with the bracket of degree $1-n$

$$
  \array{
    operation && \{-,-\}
    \\
    degree && 1-n
  }
  \,.
$$

Notice that this means that $P_2$ algebras are very similar to $P_0$-algebras: for the former the backet has degree -1, for the latter it has degree +1.

Now the [[BD-operad]], which is a chain complex of $\mathbb{R}[ [\hbar ] ]$-[[modules]] ([[formal power series]] ring in one [[variable]] $\hbar$) has as chain complex of binary operations

$$
  BD(2)
    \;\coloneqq\;
  \array{
    ( \cdots &\to& 0 &\to& \left\langle(-\cdot -)\right\rangle &\stackrel{d_{operad}}{\to}& \left\langle \hbar \{-,-\} \right\rangle &\to& 0 &\to& \cdots )
    \\
    && && 0 && 1 
  }
  \,.
$$

Notice: The differential takes the single generator in degree 0 to the single generator in degree 1. As a differential in chain complexes of $\mathbb{R}$-modules this would be the null complex, but since the bracket carries a prefactor of $\hbar$, we get something non-null if we regard this suitably filtered over $\hbar$... In particular, setting "$\hbar = 0$" by forming the [[tensor product]] with $\mathbb{R} \simeq \mathbb{R}[ [\hbar] ]/(\hbar)$ turns it into the chain complex concetrated on a single generator in degree 0. This is the $E_0$-operad.
On the other hand, for finite $\hbar$, i.e. after tensoring with $\mathbb{R}[ [\hbar] ]/(\hbar-1)$ then it becomes the $\tilde E_0$-operad, which is equivalent to the $E_0$-operad (whose algebras are simply pointed chain complexes). See also [Gwilliam-Haugseng](#GwilliamHaugseng).

$$
  \array{
    && \tilde E_0 & \simeq E_0
    \\
    & {}^{\mathllap{\hbar = 1}}\nearrow
    \\
    BD 
    \\
    & {}_{\mathllap{\hbar = 0}}\searrow
    \\
    && P_0
  }
  \,.
$$



In any case, an [[algebra over an operad]] in chain complexes over the [[BD-operad]] has operations

$$
  \array{
    operation && d && \hbar \{-,-\}
    \\
    degree && +1 && +1
  }
$$


subject to 

$$
  d (a \cdot b) = (d a) \cdot b + (-1)^{\vert a \vert} a \cdot d b - \hbar\{a,b\}
  \,. 
$$

This has the same structure as the equation above for [[BV-algebras]] if we syntactically replace $d$ by $\Delta$ and remove the factor of $\hbar$. But since $d$ and $\Delta$ are on a different footing, these similarity between these two equations is only somewhat superficial.


## References

* {#CostelloGwilliam} [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in quantum field theory Volume 2_ ([pdf](http://people.mpim-bonn.mpg.de/gwilliam/vol2may8.pdf))

* {#GwilliamHaugseng} [[Owen Gwilliam]], [[Rune Haugseng]], _Linear Batalin-Vilkovisky quantization as a functor of ∞-categories_ ([arXiv:1608.01290](https://arxiv.org/abs/1608.01290))
 