
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
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

+-- {: .num_defn}
###### Definition

A [[smooth function]] $f : X \to Y$ between two [[smooth manifold]]s is a **local diffeomorphism** if the following equivalent conditions hold

* $f$ is both a [[submersion]] and an [[immersion]];

* for each point $x \in X$ the [[derivative]] $d f : T_x X \to T_{f(x)} Y$ is an [[isomorphism]] of [[tangent space|tangent]] [[vector space]]s;

* the canonical diagram

  $$
    \array{
       T X &\stackrel{d f}{\to}& T Y
       \\
       \downarrow && \downarrow
       \\
       X &\stackrel{f}{\to}& Y
    }
  $$

  (with the [[differential]] between the [[tangent bundles]]) on top is a [[pullback]];

* for each point $x \in X$ there exists an [[open subset]] $x \in U \subset X$ such that

  1. the [[image]] $f(U)$ is an [[open subset]] in $Y$;

  1. $f$ restricted to $U$ is a [[diffeomorphism]] onto its image

     $$
       f|_U : U \stackrel{\simeq}{\to}  f(U)
     $$

=--

The equivalence of the conditions on [[tangent space]] with the conditions on [[open subset]]s follows by the [[inverse function theorem]].

+-- {: .num_remark}
###### Remark

An analogous characterization of [[étale morphisms]] between [[affine algebraic varieties]] is given by [[tangent cones]]. See there.

=--

## Properties

### General

* A local diffeomorphism is a [[local homeomorphism]] and so also an [[open map]]. By the [[inverse function theorem]].

### Abstract characterization

The [[category]] [[SmoothMfd]] of [[smooth manifold]]s may naturally be thought of as sitting inside the more general context of the [[cohesive (∞,1)-topos]] [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s. This is canonically equipped with a notion of [[differential cohesion]] exhibited by its inclusion into [[SynthDiff∞Grpd]]. This implies that there is an intrinsic notion of [[formally étale morphism]]s of smooth $\infty$-groupoids in general and of smooth manifolds in particular

+-- {: .num_prop}
###### Proposition

A [[smooth function]] is a [[formally étale morphism]] in this sense precisely if it is a local diffeomorphism.

=--

See <a href="http://nlab.mathforge.org/nlab/show/synthetic+differential+infinity-groupoid#StructureSheaves">this section</a> for more details.

## Related concepts

* [[immersion of smooth manifolds|immersion]], [[submersion]]

## References

Discussion in the [[synthetic differential geometry]] of the [[Cahiers topos]] is in 


* {#KhavkineSchreiber17} [[Igor Khavkine]], [[Urs Schreiber]], around def. 3.1 of_[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))


[[!redirects local diffeomorphisms]]