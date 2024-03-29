
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

In the context of [[generalized complex geometry]] one says for $X$ a [[manifold]], $T X$ its [[tangent bundle]] and $T^* X$ the [[cotangent bundle]] that the fiberwise [[direct sum]]-bundle $T X \oplus T^* X$ is the _generalized tangent bundle_.

More generally, a [[vector bundle]] $E \to X$ that sits in an [[exact sequence]] $T^* X \to E \to T X$ is called a _generalized tangent bundle_, such as notably those underlying a [[Courant Lie 2-algebroid]] over $X$.

## Properties

### As an associated bundle

The ordinary [[tangent bundle]] is the canonical [[associated bundle]] to the [[general linear group]]-[[principal bundle]] classified by the morphism

$$
  g_{T X} : X \to \mathbf{B} GL(n)
$$

to the [[smooth infinity-groupoid|smooth]] [[moduli stack]] of $GL(n)$.

Similarly there is a canonical morphism

$$
  (g_{T X}, g^{-T}_{T X}) : X \to \mathbf{B} O(n,n)
$$

to the [[moduli stack]] which is the [[delooping]] of the [[Narain group]] $O(n,n)$. This classifies the $O(n,n)$-principal bundle to which $T X \oplus T^* X$ is associated.

### Reduction of structure group

Where a [[reduction of structure groups|reduction of the structure group]] of the tangent bundle along $\mathbf{B} O(n) \hookrightarrow \mathbf{B} GL(n)$ is equivalently a [[vielbein]]/[[orthogonal structure]]/[[Riemannian metric]] on $X$, so a reduction of the structure group of the generalized tangent bundle along $\mathbf{B} (O(n) \times O(n)) \to \mathbf{B}O(n,n)$ is a _[[generalized vielbein]]_, defining a _[[type II geometry]]_ on $X$.

Other [[reduction of the structure group|reductions]] yield other geometric notions, for instance:

* reduction along $U(n,n) \to O(2n,2n)$ is a [[generalized complex structure]]; 

* further reduction along $SU(n,n)  \to U(n,n) \to O(2n,2n)$ is a [[generalized Calabi-Yau manifold]] structure.


[[!include Spin(8)-subgroups and reductions -- table]]



## Related concepts

* [[tangent bundle]]

* [[Courant Lie 2-algebroid]]

* [[exceptional tangent bundle]]

[[!redirects generalized tangent bundles]]
