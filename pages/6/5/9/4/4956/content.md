
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

_Differentiation_ is the [[functor]] $d : Diff \to Diff$ on the [[category]] [[Diff]] of [[smooth manifold]]s that sends

* a manifold $X$ to its [[tangent bundle]] $T X$;

* a [[smooth function]] $f : X \to Y$ to its differential $d f : T X \to T Y$:

  if $\gamma : [-1,1] \to X$ is a path in $X$ representing a vector $v \in T_x X$, then $(d f)(v) \in T_{f(x)} Y$ is the vector represented by the path
  $[-1,1] \stackrel{\gamma}{\to} X \stackrel{f}{\to} Y$. 

In a context $H$ of [[synthetic differential geometry]] the functor $d$ is simply the [[internal hom]] out of the [[infinitesimal space|infinitesimal interval]] $D$

$$
  d = [D, -] : H \to H
  \,.
$$

## Properties

From the above definition the fact that differentiation is indeed functorial is immediate. This functoriality statement is known in the literature as the [[chain rule]] for differentiation.



[[!redirects derivative]]