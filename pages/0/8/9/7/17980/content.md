
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

In [[super-algebra|super]]-[[representation theory]], what is called _adinkras_ ([Faux & Gates 2004](#FauxGates04)) is a graphical tool for denoting those [[representations]] ([[super multiplets]]) of the $\mathcal{N}$-extended [[supersymmetry]] algebras in *one* ([[time]]) dimension ([[supersymmetric quantum mechanics]] with [[number of supersymmetries|N supersymmetries]]) for which the [[supersymmetry]] generators act, up to [[derivatives]] and prefactors, by [[permutation]] of [[superfield]] components. These are called _adinkraic_ representations ([Zhang 2013, p. 16](#Zhang13)). 

While adinkraic representations are special among all representations of the 1-dimensional $\mathcal{N}$-extended supersymmetry algebra, the idea is that the [[dimensional reduction]] of representations ([[supermultiplets]]) of higher dimensional supersymmetry algebras down to 1d are of this form, at least for dimensional reduction from $d = 4$ and $N = \mathbf{4}$ ([GGMPPRW 2009, section 3](#GGMPPRW09), [Gates, Hubsch & Stiffler 2014](#GatesHubschStiffler14)).

The classification of adinkras, and hence of adinkraic representations, turns out to be controlled by [[linear codes]] ([Doran, Faux, Gates et al. 2011](#DoranFauxGatesHubschIgaLandweberMiller11)) and to be related to certain special [[super Riemann surfaces]] via [[dessins d'enfants]] ([Doran, Iga, Landweber & Mendez-Diez 13](#DoranIgaLandweberMendez-Diez13), [Doran, Iga,  Kostiuk & Mendes-Diez 2016](#DoranIgaKostiukMendes-Diez16)).


## Definition

> For general background, see at _[[geometry of physics -- supersymmetry]]_.

For $N \in \mathbb{N}$, write $\mathbb{R}^{1 \vert N}$
for the [[super Lie algebra]] over the [[real numbers]] that is spanned by a single generator $P$ in even (i.e., bosonic) degree and $N$ generators $Q_I$, $I \in \{1, 2, \cdots, N\}$ in odd (i.e., fermionic) degree, whose only non-trivial components of the [[super Lie algebra|super-]][[Lie bracket]] are

$$
  [Q_I, Q_J]  
  \,=\, 
  2 \delta_{I J} P
  \,=\,
  \left\{
   \array{
      2 P & \vert & I = J
      \\
      0 & \vert & \text{otherwise}
   }
  \right.
$$

This is the 1-dimensional $N$-extended [[super translation super Lie algebra]]. We may think of this as the super-translational symmetry of 1-dimensional $N$-extended [[super Minkowski spacetime]].

Consider then super [[Lie algebra representations]] of $\mathbb{R}^{1 \vert N}$ on [[super vector spaces]] of smooth [[superfields]] on $\mathbb{R}^{1 \vert N}$ (regarded as a [[supermanifold]]) and such that the bosonic generator $P$ acts as the [[derivative]] operator on [[smooth functions]] on $\mathbb{R}^1$ in each component. If in addition the representation is such that in the canonical [[linear basis]] the odd generators $Q_I$ send even/odd basis elements $\phi_i$ to single odd/even basis elements $\psi_j$ (as opposed to [[linear combinations]] of them), hence if the $Q_I$ act apart from degree-shift and possibly [[differentiation]] by [[permutations]] on the components of the [[superfields]], then this representation of $\mathbb{R}^{1\vert N}$ is called _adinkraic_. ([Zhang 2013, p. 16](#Zhang13)).

The corresponding _adinkra_ is the [[bipartite graph]] which expresses these permutations:

<img src="https://ncatlab.org/nlab/files/AdinkraRule.png" width="600">

> table grabbed from [Doran, Iga, Landweber & Mendez-Diez 2013, p. 7](#DoranIgaLandweberMendez-Diez13)


<img src="https://ncatlab.org/nlab/files/1dAdinkraExample.png" width="600">

> graphics grabbed from [Iga & Zhang 2015, p. 3](#IgaZhang15)

## Classification

The topology of an adinkra graph together with its edge coloring in $\{1,2, \cdots, N\}$ is called its _chromotopology_.

The set of adinkra chromotopologies is equivalent to the set of colored $N$-cubs modulo doubly even length-$N$ [[linear codes]] ([Doran, Faux, Gates, Hubsch, Iga, Landweber & Miller 2011](#DoranFauxgatesHubschIgaLandweberMiller11)).


(A [[linear code]] of length $N$ is a [[linear subspace]] of $(\mathbb{F}_2)^N$ for $\mathbb{F}_2$ the [[prime field]] with two elements and it is _doubly even_ if every element has weight a multiple of 4.)

see [Zhang 2013, chapter 2](#Zhang13)


<img src="https://ncatlab.org/nlab/files/AdinkrasFromCode.png" width="600">


> graphics grabbed from [Iga & Zhang 2015, p. 4](#IgaZhang15)


## From supermultiplets in higher dimensions

The [[dimensional reduction]] of the smallest [[supermultiplets]] of $d = 4, N = \mathbf{4}$ supersymmetry down to 1d yield adinkraic representations ([GGMPPRW 2009, section 3](#GGMPPRW09), [Gates, Hubsch & Stiffler 2014](#GatesHubschStiffler14)).

Corresponding adinkras for the chiral scalar supermultiplet (CM), the vector multiplet (VM) and the tensor multiplet (TM) look as follows:

<img src="https://ncatlab.org/nlab/files/AdinkrasFrom4d.png" width="450">


## References

For an introduction to adinkras, see the talk

* [[Lutian Zhao]], _What is an Adinkra?_ (2014) &lbrack;[slides pdf](http://math.sjtu.edu.cn/conference/Bannai/2014/data/20141213B/slides.pdf)&rbrack;

The concept of adinkras was introduced into [[supersymmetry]] [[representation theory]] in:

* {#FauxGates04} [[Michael Faux]], [[Jim Gates]], _Adinkras: A Graphical Technology for Supersymmetric Representation Theory_, Phys. Rev. D **71** (2005) 065002 &lbrack;[hep-th/0408004](https://arxiv.org/abs/hep-th/0408004), [doi:10.1103/PhysRevD.71.065002](https://doi.org/10.1103/PhysRevD.71.065002)&rbrack;

and further developed in the article

* [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], _On Graph-Theoretic Identifications of Adinkras, Supersymmetry Representations and Superfields_, Int. J. Mod. Phys. A **22** , (2007) 869-930 &lbrack;[arXiv:math-ph/0512016](https://arxiv.org/abs/math-ph/0512016), [doi:10.1142/S0217751X07035112](https://doi.org/10.1142/S0217751X07035112)&rbrack;

and many more ("DFGHIL collaboration"). For instance the relation to Clifford supermodules is discussed in

* [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], _Off-shell supersymmetry and filtered Clifford supermodules_, Algebr Represent Theor **21** (2018) 375–397 &lbracl[arXiv:math-ph/0603012](https://arxiv.org/abs/math-ph/0603012), [doi:10.1007/s10468-017-9718-8](https://doi.org/10.1007/s10468-017-9718-8)&rbrack;

kinetic terms are discussed in 

* [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], _Adinkras and the Dynamics of Superspace Prepotentials_ &lbrack;[arXiv:hep-th/0605269](https://arxiv.org/abs/hep-th/0605269), [InSpire:717895](https://inspirehep.net/literature/717895)&rbrack;

The classification of adinkras in terms of [[graphs]] and [[linear codes]] is due to

* {#DoranFauxGatesHubschIgaLandweberMiller11} [[Charles Doran]], [[Michael Faux]], [[Jim Gates]], [[Tristan Hübsch]], [[Kevin Iga]], [[Greg Landweber]], R. L. Miller, _Codes and Supersymmetry in One Dimension_, Adv. Theor. Math. Phys. **15** (2011) 1909-1970 &lbrack;[arXiv:1108.4124](https://arxiv.org/abs/1108.4124), [doi;10.4310/ATMP.2011.v15.n6.a7](https://doi.org/10.4310/ATMP.2011.v15.n6.a7)&rbrack;

and discussed in mathematical detail in

* {#Zhang11} [[Yan X Zhang]], _Adinkras for Mathematicians_ ([arXiv:1111.6055](https://arxiv.org/abs/1111.6055))

* {#Zhang13} [[Yan X Zhang]]: *The combinatorics of Adinkras*, PhD thesis, MIT (2013) &lbrack;[[Zhang-Adinkras.pdf:file]]&rbrack;


The [[dimensional reduction]] of the standard [[supermultiplets]] of $D = 4, \mathcal{N} = 1$ supersymmetry to adinkraic representations of $D = 1, \mathcal{N}=4$ is due to

* {#GGMPPRW09} [[Jim Gates]], J. Gonzales, B. MacGregor, J. Parker, R. Polo-Sherk, V. G. J. Rodgers, L. Wassink, _$4D$, $\mathcal{N} = 1$ Supersymmetry Genomics (I)_, JHEP 0912:008 (2009) &lbrack;[arXiv:0902.3830](https://arxiv.org/abs/0902.3830), [doi:10.1088/1126-6708/2009/12/008](https://doi.org/10.1088/1126-6708/2009/12/008)&rbrack;

* {#GatesHubschStiffler14} [[Jim Gates]], [[Tristan Hübsch]], Kory Stiffler, _Adinkras and SUSY Holography_, Int. J. Mod. Phys. A **29** 7 (2014) 1450041 &lbrack;[arXiv:1208.5999](https://arxiv.org/abs/1208.5999), [doi;10.1142/S0217751X14500419](https://doi.org/10.1142/S0217751X14500419)&rbrack;

See also

* {#IgaZhang15} [[Kevin Iga]], [[Yan Zhang]], _Structural Theory of 2-d Adinkras_ ([arXiv:1508.00491](https://arxiv.org/abs/1508.00491))

Discussion for $D=11$, $\mathcal{N}=1$:

* [[Jim Gates]], Yangrui Hu, S.-N. Hazel Mak, _Adinkra Foundation of Component Decomposition and the Scan for Superconformal Multiplets in 11D, $\mathcal{N} = 1$ Superspace_ &lbrack;[arXiv:2002.08502](https://arxiv.org/abs/2002.08502), <a href="https://doi.org/10.1007/JHEP09(2020)089">doi:10.1007/JHEP09(2020)089</a>&rbrack;


The relation of adinkras to special [[super Riemann surfaces]] via [[dessins d'enfants]]:

* {#DoranIgaLandweberMendez-Diez13} [[Charles Doran]], [[Kevin Iga]], [[Greg Landweber]], [[Stefan Méndez-Diez]], _Geometrization of $\mathcal{N}$-Extended 1-Dimensional Supersymmetry Algebras_, Adv. Theor. Math. Phys. **19** 5 (2015) 1043-1113 &lbrack;[arXiv:1311.3736](https://arxiv.org/abs/1311.3736), [doi:10.4310/ATMP.2015.v19.n5.a4](https://dx.doi.org/10.4310/ATMP.2015.v19.n5.a4), [pdf](https://www.charlesdoran.net/uploads/6/7/5/1/6751141/22_geometrization_of_n_extended_1_dimensional_supersymmetry_algebras_i_2015.pdf)&rbrack;

* {#DoranIgaKostiukMendes-Diez16} [[Charles Doran]], [[Kevin Iga]], Jordan Kostiuk, [[Stefan Méndez-Diez]], *Geometrization of $\mathcal{N}$-Extended 1-Dimensional Supersymmetry Algebras II*, Adv. Theor. Math> Physics **22** 3 (2018) &lbrack;[arXiv:1610.09983](https://arxiv.org/abs/1610.09983)&rbrack;

Further developments:

* {#CalkinsGatesGatesStiffler15} Mathew Calkins, D. E. A. Gates, [[Jim Gates]] Jr., Kory Stiffler, _Adinkras, 0-branes, Holoraumy and the SUSY QFT/QM Correspondence_,  International Journal of Modern Physics A **30** 11 (2015) 1550050 &lbrack;[arXiv:1501.00101](https://arxiv.org/abs/1501.00101), [doi:10.1142/S0217751X15500505](https://doi.org/10.1142/S0217751X15500505)&rbrack;

* [[S. James Gates Jr.]], Isaiah B. Hilsenrath, Saul Hilsenrath: *Modern Tensor-Spinor Symbolic Algebra Algorithms and Computing Non-Closure Geometry & Holoraumy in $11D$, $\mathcal{N} = 1$ Supergravity* &lbrack;[arXiv:2212.00614](https://arxiv.org/abs/2212.00614)&rbrack;

* [[S. James Gates Jr.]], Yangrui Hu: *Adynkra Genomes, Adynkrafields, and the 4D, $\mathcal{N} = 1$ Supergravity Superfield Prepotential* &lbrack;[arXiv:2407.09334](https://arxiv.org/abs/2407.09334)&rbrack;



Discussion in the context of [[spectral triples]] is in

* [[Matilde Marcolli]], Nick Zolman, _Adinkras, Dessins, Origami, and Supersymmetry Spectral Triples_ ([arXiv:1606.04463](https://arxiv.org/abs/1606.04463))

See also


* Wes Caldwell, Alejandro Diaz, Isaac Friend, [[Jim Gates]], Jr., Siddhartha Harmalkar, Tamar Lambert-Brown, Daniel Lay, Karina Martirosova, Victor Meszaros, Mayowa Omokanwaye, Shaina Rudman, Daniel Shin, Anthony Vershov, _On the Four Dimensional Holoraumy of the $4D$, $\mathcal{N} = 1$ Complex Linear Supermultiplet_ ([arXiv:1702.05453](https://arxiv.org/abs/1702.05453))

* [[Kevin Iga]], *Adinkras: Graphs of Clifford Algebra Representations, Supersymmetry, and Codes* ([arXiv:2110.01665](https://arxiv.org/abs/2110.01665))


* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Adinkra_symbols_(physics)">Adinkra symbols (physics)</a>_

In relation to [[pure spinors]]:

* Richard Eager, [[Simone Noja]], Raphael Senghaas, [[Johannes Walcher]], *Adinkras and Pure Spinors* &lbrack;[arXiv:2404.07167](https://arxiv.org/abs/2404.07167)&rbrack;

Relation to [[cellular automata]]:

* [[S. James Gates Jr.]], Youngik (Tom) Lee: *A Précis: Minimal Four Color Holoraumy and Wolfram's "New Kind of Science" Paradigm* &lbrack;[arXiv:2408.09342](https://arxiv.org/abs/2408.09342)&rbrack;





[[!redirects adinkras]]

[[!redirects adinkraic representation]]
[[!redirects adinkraic representations]]


