
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Borel-Weil-Bott theorem_ characterizes [[representations]] of suitable [[Lie groups]] $G$ as space of holomorphic [[sections]] of [[complex line bundles]] over [[flag varieties]] $G/B$, for $B$ a [[Borel subgroup]].
With suitable qualifiers added this is Kirillov's _[[orbit method]]_, and the construction may be interpreted as sending a [[symplectic manifold]] equipped with $G$-[[Hamiltonian action]] to its [[geometric quantization]]. As discussed there, this is equivalently given by [[fiber integration]] in [[K-theory]] and accordingly the Borel-Weil-Bott theorem is naturally regarded in the context of [[generalized Schubert calculus]] (e.g. [Kumar 12](Kumar12)).



A common method of construction of [[representations]] of [[groups]] in [[representation theory]] is to consider the invariant subspaces of the [[induced representation]] (set-theoretic or $L^2$-version). The induced representation is too big and [[Frobenius reciprocity]] indicates that they are normally not [[irreducible representation|irreducible]]. Given a [[subgroup]] $B\subset G$ and a $B$-module $V$, with $\rho\colon B\to Aut(V)$ the induced module can be represented as a space of (set-theoretic or $L^2$&#8209;) [[sections]] of the [[associated bundle]] $G\times_{G/B} V$ to the [[principal fiber bundle]] $G\to G/B$, at least when these words make sense. In [[geometric quantization]], the method to single out a sufficiently small space of sections is to look at sections which are horizontal in the sense of some [[polarization]], or equivalently horizontal for an appropriate choice of [[connection]] on the bundle. 

The first instance is the theorem of Borel--Weil, (J-P. Serre, Bourbaki Seminar 100, 1953/54) which asserts that if $B$ is the [[Borel subgroup]] of the complex semisimple group $G^{\mathbb{C}}$ (which can be considered as the [[complexification]] of a [[compact Lie group]] $G$ with the [[maximal torus]] $T=G\cap B\subset G$), then all unitary irreducible representations can be obtained as the spaces of (anti)-holomorphic line bundles associated to the principal fibration $G\to G/B$ over the generalized [[flag variety]] $G^{\mathbb{C}}/B\cong G/T$ with the fiber $\mathbb{C}_\chi$, which is the $1$-dimensional representation corresponding to a dominant integral [[character]] $\chi$; and viceversa, all such spaces of sections are irreducible. The inner product is inherited from the hermitean structure on the line bundle. 

There is an extension to higher cohomologies instead of spaces of sections, called the **Borel--Weil--Bott theorem** and numerous extensions, e.g. to Harish--Chandra sheaves to construct the infinite-dimensional representations. The original proof is by geometric and analytic methods; some of the modern extensions of the method use the algebraic [[D-module]] theory and are based on the [[Beilinson-Bernstein localization]] theorem. There are even extensions to [[quantum groups]]. 

## Related concepts

* [[orbit method]]

* [[Schubert calculus]]


## References

* Neil Chriss, [[Victor Ginzburg]], _Representation theory and complex geometry_, Birkh&#228;user 1994

* [[Jean-Pierre Serre]], _Repr&#233;sentations lin&#233;aires et espaces homog&#232;nes k&#228;hl&#233;riens des groupes de Lie compacts (d'apr&#232;s Armand Borel et Andr&#233; Weil)", S&#233;minaire Bourbaki 100: 447&#8211;454, Paris: Soc. Math. France, 1953/54,  [numdam](http://www.numdam.org/item?id=SB_1951-1954__2__447_0)

* [[Bertram Kostant]], _Lie algebra cohomology and the generalized 
Borel-Weil theorem_, 

* [[Pierre Cartier]], _Remarks on "Lie algebra cohomology and the generalized Borel-Weil theorem" by B. Kostant_, Ann. of Math. _74_, 2,  1961 [pdf](http://www.math.tamu.edu/~jml/cartier61.pdf)

* [[Jacob Lurie]], _A proof of the Borel-Weil-Bott theorem_ ([pdf](http://www.math.harvard.edu/~lurie/papers/bwb.pdf))


Lecture notes include

* Wilfried Schmid (notes by Matvei Libine), _Geometric methods in representation theory_ ([pdf](http://www.math.harvard.edu/~schmid/articles/brussels_1_30_04.pdf))

* Shrawan Kumar, _Borel-Weil-Bott theorem and geometry of Schubert varieties_ ([pdf](http://www.unc.edu/math/Faculty/kumar/notes/kumar_notes_03.pdf))
 {#Kumar12}


* P. Woit, _Topics in representation theory: the Borel-Weil theorem_, ([pdf](http://www.math.columbia.edu/~woit/notes16.pdf)), _Quantum field theory and representation theory: A sketch_ ([pdf](http://www.math.columbia.edu/~woit/sketch.pdf))

* Lisa Jeffrey, _Remarks on geometric quantization and representation theory_ [pdf](http://www.math.toronto.edu/~jeffrey/mat1312/lec14.gq.pdf)

See also

* eom: [Bott-Borel-Weil theorem](http://eom.springer.de/b/b120400.htm)

* wikipedia: [Borel&#8211;Weil&#8211;Bott theorem](http://en.wikipedia.org/wiki/Borel&#8211;Weil&#8211;Bott_theorem), [Borel&#8211;Weil theorem](http://en.wikipedia.org/wiki/Borel&#8211;Weil_theorem)


[[!redirects Borel–Weil theorem]]
[[!redirects Borel--Weil theorem]]


[[!redirects Borel-Weil-Bott theorem]]