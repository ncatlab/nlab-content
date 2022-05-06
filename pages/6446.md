
# Contents
* automatic table of contents goes here
{: toc}

## Definition 

Let $(R, \lt)$ be a [[dense order|dense]] [[linear order]] without [[bounded order|endpoints]]. An order-minimal or **o-minimal structure** on $R$ is a [[structure (model theory)|structure]] $\mathcal{S}$ on $R$ such that 

* The relation $\lt$ belongs to $\mathcal{S}_2$; 

* The elements of $\mathcal{S}_1$ are precisely finite unions of points and intervals in $R$. 

Here an interval can mean a set of the form $I_{a, b} = \{x \in R: a \lt x \lt b\}$, or $I_{\downarrow a} = \{x \in R: x \lt a\}$, or $I_{\uparrow a} = \{x \in R: a \lt x\}$. 


## Commentary 

A structure on a set $R$ can be thought of as the collection $\mathcal{S} = \bigcup_n \mathcal{S}_n$ of sets that are definable with respect to a one-sorted first-order language $L$ with a given interpretation in $R$. Thus $\mathcal{S}_n$ is the collection of subsets of $R^n$ which are defined by $n$-ary predicates in $L$. The definition of o-minimal structure supposes that $L$ contains a relation symbol $\lt$, and that $\lt$ is interpreted in $R$ as a dense linear order without endpoints. 

The o-minimality condition places a sharp restriction on which subsets of $R$ can be defined in the language. Essentially, it means that the only definable subsets of $R$ are those which are definable in terms of constants and the predicates $\lt$ and $=$. 

The archetypal example of an o-minimal structure is that of [[semi-algebraic set]]s defined over $\mathbb{R}$ (which form a structure due to the [[semialgebraic set|Tarski-Seidenberg theorem]]). 

Remarkably, quite a lot can be said about the structure of definable sets in an o-minimal structure over $\mathbb{R}$, and this is a very active area of model theory. The notion of o-minimal structure has been proposed as a reasonable candidate for an axiomatic approach to Grothendieck's hoped-for "[[tame topology]]" ( _topologie mod&#233;r&#233;e_ ). 

## O-minimal theories

A [[theory]] is o-minimal if every model $M$ of $T$ is an o-minimal structure. 

## Links

* wikipedia [o-minimal theory](http://en.wikipedia.org/wiki/O-minimal_theory)

## References 

* Michel Coste, _An Introduction to O-Minimal Geometry_ , Lecture notes Pisa 1999. ([pdf](http://perso.univ-rennes1.fr/michel.coste/polyens/OMIN.pdf))

* [[Lou van den Dries]], _Exponential rings, exponential polynomials and exponential functions_ , Pacific Journal of Mathematics **113** no.1 (1984) pp.51&#8211;66. ([pdf](http://projecteuclid.org/download/pdf_1/euclid.pjm/1102709376))

* Lou van den Dries, _Tame topology and O-minimal structures_, London Math. Soc. Lecture Notes Series 248, Cambridge U. Press 1998. 

* [[Alexandre Grothendieck]], _Esquisse d'un Programme_, section 5. English translation available in Geometric Galois Actions I (edited by L. Schneps and P. Lochak), LMS Lecture Notes Ser. 242, CUP 1997. 

* Alessandro Berarducci, _Definable groups in o-minimal structures_, [pdf](http://www.dm.unipi.it/~dinasso/marian2004/berarducci.pdf); _Cohomology of groups in o-minimal structures: acyclicity of the infinitesimal subgroup_, J. Symbolic Logic __74__:3 (2009), 891-900, [MR2548466](http://www.ams.org/mathscinet-getitem?mr=2548466), [euclid](http://projecteuclid.org/euclid.jsl/1245158089), [doi](http://dx.doi.org/10.2178/jsl/1245158089).

* Alessandro Berarducci, _O-minimal spectra, infinitesimal subgroups and cohomology_, J. Symbolic Logic __72__ (2007), no. 4, pp. 1177--1193, [MR2371198](http://www.ams.org/mathscinet-getitem?mr=2371198), [euclid](http://projecteuclid.org/euclid.jsl/1203350779 ), [doi](http://dx.doi.org/10.2178/jsl/1203350779).

* M. Edmundo, G. O. Jones, N. J. Peatfield, _Sheaf cohomology in o-minimal structures_, J. Math. Logic __6__ (2006), no. 2, pp. 163--179, [MR2317425](http://www.ams.org/mathscinet-getitem?mr=2317425), [doi](http://dx.doi.org/10.1142/S0219061306000566)

* Mario J. Edmundo, Luca Prelli, _Invariance of o-minimal cohomology with definably compact supports_, Confluentes Mathematici 7, n. 1 (2015) 35-53 [arxiv/1205.6124](http://arxiv.org/abs/1205.6124) [doi](https://doi.org/10.5802/cml.17)

* Olivier Le Gal, Jean-Philippe Rolin, _An o-minimal structure which does not admit $C^{\infty }$ cellular decomposition_, Annales de l'institut Fourier __59__:2 (2009), p. 543-562, [MR2521427](http://www.ams.org/mathscinet-getitem?mr=2521427) [Zbl 1193.03065](http://www.zentralblatt-math.org/zmath/en/search/?q=an:1193.03065) [numdam](http://www.numdam.org/item?id=AIF_2009__59_2_543_0)

* Thomas Scanlon, _Algebraic differential equations from covering maps_, Adv. Math. __330__ (2018) 1071-1100 [doi](https://doi.org/10.1016/j.aim.2018.03.008)
* Benjamin Bakker, Yohan Brunebarbe, Jacob Tsimerman, _o-minimal GAGA and a conjecture of Griffiths_, [arxiv/1811.12230](https://arxiv.org/abs/1811.12230)


[[!redirects O-minimal structure]]
[[!redirects o-minimal structures]]
[[!redirects order-minimal structure]]
[[!redirects order-minimal structures]]
[[!redirects o-minimal theory]]
[[!redirects o-minimal theories]]
