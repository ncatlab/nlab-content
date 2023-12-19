
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

See at _[cobordism hypothesis -- For non-compact cobordisms](cobordism+hypothesis#ForNoncompactCobordisms)_.

## Definition

+-- {: .num_defn }
###### Definition

For $C$ a [[symmetric monoidal (infinity,n)-category|symmetric monoidal (infinity,2)-category]], a **Calabi-Yau object** in $C$ is

* a [[dualizable object]] $X$;

* a morphism $\eta\colon\operatorname{dim}(X) \equiv ev_X \circ coev_X \longrightarrow Id_x$ in $\Omega_x C$ which is [[equivariance|equivariant]] with respect to [the canonical](cobordism%20hypothesis#TheCanonicalOnAction) [[∞-action]] of the [[circle group]] $SO(2)$ on $dim(X)$ and which is the [[unit of an adjunction|counit]] for an [[adjunction]] between the [[evaluation map]] $ev_X$ and [[coevaluation map]] $coev_X$.

=--

This is ([Lurie 09, def. 4.2.6](#Lurie09)). 

## Examples

### Calabi-Yau algebras
 {#CYAlgebra}

+-- {: .num_example }
###### Example

Let $\mathbf{S}$ be a [[good monoidal (∞,1)-category|good]] [[symmetric monoidal (∞,1)-category]]. Write $Alg(\mathbf{S})$ for the [[symmetric monoidal (∞,n)-category|symmetric monoidal (∞,2)-category]] whose [[object]]s are [[algebra in an (∞,1)-category|algebra objects]] in $\mathbf{S}$ and whose [[morphisms]] are [[bimodule]] objects. 

Then a Calabi-Yau object in $Alg(\mathbf{S})$ is an algebra object $A$ equipped with an $SO(2)$-equivariant morphism


$$
  tr \colon \int_{S^1} A \to 1
$$ 

from the [[Hochschild homology]] $\int_{S^1} A \simeq A \otimes_{A \otimes A} A$, satisfying the condition that the composite morphism

$$
  A \otimes A \simeq \int_{S^0} A \to \int_{S^1} A \stackrel{tr}{\to} 1
$$

exhibits $A$ as its own [[dual object]] $A^\vee$.

Such an algebra object is called a _[[Calabi-Yau algebra]] object_.

=--

This is ([Lurie 09, example 4.2.8](#Lurie09)).

## Properties

### Relation to extended 2d TQFT (TCFT) and the Cobordism hypothesis

A version of the [[cobordism hypothesis]] says that symmetric monoidal $(\infty,2)$-functors 

$$
  Z : Bord_2^{nc} \to \mathcal{C}
$$

out of a version of the [[(infinity,n)-category of cobordisms|(infinity,2)-category of cobordisms]] where all 2-cobordisms have at least one outgoing (ingoing) boundary component, are equivalently given by their value on the point, which is a Calabi-Yau object in $\mathcal{C}$.

This is ([Lurie 09, theorem 4.2.11](#Lurie09)). 

Here the trace condition translates to the [[cobordism]] which is the "disappearance of a circle". 

$$
  \array{
     && \longleftarrow
    \\
    & \swarrow && \nwarrow
    \\
    & \searrow && \nearrow
    \\
    && \longrightarrow
  }
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
   \ast
$$


Its would-be [[adjoint]], the "appearance of a circle" is not included in $Bord_2^{nc}$.

This is closely related to the description of [[2d TQFT]] as [[TCFT]]s ([Lurie 09, theorem 4.2.13](#Lurie09)).

[[!include 2d TQFT -- table]]

## Related concepts

* [[Calabi-Yau category]]

* [[3d Calabi-Yau object]]

## References


* {#Lurie09} [[Jacob Lurie]], section 4.2 of _[[On the Classification of Topological Field Theories]]_ ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))
 

[[!redirects Calabi-Yau objects]]