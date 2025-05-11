
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
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

A surprising parallel between classical [[Hodge theory]] and the theory of [[Galois representations]] was noted in the beginning of the 60's; shortly [[John Tate|Tate]] and [[Alexander Grothendieck|Grothendieck]] attempted to understand the topology of p-adic [[algebraic variety|varieties]] in light of this analogy.
A series of precise conjectures about p-adic Hodge theory was formulated by [[Jean-Marc Fontaine|Fontaine]] at the beginning of the 80's; three different proofs were proposed by [[Gerd Faltings|Faltings]], Niziol and [[Takeshi Tsuji|Tsuji]].
A significantly simpler approach was developed recently in works of [[Alexander Beilinson|Beilinson]] and [[Bhargav Bhatt|Bhatt]].

_This paragraph is translated from the abstract of ([Beilinson's Yaroslavly' lectures](#BeilinsonLectures2014))._

## Overview

_p-adic Hodge theory_ is the study of properties of p-adic (&#233;tale, de Rham, logarithmic crystalline) [[cohomology]] (and [[motives]]) of non-archimedean [[analytic spaces]]. The $p$-adic Hodge structure of a (proper or semi-stably compactified) p-adic analytic variety is essentially given by a relation between three important invariants of the given variety:

* p-adic de Rham cohomology equipped with the Hodge filtration,

* log-crystalline cohomology (of a potentially semi-stable model) equipped with its Frobenius and monodromy map,

* [[pro-étale cohomology]] of the extension of the given variety to a `chosen` algebraic closure of the base field, together with its natural action of the Galois group.

There is an "evident" isomorphism between p-adic de Rham cohomology and log-crystalline cohomology (both are given by a kind of differential calculus).

The main theorem of p-adic Hodge theory is that the datum of these two cohomologies and their relation
on the one side, and of pro-&#233;tale cohomology on the other side, mutually determine each other (once
equipped with their natural additional structures).

This result has been conjectured first by Grothendieck in the case of p-divisible
groups. He called it the `mysterious functor`. A conjecture generalizing this
statement to other kinds of ---algebraic--- p-adic varieties was formulated by
Jannsen in a particular case, and then grounded on the setting of [[p-adic periods]]
by Fontaine. After these important Breakthrough, the theory was fully developed by a long list of contributors (see `periodes p-adiques`, Ast&#233;risque for a first list). The comparison theorem was proved by many authors in various particular cases, and then in full generality (for algebraic varieties) by Faltings
using [[almost mathematics]].

During the last few years, there were interesting new developments.

If one works with rational coefficients (no torsion), one may get the isomorphism between both
structures in a geometric way (in an algebraic setting),
using Beilinson's approach, through (derived de Rham cohomology)[[de Rham complex]].

It is also possible to use Scholze's [[perfectoid spaces]]
and Faltings' [[almost mathematics]] to give a very elegant
proof of this theorem for proper (or more generally, semi-stably compactified) p-adic
(strict, i.e., rigid) analytic varieties. The fact that the classical result extends
to the analytic setting is essentially due (up to difficulties related to the resolution in finite characteristic, that are dealt with using Faltings' methods) to the fact that (proper) rigid analytic varieties always
have an integral model, given by a formal scheme over the ring of integers of the given
non-archimedean field.
The same proof may also extend to the non-strict situation by using a convenient base
extension, but this work has not yet been done.

The very important case of torsion coefficients has also been
addressed by Scholze in his setting, and by Bhatt, who gave a useful refinement
of Beilinson's construction. Remark that almost mathematical tools seem to be quite well adapted to the study of completed integral cohomology.

Scholze's original method involves the use of Witt vectors (already used in
Fontaine's definition of period rings), that were also
studied by Kedlaya and Liu in this Hodge theoretic context. This Witt vector
approach are interesting, but they seem to have the drawback of being
quite hard to globalize (including the archimedean norm in a context of
[[global Hodge theory]]).

It is quite clear to the experts that a nice way to overcome the difficulties that appear
when one uses Witt vectors would be to combine directly the (analytic) `derived de Rham`
approach of Beilinson and Bhatt to the `perfectoid and almost mathematics` approach of
Faltings and Scholze. Both approaches may be extended to the analytic setting using
overconvergent derived analytic spaces (see [[global analytic geometry]]).

One may say that almost geometrical derived methods could be useful to study integral completed cohomology, while usual derived geometric methods are quite
well adapted to the study of torsion phenomena in finite characteristic.

Indeed, as explained by Bhatt at the end of his paper, one may use derived de Rham cohomology
over $\Z$ to get a (non-archimedean) period ring isomorphism for an [[arithmetic variety]].

## Hodge-Tate decomposition

An early result in $p$-adic Hodge theory is the Hodge-Tate decomposition, which is a $p$-adic analogue of the Hodge decomposition in classical [[Hodge theory]]. Let $X$ be a smooth projective variety over $\mathbb{Q}_{p}$ (or more generally some finite extension of it). Let $\mathbb{C}_{p}$ be the [[p-adic complex numbers]]. Then we have

$$H^{k}(X_{\overline{\mathbb{Q}}_{p}},\mathbb{Q}_{p})\otimes_{\mathbb{Q}_{p}}\mathbb{C}_{p}=\bigoplus_{i+j=k} H^{i}(X,\Omega_{X/\mathbb{Q}}^{j})\otimes_{\mathbb{Q}}\mathbb{C}_{p}(-j)$$

## Comparison theorems

Central to modern $p$-adic Hodge theory are the comparison theorems that relate the [[de Rham cohomology]] and the [[étale cohomology]] of a smooth projective variety $X$ over $\mathbb{Q}_{p}$ (or more generally some finite extension of it), using the machinery of period rings, whose construction we will discuss in the next section.

For instance, tensoring with the de Rham period ring $B_{dR}$ gives us the following isomorphism between the de Rham and $p$-adic etale cohomology of $X$:

$$H_{\mathrm{dR}}^{i}(X)\otimes_{\mathbb{Q}_{p}} B_{\mathrm{dR}}=H_{\mathrm{et}}^{i}(X_{\overline{\mathbb{Q}}_{p}},\mathbb{Q}_{p})\otimes_{\mathbb{Q}_{p}} B_{\mathrm{dR}}$$

The ring $B_{dR}$ is equipped with a filtration and a Galois action. We have a way of recovering the de Rham cohomology from the $p$-adic etale cohomology by taking Galois invariants:

$$H_{\mathrm{dR}}^{i}(X)=(H_{\mathrm{et}}^{i}(X_{\overline{\mathbb{Q}}_{p}},\mathbb{Q}_{p})\otimes_{\mathbb{Q}_{p}} B_{\mathrm{dR}})^{\mathrm{Gal}_{\mathbb{Q}_{p}}}$$

Recovering the $p$-adic etale cohomology from the de Rham cohomology involves a different period ring, the crystalline period ring $B_{crys}$ (which is equipped with a Frobenius $\varphi$ in addition to a filtration and Galois action), and is only possible if $X$ has an integral model:

$$H_{\mathrm{et}}^{i}(X_{\overline{\mathbb{Q}}_{p}},\mathbb{Q}_{p})= \mathrm{Fil}^{0}(H_{\mathrm{dR}}^{i}(X)\otimes_{\mathbb{Q}_{p}} B_{\mathrm{crys}})^{\varphi=1}$$

## Construction of period rings

We now show how to construct $B_{dR}. $Let $\mathcal{O}_{\mathbb{C}_{p}}$ be the ring of integers of $\mathbb{C}_{p}$. We take the tilt $\mathbb{O}_{\mathbb{C}_{p}}^{\flat}$ of $\mathbb{O}_{\mathbb{C}_{p}}$, and take Witt vectors. The resulting ring $W(\mathbb{O}_{\mathbb{C}_{p}}^{\flat})$ is also called $A_{inf}(\mathcal{O}_{\mathbb{C}_{p}})$. It comes with a canonical map $\theta:A_{inf}(\mathcal{O}_{\mathbb{C}_{p}})\to \mathcal{O}_{\mathbb{C}_{p}}$. Inverting $p$ and taking the completion with respect to $\theta$ gives us the ring $B_{dR}^{+}$. There is a special element $t\in B_{dR}^{+}$ which we think of as the logarithm of the element $(1,\zeta,\zeta^{1/p},\ldots)$. Then we define $B_{dR}=B_{dR}^{+}[1/t]$.

Next we show how to construct $B_{crys}$. Once again we take $A_{inf}(\mathcal{O}_{\mathbb{C}_{p}})$ and invert $p$. Instead of completing with respect to $\theta$, as in the construction of $B_{dR}$, we take a generator $\omega$ of its kernel, and consider the ring $B_{crys}^{+}$ whose elements are power series of the form $\sum a_{n}\omega^{n}$ where the $a_{n}$'s are elements of $A_{inf}(\mathcal{O}_{\mathbb{C}_{p}})[1/p]$ which converge to $0$ as $n$ approaches infinity, with respect to the topology of $A_{inf}(\mathcal{O}_{\mathbb{C}_{p}})[1/p]$. Once again there will be an element $t$ as in the construction of $B_{dR}$; we define $B_{crys}=B_{crys}^{+}[1/t]$.

## Classification of $p$-adic Galois representations

We can abstract the concepts discussed above and take a p-adic Galois representation $V$ (without knowing, say, if it comes from some cohomology theory). We can then define

$$V_{dR}=(V\otimes B_{dR})^{\mathrm{Gal}_{\mathbb{Q}_{p}}}$$

If the dimension of $V$ is equal to the dimension of $V_{dR}$, we say that $V$ is _de Rham_. We can also apply this construction with $B_{crys}$ instead of $B_{dR}$; if the dimension stays the same we say that $V$ is _crystalline_.

## $p$-adic Hodge theory for rigid analytic spaces

[[Peter Scholze]] has developed a version of $p$-adic Hodge theory for [[rigid analytic spaces]] in [Scholze13](#Scholze13). It relies on the construction of period sheaves and develops a $p$-adic version of the [[Riemann-Hilbert correspondence]] as an intermediate step. 

## Related concepts

* [[Galois representation]]

* [[Fargues-Fontaine curve]]

* [[prismatic cohomology]]

## References

### Overview

[[Jacob Lurie]], _Lecture 1: Overview_, lecture notes from a learning seminar on the [[Fargues-Fontaine curve]], [pdf](https://www.math.ias.edu/~lurie/ffcurve/Lecture1-Overview.pdf)

### Introductory references

* Laurent Berger: _An Introduction to the Theory of $p$-adic Representations, [pdf](http://perso.ens-lyon.fr/laurent.berger/articles/article05.pdf)

* Oliver Brinon, [[Brian Conrad]]: *CMI Summer School Notes on $p$-adic Hodge Theory* (2009) &lbrack;[pdf](https://math.stanford.edu/~conrad/papers/notes.pdf), [[BrinonConrad-AdicHodgeTheory.pdf:file]]&rbrack;


Niziol's [[algebraic K-theory|K-theoretic]] proof:

* Wiesława Nizioł: _Crystalline conjecture via $K$-theory_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure 31.5 (1998): 659-681. [web](http://eudml.org/doc/82474).

### Beilinson-Bhatt approach

* [[Alexander Beilinson]], _p-adic periods and derived de Rham cohomology_, [arXiv:1102.1294](http://arxiv.org/abs/1102.1294).

* [[Alexander Beilinson]], _On the crystalline period map_, [arXiv:1111.3316](http://arxiv.org/abs/1111.3316).

* [[Bhargav Bhatt]], _p-adic derived de Rham cohomology_, [arXiv:1204.6560](http://arxiv.org/abs/1204.6560).

* [[Luc Illusie]], _Around the Poincar&#233; lemma, after Beilinson_ (Preliminary notes), 2013, [pdf](http://www.math.u-psud.fr/~illusie/derived-deRham3.pdf).

* {#BeilinsonLectures2014} [[Alexander Beilinson]], _p-adic Hodge theory_, lectures from Yaroslavl' summer school 2014, [videos](http://bogomolov-lab.ru/SHKOLA2014/talks/beilinson.html).

### $p$-adic Hodge theory for rigid analytic spaces

* {#Scholze13} [[Peter Scholze]], _p-adic Hodge theory for rigid-analytic varieties_, Forum of Mathematics, Pi, 1, e1 2013. [arXiv:1205.3463](https://arxiv.org/abs/1205.3463)

### $p$-adic absolute Hodge cohomology

* [[Frédéric Déglise]], Wiesława Nizioł: _On $p$-adic absolute Hodge cohomology and syntomic coefficients, I_, [arXiv:1508.02567](http://arxiv.org/abs/1508.02567).