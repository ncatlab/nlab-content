
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--




\tableofcontents


## Idea

The generalization of [[Teichmüller theory]] to [[arithmetic geometry]] has been called _inter-universal Teichmüller theory_ (often abbreviated _IUTT_) by [[Shinichi Mochizuki]]. It is a part of [[anabelian geometry]].

{#InterUniversal} The term "Inter-Universal" refers to Mochizuki's Key Principle of Inter-Universality [IUTT I, Section I3, Page 25-26] which requires one to work with arbitrary geometric base-points for the tempered fundamental groups. 

A choice of a geometric base-point for the tempered fundamental group corresponds to a choice of a fiber functor for the galois category of tempered coverings. Hence Mochizuki asserts [IUTT I, Section I3 Page 25-26] that the idea of working with distinct geometric base-points is tantamount to relating the distinct set-theoretic universes the fiber functors arise from and  so theory is referred to as being inter-universal. [The fundamental group is, of course, independent (or agnostic) of the choice of the fiber functor, i.e. it is an object which is oblivious to the choice of the set theoretic universe it arises from.]

Hence Mochizuki has asserted that this  theory is meant to formulated explicitly in a way that respects [[universe enlargement]], hence that it is [[universe polymorphism|universe polymorphic]] ([IUTT IV, remark 3.1.4](#IUTTIV), [Yamashita 13](#Yamashita13)).

While [IUTT I-IV] offers scant mathematical justification  of the Teichmuller aspects of the theory (i.e. [IUTT I-IV] provides no mathematical justification  why the theory is a Teichmuller Theory), a clearest proof of this Teichmuller aspect has been provided (in all dimensions) in the works of [[Kirti Joshi]]. 

It is claimed ([IUTT IV](#IUTTIV)) that a proof of the [[abc conjecture]] can be given in IUTT. In 2018, a document [[why_abc_is_still_a_conjecture.pdf:file]] was written by [[Peter Scholze]] and [[Jakob Stix]] raising objections to the argument. More accurate critiques have appeared as a part of the works of [[Kirti Joshi]] on the theory of Arithmetic Teichmuller Spaces which includes, in dimension one and genus one, a precise version of Mochizuki's IUTT. 


In brief, the novel idea due to Mochizuki, is to average over deformations of arithmetic (or an arithmetic holomorphic structure) itself (this notion has been precisely quantified in the works of [[Kirti Joshi]]). It should be remarked that Classical Teichmuller Theory should be considered as a model for Mochizuki's (and Joshi's) theory at any archimedean prime of a number field.

## Details

### Pilot objects


Important to the arguments in the latter parts of the IUTT series are what Mochizuki refers to as pilot objects. (A precise construction of Pilot objects has been independently provided in [[Kirti Joshi|Construction of Arithmetic Teichmuller Spaces III: A Rosetta Stone and a proof of Mochizuki’s Corollary 3.12]].)

 Though the terminology in [IUTT III](#IUTTIII) is very dense, Mochizuki explains in Example 3.6, Remark 3.6.1, and subsequently that these can be understood in quite elementary terms, which we now describe.

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

### General

* {#IUTTI} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory I, Construction of Hodge theaters_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20I.pdf))

* {#IUTTII} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory II, Hodge-Arakelov-theoretic evaluation_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20II.pdf))

* {#IUTTIII} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory III, Canonical splittings of the Log-theta-lattice_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20III.pdf))

* {#IUTTIV} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory IV, Log-volume computations and set-theoretic foundations_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20IV.pdf))
 

Surveys:

* [[Shinichi Mochizuki]], _Panoramic overview of inter-universal Teichmuller theory_, [pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Panoramic%20Overview%20of%20Inter-universal%20Teichmuller%20Theory.pdf)

* Benjamin Collas, _Anabelian Arithmetic Geometry—a New Geometry of Forms and Numbers: Inter-universal Teichmüller Theory or Beyond Grothendieck's Vision"_, Lobachevskii Journal of Mathematics February 2025, Volume 45, pp. 4954–4979 [Springer Nature](https://rdcu.be/ebi17)


* {#Yamashita13} Go Yamashita, _FAQ on 'Inter-Universality'_ ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/FAQ%20on%20Inter-Universality.pdf))
 

* {#Fesenko15} [[Ivan Fesenko]], _Arithmetic deformation theory via arithmetic fundamental groups and nonarchimedean theta functions_, European Journal of Mathematics September 2015, Volume 1, Issue 3, pp 405-440 ([publisher](http://link.springer.com/article/10.1007/s40879-015-0066-0), [pdf](https://www.maths.nottingham.ac.uk/personal/ibf/notesoniut.pdf))

* [[Minhyong Kim]], _Brief superficial remarks on Shinichi Mochizuki's Interuniversal Teichmueller Theory (IUTT), version 1_, 10/11/2015, ([pdf](http://people.maths.ox.ac.uk/kimm/papers/pre-iutt.pdf)).

* [[Taylor Dupuy]], Hodge Theaters: _[A First Look at the Big Hodge Theater](https://www.youtube.com/watch?v=V_tWUswSUoo)_,  _[ Confused Groups and Torsors](https://www.youtube.com/watch?v=8yacRMVIIHs&list=PLJmfLfPx1OecDVF-VgXNeCfAlisy74PHt)_

*  [RIMS/Symmetries and Correspondences workshop](https://www.maths.nottingham.ac.uk/personal/ibf/files/kyoto.iut.html): _[Inter-universal Teichm&#252;ller Theory Summit 2016](https://www.maths.nottingham.ac.uk/personal/ibf/files/iut-kyoto-pr.html)_

* {#Morrow17} [[Jackson Morrow]], _Kummer classes and Anabelian geometry_, notes from Super [QVNTS](http://www.dms.umontreal.ca/%7Eqvnts/): [Kummer Classes and Anabelian Geometry](http://www.uvm.edu/%7Etdupuy/anabelian.html) 2017 ([pdf](https://www.dropbox.com/s/kiszgkrrsjrqu4p/VermontNotes_Final.pdf?dl=0))

The following two papers give a _statement_ of [[Mochizuki's Corollary 3.12]] in plain language (not using the elaborate setup in the IUT papers), and **assuming** the inequality in it as given, derive concrete versions of (weakenings of) Szpiro's conjecture, again, using conventional terminology and techniques.

* [[Taylor Dupuy]], [[Anton Hilado]], _The Statement of Mochizuki's Corollary 3.12, Initial Theta Data, and the First Two Indeterminacies_, arXiv:[2004.13228](https://arxiv.org/abs/2004.13228)

* [[Taylor Dupuy]], [[Anton Hilado]], _Probabilistic Szpiro, Baby Szpiro, and Explicit Szpiro from Mochizuki's Corollary 3.12_, arXiv:[2004.13108](https://arxiv.org/abs/2004.13108)


### Formalization attempts
 {#ReferencesFormalizationAttempts}

Early verbalization of the idea to formalize the alleged IUT proof of the [[abc conjecture]] with a [[proof assistant]]:

* [[Timothy Chow]], MathOverflow comment (8 Apr 2020) &lbrack;[MO:a/356937](https://mathoverflow.net/a/356937/381)&rbrack;
> "one could ask if it is reasonable to request that the group of people who claim to understand Mochizuki's proof (and who believe that it is complete and correct) to formalize the proof using a proof assistant. \[...\]  When the normal process of socializing a proof breaks down, it should indeed be possible in principle for computers to "come to the rescue". \[...\] If the proof really is correct and those people really do understand it, then the project should eventually succeed, and when it does, the skeptics should be convinced. On the other hand, if the proof has a huge gap, then eventually those tasked with formalization (I'm imagining graduate students) will be forced to confront it, and it will become increasingly hard for "believers" to make excuses for why the formalization project is stalling."

Embracing the idea of reaching consensus via ([[Lean]]) formalization:

* {#MochizukiExLeanTalk2026} [[Shinichi Mochizuki]]: *On the Formalization of IUT: a preliminary progress report*, talk at *exlean* (Apr 2026) &lbrack;video:[yt](https://youtu.be/H4n1XIa2flI)&rbrack;

<center>
  <div style="margin:-40px 0px 00px 00px;">
  <a href="https://youtu.be/H4n1XIa2flI?t=138">
  <img src="https://ncatlab.org/nlab/files/Mochizuki-LeanFormalizationScreenShot.png" width="600"/></a></div>
</center>

The *LANA project* carrying out the formalization of the alleged IUT proof of the [[abc conjecture]] with a [[proof assistant]] ([[Lean]]):

* ZEN Mathematics Center: *[Lean for ANAbelian geometry (LANA)](https://zen.ac.jp/news/zmcpostevent0331e)* (March 2026)

* Alex Wilkins: *[The secret project to settle controversial maths proof with a computer](https://www.newscientist.com/article/2522687-the-secret-project-to-settle-controversial-maths-proof-with-a-computer/)*. New Scientist (April 10, 2026)

Results of this formalization effort:

* Yuichiro Hoshi, [March 2026](https://zen.ac.jp/en/zmc/topics/jwz-o8xr3v6f), [here](https://zen.ac.jp/en/zmc/topics/jwz-o8xr3v6f#:~:text=with%20regard%20to%20the%20logic):
  > "with regard to the logic by which Corollary 3.12 is derived from Theorem 3.11 as I mentioned earlier, I must take seriously the fact that many members of the LANA Project still feel that there is some insurmountable wall there."

* {#LANAReport2026} LANA Project: *Interim Report 2026: Computer-Assisted Verification of IUT Theory* (July 2026) &lbrack;[github](https://github.com/katobungen/LANA_report_202607/blob/pdf/LANA_report_202607.pdf), [[LANAProject-Report-July2026.pdf:file]]&rbrack;
  > "we isolate a specific compatibility problem at the final stage of the argument &lbrack;...&rbrack; Project LANA has not yet reconstructed a proof of the required compatibility"

* LANA Project Press Conference, Zen Mathematics Center (17 July 2026) &lbrack;[video:YT](https://www.youtube.com/live/KADN5NHmIfw?t=593s)&rbrack;
  > [40:45](https://youtu.be/KADN5NHmIfw?t=2445): "This is exactly the point that we don't understand how to prove"

* Fumiharo Kato (17 July 2026) ([x.com:2078017230537892207](https://x.com/FumiharuKato/status/2078017230537892207)):
  > "In today's press conference, we explained our efforts over the last two years which resulted in the following conclusion: The way the argument from Theorem 3.11 to Corollary 3.12 is written in the IUT papers is unformalizable. But since **Mochizuki's explanation of this point has recently started evolving**, we reserve final judgement at this time."

  > &lbrack;our emphasis&rbrack;

The problem encountered by the LANA project is claimed to be different from that previously argued in:

* {#ScholzeStix208} [[Peter Scholze]], [[Jakob Stix]]: *Why $a b c$ is still a conjecture* (Aug 2018) &lbrack;[[why_abc_is_still_a_conjecture.pdf|pdf:file]]&rbrack;

for the [LANA report 2026](#LANAReport2026) writes in its final [§10 (pp. 46)](https://ncatlab.org/nlab/files/LANAProject-Report-July2026.pdf#page=46):

> "We now compare our analysis with that made by [Scholze and Stix in &lbrack;15&rbrack;](#ScholzeStix208) \[...\] In the final part of \[15\], the occurrence of monodromy in the identifications among the various ordered one-dimensional real vector spaces appearing in the theory is pointed out as a flaw in the proof \[...\] \[We\] indicate why this occurrence of monodromy does not represent an obstruction to the intended proof strategy of Mochizuki \[...\] \[because\] our analysis does not give rise to this particular diagram; rather, the elaboration of the $\eta$-algorithm shows that the proof of the final numerical inequality hinges on the compatibility (9-1) which is not manifestly false. However, we, the LANA project, do not have a proof of (9-1) at this time."

See also: 

* Lean Zulip Board: *[LANA project announcement](https://leanprover.zulipchat.com/#narrow/channel/113488-general/topic/LANA.20project.20announcement/with/611402299)* (31 Mar 2026--)



[[!redirects IUTT]]
[[!redirects IUT]]

[[!redirects inter-universal Teichmueller theory]]



