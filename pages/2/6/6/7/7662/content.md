
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

given by composing the action of the [[covariant derivative]] on [[sections]] with the [[symbol map]]. This is an [[elliptic operator]]. The [[index of a Dirac operator|index]] of this operator is called the **$\hat A$-[[genus]]**.

### In terms of the universal $Spin$-orientation of $KO$

More abstractly, there is the universal [[orientation in generalized cohomology]] of [[KO]] over [[spin structure]], known as the [[Atiyah-Bott-Shapiro orientation]], which is a [[homomorphism]] of [[E-∞ rings]] of the form

$$
  M Spin \longrightarrow \pi_\bullet(KO)
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

## Related entries

* [[index of an elliptic complex]]

[[!include genera and partition functions - table]]



## References

The $\hat A$-genus as the index of the spin complex is discussed for instance in section 3 of

* [[Peter Gilkey]], _The Atiyah-Singer Index Theorem -- Chapter 5_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/gilkey3.pdf))
 {#Gilkey}

The relation of the characteristic series to the [[Bernoulli numbers]] is made explicit for instance in prop. 10.2 of

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

A construction via a [[1-dimensional Chern-Simons theory]] is in

* [[Owen Gwilliam]], [[Ryan Grady]], _One-dimensional Chern-Simons theory and the $\hat A$-genus_ ([arXiv:1110.3533](http://arxiv.org/abs/1110.3533))




[[!redirects A-hat genera]]