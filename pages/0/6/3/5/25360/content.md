
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

`QPMC` is a [[software verification]]-tool  for [[quantum programming languages]] (a "Quantum Protocol Model Checker").

## Related entries

* [[QWIRE]]

* [[Quipper]]

## References

Introducing `QPMC`:

* [[Yuan Feng]], Ernst Moritz Hahn, Andrea Turrini, Lijun Zhang, *`QPMC`: A Model Checker for Quantum Programs and Protocols*, in *Formal Methods. FM 2015*, Lecture Notes in Computer Science **9109**, Springer (2015)  &lbrack;[doi:10.1007/978-3-319-19249-9_17](https://doi.org/10.1007/978-3-319-19249-9_17)&rbrack;

  > "In practice, however, security analysis of [[quantum cryptography|quantum cryptographic]] protocols is notoriously difficult; for example, the manual proof of BB84 in &lbrack;15&rbrack; contains about 50 pages. It is hard to imagine such an analysis being carried out for more sophisticated quantum protocols. Thus, techniques for automated or semi-automated verification of these protocols will be indispensable."

Background and review:

* [[Mingsheng Ying]], Yuan Feng, *Model Checking Quantum Systems --- A Survey* &lbrack;[arXiv:1807.09466](https://arxiv.org/abs/1807.09466)&rbrack;

  > "But to check whether a quantum system satisfies a certain property at a time point, one has to perform a quantum. measurement on the system, which can change the state of the system. This makes studies of the long-term behaviours of quantum systems much harder than that of classical system."

  > "The state spaces of the classical systems that model-checking algorithms can be applied to are usually finite or countably infinite. However, the state spaces of quantum systems are inherently continuous even when they are finite-dimensional. In order to develop algorithms for model-checking quantum systems, we have to exploit some deep mathematical properties of the systems so that it suffices to examine only a finite number of (or at most countably infinitely many) representative elements, e.g. those in an orthonormal basis, of their state spaces."



On [[software verification|verification]] of [[Quipper]]-programs  with QPMC:

* Linda Anticoli, Carla Piazza, Leonardo Taglialegne, Paolo Zuliani, _Towards Quantum Programs Verification: From Quipper Circuits to QPMC_, In: Devitt S., Lanese I. (eds.) *Reversible Computation. RC 2016*, Lecture Notes in Computer Science **9720** Springer (2016) &lbrack;[arXiv:1708.06312](https://arxiv.org/abs/1708.06312), [doi:10.1007/978-3-319-40578-0_16](https://doi.org/10.1007/978-3-319-40578-0_16)&rbrack;

category: people

