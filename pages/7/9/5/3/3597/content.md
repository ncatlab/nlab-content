#Contents#
* automatic table of contents goes here
{:toc}

## Mixed states

Suppose we have a [[quantum state]] *Q* that arises from some random process such that the state $|\psi_{\alpha}\rangle$ has a probability $p_{\alpha}$ (we often speak of having 'prepared' the state with the associated probability).  The possible states $|\psi_{\alpha}\rangle$ need not be orthogonal and we thus call such a collection of states, a *mixed state*.  More specifically, a mixed state is often described as an *ensemble* of quantum systems.

Suppose we now measure some observable **A** on the system as a whole, i.e. on the ensemble.  The expectation value of **A** over the subset $|\psi_{\alpha}\rangle$ is $\langle A \rangle_{\alpha}=\langle\psi_{\alpha}|$**A**$|\psi_{\alpha}\rangle$.  Over the entire ensemble, this becomes

$\langle A \rangle = \sum_{\alpha}p_{\alpha}\langle A \rangle_{\alpha} = \sum_{\alpha}p_{\alpha}tr|\psi_{\alpha}\rangle\langle\psi_{\alpha}|$**A**.

## Density operator

Given the above, we define the *density operator* to be

$\mathbf{\rho}=\sum_{\alpha}|\psi_{\alpha}\rangle\langle\psi_{\alpha}|$.

We call the matrix representation of the density operator, the *density matrix*.

## Coherence

Diagonal density matrices with at least two non-zero terms on the diagonal represent *mixed states*.  Density matrices that posses non-zero off-diagonal terms represent *superposition states*.  Such states are referred to as *coherent* and the off-diagonal entries are called the *coherences*.  Any physical process that has the effect of suppressing the coherences is known as *decoherence*.

## Limitations

Note that a density operator, as the representation of the state of a quantum system, is less restrictive than a state vector which specifies the wavefunction.  However, this does mean that the density operators are not unique, i.e. two entirely different state vectors can give rise to the same density operator.

## References

Nielsen, M, and Chuang, I. *Quantum Computation and Quantum Information*, Cambridge University Press, Cambridge, 2000.

Schumacher, B. and Westmoreland, M. *Q-PSI: Quantum Processes, Systems, and Information*, Cambridge University Press, Cambridge, 2010.

## Discussion

[[Ian Durham]]:  Feel free to clean this up.
