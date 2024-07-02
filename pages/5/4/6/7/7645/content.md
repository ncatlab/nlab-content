
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


* {#BarrWells95} [[Michael Barr]], [[Charles Wells]], Section 12.4 of: *Category theory for computing science*, Prentice-Hall International Series in Computer Science (1995); reprinted in: Reprints in Theory and Applications of Categories **22** (2012) 1-538 &lbrack;[pdf](http://www.math.mcgill.ca/barr/papers/ctcs.pdf), [tac:tr22](http://www.tac.mta.ca/tac/reprints/articles/22/tr22abs.html)&rbrack;

See also:

* [[Charles Wells]]: _A Krohn-Rhodes theorem for categories_, J. Algebra **64** 1 (1980) 37-45 \[<a href="https://doi.org/10.1016/0021-8693(80)90130-1">doi:10.1016/0021-8693(80)90130-1</a>\]

* Valdis Laan: _Wreath product of set-valued functors and tensor multiplication_, Semigroup Forum. **70** Springer (2005) \[<a href="https://doi.org/10.1007/s00233-004-0162-9">doi:10.1007/s00233-004-0162-9</a>\]


* {#Berger} [[Clemens Berger]], Section 3 of: _Iterated wreath product of the simplex category and iterated loop spaces_, Advances in Mathematics **213** 1 (2007) 230-270 &lbrack;[arXiv:math/0512575](http://arxiv.org/abs/math/0512575), [doi:10.1016/j.aim.2006.12.006](https://doi.org/10.1016/j.aim.2006.12.006)&rbrack;
  

[[!redirects categorical wreath products]]
