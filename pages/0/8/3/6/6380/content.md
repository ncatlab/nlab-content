
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

Every [[variety]] in positive [[characteristic]] has a [[formal group]] attached to it, called the _Artin-Mazur formal group_. This group is often related to arithmetic properties of the variety such as being ordinary or supersingular.

The Artin-Mazur formal group in dimension $n$ is a [[formal group]] version of the [[Picard infinity-group|Picard n-group]] of flat/holomorphic [[circle n-bundles]] on the given variety. Therefore for $n = 1$ one also speaks of the _[[formal Picard group]]_ and for $n = 2$ of the _[[formal Brauer group]]_.


## Definition

Let $X$ be a [[smooth scheme|smooth]] [[proper scheme|proper]] $n$ [[dimension|dimensional]] [[variety]] over an [[algebraically closed field]] $k$ of positive [[characteristic]] $p$. Define the [[functor]] $\Phi: Art_k\to Grp$ by $\Phi(S)=\mathrm{ker}(H^n_{et}(X\otimes S, \mathbb{G}_m)\to H^n_{et}(X, \mathbb{G}_m))$. It is a fundamental result of the [paper of Artin and Mazur](#ArtinMazur) that under these hypotheses the functor is [[prorepresentable functor|prorepresentable]] by a one-dimensional [[formal group]]. This is known as the **Artin-Mazur formal group** .


## Examples

For a [[curve]], this group is often called the **[[formal Picard group]]** $\widehat{\mathrm{Pic}}$.

For a [[surface]], this group is called the **[[formal Brauer group]]** $\widehat{Br}$.


## Related concepts

* [[formal group]]

* [[height of a variety]]


## References

The original article is

* {#ArtinMazur77} [[Michael Artin]], [[Barry Mazur]], _Formal Groups Arising from Algebraic Varieties_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 1 (1977), p. 87-131  [numdam](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663)
 
Further developments are in 

* {#Stienstra87} [[Jan Stienstra]], _Formal group laws arising from algebraic varieties_, American Journal of Mathematics, Vol. 109, No.5 (1987), 907-925 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/stienstra1.pdf))


Lecture notes touching on the cases $n = 1$ and $n = 2$ include

* {#Liedtke14} Christian Liedtke, example 6.13 in _Lectures on Supersingular K3 Surfaces and the Crystalline Torelli Theorem_ ([arXiv.1403.2538](http://arxiv.org/abs/1403.2538))

Discussion of Artin-Mazur formal group for all $n$ of [[Calabi-Yau varieties]] of positive [[characteristic]] in dimension $n$ is in 

* {#GeerKatsura03} [[Gerard van der Geer]], T. Katsura, _On the height of Calabi-Yau varieties in positive characteristic_ ([arXiv:math/0302023](http://arxiv.org/abs/math/0302023))



[[!redirects Artin-Mazur formal group]]
[[!redirects Artin-Mazur formal groups]]
[[!redirects Artin–Mazur formal group]]
[[!redirects Artin–Mazur formal groups]]
[[!redirects Artin--Mazur formal group]]
[[!redirects Artin--Mazur formal groups]]