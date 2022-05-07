
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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

In the context of [[topology]], a _topological $G$-space_ (traditionally just _$G$-space_, for short, if the context is clear) is a [[topological space]] equipped with an [[action]] of a [[topological group]] $G$ -- the _[[equivariance grouo]]_ (usually taken to be the [[topological group]] underlying a [[compact Lie group]], such as a [[finite group]]).

The canonical [[homomorphisms]] of topological $G$-spaces are $G$-[[equivariant function|equivariant]] [[continuous functions]], and the canonical choice of [[homotopies]] between these are $G$-equivariant continuous homotopies (for [[trivial action|trivial]] $G$-[[action]] on the [[interval]]). 

A $G$-[[equivariant Whitehead theorem|equivariant version]] of the [[Whitehead theorem]] says that on [[G-CW complexes]] these $G$-equivariant [[homotopy equivalences]] are equivalently those maps that induce [[weak homotopy equivalences]] on all [[fixed point]] spaces for all [[subgroups]] of $G$ (compact subgroups, if $G$ is allowed to be a [[Lie group]]). 

By [[Elmendorf's theorem]], this, in turn, is equivalent to the [[(∞,1)-presheaves]] over the [[orbit category]] of $G$. See below at _[In topological spaces -- Homotopy theory](#HomotopyTheory)_.

See ([Henriques-Gepner 07](#HenriquesGepner07)) for expression in terms of [[topological groupoids]]/[[orbispaces]].

In the context of [[stable homotopy theory]] the [[stabilization]] of $G$-spaces is given by [[spectra with G-action]]; these lead to [[equivariant stable homotopy theory]]. See there for more details. (But beware that in this context one considers the richer concept of [[G-spectra]], which have a [[forgetful functor]] to [[spectra with G-action]] but better homotopy theoretic properties. ) The union of this as $G$ is allowed to vary is the [[global equivariant stable homotopy theory]].

## Properties

### Equivariant Tietze extension theorem

See at _[[equivariant Tietze extension theorem]]_

### Model structure and homotopy theory
 {#ModelStructureAndHomotopyTheory}

The standard [[homotopy theory]] on $G$-spaces used in [[equivariant homotopy theory]] considers [[weak equivalences]] which are [[weak homotopy equivalence]] on all (ordinary) [[fixed point]] spaces for all suitable [[subgroups]]. By [[Elmendorf's theorem]], this is equivalent to [[(∞,1)-presheaves]] over the [[orbit category]] of $G$.

On the other hand there is also the standard homotopy theory of [[infinity-actions]], presented by the [[Borel model structure]], in this context also called the "coarse" or "naive" equivariant model structure ([Guillou](#Guillou)).


## Examples
  {#Examples}

We discuss some classes of examples of [[G-spaces]].

### Euclidean $G$-spaces
 {#EuclideanGSpace}

Let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] [[linear representation]] of a [[finite group]] $G$ on a [[real vector space]] $V$.
Then the underlying [[Euclidean space]] $\mathbb{R}^V$ inherits the [[mathematical structure|structure]] of a [[G-space]]

\begin{xymatrix}
   \mathbb{R}^V\ar@(ul,ur)^G
\end{xymatrix}

We may call this the _[[Euclidean G-space]]_ associated with the linear representation $V$.


### Representation spheres


Let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] [[linear representation]] of a [[finite group]] $G$ on a [[real vector space]] $V$.
Then the [[one-point compactification]] of the underlying [[Euclidean space]] $\mathbb{R}^V$ inherits the [[mathematical structure|structure]] of a [[G-space]] with the [[one-point compactification|point at infinity]] a [[fixed point]]. This is called the _$V$-[[representation sphere]]_

\begin{xymatrix}
   S^V\ar@(ul,ur)^G
   \ar@{}[r]|-{:=}
   &
   \big( \mathbb{R}^V\ar@(ul,ur)^G\big)^{\mathrm{cpt}}
\end{xymatrix}


### Representation tori

Let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] [[linear representation]] of a [[finite group]] $G$ on a [[real vector space]] $V$.

If $G$ is the [[point group]] of a [[crystallographic group]] inside the [[Euclidean group]] 

$$
  N \rtimes G
  \hookrightarrow
  Iso(\mathbb{R}^V)
$$

then the $G$-[[action]] on the Euclidean space $\mathbb{R}^V$ descends to the [[quotient]] by the [[action]] of the translational [[normal subgroup]] [[lattice in a vector space|lattice]] $N$ ([this Prop.](crystallographic+group#InducedPointGroupActionOnTorus)). The resulting $G$-space is an [[n-torus]] with $G$-action, which might be called the _[[representation torus]]_ of $V$

\begin{xymatrix}
   \mathbb{R}^V\ar@(ul,ur)^G
   \ar@{}[r]|-{:=}
   &
   \big( \mathbb{R}^V\ar@(ul,ur)^G\big)/N
\end{xymatrix}

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=13">
<img src="https://ncatlab.org/schreiber/files/ExamplesOfLinearRepsAndInducedGSpaces.jpg" width="690">
</a>
</center>

> graphics grabbed from [SS 19](equivariant+Hopf+degree+theorem#SatiSchreiber19)


### Projective $G$-space


Let $G$ be a [[finite group]] (or maybe a [[compact Lie group]]) and let $V$ be a $G$-[[linear representation]] over some [[topological field|topological]] [[ground field]] $k$.

Then the corresponding _[[projective G-space]]_ is the [[quotient space]] of the [[complement]] of the origin in (the [[Euclidean space]] underlying) $V$ by the given [[action]] of the [[group of units]] of $k$ (from the $k$-[[vector space]]-[[mathematical structure|structure]] on $V$):

$$
  k P(V)
  \;:=\;
  \big(
    V \setminus \{0\}
  \big) / k^\times
$$

and equipped with the residual $G$-[[action]] on $V$ (which passes to the [[quotient space]] since it commutes with the $k$-action, by linearity).


### G-CW complexes

See at _[[G-CW complex]]_.


## Related concepts

* [[G-set]], [[G-manifold]]

* [[fixed point space]]

* [[equivariant bundle]]

* [[cyclotomic space]]

[[!include equivariant homotopy theory -- table]]

See also

* [[rational topological G-space]]

* [[equivariant rational homotopy theory]]

  [[vector G-space]]

* [[equivariant stable homotopy theory]]

* [[equivariant rational stable homotopy theory]]


## References

* {#Bredon72} [[Glen Bredon]], chapter II of: _[[Introduction to compact transformation groups]]_, Academic Press  1972


* [[Tammo tom Dieck]], Chapter 8 in: _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979 ([doi:10.1007/BFb0085965](https://link.springer.com/book/10.1007/BFb0085965))


* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_ ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf))

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))


See also the references at _[[equivariant homotopy theory]]_.


[[!redirects topological G-spaces]]
[[!redirects topological G-spaces]]

[[!redirects G-space]]
[[!redirects G-spaces]]