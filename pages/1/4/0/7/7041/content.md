
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _bump function_ is a [[smooth function]] with [[compact support]], especially one that is not zero on a space that it not [[compact space|compact]].

One reason the category [[SmthMfd]] of [[smooth manifolds]] and [[smooth functions]] is important is that a good supply of bump functions exists; this fact accounts for the great flexibility of smooth objects, in stark contrast to [[analytic geometry]] or [[algebraic varieties]] (since non-zero analytic or algebraic functions with compact support exist only on compact spaces). For instance, bump functions can be used to construct _[[partition of unity|partitions of unity]]_, which can in turn be used to smoothly patch together local structures into a global structure without obstruction, as for example [[Riemannian metric|Riemannian metrics]]. 


## Constructions

Define a function $\phi(x)$ on the standard [[open ball|open unit ball]] of the [[cartesian space]] $\mathbb{R}^n$ by 
$$
  \phi(x) = \exp\left(
   \frac1{{\|x\|^2} - 1}
  \right)
$$ 
so that $\phi(x)$ and all of its higher [[derivatives]] vanish rapidly as $x$ approaches the [[boundary]]. This gives a [[smooth function]] [[compact support|compactly supported]] on the [[unit ball]] centered at the origin. 

For $\varepsilon \gt 0$, define $\phi_\varepsilon(x) \coloneqq \phi(x/\varepsilon)$, and define 
$$\psi_\varepsilon = \frac{\phi_\varepsilon}{{\|\phi_\varepsilon\|}_1}$$ 
so that the family $(\psi_\varepsilon)_\varepsilon$ is a smooth [[approximation to the identity]] (of convolution, the [[Dirac distribution|Dirac functional]]), compactly supported on the closed ball of radius $\varepsilon$ and having an $L^1$-norm equal to $1$. Then, it is standard that for any pair $K \subset V$ with $K$ [[compact subspace|compact]] and $V$ [[open subspace|open]] in a cartesian space $\mathbb{R}^n$, we can choose an open $U$ containing $K$ and with compact [[closure]] contained in $V$, and then taking the [[convolution]] product 
$$\psi_\varepsilon \ast \chi_U$$ 
of $\psi_\varepsilon$ with the [[characteristic function]] $\chi_U$, for $\varepsilon$ sufficiently small, we obtain a smooth function equal to $1$ on $K$ and equal to $0$ outside $V$.

By performing the above construction in [[charts]], we obtain, in any [[smooth manifold]], a smooth function equal to $1$ on any [[compact subspace]] $K$ and equal to $0$ outside any [[neighbourhood]] $V$ of $K$.  (This is a smooth [[completely regular space|regularity property]].)



## References

* wikipedia, _[bump function](http://en.wikipedia.org/wiki/Bump_function)_

An different example is examined in detail in

* Juan Arias de Reyna, _An infinitely differentiable function with compact support: Definition and properties_, arXiv:[1702.05442](https://arxiv.org/abs/1702.05442) (English translation of: _Definici&#243;n y estudio de una funci&#243;n indefinidamente diferenciable de soporte compacto_, Rev. Real Acad. Ciencias 76 (1982) 21-38 available from [Universidad de Sevilla repository](http://hdl.handle.net/11441/28557))

One can also build bump functions that are _nowhere_ analytic (as opposed to merely on the boundary of the support, as above) using, for instance, the Fabius function:

* Wikipedia, [_Fabius function_](https://en.wikipedia.org/wiki/Fabius_function)

[[!redirects bump function]]
[[!redirects bump functions]]
