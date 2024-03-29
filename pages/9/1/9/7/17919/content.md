
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
##### Fusion categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Let $\mathcal{C}$ be a [[semisimple category|semisimple]] [[linear category|linear]]([[Vect]]-[[enriched category|enriched]]) (over a field $k$) category and $G$ a finite group.
A **$G$-grading** on $\mathcal{C}$ is a direct sum decomposition of $\mathcal{C}$ into _homogeneous components_ $\mathcal{C}_g$, which are again $k$-linear semisimple categories:

$$\mathcal{C} \simeq \bigoplus_{g \in G} \mathcal{C}_g$$


=--

+-- {: .num_defn}
###### Definition

A **graded fusion category** is a fusion category with a chosen $G$-grading for some group, such that the monoidal product maps $\mathcal{C}_g \times \mathcal{C}_h$ into $\mathcal{C}_{g h}$.

=--

+-- {: .num_defn}
###### Alternative Definition

Let $\Lambda_\mathcal{C}$ be the set of equivalence classes of simple objects in $\mathcal{C}$.
A $G$-grading is a map $\operatorname{deg}\colon \Lambda_\mathcal{C} \to G$ such that for any two simples $X$ and $Y$ and any simple subobject $Z \hookrightarrow X \otimes Y$, we have $\operatorname{deg}([Z]) = \operatorname{deg}([X]) \operatorname{deg}([Y])$.


=--

## Terminology

* The trivial component $\mathcal{C}_1$ of the grading is a full fusion subcategory.
* A $G$-extension of a fusion category $\mathcal{D}$ is a $G$-graded fusion category $\mathcal{C}$ such that $\mathcal{D} \simeq \mathcal{C}_1$.
* A grading is faithful if $\mathcal{C}_g \neq 0$ for all $g \in G$. This is a standard assumption.
* The __adjoint category__ $\mathcal{C}_{\text{ad}}$ is the full fusion subcategory of $\mathcal{C}$ spanned by objects of the form $X \otimes X^*$.

## Examples

* Every fusion category has the trivial grading from the trivial group.
* $G$-graded vector spaces for a finite group $G$ are naturally a graded fusion category.
* The universal grading, see below.
* [[$G$-crossed braided fusion categories]] are a (kind of) [[categorification]] of [[crossed module]]s, and therefore carry a grading as part of the data.

## Universal grading

From the definition, it is clear that gradings are covariant in the group.
A group homomorphism $\phi\colon G \to H$ gives an obvious map of the set of gradings:

$$ \mathcal{C} \simeq \bigoplus_{h \in H} \bigoplus_{g \in \phi^{-1}(h)} \mathcal{C}_g $$

or

$$ \operatorname{deg}_H = \phi \circ \operatorname{deg}_G $$

Morphisms of gradings are therefore simply group homomorphisms.

For every fusion category $\mathcal{C}$, there exists a universal grading by a group $U_\mathcal{C}$.
It has the following properties:

* It is faithful.
* The trivial component is the full fusion subcategory spanned by objects of the form $X \otimes X^*$.
* Every full fusion subcategory $\mathcal{D} \subset \mathcal{C}$ containing the adjoint category $\mathcal{C}_{\text{ad}}$ is of the form $\mathcal{D} \simeq \bigoplus_{h \in H} \mathcal{C}_h$ for some subgroup $H \subset U_\mathcal{C}$.
* The group of monoidal automorphisms of the identity functor is canonically isomorphic to $\operatorname{Hom}(U_\mathcal{C}, k^\times)$.

## References ##

* Shlomo Gelaki, Dmitri Nikshych, [Nilpotent fusion categories](https://arxiv.org/abs/math/0610726)
* [[Pavel Etingof]], Dmitri Nikshych, Victor Ostrik, with an appendix by Ehud Meir, [Fusion categories and homotopy theory](https://arxiv.org/abs/0909.3140v2)
* Vladimir Drinfeld, Shlomo Gelaki, Dmitri Nikshych, Victor Ostrik, [On braided fusion categories I](https://arxiv.org/abs/0906.0620)

[[!redirects graded fusion categories]]