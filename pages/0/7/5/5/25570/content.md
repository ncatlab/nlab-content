+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **quaternionic set** is a [[simplicial set]] with a [[quaternion group|quarternionic]] symmetry, in other words it is a [[presheaf]] on the quaternionic simplex category $\Delta Q$ which contains the ordinary [[simplex category]] $\Delta$ plus $Q_{n+1}^{op}$ as the automorphism group at the objects $[n]$ whence quaternionic sets are an example of the construction of [[skew-simplicial set|skew-simplicial sets]] from a [[crossed group|crossed simplicial group]].

## Definition

Let $Q_n$ be the group given by the presentation $\{x,y| x^n=y^2\;,yxy^{-1}=x^{-1}\}$ be the nth [[quaternion group]], also called a binary [[dihedral group]].

+-- {: .num_defn }
###### Definition
The **quaternionic simplex category** $\Delta Q$ has objects $[n],\; n\geq 0\;$, contains the (topologists’) [[simplex category]] $\Delta$ as a subcategory and has $Aut_{\Delta Q}([n])=Q_{n+1}^{op}$. Furthermore, any morphism $\varphi$ in $\Delta Q$ can be written uniquely as a product $\varphi=s\circ q$ with $s\in \Delta$ and $q=Q_{n+1}^{op}$. A **quaternionic set** is a presheaf on $\Delta Q$.
=--

## Properties

* According to the classification of [[crossed group|crossed simplicial groups]], $\Delta Q$ corresponds to the [[exact sequence]] of crossed groups $1\to \mathbb{Z}/2\to Q_*\to D_*\to 1\; .$ Whence it is of _dihedral type_. The [[geometric realization]] of $Q_*$ is the normalizer of $S^1$ in $S^3$ (cf. [Fiedorowicz-Loday](#FL91), [Krasausakas](#Krasausakas87)).

* Truncating $\Delta Q$ at $[1]$ and taking presheaves, one obtains a category of quaternionic graphs $Set^{\Delta Q_{\leq 1}^{op}}$ with a $Q_2$ action, just like [[graphic category|reflexive graphs]] result from $\Delta_1$, resp. reversible graphs from truncating $\Delta S$ in the [[symmetric set|symmetric simplex category]].

## Related entries

* [[skew-simplicial set]]

* [[crossed group]]

* [[cyclic set]]

* [[quaternion]]


## References

* {#Loday87}[[Jean-Louis Loday]], _Homologies diédrale et quaternionique_, Adv. in Math. **66** (1987) pp.119-148.

* {#Dunn89}Gerald Dunn, _Dihedral and Quaternionic Homology and Mapping Spaces_, K-theory **3** (1989) pp.141-161.

* {#Krasauskas87}R. Krasauskas, _Skew-simplicial groups_, Lithuanian Math. J. **27** pp.47-54 (1987).

* {#FL91}Zbigniew Fiedorowicz, [[Jean-Louis Loday]], _Crossed simplicial groups and their associated homology_, Trans. AMS **326** pp.57-87 (1991).

* [[Tobias Dyckerhoff]], [[Mikhail Kapranov]], _Crossed simplicial groups and structured surfaces_, arXiv:1403.5799 (2014). ([abstract](https://arxiv.org/abs/1403.5799))



