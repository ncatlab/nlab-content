
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $G$ a suitable [[equivariant homotopy theory|equivariance group]], the _infinite projective G-space_ is the [[projective G-space]] corresponding to the "complete infinite $G$-representation", namely to a given [[G-universe]].

Over the [[ground field]] of [[complex numbers]] this is the generalization to [[topological G-spaces]]/$G$-[[equivariant homotopy theory]] of the infinite [[complex projective space]], hence the [[classifying space]] for [[complex line bundles]], now classifying [[equivariant bundle|equivariant]] [[complex line bundles]].

## Definition

+-- {: .num_defn #InfiniteProjectiveGSpace}
###### Definition
**([[classifying space|infinite]] [[complex projective space|complex]] [[projective G-space]])**

For $G$ an [[abelian group|abelian]] [[compact Lie group]], let 

\[
  \label{GUniverseForInfiniteComplexProjectiveSpace}
  \mathcal{U}_G
  \;\coloneqq\;
  \underset{k \in \mathbb{N}}{\bigoplus}
  \underset{\mathbf{1}_V \in R(G)}{\bigoplus}
  \mathbf{1}_V
\]

be the [[G-universe]] being the infinite [[direct sum]] of all [[complex numbers|complex]] 1-[[dimension|dimensional]] [[linear representations]] of $G$, regarded as a [[topological G-space]] with [[topological space|toplogy]] the [[colimit]] of its [[finite dimensional vector space|finite-dimensional]] [[linear subspaces]].


Then the _[[infinite complex projective G-space]]_ is the [[colimit]]

$$
  P\big( 
    \mathcal{U}_G
  \big)
  \;\coloneqq\;
  \underset{
    \underset{
      {
        V \subset \mathcal{U}_G
      }
      \atop
      {
         dim(V) \lt \infty
      }
    }{\longrightarrow}
  }{\lim}
  P\big( V \big)
$$

of the [[projective G-spaces]] for all the [[finite dimensional vector space|finite-dimensional]] $G$-[[linear representations]] inside the [[G-universe]] (eq:GUniverseForInfiniteComplexProjectiveSpace).


=--

(e.g. [Greenlees 01, Sec. 9.2](#Greenlees01))

## Related concepts

* [[equivariant complex oriented cohomology theory]]

## References

* {#Greenlees01} [[John Greenlees]], Section 9.A of: _Equivariant formal group laws and complex oriented cohomology theories_, Homology Homotopy Appl. Volume 3, Number 2 (2001), 225-263 ([euclid:hha/1139840255](https://projecteuclid.org/euclid.hha/1139840255))

[[!redirects infinite complex projective G-spaces]]

[[!redirects infinite projective G-space]]
[[!redirects infinite projective G-spaces]]

