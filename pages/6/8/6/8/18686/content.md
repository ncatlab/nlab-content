
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In the context of [[spin geometry]], the _Feynman slash notation_ is a notation  popular in [[physics]] texts, specifically in [[quantum field theory]], where it was introduced by [[Richard Feynman]], for the [[Clifford algebra]]-element associated with a given [[vector]].

Abstractly, given an [[inner product space]] $(V, \langle -\rangle)$ with associated [[Clifford algebra]] $Cl_{(V,\langle -,-\rangle)}$, then there is a canonical [[linear map]]

$$
  f\;\colon\;V \longrightarrow Cl_{(V,\langle -,-\rangle)}
$$

such that $f(v)\cdot f(v) = \langle v,v\rangle \cdot 1 \in  Cl_{(V,\langle -,-\rangle)}$.

Now let $\left( x^\mu\right)_{\mu = 1}^{dim(V)}$ be a [[linear basis]] for $V$, so that every vector $D \in V$ may be expanded, using the [[Einstein summation convention]], as

$$
  D \,=\, D_\mu x^\mu
  \,,
$$

and let $\left( \gamma^\mu \coloneqq f(x^\mu)\right)$ be the corresponding generators of the [[Clifford algebra]]. Then this map is given by

$$  
  D \,\mapsto\, D_\mu \gamma^\mu
  \,.
$$

This particular class of instances of the [[Einstein summation convention]] on the right is further abbreviated with a slash as

$$
  \slash{D} \,\coloneqq\, D_\mu \gamma^\mu
  \,.
$$

This is the __Feynman slash notation__.

> (Chrome users beware that the `\slash{...}` command used in the previous line may not be currently rendering in that browser.)

Concretely, in [[quantum field theory]], the [[Dirac operator]] on [[Minkowski spacetime]] may be expanded as $\mathrm{i} \gamma^\mu \frac{\partial}{\partial x^\mu}$ and this is then similarly abbreviated as

$$
  \mathrm{i} \slash{\partial} 
    \;\coloneqq\; 
  \mathrm{i} \gamma^\mu \frac{\partial}{\partial x^\mu}
  \,.
$$


## Related concepts

* [[Einstein summation convention]]


## References

* Wikipedia, _[Feynman slash notation](https://en.wikipedia.org/wiki/Feynman_slash_notation)_


[[!redirects Feynman slash]]
[[!redirects Feynman slash notation]]
