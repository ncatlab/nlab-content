
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A [[group]] is __solvable__ if it is a [[finite number|finite]] iterated [[group extension]] of an [[abelian group]] by [[abelian groups]]. 

In other words, there exists a finite sequence 

$$
  \{ 1\}\subset G_1 \subset G_2 \subset \ldots \subset G_k = G,
$$

in which $G_{j-1}$ is [[normal subgroup|normal]] in $G_j$ and $G_j/G_{j-1}$ is [[abelian group|abelian]].

## Examples

### Galois groups

The terminology "solvable groups" comes from elementary [[Galois theory]]: every [[polynomial]] [[equation]] $\phi$ over an [[integral domain]] $K$ has a corresponding [[Galois group]] $Gal(\phi/K)$, and $Gal(\phi/K)$ is a solvable group if and only if $\phi$ is a [[solvable polynomial equation|solvable equation]] (meaning that all its solutions in an [[algebraic closure]] of $K$ are expressible using the elements of $K$, the field operations, and extraction of roots).


### Nilpotent groups

A [[nilpotent group]] is a solvable group given by *[[central extensions|central]]* [[group extensions]].

## Related concepts

* [[nilpotent group]]

## References

Textbooks:

* [[Cornelia Druţu]], [[Michael Kapovich]], Chapter 13 of: *Geometric group theory*, Colloquium Publications **63**, AMS 2018 ([ISBN:978-1-4704-1104-6](https://bookstore.ams.org/coll-63/), [pdf](https://courses.maths.ox.ac.uk/node/view_material/35649))

See also:

* [[eom]]: [solvable group](http://eom.springer.de/s/s086130.htm), [Lie group, solvable](http://eom.springer.de/l/l058690.htm)

* Wikipedia, *[Solvable group](http://en.wikipedia.org/wiki/Solvable_group)*


[[!redirects solvable group]]
[[!redirects solvable groups]]
[[!redirects solvable subgroup]]
[[!redirects solvable subgroups]]


[[!redirects soluble group]]
[[!redirects soluble groups]]
[[!redirects soluble subgroup]]
[[!redirects soluble subgroups]]