
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


\tableofcontents


## Idea

In the theory of *[[computation]]*, a *threshold theorem* (short for *error threshold*) states that when the error-rates of realistic [[logic gate]]-components are below a given threshold, then [[error correction]] can achieve an arbitrarily error-free computation.

For classical computation, where an early version of this statement is due to [von Neumman 1956](#vonNeumman56), the reality of virtually error-free (digitial) computing machines has become commonplace and threshold theorems are rarely discussed anymore these days. 

This situation is different for [[quantum computing]], where threshold theorems (proven by [Knill, Laflamme & Zurek 1998](#KnillLaflammeZurek98)) and [Aharonov and Ben-Or 2008](#AharonovBen-Or08) are the basis for ongoing hopes that [[quantum error correction]] technology can achieve scalable useful [[quantum computers]] even with near-term available noisy [[qbits]] and noisy [[quantum logic gates]] (cf. *[NISQ](quantum+computation#ReferencesNISQ)*).


## References

### For classical computing

* {#vonNeumman56} [[John von Neumann]] (notes by R. S. Pierce): *Probabilistic Logics and the Synthesis of Reliable Organisms From Unreliable Components*, in: *Automata Studies*, Princeton University Press (1956) 329-378 &lbrack;[doi;10.1515/9781400882618-003](https://doi.org/10.1515/9781400882618-003), [pdf](https://personalpages.manchester.ac.uk/staff/nikolaos.kyparissas/uploads/VonNeumann1956.pdf), [pdf](https://static.ias.edu/pitp/archive/2012files/Probabilistic_Logics.pdf)&rbrack;


### For quantum comuting

> For more see [here](quantum+error+correction#FeasabilityReferences) at *[[quantum error correction]]*.

Original proofs of threshold theorems for various error-models in [[quantum computing]]:

* {#KnillLaflammeZurek98} [[Emanuel Knill]], [[Raymond Laflamme]], [[Wojciech Zurek]]: *Resilient Quantum Computation: Error Models and Thresholds*, Science **279** 5349 (1998) 342-345 &lbrack;[doi;10.1126/science.279.5349.342](https://doi.org/10.1126/science.279.5349.342), [arXiv:quant-ph/9702058](https://arxiv.org/abs/quant-ph/9702058)&rbrack;

* {#AharonovBen-Or08} [[Dorit Aharonov]], [[Michael Ben-Or]]: *Fault-Tolerant Quantum Computation with Constant Error Rate*, SIAM Journal on Computing **38** 4 (2008) &lbrack;[doi:10.1137/S0097539799359385](https://doi.org/10.1137/S0097539799359385), [arXiv:quant-ph/9906129](https://arxiv.org/abs/quant-ph/9906129)&rbrack;

following

* [[Peter Shor]]: *Fault-tolerant quantum computation*, Proceedings of 37th Conference on Foundations of Computer Science (1996) 56-65 &lbrack;[doi:10.1109/SFCS.1996.548464](https://doi.org/10.1109/SFCS.1996.548464)&rbrack;

Review:

* [[Daniel Gottesman]], §5 in: *An Introduction to Quantum Error Correction and Fault-Tolerant Quantum Computation*, in: *Quantum Information Science and Its Contributions to Mathematics*, Proceedings of Symposia in Applied Mathematics **68** (2010) &lbrack;[arXiv:0904.2557](https://arxiv.org/abs/0904.2557), [doi:10.1090/psapm/068 ](https://doi.org/10.1090/psapm/068)&rbrack;


Lecture notes:

* [[Seth Lloyd]]: *Fault Tolerant Quantum Computing*, Lecture 14 in *Quantum Computing (CST Part II)* &lbrack;[pdf](https://www.cl.cam.ac.uk/teaching/1920/QuantComp/Quantum_Computing_Lecture_14.pdf)&rbrack;

See also: 

* Wikipedia: *[Threshold theorem](https://en.wikipedia.org/wiki/Threshold_theorem)*


[[!redirects error threshold theorems]]

[[!redirects threshold theorem]]
[[!redirects threshold theorems]]


