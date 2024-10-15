
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

In 2-dimensional [[quantum field theory]] (QFT), a TY category is thought to encode as a *symmetry category* what is nowadays known as a [[non-invertible symmetry]], where the [[objects]] of the category correspond to line [[defects]]. 

## Definition 

A Tambara-Yamagami category $TY(G)$ is defined as follows. 

Starting from a [[finite group]] $G$, consider the set $I=G\coprod \{m\}$. We construct $TY(G)$ by defining the simple objects as $\{U_g\}_{g\in G}\coprod \{U_m\}$. These have fusion rules:

* $U_{g}\otimes U_{g'}=U_{gg'}$
* $U_{g}\otimes U_m = U_m$
* $U_m\otimes U_g = U_m$
* $U_m\otimes U_m = \sum_{g\in G} U_g$

Unless stated otherwise, we assume the ground field of $TY(G)$ to be $\mathbb{C}$. It has been shown that the above fusion rules also admit categorification over the reals (see [Plavnik & Sanford & Sconce 2023](#PlavnikSanfordSconce2023)).

## Properties

It was shown by [Tambara & Yamagami (1998)] (#Tambara1998tensor) that these categories are classified by pairs $(\chi,\tau)$ for $\chi:G\times G\to \mathbb{C}^*$ a bicharacter, and $\tau$ a square root of $\frac{1}{|G|}$.

+-- {: .num_remark}
###### Remark
Since $\chi$ is symmetric and nondegenerate, $TY(G)$ exists only if $G$ is abelian. $TY(G)$ is not necessarily unique for a choice of $G$.
=--

+-- {: .num_prop}
###### Proposition
$TY(G)$ is a [unitary fusion category](unitary+fusion+category).
=--

This follows from ([Galindo & Hong & Rowell 2013, theorem 5.20](#GalindoHongRowell2013)).

+-- {: .num_prop}
###### Proposition
$TY(G)$ is a braided fusion category if and only if $G\cong\mathbb{Z}_{2}^{n}$.
=--

The above is due to ([Siehler 2000, theorem 1.2(1)](#Siehler2000)).

## Examples

* $TY(\mathbb{Z}_{2})$ is realised by two distinct unitary fusion categories (distinguished by the Frobenius-Schur indicator $\varkappa_{m}\in\{+1,-1\}$ of $m$), each of which admit $4$ distinct braidings. All $8$ of these unitary braided fusion categories (UBFCs) are [modular](modular+tensor+category). Two of the UBFCs with $\varkappa_{m}=+1$ are known as the Ising categories, while two of the UBFCs with $\varkappa_{m}=-1$ describe [$SU(2)$-anyons](su2-anyon) at level $k=2$.

* As worked out in [Tambara & Yamagami (1998)](#Tambara1998tensor), for $TY(\mathbb{Z}_2\times\mathbb{Z}_2)$, there are two possible choices of roots ($\tau=\pm\frac{1}{2}$), and two choices of classes of bicharacters. For $\tau=\frac{1}{2}$ and trivial bicharacter, $TY$ is the [[category of representations]] of the [[dihedral group]] $D_8$. For $\tau=-\frac{1}{2}$ and trivial character, this is the representation category of the [[quaternion group]] $Q_8$. For $\tau=\frac{1}{2}$ and nontrivial character, this is the representation category of the Kac-Paljutkin 8-dimensional [[Hopf algebra]]. The remaining choice does not correspond to the category of representations of a Hopf algebra (see also [[Tannaka duality]]). 


## References

* {#PlavnikSanfordSconce2023} Julia Plavnik, Sean Sanford, Dalton Sconce, *Tambara-Yamagami Categories over the Reals: The Non-Split Case*, preprint (2023) &lbrack;[arXiv:2303.17843](https://arxiv.org/abs/2303.17843)&rbrack;

* {#GalindoHongRowell2013} Cesar Galindo, Seung-Moon Hong, [[Eric Rowell]], *Generalized and Quasi-Localizations of Braid Group Representations*, International Mathematics Research Notices **2013(3)** (2013) 693-731 &lbrack;[doi:10.1093/imrn/rnr269](https://doi.org/10.1093/imrn/rnr269)&rbrack;

* {#Siehler2000} Jacob Siehler, *Braided Near-Group Categories*, preprint (2000) &lbrack;[arXiv:0011037](https://arxiv.org/abs/math/0011037)&rbrack;

* {#AnyonWiki} AnyonWiki, [List of small multiplicity-free fusion rings](http://www.thphys.nuim.ie/AnyonWiki/index.php/List_of_small_multiplicity-free_fusion_rings)

### General

Original articles:

* {#Tambara1998tensor} [[Daisuke Tambara]], [[Shigeru Yamagami]], *Tensor categories with fusion rules of self-duality for finite abelian groups*, Journal of Algebra **209**  (1998)  692-707 &lbrack;[doi:10.1006/jabr.1998.7558](https://doi.org/10.1006/jabr.1998.7558)&rbrack;
 

[[!redirects Tambara-Yamagami categories]]
