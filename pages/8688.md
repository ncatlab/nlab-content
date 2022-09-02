

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a monoidal category $C$ with monoidal product $\otimes$,
and an object $V$ in $C$, the quantum Yang-Baxter operator
is a morphism $R : V\otimes V\to V\otimes V$ which satisfies quantum Yang-Baxter equation in $V\otimes V\otimes V$
$$
R_{12}  R_{13}  R_{23} = R_{23} R_{13} R_{12}
$$

where the subscripts indicate which tensor factors are being utilized, for instance $R_{12} = R\otimes id_V\in V\otimes V\otimes V$.

This equation is in particular satisfied by the component $\mathcal{R}_{VV}$ at $V$ of any brading $\mathcal{R}$ on $C$.
Typical categories where the equation is considered are the category of vector spaces when the solutions are called $R$-matrices (or quantum Yang-Baxter matrices), categores of representations of quantum groups when a particular solution is called a universal $\mathcal{R}$-element and the category of sets when we talk about [[set theoretic Yang-Baxter equation|set theoretic solutions of Yang-Baxter equation]].

#### Historical motivation

The _quantum Yang-Baxter equation_ has been proposed by Baxter in the context of a particular model of [[statistical mechanics]] (6-vertex model ??) and called star-triangle relation. Later it has been generalized and axiomatized to a number of contexts: it is most notably satisfied by the universal R-element in a [[quasitriangular Hopf algebra]]. In some context it is equivalent to a braid relation for certain transposed matrix. Some solutions to quantum Yang-Baxter equation have good limits in classical mechanics which are [[classical r-matrices]], and the latter satisfy the classical Yang-Baxter equation. 

## Equation with spectral parameter

With multiplicative spectral parameter, the equation reads

$$
R_{12} (u) R_{13} (uv) R_{23} (v) = R_{23}(v) R_{13}(uv) R_{12}(u)
$$

where the subscripts indicate which tensor factors are being utilized.

## Related concepts

[[!include Yang-Baxter equations -- contents]]

## References

* A. U. Klymik, K. Schmuedgen, _Quantum groups and their representations_, Springer 1997.

* V. Chari, A. Pressley, _A guide to quantum groups_, Cambridge Univ. Press 1994

* [[V. G. Drinfel'd]], _Quantum groups_, Proceedings of the International Congress of Mathematicians 1986, Vol. 1, 798&#8211;820, AMS 1987, [djvu:1.3M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.djvu), [pdf:2.5M](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1986.1/ICM1986.1.ocr.pdf)

* D. Gurevich, V. Rubtsov, _Yang-Baxter equation and deformation of associative and Lie algebras_, in: Quantum Groups, Springer Lecture Notes in Math. __1510__ (1992) 47-55,[doi](http://dx.doi.org/10.1007/BFb0101177)

* P. P. Kulish, N. Yu. Reshetikhin, E. K. Sklyanin, _Yang-Baxter equation and representation theory: I_, Lett. Math. Phys. __5__:5 (1981), 393-403, [doi](http://dx.doi.org/10.1007/BF02285311)




[[!redirects quantum R-matrix]]
[[!redirects quantum Yang-Baxter equation]]