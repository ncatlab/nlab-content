
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

A _line Lie $n$-algebra_ over a ground [[field]] $k$ is the [[Lie n-algebra]] analog of the abelian (trivial) 1-[[dimensional]] [[Lie algebra]] on $k$.

## Definition

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}, n \geq 1$ the **line Lie $n$-algebra** 

$$
  b^{n-1} k \in L_\infty \stackrel{CE}{\hookrightarrow} dgAlg^{op}
$$

is the [[L-∞ algebra]] whose [[Chevalley-Eilenberg algebra]] 

$$
  CE(b^{n-1} \mathbb{R}) = 
    (\wedge^\bullet \langle c\rangle , d = 0)
$$

is the free graded-commutative algebra on a single generator $C$ in degree $k$ equipped with the trivial differential

$$
  d c = 0
  \,.
$$

=--


+-- {: .num_example}
###### Example

For $n = 2$ then the _line Lie 2-algebra_ is the [[Lie 2-algebra]] that comes from the [[differential crossed module]] $(\mathbb{R} \to 0)$.

=--


## Properties

* For $\mathfrak{g}$ a [[Lie algebra]] a [[cocycle]] $\mu$ in degree $n$-[[Lie algebra cohomology]] on $\mathfrak{k}$ is equivalently a morphism of [[L-∞ algebra]]s

  $$
    \mu : \mathfrak{g} \to b^{n-1}\mathbb{R}
    \,.
  $$

  More generally, for $\mathfrak{g}$ an [[L-∞ algebra]], a degree-$n$ cocycle in [[∞-Lie algebra cohomology]] is given by such a morphism.

* There is a unique (up to rescaling) indecomposable [[invariant polynomial]] on $b^{n-1} \mathbb{R}$, given by the shifted copy of the generator $c$ in the [[Weil algebra]] $W(b^{n-1}\mathbb{R})$.

  Equivalently, we have

  $$
    inv(b^{n-1}\mathbb{R}) = CE(b^n \mathbb{R})
    \,.
  $$

* The [[Lie integration]] (see there) of $b^{n-1}\mathbb{R}$ is the <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">line Lie n-group</a> $\mathbf{B}^{n-1}\mathbb{R}$.

## Related concepts

* [[translation Lie algebra]]

* [[super translation Lie algebra]]

[[!redirects line Lie n-algebras]]

[[!redirects line Lie algebra]]
[[!redirects line Lie 2-algebra]]
