
#Contents#
* table of contents
{:toc}

## Idea

A [[spectral sequence]] induced by the [[Hodge filtration]] on a [[complex analytic space]] $X.

Write $\Omega^\bullet$ for the [[holomorphic de Rham complex]].

The Fr&#246;licher spectral sequence has the form

$$
  E_1^{p,1}
  =
  (H^q(X,\Omega^p), \partial)
   \Rightarrow
  H^{p+q}(X, \Omega^\bullet)
$$

with $E_\infty^{p,q} = Gr^p H^{p+q}(X)$ the [[associated graded]] of the [[Hodge filtration]]

$$
  F^p H^k(X,\mathbb{C})
  \coloneqq
  im\left(
    H^k(X, \Omega^{\bullet \geq p})
   \to 
    H^k(X, \Omega^\bullet)
  \right)
  \,.
$$

+-- {: .num_theorem }
###### Theorem

If $X$ is [[compact topological space|compact]] and carries the structure of a [[Kähler manifold]], then the Fr&#246;licher spectral sequence degenerates at $E_1$.

=--

Traditionally this was proven ([Fr&#246;licher 55](#Frolicher55)) by way of  [[harmonic differential forms]].  In ([Deligne-Illusie 87](#DeligneIllusie87)) this is proven instead by reduction to [[positive characteristic]].

## Related concepts

* [[Hodge-de Rham spectral sequence]]

## References

Original articles include

* {#Frolicher55} [[Alfred Frölicher]], _Relations between the cohomology groups of Dolbeault and topological invariants_, Proceedings of the National Academy of Sciences 41: 641&#8211;644 (1955)

* {#DeligneIllusie87} [[Pierre Deligne]], [[Luc Illusie]] Rel&#232;vements modulo $p^2$ et d&#182;ecomposition du complexe de de Rham_, Invent. Math. 89 (1987), no. 2, 247-270.

A textbook account is in

* {#Voisin02} [[Claire Voisin]], section 8.3.3 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3

* {#Voisin} [[Claire Voisin]], _Hodge theory and the topology of compact K&#228;hler and complex projective manifolds_ ([pdf](http://www.math.columbia.edu/~thaddeus/seattle/voisin.pdf))


[[!redirects Frolicher spectral sequence]]