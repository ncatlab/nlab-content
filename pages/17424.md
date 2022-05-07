
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _real projective space_ $\mathbb{R}P^n$ is the [[projective space]] of the real [[vector space]] $\mathbb{R}^{n+1}$.

Equivalently this is the [[Grassmannian]] $Gr_1(\mathbb{R}^{n+1})$.

## Properties

### Cell structure
 {#CellStructure}

+-- {: .num_prop #RealProjectiveSpaceCWComplex}
###### Proposition
**([[CW-complex]] structure)**

For $n \in \mathbb{N}$, the real projective space $\mathbb{R}P^n$ admits the structure of a [[CW-complex]].

=--

+-- {: .proof}
###### Proof

Use that $\mathbb{R}P^n \simeq S^n/(\mathbb{Z}/2)$ is the [[quotient space]] of the [[Euclidean space|Euclidean]] [[n-sphere]] by the $\mathbb{Z}/2$-action which identifies [[antipode|antipodal points]].

The standard CW-complex structure of $S^n$ realizes it via two $k$-cells for all $k \in \{0, \cdots, n\}$, such that this $\mathbb{Z}/2$-action restricts to a homeomorphism between the two $k$-cells for each $k$. Thus $\mathbb{R}P^n$ has a CW-complex structure with a single $k$-cell for all $k \in \{0,\cdots, n\}$. 

=--


### Relation to classifying space

The infinite real projective space $\mathbb{R}P^\infty \coloneqq \underset{\longrightarrow}{\lim}_n \mathbb{R}P^n$ is the [[classifying space]] for [[real line bundles]]. It has the [[homotopy type]] of the [[Eilenberg-MacLane space]] $K(\mathbb{Z}/2,1) = B \mathbb{Z}/2$.

### Kahn-Priddy theorem

* [[Kahn-Priddy theorem]]

## Related concepts

* [[complex projective space]]

* [[classifying space]]

## References

See also:

* Wikipedia, _[Real projective space](https://en.wikipedia.org/wiki/Real_projective_space)_

Computation of [[cohomotopy]]-sets of real projective space:

* {#West71} Robert West, _Some Cohomotopy of Projective Space_, Indiana University Mathematics Journal Indiana University Mathematics Journal Vol. 20, No. 9 (March, 1971), pp. 807-827 ([jstor:24890146](https://www.jstor.org/stable/24890146))



[[!redirects real projective spaces]]
