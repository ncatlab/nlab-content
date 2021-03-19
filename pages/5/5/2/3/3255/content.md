
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

# Contents #
* table of contents 
{: toc}

## Idea

The **cellular approximation theorem** states that every [[continuous map]] between [[CW complexes]] (with chosen CW presentations) is [[homotopy|homotopic]] to a [[cellular map]], hence a map that respects the [[cell complex]]-structure, mapping [[n-skeleta]] to $n$-skeleta for all $n$.

This is the analogue for [[CW-complexes]] of the [[simplicial approximation theorem]] (sometimes also called lemma): that every continuous map between the [[geometric realizations]] of [[simplicial complexes]] is [[homotopy|homotopic]] to a map induced by a map of [[simplicial complexes]] (after subdivision). 

## Statement 

+-- {: .num_theorem #CellularApproximationTheorem} 
###### Theorem 

Given a [[continuous map]] $f \colon (X, A) \to (X', A')$ between [[relative CW-complexes]] that is cellular on a subcomplex $(Y, B)$ of $(X, A)$, there is a cellular map $g \colon (X, A) \to (X', A')$ that is [[homotopy|homotopic]] to $f$ relative to $Y$. 

=-- 


It follows that if two cellular maps between CW-complexes are homotopic, then they are so by a cellular homotopy.

([Spanier 66, p. 404](#Spanier66), review in [May 99, Section 10.4](#May99), [Hatcher 02, Thm. 4.8](#Hatcher02))

## Applications

### Finite-dimensional universal bundles
 {#FiniteDimensionalUniversalBundles}

For $G$ a suitable [[topological group]], consider the [[universal principal bundle]] $E G \to B G$ over the [[classifying space]] equipped with some [[CW-complex]]-structure (as typically comes with its construction as a [[sequential colimit]] of [[Grassmannians]]).


Then the cellular approximation theorem (Thm. \ref{CellularApproximationTheorem}) implies at once that the [[pullback bundle|pullback]] $E_d G$ of the [[universal principal bundle]] $E G$ from $B G$ to its $d+1$-[[cellular skeleton|skeleton]]

\begin{xymatrix@=28pt}
  E_{d} G
  \ar[r]
  \ar[d]
  \ar@{}[dr]|-{\mbox{\tiny\rm(pb)}}
  & E G
  \ar[d]
  \\
  \mathrm{sk}_{d+1} B G
  \;
  \ar@{^{(}->}[r]
  & 
  B G
\end{xymatrix}

is universal for $G$-[[principal bundles]] over $d$-dimensional [[cell complexes]] $X^d$ (in particular: over $d$-dimensional [[smooth manifolds]], via any of their [[smooth triangulations]]) -- in that forming [[pullback bundles|pullback]] of $E_d G$ identifies [[homotopy classes]] of maps  $X^d \to sk_{d+1} B G$ with [[isomorphism classes]] of $G$-principal bundles over $X^d$.

Beware here the required skeletal degree: On the one hand, the cellular approximation theorem gives that every isomorphism class of a $G$-principal bundle on $X^d$ is hit already by pullback from just the $d$-skeleton $sk_d B G$. But in order for the isomorphism relation of bundles to be reflected in the homotopy relation of their classifying maps one needs the $(d+1)$-skeleton: Because the [[cylinder]] $X^d \times [0,1]$ on which [[left homotopy]] of maps is defined, is $d+1$-skeletal of $X^d$ is $d$-skeletal.

Such finite-dimensional $G$-principal bundles, universal for base spaces of fixed bounded dimension, have the advantage that they carry an ordinary [[smooth manifold]]-[[mathematical structure|structure]] (instead of just a [[generalized smooth space]]-structure) and as such an ordinary [[principal connection]], which is a [[universal connection]] for bundles over fixed bounded-dimensional base spaces. In this way these finite-dimensional universal bundles serve as a foundation for [[Chern-Weil theory]] ([Chern 51 -- p. 45 and 67](Chern-Weil+theory#Chern51), [Narasimhan-Ramanan 61](Chern-Weil+theory#NarasimhanRamanan61), [Narasimhan-Ramanan 63](Chern-Weil+theory#NarasimhanRamanan63), [Sclafly 80](Chern-Weil+theory#Schlafly80)).

## Related concepts

* [[CW-approximation theorem]]

* [[Whitehead's theorem]]

## References

### General

* {#Spanier66} [[Edwin Spanier]], ch. 7. sec. 6, cor. 18 (p. 404)  of: _Algebraic topology_, Springer 1966 ([doi:10.1007/978-1-4684-9322-1](https://link.springer.com/book/10.1007/978-1-4684-9322-1))

* {#May99} [[Peter May]],  sec. 10.4 in: _[[A Concise Course in Algebraic Topology]]_, University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* {#Hatcher02} [[Allen Hatcher]], Theorem 4.8, [p. 349](http://pi.math.cornell.edu/~hatcher/AT/AT.pdf#page=358) in: _Algebraic topology_, Cambridge Univ. Press 2002 ([web](http://pi.math.cornell.edu/~hatcher/AT/ATpage.html))


See also

* Wikipedia, _[Cellular approximation](http://en.wikipedia.org/wiki/Cellular_approximation)_

### In equivariant homotopy theory
 {#ReferencesInEquivariantHomotopyTheory}

Cellular approximation for [[G-CW complexes]] in [[equivariant homotopy theory]] is due to:

* {#Matumoto71} [[Takao Matumoto]], Theorem 4.4 in: _On $G$-CW complexes and a theorem of JHC Whitehead_, J. Fac. Sci. Univ. Tokyo Sect. IA 18, 363-374, 1971 ([[matumoto.pdf:file]])

Textbook account:

* {#tomDieck87} [[Tammo tom Dieck]], Theorem 2.1 in: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))

Review:

* [[Jay Shah]], Theorem 2.5 in: _Equivariant algebraic topology_, 2010 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2010/REUPapers/Shah.pdf), [[ShahEquivariantAlgebraicTopology.pdf:file]])

[[!redirects equivariant cellular approximation theorem]]