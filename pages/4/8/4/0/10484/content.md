
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The analog of a [[Cartesian space]] in [[supergeometry]], a [[supermanifold]] with a single canonical [[coordinate chart]].

For suitable even|odd dimension this is naturally equipped with the structure of a [[supergroup]] that makes it a [[super-translation group]]. For Minkowski signature this is [[super-Minkowski spacetime]].


## Definition


For $p,q \in \mathbb{N}$, let $\mathbb{R}^{p|q}$ the _super Cartesian space_ of [[dimension]]_ $(p|q)$. This is the [[supermanifold]] defined by the fact that its [[algebra of functions]] is freely generated, as a [[smooth superalgebra]] by even-graded [[coordinate]]-functions $\langle \{x^a\}_{1}^p$ and odd-graded coordinate function $\{ \theta^\alpha\}_{\alpha= 1}^q$. Equivalently this is the [[tensor product]] of the [[smooth functions]] on $\mathbb{R}^p$ with the real [[Grassmann algebra]] on $q$ generators:

$$
  \begin{aligned}
      C^\infty(\mathbb{R}^{p|q}) 
      & \coloneqq 
      \langle \{x^a\}_{1}^p, \{ \theta^\alpha\}_{\alpha= 1}^q \rangle
      \\
      & = C^\infty(\mathbb{R}^p)\otimes_{\mathbb{R}} \wedge^\bullet \mathbb{R}^q
  \end{aligned}
  \,.
$$

For more see at _[[affine super scheme]]_ and at _[[geometry of physics -- superalgebra]]_ and at _[[geometry of physics -- supergeometry]]_.


## Examples

* [[superpoint]], [[odd line]]

* [[super Minkowski spacetime]]

## Properties

### De Rham complex of differential forms

We discuss the [[de Rham complex]] of [[super differential forms]] on a super Cartesian space. (See also at _[[signs in supergeometry]]_.)

Accordingly, by the discussion at _[[Kähler forms]]_, the [[de Rham complex]] of [[super differential forms]] on $\mathbb{R}^{p|q}$ is freely generated as a super-[[module]] over the [[smooth superalgebra]] $C^\infty(\mathbb{R}^{p|q})$ by expressions of the form $\mathbf{d}x^{a_1} \wedge \cdots \wedge \mathbf{d}x^{a_k} \wedge \mathbf{d}\theta^{\alpha_1} \wedge \cdots \wedge \mathbf{d}\theta^{\alpha_l}$.

$$
  \Omega^\bullet(\mathbb{R}^{p|q})
  = 
  C^\infty(\mathbb{R}^{p|q})
  \left[
   \left\{
     \mathbf{d}x^{a_1} \wedge \cdots \wedge \mathbf{d}x^{a_k} 
     \wedge 
     \mathbf{d}\theta^{\alpha_1} \wedge \cdots \wedge \mathbf{d}\theta^{\alpha_l}
   \right\}
  \right]
  \,.
$$

This [[de Rham complex]] now carries the structure of a 

* differential graded-commutative graded commutative superalgebra 

which should be thought of as bracketet as follows

* differential graded-commutative graded (commutative superalgebra).

This means in effect that elements of $\Omega^\bullet(\mathbb{R}^{p|q})$ carry a $\mathbb{Z} \times \mathbb{Z}_2$-[[graded object|grading]], where we may say that 

* $\mathbb{Z}$ corresponds to the "cohomological grading";

* $\mathbb{Z}_2$ corresponds to the super-grading.

We write 

$$
  (n,\sigma)\in \mathbb{Z} \times \mathbb{Z}_2
$$ 

for elements in this grading group. 

In this notation the grading of the elements in $\Omega^\bullet(\mathbb{R}^{p|q})$ is all induced by the fact that the de Rham differential $\mathbf{d}$ itself is a [[derivation]] of degree $(1,even)$.

| generator | bi-degree |
|--|--|
| $x^a$ | (0,even) |
| $\theta^\alpha$ | (0,odd) |
| $\mathbf{d}$ | (1,even) |

Here the last line means that we have

| generator | bi-degree |
|--|--|
| $x^a$ | (0,even) |
| $\theta^\alpha$ | (0,odd) |
| $\mathbf{d}x^a$ | (1,even) |
| $\mathbf{d}\theta^\alpha$ | (1,odd) |


The formula for the "cohomologically- and super-graded commutativity" in $\Omega^\bullet(\mathbb{R}^{p|q})$ is 

$$
  \alpha \wedge \beta 
  = 
  \;
  (- 1)^{n_\alpha n_\beta + \sigma_\alpha \sigma_\beta}
  \;
  \beta \wedge \alpha
$$

for all $\alpha,  \beta \in \Omega^\bullet(\mathbb{R}^{p|q})$ of homogeneous $\mathbb{Z}\times \mathbb{Z}_2$-degree. Hence there are _two_ contributions to the sign picked up when exchanging two super-differential forms in the wedge product:

1. there is a "cohomological sign" which for commuting a $p_1$-forms past a $p_2$-form is $(-1)^{p_1 p_2}$;

1. in addition there is a "super-grading" sich which for commuting a $\sigma_1$-graded coordinate function past a $\sigma_2$-graded coordinate function (possibly under the de Rham differential) is $(-1)^{\sigma_1 \sigma_2}$.


Some examples:

$$
  x^{a_1} (\mathbf{d}x^{a_2}) = + (\mathbf{d}x^{a_2}) x^{a_1}
$$


$$
  \theta^\alpha (\mathbf{d}x^a) = + (\mathbf{d}x^a) \theta^\alpha
$$

$$
  \theta^{\alpha_1} (\mathbf{d}\theta^{\alpha_2}) 
   = 
  - (\mathbf{d}\theta^{\alpha_2}) \theta^{\alpha_1}
$$

$$
  \mathbf{d}x^{a_1}
  \wedge
  \mathbf{d} x^{a_2}
  =
  -
  \mathbf{d} x^{a_2}
  \wedge
  \mathbf{d} x^{a_1}
$$


$$
  \mathbf{d}x^a
  \wedge
  \mathbf{d} \theta^{\alpha}
  =
  -
  \mathbf{d}\theta^{\alpha}
  \wedge
  \mathbf{d} x^a
$$

$$
  \mathbf{d}\theta^{\alpha_1}
  \wedge
  \mathbf{d} \theta^{\alpha_2}
  =
  +
  \mathbf{d}\theta^{\alpha_2}
  \wedge
  \mathbf{d} \theta^{\alpha_1}
$$

## Related concepts


* [[supergeometry]]

* [[super smooth set]]

* [[smooth super infinity-groupoid]]

* [[super formal smooth infinity-groupoid]]

* [[super-Cartan geometry]]

[[!redirects super Cartesian spaces]]

[[!redirects Cartesian superspace]]
[[!redirects Cartesian superspaces]]

[[!redirects super-Cartesian space]]

[[!redirects super Euclidean space]]
[[!redirects super Euclidean spaces]]
[[!redirects super-Euclidean space]]
[[!redirects super-Euclidean spaces]]

