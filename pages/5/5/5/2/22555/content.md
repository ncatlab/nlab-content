

#Contents#
* table of contents
{:toc}

## Idea

In [[quantum information theory]], a *stabilizer code* is a [[quantum error correcting code]] whose [[code subspace]] is the [[fixed subspace]] of an [[abelian group|abelian]] [[subgroup]] $\{-1\} \notin S \subset \mathcal{P}_n$ of the [[Pauli group]] $\mathcal{P}_n$ [[group action|acting]] on a register of $n$ [[q-bits]].

Conversely, $S \subset \mathcal{P}_n$ is then the [[stabilizer subgroup]] of the code space, whence the name of this class of codes.

Most [[quantum error correcting codes]] known are in fact stabilizer codes.

The condition $\{-1\} \notin S$ is necessary for the code subspace not to be trivial (the zero space). Notice that this implies that the elements with phases $\pm i$ in the definition ([here](Pauli+group#eq:PauliGroupAsMatrixSubgroup)) of the [[Pauli group]] do not appear in the stabilizer group $S$ (for their square would be $-1$), whence the stabilizer group is actually a subgroup of a tensor power $Q_n \subset \mathcal{P}_n$ of the [[quaternion group]] inside the [[Pauli group]] (see [there](Pauli+group#RelationToQuaternionGroup)).

## Properties

### Relation to classical binary codes

Quantum stabilizer codes are closely related to classical [[error correcting codes]], specifically to [[binary linear codes]].

(e.g. [Ball, Centelles & Huber 20, Sec. 2.3](#BallCentellesHuber20))

## References

Stabilizer codes were introduced in:

* [[Daniel Gottesman]], *Stabilizer Codes and Quantum Error Correction* ([arXiv:quant-ph/9705052](https://arxiv.org/abs/quant-ph/9705052))

following

* [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

* [[Andrew M. Steane]], *Multiple Particle Interference and Quantum Error Correction*,  	Proc. Roy. Soc. Lond. A452 (1996) 2551 ([arXiv:quant-ph/9601029](https://arxiv.org/abs/quant-ph/9601029))




Review:

* {#BallCentellesHuber20} Simeon Ball, Aina Centelles, Felix Huber, Section 2 of: *Quantum error-correcting codes and their geometries* ([arXiv:2007.05992](https://arxiv.org/abs/2007.05992))

See also

* Wikipedia, *[Stabilizer code](https://en.wikipedia.org/wiki/Stabilizer_code)*

Realization in [[experiment]]:

Realization of [[quantum error correction]] in [[experiment]]:

* D. G. Cory, M. D. Price, W. Maas, [[Emanuel Knill]], [[Raymond Laflamme]], [[Wojchiek H. Zurek]], T. F. Havel, and S. S. Somaroo, *Experimental Quantum Error Correction*, Phys. Rev. Lett. 81, 2152 (1998) ([doi:10.1103/PhysRevLett.81.2152](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.81.2152))




[[!redirects stabilizer codes]]

[[!redirects quantum stabilizer code]]
[[!redirects quantum stabilizer codes]]
