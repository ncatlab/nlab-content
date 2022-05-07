
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

The *Pauli group* $\mathcal{P}_1$ is the [[finite group]] of [[order of a group|order]] 16 which is [[isomorphism|isomorphic]] to the [[subgroup]] of the [[complex numbers|complex]] [[general linear group]] $GL(2,\mathbb{C})$ that consists of the multiples by $\pm 1$ and $\pm i$  of the four [[Pauli matrices]] $\sigma_{0,1,2,3}$:

\[
  \label{PauliGroupAsMatrixSubgroup}
  \mathcal{P}_1
  \;\coloneqq\;
  \big\{
    \pm \sigma_0,
    \,
    \pm \sigma_1,
    \,
    \pm \sigma_2,
    \,
    \pm \sigma_3,
    \,\;
    \pm i \sigma_0,
    \,
    \pm i \sigma_1,
    \,
    \pm i \sigma_2,
    \,
    \pm i \sigma_3,
  \big\}
  \;\subset\;
  GL(2,\mathbb{C})
  \,,
\]

where

$$
  \sigma_0
  \;\coloneqq\;
  \left[
  \array{
    1 & 0 
    \\
    0 & 1
  }
  \right]
  ,\,\;
  \sigma_1
  \;\coloneqq\;
  \left[
  \array{
    0 & 1 
    \\
    1 & 0
  }
  \right]
  ,\,\;
  \sigma_2
  \;\coloneqq\;
  \left[
  \array{
    1 & 0 
    \\
    0 & -1
  }
  \right]
  ,\,\;
  \sigma_3
  \;\coloneqq\;
  \left[
  \array{
    0 & -i 
    \\
    i & 0
  }
  \right]
  \,.
$$

In [[quantum information theory]] one often considers the higher Pauli group $\mathcal{P}_n$ whose elements are (multiples by $\pm 1$, $\pm i$) of $n$-fold [[tensor products of vector spaces|tensor products]] of the Pauli matrices.

## Properties

### Relation to the quaternion group
 {#RelationToQuaternionGroup}

The [[quaternion group]] $Q$ is the ([[normal subgroup|normal]]) [[subgroup]] of the Pauli group (eq:PauliGroupAsMatrixSubgroup) omitting the $\pm 1$-phases on nonidentity matrices:

\[
  \label{QuaternionGroupAsMatrixSubgroup}
  Q
  \;\simeq\;
  \big\{
    \pm \sigma_0,
    \,
    \pm i\sigma_1,
    \,
    \pm i\sigma_2,
    \,
    \pm i\sigma_3,
  \big\}
  \;\subset\;
  GL(2,\mathbb{C})
  \,,
\]

In fact, the Pauli group is a [[semidirect product group]] of the [[quaternion group]] with the [[cyclic group of order 2]]:

$$
  \mathcal{P}_1
  \;\simeq\;
  Q \rtimes \mathbb{Z}/2
  \,.
$$

## Related concepts

* [[stabilizer code]]

## References

See also:

* Wikipedia, *[Pauli group](https://en.wikipedia.org/wiki/Pauli_group)*

Discussion in the context of [[quantum error correction codes]]:

* Simeon Ball, Aina Centelles, Felix Huber, p. 8 of: *Quantum error-correcting codes and their geometries* ([arXiv:2007.05992](https://arxiv.org/abs/2007.05992))


[[!redirects Pauli groups]]

