
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

Let $(R, \lt)$ be a [[dense linear order|dense]] [[linear order]] without [[bounded order|endpoints]]. An order-minimal or **o-minimal structure** on $R$ is a [[structure (model theory)|structure]] $\mathcal{S}$ on $R$ such that 

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

## Relation to number theory and arithmetic geometry

The theory of o-minimal structures has applications to [[number theory]] and [[arithmetic geometry]], for example via the Pila-Wilkie theorem, which is used in proofs of Lang's conjecture, the Manin-Mumford conjecture, and the Andre-Oort conjecture (see [Tsimerman19](#Tsimerman19)).

## Links

* wikipedia [o-minimal theory](http://en.wikipedia.org/wiki/O-minimal_theory)

## References 

General:

* Michel Coste, _An introduction to O-minimal geometry_ , Lecture notes Pisa 1999. ([pdf](http://perso.univ-rennes1.fr/michel.coste/polyens/OMIN.pdf))

* [[Lou van den Dries]], _Exponential rings, exponential polynomials and exponential functions_ , Pacific Journal of Mathematics **113** no.1 (1984) pp.51&#8211;66. ([pdf](http://projecteuclid.org/download/pdf_1/euclid.pjm/1102709376))

* Lou van den Dries, _Tame topology and O-minimal structures_, London Math. Soc. Lecture Notes Series 248, Cambridge U. Press 1998. 

* [[Alexandre Grothendieck]], _Esquisse d'un Programme_, section 5. English translation available in Geometric Galois Actions I (edited by L. Schneps and P. Lochak), LMS Lecture Notes Ser. 242, CUP 1997. 

* Alessandro Berarducci, _Definable groups in o-minimal structures_, [pdf](http://www.dm.unipi.it/~dinasso/marian2004/berarducci.pdf); _Cohomology of groups in o-minimal structures: acyclicity of the infinitesimal subgroup_, J. Symbolic Logic __74__:3 (2009), 891-900, [MR2548466](http://www.ams.org/mathscinet-getitem?mr=2548466), [euclid](http://projecteuclid.org/euclid.jsl/1245158089), [doi](https://doi.org/10.2178/jsl/1245158089).

* Alessandro Berarducci, _O-minimal spectra, infinitesimal subgroups and cohomology_, J. Symbolic Logic __72__ (2007), no. 4, pp. 1177--1193, [MR2371198](http://www.ams.org/mathscinet-getitem?mr=2371198), [euclid](http://projecteuclid.org/euclid.jsl/1203350779 ), [doi](https://doi.org/10.2178/jsl/1203350779).

* M. Edmundo, G. O. Jones, N. J. Peatfield, _Sheaf cohomology in o-minimal structures_, J. Math. Logic __6__ (2006), no. 2, pp. 163--179, [MR2317425](http://www.ams.org/mathscinet-getitem?mr=2317425), [doi](https://doi.org/10.1142/S0219061306000566)

* Mario J. Edmundo, Luca Prelli, _Invariance of o-minimal cohomology with definably compact supports_, Confluentes Mathematici 7, n. 1 (2015) 35-53 [arxiv/1205.6124](http://arxiv.org/abs/1205.6124) [doi](https://doi.org/10.5802/cml.17)

* M. J. Edmundo, N. J. Peatfield, _O-minimal Čech cohomology_, (2006) [pdf](https://repositorioaberto.uab.pt/bitstream/10400.2/2839/1/ConstCech.pdf)

* Ricardo Bianconi, Rodrigo Figueiredo, _O-minimal de Rham cohomology_, [arxiv/1904.05485](https://arxiv.org/abs/1904.05485)

* Olivier Le Gal, Jean-Philippe Rolin, _An o-minimal structure which does not admit $C^{\infty }$ cellular decomposition_, Annales de l'institut Fourier __59__:2 (2009), p. 543-562, [MR2521427](http://www.ams.org/mathscinet-getitem?mr=2521427) [Zbl 1193.03065](http://www.zentralblatt-math.org/zmath/en/search/?q=an:1193.03065) [numdam](http://www.numdam.org/item?id=AIF_2009__59_2_543_0)

* Thomas Scanlon, _Algebraic differential equations from covering maps_, Adv. Math. __330__ (2018) 1071-1100 [doi](https://doi.org/10.1016/j.aim.2018.03.008)
* Benjamin Bakker, Yohan Brunebarbe, Jacob Tsimerman, _o-minimal GAGA and a conjecture of Griffiths_, [arxiv/1811.12230](https://arxiv.org/abs/1811.12230)

* [[Reid Barton]], Johan Commelin, _Model categories for o-minimal geometry_ ([arXiv:2108.11952](https://arxiv.org/abs/2108.11952))

* {#Tsimerman19} Jacob Tsimerman, _Functional transcendence results and arithmetic applications_, Proceedings of the International Congress of Mathematicians (ICM 2018), pp. 435-454 (2019) [doi](https://doi.org/10.1142/9789813272880_0062) [pdf] (https://eta.impa.br/dl/091.pdf)

In Physics, the concept of [[tame topology]] and [[o-minimal structures]] appears in a proposal for a finiteness condition in [[QFT]] in

* [[Michael Douglas]], [[Thomas Grimm]], and Lorenz Schlechter. *The Tameness of Quantum Field Theory, Part I--Amplitudes.* (2022)([arXiv:2210.10057](https://arxiv.org/abs/2210.10057)).

* [[Michael Douglas]], [[Thomas Grimm]], and Lorenz Schlechter. *The Tameness of Quantum Field Theory, Part II--Structures and CFTs* (2023) ([arXiv:2302.04275] (https://arxiv.org/abs/2302.04275)).

[[!redirects O-minimal structure]]
[[!redirects o-minimal structures]]
[[!redirects order-minimal structure]]
[[!redirects order-minimal structures]]
[[!redirects o-minimal theory]]
[[!redirects o-minimal theories]]
