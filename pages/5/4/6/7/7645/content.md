
> for disambiguation see _[[wreath product]]_

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Let $A$ be a [[small category]]. Its _categorical wreath product_  with the [[simplex category]] is the category $\Delta \wr A$ whose

* objects are $k$-tuples $([k], (a_1, \cdots, a_k))$ of objects of $A$, for any $k \in \mathbb{N}$;

* morphisms are tuples 

  $$
    (\phi, \phi_{i j}) : ([k],(a_1, \cdots, a_k)) \to ([l],(b_1, \cdots, b_l))
  $$ 

  consisting of 

  * a morphism $\phi: [k] \to [l]$ in $\Delta$;

  * morphisms $\phi_{i j} : a_i \to b_j$ for $0 \lt i \leq k$ and $\phi(i-1) \lt j \leq \phi(i)$.

=--

([Berger, def. 3.1](#Berger)).

+-- {: .num_remark}
###### Remark

An object of $\Delta \wr A$ is to be thought of as a sequence of morphisms labeled by objects of $A$

$$
  \array{
    0
    \\
    \downarrow \mathrlap{a_1}
    \\
    1 
    \\
    \downarrow \mathrlap{a_2}
    \\
    \downarrow
    \\
    \vdots
    \\
    \downarrow \mathrlap{a_n}
    \\
    n
  }
$$

and morphisms are given by maps between these linear orders equipped with morphisms from the $k$th object in the source to all the objects in the target that sit in between the image of the $k$th step.

=--

## Examples

* The $k$-fold wreath product of the [[simplex category]] with itself is the 
  $n$th [[Theta-category]] $\Theta_n = \Delta^{\wr n}$.

* Other applications are discussed at _[[club]]_ and at _[[terminal coalgebra of an endofunctor]]_.

## References

Section 3 of 

* [[Clemens Berger]], _Iterated wreath product of the simplex category and iterated loop spaces_ ([arXiv:math/0512575](http://arxiv.org/abs/math/0512575)),
  {#Berger}

[[!redirects categorical wreath products]]
