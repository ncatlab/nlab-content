
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
  \mathbb{O}P^2 \,\simeq\, D^{16} \underset{h_{\mathbb{O}}}{\cup} \mathbb{O}P^1
$$

between the [[octonionic projective plane]] and the [[attaching space]] obtained from the [[octonionic projective line]] along the [[octonionic Hopf fibration]].

=--

([Lackmann 19, Lemma 3.4.](#Lackmann19))

([Mimura 67, page 166](#Mimura67))

See also at _[[cell structure of projective spaces]]_.

### Homotopy groups

+-- {: .num_prop #HomotopyGroupsOfOctonionicProjectivePlane}
###### Proposition

The [[homotopy groups]] of octonionic projective plane are
\[
  \label{ListOfHomotopyGroupsOfOctonionicProjectivePlane}
    \pi_k
    \big(
      \mathbb{O}P^2
    \big)
    \;=\;
    \left\{
    \array{
      1 &\vert& k \leq 7
      \\
      \pi_k
      \big(
        S^8
      \big)
      &\vert&
      8 \leq k \leq 14
    }
    \right.
\]
Further homotopy groups are
$$\pi_{15}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_{120}$$
$$\pi_{16}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_2^3$$
$$\pi_{17}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_2^4$$
$$\pi_{18}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_{24}\times\mathbb{Z}_2$$
$$\pi_{19}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_{504}\times\mathbb{Z}_2$$
$$\pi_{20}\big(\mathbb{O}P^2\big)
\cong 1$$
$$\pi_{21}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_6$$
$$\pi_{22}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}_4$$
$$\pi_{23}\big(\mathbb{O}P^2\big)
\cong\mathbb{Z}\times\mathbb{Z}_{120}\times\mathbb{Z}_2^2\,.$$
(While $\pi_{15}\big(S^8\big)
\cong\mathbb{Z}\times\mathbb{Z}_{120}$, which includes the [[homotopy class]] of the [[octonionic Hopf fibration]].)

=--

([Lackmann 19, page 7](#Lackmann19))

([Mimura 67, Theorem 7.2.](#Mimura67))

### Cohomology

+-- {: .num_prop #CohomologyOfOctonionicProjectivePlane}
###### Proposition

For $A \in $ [[Ab]] any [[abelian group]], then the [[ordinary cohomology]] [[cohomology groups|groups]] of octionionic projective plane $\mathbb{O}P^2$ with [[coefficients]] in $A$ are

$$
  H^k(\mathbb{O}P^2,A)
   \simeq
  \left\{
    \array{
       A & for \; k=0,8,16
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

=--

([Lackmann 19, Corollary 4.1.](#Lackmann19))

### AKM-Theorem

+-- {: .num_prop}
###### Proposition
**(octonionic [[AKM-theorem]])**

The [[13-sphere]] is the [[quotient space]] of the (right-)[[octonionic projective plane]] by the left multiplication [[action]] by [[Sp(1)]]:

$$
  \mathbb{O}P^2 / \mathrm{Sp}(1)
  \simeq
  S^{13}
$$

=--

([Atiyah-Berndt 02](#AtiyahBerndt02))



## Related concepts

* [[Cayley 4-form]]

## References

### General

* {#Lackmann19} [[Malte Lackmann]], _The octonionic projective plane_, in MATRIX Book Series **4**, Springer (2021) &lbrack;[doi:10.1007/978-3-030-62497-2_6](https://doi.org/10.1007/978-3-030-62497-2_6), [arXiv:1909.07047](https://arxiv.org/abs/1909.07047)&rbrack;

See also:

* Wikipedia, _[Cayley plane](http://en.wikipedia.org/wiki/Cayley_plane)_

* Salzmann et. al., *Compact Projective Planes, with an introduction to Octonion Geometry*


The [[AKM-theorem]] for $\mathbb{O}P^2$:

* {#AtiyahBerndt02} [[Michael Atiyah]], [[Jürgen Berndt]], in:  Surv. Differ. Geom. VIII, Papers in Honor of Calabi, Lawson, Siu and Uhlenbeck (International Press, Somerville, MA, 2003) 1-27 ([arXiv:math/0206135](https://arxiv.org/abs/math/0206135), [doi:10.4310/SDG.2003.v8.n1.a1](https://dx.doi.org/10.4310/SDG.2003.v8.n1.a1))



### In string theory

Discussion of the [[Witten genus]] of Cayley plane-[[fiber bundles]] is in

* {#McTague10} [[Carl McTague]], _The Cayley Plane and the Witten Genus_ ([arXiv:1006.0728](http://arxiv.org/abs/1006.0728))

Indications that [[M-theory]] in 10+1 dimensions may be understood as the [[KK-compactification]] on Cayley-plane [[fibers]] of some kind of [[bosonic M-theory]] in 26+1 dimensions:

* [[Hisham Sati]], _$\mathbb{O}P^2$ bundles in M-theory_, Commun. Num. Theor. Phys 3:495-530,2009 ([arXiv:0807.4899](https://arxiv.org/abs/0807.4899))

* [[Hisham Sati]], _On the geometry of the supermultiplet in M-theory_, Int. J. Geom. Meth. Mod. Phys. 8 (2011) 1-33 ([arXiv:0909.4737](https://arxiv.org/abs/0909.4737))

* [[Michael Rios]], [[Alessio Marrani]], [[David Chester]], _Exceptional Super Yang-Mills in $D=27+3$ and Worldvolume M-Theory_, Phys. Lett. B, 808, (2020)
([arXiv:1906.10709](https://arxiv.org/abs/1906.10709))

* {#Mimura67} Mamoru Mimura, _The Homotopy groups of Lie groups of low rank_, J. Math. Kyoto Univ. 6 (2) 131 - 176, 1967. [https://doi.org/10.1215/kjm/1250524375](https://doi.org/10.1215/kjm/1250524375)


[[!redirects Cayley planes]]

[[!redirects octonion projective plane]]
[[!redirects octonion projective planes]]

[[!redirects octonionic projective plane]]
[[!redirects octonionic projective planes]]


