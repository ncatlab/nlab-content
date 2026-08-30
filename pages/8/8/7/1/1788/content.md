> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


[[complexity]]


***

**On the Derivation of K-Theory from M-Theory**

> In their optimistically titled article, DMW20 had presented a quantum and M-theoretic consistency check of the widely considered *Hypothesis K* --- that type IIA RR-flux is quantized in K-theory ---, by carefully matching, in a certain subsector, the resulting partition function in 10D to that of the shifted-integrally quantized C-field in 11D. This motivates asking for something closer to an actual derivation of *Hypothesis K* from M-theory by first making a more comprehensive hypothesis about the flux-quantization in 11D and then obtaining *Hypothesis K* as the systematic result of its dimensional reduction. Here we present an observation further in this direction: 

> We show that the recently discussed *Hypothesis H* (for *coHomotopy* cohomology theory) --- that C-field flux is quantized in (tangentially twisted) 4-Cohomotopy ---, together with a regularity condition on the circle-reduction, *implies* that IIA fluxes are quantized in a nonabelian deformation of twisted K-theory with the nonlinear Gauss law of the NS 7-flux taken into account.

> Mathematically, what we prove is (i) that the subspace of the cyclic loop space of $S^4$ on loops of low Dirichlet energy admits a universal comparison map to the classifying space for twisted K-theory over 10D, which on RR-fluxes is multiplication by 2, and (ii) that on the homotopy fiber of vanshing $D_6$ and $D_8$ charge (which corresponds to the subsector DMW20 considered) this may be divided by 2.

> Besides precisely stating this and related theorems, we explain the relation to flux quantization of 11D/10D supergravity. The proofs are non-trivial and are relegated to a companion article.

***

\begin{tikzcd}
	{(\mathbf{L}, \otimes, 1)} && {(\mathbf{M}, \times, \top)}
	\arrow["{!}", from=1-1, to=1-1, loop, in=145, out=215, distance=20mm]
	\arrow[""{name=0, anchor=center, inner sep=0}, "M"', shift right=2, from=1-1, to=1-3]
	\arrow[""{name=0p, anchor=center, inner sep=0}, phantom, from=1-1, to=1-3, start anchor=center, end anchor=center, shift right=2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "L"', shift right=2, from=1-3, to=1-1]
	\arrow[""{name=1p, anchor=center, inner sep=0}, phantom, from=1-3, to=1-1, start anchor=center, end anchor=center, shift right=2]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=1p, to=0p]
\end{tikzcd}

---


\begin{definition}
    \label{topological semantics}
    Let $T$ be a topological space closed under arbitrary intersections (i.e. an [[Alexandrov topology]], not to be confused with [[Alexandrov space]]), a topological interpretation (of _propositional_ subtractive logic) is a function $\llbracket \cdot \rrbracket$ from sentences to opens of $T$ satisfying:

$$
        \llbracket A \rrbracket = \begin{cases}
            T & \,\text{if}\, A = \top\\
            \emptyset & \,\text{if}\, A = \bot \\
            \llbracket B \rrbracket \cup \llbracket C \rrbracket & \,\text{if}\, A = B \wedge C \\
            \llbracket B \rrbracket \cap \llbracket C \rrbracket & \,\text{if}\, A = B \vee C \\
            \mathrm{Ext}(\llbracket B \rrbracket \setminus \llbracket C \rrbracket) & \,\text{if}\, A = B \implies C \\
            \mathrm{Int}(\llbracket B \rrbracket \setminus \llbracket C \rrbracket) & \,\text{if}\, A = B - C
        \end{cases}
    $$

and we say that $A \vdash B$ is _true_ for this interpretation if $\llbracket A \rrbracket \subseteq \llbracket B \rrbracket$
\end{definition}