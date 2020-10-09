
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
#### Linguistics
+-- {: .hide}
[[!include linguistics - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

**Generalized quantifiers** were introduced into [[model theory]] by the Polish logician A. Mostowski in order to supplement the usual [[existential quantifier|existential]] and [[universal quantifiers]] of [[first-order logic|first-order predicate logic]] with the aim to circumvent shortcomings concerning expressivity and categoricity.

Their subsequent use for the [[semantics|semantic]] analysis of natural language determiners in the footsteps of [[Richard Montague]] revolutionized [[linguistics]] in the early 1970s.

## Definition

+-- {: .num_defn #GeneralizedQuantifier}
###### Definition

A _generalized quantifier_ or an _interpretation of a quantifier symbol_ $Q$ is a mapping $\mu_Q$ from triples of cardinal numbers $\langle \mathfrak{m},\mathfrak{n},\mathfrak{p}\rangle$ such that $\mathfrak{m}+\mathfrak{n}=\mathfrak{p}$ to $\Omega=\{0,1\}$. The satisfaction relation for $Q$ is defined for structures $\mathfrak{A}$ with carrier $A$ and valuation $x$ by

$$
\begin{aligned}
\mathfrak{A}\models_x(Qv_n)\phi\quad&{iff}\quad \mu_Q(\mathfrak{m},\mathfrak{n},\mathfrak{p})=1\;,\; with
\\
\mathfrak{m}&=card(\{a\in A:\mathfrak{A}\models_{x(n/a)}\phi\})
\\
\mathfrak{n}&=card(\{a\in A:\mathfrak{A}\models_{x(n/a)}\not\phi\})
\\
\mathfrak{p}&=card(A)\;.
\end{aligned}
$$

=--

## Examples

* The [[universal quantifier]] $\forall$ has $\mu_\forall(\mathfrak{m},\mathfrak{n},\mathfrak{p})=1$ iff $\mathfrak{n}=0$.

* The quantifier $Q_\alpha$ "there exist at least $\aleph_\alpha$" is given by $\mu_{Q_\alpha}(\mathfrak{m},\mathfrak{n},\mathfrak{p})=1$ iff $\mathfrak{m}\geq\aleph_{\alpha}\;$.

* The quantifier $\mathsf{W}$ "most" is given by $\mu_{\mathsf{W}}(\mathfrak{m},\mathfrak{n},\mathfrak{p})=1$ iff $\mathfrak{m}\gt\mathfrak{n}\;$. Note that this uses the second variable as well, whereas $\forall$ or $Q_\alpha$ depend only on $card(\{a\in A:\mathfrak{A}\models_{x(n/a)}\phi\})$.

## Related entries

* [[model theory]]

* [[second-order logic]]

* [[cardinal number]]

* [[Lawvere distribution]]

* [[Richard Montague]]


## References

Generalized quantifiers were introduced in

* A. Mostowski, _On a Generalization of Quantifiers_ , Fund. Math. **44** (1957). ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm44/fm4412.pdf))

An early textbook account is in ch.13 of

* {#BellSlomson}[[John Bell|J. L. Bell]], A. B. Slomson, _Models and Ultraproducts: An Introduction_ , North-Holland Amsterdam 1969. (Dover reprint)

Several chapters treat their model-theoretic role in

* J. Barwise, [[Solomon Feferman|S. Feferman]] (eds.), _Model-theoretic Logics_ , Springer Heidelberg 1985 (freely available online: [toc](http://projecteuclid.org/euclid.pl/1235417263#toc)) .

In the context of [[Martin-Löf type theory]] they are discussed by

* G. Sundholm, _Constructive Generalized Quantifiers_ , Synthese **79** no.1 (1989) pp.1-12.

For the use of generalized quantifiers in natural language semantics see

* J. Barwise, R. Cooper, _Generalized Quantifiers and Natural Language_ , Linguistics and Philosophy **4** no.2 (1981) pp.159-219.

* E. Keenan, D. Paperno (eds.), _Handbook of Quantifiers in Natural Language _ , Springer 2012.

* E. Keenan, D. Paperno (eds.), _Handbook of Quantifiers in Natural Language: vol.2 _ , Springer 2017.

* E. Keenan, J. Stavi, _A semantic characterization of natural language determiners_ , Linguistics & Philosophy **9** (1986) pp.253–326.

* D. Westerståhl, _Generalized quantifiers: linguistics meets model theory_ , in Aloni, Dekker (eds.), _The Cambridge Handbook of Semantics_ , Cambridge UP 2014. ([draft](https://www.philosophy.su.se/polopoly_fs/1.165898.1391710202!/menu/standard/file/2013%20CambridgeHandbookGQ.pdf))

Some problems with the standard approach in linguistics are discussed in

* H. Ben-Yami, _Generalized Quantifiers, and Beyond_ , Logique Et Analyse no.208 (2009) pp.309-326.

* M. Hackl, _On the Grammar and Processing of Proportional Quantifiers: Most Versus More Than Half_ , Natural Language Semantics **17** no.1 (2009) pp.63-98.

A dependent type theoretic analysis of natural language generalized quantifiers is in

* T. Fernando, _Conservative generalized quantifiers and presupposition_ , Semantics and Linguistic Theory **XI** (2001) pp.172–91. ([draft](http://www.scss.tcd.ie/Tim.Fernando/cgq.pdf))

They are modelled in compact closed categories in

* J. Hedges, [[Mehrnoosh Sadrzadeh|M. Sadrzadeh]], _A Generalised Quantifier Theory of Natural Language in Categorical Compositional Distributional Semantics with Bialgebras_  , Math. Struc. Theor. Comp. Sci. 2019. ([link](https://www.cambridge.org/core/journals/mathematical-structures-in-computer-science/article/generalised-quantifier-theory-of-natural-language-in-categorical-compositional-distributional-semantics-with-bialgebras/9738AE3A40B9A51AE2134D13E4FD3C5B))

[[!redirects Generalized quantifier]]
[[!redirects Generalized Quantifier]]
[[!redirects generalized quantifiers]]
[[!redirects Generalized quantifiers]]
[[!redirects Generalized Quantifiers]]
[[!redirects generalised quantifier]]
[[!redirects Generalised quantifier]]
[[!redirects Generalised quantifiers]]
[[!redirects Generalised Quantifier]]