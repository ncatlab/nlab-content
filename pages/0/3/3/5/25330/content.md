
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Contents
* this block creates the table of contents, leave as is
{: toc}


## Idea

A **Tambara-Yamagami** (TY) category is a [[fusion category]] that may be regarded as a non-trivial extension of a category of $G$-[[graded vector spaces]], for $G$ a [[finite group]]. By nontrivial extension we mean that, even though it is constructed from a category of $G$-graded vector spaces, it itself cannot be presented as such. 

In 2-dimensional [[quantum field theory]] (QFT), a YT category is thought to encodes what is nowadays known as a *[[non-invertible symmetry]]*, where the [[objects]] of the category correspond to line [[defects]].

## Definition 

A Tambara-Yamagami category $TY(G)$ is defined as follows. 

Starting from a [[finite group]] $G$, consider the set $I=G\coprod \{m\}$. We construct $TY(G)$ by defining the simple objects as $\{U_g\}_{g\in G}\coprod \{U_m\}$. These have fusion rules:

* $U_{g}\otimes U_{g'}=U_{gg'}$
* $U_{g}\otimes U_m = U_g$
* $U_m\otimes U_g = U_g$
* $U_m\otimes U_m = \sum_{g\in G} U_g$


## Properties

It was shown by [Tambara & Yamagami (1998)] (#Tambara1998tensor) that these categories are classified by pairs $(\chi,\tau)$ for $\chi:G\times G\to \C^*$ a bicharacter, and $\tau$ a square root of $\frac{1}{|G|}$.


## Examples

(...)


## References

### General

Original articles:

* {#Tambara1998tensor} [[Daisuke Tambara]], [[Shigeru Yamagami]], *Tensor categories with fusion rules of self-duality for finite abelian groups*, Journal of Algebra **209**  (1998)  692-707 &lbrack;[doi:10.1006/jabr.1998.7558](https://doi.org/10.1006/jabr.1998.7558)&rbrack;


[[!redirects Tambara-Yamagami categories]]
