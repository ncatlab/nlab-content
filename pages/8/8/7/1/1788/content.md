> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


[[complexity]]


***

**Prequantizing the C-field in IR-Completed 11D Supergravity**

**Abstract.** 
The traditional construction of (pre)symplectic phase spaces by variation of Lagrangian densities relies on gauge potentials and therefore applies globally only in the topologically trivial sector of (higher) gauge fields.
For IR-completions (via flux quantizations) of the C-field of 11D supergravity we instead determine the presymplectic and prequantum structure globally by analysis of the recently constructed phase space stack. We find that there is an essentially unique closed 2-form on the reduced phase space whose pullback to the phase space stack is the fiber integral over the Cauchy surface of a differential polynomial in the bicomplex components of the C-field flux densities. This turns out to have a unique potential of the same nature, and to coincide on topologically trivial fields with the traditional symplectic form on the C-field sector of 11D SuGra. Hence it generalizes the latter to IR-completions, where its potential moreover exhibits a prequantization --- a prerequisite for (geometric) quantization.

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