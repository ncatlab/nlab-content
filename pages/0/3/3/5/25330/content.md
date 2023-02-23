# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

A **Tambara-Yamagami** (TY) category is a [[fusion category]] that may be regarded as a non-trivial extension of a category of $G$-graded vector spaces, for $G$ a finite group. By nontrivial extension we mean that, even though it is constructed from a category of $G$-graded vector spaces, it itself cannot be presented as such. In 2d QFT, it encodes what is nowadays known as a [[non-invertible symmetry]], where the objects of the category correspond to line defects.

## Definition 

A Tambara-Yamagami category $TY(G)$ is defined as follows. Starting from a finite group $G$, consider the set $I=G\coprod \{m\}$. We construct $TY(G)$ by defining the simple objects as $\{U_g\}_{g\in G}\coprod \{U_m\}$. These have fusion rules:

* $U_{g}\otimes U_{g'}=U_{gg'}$
* $U_{g}\otimes U_m = U_g$
* $U_m\otimes U_g = U_g$
* $U_m\otimes U_m = \sum_{g\in G} U_g$


## Properties

It was shown in ([Tambara 1998] (#Tambara1998tensor)) that these categories are classified by pairs $(\chi,\tau)$ for $\chi:G\times G\to \C^*$ a bicharacter, and $\tau$ a square root of $\frac{1}{|G|}$.


## Examples

(...)


## References

### General

Original articles:

*{#Tambara1998tensor} Tambara, Daisuke, and Shigeru Yamagami. "Tensor categories with fusion rules of self-duality for finite abelian groups." Journal of Algebra 209.2 (1998): 692-707.