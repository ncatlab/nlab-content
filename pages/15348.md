
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

* $\mathcal{J}_2$ is an example of an [[variety of algebras]] that is also a topos (cf. Johnstone 1985).

* $\mathcal{J}_2=Sh(M_2,J)$ where $M_2$ is the free monoid on two generators $a, b$ and $J$ is the [[coverage]] whose only covering family on the unique object $\cdot$ of $M_2$ is $\{a:\cdot\rightarrow \cdot ,b:\cdot\rightarrow\cdot\}$. So $\mathcal{J}_2$ is in a fact a [[Grothendieck topos]].

* $M_2$, as a free monoid, is cancellative, hence all-monic and, accordingly, $\mathcal{J}_2$ is an [[étendue]] ([[Peter Freyd]]). It is discussed from this [[étendue|perspective]] as a [[petit topos]] for _labeled graphs_ in (Lawvere 1989).

* Actually, Freyd observed that $\mathcal{J}_2/F(1)\cong Sh(2^\mathbb{N})$ with $F(1)$ the free J&#243;nsson-Tarski algebra on one generator and $2^\mathbb{N}$ the [[Cantor space]] - this motivates the above quote from Bunge&Funk: $\mathcal{J}_2$ looks locally like (the sheaf topos on) $2^\mathbb{N}$ ! $Sh(2^\mathbb{N})$ classifies ' subsets of $\mathbb{N}$ ' in the sense that for cocomplete $\mathcal{E}$ geometric morphisms $\mathcal{E}\to Sh(2^\mathbb{N})$ correspond to morphisms $\Delta(\mathbb{N})\to\Delta(2)$ in $\mathcal{E}$, with $\Delta$ the [[constant sheaf functor]] (cf. [Mac Lane& Moerdijk](#MacLaneMoerdijk), ex.VIII.10, pp.470-71, ex.X.6, pp.572-73).

##Generalizations

The idea to consider generalizations of $\mathcal{J}_2$ seemed to have appeared first in the context of work on &#233;tendues (Rosenthal 1981, Lawvere 1989).

###Rosenthal's approach

K. Rosenthal (1981) starts from two basic facts about &#233;tendues, namely that $Set^{\mathcal{C}^{op}}$ is an [[étendue]] iff all morphisms in $\mathcal{C}$ are monic, and that $Sh(\mathcal{E},J)$ is an &#233;tendue if $\mathcal{E}$ is an &#233;tendue. His goal is to construct &#233;tendues
from an all-monic $\mathcal{C}$ by defining a topology $J$ on $Set^{\mathcal{C}^{op}}$ from a functor $H:\mathcal{C}\to Set$ satisfying:

1. $H(f)$ is monic ,and

2. if $x\in Im(H(f))\cap Im(H(g))$ then there is $k\in\mathcal{C}$ with $k\leq f$ and $k\leq g$ such that $x\in Im(H(k))$.

Now given $X\in\mathcal{C}$ and a sieve $B\in\Omega(X)$ define a sieve 

$j_X(B):=\{\quad f\in\mathcal{C}| cod(f)=X\quad\wedge\quad Im(H(f))\subseteq\bigcup _{g\in B} Im(H(g))\quad\}.$

The resulting map $j:\Omega\to\Omega$ is a topology.

For $\mathcal{C}^{op}=\mathcal{M}_2$, the free monoid on two generators, and $H(X)=2^\mathbb{N}$, the functor constantly the Cantor set, this yields $\mathcal{J}_2$.

The generalization to $\mathcal{C}^{op}=\mathcal{M}_\infty$, the free monoid on countably infinite many generators, and the [[Baire space of sequences|Baire space]] $\mathbb{B}=\mathbb{N}^\mathbb{N}$ exhibits the **infinite J&#243;nsson-Tarski topos** $\mathcal{J}_\infty$, i.e. the category of sets $A$ with an isomorphism to $A^\mathbb{N}$, as $Sh(\mathbb{N}^\mathbb{N})$ locally.

### Jónsson-Tarski toposes via profunctors

Work on a categorical concept of self-similarity led T. Leinster (2007) to another generalization of the Jónsson-Tarski topos. He starts from the observation that any profunctor $M:\mathcal{A} &#8696;\mathcal{B}$ comes with an adjunction $-\otimes M\dashv [M,-]:Set^{\mathcal{A}^{op}}\to Set^{\mathcal{B}^{op}}$ where the left adjoint stems from profunctor composition and the right adjoint is defined for presheaves $X\in Set^{\mathcal{B}^{op}}$ and $a\in \mathcal{A}$ as $[ M,X ] (a) := Nat(M(-,a),X)$ i.e. the set of natural transformations from $M(-,a)$ to $X$ or, in other words, $Hom(M(-,a),X)$ in $Set^{\mathcal{B}^{op}}$.

For an endoprofunctor $M:\mathcal{A} &#8696;\mathcal{A}$ define a **J&#243;nsson-Tarski M-algebra** as a pair $(X,\xi)$ where $X\in Set^{\mathcal{A}^{op}}$ and $\xi$ a natural isomorphism $X\overset{\simeq}{\to} [M,X]$. The resulting category $\mathcal{J}_M$ is a topos since a site $(\mathcal{A}_M,J)$ can be constructed from $\mathcal{A}$ by adjoining new arrows $b\overset{m}{\to} a$ for each $b,a\in\mathcal{A}$ and $m\in M(b,a)$ with covers $J(a)$ the set of these arrows (cf. Worrell 2002, Leinster 2007). Furthermore, $\mathcal{J}_M$ is monadic over $Set^{\mathcal{A}^{op}}$.

The classical J&#243;nsson-Tarski topos $\mathcal{J}_2$ arises from this process by taking $M=\mathbf{2}:\mathbf{1} &#8696;\mathbf{1}$ assigning to the unique object $(\bullet,\bullet)$ of the category $\mathbf{1}\times\mathbf{1}$ the two element set $\{\star,\ast\}$. A presheaf on $\mathbf{1}$ is just a set $X$ whence $[\mathbf{2}, X](\bullet)$ is just the set of all maps $\{\star,\ast\}\to X$ i. e. $X\times X$. The site for it is the free category generated by the graph with one node $\bullet$ and two edges $\star,\ast$ i. e. the free monoid on two generators and with coverage $\{\star,\ast\}$.


## Related entries

* [[Jónsson-Tarski algebra]]

* [[Cantor space]]

##Link

Some further properties of $\mathcal{J}_2$ are discussed in the answer to this

* [MO-question](https://mathoverflow.net/questions/396041/images-of-complemented-subobjects-in-hyperconnected-toposes-over-boolean-bases/396043?r=SearchResults&s=1|33.5942#396043)


##References

* [[Marta Bunge]], [[Jonathon Funk]], _Singular Coverings of Toposes_ , Springer LNM vol. 1890, Heidelberg 2006.

* [[Peter Johnstone]], _When is a Variety a Topos?_ , Algebra Universalis **21** (1985) pp.198-212.

* [[Peter Johnstone]], _Collapsed Toposes as Bitopological Spaces_ , pp.19-35 in _Categorical Topology_ , World Scientific Singapore 1989.

* [[Peter Johnstone]], _Collapsed Toposes and Cartesian Closed Varieties_ , JA **129** (1990) pp.446-480.

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. I_ , Oxford UP 2002. (sec. A2.1, p.80)

* [[Peter Johnstone|P. T. Johnstone]], A. J. Power, T. Tsujishita, H. Watanabe, J. Worrell, _The structure of categories of coalgebras_ , Theoret. Comp. Sci **260** (2001) pp.87-117.

* [[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* [[Tom Leinster]], _J&#243;nsson-Tarski toposes_, Talk Nice 2007.  ([slides](http://www.maths.ed.ac.uk/~tl/nice/jt.pdf))

* [[Saunders Mac Lane|S. Mac Lane]], [[Ieke Moerdijk|I. Moerdijk]], _Sheaves in Geometry and Logic_ , Springer Heidelberg 1994.{#MacLaneMoerdijk} (pp.470-471)

* [[Kimmo I. Rosenthal]], _&#201;tendues and Categories with Monic Maps_ , JPAA **22** (1981) pp.193-212.

* James Worrell, _A Note on Coalgebras and Presheaves_ , Electronic Notes in Theoretical Computer Science **65** no.3 (2003) pp.1-10.


[[!redirects Jonsson-Tarski topos]]
[[!redirects Jonsson-Tarski Topos]]