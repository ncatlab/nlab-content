

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--


\tableofcontents


## Idea 

The *Atiyah-Jänich theorem* ([Atiyah 1967 Thm A1](#Atiyah67), [Jänich 1965](#Jänich65)) states that the space of [[Fredholm operators]] $Fred(\mathscr{H})$ on a (countably infinite-dimensional [[separable Hilbert space|separable]], [[complex vector space|complex]]) [[Hilbert space]] $\mathscr{H}$ is a [[classifying space]] for [[topological K-theory]] $K(-)$:

For $X$ a [[compact Hausdorff space]], the [[homotopy classes]] of [[continuous maps]] from $X$ (hence the [[connected components]] of the [[mapping space]]) to $Fred(\mathscr{H})$ are in [[natural bijection]] with $K(X)$

$$
  \pi_0 \, 
  Map\big(
    X,
    \,
    Fred(\mathscr{H})
  \big)
  \xrightarrow[\sim]{ind_X}
  K(X)
  \,,
$$

where $ind_X$ forms the *index bundle*, an $X$-parameterized enhancement of the [[Fredholm index]].

This relation generalizes to a definition of [[twisted K-theory]] and of [[equivariant K-theory]] (hence of [[twisted equivariant K-theory]]) as given by homotopy classes of [[sections]] of $Fred(\mathscr{H})$-[[fiber bundles]] ([Atiyah & Segal 2004](#AtiyahSegal04)).


## References

The original articles:

* {#Atiyah67}  [[Michael Atiyah]], Thm. A1 in: *K-theory*, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin (1967) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]]&rbrack;

* {#Jänich65} [[Klaus Jänich]]: *Vektorraumbündel und der Raum der Fredholm-Operatoren*, Mathematische Annalen **161** (1965) 129–142 &lbrack;[doi:10.1007/BF01360851](https://doi.org/10.1007/BF01360851)&rbrack;

In monographs:

* {#Karoubi} [[Max Karoubi]], §7.10 in: _K-Theory -- An Introduction_, Grundlehren der mathematischen Wissenschaften **226**, Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3)&rbrack;

Lecture notes:

* Arshay Sheth: *The Atiyah-Jänich Theorem* &lbrack;[pdf](https://warwick.ac.uk/fac/sci/maths/people/staff/sheth/report_talk12_arshaysheth.pdf), [[Sheth-AtiyahJanich.pdf:file]]&rbrack;

As the basis of a definition of [[twisted K-theory]] and [[equivariant K-theory]] and [[twisted equivariant K-theory]]:

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], _Twisted K-theory_, Ukrainian Math. Bull. **1** 3 (2004) &lbrack;[arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf)&rbrack;

[[!redirects Atiyah-Janich theorem]]
[[!redirects Atiyah-Jaenich theorem]]
