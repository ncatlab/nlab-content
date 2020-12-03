

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### In terms of an operator index

For $X$ a [[smooth manifold]] of even [[dimension]] and with [[spin structure]], write $\mathcal{S}(X)$ for the [[spin bundle]] and 

$$
  \mathcal{S}(X) \simeq \mathcal{S}^+(X) \oplus \mathcal{S}^-(X)
$$

for its decomposition into [[chiral spinor]] bundles. For $(X,g)$ the [[Riemannian manifold]] structure and $\nabla$ the corresponding [[Levi-Civita connection|Levi-Civita]] [[spin connection]] consider the map

$$
  c \circ \nabla 
  \;\colon\;
  \Gamma(\mathcal{S}^+(X))
  \to 
  \Gamma(\mathcal{S}^-(X))
$$

given by [[composition|composing]] the action of the [[covariant derivative]] on [[sections]] with the [[symbol map]]. This is an [[elliptic operator]]. The [[index of a Dirac operator|index]] of this operator is called the **$\hat A$-[[genus]]**.

### In terms of the universal $Spin$-orientation of $KO$

More abstractly, there is the universal [[orientation in generalized cohomology]] of [[KO]] over [[spin structure]], known as the [[Atiyah-Bott-Shapiro orientation]], which is a [[homomorphism]] of [[E-∞ rings]] of the form

$$
  M Spin \longrightarrow KO
$$

from the universal [[spin structure]] [[Thom spectrum]]. The $\hat A$-genus 

$$
  \Omega_\bullet^{SO}\longrightarrow \pi_\bullet(KO)\otimes \mathbb{Q}
$$

is the corresponding homomorphism in [[homotopy groups]].


## Properties

### Characteristic series

The [characteristic series](genus#LogarithmAndCharacteristicSeries) of the $\hat A$-genus is

$$
  \begin{aligned}
    K_{\hat A}(e)
     & =
    \frac{z}{e^{z/2} - e^{-z/2}}
    \\
     &= 
    \exp\left(
       - \sum_{k \geq 2} \frac{B_k}{k} \frac{z^k}{k!}
     \right)
  \end{aligned}
  \,,
$$

where $B_k$ is the $k$th [[Bernoulli number]] ([Ando-Hopkins-Rezk 10, prop. 10.2](#AndoHopkinsRezk10)).

### Relation to the Todd genus
  {#RelationToTheToddGenus}

Given the [[complexfication]] of a  [[real vector bundle]] $\mathcal{X}$ to a [[complex vector bundle]] $\mathcal{E} \otimes \mathbb{C}$, the $\hat A$-class of $\mathcal{E}$ is the [[square root]] of the [[Todd class]] of $\mathcal{E} \otimes \mathbb{C}$ (e.g. [de Lima 03, Prop. 7.2.3](#deLima03)).


### As a Rozansky-Witten invariant

+-- {: .num_prop #RozanskyWittenWilsonLoopOfUnknotIsSquareRootOfAHat}
###### Proposition
**([[Rozansky-Witten Wilson loop of unknot is A-hat genus|Rozansky-Witten Wilson loop of unknot is square root of A-hat genus]])**

For $\mathcal{M}^{4n}$ a [[hyperkähler manifold]] (or just a [[holomorphic symplectic manifold]]) the [[Rozansky-Witten invariant]] [[Wilson loop observable]] associated with the [[unknot]] in the [[3-sphere]] is the [[square root]] $\sqrt{{\widehat A}(\mathcal{M}^{4n})}$ of the [[A-hat genus]] of $\mathcal{M}^{4n}$.

=--

This is [Roberts-Willerton 10, Lemma 8.6](Rozansky-Witten+Wilson+loop+of+unknot+is+A-hat+genus#RobertsWillerton10), using the [[Wheels theorem]] and the [[Hitchin-Sawon theorem]].


## Related entries

* [[Todd genus]]

* [[index of an elliptic complex]]

[[!include genera and partition functions - table]]



## References

The $\hat A$-genus as the index of the spin complex is discussed for instance in:

* {#Gilkey} [[Peter Gilkey]], Section 3 of: _The Atiyah-Singer Index Theorem -- Chapter 5_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/gilkey3.pdf))

* {#deLima03} Levi Lopes de Lima, _The Index Formula for Dirac operators: an Introduction_, 2003 ([pdf](https://impa.br/wp-content/uploads/2017/04/PM_10.pdf)) 

The relation of the characteristic series to the [[Bernoulli numbers]] is made explicit for instance in prop. 10.2 of

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

A construction via a [[1-dimensional Chern-Simons theory]] is in

* [[Owen Gwilliam]], [[Ryan Grady]], _One-dimensional Chern-Simons theory and the $\hat A$-genus_ ([arXiv:1110.3533](http://arxiv.org/abs/1110.3533))




[[!redirects A-hat genera]]