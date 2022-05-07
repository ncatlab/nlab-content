
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}



## Idea

An **&#233;tendue** (also 'etendue', or 'etendu'; from French '&#233;tendue' (fem.)- _extent_) is a [[topos]] $\mathcal{Y}$ that locally looks like the category of sheaves on a space:
>Briefly, the slogan is that $\mathcal{Y}$ is locally a topological space. ([Lawvere 1976](#Lawvere76), p.129)

Originally defined by [[A. Grothendieck]] in one of the famous 'excercises' of [SGA4](#SGA4) (ex. 9.8.2) as a [[Grothendieck topos]] $\mathcal{Y}$ that has a well-supported object $X$ such that the [[slice topos]] $\mathcal{Y}/X$ is equivalent to a sheaf topos on a topological space, the definition was generalized by [[Lawvere]] (1975,1976) by dropping the spatiality of the slice and require only that $\mathcal{Y}/X$ is a [[localic topos]].

Several characterizations of &#233;tendues are known and the _Ur_-example of an &#233;tendue, the presheaf topos $\mathcal{S}^G$ of group actions, exhibits one in terms of sites rather directly: it has a [[site]] where every morphism is monic. Other characterizations involve (local) [[equivalence relations]] and yield connections to [[orbifolds]], [[foliations]], and [[stacks]], which are instrumental for the generalization to _$\infinity$-&#233;tendues_ (cf. [Carchedi 2013](#Carchedi13)).

&#201;tendues play an important role in Lawvere's approach to [[cohesion]] and the distinction between [[petit and gros toposes]] where they provide one of the classes of **petit** toposes (generalized spaces). In this context, Lawvere (1989,1991) interprets the cancellative property of the site as enabling an interpretation of &#233;tendues as _categories of processes_. 

## Definition

A topos $\mathcal{Y}$ is called an _&#233;tendue_ if there is an object $X\in|\mathcal{Y}|$ such that the unique $X\rightarrow 1$ is epic and the [[slice topos]] $\mathcal{Y}/X$  is a [[localic topos]].[^fine]

[^fine]:  An epic $k:X\rightarrow Y$ induces a [[geometric morphism]] $k_\ast:\mathcal{Y}/X\rightarrow \mathcal{Y}/Y$ whose inverse image part, the change of base functor, $k^\ast:\mathcal {Y}/Y\rightarrow\mathcal{Y}/X$ is faithful, which says by definition that $k_\ast$ is a surjection, and in case $Y=1$, one says that $\mathcal{Y}/X$ _covers_ $\mathcal{Y}$. $k_\ast$ is an [[étale geometric morphism]].

## Examples

> The first example of an &#233;tendue seems to have been the [[space of moduli]] of algebraic curves, which is prevented from being globally a space due to the action of the [[Galois groups]] within each point. Yes, something vaguely reminiscent of particle spin is going on in such spaces, and the most naked form is that for any group G, the category $\mathcal{S}^G$ is an &#233;tendue with only one point! This is easily seen from the observations that $\mathcal{S}^G/G\cong\mathcal{S}^G$ and that $G\twoheadrightarrow 1$ where the last two $G$'s denote the regular representation.      ([Lawvere 1976](#Lawvere76), pp.129-130)

* The [[Sierpinski topos]] $\mathcal{S}^{\cdot\rightarrow\cdot}$, as the sheaf topos on the [[Sierpinski space]], is an &#233;tendue.

* The topos  $\mathcal{S}^{\cdot\rightrightarrows\cdot}$ of _directed [[graphs]]_ (aka [[quivers]]; Lawvere calls them *irreflexive graphs*) is an &#233;tendue, as it is locally equivalent to the sheaf topos on a three point space  (Lawvere 1986). The contrast between $\mathcal{S}^{\cdot\rightrightarrows\cdot}$ and the topos  $\mathcal{S}^{\Delta_1^{op}}$ of _reflexive graphs_ is a paradigmatic example of the distinction between a _petit_ and a _gros_ topos.

* The [[Jónsson-Tarski topos]] $\mathcal{J}_2$ is an &#233;tendue, as it is locally equivalent to the sheaf topos on the [[Cantor space]]. It is discussed as a petit topos for _labeled graphs_ in (Lawvere 1989).
 
## Properties

* **Proposition**. A Grothendieck topos $\mathcal{Y}$ is an &#233;tendue iff there exists a [[site]] $(\mathcal{C}, J)$ for $\mathcal{Y}$ such that every morphism of $\mathcal{C}$ is monic.

* In particular for small $\mathcal{C}$, the presheaf topos $\mathcal{S}^{\mathcal{C}^{op}}$ is an &#233;tendue iff all morphisms in $\mathcal{C}$ are monic. In particular for [[monoid]]s $\mathcal{C}$ this is sometimes called [[left cancellative category|left cancellative]] (e.g. each free monoid is left cancellative).

* [[Subtoposes]] of &#233;tendues are &#233;tendues. K. Rosenthal uses this together with the preceding remark on $\mathcal{S}^{\mathcal{C}^{op}}$ for all-monic $\mathcal{C}$ in order to construct further &#233;tendues $Sh_j(\mathcal{S}^{\mathcal{C}^{op}})$ via a topology $j$ from a suitable functor $H:\mathcal{C}\to\mathcal{S}$ (for further details see [[Jónsson-Tarski topos]] or Rosenthal(1981)).

* A Grothendieck topos is a _[[boolean topos|Boolean]] &#233;tendue_ precisely if it satisfies the _internal [[axiom of choice]]_ (Freyd&Scedrov 1990). An example of such a Boolean &#233;tendue is $\mathcal{S}^G$, for $G$ a group.

* &#201;tendues are 'locally co-decidable' in the sense that for a small $\mathcal{C}$ the functor category $[\mathcal{C},Set]$ is a [[locally decidable topos]] precisely if $[\mathcal{C}^{op},Set]$ is an [[étendue]]. Also the all-monic-site property is dual to the all-epic-site property of locally decidable toposes. Both concepts are subsumed under the notion of having a (sub canonical) site representation with no (non-trivial) [[idempotents]] (McLarty 2006, Lawvere 2007).

## Slice toposes of étendues are étendues

One can use the site characterization to show that being an étendue topos is a _local property_.

+-- {: .num_prop #etendue_slices}
###### Proposition
Let $Sh(\mathcal{C},J)$ be an étendue topos with $(\mathcal{C}, J)$ being an all-monic-site presentation and $P:C^{op}\to Set$ be a presheaf on $\mathcal{C}$  that is a $J$-sheaf. Then $Sh(\mathcal{C},J)/P$ is an étendue topos.
=--

+-- {: .proof}
###### Proof
It suffices to show that $Sh(\mathcal{C},J)/P$ has an all-monic site presentation. By exercise III.8 in [Mac Lane-Moerdijk (1994, p.157)](#MacLaneMoerdijk) there exists a topology $J'$ on the [[category of elements]] $\int_\mathcal{C} P$ such that
$$Sh(\mathcal{C},J)/P\simeq Sh(\int_\mathcal{C} P,J')\; .$$
Whence it suffices to show that $\int_\mathcal{C} P$ is all-monic: Let $f:(C,x)\to (D,y)$ be a morphism in $\int_\mathcal{C} P$ and $g,h:(B,z)\rightrightarrows (C,x)$ such that $f\cdot g=f\cdot h$ then $g=h$ since composition in $\int_\mathcal{C} P$ is inherited from $\mathcal{C}$ and the latter was all-monic by assumption.

=--

+-- {: .num_prop #IAC_local}
###### Corollary
Let $\mathcal{E}$ be a Grothendieck topos satisfying the [[axiom of choice|internal axiom of choice]] (IAC). Then any [[slice topos]] $\mathcal{E}/X$ satisfies the internal axiom of choice as well.
=--
+-- {: .proof}
###### Proof
By Freyd-Scedrov ([1990](#FreydScedrov90), p.181) a Grothendieck topos $\mathcal{E}$ satisfies IAC iff $\mathcal{E}$ is a Boolean étendue. But being [[Boolean category|Boolean]] is a local property whence by the preceding proposition all slices $\mathcal{E}/X$ are Boolean étendues.
=--

## Related entries

* [[localic topos]]

* [[petit topos]]

* [[locally decidable topos]]

* [[Deligne-Mumford stack]]

* [[bicategory of fractions]]



##References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, Springer LNM vol.269 (1972), pp.479-484.

* {#Carchedi13}[[David Carchedi]], _Higher Orbifolds and Deligne-Mumford Stacks as Structured Infinity Topoi_ , arXiv1312.2204 (2013). ([pdf](http://arxiv.org/pdf/1312.2204v1.pdf))

* {#FreydScedrov90}[[Peter Freyd|P. J. Freyd]], A. Scedrov, _[[Categories, Allegories]]_ , North-Holland Amsterdam 1990.

* [[Peter Johnstone]], _Sketches of an [[Elephant]] II_, Oxford UP 2002, pp.769-775.

* [[A. Kock]], [[I. Moerdijk]], _Presentations of Etendues_ , Cah. Top. G&#233;om. Diff. Cat. **XXXII** 2 (1991) pp.145-164. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1991__32_2/CTGDC_1991__32_2_145_0/CTGDC_1991__32_2_145_0.pdf))

* [[A. Kock]], [[I. Moerdijk]], _Every &#233;tendue comes from a local equivalence relation_ , JPAA **82** (1992) pp.155-174.

* [[M. V. Lawson]], [[B. Steinberg]], _Ordered groupoids and &#233;tendues_ , Cah. Top. G&#233;om. Diff. Cat. **XXXXV** 2 (2004) pp.82-108. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_2004__45_2/CTGDC_2004__45_2_82_0/CTGDC_2004__45_2_82_0.pdf))

* [[F. William Lawvere]], _Variable sets etendu and variable structure in topoi_ , Lecture notes University of Chicago 1975.

* {#Lawvere76}[[F. William Lawvere]], _Variable quantities and variable structures in topoi_ , pp.101-131 in Heller, Tierney (eds.), Algebra, Topology and Category Theory, Academic Press New York 1976. 

* [[F. William Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](http://www.tac.mta.ca/tac/reprints/articles/9/tr9.pdf))

* [[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* [[F. William Lawvere]], _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM vol. 1488 (1991).

* [[F. William Lawvere]], _Axiomatic Cohesion_ , TAC **19** no. 3 (2007) pp.41-49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* [[F. William Lawvere]], _Cohesive Toposes: Combinatorial and Infinitesimal Cases_, Como Ms. 2008. ([pdf](http://comocategoryarchive.com/Archive/temporary_new_material/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf))

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994.

* [[Colin McLarty]], _Every Grothendieck Topos has a One-Way Site_ , TAC **16** no. 5 (2006) pp.123-126. ([pdf](http://www.tac.mta.ca/tac/volumes/16/5/16-05.pdf))

* [[Ieke Moerdijk]], _Foliations, groupoids and Grothendieck étendues_ , Rev. Acad. Cienc. Zaragoza (2) **48** (1993) pp.5-33.

* [[Dorette A. Pronk]], _Etendues and stacks as bicategory of fractions_ , Comp. Math. **102** 3 (1996) pp.243-303. ([pdf](http://archive.numdam.org/ARCHIVE/CM/CM_1996__102_3/CM_1996__102_3_243_0/CM_1996__102_3_243_0.pdf))

* [[Pedro Resende]], _Groupoid Sheaves as Quantale Modules_ , arXiv.0807.4848v3 (2011). ([pdf](http://arxiv.org/pdf/0807.4848v3.pdf))

* [[Kimmo I. Rosenthal]], _&#201;tendues and Categories with Monic Maps_ , JPAA **22** (1981) pp.193-212.

* [[Kimmo I. Rosenthal]], _Sheaves and Local Equivalence Relations_ , Cah. Top. G&#233;om. Diff. Cat. **XXV** 2 (1984) pp.179-206. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1984__25_2/CTGDC_1984__25_2_179_0/CTGDC_1984__25_2_179_0.pdf))

* [[Kimmo I. Rosenthal]], _Covering &#201;tendues and Freyd's Theorem_ , Proc. AMS **99** 2 (1987) pp.221-222. ([pdf](http://www.ams.org/journals/proc/1987-099-02/S0002-9939-1987-0870775-X/S0002-9939-1987-0870775-X.pdf))

[[!redirects etendue]]
[[!redirects etendues]]
[[!redirects étendues]]