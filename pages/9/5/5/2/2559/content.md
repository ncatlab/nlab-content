[[!redirects fractional exponential]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition#

[[William Lawvere]]'s definition of an _atomic_ [[infinitesimal space]] is as an [[object]] $\Delta$ in a [[topos]] $\mathcal{T}$ such that the [[inner hom]] [[functor]] $(-)^\Delta : \mathcal{T} \to \mathcal{T}$ has a [[right adjoint]] (is an [[atomic object]]).

Notice that by definition of [[inner hom]], $(-)^\Delta$ always has a [[left adjoint]]. A [[right adjoint]] can only exist for very particular objects. Therefore the term **amazing right adjoint**.

## Right adjoints to representable exponentials 

Assume $\mathcal{T} = Sh(C)$ is a [[Grothendieck topos]], that the [[Grothendieck topology]] on the [[site]] $C$ is [[subcanonical coverage|subcanonical]]. Let $\Delta \in C \hookrightarrow Sh(C)$ be a [[representable functor|representable object]]. 
Then, $(-)^\Delta: Sh(C)\to Sh(C)$ has a [[right adjoint]], hence $\Delta$ is an atomic [[infinitesimal space]],  precisely if $(-)^\Delta: C\to C$ preserves [[colimit]]s.
This is a special case of the general [[adjoint functor theorem#in_toposes]].
For if $(-)^\Delta$ preserves colimits, its [[right adjoint]] is

$$
 (-)_\Delta : (Y \in Sh(C)) \mapsto (U \mapsto Sh_C(U^\Delta, Y))
  \,.
$$ 

The $Y_\Delta$ defined this way is indeed a sheaf, due to the assumption that $(-)^\Delta$ preserves colimits. So this is indeed a [[right adjoint]].

## Related concepts

* A [[topos]] $\mathcal{X}$ is a [[local topos]] (over [[Set]]) if its [[global section]] functor $\Gamma = Hom(1_{\mathcal{X}}, -)$ admits a [[right adjoint]]. This is hence an "external" version of the amazing right adjoint, exhibiting $1_{\mathcal{X}}$ as "atomic". 

* The topic of amazing right adjoints appears to have been studied mostly for toposes, but a related definition has been given for any category (with products): if $O$ is an [[exponentiable object]] of a category $\mathcal{C}$, then $O$ being a [[tiny object]] in the sense of [Definition 0.1](#Yetter1987) means that the [[internal hom|endofunctor]] $(-)^O$ has a right adjoint. (This adjoint is sometimes denoted $(-)^{1/O}$, c.f. [Lawvere, p.269](#Lawvere2002), and called 'fractional exponential')

In this situation, one then has, symbolically

$$
  (-)\times O \quad \dashv\quad (-)^O \quad \dashv\quad  (-)^{1/O}
$$

## References#

The ubiquity of right adjoints to exponential functors in the context of [[synthetic differential geometry]] was first pointed out in Lawvere (1980). Lawvere (2004) suggests to augment [[lambda calculus]] with such fractional operators. Thorough discussion of the concept is in Yetter (1987) and Kock&Reyes (1999). Moerdijk&Reyes (1991) have a succinct overview in the context of SDG as does Lawvere (1997).

* [[William Lawvere]], _Toward the Description in a Smooth Topos of the Dynamically Possible Motions and Deformations of a Continuous Body_, Cah.Top.G&#233;om.Diff.Cat. **21** no.4 (1980) pp.377-392. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1980__21_4/CTGDC_1980__21_4_377_0/CTGDC_1980__21_4_377_0.pdf))

* [[William Lawvere]], _[[Toposes of laws of motion]]_, 1997.

* {#Law04} [[William Lawvere]], _Left and right adjoint operations on spaces and data types_ , Theor. Comp. Sci. **316** (2004) pp.105-111.

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]] , Springer Heidelberg 1991. (appendix 4)

* [[Anders Kock]], [[Gonzalo E. Reyes]], _Aspects of Fractional Exponent Functors_ , TAC **5** (1999) pp.251-265. ([pdf](http://www.tac.mta.ca/tac/volumes/1999/n10/n10.pdf))

* {#Yetter1987} [[David Yetter]], _On Right Adjoints of Exponential Functors_ , JPAA **45** (1987) pp.287-304. (Corrections in JPAA **58** (1989) pp.103-105)

* {#Lawvere2002} [[William Lawvere]], Categorical algebra for continuum micro physics, Journal of Pure and Applied Algebra 175 (2002) 267&#8211;287

A [[modal type theory]] for [[tiny objects]]:

* [[Mitchell Riley]], *A Type Theory with a Tiny Object* &lbrack;[arXiv:2403.01939](https://arxiv.org/abs/2403.01939)&rbrack;

* [[Mitchell Riley]]: *Tiny Objects in Type Theory*, [talk at](CQTS#RileyTinyApr2024) *[Running HoTT 2024](CQTS#RunningHoTT2024)*, [[CQTS]] @ NYU Abu Dhabi (Apr 2024) &lbrack;slides:[[Riley-TinyTypes-Apr2024.pdf:file]], video: [kt](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_31zdfvgi?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_31zdfvgi)&rbrack;

