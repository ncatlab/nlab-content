
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


# Grothendieck inequality
* table of contents
{: toc}

## Statement

Let $B$ be the [[unit ball]] of a [[separable space|separable]] [[Hilbert space]] over the [[real number|real]] or [[complex numbers]]. Then the [[inner product|scalar product]], $\langle\cdot,\cdot\rangle : B \times B \to \mathbb{C}$ has the following special property:

+-- {: .num_theorem}
###### Theorem

There exist [[infinite sequence|sequences]] $f_n,g_n: B \to \mathbb{C}$ of [[norm topology|norm]]-[[continuous functions]], such that

* $\langle x, y \rangle = \sum_n f_n(x) g_n(y)$ for all $x, y \in B$

* $\sum_n \, \sup_B \left| f_n \right| \, \sup_B \left| g_n \right| \, &lt; \, \infty$
=--

In other words, $\langle\cdot,\cdot\rangle$, as a [[function of two variables]], is an element of the [[projective tensor product]] $C(B) {\displaystyle\hat{\otimes}} C(B)$. Its [[projective tensor norm]] is known as __Grothendieck's constant__. The precise value of this constant is different in the real and complex case, and neither one is known exactly.


## Related concepts

* [[inequality]]

* [[Cauchy-Schwarz inequality]]

* [[Bell's inequality]]

## References

### General

Due to:

* [[Alexander Grothendieck]], *Résumé des résultats essentiels dans la théorie des produits tensoriels topologiques et des espaces nucléaires*, Annales de l'Institut Fourier, **4** (1952) 73-112 &lbrack;[numdam:AIF_1952__4__73_0](http://www.numdam.org/item/?id=AIF_1952__4__73_0)&rbrack;

Review:

* Leqi Zhu, *Grothendieck's inequality* (2018) &lbrack;[pdf](http://www.cs.toronto.edu/~toni/Courses/Proofs-SOS-2018/Lectures/grothendieck.pdf)&rbrack;

* Ron Blei, _Analysis in integer and fractional dimensions_, Cambridge University Press (2009) &lbrack;[doi:10.1017/CBO9780511543012](https://doi.org/10.1017/CBO9780511543012)&rbrack;

See also:

* Wikipedia, *[Grothendieck inequality](https://en.m.wikipedia.org/wiki/Grothendieck_inequality)*

### In quantum physics
 {#ReferencesInQuantumPhysics}

Discussion of Grothendieck's inequality in [[quantum physics]], in relation to [[Bell's inequality]], originates with:

* [[Boris S. Tsirelson]], *Quantum analogues of the Bell inequalities. The case of two spatially separated domains*, Journal of Soviet Mathematics **36** (1987) 557–570 &lbrack;[doi:10.1007/BF01663472](https://doi.org/10.1007/BF01663472)&rbrack;

reviewed in

* [[Boris S. Tsirelson]], *Some results and problems on quantum Bell-type inequalities* Hadronic Journal Supplement **8** 4 (1993) 329-345 &lbrack;[pdf](https://www.tau.ac.il/~tsirel/download/hadron.pdf), [[Tsirelson-QuantumBellType.pdf:file]] [web](https://www.tau.ac.il/~tsirel/download/hadron.html)&rbrack;

  > (but see the erratum [here](https://www.tau.ac.il/~tsirel/Research/bellopalg/main.html))

* Wikipedia, *[Tsirelson's bound](https://en.wikipedia.org/wiki/Tsirelson%27s_bound)*

 

Further discussion:

* Antonio Acín, Nicolas Gisin, and Benjamin Toner, *Grothendieck’s constant and local models for noisy entangled quantum states*, Phys. Rev. A **73** (2006) 062105 &lbrack;[doi:10.1103/PhysRevA.73.062105](https://doi.org/10.1103/PhysRevA.73.062105), [arXiv:quant-ph/0606138](https://arxiv.org/abs/quant-ph/0606138)&rbrack;

* Hoshang Heydari, *Quantum Violation: Beyond Clauser-Horne-Shimony-Holt Inequality*, J. Phys. A: Math. Gen. **39** (2006) 11869-11875 &lbrack;[arXiv:quant-ph/0603050](https://arxiv.org/abs/quant-ph/0603050), [doi:10.1088/0305-4470/39/38/012](https://iopscience.iop.org/article/10.1088/0305-4470/39/38/012)&rbrack;

* Jop Briët, Harry Buhrman & Ben Toner, *A Generalized Grothendieck Inequality and Nonlocal Correlations that Require High Entanglement*, Comm. Math. Phys. **305** (2011) 827–843 &lbrack;[doi:10.1007/s00220-011-1280-3](https://doi.org/10.1007/s00220-011-1280-3)&rbrack;

* Flavien Hirsch, Marco Túlio Quintino, Tamás Vértesi, Miguel Navascués, Nicolas Brunner, Quantum **1** (2017) 3 *Better local hidden variable models for two-qubit Werner states and an upper bound on the Grothendieck constant $K_G(3)$* &lbrack;[doi:10.22331/q-2017-04-25-3](https://doi.org/10.22331/q-2017-04-25-3), [arXiv:1609.06114](https://arxiv.org/abs/1609.06114)&rbrack;

* A. Vourdas, *Grothendieck bound in a single quantum system*, J. Phys. A: Math. Theor. **55** (2022) 435206 &lbrack;[arXiv:2212.11663](https://arxiv.org/abs/2212.11663), [doi:10.1088/1751-8121/ac9dcf](https://iopscience.iop.org/article/10.1088/1751-8121/ac9dcf)&rbrack;



[[!redirects Grothendieck inequality]]
[[!redirects Grothendieck's inequality]]


[[!redirects Grothendieck constant]]
[[!redirects Grothendieck's constant]]
[[!redirects Grothendieck's constant]]
[[!redirects Grothendieck\'s constant]]
