

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

> For more see at *[[Yang-Baxter equation]]*.


#Contents#
* table of contents
{:toc}

## Idea

Given a [[monoidal category]] $C$ with [[tensor product]] $\otimes$, and an [[object]] $V$ in $C$, a *quantum Yang-Baxter operator* is a [[morphism]] of the form 

$$
  R \,\colon\, V\otimes V\to V\otimes V
$$ 

which satisfies the following *quantum Yang-Baxter equation* in $V\otimes V\otimes V$

$$
  R_{12}  
  \,
  R_{13}  
  \,
  R_{23} 
  \;=\; 
  R_{23} 
  \,
  R_{13} 
  \,
  R_{12}
  \,,
$$

where the subscripts indicate which tensor factors are being utilized, for instance $R_{12} = R\otimes id_V\in V\otimes V\otimes V$.

This equation is in particular satisfied by the component $\mathcal{R}_{V V}$ at $V$ of any [[braided monoidal category|braiding]] $\mathcal{R}$ on $C$.

Typical categories where the equation is considered are 

1. the [[category of vector spaces]] when the solutions are called *$R$-matrices* (or *quantum Yang-Baxter matrices*), 

1. [[categories of representations]] of [[quantum groups]]; often (a completion of) a quantum group $G$ itself has a particular element $\mathcal{R}$, called a *universal $\mathcal{R}$-element*, satisfying axioms ([[quasitriangular bialgebra|quasitriangularity]]) ensuring that its image in every representation satisfies qYBE

1. the [[category of sets]] where one speaks about [[set theoretic Yang-Baxter equation|set theoretic solutions of Yang-Baxter equation]].


\begin{remark}\label{HistoricalMotivation}
**(Historical motivation)**
\linebreak

The _quantum Yang-Baxter equation_ has been proposed by Baxter in the context of a particular model of [[statistical mechanics]] (the 8-vertex model) and called *star-triangle relation* &lbrack;[Baxter (1978)](#Baxter78), [Baxter (1982)](#Baxter82)&rbrack;. 

Later it has been generalized and axiomatized to a number of contexts: it is most notably satisfied by the universal R-element in a [[quasitriangular Hopf algebra]]. In some context it is equivalent to a braid relation for certain transposed matrix. Some solutions to quantum Yang-Baxter equation have good limits in classical mechanics which are [[classical r-matrices]], and the latter satisfy the [[classical Yang-Baxter equation]]. 
\end{remark}

## Equation with spectral parameter

With multiplicative spectral parameter, the equation reads

$$
  R_{12} (u) 
  \,
  R_{13} (u v) 
  \,
  R_{23} (v) 
  \;=\; 
  R_{23}(v) 
  \,
  R_{13}(u v) 
  \,
  R_{12}(u)
$$

where the subscripts indicate which tensor factors are being utilized.


## Related concepts

[[!include Yang-Baxter equations -- contents]]



## References

The ([[quantum Yang-Baxter equation|quantum]]) *Yang-Baxter equation* was named (cf. [Perk & Au-Yang 2006](#PerkAu-Yang06)) by [[Ludwig Fadeev]] in the late 1970s, in honor of:

* [[Chen Ning Yang]]: *Some Exact Results for the Many-Body Problem in one Dimension with Repulsive Delta-Function Interaction*, Phys. Rev. Lett. **19** (1967) 1312 &lbrack;[doi:10.1103/PhysRevLett.19.1312](https://doi.org/10.1103/PhysRevLett.19.1312)&rbrack;

* [[Chen Ning Yang]]: *S Matrix for the One-Dimensional $N$-Body Problem with Repulsive or Attractive $\delta$-Function Interaction*, Phys. Rev. **168** (1968) 1920 &lbrack;[doi:10.1103/PhysRev.168.1920](https://doi.org/10.1103/PhysRev.168.1920)&rbrack;

and

* {#Baxter78} [[Rodney J. Baxter]], *Solvable eight-vertex model on an arbitrary planar lattice*, Philos. Trans. Royal Society A **289** 1359 (1978) &lbrack;[doi:10.1098/rsta.1978.0062](https://doi.org/10.1098/rsta.1978.0062)&rbrack;

* {#Baxter82} [[Rodney J. Baxter]], *Exactly Solved Models in Statistical Mechanics*, Academic Press (1982) &lbrack;[webpage](https://physics.anu.edu.au/research/ftp/mpg/baxter_book.php), [pdf](https://physics.anu.edu.au/research/ftp/_files/Exactly.pdf)&rbrack;

Introduction and review:

* [[Michio Jimbo]], *Introduction to the Yang-Baxter Equation*, Int. J. Modern Physics A **4** 15 (1989) 3759-3777 &lbrack;[doi:10.1142/S0217751X89001503](https://doi.org/10.1142/S0217751X89001503)&rbrack; 

  reprinted in: *Braid Group, Knot Theory and Statistical Mechanics*, Advanced Series in Mathematical Physics **9**, World Scientific (1991) &lbrack;[doi:10.1142/0796](https://doi.org/10.1142/0796)&rbrack;

* {#PerkAu-Yang06} Jacques H. H. Perk, Helen Au-Yang: *Yang-Baxter Equations*, Encyclopedia of Mathematical Physics **5** (2006) 465-473 &lbrack;[arXiv:math-ph/0606053](https://arxiv.org/abs/math-ph/0606053)&rbrack;


See also:

* Wikipedia, *[Yang-Baxter equation](https://en.wikipedia.org/wiki/Yang%E2%80%93Baxter_equation)*

* [[eom]], *[Yang-Baxter equation](https://encyclopediaofmath.org/index.php?title=Yang-Baxter_equation)*

Further discussion in the context of [[quantum groups]]:

* A. U. Klymik, K. Schmuedgen, _Quantum groups and their representations_, Springer 1997.

* V. Chari, A. Pressley, _A guide to quantum groups_, Cambridge Univ. Press 1994

* [[V. G. Drinfel'd]], _Quantum groups_, Proceedings of the International Congress of Mathematicians 1986, Vol. 1, 798&#8211;820, AMS 1987, [djvu:1.3M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.djvu), [pdf:2.5M](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1986.1/ICM1986.1.ocr.pdf)

* D. Gurevich, [[V. Rubtsov]], _Yang-Baxter equation and deformation of associative and Lie algebras_, in: Quantum Groups, Springer Lecture Notes in Math. __1510__ (1992) 47-55,[doi](https://doi.org/10.1007/BFb0101177)

* P. P. Kulish, [[Nicolai Reshetikhin]], E. K. Sklyanin, _Yang-Baxter equation and representation theory: I_, Lett. Math. Phys. __5__:5 (1981), 393-403, [doi](http://dx.doi.org/10.1007/BF02285311)

Discussion in the context of [[braid group representations]]:

* [[Camilo Arias Abad]], §5.1 *Introduction to representations of braid groups*, Rev. colomb. mat. vol.49 no.1 (2015) &lbrack;[arXiv:1404.0724](https://arxiv.org/abs/1404.0724), [doi:10.15446/recolma.v49n1.54160](https://doi.org/10.15446/recolma.v49n1.54160)&rbrack;




[[!redirects quantum R-matrix]]

[[!redirects quantum Yang-Baxter matrix]]


[[!redirects quantum Yang-Baxter equation]]

