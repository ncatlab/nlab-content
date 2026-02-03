> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak



***

### In practice

As of the 2020s, quantum error correction (QEC) on the available noisy ([NISQ](quantum+computation#ReferencesNISQ)) machines is the dominant paradigm strategy, both in academia and in industry, for achieving meaningful (commercial value) [[quantum computation]] in the future. 

More specifically, the dominant idea is to use [[surface codes]] for the encoding of logical qubits, on which [[Clifford gates]] are implemented natrively, and to use magic state resources in order to implement the remaining T-gates.

In technical discussions of aspects of this paradigm the nature of the end game of this approach can easily be missed. It is important to notice that, even in optimistic scenarios where suitable error thresholds can be achieved, the NISQ+QEC paradigm for future robust quantum computing aims at a staggering scenario of quantum/classical hardware engineering:

Namely the error correcting mechanism that will have to be carried out on a meaningful quantum computer which, say, implements [[Shor's algorithm]] for cracking RSA encryption, is going to involve a humongous rate of data processing that will require in excess of the classical computational power of contemporary building-sized supercomputers (cf. [Waintal 2024](#Waintal24)), which will need (cf. [riverlane](#Riverlane2026)) to exchange hundres of terabytes per second with the quantum device (reading error "syndrome" data form the quantum computer, processing this and then sending back error correction commands).

But at this rate of data any ordinary data cables between the quantum and the classical machine would be too slow (latency problem), and would anyways risk the transfer of too much heat from the outside world into the quantum machine operating at near absolute zero temperature.  Therefore one will need to somehow *integrate* the classical supercomputer into the colled quantum machine. But that runs into blatant thermodynamic constraints, since the heat produced by the classical computation will threaten then extremely cool state needed even for the noisy qubits.


* {#Waintal24} Xavier Waintal: *The Quantum House Of Cards*, PNAS **121** 1 (2024) e2313269120 \[<a href="https://doi.org/10.1073/pnas.2313269120">doi:10.1073/pnas.2313269120</a>, [arXiv:2312.17570](https://arxiv.org/abs/2312.17570)\]

* {#Riverlane2026} [riverlane](https://www.riverlane.com/): *[Quantum Error Correction](https://www.riverlane.com/quantum-error-correction)*

* Volkan Erol: *Quantum Computing is No Longer a Physics Problem. It is a Systems Engineering Nightmare* (Jan 2026)


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




