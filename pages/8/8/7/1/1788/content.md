

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***


\begin{imagefromfile}
    "file_name": "NYU-Physics-Research.png",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -30,

        "bottom": 20,
        "right": 0, 
        "left": 20
    }
\end{imagefromfile}


> **Abstract.** [[nLab:fractional quantum Hall system|Fractional quantum Hall systems]] (FQH) are a main contender for future [[nLab:quantum material|hardware]]-implementation of error-*protected* [[nLab:quantum registers]] (“[[nLab:topological order|topological]] [[nLab:qbits]]”) subject to error-protected [[nLab:quantum operations]] (“[[nLab:topological quantum computing|topological quantum gates]]”), both [plausibly necessary](/topological+quantum+computation#ReferencesNeedForTopologicalProtection) for future [[nLab:quantum computing]] at [useful scale](/nlab/show/quantum+computation#ReferencesNISQ), but both remaining insufficiently understood.

> One issue is that [[nLab:FQH system|FQH]] [[nLab:anyons]] [are](/nlab/show/quantum+Hall+effect#IntroAnyonicQuasiParticles) ([[nLab:vortices]] supported by) [[nLab:magnetic field|magnetic]] [[nLab:flux]] [[nLab:quanta]], while proper [[nLab:geometry of physics -- flux quantization|flux quantization]] in [[nLab:FQH systems]] has [remained problematic](https://arxiv.org/pdf/1510.07698#page=35). 

> This talk is to present a novel [[nLab:non-Lagrangian field theory|non-Lagrangian]] [[nLab:effective field theory|effective]] [[nLab:quantum field theory]] for [[nLab:FQH system|FQH]] [[nLab:anyons]] which is all based on proper [[nLab:geometry of physics -- flux quantization|flux quantization]], reducing the analysis of [[nLab:anyon|anyonic]] [[nLab:quantum physics|quantum]] [[nLab:quantum states|-states]], [[nLab:quantum observable|-observables]], and [[nLab:quantum measurement|-measurement channels]] to rigorous [[nLab:algebraic topology]].

> I will indicate how [[nLab:fractional statistics]] and [[nLab:topological order]] of [[nLab:FQH systems]] is (re-)derived while some predictions differ subtly from those of traditional [effective Chern-Simons theory](/nlab/show/abelian+Chern-Simons+theory#AbelianCSTheoryAsEffectiveQFTForFRactionalQuantumHall) --- which might be observable in experiment and might inform the search for topological quantum hardware.


\linebreak



Let $\mathbb{Z}^n_{\sum= [0]_k } \hookrightarrow \mathbb{Z}^n$ be the subgroup on those [[n-tuple|$n$-tuples]] of [[integers]] $(n_i)_{i = 1}^n$ whose [[sum]] is a multiple of $k \in \mathbb{Z}$, hence whose sum vanishes [[modulo]] $k$: $\sum_i n_i = 0 \,mod\, k$.

The [[cosets]] of this [[subgroup]] inclusion are clearly indexed by $C_k \equiv \mathbb{Z}/k$, and an element $(n_i)_{i=1}^k \,\in\,\mathbb{Z}^n$ belongs to the coset $r \,mod\, k$ if $\sum_i n_i = r \,mod\, k$. Hence we have a [[short exact sequence]] 

$$
  0 
    \to 
  \mathbb{Z}^n_{\sum = [0]_k}
    \longrightarrow
  \mathbb{Z}^n
    \xrightarrow{\sum \,\mathrm{mod}\, k}
  C_k
    \to 
  0
$$





(...)