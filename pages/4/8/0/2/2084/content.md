
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

A _quasi-triangular bialgebra_ / _triangular bialgebra_ is a [[bialgebra]] equipped with just the right structure such as to make its [[category of modules]] into a [[braided monoidal category]]/[[symmetric monoidal category]].

## Definition

Let $A$ be an algebra in a symmetric [[monoidal category]] $C$ with symmetry $\tau$; fix $m,l$ and $D\in A^{\otimes k}$ and let $1\leq i_r\leq l$ for $1\leq r\leq m$ be different. Then denote $D_{i_1,\ldots,i_m}\in A^{\otimes n}$ as the image of $R\otimes 1^{\otimes (l-m)}$ under the permutation which is the composition of the $m$ transpositions $(r,i_r)$ of tensor factors interchanging $r$ and $i_r$. In the following $C$ is the monoidal category of $k$-vector spaces. 

A $k$-[[bialgebra]] (in particular $k$-[[Hopf algebra]]) is __quasitriangular__ if there is an invertible element $R\in H\otimes H$ such that for any $h\in H$
$$
\tau\circ\Delta(h) = R\Delta(h)R^{-1}
$$
where $\tau=\tau_{H,H}:H\otimes H\to H\otimes H$ and

$$
(\Delta\otimes id)(R)=R_{13} R_{23}
$$

$$
(id\otimes\Delta)(R)=R_{13} R_{12}
$$

An invertible element $R$ satisfying these 3 properties is called the __universal $R$-element__. As a corollary 

$$
(\epsilon\otimes id) R = 1,\,\,\,\,\,(id\otimes\epsilon)R = id
$$

and the [[quantum Yang-Baxter equation]] holds in the form

$$
R_{12} R_{13} R_{23} = R_{23} R_{13} R_{12} 
$$


A quasitriangular $H$ is called __triangular__ if $R_{21}:=\tau(R) = R^{-1}$. 

The category of representations of a quasitrianguar bialgebra is a _braided_ monoidal category. If $R$ is a universal $R$-element, then $R_{21}^{-1}$ is as well. If $H$ is quasitriangular, $H^{cop}$ and $H_{op}$ are as well, with the universal $R$-element being $R_{21}$, or instead, $R_{12}^{-1}$. Any twisting of a quasitriangular bialgebra by a [[bialgebra cocycle|bialgebra 2-cocycle]] twists the universal $R$-element as well; hence the twisted bialgebra is again quasitriangular. Often the $R$-element does not exist as an element in $H\otimes H$ but rather in some completion of the tensor square; we say that $H$ is essentially quasitriangular, this is true for quantized enveloping algebras $U_q(G)$ in the rational form. The famous Sweedler's Hopf algebra has a 1-parameter family of universal $R$-matrices. 

## Properties

### Tannaka duality

A quasitriangular structure on a [[bialgebra]] corresponds to a [[braided monoidal category]] structure on the [[category of modules]] of the underlying algebra. (For instance chapter 1, section 2 of ([Carroll](#Carroll))).

[[!include structure on algebras and their module categories - table]]

## Related concepts

* [[quasitriangular Hopf algebra]]


## References

* V. G. Drinfel'd, _Quantum groups_, Proc. ICM 1986, Vol. 1, 2 798&#8211;820, AMS 1987.

* S. Majid, _Quasitriangular Hopf algebras and Yang-Baxter equations_, Int. j. mod. physics A, __5__, 01, pp. 1-91 (1990) [doi:10.1142/S0217751X90000027](http://dx.doi.org/10.1142/S0217751X90000027)

* S. Majid, _Foundations of quantum group theory_, Cambridge University Press 1995, 2000.

* A. U. Klymik, K. Schmuedgen, _Quantum groups and their representations_, Springer 1997.

* V. Chari, A. Pressley, _A guide to quantum groups_, Camb. Univ. Press 1994

* Robert Carroll, _Calculus revisited_ 
 {#Carroll}

[[!redirects quasitriangular bialgebras]]

[[!redirects triangular bialgebra]]
[[!redirects triangular bialgebras]]

[[!redirects universal R-element]]
