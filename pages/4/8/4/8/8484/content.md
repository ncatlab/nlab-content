
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $\mathbf{k}$ be a [[field]] of [[characteristic]] 0 and $\lambda \in \mathbf{k}^*$. A **$\lambda$-Drinfeld associator**, or just **$\lambda$-associator**, is a [[grouplike element]] $\Phi(a,b)$ of the $\mathbf{k}$-[[associative algebra|algebra]] of [[formal power series]] in two non-commuting [[variables]] $a,b$ satisfying:

1. The pentagon equation 
$$
\Phi(t_{12} , t_{23} + t_{24} )\Phi(t_{13} + t_{23} , t_{34} ) = \Phi(t_{23} , t_{34} )\Phi(t_{12} + t_{13} , t_{24} + t_{34} )\Phi(t_{12} , t_{23} )
$$
in $\widehat{U(L_4)}$
2. the hexagon equation 
$$
\exp(\lambda a/2)\Phi(c,a)\exp(\lambda c/2)\Phi(b,c)\exp(\lambda b/2)\Phi(a,b)=1
$$

where $L_4$ is the fourth [[Drinfeld-Kohno Lie algebra]] and $c=-a-b$.

+-- {: .num_remark}
###### Remark

The set of "0-associators" is what is called the _[[Grothendieck-Teichmueller group]]_. This acts freely on the set of Drinfeld associators.

=--

## Relations with braided monoidal categories

These [[equations]] are modelled on the defining [[axioms]] of [[braided monoidal categories]]. Indeed, associators provides a universal way of constructing braided monoidal categories out of some [[Lie algebra|Lie algebraic]] data.

Drinfeld associators are also used to construct [[quasi-Hopf algebra|quasi-Hopf algebras]]. 

+-- {: .num_theorem}
###### Theorem

Let $(\mathfrak{g},t)$ be a metrizable [[Lie algebra]], that is a Lie algebra $\mathfrak{g}$ together with a non-degenerate symmetric $\mathfrak{g}$-invariant 2-tensor $t$. Then if $\Phi$ is a $\lambda$-associator and $\hbar$ a formal variable, then the action of 
$$
\Phi(\hbar (t \otimes 1),\hbar (1\otimes t)) \in U(\mathfrak{g})^{\otimes 3}[[\hbar]]
$$
 and $e^{\hbar \lambda t/2}\circ P$ turns the category of $U(\mathfrak{g} ) [ [ \hbar ] ] $ module into a braided monoidal category, where $P$ is the flip: $P(a\otimes b)=b\otimes a$.
=--

+-- {: .num_remark}
###### Remark

Examples of metrizable Lie algebras are provided by [[simple Lie algebras]], in which case $t$ is a scalar mutliple of the [[Killing form]]. The braided monoidal category obtained this way is equivalent to that constructed from the corresponding [[quantum group]], by the [[Drinfeld-Kohno theorem]].

=--

##Existence##
An explicit associator over $\mathbf{C}$ was constructed by [[Drinfeld]] from the [[monodromy]] of a universal version of the [[Knizhnik-Zamolodchikov equation]]. Using the non-emptiness of the set of associators, and the fact that is is a [[torsor]] under the [[action]] of the 
[[Grothendieck-Teichmueller group]], he show that associators over $\mathbf{Q}$ also exists.

##Applications##
* [[Drinfeld-Kohno theorem]]
* [[Etingof-Kazhdan quantization functor]]
* [[Formality]] of the [[little 2-disk operad]]
* Construction of a functorial [[universal finite type invariant]]
* [[dilogarithm]] 
* [[Hausdorff series]], [[Kashiwara-Vergne conjecture]]

## References

* [[Vladimir Drinfeld]]. On quasitriangular quasi-Hopf algebras and on a group that is closely connected with Gal($\overline{\mathbf{Q}}/\mathbf{Q}$). _Leningrad Math. J._ 2:4 (1990), 829–860. ([mathnet.ru](http://mi.mathnet.ru/eng/aa199))
* [[Dror Bar-Natan]]. _On associators and the Grothendieck-Teichmuller group I._ Selecta Math. (N.S.)  4:2 (1998), 183–212. ([pdf](https://www.math.toronto.edu/drorbn/papers/GT1/GT1.pdf))
* A. Alekseev, C. Torossian, _The [[Kashiwara-Vergne conjecture]] and Drinfeld’s associators_, Ann. of Math. 175 (2012), no.2, 415–463 [pdf](http://www.math.jussieu.fr/~torossian/AT1.pdf);  _Kontsevich deformation quantization and flat connections_ [arxiv/0906.0187](https://arxiv.org/abs/0906.0187) [doi](https://doi.org/10.1007/s00220-010-1106-8)
* A. Alekseev, B. Enriques, C. Torossian, _Drinfeld associators, braid groups and explicit solutions of the Kashiwara-Vergne equations_, Publ. Math. Inst. Hautes ́Etudes Sci. 112 (2010), 143--189 [arxiv/0903.4067](https://arxiv.org/abs/0903.4067)
* [[Anton Alekseev]], Florian Naef, Xiaomeng Xu, Chenchang Zhu, _Chern–Simons, Wess–Zumino and other cocycles from Kashiwara–Vergne and associators_, Letters in Mathematical Physics __108__:3 (2018) 757–778 [doi](https://doi.org/10.1007/s11005-017-0985-4)

[[!redirects Drinfeld associators]]