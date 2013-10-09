
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Discussion of [[superalgebra]] and [[supergeometry]] involves, by definition, crucial minus signs appearing in certain expressions. While there is a systematic rule for these, when superalgebra/supergeometry is combined with other topics that crucially involve their own signs, such as [[homological algebra]], or ordering of terms, such as in [[noncommutative algebra]], then the combined sign rule may appear intricate. This page here is meant to explicitly list some common expressions with their signs, for easy reference. We follow the article ([Deligne-Freed 99](#DeligneFreed99)) which has the same goal.

## Topics

### Differential forms on supermanifolds
 {#DifferentialFormsOnSupermanifolds}

We discuss the sign rules for the [[de Rham complex]] of [[differential forms]] on a [[supermanifold]]. (See also [Deligne-Freed 99, section 6](#DeligneFreed99))

For $p,q \in \mathbb{N}$, let $\mathbb{R}^{p|q}$ the [[super Cartesian space]] of [[dimension]] $(p|q)$. This is the [[supermanifold]] defined by the fact that its [[algebra of functions]] is freely generated, as a [[smooth superalgebra]] by even-graded [[coordinate]]-functions $\langle \{x^a\}_{1}^p$ and odd-graded coordinate function $\{ \theta^\alpha\}_{\alpha= 1}^q$

$$
  C^\infty(\mathbb{R}^{p|q}) = \langle \{x^a\}_{1}^p, \{ \theta^\alpha\}_{\alpha= 1}^q \rangle
  \,.
$$

Accordingly, by the discussion at _[[Kähler forms]]_, the [[de Rham complex]] of [[differential forms]] on $\mathbb{R}^{p|q}$ is freely generated as a super-[[module]] over the [[smooth superalgebra]] $C^\infty(\mathbb{R}^{p|q})$ by expressions of the form $\mathbf{d}x^{a_1} \wedge \cdots \wedge \mathbf{d}x^{a_k} \wedge \mathbf{d}\theta^{\alpha_1} \wedge \cdots \wedge \mathbf{d}\theta^{\alpha_l}$.

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
  x^{a_1} x^{a_2} = + x^{a_2} x^{a_1}
$$

$$
  x^a \theta^\alpha = + \theta^\alpha x^a
$$

$$
  \theta^{\alpha_1} \theta^{\alpha_2}
  =
  -
  \theta^{\alpha_2} \theta^{\alpha_1}
$$


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

### Cohomology of super Minkowski spacetime

We discuss the [[Chevalley-Eilenberg algebra]] of [[super Minkowski spacetime]], regarded as a [[super translation Lie algebra]], equivalently as the [[quotient]] of the [[quotient]] of the 
[[super Poincaré Lie algebra]] by the [[Lorentz Lie algebra]].

This is the sub-algebra of the [above](#DifferentialFormsOnSupermanifolds) de Rham complex of the [[left invariant differential forms]]:

$$
  CE(\mathbb{R}^{d-1,1;N})
  =
  \Omega^\bullet_{li}(\mathbb{R}^{d-1,1;N})
  \hookrightarrow
  \Omega^\bullet(\mathbb{R}^{d-1,1;N})
  \,.
$$

With the [above](#DifferentialFormsOnSupermanifolds) notation these are

$$
  \psi^\alpha \coloneqq \mathbf{d}\theta^\alpha
$$

$$
  e^a \coloneqq \mathbf{d}x^a + \theta \Gamma^a \mathbf{d}\theta
  \,.
$$

With the [above](#DifferentialFormsOnSupermanifolds) sign rules it follows that


$$
  e^{a_1} \wedge e^{a_2} = + e^{a_2} \wedge e^{a_1}
$$

$$
  e^{a} \wedge \psi^\alpha = - \psi^\alpha \wedge e^a
$$

$$
  \psi^{\alpha_1} \wedge \psi^{\alpha_2}
  = 
  + 
  \psi^{\alpha_2} \wedge \psi^{\alpha_1}
  \,.
$$

## References


* [[Pierre Deligne]], [[Dan Freed]], _Sign manifesto_ ([pdf](http://publications.ias.edu/sites/default/files/79_SignManifesto.pdf)) 
   {#DeligneFreed99}

which appears in
 
* [[Pierre Deligne]], [[Daniel Freed]], _Supersolutions_ ([arXiv:hep-th/9901094](http://arxiv.org/abs/hep-th/9901094)).

which in turn appears in 

* [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))