[[!redirects generalised Scherk-Schwarz reduction]]
[[!redirects generalised Scherk-Schwarz reduction]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _generalized Scherk-Schwarz reduction_ is a [[dimensional reduction]] combined with a [[duality]] twist for [[exceptional field theory]] and [[double field theory]].

Consider an [[exceptional field theory]] on a certain extended space, i.e. a [[smooth manifold]] locally [[isomorphism|isomorphic]] to $U \times R$, where $R$ is the underlying [[vector space]] of the [[fundamental representation]] of some [[duality in string theory|duality]] [[group]] $G$ (e.g. [[U-duality]] or [[T-duality]]). Let us call $x$ the local coordinates of the base manifold $U$ and $(y,\tilde{y})$ the ones of the [[fiber]] $R$, called _internal manifold_.

A _generalized Scherk-Schwarz reduction_ is performed by introducing twisting $G$-valued matrices $E^{A}_{\;\;M}(y,\tilde{y})$ and by encoding all the dependence of the fields on the coordinates of the internal manifold with the following ansatz:

$$ T_{M_1 \dots M_n}(x,y,\tilde{y}) = E^{A_1}_{\;\;M_1}(y,\tilde{y}) \cdots E^{A_n}_{\;\;M_n}(y,\tilde{y}) T_{A_1\dots A_n}(x) $$

on any generalized [[tensor field]] $T_{M_1 \dots M_n}$ on the extended space. The $G$-valued matrices $E^{A}_{\;\;M}(y,\tilde{y})$ can be seen as generalized [[frame fields]] for the internal manifold.

## Examples

### Double field theory on the torus

Consider a [[double field theory]] on the torus $T^{2n}$, where the [[T-duality]] group $O(n,n)$ acts in the [[fundamental representation]]. We are in the case where the _external space_ is just a point. Let the doubled metric be

$$ \mathcal{H}_{MN} = \begin{pmatrix} g -B g^{-1}B & B g^{-1} \\ -g^{-1}B  &  g^{-1}\end{pmatrix} $$

Now, if we define $O(n,n)$-valued matrices

$$ E^A_{\;\;M} = \begin{pmatrix}e^a_{\mu} & 0 \\ e^\rho_a B_{\rho\mu} & e^\mu_a \end{pmatrix} $$

we can immediately write the generalized Scherk-Schwarz reduction over the point by

$$ \mathcal{H}_{MN}(y,\tilde{y}) = E^{A_1}_{\;\;M_1}(y,\tilde{y}) \cdots E^{A_n}_{\;\;M_n}(y,\tilde{y}) \mathcal{H}_{AB} $$

where $\mathcal{H}_{AB} = \mathrm{diag}(\delta_{a b},\,\delta^{a b})$. This simple example captures the analogy with ordinary [[frame fields]].


## Related concepts

* [[doubled geometry]]

* [[exceptional field theory]]

* [[gauged supergravity]]