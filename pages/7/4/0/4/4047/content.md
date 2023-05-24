
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

## Idea

A **ribbon category** &lbrack;[Reshetikhin & Turaev (1990)](#ReshetikhinTuraev90)&rbrack; (also called a **tortile category** &lbrack;[Joyal & Street (1993)](#JoyalStreet93)&rbrack; or **balanced rigid braided tensor category**) is a [[monoidal category]] $(\mathcal{C}, \otimes, \mathbb{1}, \alpha, l, r)$ equipped with [[braiding]] $\beta=\{\beta_{X,Y}\}$, twist $\theta=\{\theta_X\}$ and duality $(\vee, b, d)$ that satisfy some compatibility conditions. 

## Definition

A [[braided monoidal category]] is a [[monoidal category]] $\mathcal{C}$ equipped with a [[braiding]] $\beta$, which is a [[natural isomorphism]] $\beta_{X,Y}\colon X \otimes Y \to Y \otimes X$ obeying the [[hexagon identities]].

A braided monoidal category is *[[rigid monoidal category|rigid]]* if, for every [[object]] $X$, there exist objects $X^{\vee}$ and ${^{\vee}}X$ (called its [[dualisable object|right and left dual]]) and associated morphisms
$$b_X:\mathbb{1}\to X\otimes X^{\vee}, d_X: X^{\vee}\otimes X\to \mathbb{1}$$
$$b_X:\mathbb{1}\to {^{\vee}}X\otimes X, d_X: X\otimes {^{\vee}}X\to \mathbb{1}$$
obeying the zig-zag identities.

A **twist** on rigid braided monoidal category is a [[natural isomorphism]] from the [[identity functor]] to itself, with components $\theta_X \colon X \to X$ for which
$$\theta_{X\otimes Y}=\beta_{Y,X}\beta_{X,Y}\theta_{X}\otimes \theta_{Y},$$
$$\theta_{\mathbb{1}}=\mathrm{id},$$
$$\theta_{X^{\vee}}=\theta_{X}^{\vee}.$$

A ribbon category is a rigid braided monoidal category equipped with such a twist.

## Related concepts

* [[modular tensor category]]


## Reference

* {#ReshetikhinTuraev90} [[Nicolai Reshetikhin]], [[Vladimir Turaev]], *Ribbon graphs and their invariants derived from quantum groups*, Commun. Math. Phys. **127** 1 (1990) &lbrack;[doi:10.1007/BF02096491](https://doi.org/10.1007/BF02096491)&rbrack;

* {#JoyalStreet93} [[André Joyal]], [[Ross Street]], *Braided tensor categories*, Advances in Mathematics **102** (1993) 20–78 &lbrack;[doi:10.1006/aima.1993.1055](https://doi.org/10.1006/aima.1993.1055)&rbrack;

* [[Mei Chee Shum]], *Tortile tensor categories*, Journal of Pure and Applied Algebra **93** 1 (1994) 57-110 &lbrack;<a href="https://doi.org/10.1016/0022-4049(92)00039-T">10.1016/0022-4049(92)00039-T</a>&rbrack;


[[!redirects ribbon category]]
[[!redirects ribbon categories]]
[[!redirects tortile category]]
[[!redirects tortile categories]]
[[!redirects tortile monoidal category]]
[[!redirects tortile monoidal categories]]
