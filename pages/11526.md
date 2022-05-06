
#Contents#
* table of contents
{:toc}

## Idea

In [[equivariant stable homotopy theory]] over a [[compact Lie group]] $G$, a _$G$-universe_ is a $G$-[[representation]] that contains "all" representations of $G$ of sorts. 

This is used in one definition of [[G-spectra]] via [[looping and delooping]] by [[representation spheres]].

## Definition

A **[[G-universe]]** in this context is (e.g. [Greenlees-May, p. 10](#GreenleesMay)) an infinite dimensional real [[inner product space]] equipped with a linear $G$-[[action]] that is the [[direct sum]] of countably many copies of a given [[set]] of (finite dimensional) [[representations]] of $G$, at least containing the trivial representation on $\mathbb{R}$ (so that $U$ contains at least a copy of $\mathbb{R}^\infty$).

## Applications

### Infinite complex projective $G$-space

+-- {: .num_defn #InfiniteProjectiveGSpace}
###### Definition
**([[infinite complex projective G-space]])**

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

This concept is at the heart of _[[equivariant complex oriented cohomology theory]]_.


## Related concepts

* [[RO(G)-grading]]

* [[infinite projective G-space]]

## References

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))


[[!redirects G-universes]]