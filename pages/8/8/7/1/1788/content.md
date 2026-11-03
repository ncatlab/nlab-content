

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", there is no harm in breaking the lock, as it is just caused by bot traffic. When the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\tableofcontents

## The 3Qbit code

### The classical case
 {#TheClassicalCase}

A [[bit]] $b \in \{0,1\}$ stored or transmitted in a noisy medium may get flipped, $b \mapsto b \oplus 1$, with some small probability $p$. The simplest remedy is redundancy: encode each *logical bit* by a triple of equal *physical bits*,

$$
  0 \;\mapsto\; 000
  \,,
  \qquad
  1 \;\mapsto\; 111
  \,.
$$

If at most one of the bits $b_1 b_2 b_3$ gets flipped, its position is determined by the two parities

$$
  s_1 \;\coloneqq\; b_1 \oplus b_2
  \,,
  \qquad
  s_2 \;\coloneqq\; b_2 \oplus b_3
  \,,
$$

which vanish on the codewords. This pair is the *error syndrome*:

$$
  \begin{aligned}
    (s_1, s_2) = (0,0) & \;\;\Rightarrow\;\; \text{no error}
    \\
    (s_1, s_2) = (1,0) & \;\;\Rightarrow\;\; \text{bit 1 flipped}
    \\
    (s_1, s_2) = (1,1) & \;\;\Rightarrow\;\; \text{bit 2 flipped}
    \\
    (s_1, s_2) = (0,1) & \;\;\Rightarrow\;\; \text{bit 3 flipped}
  \end{aligned}
$$

Flipping the indicated bit back (equivalently: taking the majority vote) recovers the logical bit. This fails only if two or more bits were flipped, which happens with probability $3p^2 - 2p^3 \lt p$ (for $p \lt 1/2$).

Here the syndrome is obtained in the most direct way: by reading out, hence by *measuring*, the three physical bits. Classically, this does no harm.

### The issue with the quantum case
 {#TheIssueWithTheQuantumCase}

Now the information to be protected is the state $\vert \psi \rangle = \alpha \vert 0 \rangle + \beta \vert 1 \rangle$ of a [[qbit]], hence the amplitudes $\alpha, \beta \in \mathbb{C}$. Copying $\vert\psi\rangle \mapsto \vert\psi\rangle^{\otimes 3}$ is ruled out by the [[no-cloning theorem]], but the *linear* extension of the classical encoding,

$$
  \vert \psi \rangle
  \;\mapsto\;
  \vert \psi_L \rangle
  \;\coloneqq\;
  \alpha \vert 000 \rangle + \beta \vert 111 \rangle
  \,,
$$

is fine: two [[CNOT gate|CNOT gates]] implement it on $\vert\psi\rangle \otimes \vert 00 \rangle$ (see [below](#TheProperQuantumCase)). A flip of the $i$th qbit now acts by the Pauli operator $X_i$ (with $X_0 \coloneqq 1$ for the error-free case), e.g.

$$
  X_2 \vert \psi_L \rangle
  \;=\;
  \alpha \vert 010 \rangle + \beta \vert 101 \rangle
  \,.
$$

Applying the classical strategy verbatim means measuring the three qbits in the computational basis. This does reveal the syndrome, but already the first measurement collapses the state onto one of its two branches (here $\vert 010\rangle$ or $\vert 101 \rangle$, with probability $\vert\alpha\vert^2$ or $\vert\beta\vert^2$, respectively). The error is diagnosed, but the amplitudes $\alpha, \beta$ (the very data to be protected) are lost.

Notice, however, that the syndrome takes the same value on both branches (here $(s_1, s_2) = (1,1)$ for $\vert 010\rangle$ as well as for $\vert 101\rangle$). So each $X_i \vert \psi_L\rangle$ is a joint eigenstate of the parity observables $Z_1 Z_2$ and $Z_2 Z_3$, with eigenvalues $(-1)^{s_1}$ and $(-1)^{s_2}$. The individual bits must not be measured, but their parities may.

This motivates adjoining auxiliary *ancilla* qbits onto which the parities are imprinted by unitary gates. A [[quantum measurement]] of just the ancillas is then a measurement on the total system which reveals the syndrome without collapsing the encoded state.

### The proper quantum case
 {#TheProperQuantumCase}

Concretely, adjoin two ancilla qbits in state $\vert 00 \rangle$ and imprint on them the parities by four CNOT gates:

$$
  \vert b_1 b_2 b_3 \rangle \otimes \vert 00 \rangle
  \;\longmapsto\;
  \vert b_1 b_2 b_3 \rangle \otimes \vert b_1 \oplus b_2 ,\, b_2 \oplus b_3 \rangle
  \,.
$$

Since the parities agree on both branches of $X_i \vert \psi_L \rangle$, this unitary maps

$$
  X_i \vert \psi_L \rangle \otimes \vert 00 \rangle
  \;\longmapsto\;
  X_i \vert \psi_L \rangle \otimes \vert s_1 s_2 \rangle
  \,.
$$

This being a product state, measuring the ancillas yields the syndrome $(s_1, s_2)$ with certainty and leaves the code qbits in $X_i \vert\psi_L\rangle$, uncollapsed. Applying $X_i$ once more, with $i$ read off from the syndrome table [above](#TheClassicalCase), restores $\vert \psi_L \rangle$.

This is the *3-qbit bit flip code*. Its full circuit reads as follows: encoding, error (here on the second qbit), syndrome extraction, measurement, correction:

\begin{tikzcd}[row sep=small, column sep=small]
\vert\psi\rangle \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[d,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[ddd,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X^{s_1 \bar s_2}} \arrow[r,dash] & {} \\
\vert 0\rangle \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X} \arrow[r,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & \bullet \arrow[r,dash]\arrow[ddd,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X^{s_1 s_2}} \arrow[r,dash]\arrow[u,equal] & {} \\
\vert 0\rangle \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & {} \arrow[r,dash] & \boxed{X^{\bar s_1 s_2}} \arrow[r,dash]\arrow[u,equal] & {} \\
\vert 0\rangle \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{\mathrm{meas}} \arrow[r,equal] & s_1 \arrow[u,equal] & \\
\vert 0\rangle \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & \oplus \arrow[r,dash] & \boxed{\mathrm{meas}} \arrow[r,equal] & s_2 \arrow[u,equal] &
\end{tikzcd}

Here $\bar s \coloneqq 1 \oplus s$, $X^0 \coloneqq 1$ and $X^1 \coloneqq X$. The final gates are classically controlled (double lines) by the measurement outcomes, so they flip exactly the qbit indicated by the syndrome.

The code protects only against single bit flips. Conjugating with Hadamard gates turns it into the analogous *phase flip code* (protecting against single $Z_i$-errors), and nesting the two yields Shor's 9-qbit code.



\linebreak

[hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism)

Quantum incrementers:

* *A Class of Efficient Quantum Incrementer Gates for Quantum Circuit Synthesis*, International Journal of Modern Physics B **28** 01 (2014) 1350191 \[<a href="https://doi.org/10.1142/S0217979213501919">doi:10.1142/S0217979213501919</a>\]

* Vivien Vandaele: *Asymptotically Optimal Quantum Circuits for Comparators and Incrementers* \[<a href="https://arxiv.org/abs/2603.12917">arXiv:2603.12917</a>\]
