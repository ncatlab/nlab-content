<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A closed time-like curve (sometimes colloquially termed a [[wormhole]]) have seen a resurgence of interest in recent years, particularly in relation to [[quantum information]] (though not exclusive to it).  A closed time-like curve (CTC) can be described by a metric whose time dimension is circular, i.e. it wraps around on itself.  There are numerous paradoxes that arise when considering such curves and many physicists doubt their existence.  Under certain circumstances, however, they are allowed under the rules of [[general relativity]].

## The Deutsch-Bacon consistency condition

In 1991 David Deutsch proposed the following criterion, later further explored by Dave Bacon, in order for consistency to be maintained for [[quantum states]] on a closed time-like curve.

A quantum system $A$ has [[density operator]] $\rho_{A}$.  It interacts with a quantum system $E$ with density operator $\rho_{env}$ that is on an closed time-like curve.  Under a [[unitary]] operation, $\rho_{env}$ cannot evolve, i.e.

$$
\rho_{env} = Tr_{A}[U(\rho_{A}\otimes\rho_{env})U^{\dagger}]
$$

where $Tr_{A}$ is the [[partial trace]].  Note that this construction explicitly employs the [[quantum operation]] formalism and is considered to be an [[open quantum system]].

### Criticism

Note that since multiple wavefunctions can produce the same density operator, this consistency condition allows the wavefunction to change.  In addition, the condition is not strict enough to be used to _identify_ a quantum system on a CTC since some common quantum processes obey this equation somewhat accidentally.

## The strong consistency condition

A stronger consistency condition (see paper by Durham below) would prevent the wavefunction from evolving.  Thus suppose we have a quantum system $|A\rangle$ interacting with a quantum system $|E\rangle$ that is on a CTC.  The strong consistency condition requires

$$
(|A^{\prime}\rangle \otimes |E\rangle) = U(|A\rangle \otimes |E\rangle)
$$

where $|A^{\prime}\rangle$ is the state of system $A$ after the unitary evolution.

+--{: .query}
Ian: So, how can we tackle CTCs with categories?
=--

## References

* Dave Bacon, _Quantum Computational Complexity in the Presence of Closed Timelike Curves_ ([pdf](http://arxiv.org/pdf/quant-ph/0309189v3))

* Charles H. Bennett, Debbie Leung, Graeme Smith, John A. Smolin, _Can closed timelike curves or nonlinear quantum mechanics improve quantum state discrimination or help solve hard problems?_ ([pdf](http://arxiv.org/pdf/0908.3023))

* Ian T. Durham, _Quantum communication on closed time-like curves_ ([pdf](http://arxiv.org/pdf/0803.3287v3))

* T.C. Ralph, _Unitary Solution to a Quantum Gravity Information Paradox_ ([pdf](http://arxiv.org/pdf/0708.0449v1))

[[!redirects closed time-like curve]]
[[!redirects closed timelike curve]]
[[!redirects closed time like curve]]
[[!redirects closed timelike curves]]
[[!redirects closed time like curves]]