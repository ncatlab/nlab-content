
# Multi-adjoints

* table of contents
{: toc}

## Idea

A **multi-adjoint** is like an [[adjoint functor]] but sends each object to a family of objects rather than a single one.

## Definition

Let $G:D\to C$ be a [[functor]].  We say $G$ has a **left multi-adjoint** if for each $x\in C$ there is a [[family]] of morphisms $\{\eta_{x,i} : x \to G z_i\}_{i\in I}$ such that for any morphism $f:x\to G y$ there exists a unique pair of an index $i\in I$ and a morphism $g:z_i \to y$ such that $f = G g \circ \eta_{x,i}$.

## Examples

* Every [[parametric right adjoint]] with [[locally small category|locally small]] codomain has a left multi-adjoint.  And conversely, if $D$ has a [[terminal object]] and $G:D\to C$ has a left multi-adjoint, then it is a parametric right adjoint.

* The category of [[fields]] has a multi-initial object, i.e. the functor $Fld \to 1$ has a left multi-adjoint.  This consists of all the "prime fields", $\mathbb{Q}$ and $\mathbb{F}_p$ for some prime $p$.

## Remarks

Of course, if each set $I$ is a [[singleton]], then this is an actual [[left adjoint]].  On the other hand, if we remove the uniqueness requirement, this reduces to the [[solution set condition]].  Thus, a multi-adjoint is "halfway between" the solution-set condition and the actual existence of an adjoint.

If we weaken the notion of adjunction in the opposite way, by removing the uniqueness requirement but keeping $I$ a singleton (or equivalently add to the solution-set condition that $I$ is a singleton), we obtain a [[weak adjoint]].

## References

* Axel Osmond, _On Diers theory of Spectrum I: Stable functors and right multi-adjoints_, ([arXiv:2012.00853](https://arxiv.org/abs/2012.00853))

* Axel Osmond, _On Diers theory of Spectrum II: Geometries and dualities_, ([arXiv:2012.00853](https://arxiv.org/abs/2012.02167))

[[!redirects left multi-adjoint]]
[[!redirects right multi-adjoint]]
