
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}


## Idea

A **De Morgan topos** $\mathcal{E}$ is a middle thing between a [[Boolean topos]] with a [[classical logic|classical internal logic]] and a general [[topos]] with an [[intuitionistic logic|intuitionistic internal logic]], in that the lattices of [[subobjects]] in $\mathcal{E}$ obey a weak form of the [[law of excluded middle]] which defines a [[De Morgan Heyting algebra]].

The de Morgan property has many equivalent formulations and many facets making the class of de Morgan toposes an important one in [[topos theory]]. From the perspective on toposes as generalized spaces they correspond to _extremally disconnected spaces_ in [[topology]].


## Definition

A topos $\mathcal{E}$ is called a __De Morgan topos__ if its [[subobject classifier]] $\Omega$ is an internal [[De Morgan Heyting algebra]].


## Examples

* Every [[Boolean topos]] is a De Morgan topos.

* A simple example of a topos that is De Morgan but not Boolean is the [[Sierpinski topos]] $Set^{\to}$ the [[arrow category]] of $Set$: the diagram category $\to$ is easily seen to satify the [[Ore condition]] (cf. [below](#presheaf-deMorgan)).

* The topos $Sh(X)$ of sheaves on a topological space $X$ is De Morgan precisely iff $X$ is [[extremally disconnected topological space|extremally disconnected]], i.e. the closure of every open subset is open. (Since $Set^{\to}$ is equivalently the topos of sheaves on [[Sierpinski space]] it instantiates this case as well.)

* [[injective topos|Injective Grothendieck toposes]] are De Morgan (cf. [Johnstone 2002, p.739](#Johnstone)).


## Some equivalent formulations

The importance of the concept of a De Morgan topos stems partly from the fact that for many statements whose classical (Boolean) validity is lost in intuitionistic logic the De Morgan property delineates precisely the range of toposes where the statement is valid. An illustration of this is e.g. the implication that maximal ideals are prime in commutative rings. 

Though such statements are in fact equivalent to the De Morgan property they are better viewed as higher-order properties of De Morgan toposes.

In contrast, there exists also a long list, mostly due to [Johnstone (1979)](#Johnstone79), of statements equivalent to the De Morgan property, that are logically of the same complexity and are often more convenient to work with than the original definition. Some of the most important of these appear in the following:

+-- {: .num_prop #deMorgan_equivalents}
###### Proposition
Let $\mathcal{E}$ be a topos. The following are equivalent:

* $\mathcal{E}$ is a De Morgan topos.

* For all formulae $\varphi,\psi$ : $\mathcal{E}\models \neg (\varphi\wedge\psi)\Leftrightarrow(\neg\varphi\vee\neg\psi)$ .

* For every formula $\varphi$ : $\mathcal{E}\models \neg\varphi\vee\neg\neg\varphi$.

* For every subobject $X\rightarrowtail Y$: $\neg X\vee\neg\neg X=Y$.

* $Sub(X)$ is a De Morgan Heyting algebra for every $X\in\mathcal{E}$.

* The canonical monomorphism $(\top,\bot):1\coprod 1\rightarrowtail\Omega_{\neg\neg}$ to the subobject classifier of $Sh_{\neg\neg}(\mathcal{E})$ is an isomorphism.

* $\Omega_{\neg\neg}$ is [[decidable object|decidable]].

* $1\coprod 1$ is a retract of $\Omega_{\neg\neg}$.

* $1\coprod 1$ is [[injective object|injective]].

* Every $\neg\neg$-sheaf is decidable.

* $\bot:1\to\Omega$ has a [[complement]].

* The [[real numbers object|object of Dedekind reals]] coincides with the object of [[Dedekind-MacNeille completion|Dedekind-MacNeille reals]].
=--

The first few equivalences are based mainly on the validity of the "law of excluded middle" for elements of the form $\neg a$ in any [[De Morgan Heyting algebra]]. For the rest see e.g. [Johnstone (2002, pp.999-1000)](#Johnstone). The very last point is supplied by [Johnstone (1979)](#Johnstone79).




## Properties

The following shows that 'being De Morgan' is a _local property_ i.e. stable under slicing. This is immediate from the fact that the functor $\mathcal{E}\to\mathcal{E}/A$ sending $X$ to the projection $p_A: X\times A\to A$ is [[logical functor|logical]] hence preserves the various equivalent formulations of De Morgan's law.

+-- {: .num_prop #local_property}
###### Proposition
Let $A$ be an object of the De Morgan topos $\mathcal{E}$. Then the [[slice topos]] $\mathcal{E}/A$ is De Morgan as well.
=--

+-- {: .num_prop #presheaf-deMorgan}
###### Proposition
Let $\mathcal{C}$ be a small category. The [[presheaf topos]] $Set^{\mathcal{C}^{op}}$ is De Morgan precisely if $\mathcal{C}$ satifies the [[Ore condition]].
=--

This result due to [[Peter Johnstone]] appears e.g. in [Johnstone (1979)](#Johnstone79). Compare also the generalizations in [Kock-Reyes (1994)](#KR94) and [Caramello (2012)](#Caramello12).

Since the [[dense topology]] coincides with the [[atomic site|atomic topology]] on $\mathcal{C}$ satisfying the Ore condition the preceding proposition implies that the [[double negation|double negation subtopos]] of a De Morgan presheaf topos $Set^{\mathcal{C}^{op}}$ is always [[atomic topos|atomic]].


### De Morganization

It was discovered by [[Olivia Caramello]] that every topos $\mathcal{E}$ can be associated with a De Morgan topos $Sh_m(\mathcal{E})$, its [[De Morganization]], in a universal way:

+--{: .num_prop #largest_deMorgan}
###### Proposition
Given a topos $\mathcal{E}$. There exists a unique largest [[dense subtopos]] $Sh_m(\mathcal{E})$ of $\mathcal{E}$ that is a De Morgan topos.
=--

For a proof see [Caramello (2009)](#Caramello09). The $m$ that occurs here, refers to the _De Morgan topology_ , cf. [[De Morganization]].

As $Sh_{\neg\neg}(\mathcal{E})$, the sheaf subtopos for the [[double negation|double negation topology]] $\neg\neg$ , is the _smallest_ dense De Morgan subtopos, we see that all dense De Morgan subtoposes lie in the interval between $Sh_{\neg\neg}(\mathcal{E})$ and $Sh_{m}(\mathcal{E})$.

In analogy with [[skeletal geometric morphism|skeletal geometric morphisms]] that preserve $\neg\neg$-sheaves, geometric morphisms $\mathcal{F}\to\mathcal{E}$ that map $m$-sheaves in $\mathcal{F}$ to $m$-sheaves in $\mathcal{E}$ are called $m$_-skeletal_. They occur in the following characterization of De Morgan toposes (cf. [[De Morganization]]):

+--{: .num_prop #deMorgan_m-skeletal}
###### Proposition
A topos $\mathcal{E}$ is De Morgan iff every geometric morphism $\mathcal{F}\to\mathcal{E}$ is $m$-skeletal. $\qed$
=--


### The Gleason cover

Another way to associate a De Morgan topos to an arbitrary topos $\mathcal{E}$ was proposed by [[Peter Johnstone]] in the late 70s (Johnstone [1979b](#Johnstone79b), [1980](#J80)). The so called _Gleason cover_ $\gamma\mathcal{E}$ of $\mathcal{E}$ generalizes a construction in [[topology]] that covers an arbitrary [[space]] by an extremally disconnected topological space.

......


### Relation to cohesion

Given that the [above conditions](#deMorgan_equivalents) concern $1\coprod 1$ and the contractability of $\Omega_{\neg\neg}$ it comes as no surprise that the De Morgan property interacts interestingly with [[Lawvere|Lawvere's]] axiomatic approach to [[cohesion]] and, in particular, with the part of it that concerns the connectedness of the subobject classifier in a cohesive topos of spaces. A first indication of this is the following:

+-- {: .num_prop #omega_connected}
###### Proposition
Let $Set^{\mathcal{C}^{op}}$ be a [[presheaf topos]]. Then its [[subobject classifier]] is connected iff $1\in Set^{\mathcal{C}^{op}}$ is a [[connected]] object and $Set^{\mathcal{C}^{op}}$ is not de Morgan iff there exists a connected object $X\in Set^{\mathcal{C}^{op}}$ such that $1\coprod 1\rightarrowtail X$ .
=--

This result appears in [La Palme-Reyes-Reyes-Zolfaghari (2004, p.220)](#RZZZ04) where it is attributed to [[Lawvere]].

The following result due to [Mielke (1984)](#Mielke84) shows that the De Morgan property coincides with the (local) absence of a non-trivial [[interval object|interval objects]] in a topos.

Here by an interval object we mean an internal linearly ordered object $I$ with disjoint least and greatest elements $m:1\to I$ and $M:1\to I$, respectively, i.e. roughly the sort of thing that is classified by [[sSet]].

An interval object is _trivial_ if $I\simeq I_1\coprod I_2$ and $m,M$ factor through $I_1,I_2$, respectively. A topos $\mathcal{E}$ is said to be **homotopically trivial** if every interval object in $\mathcal{E}$ is trivial, $\mathcal{E}$ is said to _locally homotopically trivial_ if the [[slice topos]] $\mathcal{E}/X$ is homotopically trivial for all $X\in\mathcal{E}$.

+-- {: .num_prop #deMorgan_interval}
###### Proposition
A topos $\mathcal{E}$ is locally homotopically trivial iff $\mathcal{E}$ is a De Morgan topos. If subobjects of $1$ generate, then $\mathcal{E}$ is homotopically trivial iff $\mathcal{E}$ is a De Morgan topos. 
=--

For situations where subobjects of $1$ generate see e.g. [Johnstone (1977, sec.5.3 pp.145ff)](#Johnstone77). For a [[Grothendieck topos]] $\mathcal{E}$, this happens precisely when $\mathcal{E}$ is equivalent to $Sh(L)$ for some [[locale]] $L$. From e.g. [Borceux (1994, p.443)](#Borceux94) it follows then that $Sh(L)$ _is homotopically trivial_ precisely when $L$ is a _De Morgan locale_.


### Relation to model theory

....

+-- {: .num_prop #model_companion}
###### Proposition
Let $\mathcal{T}$ be a coherent theory. Then $\mathcal{T}$ admits a [[model companion]] and $Mod(\mathcal{T})$ has the [[amalgamation property]] iff for each $B\in\mathcal{T}$ , the lattice of subobjects of $B$ admits a negation satisfying $\neg A\vee\neg\neg A = B$.
=--

This result appears without proof in [Harun (1976, p.73)](#Harun96) where it is attributed to a preprint of [[André Joyal]] and [[Gonzalo E. Reyes]].


## Related entries

* [[De Morganization]]
* [[De Morgan Heyting algebra]]
* [[De Morgan category]]
* [[Ore condition]]
* [[double negation]]
* [[topos]]
* [[Boolean topos]]
* [[law of excluded middle]]
* [[skeletal geometric morphism]]
* [[ultrafilter principle]]

## References

* A. Bagchi, _De Morgan's law and related identities in classifying topoi_ , Proc. CT91 pp.1-32, American Mathematical Society 1992.

* A. Bagchi, _Lee Identities in Topoi I_ , JPAA **120** (1997) pp.143-159.

* [[Francis Borceux]], _Handbook of Categorical Algebra vol.3_ , Cambridge UP 1994. (sections 1.2, 7.3)

* {#Caramello09}[[Olivia Caramello]], _De Morgan classifying toposes_ , Adv. in Math. **222** (2009) pp.2117-2144. ([arXiv:0808.1519](http://arxiv.org/abs/0808.1519))

* {#Caramello12}[[Olivia Caramello]], _Topologies for intermediate logics_ , arXiv:1205.2547 (2012). ([arXiv:1205.2547](http://arxiv.org/abs/1205.2547))

* {#CJ09}[[Olivia Caramello]], [[Peter Johnstone]], _De Morgan's law and the Theory of Fields_ , Adv. in Math. **222** (2009) pp.2145-2152. ([arXiv:0808.1572](http://arxiv.org/abs/0808.1572))

* {#Harun76}R. Harun, _Applications of De Morgan toposes and the Gleason cover_ , PhD Montr&#233;al 1996. ([pdf 4.6MB](http://www.collectionscanada.gc.ca/obj/s4/f2/dsk2/ftp04/mq29711.pdf))

* {#Johnstone77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint New York 2014, exercise 5.5.3 p.162)

* {#Johnstone79}[[Peter Johnstone]], _Conditions Related to De Morgan's Law_ , pp.479-491 in LNM **753** Springer Heidelberg 1979.

* {#Johnstone79b}[[Peter Johnstone]], _Another Condition Equivalent to De Morgan's Law_ , Comm. Alg. **7** (1979) pp.1309-1312.

* {#Johnstone80}[[Peter Johnstone]], _The Gleason Cover of a Topos I_ , JPAA **19** (1980) pp.171-192. 

* {#Johnstone81}[[Peter Johnstone]], _The Gleason Cover of a Topos II_ , JPAA **22** (1981) pp.229-247. 

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol. II_, Oxford UP 2002. (section D4.6, pp.998ff)

* {#Johnstone13}[[Peter Johnstone]], _The Gleason Cover of a Realizability Topos_ , TAC **28** no.32 (2013) pp.1139-1152. ([abstract](http://www.tac.mta.ca/tac/volumes/28/32/28-32abs.html))

* {#KR94}[[Anders Kock]], [[Gonzalo E. Reyes]], _Relatively Boolean and De Morgan Toposes and Locales_ , Cah. Top. G&#233;om. Diff. Cat. **35** no.3 (1994) pp.249-261. ([numdam](http://www.numdam.org/numdam-bin/item?id=CTGDC_1994__35_3_249_0))

* {#LawvereMenni15} [[William Lawvere]], [[Matías Menni]], _Internal choice holds in the discrete part of any cohesive topos satisfying stable connected codiscreteness_ , TAC **30** no.26 (2015) pp.909-932. ([abstract](http://www.tac.mta.ca/tac/volumes/30/26/30-26abs.html))

* K. B. Lee, _Equational Classes of Distributed Pseudo-Complemented Lattices_ , Can. J. Math. **22** (1970) pp.881-891. ([pdf](http://cms.math.ca/openaccess/cjm/v22/cjm1970v22.0881-0891.pdf))

* B. Loiseau, M.-M. Mawanda, _On Natural Number Objects, Finiteness and Kripke-Platek Models in Toposes_ , JPAA **61** (1989) pp.257-266.

* {#Mawanda88} M.-M. Mawanda, _Well-ordering and Choice in Toposes_ , JPAA **50** (1988) pp.171-184.

* {#Mielke84} M. V. Mielke, _Homotopically Trivial Toposes_ , Pacific J. Math. **110** no.1 (1984) pp.171-182. ([euclid](https://projecteuclid.org/euclid.pjm/1102711108))

* {#Mielke93} M. V. Mielke, _Topos based homology theory_ , Comment. Math. Univ. Carolinae **34** (1993) pp.549-565. ([pdf](http://www.kurims.kyoto-u.ac.jp/EMIS/journals/CMUC/pdf/cmuc9303/mielke.pdf))

* [[Chris Mulvey]], _The Maximality of Filters_ , JPAA **68** (1990) pp.253-258.

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* M. E. Szabo, _Categorical De Morgan laws_ , Alg. Universalis **12** (1981) pp.93-102.


[[!redirects De Morgan topos]]
[[!redirects de Morgan topos]]
[[!redirects De Morgan topoi]]
[[!redirects de Morgan topoi]]
[[!redirects De Morgan toposes]]
[[!redirects de Morgan toposes]]

[[!redirects DeMorgan topos]]
[[!redirects demorgan topos]]
[[!redirects De Morgan Topos]]

[[!redirects De Morganization]]
[[!redirects De Morganisation]]
[[!redirects De Morganizations]]
[[!redirects De Morganisations]]
