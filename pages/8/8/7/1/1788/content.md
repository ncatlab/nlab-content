> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak



***

### In practice

As of the 2020s, quantum error correction (QEC) applied to noisy intermediate-scale quantum ([NISQ](quantum+computation#ReferencesNISQ)) machines is the dominant paradigm in both academia and industry for achieving meaningful commercial value [[quantum computation]]. Specifically, the prevailing strategy utilizes [[surface codes]] for the encoding of logical qubits—upon which [[Clifford gates]] are implemented natively—supplemented by "magic state" resource distillation to implement the remaining universal [[T-gates]].

In technical discussions, the physical reality of the "endgame" of this approach may be easily missed: Even in optimistic scenarios where theoretical error thresholds are achieved, the NISQ+QEC roadmap requires envisioning a staggering future feat of quantum and classical hardware engineering, haunted by intrinsic design tensions.

Namely, the error-correcting mechanism required to run a useful, large-scale application—such as [[Shor's algorithm]] (e.g. for cracking RSA-2048 encryption) involves an astronomical rate of data processing. To maintain the logical quantum state, the auxiliary classical system must measure millions of physical qubits every microsecond, exchanging hundreds of terabytes of error "syndrome" data per second between the quantum device and its classical controller (cf. [Riverlane](#Riverlane2026)). This is a data rate of the order of the global internet traffic! Decoding this torrent of data in real-time requires an amount of classical computational power that exceeds the capabilities of contemporary, building-sized exascale supercomputers (cf. [Waintal 2024](#Waintal24)). 

Even if such classical computing power is or were available, standard data cables connecting the quantum chip to an external supercomputer would introduce signal latency exceeding the coherence time of current qubits, rendering the correction commands obsolete upon arrival. Furthermore, the sheer volume of data transfer will or would transmit enormous amounts of thermal noise from the outside world into the quantum machine, jeopardizing its near-zero cooling and its quantum coherence.

This problem is also known as the *decoding bottleneck*

To overcome this formidable scenario, the NISQ+QEC field has now turned to speculating on future classical hardware technology where Application Specific Integrated Circuit (ASICs) hardware is integrated directly into the ultra-cooled quantum refrigerator (e.g., via specialized "Cryo-CMOS" logic; cf. [Erol 2026](#Erol2026)).  However, this poses severe thermodynamic contradictions: Standard silicon transistors suffer from carrier freeze-out below $\sim 40K$, whence we need to envision an entire new kind of classical computing hardware. More generally, the cooling power at the base of a dilution refrigerator is strictly limited to a few micro-Watts. Therefore, placing a petaflop ASIC chip in near proximity to the quantum device would produce excess heat that under currently understood conditions would destroy the cryogenic environment that the quantum computer relies on.

In conclusion, the NISQ+QEC roadmap for achieving meaningful commercial value quantum computers is now tacitly banking on unheard of and intrinsically dubious future progress in *classical supercomputing* technology --- which, assuming it can be brought into existence, would then *not* be used for contentful computation itself, but would solely serve the task of preventing the memory of a quantum computer from decaying.



Of course, the initial problem at the base of this story is the instability of current qubit technology. The problem is akin to that of a bucket brigade which operates with extremely leaky buckets. In this picture, the QEC-style solution is like using ever more buckets together with sophisticated machinery that cleverly catches the leaked water only to fill it back into the buckets. 
This analogy makes clear that an alternative strategy may be to actually fix the buckets. On the quantum technology side this corresponds to the approach of [[topological quantum computing]] (cf. [Das Sarma 2022](#DasSarma22)), where it is not runtime software redundancy that stabilizes shaky qubits, but intrinsic physical effects in topological quantum hardware. However, while such topological stabilization of quantum states and topological protection of quantum gates exists in theory (and even that theory is not well developed at this point) essentially no experience with practical engineering implementation exists at this point. 


* {#Waintal24} Xavier Waintal: *The Quantum House Of Cards*, PNAS **121** 1 (2024) e2313269120 \[<a href="https://doi.org/10.1073/pnas.2313269120">doi:10.1073/pnas.2313269120</a>, [arXiv:2312.17570](https://arxiv.org/abs/2312.17570)\]

* {#Riverlane2026} [riverlane](https://www.riverlane.com/): *[Quantum Error Correction](https://www.riverlane.com/quantum-error-correction)*

* {#Erol2026} Volkan Erol: *Quantum Computing is No Longer a Physics Problem. It is a Systems Engineering Nightmare* (Jan 2026)

* {#DasSarma22} [[Sankar Das Sarma]]: *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)
  > "The qubit systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. \[...\] What is missing is the breakthrough \[...\] bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called topological quantum computing."


### FQH Excitation modes



On multiple modes resolving the would-be single GMP mode for [FQH excitations](quantum+Hall+effect#CollectiveExcitations) 

near filling fraction $\nu = 1/4$:

* Dung Xuan Nguyen, [[F. D. M. Haldane]], [[Edward H. Rezayi]], [[Dam Thanh Son]], Kun Yang: *Multiple Magnetorotons and Spectral Sum Rules in Fractional Quantum Hall Systems*, Phys. Rev. Lett. **128** (2022) 246402 \[<a href="https://doi.org/10.1103/PhysRevLett.128.246402">doi:10.1103/PhysRevLett.128.246402</a>, [arXiv:2111.10593](https://arxiv.org/abs/2111.10593), suppl:[pdf](https://journals.aps.org/prl/supplemental/10.1103/PhysRevLett.128.246402/Supp.pdf)\]

at [Jain filling fractions](quantum+Hall+effect#CompositeParticlePicture) $n/(2 p n \pm 1)$ with ${\vert n \vert}\geq 2$ (e.g. $\nu = 2/5, 3/7, 2/9, 2/7$):

* [[Ajit C. Balram]], Zhao Liu, [[Andrey Gromov]], [[Zlatko Papić]]: *Very-High-Energy Collective States of Partons in Fractional Quantum Hall Liquids*, Phys. Rev. X **12** (2022) 021008 \[<a href="https://doi.org/10.1103/PhysRevX.12.021008">doi:10.1103/PhysRevX.12.021008</a>, [arXiv:2111.10395](https://arxiv.org/abs/2111.10395)\]

at filling fractions $\nu  = n/(4 n \pm 1)$:

* [[Ajit C. Balram]], G. J. Sreejith, [[Jainendra K. Jain]]: *Splitting of Girvin-MacDonald-Platzman density wave and the nature of chiral gravitons in fractional quantum Hall effect*, Phys. Rev. Lett. **133** (2024) 246605 \[<a href="https://doi.org/10.1103/PhysRevLett.133.246605">doi:10.1103/PhysRevLett.133.246605</a>, [arXiv:2406.02730](https://arxiv.org/abs/2406.02730)\]

in FQH liquids that are not fully spin-polarized:

* Rakesh K. Dora, [[Ajit C. Balram]]: *Dispersion of collective modes in spinful fractional quantum Hall states on the sphere* \[<a href="https://arxiv.org/abs/2509.13100">arXiv:2509.13100</a>\] 


\begin{example}
In the category of [[schemes]] the subcategory of [[affine schemes]] is dense, see [[affine scheme#AffineSchemesFullSubcategoryOfOppositeOfRings|here]].
\end{example}

\begin{example}
In the category of [[smooth manifolds]], the full subcategory whose objects are given by $\mathbb{R}^n$ for $n\geq 1$ with the standard smooth structure, is dense.
\end{example}




