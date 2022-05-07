

# Dimension
* table of contents
{: toc}

## Idea

A notion of _dimension_ is a notion of "size" of [[object]]s. There are various variations of what exactly this means, applicaple in various contexts, that tend to agree when they jointly apply.

### Of spaces

There are many notions of _dimension_ of [[space]]s.  What they all have in common is that the [[cartesian space]] $\mathbb{R}^n$ has dimension $n$.

*  The __dimension__ of a [[vector space]] $V$ is the [[cardinality]] of any [[set]] $X$ such that $V$ is [[free object|free]] (as a vector space) on $X$.  (It is a theorem, equivalent to the [[axiom of choice]], that every vector space has a unique dimension.)  For [[modules]] over [[rings]] that are not [[fields]] (for which the theorem above does not hold, neither existence nor uniqueness) the term used is [[rank]].

   The trace of a vector space coincides with its categorical trace in the [[symmetric monoidal category]] [[Vect]] of [[vector space]]s.

*  A [[manifold]] has [[dimension of a manifold]]equal to $n$ if it is locally isomorphic to the [[Cartesian space]] $\mathbb{R}^n$.  A [[complex manifold]] is of __complex dimension__ $n$ if it is locally isomorphic to $\mathbb{C}^n$, hence has (real) dimension $2 n$.

*  A [[topological space]] $X$ has (Lebesgue) __[[covering dimension]]__ less than $n$ if every [[open cover]] $U$ of $X$ has a [[refinement]] $V$ such that every element of $X$ belongs to fewer than $n + 1$ elements of $V$.  (Then $X$ has dimension $n$ if it has dimension less than $n + 1$ but not less than $n$.)  By [[negative thinking]], this makes sense for $n \geq -1$; precisely the [[empty space]] has dimension $-1$, and precisely the [[point]] (of course) has dimension $0$.

* A [[CW-complex]] has [[dimension of a CW-complex]], this being the largest $n$ for which there are nontrivial $n$-[[cells]].

*  A [[metric space]] has a __[[Hausdorff dimension]]__ which may be any non-negative real number.

* A space in [[noncommutative geometry]] ([[spectral geometry]] via [[spectral triples]]) may have a notion of [[KO-dimension]].

See also

  * [[homotopy dimension]]

  * [[cohomology dimension]]

  * [[Heyting dimension]]

### Of objects in an abelian category: Length

See at _[[length of an object]]_.

### Of objects in a symmetric monoidal category: Euler characteristic

The dimension of a (finite dimensional) [[vector space]] $V$ over a [[field]] $k$ is equivalently the [[trace]] of the [[identity]] [[morphism]] in the [[symmetric monoidal category]] [[Vect]] (which is a linear map $k \to k$, canonically identified with an element in $k$)

$$
  tr(V) := tr(Id_V) : k \to V \otimes V^* \stackrel{\simeq}{\to} V^* \otimes V \to k
  \,.
$$

Therefore it makes sense for any [[symmetric monoidal category]] $C$ and every [[dualizable object]] $V$ to call $tr(Id_V) : 1 \to 1$ the _categorical trace of $V$. 

This definition subsumes standard notions of _[[Euler characteristic]]_ and hence may also be thought of as generalizing that notion.

### Of objects in an $(\infty,1)$-topos

The following notions of dimension capture aspects of the concept for objects in a [[topos]] or more generally an [[(∞,1)-topos]]:

* [[homotopy dimension]]

* [[cohomological dimension]] 

* [[covering dimension]]

* [[Heyting dimension]]

### Frobenius-Perron dimension

* [[Frobenius-Perron dimension]]

## Properties

* [[global dimension theorem]]

* [[topological invariance of dimension]]

## Related concepts

[[!include notions of dimension -- contents]]


## References

For the dimension in symmetric monoidal categories see the references at [[Euler characteristic]].

A general abstract [[(∞,1)-topos theory|(∞,1)-topos theoretic]] discusssion of notions of homotopy/cohomology/covering _dimension_ is in section 7.2 of 


* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects dimension]]
[[!redirects dimensions]]

[[!redirects dimensional]]
