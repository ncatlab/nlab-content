
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
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

A **graded fusion category** is a fusion category with a chosen $G$-grading for some group, such that the monoidal product maps $\mathcal{C}_g \times \mathcal{C}_h$ into $\mathcal{C}_{gh}$.

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

## Examples

* Every fusion category has the trivial grading from the trivial group.
* $G$-graded vector spaces for a finite group $G$ are naturally a graded fusion category.
* 