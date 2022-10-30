
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

### General

For $S \to X$ a [[spinor bundle]] over a [[Riemannian manifold]] $(X,g)$, a _Dirac operator_ on $S$ is an [[differential operator]] on ([[sections]] of) $S$ whose [[principal symbol]] is that of $c \circ d$, where $d$ is the [[exterior derivative]] and $c$ is the [[symbol map]].

More abstractly, for $D$ a Dirac operator, its normalization $D(1+ D^2)^{-1/2}$ is a [[Fredholm operator]], hence defines an element in [[K-homology]].


### Origin and role in Physics

The first relativistic Schr&#246;dinger type equation found was Klein-Gordon. At first it did not look that K-G equation could be interpreted physically because of negative energy states and other paradoxes. [[Paul Dirac]] proposed to take a square root of [[Laplace operator]] within the matrix-valued differential operators and obtained a Dirac equation; matrix valued generators involved representations of a Clifford algebra. It also had negative energy solutions, but with half-integer spin interpretation which was appropriate the Pauli exclusion principle together with the Dirac sea picture came at rescue (Klein-Gordon is now also useful with more modern formalisms). 

(...)

## Definition

### In components

The tangent bundle of an oriented Riemannian $n$-dimensional manifold $M$ is an $SO(n)$-bundle. Orientation means that the first [[Stiefel-Whitney class]] $w_1(M)$ is zero. If $w_2(M)$ is zero than the $SO(n)$ bundle can be lifted to a $Spin(n)$-bundle. A choice of connection on such a $Spin(n)$-bundle is a $Spin$-structure on $M$. There is a standard $n/2$-dimensional representation of $Spin(n)$-group, so called Spin representation, which is depending, if $n$ is odd irreducible, and if $n$ is even it decomposes into the sum of two irreducible representations of equal dimension $S_+$ and $S_-$. Thus we can associate associated bundles to the original $Spin(n)$ bundle $P$ with respect to these representations. Thus we get the **spinor bundles** $E_\pm := P\times_{Spin(n)} S_\pm\to M$
and $E = E_+\oplus E_-$.

Gamma matrices, which are the representations of the [[Clifford algebra]] 
$$
\gamma_a \gamma_b + \gamma_b \gamma_a = -2\delta_{ab} I
$$
$$
\gamma_5 = i^{n(n+1)/2}\gamma_1\cdots\gamma_n, \,\,\,\,\gamma^2_5 = I
$$

thus act on such a space; certain combinations of products of gamma matrices with partial derivatives define a first order Dirac operator $\Gamma(E)\to\Gamma(E_-)$; there are several versions, in mathematics is pretty important the chiral Dirac operator 
$$
\Gamma(M,E_+)\to \Gamma(M,E_-)
$$
given by local formula
$$
\sum_a \gamma^a e^\mu_a(x) \nabla_\mu \frac{1+\gamma_5}{2}
$$
where $e^\mu_a(x)$ are orthonormal frames of tangent vectors and $\nabla_\mu$ is the [[covariant derivative]] with respect to the Levi-Civita spin connection. The expression $\frac{1+\gamma_5}{2}$ is the chirality operator. 

In Euclidean space the Dirac operator is elliptic, but not in Minkowski space. 

The Dirac operator is involved in approaches to the [[Atiyah-Singer index theorem]] about the index of an elliptic operator: namely the index can be easier calculated for Dirac operator and the deformation to the Dirac operator does not change the index. An appropriate version of a Dirac operator is a part of a concept of the [[spectral triple]] in [[noncommutative geometry]] a la [[Alain Connes]]. 

## Examples

* [[Kähler-Dirac operator]]

* [[Dolbeault-Dirac operator]]

* [[Spin^c Dirac operator]]


## Related concepts

* [[index of a Dirac operator]]

* [[Fredholm module]], [[K-homology]], [[KK-theory]]

## References

Textbooks include

* H. Blaine Lawson Jr. , Marie-Louise Michelson, _Spin geometry_, Princeton Univ. Press 1989.

* [[Thomas Friedrich]], _Dirac operators in Riemannian geometry_, Graduate studies in mathematics 25, AMS (1997)
 {#Friedrich97}


See also

* C. Nash, _Differential topology and quantum field theory_, Acad. Press 1991. 


* [[Dan Freed]], _Geometry of Dirac operators_ ([pdf](http://www.ma.utexas.edu/users/dafr/DiracNotes.pdf))
 {#Freed}

* [[Michael Atiyah]], [[Raoul Bott]], V. K. Patodi, _On the heat equation and the index theorem_, Invent. Math. 19 (1973), 279&#8211;330.

* N. Berline, [[Ezra Getzler]], M. Vergne, _Heat kernels and Dirac operators_, Grundlehren __298__, Springer 1992, "Text Edition" 2003.

* [[Eckhard Meinrenken]], _Clifford algebras and Lie groups_, Lecture Notes, University of Toronto, Fall 2009.

* Jing-Song Huang, Pavle Pand&#382;i&#263;, J.-S. Huang, P. Pandzic, Dirac Operators in Representation Theory,. Birkh&#228;user, Boston, 2006, 199 pages; short version _Dirac operators in representation theory_, 48 pp. [pdf](http://www.ims.nus.edu.sg/Programs/liegroups/files/singnotes.pdf)

* J.-S. Huang, Pavle Pand&#382;i&#263;, _Dirac cohomology, unitary representations and a proof of a conjecture of Vogan_, J. Amer. Math. Soc. __15__ (2002), 185&#8212;202.

* R. Parthasarathy, _Dirac operator and the discrete series_, Ann. of Math. __96__ (1972), 1-30.


[[!redirects Dirac operators]]


