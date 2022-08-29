
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In as far as a [[computation]] is a [[function]] from input data to output result, a *reversible computation* is an [[invertible]] function, where the input may be recovered from knowledge of the output.
More generally, as far as a [[computation]] is any [[morphism]] (under the [[computational trilogy]]), a reversible computation is an *[[isomorphism]]*.



Typical operations of a [[classical computer]] are not reversible: For example standard logical gates such as [[AND]], [[XOR]] etc. are [[functions]] of the form $\{0,1\}^2 \longrightarrow \{0,1\}$ and as such not [[invertible]]. Standard classical gates which are invertible include the [[NOT]]-gate $\{0,1\} \xrightarrow{\sim} \{0,1\}$ (which switches its single input bit) and the [[CNOT]]-gate $\{0,1\}^2 \xrightarrow{\sim} \{0,1\}^2$ (which keeps the first "control" bit and switches the second bit if the first equals 1). 

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/LeibnizMachineReversible.jpg" width="550">
</div>

{#ExampleOfIncrementalAddition} Using just these reversible NOT- and CNOT-gates one may for instance implement the operation of *incremental [[addition]]* $(-)+n \;\colon\; \mathbb{Z} \xrightarrow{\sim} \mathbb{Z}$ by a fixed [[natural number]] $n$ (e.g. [Kaye 2004](#Kaye04)). As opposed to binary addition $(-) + (-) \,\colon\, \mathbb{Z}^2 \xrightarrow{\;} \mathbb{Z}$, this operation is invertible, the [[inverse]] being the corresponding incremental [[subtraction]] $(-)-n \;\colon\; \mathbb{Z} \xrightarrow{\sim} \mathbb{Z}$. 


This state of affairs was reflected, for instance, in [[Gottfried Leibniz]]'s *[stepped reckoner](https://en.wikipedia.org/wiki/Stepped_reckoner)* machine, which performs incremental addition when its crank is turned in one direction, and the inverse incremental subtraction when the crank is turned back in the opposite direction.

\linebreak

But the NOT- and CNOT-gates by themselves are not universal.
On the other hand, the [[CCNOT]] gate $\{0,1\}^3 \xrightarrow{\sim} \{0,1\}^3$ (which regards the first two inputs as control bits and switches the third input if these two are both 1) is both invertible as well as universal (e.g. [Nielsen & Chuang 2000, §1.4.1](#NielsenChuang00)), in that any function of the form $\{0,1\}^{n_1} \xrightarrow{\;} \{0,1\}^{n_2}$ is equal to a circuit of CCNOT gates pre-composed with some cartesian power of $\{0\} \xhookrightarrow{\;} \{0,1\}$ (introducing auxiliary "bath" or "ancilla" bits) and post-composed with some cartesian power of $\{0,1\} \to \ast$ (deleting auxiliary bits). In other words: Every irreversible classical computation on some computing system may be understood as a reversible computation on the system coupled to an ambient "bath" together with a loss of information of computation output into this bath.

Indeed, in terms of [[physics|physical]] implementation of computation, the distinction between reversible and irreversible computation is essentially that of reversible or irreversible dynamical processes as known from [[thermodynamics]]: Fundamentally and under idealized conditions, physical processes are invertible, but "at finite temperature" there is [[entropy]]-increase associated with most processes, making them irreversible. This relation between (non-)reversible computation and [[thermodynamics]] is known as *Landauer's principle* (due to [Landauer 1961](#Landauer61), review e.g. in [Nielsen & Chuang 2000, §3.2.5](#NielsenChuang00)).

While the notion of reversible computation was originally conceived in the context of classical computation, more recently its key example is understood to be *[[quantum computation]]*: Here the logical gates (*ex*cluding the final [[quantum measurement]] which [[wave function collapse|collapses]] the [[quantum state]]) are [[linear functions]] which are [[unitary operator]] and hence necessarily [[invertible]] (see [Frank 2003](#Frank03) for emphasis).

Therefore, the practical problem of implementing quantum computation faces analogous [[thermodynamics|thermodynamical]] issues as embodied by Landauer's principle, which are the reason for the need of [[quantum error correction]] and/or [[topological quantum computation|topological quantum stabilization]].




## References

Original articles:

* {#Landauer61} [[Rolf Landauer]], *Irreversibility and Heat Generation in the Computing Process*,  IBM Journal of Research and Development **5** 3 (1961) 183–191 &lbrack;[doi:10.1147%2Frd.53.0183](https://doi.org/10.1147%2Frd.53.0183)&rbrack; 

* [[Charles H. Bennett]], *Logical Reversibility of Computation*, IBM Journal of Research and Development  **17** 6  (1973) &lbrack;[doi:10.1147/rd.176.0525](https://doi.org/10.1147/rd.176.0525)&rbrack;

Review:

* [[Charles H. Bennett]], *The thermodynamics of computation -- a review*, International Journal of Theoretical Physics **21** (1982) 905–940 &lbrack;[doi:10.1007/BF02084158](https://doi.org/10.1007/BF02084158)&rbrack;

* [[Rolf Landauer]], [[Charles H. Bennett]]: *[The Fundamental Physical Limits of Computation](https://www.scientificamerican.com/article/the-fundamental-physical-limits-of-computation/)*, Scientific American **253** 1 (1985)

* [[Rolf Landauer]]: *Computation: A Fundamental Physical View*, Phys. Scr. **35** (1987) 88 &lbrack;[doi:10.1088/0031-8949/35/1/021](https://iopscience.iop.org/article/10.1088/0031-8949/35/1/021)&rbrack;

* [[Charles H. Bennett]], *Notes on the history of reversible computation*,  IBM Journal of Research and Development *32* 1 (1988) &lbrack;[doi:10.1147/rd.321.0016](https://doi.org/10.1147/rd.321.0016)&rbrack;

* [[Charles H. Bennett]], *Notes on Landauer's principle, reversible computation, and Maxwell's Demon*, Studies in History and Philosophy of Science Part B: Studies in History and Philosophy of Modern Physics, **34** 3 (2003) 501-510 (<a href="https://doi.org/10.1016/S1355-2198(03)00039-X">doi:10.1016/S1355-2198(03)00039-X</a>)

See also:

* Wikipedia, *[Reversible computing](https://en.wikipedia.org/wiki/Reversible_computing)*

* Wikipedia, *[Landauer's principle](https://en.wikipedia.org/wiki/Landauer%27s_principle)*

Discussion of reversible computation in view of [[quantum computation]]:

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], §1.4.1 and §3.2.5 in: *Quantum computation and quantum information*, Cambridge University Press (2000) $[$[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]$]$

* {#Frank03} [[Michael P. Frank]], *Reversible Computing -- Quantum Computing’s Practical Cousin*, Simons Conference Lecture, Stony Brook (2003) &lbrack;[pdf](http://insti.physics.sunysb.edu/conf/simons-qcomputation/talks/frank.pdf), [[Frank-ReversibleComputing.pdf:file]]&rbrack;

* {#Kaye04} [[Phillip Kaye]], *Reversible addition circuit using one ancillary bit with application to quantum computing* &lbrack;[quant-ph/0408173](https://arxiv.org/abs/quant-ph/0408173)&rbrack;

* [[Phillip Kaye]], [[Raymond Laflamme]], [[Michele Mosca]], §1.5 in: *An Introduction to Quantum Computing*, Oxford University Press (2007) &lbrack;[pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149125645.pdf), [ISBN:9780198570493](https://global.oup.com/academic/product/an-introduction-to-quantum-computing-9780198570493?cc=at&lang=en&)&rbrack;
 

* [[Michael P. Frank]], Karpur Shukla, *Quantum Foundations of Classical Reversible Computing*, Entropy **23** 6 (2021) 701  &lbrack;[arXiv:2105.00065](https://arxiv.org/abs/2105.00065), [doi:10.3390/e23060701](https://doi.org/10.3390/e23060701)&rbrack;




[[!redirects reversible computations]]

[[!redirects reversible computing]]

[[!redirects Landauer's principle]]
[[!redirects Landauer principle]]


