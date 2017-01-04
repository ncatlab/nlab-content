[[!redirects empty 162]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Cohesion
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}
[[!redirects Sufficiently cohesive topos]]
[[!redirects contractible object]]
[[!redirects sufficient cohesion]]
[[!redirects sufficiently cohesive toposes]]
[[!redirects Sufficient Cohesion]]

## Idea

A **sufficiently cohesive topos** is a topos that has enough connected objects. This can be viewed as a strong form of cohesiveness in the context of [[William Lawvere|Lawvere's]] axiomatic approach to [[big topos|gros toposes]].

## Terminological preliminaries

Sufficient cohesion is a relative concept and requires minimally the presence of an [[essential geometric morphism]] $p:\mathcal{E}\to\mathcal{S}$. Here we state it for an [[adjoint quadruple]] $p_!\dashv p^* \dashv p_* \dashv p^!:\mathcal{S}\to\mathcal{E}$ such that $p^!$ (and hence $p^\ast$) is [[fully faithful]] and $p_!$ preserves finite products.

This is called a 'cohesive topos' at [[cohesive topos]], and will be referred to as a _'weakly cohesive topos'_ in the present entry - a sufficiently cohesive topos in this context corresponds to the axiomatization of a 'gros topos' in Lawvere ([1986](#Law86)) where the concept was considered for the first time. 

A weakly cohesive topos is called _pre-cohesive_ if $p$ furthermore satisfies the [[Nullstellensatz]] i.e. the canonical map $\theta:p_\ast\to p_!$ is an epimorphism. This is the situation explored in Menni ([2014a](#Menni14a), [2014b](#Menni14b)).

A pre-cohesive topos that furthermore satisfies the _continuity principle_ that $p_1(X^{p^\ast(Y)})\simeq p_!(X)^{Y}$ for all $X\in\mathcal{E}$, $Y\in\mathcal{S}$, is called _'cohesive'_ in Lawvere ([2007](#Law07)) where the term 'sufficently cohesive' occurs for the first time though the essential results are already present throughout the 1990s ([1986](#Law86), [1992](#Law92), [1997](#Law99)).

## Definitions

+-- {: .num_defn #Contractible_object}
###### Definition 
An object $X$ in a weakly cohesive topos $p:\mathcal{E}\to\mathcal{S}$ is called _contractible_ if for every object $Y\in\mathcal{E}$: $p_!(X^Y)=1$. 
=--

+-- {: .num_rem}
###### Remark
In particular, a contractible is connected: $p_!(X)=p_!(X^1)=1$.
=--

+-- {: .num_defn #Sufficient_Cohesion}
###### Definition 
A weakly cohesive topos $p:\mathcal{E}\to\mathcal{S}$ is called _sufficiently cohesive_ if the [[subobject classifier]] $\Omega$ is contractible i.e. $p_!(\Omega^X)=1$ for every object $X\in\mathcal{E}$ or, in other words, if all power objects are connected. 
=--

+-- {: .num_rem}
###### Remark
Since in general, every object $X$ embeds into its power object $X\rightarrowtail\Omega^X$ it follows that in a sufficiently cohesive topos $\mathcal{E}$ every object embeds into a [[connected object]] i.e. $\mathcal{E}$ has _enough connected objects_.

Furthermore, since in a [[Cartesian closed category]] $X^{(Y\times Z)}\simeq(X^Y)^Z$ one sees that in a sufficiently cohesive topos power objects $\Omega^X$ are not merely connected but even contractible: $p_!((\Omega^X)^Z)=p_!(\Omega^{X\times Z})=1$ and hence it follows that in a sufficiently cohesive topos every object embeds into a contractible object.

Conversely, if every power object $\Omega^X$ embeds into a connected object then the power objects $\Omega^X$ will be connected themselves by proposition \ref{connected_retract} below since power objects are injective in general. Whence a topos is sufficiently cohesive iff every object embeds into a connected object iff every object embeds into a contractible object. The last formulation is taken as the definition of sufficient cohesion in Lawvere ([2007](#Law07)).
=--

## Properties

+-- {: .num_proposition #connected_retract}
###### Proposition
In a weakly cohesive topos, retracts of connected objects are connected themselves.
=--

**Proof**. Let $X$ be a retract of $Y$ with $p_!(Y)=1$. Then $id_X$ factors as $X\rightarrowtail Y\to X$ and applying $p_!$ shows that $id_{p_!(X)}$ factors through the terminal object $p_!(Y)$. $\qed$

Since in general, injective objects $I$ are retracts of the objects $X$ that they embed into because such inclusions $I\rightarrowtail X$ factor through $id_I$ by injectivity, it follows that in a weakly cohesive topos _injective objects that embed into a connected object are connected_ themselves.

...

## Related entries

* [[cohesive topos]]

* [[Nullstellensatz]]

* [[quality type]]

* [[connected object]]

* [[injective object]]

## References

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#JS11} [[Peter Johnstone|P. Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#J02} [[Peter Johnstone|P. Johnstone]], _Sketches of an Elephant vol. 1_ , Cambridge UP 2002. 

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law86} [[F. W. Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](ftp://ftp.tac.mta.ca/tac/html/tac/reprints/articles/9/tr9.pdf))

* {#Law91a} [[F. W. Lawvere]], _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law92} [[F. W. Lawvere]], _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al (eds.), _The Space of Mathematics_ , de Gruyter Berlin 1992.

* {#Law99} [[F. W. Lawvere]], _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law07} [[F. W. Lawvere]], _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp.41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* {#MarmoMenni16}F. Marmolejo, [[Matías Menni|M. Menni]], _On the relation between continuous and combinatorial_ , arXiv:1602.02826 (2016). ([abstract](http://arxiv.org/abs/1602.02826))

* {#Menni14a} [[Matías Menni|M. Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah. Top. G&#233;om. Diff. Cat. **LV** (2014). ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))

* {#Menni14b} [[Matías Menni|M. Menni]], _Continuous Cohesion over Sets_ , TAC **29** no.20 (2014) pp.542-568. ([pdf](http://www.tac.mta.ca/tac/volumes/29/20/29-20.pdf))












