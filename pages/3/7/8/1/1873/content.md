
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



* **groupoid of Lie-algebra valued forms**

* [[2-groupoid of Lie 2-algebra valued forms]]

* [[3-groupoid of Lie 3-algebra valued forms]]

* [[∞-groupoid of ∞-Lie-algebra valued forms]]

***

#Contents#
* automatic table of contents goes here
{:toc}



## Idea

The [[∞-Lie groupoid|Lie groupoid]] of _Lie algebra valued forms_ is a kind of differential refinement of the [[delooping]] [[∞-Lie groupoid|Lie groupoid]] $\mathbf{B}G$ of a [[Lie group]] $G$:

its $U$-parameterized smooth families of objects are _[[Lie algebra]] valued [[differential form]]s_ on $U$. Its $U$-parameterized families of morphisms are gauge transformations of these forms by $G$-valued [[smooth function]]s on $U$.

A [[cocycle]] with coefficients in this groupoid is a [[connection on a bundle]].

For more discussion of this see <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#LieGroups">∞-Lie groupoid -- Lie groups</a>.

## Definition 

+-- {: .un_defn}
###### Definition

For $G$ a [[Lie group]] the **groupoid of $Lie(G)$-valued differential forms** is as a [[groupoid]] [[internal category|internal to]] [[smooth spaces]], the [[sheaf]] of groupoids

$$
  \bar \mathbf{B}G := G TrivBund_\nabla(-) := [P_1(-), \mathbf{B}G]
$$

that to a smooth test space $U \in Diff$ assigns the [[functor category]] $[P_1(U),\mathbf{B}G]$ of smooth functors (functors internal to [[smooth spaces]]) from the [[path groupoid]] $P_1(U)$ of $U$ to the one-object [[delooping]] groupoid $\mathbf{B}G$.
=--

## Properties

+-- {: .un_theorem}
###### Theorem

The groupoid $\bar \mathbf{B}G$ is canonically equivalent to the smooth groupoid where
* objects are smooth $g$-valued 1-forms $A \in \Omega^1(U, g)$;
* morphisms $h : A \to A'$ are given by smooth $G$-valued functions $h \in C^\infty(U,G)$ such that
  $$
    A' = Ad_h(A) - h^* \bar \theta
  $$

Here $\bar \theta$ is the right invariant [[Maurer-Cartan form]] on $G$. A common way to write this is   $A' = Ad_h(A) + h d h^{-1}$.

=--

A proof is in [SchrWalI](#http://arxiv.org/abs/0705.0452).

### Differential nonabelian cohomology 

+-- {: .un_theorem}
###### Theorem

The [[cohomology]] with coefficients in $\bar \mathbf{B}G$ classifies $G$-[[principal bundles]] [[connection on a bundle]] with connection.

More is true: there is a natural canonical equivalence of groupoids
$$
  \mathbf{H}_{Diff}(X, \bar \mathbf{B}G)
  \simeq
  G Bund_\nabla(X)
  \,.
$$
=--


* There is the obvious projection
  $$
    \bar \mathbf{B}G \to \mathbf{B}G
    \,.
  $$

* Lifting a $G$-cocycle through this projection to a differential $G$-cocycle means equipping it with a [[connection on a bundle|connection]].

For $G = U(n)$ these differential cocycles model the [[Yang-Mills field]] in physics.

* For $G = U(1)$ the sheaf $\bar \mathbf{B}U(1)(-)$ coincides with the the [[Deligne cohomology|Deligne complex]] in degree 2, $\bar \mathbf{B}U(1)\simeq \mathbb{Z}(2)_D^\infty$, as described there. 

  * This corresponds to the [[electromagnetic field]].


## Generalization

See [[2-groupoid of Lie 2-algebra valued forms]].


## References

Details are in

* [[Urs Schreiber|U.S.]], [[Konrad Waldorf]], _Parallel Transport and Functors_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SWI">web</a>)

The definition in terms of differential forms is def 4.6 there. The equivalence to $[P_1(-), \mathbf{B}G]$ is proposition 4.7.

See also 

<a href="http://ncatlab.org/schreiber/edit/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+survey#ConnectionOnPrincipalBundle">differential cohomology in an (∞,1)-topos -- survey - connections on bundles</a>.


[[!redirects Lie-algebra valued 1-form]]
[[!redirects Lie-algebra valued 1-forms]]
[[!redirects Lie-algebra valued differential 1-form]]
[[!redirects Lie-algebra valued differential 1-forms]]

[[!redirects groupoid of Lie-algebra valued 1-forms]]

[[!redirects Lie algebra valued 1-forms]]
[[!redirects Lie algebra valued 1-form]]