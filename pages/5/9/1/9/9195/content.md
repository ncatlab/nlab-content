
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _Einstein-Yang-Mills-Dirac theory_  in [[physics]] is the [[theory (physics)|theory]]/[[model (in theoretical physics)]] describing [[gravity]] together with [[Yang-Mills fields]] and coupled to [[fermion|fermionic]] [[matter]]. 

Einstein-Yang-Mills-Dirac theory is a [[local Lagrangian]] [[field (physics)|field]] theory defined by the [[action functional]] which is the [[Einstein-Hilbert action]] plus the [[Yang-Mills action functional]] involving the given metric,

$$
  S_{G+YM}
  \;
   \colon
  \;
  (e, \nabla, \psi)
  \mapsto
  \int_{X} R(e) vol(e)
  + 
  \int_X \langle F_\nabla \wedge \star_e F_\nabla\rangle
  + 
  \int_X (\psi, D_{e,\nabla} \psi)
  \,,
$$

where 

* $X$ is the [[compact topological space|compact]] [[smooth manifold]] underlying [[spacetime]], 

* $e$ is the [[vielbein field]] which encodes the [[field (physics)|field]] of [[gravity]] 

* $\nabla$ is the $G$-[[principal connection]] which encodes the [[Yang-Mills field]], 

* $vol(e)$ is the [[volume form]] induced by $e$;

* $R(e)$ is the [[scalar curvature]] of $e$;

* $F_\nabla$ is the [[field strength]]/[[curvature]] [[differential 2-form]] of $\nabla$;

* $\star_e$ is the [[Hodge star]] operator induced by $e$.

* $\langle -,-\rangle$ is the given [[invariant polynomial]] on the [[Lie algebra]] of the [[gauge group]].

## Related concepts

* [[Einstein-Hilbert action]]

* [[Einstein-Maxwell theory]]

* [[Einstein-Yang-Mills theory]]

* **Einstein-Yang-Mills-Dirac theory**

  * [[spectral action]]

* [[Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory]]

[[!include standard model of fundamental physics - table]]

## References

* Gerd Rudolph, Torsten Tok, Igor P. Volobuev, _Exact solutions in Einstein-Yang-Mills-Dirac systems_, J.Math.Phys. 40 (1999) 5890-5904 ([arXiv:gr-qc/9707060](http://arxiv.org/abs/gr-qc/9707060))

Section _[Prequantum gauge theory and Gravity](geometry+of+physics#ActionFunctionalsForChernSimonsTypeGaugeTheories)_ in 

* _[[geometry of physics]]_

[[!redirects Einstein-Yang-Mills-Dirac theories]]
