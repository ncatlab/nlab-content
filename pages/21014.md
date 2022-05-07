
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

A _Sullivan chord diagram_ ([Cohen-Godin 03, Def. 1](#CohenGodin03), following [Chas-Sullivan 02](#ChasSullivan02)) is a finite undirected [[graph]] given by attaching the external [[vertices]] of [[trees]], equipped with [[cyclic ordering]] around their [[vertices]], to a number of embedded [[orientation|oriented]] [[circles]], e.g.

<center>
<img src="https://ncatlab.org/nlab/files/SullivanChordDiagram.jpg" width="400">
</center>

such that the embedded circles are [[boundary]] [[connected component|components]] of the induced [[ribbon graph]] [[surface]]:

<center>
<img src="https://ncatlab.org/nlab/files/SurfaceInducedBySullivanChordDiagram.jpg" width="450">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


This way Sullivan chord diagrams $D$ induce 2-dimensional [[cobordisms]], namely  [[cospans]] of [[topological spaces]], 

$$
  \array{
    && \Sigma_D
    \\
    & \nearrow && \nwarrow
    \\
    \mathllap{ \big( \underset{q}{\sqcup}  S^1  \big) \simeq \; }
    \partial_{in}\Sigma_D
    && &&
    \partial_{out} \Sigma_D
    \mathrlap{ \; \simeq \big( \underset{p}{\sqcup} S^1 \big) }
  }
$$

with the induced [[ribbon graph]] [[surface]] $\Sigma_D$ at the tip, the $p$ [[boundary]] [[connected component|components]] corresponding to the embedded circles (shown above in grey) as one leg, and the remaining $q$ boundary components (shown in blue) as the other.

Applying to this [[cospan]] the [[space of maps]]-[[functor]] $Maps(-,X)$ into any [[topological space]] $X$, yields a [[span]]/[[correspondence]]


$$
  \array{
    && Maps(\Sigma_D, X)
    \\
    & \swarrow && \searrow
    \\
    \big(\mathcal{L}X\big)^q
    && &&
    \big(\mathcal{L}X\big)^p
  }
$$

between [[product topological spaces|products]] of the [[free loop space]] of $X$ with itself. The induced [[integral transform]] operations on the [[ordinary homology]] of the [[free loop spaces]] are generalized [[string topology]]-operation ([Cohen-Godin 03, Section 2](#CohenGodin03)).

(It is for this [[integral transform]] construction that the [[complement]] of the embedded circles is required to be a [[tree]], for this allows to [[contractible topological space|contract]] the [[spaces of maps]] out of these components, up to [[homotopy]].) 

Sullivan chord diagrams also naturally [[action|act]] on [[Hochschild homology]]/[[cyclic homology]] ([Tradler-Zeinalian 04](#TradlerZeinalian04), [Tradler-Zeinalian 06](#TradlerZeinalian06)).

## Properties

### Relation to round chord diagrams

Every [[round chord diagram]] is also a Sullivan chord diagram.

### Relation to Jacobi diagrams

Sullivan chord diagrams are much like [[Jacobi diagrams]], but more general in that they may have more than one (disjointly) embedded circle and in that they are not required to be trivalent, and less general in that the complement of the embedded circles is required to be a disjoint union of [[trees]]. The last condition need not be satisfied by [[Jacobi diagrams]], and hence not every Jacobi diagram is a Sullivan diagram.

For example, the following [[Jacobi diagram]] is *NOT* a Sullivan chord diagram:

<center>
<img src="https://ncatlab.org/nlab/files/OneLoopJacobiDiagram.jpg" width="200">
</center>


### Relation to horizontal chord diagrams
 {#RelationToHorizontalChordDiagrams}

One obtains Sullivan chord diagrams with $p$ disjoint embedded circles from [[horizontal chord diagrams]] by closing up strands after acting with a [[permutation]] with $p$ cycles ($p$ [[orbits]])

<center>
<img src="https://ncatlab.org/nlab/files/ClosingHorizontalChordsToSullivanChordsIII.jpg" width="800">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

## Related concepts

[[!include chord diagrams and weight systems -- table]]

## Applications

[[!include chord diagrams as multi-trace observables in BMN matrix model -- example]]


## References


In [[string topology]]:

The definition is due to

* {#CohenGodin03} [[Ralph Cohen]], [[Veronique Godin]], _[[A Polarized View of String Topology]]_, In: [[Graeme Segal]], [[Ulrike Tillmann]] (eds.) _Topology, Geometry and Quantum Field Theory_, LMS, Lecture Notes Series 308, 2004 ([arXiv:math/0303003](https://arxiv.org/abs/math/0303003), [doi:10.1017/CBO9780511526398.008](https://doi.org/10.1017/CBO9780511526398.008))

following

* {#ChasSullivan02} [[Moira Chas]], [[Dennis Sullivan]], _Closed string operators in topology leading to Lie bialgebras and higher string algebra_,  In: O.A. Laudal , R. Piene (eds.) _The Legacy of Niels Henrik Abel_, Springer 2004 ([arXiv:math/0212358](https://arxiv.org/abs/math/0212358), [doi:10.1007/978-3-642-18908-1_27](https://doi.org/10.1007/978-3-642-18908-1_27))

Also:

* [[Ralph Kaufmann]], Def. 1.4 of: _Moduli space actions on the Hochschild Co-Chains of a Frobenius algebra I: Cell Operads_ ([arXiv:math/0606064](https://arxiv.org/abs/math/0606064))


Review:

* [[Ralph Cohen]], [[Alexander Voronov]], around Def. 3.2.2 in: _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))

* [[Ralph Kaufmann]], Section 4.6 of: _Graphs, Strings, and Actions_, In: Tschinkel Y., Zarhin Y. (eds.) _Algebra, Arithmetic, and Geometry_, Progress in Mathematics, vol 270. Birkhäuser 2009 ([doi:10.1007/978-0-8176-4747-6_5](https://doi.org/10.1007/978-0-8176-4747-6_5))





Action on [[Hochschild homology]]:

* {#TradlerZeinalian04} [[Thomas Tradler]], [[Mahmoud Zeinalian]], _On the Cyclic Deligne Conjecture_, Journal of Pure and Applied Algebra, Volume 204, Issue 2, 1 February 2006, Pages 280-299 ([arXiv:math/0404218](https://arxiv.org/abs/math/0404218), [doi:10.1016/j.jpaa.2005.04.009](https://doi.org/10.1016/j.jpaa.2005.04.009))

* {#TradlerZeinalian06} [[Thomas Tradler]], [[Mahmoud Zeinalian]], _Algebraic String Operations_, K-Theory v. 38, n. 1 (November, 2007): 59-82 ([arXiv:math/0605770](https://arxiv.org/abs/math/0605770), [doi:10.1007/s10977-007-9005-2](http://dx.doi.org/10.1007/s10977-007-9005-2))

[[!redirects Sullivan chord diagrams]]




