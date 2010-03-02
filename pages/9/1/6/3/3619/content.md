<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Product States

Consider two [[quantum system]]s, $A$ and $B$, with state vectors $|\Psi^{(A)}\rangle$ and $|\Psi^{(B)}\rangle$ respectively.  The combined state of the system may be described by a single state vector $|\Psi^{(AB)}\rangle=|\Psi^{(A)}\rangle \otimes |\Psi^{(B)}\rangle$.

## Example

As an example, suppose that in the basis $\{|0\rangle ,|1\rangle\}$, $|\Psi^{(A)}\rangle = \frac{1}{\sqrt{2}}\left(|0\rangle +|1\rangle\right)$.  This can be interpreted as system $A$ being in state $|0\rangle$ with probability 1/2 and state $|1\rangle$ with probability 1/2.  Suppose further that $|\Psi^{(B)}\rangle = |0\rangle$.  Then we have

$|\Psi^{(AB)}\rangle=|\Psi^{(A)}\rangle \otimes |\Psi^{(B)}\rangle=\frac{1}{\sqrt{2}}\left(|0\rangle +|1\rangle\right)\otimes|0\rangle=\frac{1}{\sqrt{2}}\left(|00\rangle +|10\rangle\right)$.

Such a state is said to be a **product state** because it is "factorable," i.e. it can be formed from some combination of individual states in the basis.

## Entangled States

Compare the above example to the state

$|\Psi^{(AB)}\rangle=\frac{1}{\sqrt{2}}\left(|00\rangle +|11\rangle\right)$.

This state is not a product state since it cannot be formed from any combination of individual states in the given basis.  Such a state is known as an **entangled state** because it is said to be "non-factorable."  Entangled states are, in fact, [[pure states]] rather than [[mixed states]] because they cannot be broken down further.

The formation of entangled states requires an external action that, mathematically, takes the form of some type of unitary operator acting on a product state.  Physically this usually entails interacting systems $A$ and $B$ in some way, e.g. one method for entangling photons is producing them from the same source.

## Discussion

[[Ian Durham]]: Feel free to clean this up a bit.

[[!redirects entangled state]]
[[!redirects entangled]]
[[!redirects separable]]