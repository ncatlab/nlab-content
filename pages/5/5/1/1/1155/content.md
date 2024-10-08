

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Combinatorial spectra_ is to [[spectra]] of [[topological spaces]] as a [[simplicial sets]] are to [[topological spaces]]: 

Combinatorial spectra are [[graded sets]] that behaves like a set of [[simplices]] constituting a space, but such that the simplices are not just in [[natural number|non-negative]] degree $n \in \mathbb{N}$ but in all [[integer|integral]] degrees $n \in \mathbb{Z}$, hence including negative degrees.

## Definition

A **combinatorial spectrum** is ([Kan 63, def. 4.1](#Kan63)) 

* a sequence $E = \{E_n\}_{n \in \mathbb{Z}}$ of [[pointed set]]s 

* equipped for each $n \in \mathbb{Z}$ and $i \in \mathbb{N}$ with

  * morphisms of [[pointed set]]s $d_i : E_n \to E_{n-1}$ called **face maps**;

  * morphisms of [[pointed set]]s $s_i : E_n \to E_{n+1}$ called **degeneracy maps**

* such that

  * the usual [[simplicial set|simplicial identities]] are satisfied;

  * each simplex has only finitely many faces different from the point of $E_{n-1}$: i.e. for every $x \in E_n$ there are only finitely many $i \in \mathbb{N}$ for which $d_i(x)$ is not the point.

## Examples

The standard [[simplicial set]]s corresponding to the standard [[simplex|simplices]] have their analogs for simplicial spectra. The difference is that regarded as a spectrum the $k$-simplex may sit in any degree $n \in \mathbb{N}$, not necessarily in degree $k$.

**The $(k+1)$-simplex in degree $n$.** For each integer $n \in \mathbb{Z}$ and $k \in \mathbb{N}$ there is a spectrum 

$$
  \Delta^{k}[n-k]
$$ 

which is _generated_ from a single element $x \in E_n$ subject to the relation that $d_i x = *$ for $i \gt k$.  So this is something with $(k+1)$-faces, hence looking like a $k$-[[simplex]], but sitting in degree $n$. 

The sub-spectrum

$$
  \partial (\Delta^{k}[n-k])
$$ 

of $\Delta^{k}[n-k]$ generated by the faces $d_i x$. This is the **boundary** of the $k$-simplex in degree $n$.

The spectrum

$$
  S^n
$$

generated by a single simplex $x \in E_n$ subject to the relation $d_i x = 0$ for all $i$. This is the **$n$-sphere** as a spectrum.


The sub-spectrum $\Lambda^{k}_j[n-k]$ for $0 \leq j \leq k$ is the sub-spectrum of $\Delta^{k}[n-k]$ generated from all the faces $d_i x$ except $d_j x$. This is the  $j$th **horn** of the $k$-simplex in degree $n$. Compare with the [[horn]] of a [[simplex]].

As for [[simplex|simplices]], there are canonical [[horn]] inclusion morphisms of combinatorial spectra

$$
  \Lambda^k_j[n-k] \hookrightarrow \Delta^k[n-k]
  \,.
$$

A condition entirely analogous to the [[Kan fibration]] condition on [[Kan complex|Kan simplicial sets]] leads to the notion of **Kan combinatorial spectrum**.

## Properties

### Model category structure
 {#ModelCategoryStructure}

The category of combinatorial spectra admits a [[model
structure]] ([Brown 73](#Brown73)), whose cofibrations are monomorphisms
and weak equivalences are maps that induce isomorphisms
on homotopy groups.

Generating (acyclic) cofibrations are given by inclusions
of horns respectively boundaries into stable simplices,
as defined in the previous section, in complete analogy
with the usual Kan-Quillen model structure
on simplicial sets.
(Acyclic) fibrations are maps satisfying
the corresponding lifting properties.

This is indeed a [[model structure for spectra]], related by a [[zig-zag]] of [[Quillen equivalences]] to the [[Bousfield-Friedlander model structure]] on [[sequential spectra]]  ([Bousfield-Friedlander 78, section 2.5](#BousfieldFriedlander78)). See also [below](#RelationshipToOtherSpectra).

### Smash product

In ([Brown 73, Appendix&#160;A](#Brown73)) is defined a  [[smash product of spectra]] on the [[homotopy category]] of combinatorial spectra.
The main idea is to define the smash product
of a stable $m$-simplex and a stable $n$-simplex
to be the stable $(m+n)$-simplex whose face maps
are defined using the face maps of the two simplices
involved using a formula that somewhat resembles
the formula for the differential of the tensor
product of two chain complexes.

Whether or not it is possible to introduce a symmetric
monoidal smash product on the category of combinatorial
spectra obtaining a [[monoidal model category]]
that is Quillen equivalent to the
monoidal model category of (say)
symmetric simplicial spectra is currently
an open problem.


### Relationship to other spectra
 {#RelationshipToOtherSpectra}

From the perspective of a combinatorial spectrum, an "intuitive spectrum" is supposed to be some sort of space-like object having "cells in all integer dimensions," while a "space" (or simplicial set) has cells only in nonnegative dimensions.  The traditional definitions of spectra approximate this intuition by using a *sequence* of spaces $\{E_n\}$ with maps $E_n \to \Omega E_{n+1}$ or $\Sigma E_n \to E_{n+1}$, where we think of the space $E_n$ as being "shifted down by $n$ dimensions."  Thus, for instance, the $(-2)$-cells of the spectrum can come from 0-cells of $E_2$, or 1-cells in $E_3$, or 2-cells in $E_4$, etc.  The structure maps $\Sigma E_n \to E_{n+1}$ support this intuition, since the suspension $\Sigma$ shifts things up by one dimension; thus it maps the $k$-cells of $E_n$ into the $k+1$-cells of $E_{n+1}$.

In fact, this can be made precise: starting from a spectrum of simplicial sets, in the sense of a sequence of spaces with maps $\Sigma E_n \to E_{n+1}$, one can construct a combinatorial spectrum by "piecing together" the cells in all dimensions.  This construction can be found in Kan's original article; it provides an equivalence 
of [[homotopy theories]] between combinatorial spectra and ordinary spectra built from simplicial sets. In ([Bousfield-Friedlander 78, section 2.5](#BousfieldFriedlander78)) this is lifted to a [[zig-zag]] of [[Quillen equivalence]] between the model structure for Kan's combinatorial spectra and the [[Bousfield-Friedlander model structure]] on [[sequential spectra]] in [[sSet]] to 

[[Mike Shulman|I]] don't know whether anyone has gone back to treat combiantorial from a "modern" standpoint, such as by putting a [[monoidal model category]] structure on combinatorial spectra.  They do seem less interesting and useful from a modern standpoint, because no one has ever managed to give them a [[smash product]] which is associative and unital on the point-set level; thus they don't provide a good framework for talking about ($A_\infty$ or $E_\infty$) ring spectra, module spectra, and other aspects of [[brave new algebra]].  It's also not clear how hard anyone has tried, though.  Presumably one would have to modify the definition by incorporating the "symmetries" somehow, as is done for example by passing from ordinary simplicial-set spectra to [[symmetric spectrum|symmetric spectra]].

### Stable Dold-Kan correspondence

Combinatorial spectra [[internalization|internal]] to [[abelian groups]] ([Kan 63, def. 51](#Kan63)) are [[equivalence of categories|equivalent]] to [[chain complexes]] ([Kan 63, prop.5.8](#Kan63)). See at _[[stable Dold-Kan correspondence]]_ for more on this.

## Related concepts

* [[(∞,Z)-category]]

## References

An early reference is

* {#Kan63} [[Daniel Kan]], _Semisimplicial spectra_, Illinois J. Math. Volume 7, Issue 3 (1963), 463-478. ([Euclid](http://projecteuclid.org/euclid.ijm/1255644953))

see also at _[[stable Dold-Kan correspondence]]_.

The definition is recalled in part II, section 7 of 

* {#Brown73} [[Kenneth Brown]], _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_, 1973

Discussion of the relation (equivalence of [[homotopy categories]]) to the [[Bousfield-Friedlander model structure]] on [[sequential spectra]] in [[simplicial sets]] is in

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], section 2.5 of _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf))

See also

* Ruian Chen, [[Igor Kriz]] and Ales Pultr, _Kan's combinatorial spectra and their sheaves revisited_, Theory and Applications of Categories, Vol. 32, 2017, No. 39, pp 1363-1396. ([TAC](http://www.tac.mta.ca/tac/volumes/32/39/32-39abs.html)) 

[[!redirects combinatorial spectra]]

[[!redirects model structure on combinatorial spectra]]
