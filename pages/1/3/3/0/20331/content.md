

#Contents#
* table of contents
{:toc}

## Idea

The [[quaternion|quaternionic]] [[projective space]] $\mathbb{H}P^n$ is the [[space]] of right (or left) [[quaternion]] [[lines]] through the origin in $\mathbb{H}^{n+1}$, hence the space of [[equivalence classes]] $[q_1, \cdots, q_{n+1}]$ of [[n-tuple|(n+1)-tuples]]  of [[quaternions]] excluding zero, under the [[equivalence relation]] given by right (or left) [[multiplication]] with non-zero quaternions

$$
  \mathbb{H}P^n
  \;\coloneqq\;
  \big\{
    [q_1, \cdots, q_{n+1}]
  \big\}
  \;\coloneqq\;
  \Big(
    \big\{
      (q_1, \cdots, q_{n+1})
    \big\} 
    \setminus 
    \{(0, \cdots, 0)\}  
  \Big)
  /_{ 
    (q_1, \cdots, q_{n+1}) 
      \sim  
    (q_1 q, \cdots, q_{n+1} q)  
    \vert 
    q \neq 0
  }
$$

## Properties
 {#Properties}

### As a coset space


As any [[Grassmannian]], quaternion projective space is canonically a [[coset space]], in this case of the [[quaternion unitary group]] $Sp(n+1)$ by the [[central product group]] [[Sp(n).Sp(1)]]:

\[
  \label{SpnCosetSpaceRealization}
  \mathbb{H}P^n
  \;\simeq\;
  \frac{
    Sp(n+1)
  }{
    Sp(n)\cdot Sp(1)
  }
\]

### As a quaternion-Kähler symmetric space (Wolf space)

By the [[coset space]]-realization (eq:SpnCosetSpaceRealization), quaternion projective space is naturally a [[quaternion-Kähler manifold]] which is also a [[symmetric space]]. As such it is an example of a [[Wolf space]].

## Related concepts

* [[real projective space]]

* [[complex projective space]]

## References

### General

See also 

* Wikipedia, _[Quaternionic projective space](https://en.wikipedia.org/wiki/Quaternionic_projective_space)_

### In string theory
  {#ReferencesInStringTheory}

[[M-theory on 8-manifolds|M-theory on the 8-manifold]] $\,\mathbb{H}P^2$, hence on a [[quaternion-Kähler manifold]] of dimension 8 with [[holonomy]] [[Sp(2).Sp(1)]], is considered in

* [[Michael Atiyah]], [[Edward Witten]], p. 75 onwards in  _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

and argued to be [[duality in string theory|dual]] to [[M-theory on G2-manifolds]] in three different ways, which in turn is argued to lead to a a possible [[proof]] of [[confinement]] in the resulting 4d [[effective field theory]] (see [there](M-theory+on+G2-manifolds#Confinement) for more).

[[!redirects quaternionic projective spaces]]

[[!redirects HP^n]]
[[!redirects HPn]]

[[!redirects HP^1]]
[[!redirects HP1]]

[[!redirects HP^2]]
[[!redirects HP2]]


