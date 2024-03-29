+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
#### Functional analysis
### Contents {: .clickToReveal}
### Contents {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

This page is inspired by the following question, which appeared [on MathOverflow](http://mathoverflow.net/questions/79713/lp-mathbbr-vs-lq-mathbbr).

> Let $p,q \in (1,\infty)$ with $p\neq q$.  Are the [[Banach spaces]] $L^p(\mathbb{R})$, $L^q(\mathbb{R})$  [[norm isomorphism|isomorphic]]?

More generally, one can ask:

> Given two [[Banach spaces]], $X$ and $Y$, when are they [[norm isomorphism|isomorphic]]?

The following started out as an adapted version of Bill Johnson's answer to the MathOverflow question.

One way to prove that a [[Banach space]] $X$ is not [[norm isomorphism|isomorphic]] to a Banach space $Y$ is to exhibit a property which is preserved under isomorphisms that $X$ has but $Y$ does not.  For example, among the spaces $L_p(\mathbb{R})$ for $p \in [1,\infty]$, $L_\infty$ is the only nonseparable space, and $L_1$ is the only separable space with a nonseparable dual.  Thus $L_1$ and $L_\infty$ are not isomorphic to each other or to any $L_p$ with $p \in (1,\infty)$.  

To distinguish among the $L_p$ with $p \in (1,\infty)$ finer properties are needed.
[[type (functional analysis)|Type]] and [[cotype (functional analysis)|cotype]] are examples of such properties.  The [[type (functional analysis)|(best) type]] and [[cotype (functional analysis)|cotype]] of $L_p$ are standard calculations: if $p \in [1,2]$ then $L_p$ has type $p$ and cotype $2$ (and no better), and if $p \in [2,\infty)$ then $L_p$ has type $2$ and cotype $p$ (and no better). See for example in Theorem 6.2.14 of [AK06](#AK06).  From that, one can see that if $p \ne q$, then $L_p$ and $L_q$ either have different (best) type or different (best) cotype.

Type and cotype depend only on the collection of finite dimensional subspaces of a space (we call such a property a [[local property]]).  So neither can be used to prove, e.g., that for $p \ne 2$, $L_p$ is not isomorphic to $\ell_p$.  One way of proving this is to show that for $p \ne 2$, $\ell_2$ embeds isomorphically into $L_p$ but not into $\ell_p$ (see also [AK](#AK)).


### References ###

* {: #AK06 } **AK06** Albiac, Fernando and Kalton, Nigel.
Topics in Banach space theory.
Graduate Texts in Mathematics, 233. Springer, New York, 2006. xii+373 pp. ISBN: 978-0387-28141-4; [MR2192298](http://www.ams.org/mathscinet-getitem?mr=2192298)