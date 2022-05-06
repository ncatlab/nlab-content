
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Adams conjecture_ is a statement about triviality of [[spherical fibrations]] associated to certain formal differences of [[vector bundles]] ([[K-theory]] classes) via the [[J-homomorphism]]. The conjecture was stated in ([Adams 63, conjecture 1.2](#Adams63)), for vector bundles of rank up to two over a [[finite CW-complex]], which was proven in ([Adams 63, theorem 1.4](#Adams63)).  A general proof was then given in ([Quillen 71](Quillen71)). 

The Adams conjecture/Adams-Quillen theorem serves a central role in the identification of the [[image of the J-homomorphism]]. 



## Statements

Let $X$ be (the [[homotopy type]] of) a [[topological space]]. For $V \;\colon\; X \longrightarrow B O$ classifying a real [[vector bundle]] on $X$, the corresponding [[spherical fibration]] is classified by the composite

$$
  J(V)
   \;\colon\;
  X \stackrel{V}{\longrightarrow} B O \stackrel{J}{\longrightarrow} B GL_1(\mathbb{S})
$$

with the delooped [[J-homomorphism]].
This descends to a map from [[topological K-theory]] to [[spherical fibrations]].

Now for $L$ a [[line bundle]] on some $X$ and for non-vanishing $k \in \mathbb{Z}$, [[John Adams]] observed that the [[spherical fibration]] associated with the difference $L^{\otimes k} - L \in K O(X)$ has the property that some $k$-fold multiple of it has trivial spherical fibration, hence that there is $N \in \mathbb{N}$ for which

$$
  J\left(
    \oplus^{k^N} (L^{\otimes k} - L)
  \right)
  = 0
  \,.
$$

Noticing that $L \mapsto L^{\otimes^k} = \Psi^k(L)$ is the $k$th [[Adams operation]] on [[K-theory]] applied to the [[line bundle]] $L$, [[John Adams]] then conjectured that the above is true for all [[vector bundles]] $V$ in the form

$$
  J\left(
    \oplus^{k^N} (\Psi^k(V) - V)
  \right)
  = 0
  \,.
$$


## Related entries

* [[J-homomorphism]]

* [[Schur index]]

## References

### General

The conjecture originates in

* {#Adams63} [[John Adams]], _On the groups $J(X)$ I: Topology_, 2 (1963) pp. 181&#8211;195 
 
Review:

* [[Akhil Mathew]], _The Adams conjecture I_ ([web](http://amathew.wordpress.com/2013/01/23/the-adams-conjecture-i/))

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lecture 30 in: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])


The [[proof]] of the Adams conjecture is originally due to

* {#Quillen71} [[Daniel Quillen]], _The Adams conjecture_, Topology, vol 10, 1971  ([pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/Quillen.pdf))
 
The proof using [[algebraic geometry]] is due to 

* [[Dennis Sullivan]], _Genetics of homotopy theory and the Adams conjecture_, The Annals of Mathematics, Second Series, Vol. 100, No. 1 (Jul., 1974), pp. 1-79 ([JSTOR](http://www.jstor.org/stable/1970841), [pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/Sullivan.pdf))

Yet another proof via [[Becker-Gottlieb transfer]] is due to 

* J. Becker, D. Gottlieb, _The transfer map and fiber bundles_ Topology , 14 (1975) {#BeckerGottlieb75}

### In equivariant cohomology
 {#ReferencesInEquivariantCohomology}

The generalization to [[equivariant cohomology]] ([[equivariant K-theory]]) is discussed in

* [[Tammo tom Dieck]], theorem 11.3.8 in _[[Transformation Groups and Representation Theory]]_ Lecture Notes in Mathematics 766 Springer 1979

* Z. Fiedorowicz, H. Hauschild, [[Peter May]], theorem 0.4 of _Equivariant algebraic K-theory_, _Equivariant algebraic K-theory_, Algebraic K-Theory. Springer, Berlin, Heidelberg, 1982. 23-80 ([pdf](http://math.uchicago.edu/~may/PAPERS/40.pdf))

* Henning Hauschild, [[Stefan Waner]], theorem 0.1 of _The equivariant Dold theorem mod $k$ and the Adams conjecture_, Illinois J. Math. Volume 27, Issue 1 (1983), 52-66. ([euclid:1256065410](https://projecteuclid.org/euclid.ijm/1256065410))

* Kuzuhisa Shimakawa, _Note on the equivariant $K$-theory spectrum_, Publ. RIMS, Kyoto Univ. **29** (1993), 449-453 ([pdf](http://www.ems-ph.org/journals/show_pdf.php?issn=0034-5318&vol=29&iss=3&rank=5), [doi](https://doi.org/10.2977/prims/1195167052))

* Christopher French, theorem 2.4 in _The equivariant $J$–homomorphism for finite groups at certain primes_, Algebr. Geom. Topol. Volume 9, Number 4 (2009), 1885-1949 ([euclid:1513797069](https://projecteuclid.org/euclid.agt/1513797069))

[[!redirects Adams conjectures]]

[[!redirects Adams' conjecture]]
[[!redirects Adams' conjectures]]

[[!redirects equivariant Adams conjecture]]
[[!redirects equivariant Adams conjectures]]
