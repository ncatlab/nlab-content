
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

## Idea

A **ribbon category**  (also called a **tortile category** or **balanced rigid braided tensor category**) is a monoidal category $(\mathcal{C}, \otimes, \mathbb{1}, \alpha, l, r)$ equiped with braiding $\beta=\{\beta_{X,Y}\}$, twist $\theta=\{\theta_X\}$ and duality $(\vee, b, d)$ which satisfy some compatible conditions. The name _ribbon category_ is introduced by Reshetikhin and Turaev in [their work](https://link.springer.com/article/10.1007/BF02096491) in 1990, the name _tortile category_ is used by Joyal and Street in [their work](https://www.sciencedirect.com/science/article/pii/S0001870883710558).

## Definition

A braided monoidal tensor category is a monoidal category $\mathcal{C}$ equipped with a braiding $\beta=\{\beta_{X,Y}\}$ which is a set of isomorphisms natual in $X$ and $Y$ and satisfies the hexogon relation.  

A braided tensor category $(\mathcal{C}, \otimes, \mathbb{1}, \alpha, l, r, \beta)$ is rigid if, for every object $X$, there exist objects $X^{vee}$ and ${^{\vee}}X$ (called right dual and left dual) and associated morphsims
$$b_X:\mathbb{1}\to X\otimes X^{\vee}, d_X: X^{\vee}\otimes X\to \mathbb{1}$$
$$b_X:\mathbb{1}\to {^{\vee}}X\otimes X, d_X: X\otimes {^{\vee}}X\to \mathbb{1}$$
which satisfy some consistency conditions. 

The twist on rigid braided tensor category is a set of isomorphism $\theta=\{\theta_X\}$ for which
$$\theta_{X\otimes Y}=\beta_{Y,X}\beta_{X,Y}\theta_{X}\otimes \theta_{Y},$$
$$\theta_{\mathbb{1}}=\mathrm{id},$$
$$\theta_{X^{\vee}}=\theta_{X}^{\vee}.$$


A ribbon category is a rigid braided Tensor category equiped with a twist.
## Reference
* N. Y. Reshetikhin and V. G. Turaev, Ribbon graphs and their invaraints derived from quantum groups, Commun.Math. Phys. (1990) 127: 1. https://doi.org/10.1007/BF02096491
* A. Joyal and R. Street, Braided tensor categories, Advances in Mathematics, 102: 20–78, doi:10.1006/aima.1993.1055

[[!redirects ribbon category]]
[[!redirects ribbon categories]]
[[!redirects tortile category]]
[[!redirects tortile categories]]
