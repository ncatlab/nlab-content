
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

## Definition

+-- {: .num_defn }
###### Definition

For $C$ a [[symmetric monoidal (infinity,n)-category|symmetric monoidal (infinity,2)-category]], a **Calabi-Yau object** in $C$ is

* a dualizable object;

* a morphism $\eta : dim(X) : ev_X \circ circoev_X \to Id_x$ in $\Omega_x C$ which is equivariant with respect to the canonical action of the [[circle group]] on $dim(X)$ and which is the [[unit of an adjunction|counit]] for an [[adjunction]] between $ev_X$ and $coev_X$.

=--

This is ([Lurie, def. 4.2.6](#Lurie)). 

## Examples

### Calabi-Yau algebras
 {#CYAlgebra}

+-- {: .num_example }
###### Example

Let $\mathbf{S}$ be a [good]() [[symmetric monoidal (∞,1)-category]]. Write $Alg(\mathbf{S})$ for the [[symmetric monoidal (∞,n)-category|symmetric monoidal (∞,2)-category]] whose [[object]]s are [[algebra in an (∞,1)-category|algebra objects]] in $\mathbf{S}$ and whose [[morphism]]s are [[bimodule]] objects. 

Then a Calabi-Yau object in $Alg(\mathbf{S})$ is an algebra object $A$ equipped with an $SO(2)$-equivariant morphism

$$
  tr : \int_{S^1} A \to 1
$$ 

satisfying the condition that the composite morphism

$$
  A \otimes A \simeq \int_{S^0} A \to \int_{S^1} A \stackrel{tr}{\to} 1
$$

exhibits $A$ as its own dual $A^\vee$.

Such an algebra object is called a [[Calabi-Yau algebra]] object.

=--

This is ([Lurie, example 4.2.8](#Lurie)).

## Properties

A version of the [[cobordism hypothesis]] says that symmetric monoidal $(\infty,2)$-functors 

$$
  Z : Bord_2^{nc} \to \mathcal{C}
$$

out of a version of the [[(infinity,n)-category of cobordisms|(infinity,2)-category of cobordisms]] where all 2-cobordisms have at least one outgoing (ingoing) boundary component, are equivalently given by their value on the point, which is a Calabi-Yau object in $\mathcal{C}$.

This is [Lurie, 4.2.11](#Lurie). 

This is closely related to the description of [[TCFT]]s ([Lurie, theorem 4.2.13](#Lurie)).

## Related concepts

* [[Calabi-Yau category]]

## References

Section 4.2 of 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_
 {#Lurie}

[[!redirects Calabi-Yau objects]]