
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Superalgebra
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

In [[super-algebra|super]]-[[representation theory]], what is called _adinkras_ ([Faux-Gates 04](#FauxGates04)) is a graphical tool for denoting those [[representations]] ([[super multiplets]]) of the $\mathcal{N}$-extended [[supersymmetry]] algebras in one dimension ([[supersymmetric quantum mechanics]] with [[number of supersymmetries|N supersymmetries]]) for which the [[supersymmetry]] generators act, up to [[derivatives]] and prefactors, by [[permutation]] of [[superfield]] components. These are called _adinkraic_ representations ([Zhang 13, p. 16](#Zhang13)). 

While adinkraic representations are special among all representations of the 1-dimensional $\mathcal{N}$-extended supersymmetry algebra, the idea is that the [[dimensional reduction]] of representations ([[supermultiplets]]) of higher dimensional supersymmetry algebras down to 1d are of this form, at least for dimensional reduction from $d = 4$ and $N = \mathbf{4}$ ([GGMPPRW 09, section 3](#GGMPPRW09), [Gates-Hubsch-Stiffler 14](#GatesHubschStiffler14)).

The classification of adinkras, and hence of adinkraic representations, turns out to be controlled by [[linear codes]] ([Doran & Faux & Gates & HubschIgaLandweberMiller 11](#DoranFauxGatesHubschIgaLandweberMiller11)) and to be related to certain special [[super Riemann surfaces]] via [[dessins d'enfants]] ([Doran & Iga & Landweber & Mendez-Diez 13](#DoranIgaLandweberMendez-Diez13), [Doran & Iga & Kostiuk &Mendes-Diez 16](#DoranIgaKostiukMendes-Diez16)).

## Definition

For background, see at _[[geometry of physics -- supersymmetry]]_.

For $N \in \mathbb{N}$, write $\mathbb{R}^{1 \vert N}$
for the [[super Lie algebra]] over the [[real numbers]] that is spanned by a single generator $P$ in even (i.e., bosonic) degree and $N$ generators $Q_I$, $I \in \{1, 2, \cdots, N\}$ in odd (i.e., fermionic) degree, whose only non-trivial components of the super-[[Lie bracket]] are

$$
  [Q_I, Q_J]  = 2 \delta_{I J} P
  =
  \left\{
   \array{
      2 P & \vert & I = J
      \\
      0 & \vert & \text{otherwise}
   }
  \right.
$$

This is the 1-dimensional $N$-extended [[super translation super Lie algebra]]. We may think of this as the super-translational symmetry of 1-dimensional $N$-extended [[super Minkowski spacetime]].

Consider then super [[Lie algebra representations]] of $\mathbb{R}^{1 \vert N}$ on [[super vector spaces]] of smooth [[superfields]] on $\mathbb{R}^{1 \vert N}$ (regarded as a [[supermanifold]]) and such that the bosonic generator $P$ acts as the [[derivative]] operator on [[smooth functions]] on $\mathbb{R}^1$ in each component. If in addition the representation is such that in the canonical [[linear basis]] the odd generators $Q_I$ send even/odd basis elements $\phi_i$ to single odd/even basis elements $\psi_j$ (as opposed to [[linear combinations]] of them), hence if the $Q_I$ act apart from degree-shift and possibly [[differentiation]] by [[permutations]] on the components of the [[superfields]], then this representation of $\mathbb{R}^{1\vert N}$ is called _adinkraic_. ([Zhang 13, p. 16](#Zhang13)).

The corresponding _adinkra_ is the [[bipartite graph]] which expresses these permutations:

<img src="https://ncatlab.org/nlab/files/AdinkraRule.png" width="600">

> table grabbed from [Doran & Iga & Landweber & Mendez-Diez 13, p. 7](#DoranIgaLandweberMendez-Diez13)


<img src="https://ncatlab.org/nlab/files/1dAdinkraExample.png" width="600">

> graphics grabbed from [Iga-Zhang 15, p. 3](#IgaZhang15)

## Classification

The topology of an adinkra graph together with its edge coloring in $\{1,2, \cdots, N\}$ is called its _chromotopology_.

The set of adinkra chromotopologies is equivalent to the set of colored $N$-cubs modulo doubly even length-$N$ [[linear codes]] ([Doran-Faux-Gates-Hubsch-Iga-Landweber-Miller 11](#DoranFauxgatesHubschIgaLandweberMiller11))


(A [[linear code]] of length $N$ is a [[linear subspace]] of $(\mathbb{F}_2)^N$ for $\mathbb{F}_2$ the [[prime field]] with two elements and it is _doubly even_ if every element has weight a multiple of 4. )

see [Zhang 13, chapter 2](#Zhang13)


<img src="https://ncatlab.org/nlab/files/AdinkrasFromCode.png" width="600">


> graphics grabbed from [Iga-Zhang 15, p. 4](#IgaZhang15)

## From supermultiplets in higher dimensions

The [[dimensional reduction]] of the smallest [[supermultiplets]] of $d = 4, N = \mathbf{4}$ supersymmetry down to 1d yield adinkraic representations ([GGMPPRW 09, section 3](#GGMPPRW09), [Gates-Hubsch-Stiffler 14](#GatesHubschStiffler14)).

Corresponding adinkras for the chiral scalar supermultiplet (CM), the vector multiplet (VM) and the tensor multiplet (TM) look as follows:

<img src="https://ncatlab.org/nlab/files/AdinkrasFrom4d.png" width="450">


## References

For an introduction to adinkras, see the talk

* [[Lutian Zhao]], _What is an Adinkra?_, 2014 ([slides](http://math.sjtu.edu.cn/conference/Bannai/2014/data/20141213B/slides.pdf))

The concept of adinkras was introduced into [[supersymmetry]] [[representation theory]] in 

* {#FauxGates04} [[Michael Faux]], [[Jim Gates]], _Adinkras: A Graphical Technology for Supersymmetric Representation Theory_, Phys.Rev. D71 (2005) 065002 ([hep-th/0408004](https://arxiv.org/abs/hep-th/0408004))

and further developed in the article

* [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], _On Graph-Theoretic Identifications of Adinkras, Supersymmetry Representations and Superfields_, Int. J. Mod. Phys. A22: 869-930, 2007 ([arXiv:math-ph/0512016](https://arxiv.org/abs/math-ph/0512016))

and many more ("DFGHIL collaboration"). For instance the relation to Clifford supermodules is discussed in

* [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], _Off-shell supersymmetry and filtered Clifford supermodules_ ([arXiv:math-ph/0603012](https://arxiv.org/abs/math-ph/0603012))

kinetic terms are discussed in 

* [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], _Adinkras and the Dynamics of Superspace Prepotentials_ ([arXiv:hep-th/0605269](https://arxiv.org/abs/hep-th/0605269))

The classification of adinkras in terms of [[graphs]] and [[linear codes]] is due to

* {#DoranFauxGatesHubschIgaLandweberMiller11} [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], R. L. Miller, _Codes and Supersymmetry in One Dimension_, Adv. in Th. Math. Phys. 15 (2011) 1909-1970 ([arXiv:1108.4124](https://arxiv.org/abs/1108.4124))

and discussed in mathematical detail in

* {#Zhang11} [[Yan X Zhang]], _Adinkras for Mathematicians_ ([arXiv:1111.6055](https://arxiv.org/abs/1111.6055))

* {#Zhang13} [[Yan X Zhang]], _The combinatorics of Adinkras_, PhD thesis, MIT (2013) ([pdf](http://math.mit.edu/~yanzhang/math/thesis_adinkras.pdf))

The [[dimensional reduction]] of the standard [[supermultiplets]] of $D = 4, \mathcal{N} = 1$ supersymmetry to adinkraic representations of $D = 1, \mathcal{N}=4$ is due to

* {#GGMPPRW09} [[Jim Gates]], J. Gonzales, B. MacGregor, J. Parker, R. Polo-Sherk, V.G.J. Rodgers, L. Wassink, _$4D$, $N = 1$ Supersymmetry Genomics (I)_, JHEP 0912:008,2009 ([arXiv:0902.3830](https://arxiv.org/abs/0902.3830))

* {#GatesHubschStiffler14} [[Jim Gates]], [[Tristan Hübsch]], Kory Stiffler, _Adinkras and SUSY Holography_, Int. J. Mod. Phys. A29 no. 7, (2014) 1450041 ([arXiv:1208.5999](https://arxiv.org/abs/1208.5999))

See also

* {#IgaZhang15} [[Kevin Iga]], [[Yan Zhang]], _Structural Theory of 2-d Adinkras_ ([arXiv:1508.00491](https://arxiv.org/abs/1508.00491))

Discussion for $D=11$, $\mathcal{N}=1$:

* [[Jim Gates]], Yangrui Hu, S.-N. Hazel Mak, _Adinkra Foundation of Component Decomposition and the Scan for Superconformal Multiplets in 11D, $\mathcal{N} = 1$ Superspace_ ([arXiv:2002.08502](https://arxiv.org/abs/2002.08502))




The relation of adinkras to special [[super Riemann surfaces]] via [[dessins d'enfants]] is due to

* {#DoranIgaLandweberMendez-Diez13} [[Charles Doran]], [[Kevin Iga]], [[Greg Landweber]], [[Stefan Méndez-Diez]], _Geometrization of $\mathcal{N}$-Extended 1-Dimensional Supersymmetry Algebras_ ([arXiv:1311.3736](https://arxiv.org/abs/1311.3736))

* {#DoranIgaKostiukMendes-Diez16} [[Charles Doran]], [[Kevin Iga]], Jordan Kostiuk, [[Stefan Méndez-Diez]], _Geometrization of $\mathcal{N}$-Extended 1-Dimensional Supersymmetry Algebras II_ ([arXiv:1610.09983](https://arxiv.org/abs/1610.09983))

Further developments includes

* {#CalkinsGatesGatesStiffler15} Mathew Calkins, D. E. A. Gates, [[Jim Gates]] Jr., Kory Stiffler, _Adinkras, 0-branes, Holoraumy and the SUSY QFT/QM Correspondence_ ([arXiv:1501.00101](https://arxiv.org/abs/1501.00101))

Discussion in the context of [[spectral triples]] is in

* [[Matilde Marcolli]], Nick Zolman, _Adinkras, Dessins, Origami, and Supersymmetry Spectral Triples_ ([arXiv:1606.04463](https://arxiv.org/abs/1606.04463))

See also


* Wes Caldwell, Alejandro Diaz, Isaac Friend, [[Jim Gates]], Jr., Siddhartha Harmalkar, Tamar Lambert-Brown, Daniel Lay, Karina Martirosova, Victor Meszaros, Mayowa Omokanwaye, Shaina Rudman, Daniel Shin, Anthony Vershov, _On the Four Dimensional Holoraumy of the $4D$, $\mathcal{N} = 1$ Complex Linear Supermultiplet_ ([arXiv:1702.05453](https://arxiv.org/abs/1702.05453))

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Adinkra_symbols_(physics)">Adinkra symbols (physics)</a>_


[[!redirects adinkras]]

[[!redirects adinkraic representation]]
[[!redirects adinkraic representations]]




