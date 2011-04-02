+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


Let $Ch(\mathcal{A})$ be a [[category of chain complexes]] in a [[category]] $\mathcal{A}$ that is a [[closed monoidal category]]. For instance the category of chain complexes in $\mathcal{A} = $ [[Vect]]${}_k$.

For $V \in Ch$ any [[object]] -- any [[chain complex]] -- write

$$
  end(V) := [V,V] \in Ch
$$

for the [[internal hom]] object of morphisms from $V$ to $V$. This is the chain complex which in degree $n$ is

$$
  end(V)_n = \bigoplus_{i \in \mathbb{Z}} Hom_{\mathcal{A}}(V_i, V_{i+n})
$$

and whose [[differential]] 

$$
  \delta_{end(V)} : end(V)_n \to end(V)_{n-1} 
$$

is given by 

$$
  \delta_{end(V)} (V_i \stackrel{f}{\to} V_{i+1})
  =
  (V_i \stackrel{f}{\to} V_{i+n} \stackrel{\delta_V}{\to} V_{i+n-1})  
  - (-1)^i
  (V_{i+1} \stackrel{\delta_V}{\to} V_i \stackrel{f}{\to} V_{i+1})
  \,.
$$

This complex naturally carries the structure of an [[internalization|internal]] [[Lie algebra]], hence of a [[dg-Lie algebra]] with Lie bracket given by the graded [[commutator]] for $f \in end(V)_k$ and $g \in end(V)_l$

$$
  [f,g] = f \circ g - (-1)^{k \cdot l} g \circ f
  \,.
$$

This 

$$
  \mathfrak{gl}(V) := (end(V), [-,-])
$$ 

is the **endomorphism dg-Lie algebra** of $V$. Or, since dg-Lie algebras are special cases of [[L-∞ algebra]]s: the **endomorphism $L_\infty$-algebra** of $V$.

## Representation

A [[representation]] of an [[L-∞ algebra]] $\mathfrak{g}$ on a chain complex $V$ is a morphism of $L_\infty$-algebras

$$
  \rho : \mathfrak{g} \to \mathfrak{gl}(V)
  \,.
$$

Sometimes this is called a _representation up to homotopy_ . 

## Examples

* For $V$ a [[vector space]] regarded as a [[chain complex]] concentrated in degree-0, $\mathfrak{gl}(V)$ is the ordinary [[general linear Lie algebra]] of $V$. 

## References

The definition is considered for instance in

* Yunhe Sheng, [[Chenchang Zhu]], _Integration of semidirect product Lie 2-algebras_

[[!redirects endomorphism L-∞ algebra]]
[[!redirects endomorphism L-∞ algebras]]

[[!redirects endomorphism L-infinity algebra]]
[[!redirects endomorphism L-infinity algebras]]