+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Idea

The generalization of [[Teichmüller theory]] to [[arithmetic geometry]] has been called _inter-universal Teichmüller theory_ (often abbreviated _IUTT_) by [[Shinichi Mochizuki]]. It is a part of [[anabelian geometry]].

{#InterUniversal} The term "inter-universal" apparently refers to the fact that the theory is meant to formulated explicitly in a way that respects [[universe enlargement]], hence that it is [[universe polymorphism|universe polymorphic]] ([IUTT IV, remark 3.1.4](#IUTTIV), [Yamashita 13](#Yamashita13)).

It is claimed ([IUTT IV](#IUTTIV)) that a proof of the [[abc conjecture]] can be given in IUTT. In 2018, a document [[why_abc_is_still_a_conjecture.pdf:file]] was written by [[Peter Scholze]] and [[Jakob Stix]] raising objections to the argument. 

## Overview of the proof

### Dénouement

The logic of the final part of Mochizuki's approach to the [[abc conjecture]] is fairly straightforward in outline, and not, as far we know, a point of contention. We describe it here, deliberately using completely different notation from the IUTT papers to bring out the structure of the argument. Throughout, we shall assume that we have certain data $\mathbb{M}$, which we shall treat as a black box.

\begin{assum} \label{AssumptionMainInequalityInIUTT} Given $\mathbb{M}$, there are [[real number | real numbers]] $t_{\mathbb{M}}$ and $q_{\mathbb{M}}$ such that $-t_{\mathbb{M}} \geq - q_{\mathbb{M}}$. \end{assum}

\begin{cor} \label{CorollaryInequalityForConstant} Given any real number $c_{\mathbb{M}}$ such that $-t_{\mathbb{M}} \leq c_{\mathbb{M}} \cdot  q_{\mathbb{M}}$, we have that $c_{\mathbb{M}} \geq -1$. \end{cor}

\begin{proof} Immediate. \end{proof} 

\begin{assum} \label{AssumptionConstantInvolvedInAbcConjecture} For a particular choice of $\mathbb{M}$, one can construct a $c_{\mathbb{M}}$ such that:

1. $-t_{\mathbb{M}} \leq c_{\mathbb{M}} \cdot q_{\mathbb{M}}$;
1. if $c_{\mathbb{M}} \geq -1$, then the abc conjecture holds.

\end{assum}

\begin{thm} The abc conjecture holds. \end{thm} 

\begin{proof} Follows immediately from Corollary \ref{CorollaryInequalityForConstant} and Assumption \ref{AssumptionConstantInvolvedInAbcConjecture}. \end{proof}

\begin{rmk} That Assumption \ref{AssumptionMainInequalityInIUTT} holds is the fundamental result of the IUTT series of papers. It is Corollary 3.12 in [IUTT III](#IUTTIII), and it is this corollary to which the objections raised by Scholze and Stix pertain.

That Assumption \ref{AssumptionConstantInvolvedInAbcConjecture} holds is the main purpose of [IUTT IV](#IUTTIV). It is established by Theorem 1.10 and Corollary 2.2. Theorem 1.10 establishes the particular inequality of the form $c_{\mathbb{M}} \geq -1$ that will be made use of; Corollary 2.2 specialises and refines it to an inequality which directly implies the abc conjecture. As far we know, these parts of the argument are expected to be sound.
\end{rmk}

## Related concepts

* [[anabelian geometry]]

* [[étale theta function]]

* [[Frobenioid]]

* [[initial Θ-data]]

* [[universe polymorphism]]

* [[poly-morphism]] (not to be be confused with [[polymorphism]])

## References

* {#IUTTI} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory I, Construction of Hodge theaters_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20I.pdf))

* {#IUTTII} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory II, Hodge-Arakelov-theoretic evaluation_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20II.pdf))

* {#IUTTIII} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory III, Canonical splittings of the Log-theta-lattice_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20III.pdf))

* {#IUTTIV} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory IV, Log-volume computations and set-theoretic foundations_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20IV.pdf))
 

Surveys include

* [[Shinichi Mochizuki]], _Panoramic overview of inter-universal Teichmuller theory_, [pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Panoramic%20Overview%20of%20Inter-universal%20Teichmuller%20Theory.pdf)


* {#Yamashita13} Go Yamashita, _FAQ on 'Inter-Universality'_ ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/FAQ%20on%20Inter-Universality.pdf))
 

* {#Fesenko15} [[Ivan Fesenko]], _Arithmetic deformation theory via arithmetic fundamental groups and nonarchimedean theta functions_, European Journal of Mathematics September 2015, Volume 1, Issue 3, pp 405-440 ([publisher](http://link.springer.com/article/10.1007/s40879-015-0066-0), [pdf](https://www.maths.nottingham.ac.uk/personal/ibf/notesoniut.pdf))

* [[Minhyong Kim]], _Brief superficial remarks on Shinichi Mochizuki's Interuniversal Teichmueller Theory (IUTT), version 1_, 10/11/2015, ([pdf](http://people.maths.ox.ac.uk/kimm/papers/pre-iutt.pdf)).

* [[Taylor Dupuy]], Hodge Theaters: _[A First Look at the Big Hodge Theater](https://www.youtube.com/watch?v=V_tWUswSUoo)_,  _[ Confused Groups and Torsors](https://www.youtube.com/watch?v=8yacRMVIIHs&list=PLJmfLfPx1OecDVF-VgXNeCfAlisy74PHt)_

*  [RIMS/Symmetries and Correspondences workshop](https://www.maths.nottingham.ac.uk/personal/ibf/files/kyoto.iut.html): _[Inter-universal Teichm&#252;ller Theory Summit 2016](https://www.maths.nottingham.ac.uk/personal/ibf/files/iut-kyoto-pr.html)_

* {#Morrow17} [[Jackson Morrow]], _Kummer classes and Anabelian geometry_, notes from Super [QVNTS](http://www.dms.umontreal.ca/%7Eqvnts/): [Kummer Classes and Anabelian Geometry](http://www.uvm.edu/%7Etdupuy/anabelian.html) 2017 ([pdf](https://www.dropbox.com/s/kiszgkrrsjrqu4p/VermontNotes_Final.pdf?dl=0))

* [[Taylor Dupuy]], Anton Hilado, _The Statement of Mochizuki's Corollary 3.12, Initial Theta Data, and the First Two Indeterminacies_, arXiv:[2004.13228](https://arxiv.org/abs/2004.13228)

* [[Taylor Dupuy]], Anton Hilado, _Probabilistic Szpiro, Baby Szpiro, and Explicit Szpiro from Mochizuki's Corollary 3.12_, arXiv:[2004.13108](https://arxiv.org/abs/2004.13108)

[[!redirects IUTT]]

[[!redirects inter-universal Teichmueller theory]]