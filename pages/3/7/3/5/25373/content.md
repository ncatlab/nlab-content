
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What has come to be known as *measurement based quantum computation* is a scheme for [[quantum computation]] in which [[quantum gates]] are implemented by partial [[quantum measurement]] on [[entanglement|entangle states]] ([[Bell states]]).

Due to [[wavefunction collapse]] upon [[quantum measurement]], such processes are not [[reversible computation|reversible]] on the total [[quantum state space]] --- conversely, each such measurement-based gate operation "uses up the entanglement-resource" in order to implement ([[reversible computation|reversible]]) [[quantum gates]] on a computational subspace. Therefore one also speaks of "one-way quantum computation" &lbrack;[Raussendorf &Briegel (2001)](#RaussendorfBriegel01)&rbrack;.

## Related concepts

* [[quantum measurement]]

* [[quantum teleportation]]

* [[quantum computation]]

  * [[adiabatic quantum computation]]

  * [[topological quantum computation]]


## References

The original articles:

* [[Daniel Gottesman]], [[Isaac L. Chuang]], *Quantum Teleportation is a Universal Computational Primitive*, Nature **402** (1999) 390-393 &lbrack;[doi:10.1038/46503](https://doi.org/10.1038/46503), [arXiv:quant-ph/9908010](https://arxiv.org/abs/quant-ph/9908010)&rbrack;

* [[Emanuel Knill]], [[Raymond Laflamme]], [[Gerard J. Milburn]], *A scheme for efficient quantum computation with linear optics*, Nature **409** (2001) 46–52 &lbrack;[doi:10.1038/35051009](https://doi.org/10.1038/35051009)&rbrack;

* {#RaussendorfBriegel01} [[Robert Raussendorf]], [[Hans J. Briegel]], *A One-Way Quantum Computer*, Phys. Rev. Lett. **86** (2001) 5188 &lbrack;[doi:10.1103/PhysRevLett.86.5188](https://doi.org/10.1103/PhysRevLett.86.5188)&rbrack;


* [[Michael Nielsen]], *Quantum computation by measurement and quantum memory*, Physics Letters A **308** (2003) 96–100 &lbrack;<a href="https://doi.org/10.1016/S0375-9601(02)01803-0">doi:10.1016/S0375-9601(02)01803-0</a>&rbrack;

* [[Debbie W. Leung]], *Quantum computation by measurements*,  International Journal of Quantum Information **02** 01 (2004) 33-43 &lbrack;[arXiv:quant-ph/0310189](https://arxiv.org/abs/quant-ph/0310189), [doi:10.1142/S0219749904000055](https://doi.org/10.1142/S0219749904000055)&rbrack;

Review:

* [[Hans J. Briegel]], [[Dan E. Browne]], [[Wolfgang Dür]], [[Robert Raussendorf]], [[Maarten Van den Nest]], *Measurement-based quantum computation*, Nature Physics **5** 1 (2009) 19-26 &lbrack;[arXiv:0910.1116](https://arxiv.org/abs/0910.1116), [doi:10.1038/nphys1157](https://doi.org/10.1038/nphys1157)&rbrack;

Using (motivating) the [[ZX-calculus]] for describing measurement-based quantum protocols

* [[Ross Duncan]], [[Simon Perdrix]], *Rewriting Measurement-Based Quantum Computations with Generalised Flow*, in: *Automata, Languages and Programming. ICALP 2010*, Lecture Notes in Computer Science **6199**, Springer (2010) &lbrack;[doi:10.1007/978-3-642-14162-1_24](https://doi.org/10.1007/978-3-642-14162-1_24)&rbrack;

    
