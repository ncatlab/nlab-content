**Under Construction**

This page is mostly a stub right now.

See also Wikipedia's [Stinespring factorization theorem](http://en.wikipedia.org/wiki/Stinespring_factorization_theorem)


+-- {: .un_theorem}
###### Stinespring's dilation theorem

Let $T: S_{1}(\mathcal{H}) \to S_{2}(\mathcal{H})$ be a completely positive trace-preserving (CPTP) map between states on a finite-dimensional Hilbert space, $\mathcal{H}$.  Then there exists a Hilbert space $\mathcal{A}$ and a unitary operation $U$ on $\mathcal{H}\otimes\mathcal{A}$ such that

$$
   T(\rho) = Tr_{\mathcal{A}}U(\rho \otimes \rho_{\mathcal{A}})U^{\dagger}
$$

for all $\rho \in S_{n}(\mathcal{H})$, where $Tr_{\mathcal{A}}$ is the [[partial trace]] on the $\mathcal{A}$-system.  We refer to $\mathcal{A}$ as an _ancilla_ system and it is chosen such that dim$\mathcal{A}\le$dim$^{2}\mathcal{H}$.  This representation is unique up to unitary equivalence.

=--

+-- {: .query}
TO DO: Write down the proof.
=--

This dilation construction of channels and states is commonly termed the "Church of the Larger Hilbert Space" (coined by John Smolin) since it incorporates the Hilbert space of both the state under consideration as well the environment, even though the operation is on the system only in most cases (for an exception, see the discussion of open quantum systems below).  Note that Stinespring's theorem can also be used to show that every [[mixed state]] can be thought of as arising from some [[mixed state|pure state]] on a larger Hilbert space.