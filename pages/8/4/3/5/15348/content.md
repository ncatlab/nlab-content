
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


##Idea
The _J&#243;nsson-Tarski topos_ is 'the topos analogue of the [[Cantor space]]'.[^fine]

[^fine]: Quote from Bunge&Funk (2006, p.183). 

##Definition
The **J&#243;nsson-Tarski topos** $\mathcal{J}_2$ is the category of [[Jónsson-Tarski algebras]] considered as topos, i.e. its objects are sets $X$ together with an isomorphism $X\to X\times X$ and morphisms are functions that commute with the structure isomorphisms.

##Properties

* $\mathcal{J}_2$ is an example of an [[algebraic variety]] that is also a topos (cf. Johnstone 1985).

* $\mathcal{J}_2=Sh(M_2,J)$ where $M_2$ is the free monoid on two generators $a, b$ and $J$ is the [[coverage]] whose only covering family on the unique object $\cdot$ of $M_2$ is $\{a:\cdot\rightarrow \cdot ,b:\cdot\rightarrow\cdot\}$. So $\mathcal{J}_2$ is in a fact a [[Grothendieck topos]].

* $M_2$, as a free monoid, is cancellative and, accordingly, $\mathcal{J}_2$ is an [[étendue]] ([[Peter Freyd]]). It is discussed from this [[étendue|perspective]] as a [[petit topos]] for _labeled graphs_ in (Lawvere 1989).
* Actually, Freyd showed that $\mathcal{J}_2/F(1)\cong Sh(\mathcal{X})$ with $F(1)$ the free J&#243;nsson-Tarski algebra on one generator and $\mathcal{X}$ the [[Cantor space]] - this motivates the above quote from Bunge&Funk: $\mathcal{J}_2$ looks locally like (the sheaf topos on) $\mathcal{X}$ !

##Generalizations
The idea to consider generalizations of $\mathcal{J}_2$ seemed to have appeared first in the context of work on &#233;tendues (Rosenthal 1981, Lawvere 1989).

+-- {: .query}
Caveat: this entry is still in progress!
=--

##References

* [[Marta Bunge]], [[Jonathon Funk]], _Singular Coverings of Toposes_ , Springer LNM vol. 1890, Heidelberg 2006.

* [[Peter Johnstone]], _When is a Variety a Topos?_ , Algebra Universalis **21** (1985) pp.198-212.

* [[Peter Johnstone]], _Collapsed Toposes as Bitopological Spaces_ , pp.19-35 in _Categorical Topology_ , World Scientific Singapore 1989.

* [[Peter Johnstone]], _Collapsed Toposes and Cartesian Closed Varieties_ , JA **129** (1990) pp.446-480.

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. I_ , Oxford UP 2002. (sec. A2.1, p.80)

* [[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* [[Tom Leinster]], _J&#243;nsson-Tarski toposes_, Talk Nice 2007 ([slides](http://www.maths.ed.ac.uk/~tl/nice/jt.pdf))

* [[Kimmo I. Rosenthal]], _&#201;tendues and Categories with Monic Maps_ , JPAA **22** (1981) pp.193-212.

* James Worrell, _A Note on Coalgebras and Presheaves_ , Electronic Notes in Theoretical Computer Science **65** no.3 (2003) pp.1-10.


[[!redirects Jonsson-Tarski topos]]
[[!redirects Jonsson-Tarski Topos]]