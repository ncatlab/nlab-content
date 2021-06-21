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

Please note: everything in this section is heavily under construction! Contrary to possible current appearances, it is a serious attempt to shed some light on aspects of Mochizuki's work, and is not in any way intended as a parody or to do any disservice to Mochizuki's work, quite the contrary. We ask the reader for patience until such a time as what the page is intended to become is more clear.

### Dénouement {#Dénouement}

The logic of the final part of Mochizuki's approach to the [[abc conjecture]] is fairly straightforward in outline, and not, as far we know, a point of contention. We describe it here, deliberately using completely different notation from the IUTT papers to bring out the structure of the argument. Throughout, we shall assume that we have certain data $\mathbb{M}$, which we shall treat as a black box.

\begin{assum} \label{AssumptionMainInequalityInIUTT} Given $\mathbb{M}$, there are [[real number | real numbers]] $t_{\mathbb{M}}$ and $q_{\mathbb{M}}$ such that $-t_{\mathbb{M}} \geq - q_{\mathbb{M}}$. \end{assum}

\begin{cor} \label{CorollaryInequalityForConstant} Given any real number $c$ such that $-t_{\mathbb{M}} \leq c \cdot  q_{\mathbb{M}}$, we have that $c \geq -1$. \end{cor}

\begin{proof} Immediate. \end{proof} 

\begin{assum} \label{AssumptionConstantInvolvedInAbcConjecture} For a particular choice of $\mathbb{M}$, one can construct a real number $c_{\mathbb{M}}$ such that:

1. $-t_{\mathbb{M}} \leq c_{\mathbb{M}} \cdot q_{\mathbb{M}}$;
1. if $c_{\mathbb{M}} \geq -1$, then the abc conjecture holds.

\end{assum}

\begin{thm} (Conditional on Corollary 3.12 of IUTT III) The abc conjecture holds. \end{thm} 

\begin{proof} Follows immediately from Corollary \ref{CorollaryInequalityForConstant} and Assumption \ref{AssumptionConstantInvolvedInAbcConjecture}. \end{proof}

\begin{rmk} That Assumption \ref{AssumptionMainInequalityInIUTT} holds is the fundamental result of the IUTT series of papers. It is [[Mochizuki's corollary 3.12|Corollary 3.12]] in [IUTT III](#IUTTIII), and it is this corollary to which the objections raised by Scholze and Stix pertain.

That Assumption \ref{AssumptionConstantInvolvedInAbcConjecture} holds is the main purpose of [IUTT IV](#IUTTIV). It is established by Theorem 1.10 and Corollary 2.2. Theorem 1.10 establishes the particular inequality of the form $c_{\mathbb{M}} \geq -1$ that will be made use of; Corollary 2.2 specialises and refines it to an inequality which directly implies the abc conjecture. As far we know, these parts of the argument are expected to be sound.
\end{rmk}

### The key corollary

As discussed in the previous section, the cornerstone of the IUTT series of papers (at least with regard to the abc conjecture) is Corollary 3.12 in [IUTT III](#IUTTIII). We attempt here to explain certain aspects of this corollary. We shall continue to use completely different notation from the IUTT papers to try to bring out certain key ideas. To begin with, we shall continue to assume that we have a black box of data $\mathbb{M}$. We shall first indicate the logical structure of the corollary, devoid of any significant content. 

\begin{assum} There is a certain subset $T_{\mathbb{M}}$ of $\mathbb{R} \cup \{ \infty \}$, where $\mathbb{R}$ is the [[real number|set of real numbers]].  \end{assum}  

\begin{assum} There is a real number $q_{\mathbb{M}}$. \end{assum}

There are two key aspects to Corollary 3.12 in [IUTT III](#IUTTIII), which we now state.

\begin{thm} \label{TheoremIUTTMain} (If correct!) For any $t_{\mathbb{M}} \in T_{\mathbb{M}}$, we in fact have that $t_{\mathbb{M}} \neq \infty$, and thus that $t_{\mathbb{M}} \in \mathbb{R}$. Moreover, $-t_{\mathbb{M}} \geq -q_{\mathbb{M}}$. \end{thm}

\begin{rmk} A major point of confusion in attempts to understand Mochizuki's work has surrounded what Mochizuki refers to as 'indeterminacies'. At the level we are working at here, things are clear: all that matters is that $t_{\mathbb{M}}$ may be any one of a set of possible real numbers (what this set is is described precisely by Mochizuki, but this is irrelevant to the question of understanding the logic of the overall argument), whilst $q_{\mathbb{M}}$ is a specific real number. 

In particular, the [dénouement](#Dénouement) of Mochizuki's argument to prove the abc conjecture goes through regardless of the choice of $t_{\mathbb{M}}$ amongst the set $T_{\mathbb{M}}$.  
\end{rmk} 

We now begin working towards explaining what $T_{\mathbb{M}}$ and $q_{\mathbb{M}}$ are.

#### Pilot objects

Both the set $T_{\mathbb{M}}$ and the real number $q_{\mathbb{M}}$ are constructed ultimately from what Mochizuki refers to as pilot objects. Though the terminology in [IUTT III](#IUTTIII) is very dense, Mochizuki explains in Example 3.6, Remark 3.6.1, and subsequently that these can be understood in quite elementary terms, which we now describe.

Let $X$, $F$, $F_{mod}$, and $\underline{\mathbb{V}}$ be as at [[initial Θ-data]]: $X$ is a once-puncturing of an [[elliptic curve]] $E$, $F$ is a [[number field]], $F_{mod}$ is the [[field of moduli]] of $X$ with respect to $F$, $\underline{\mathbb{V}}$ is a certain set of [[valuation|valuations]], and all of $X$, $F$, $\overline{F}$, and $\underline{\mathbb{V}}$ satisfy certain conditions which will be referred to here only as needed. Let $F^{\times}_{mod}$ denote the [[group of units|multiplicative group]] of $F_{mod}$.

Let $v \in \underline{\mathbb{V}}$. By definition, $v$ is a valuation on $K_E$, where $K_E$ is as defined at [[initial Θ-data]]. Denote the completion of $K_E$ with respect to $v$ by $K_{v}$, denote the [[ring of integers]] of $K_{v}$ by $\mathcal{O}_{K_{v}}$, and denote the [[group of units]] of these two rings by $K^{\times}_{v}$ and $\mathcal{O}_{v}^{\times}$ respectively. 

Let $\beta_{v}: F_{mod}^{\times} \rightarrow K_{v}^{\times} / \mathcal{O}^{\times}_{v}$ denote the [[homomorphism|group homomorphism]] induced by the composition of the field inclusion $F_{mod} \hookrightarrow K_{E}$ with the canonical ring homomorphisms $K_{E} \hookrightarrow K_{v} \twoheadrightarrow K_{v} / \mathcal{O}_{v}$. 

\begin{defn} \label{DefinitionFStarMOD} We denote by $F^{*}_{MOD}$ the category whose objects consist of:

1. An $F^{\times}_{mod}$-[[torsor]] $T$, where [[torsor]] here is understood with respect to the [[category of sets]].

1. For every $v \in \underline{\mathbb{V}}$, a trivialisation $t_{v}$ of the $K_{v}^{\times} / \mathcal{O}_{K_v}^{\times}$-torsor $T_{v}$ obtained from $T$ by change of structure group with respect to $\beta_{v}$. We require that there is a $t \in T$ such that, for all but finitely many $v$, $t_{v}$ is equal to the trivialisation of $T_{v}$ determined by $\beta_{v}(t)$. (See [[torsor]] for the details of trivialisation of a torsor, and for the notion of change of structure group of a torsor.)
  
TODO: FINISH

\end{defn}

\begin{rmk} Definition \ref{DefinitionFStarMOD} is Example 3.6 in [IUTT III](#IUTTIII), and is also discussed in Remark 3.6.1. Remark 3.1.5 of [IUTT I](#IUTTI) is also relevant. \end{rmk}





## Related concepts

* [[anabelian geometry]]

* [[étale theta function]]

* [[Frobenioid]]

* [[initial Θ-data]]

* [[Mochizuki's corollary 3.12]]

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

The following two papers give a _statement_ of [[Mochizuki's Corollary 3.12]] in plain language (not using the elaborate setup in the IUT papers), and **assuming** the inequality in it as given, derive concrete versions of (weakenings of) Szpiro's conjecture, again, using conventional terminology and techniques.

* [[Taylor Dupuy]], Anton Hilado, _The Statement of Mochizuki's Corollary 3.12, Initial Theta Data, and the First Two Indeterminacies_, arXiv:[2004.13228](https://arxiv.org/abs/2004.13228)

* [[Taylor Dupuy]], Anton Hilado, _Probabilistic Szpiro, Baby Szpiro, and Explicit Szpiro from Mochizuki's Corollary 3.12_, arXiv:[2004.13108](https://arxiv.org/abs/2004.13108)

[[!redirects IUTT]]

[[!redirects inter-universal Teichmueller theory]]