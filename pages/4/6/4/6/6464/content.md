
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _totalization_ of a [[cosimplicial object]] is the [[duality|dual]] concept to the [[geometric realization]] of a [[simplicial object]].

## Definition

### As an end

For $A : \Delta \to C$ a [[cosimplicial object]] in a [[category]] $C$ which is [[powering|powered]] over [[simplicial sets]] and for

$$
  \Delta : [n] \mapsto \Delta[n]
$$

the canonical cosimplicial simplicial set of [[simplices]], the **totalization** of $A$ is the [[end]]

\[
  \label{AsAnEnd}
  \int_{[k]\in \Delta}
  (A_k)^{\Delta[k]}
  \,\,\,
  \in 
  C
  \,.
\]

### As the homotopy limit
 {#AsTheHomotopyLimit}

For a [[cosimplicial object]] $A \colon \Delta \to \mathcal{C}$ in a suitable [[model category]] such that $A$ is a [[fibrant object]] with respect to the [[Reedy model structure]] on $Func(\Delta, \mathcal{C})$, totalization in terms of the [[end]]-construction above in (eq:AsAnEnd) is a model for the [[homotopy limit]] over $A$.

([Hirschhorn 15, theorem 9.2](#Hirschhorn15))

## Properties

### Homotopy and homology

The [[homotopy groups]] of the totalization of a [[cosimplicial space]] are computed by a [[Bousfield-Kan spectral sequence]]. 

The [[homology groups]] by an [[Eilenberg-Moore spectral sequence]].
  



## Related concepts

Formally the dual to totalization is [[geometric realization]]: where totalization is the [[end]] over a [[power]]ing with $\Delta$, realization is the [[coend]] over the [[tensoring]].

But various other operations carry names similar to "totalization". For instance a [[total chain complex]] is related under [[Dold-Kan correspondence]] to the [[diagonal of a bisimplicial set]] -- see at *[[Eilenberg-Zilber theorem]]*. As discussed at _[[bisimplicial set]]_, this is [[weak homotopy equivalence|weakly homotopy equivalent]] to the operation that is often called $Tot$ and called the _total simplicial set_ of a bisimplicial set.

To a cosimplicial chain complex we can assign a double complex by taking the alternating sum of the coface maps. Then the totalization of this cosimplicial object and the totalization of the double complex as defined in homological algebra coincide. Moreover, the associated [[Bousfield-Kan spectral sequence]] and [[spectral sequence of a double complex]] coincide.

## References

The concept [[cosimplicial spaces]] originates with

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], chapter X.3 of _[[Homotopy limits, completions and localizations]]_, Lecture Notes in Mathematics, Vol 304, Springer 1972

Quick review includes

* [[Daniel Dugger]], section 5.3 of _A primer on homotopy colimits_ ([pdf](https://pages.uoregon.edu/ddugger/hocolim.pdf))

The generalization to [[cosimplicial objects]] in more general [[model categories]] is discussed in

* {#Bousfield03} [[Aldridge Bousfield]], _Cosimplicial resolutions and homotopy spectral sequences in model categories_, Geom. Topol. 7 (2003) 1001-1053 ([arXiv:math/0312531](http://arxiv.org/abs/math/0312531))

Review of this includes

* {#Levine13} [[Marc Levine]], _The Adams-Novikov spectral sequence and Voevodsky's slice tower_, Geom. Topol. 19 (2015) 2691-2740 ([arXiv:1311.4179](http://arxiv.org/abs/1311.4179))

Some kind of notes are in

* Rosona Eldred, _Tot primer_ ([pdf](https://drive.google.com/file/d/0B6WoYElpsU2TTXdNbmNyXzZjamc/view))

Discussion of totalizations as [[homotopy limits]] includes

* {#Hirschhorn15} [[Philip Hirschhorn]], Section 9 of: _The diagonal of a multicosimplicial object_ ([arXiv:1506.06837](https://arxiv.org/abs/1506.06837))

* [[Akhil Mathew]], [[Vesna Stojanoska]], _Fibers of partial totalizations of a pointed cosimplicial space_, Proc. Amer. Math. Soc. 144 (2016), no. 1, 445--458 ([arXiv:1408.1665](https://arxiv.org/abs/1408.1665))

[[!redirects totalizations]]