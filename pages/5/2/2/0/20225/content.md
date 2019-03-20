
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Definition

There is some variation in the literature on what one calls a "[[quaternionic]] [[manifold]]''. The most general definition, however, encompassing all the others, is:

+-- {: .num_defn #QuaternionicManifold}
###### Definition
**(Quaternionic manifold)**

For $n \geq 2$, a **quaternionic manifold** is a real 4n-dimensional manifold M with a $\text{GL} (n,\mathbf{H})\cdot \mathbf{H} ^{\times }$-structure which admits a [[torsion]]-free [[connection]] $\nabla$ (i.e. is integrable as a [[G-structure]]).


=--

When $\nabla$ does not exist $M$ is called _almost quaternionic_, and this is just a [[reduction of the structure group]] of $M$ along a [[Lie group]] inclusion $\text{GL}(n, \mathbf{H}) \hookrightarrow \text{GL}(4n, \mathbf{R})$. 

Other definitions have been given, based on the following useful but more naïve reasoning: consider two almost [[complex structures]] on a smooth $4n$-manifold $M$, say $\langle X, I \rangle$ and $\langle X, J \rangle$, given the relation $\{ I, J \} =0$. Then call the structure $\langle X, I, J \rangle$ is called _almost quaternionic_ and a map $\varphi:  \langle X, I, J \rangle \rightarrow \langle Y, K, F \rangle$ of almost quaternionic structures is called "quaternionic" if it is separately [[complex analytic]] as a map $\langle X, I \rangle \rightarrow \langle Y, K \rangle$ and also as a map $\langle X, J \rangle \rightarrow \langle Y, F \rangle$. 

When $\mathbf{R}^4$ is given a quaternionic multiplication with anti-commuting imaginary units $i$ and $j$, this is actually equivalent to $\varphi : \mathbf{R}^4 \rightarrow \mathbf{R}^4$ satisfying the [[Cauchy-Feuter]] complex:
$$ i \frac{\partial}{\partial u_3} = \frac{\partial }{\partial u _4}, j \frac{\partial }{ \partial u_2} = \frac{\partial }{\partial u_4}$$
$$i \frac{\partial}{\partial u_1} = \frac{\partial }{\partial u_2}, j \frac{\partial }{\partial u_1 } = \frac{\partial }{\partial u_3}$$
known as a starting point for defining a notion of "quaternionic [[holomorphy]]", since the Cauchy-Feuter complex consists of two separate [[Cauchy-Riemann]] systems in the imaginary units $i, j$. Such a complex exists on $\mathbf{R}^{4n}$ for any $n$ as an extended Cauchy-Fueter complex consisting of the systems above, repeated for each set of four coordinates. Hence, $\mathbf{R}^{4n}$ as a smooth manifold can always be endowed with an almost quaternionic structure. On this account of quaternionic structure, a _quaternionic $n$-manifold_ is then an almost quaternionic structure on a smooth manifold $M$ such that $M$ has an atlas of quaternionic maps, considered with respect to the standard quaternionic structure on $\mathbf{R}^{4n}$ just described. However, such a definition has serious drawbacks, such as the fact that quaternionic projective $n$-space $\mathbf{H}P^n$ is not a "quaternionic manifold" in this sense for any $n$. It is, however, a quaternionic manifold under the official definition above. 

## Holonomy

(...)

## Twistor Space of a Quaternionic Manifold

## Related concepts

* [[biquaternionic manifold]], [[hypercomplex manifold]], [[Kähler manifold]], [[hyper-Kähler manifold]]

## References

Book references include:

* {#Besse}[[Arthur Besse]], _Einstein Manifolds_, Springer-Verlag 1987.

* {#Joyce} [[Dominic Joyce]], _Compact Manifolds with Special Holonomy_, Oxford University Press, 2000.

Classical references:

* {#Salamon} S.M. Salamon, "Differential Geometry of Quaternionic Manifolds", Annales scientifiques de l’É.N.S. 4e série, tome 19, no 1 (1986), p. 31-55.

See also

* Wikipedia, _[Quaternionic manifold](https://en.wikipedia.org/wiki/Quaternionic_manifold)_

[[!redirects quaternionic manifolds]]
[[!redirects quaternion manifold]]
