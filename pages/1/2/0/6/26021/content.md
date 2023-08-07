
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

As described in ['t Hooft (1980)](#tHooft1980), a [[global symmetry]] of a [[quantum field theory]] is said to have a **'t Hooft anomaly** if it is non-anomalous as a global symmetry but has a [[quantum anomaly]] if one attempts to turn it into a [[gauge symmetry]].

Informally, a global symmetry described by the [[action]] of a [[group]] $G$ may be "coupled" to a [[gauge potential]] $A$ (a [[connection on a bundle]]). Denoting the [[partition function]] coupled to such a connection as $Z(A)$, the partition function of the gauged theory is, modulo normalization factors, $Z=\sum_A Z(A).$ If the symmetry has a 't Hooft anomaly, then perfoming a [[gauge transformation]] on all connections results in a nontrivial phase multiplying each partition function $Z_g=\sum_A \phi(A,g) Z(g\cdot A)$ where each phase $\phi(A,g)$ depends on the particular background field and gauge transformation, so that generally $Z\neq Z_g$. This is problematic since the partition function is supposed to be gauge invariant.

For $G$ a [[finite group]], and when the $n$-dimensional spacetime $\Sigma$ is the boundary of an $(n+1)$-dimensional space $X$, this situation may be remedied by "coupling" the $n$-dimensional theory with symmetry $G$ to a $(n+1)$-dimensional [[topological quantum field theory]] (a [[Dijkgraaf-Witten theory]] classified by $H^{n+1}(G,U(1))$) on $X$ such that the phase contributions of a gauge transformation of both cancel each other. This is known as *anomaly inflow* (see e.g. [Freed, Hopkins, Lurie, and Teleman (2009)](#FHLT09) and [Freed (2014)](#Freed14)).

Any [[generalized global symmetry]] is also thought to potentially exhibit 't Hooft anomalies described by a TQFT. In the literature, this is referred to as the *Anomaly TFT*, an [[invertible field theory]] (cf. [Freed 2014](#Freed14)), but little is known about what this TQFT is supposed to be for cases not equivalent to group-like cases (for which the TQFT is DW).


## References
 {#References}

* {#tHooft1980} [[Gerard 't Hooft]], *Naturalness, Chiral Symmetry, and Spontaneous Chiral Symmetry Breaking* In: G. 'Hooft et al., *Recent Developments in Gauge Theories*, NATO Advanced Study Institutes Series **59**, Springer (1980) &lbrack;[doi:10.1007/978-1-4684-7571-5_9](https://doi.org/10.1007/978-1-4684-7571-5_9)&rbrack;

* {#FHLT09} [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], *[[Topological Quantum Field Theories from Compact Lie Groups]]*, in P. R. Kotiuga (ed.) *A celebration of the mathematical legacy of Raoul Bott* AMS (2010) &lbrack;[arXiv:0905.0731](https://arxiv.org/abs/0905.0731), [ISBN:978-0-8218-4777-0](https://bookstore.ams.org/view?ProductCode=CRMP/50)&rbrack;

* {#Freed14} [[Daniel Freed]]. *Anomalies and Invertible Field Theories*, talk at [StringMath2013](http://scgp.stonybrook.edu/events/event-pages/string-math-2013) &lbrack;[arXiv:1404.7224](https://arxiv.org/abs/1404.7224)&rbrack;

[[!redirects 't Hooft anomalies]]
