
#Contents#
* table of contents
{:toc}

## Idea

The _Cayley plane_ is the [[projective plane]] over the [[octonions]], i.e. the [[octonionic projective space]] $\mathbb{O} P^2$.

## Definition

The Cayley plane can't be constructed using homogeneous coordinates the way it works for projective planes over [[division rings]], since multiplication of octonions is not associative.  However, it can be constructed in several other ways that generalize the approach for division rings:

* One can start with $\mathbb{O}^2$ and give it the structure of an [[affine plane]] in the obvious way, and then add "points at infinity" in the usual way to obtain a projective plane.  This is the most straightforward approach, but as always it has the defect that it makes the line at infinity appear special.

* One can consider the space of $3\times 3$ matrices over $\mathbb{O}$ that are "Hermitian" and idempotent, hence can be imagined as "projections onto dimension-1 subspaces of $\mathbb{O}^3$".

* Writing out the components of such a matrix explicitly, one obtains a *Veronese vector* $(x_1,x_2,x_3;\xi_1,\xi_2,\xi_3)$ where $x_i\in \mathbb{O}$ and $\xi_i\in \mathbb{R}$, such that $\xi_i \overline{x_i} = x_j x_k$ and $\Vert x_i\Vert^2 = \xi_j \xi_k$ for all cyclic permutations $(i,j,k)$ of $(1,2,3)$.  The Cayley plane can be identified with the space of nonzero such vectors modulo the scalar action of $\mathbb{R}$.

## Properties

### General

The octonionic projective plane is a non-Desarguesian plane, that is, [[Desargues' theorem]] does not hold. See [[projective plane]].



### Isometries

* [[F4]] is the [[isometry group]] of $\mathbb{O} P^2$, with the [[stabilizer]] of a point being [[Spin(9)]]. Hence $\mathbb{O} P^2 \cong F_4/Spin(9)$.


### Cell structure

+-- {: .num_prop} 
###### Proposition

There is a [[homeomorphism]]

$$
  \mathbb{O}P^2 \,\simeq\, S^{15} \underset{h_{\mathbb{O}}}{\cup} \mathbb{O}P_1
$$

between the [[octonionic projective plane]] and the [[attaching space]] obtained from the [[octonionic projective line]] along the [[octonionic Hopf fibration]].

=--

([Lackman 19, Lemma 3.4](#Lackman19))

See also at _[[cell structure of projective spaces]]_.



## Related concepts

* [[Cayley 4-form]]

## References

* {#Lackman19} [[Malte Lackmann]], _The octonionic projective plane_ ([arXiv:1909.07047](https://arxiv.org/abs/1909.07047))


See also:

* Wikipedia, _[Cayley plane](http://en.wikipedia.org/wiki/Cayley_plane)_

* Salzmann et. al., *Compact Projective Planes, with an introduction to Octonion Geometry*

Discussion of the [[Witten genus]] of Cayley plane-[[fiber bundles]] is in

* {#McTague10} [[Carl McTague]], _The Cayley Plane and the Witten Genus_ ([arXiv:1006.0728](http://arxiv.org/abs/1006.0728))


[[!redirects Cayley planes]]

[[!redirects octonion projective plane]]
[[!redirects octonion projective planes]]

[[!redirects octonionic projective plane]]
[[!redirects octonionic projective planes]]


