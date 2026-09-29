> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.



***



## References

[[quantum metric]]

Original discussion:

* [[Jean-Pierre Provost]], [[Gérard Vallée]]: *Riemannian structure on manifolds of quantum states*, Commun. Math. Phys. **76** (1980) 289--301 &lbrack;[doi:10.1007/BF02193559](https://doi.org/10.1007/BF02193559), [euclid:cmp/1103908308](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-76/issue-3/Riemannian-structure-on-manifolds-of-quantum-states/cmp/1103908308.full)&rbrack; 

* [[William K. Wootters]]: *Statistical distance and Hilbert space*, Phys. Rev. D **23** (1981) 357 &lbrack;[doi:10.1103/PhysRevD.23.357](https://doi.org/10.1103/PhysRevD.23.357)&rbrack;

(...)

* [[Frédéric Piéchon]], Arnaud Raoux, [[Jean-Noël Fuchs]], Gilles Montambaux: *Geometric orbital susceptibility: quantum metric without Berry curvature*, Phys. Rev. B **94**  (2016) 134423 &lbrack;[doi:10.1103/PhysRevB.94.134423](https://doi.org/10.1103/PhysRevB.94.134423), [arXiv:1605.01258](https://arxiv.org/abs/1605.01258)&rbrack;
  > (for 2-band systems: (8) on [p. 2](https://arxiv.org/pdf/1605.01258#page=2))



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