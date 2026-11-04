

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", there is no harm in breaking the lock, as it is just caused by bot traffic. When the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\tableofcontents

## The 3Qbit code

### The classical case
 {#TheClassicalCase}

We regard [[bit]] values as elements of $\mathbb{Z}/2 = \{0,1\}$, the integers modulo 2. Their addition is the *exclusive or* (xor) of bits, denoted

$$
  0 \oplus 0 \,=\, 1 \oplus 1 \,=\, 0
  \,,
  \qquad
  0 \oplus 1 \,=\, 1 \oplus 0 \,=\, 1
  \,,
$$

so that $b \mapsto b \oplus 1$ is the flip of a bit $b$, while their multiplication is the logical *and*.

A bit stored or transmitted in a noisy medium may get flipped with some small probability $p$. The simplest remedy is redundancy: encode each *logical bit* by a triple of equal *physical bits*,

$$
  \array{
    \mathbb{Z}/2 &\longrightarrow& (\mathbb{Z}/2)^3
    \\
    b &\mapsto& (b,b,b) \,.
  }
$$

If at most one of the bits in $(b_1, b_2, b_3)$ gets flipped, its position is determined by the two parities

$$
  s_1 \;\coloneqq\; b_1 \oplus b_2
  \,,
  \qquad
  s_2 \;\coloneqq\; b_2 \oplus b_3
  \,,
$$

which vanish exactly on the codewords $(0,0,0)$ and $(1,1,1)$. This pair is the *error syndrome*:

$$
  \begin{aligned}
    (s_1, s_2) = (0,0) & \;\;\Leftrightarrow\;\; \text{no error}
    \\
    (s_1, s_2) = (1,0) & \;\;\Leftrightarrow\;\; \text{bit 1 flipped}
    \\
    (s_1, s_2) = (1,1) & \;\;\Leftrightarrow\;\; \text{bit 2 flipped}
    \\
    (s_1, s_2) = (0,1) & \;\;\Leftrightarrow\;\; \text{bit 3 flipped}
  \end{aligned}
$$

Flipping the indicated bit back (equivalently: taking the majority vote) recovers the logical bit. This fails only if two or more bits were flipped, which happens with probability $3p^2 - 2p^3 \lt p$ (for $p \lt 1/2$).

Here the syndrome is obtained in the most direct way: by reading out, hence by *measuring*, the three physical bits. Classically, this does no harm.

### The issue with the quantum case
 {#TheIssueWithTheQuantumCase}

Now the information to be protected is the state ${\vert \psi \rangle} = \alpha {\vert 0 \rangle} + \beta {\vert 1 \rangle}$ of a [[qbit]], hence the amplitudes $\alpha, \beta \in \mathbb{C}$. The classical encoding extends linearly to

$$
  {\vert \psi \rangle}
  \;\mapsto\;
  {\vert \psi_L \rangle}
  \;\coloneqq\;
  \alpha {\vert 000 \rangle} + \beta {\vert 111 \rangle}
  \,,
$$

implemented on ${\vert \psi \rangle} \otimes {\vert 00 \rangle}$ by two [[CNOT gate|CNOT gates]] (see [below](#TheProperQuantumCase)). This is a copying operation, namely of the computational basis states. The [[no-cloning theorem]] only rules out that copying be [[natural transformation|natural]] (in particular: independent of the choice of basis), which would instead send ${\vert \psi \rangle}$ to ${\vert \psi \rangle}^{\otimes 3}$.

A flip of the $i$th qbit now acts by the Pauli operator $X_i$ (with $X_0 \coloneqq 1$ for the error-free case), e.g.

$$
  X_2 {\vert \psi_L \rangle}
  \;=\;
  \alpha {\vert 010 \rangle} + \beta {\vert 101 \rangle}
  \,.
$$

Applying the classical strategy verbatim means measuring the three qbits in the computational basis. This does reveal the syndrome, but already the first measurement collapses the state onto one of its two branches (here ${\vert 010 \rangle}$ or ${\vert 101 \rangle}$, with probability ${\vert \alpha \vert}^2$ or ${\vert \beta \vert}^2$, respectively). The error is diagnosed, but the amplitudes $\alpha, \beta$ (the very data to be protected) are lost.

Notice, however, that the syndrome takes the same value on both branches (here $(s_1, s_2) = (1,1)$ for ${\vert 010 \rangle}$ as well as for ${\vert 101 \rangle}$). So each $X_i {\vert \psi_L \rangle}$ is a joint eigenstate of the parity observables $Z_1 Z_2$ and $Z_2 Z_3$, with eigenvalues $(-1)^{s_1}$ and $(-1)^{s_2}$. The individual bits must not be measured, but their parities may.

This motivates adjoining auxiliary *ancilla* qbits onto which the parities are imprinted by unitary gates. A [[quantum measurement]] of just the ancillas is then a measurement on the total system which reveals the syndrome without collapsing the encoded state.

### The proper quantum case
 {#TheProperQuantumCase}

Concretely, adjoin two ancilla qbits in state ${\vert 00 \rangle}$ and imprint on them the parities by four CNOT gates:

$$
  {\vert b_1 b_2 b_3 \rangle} \otimes {\vert 00 \rangle}
  \;\mapsto\;
  {\vert b_1 b_2 b_3 \rangle} \otimes {\vert b_1 \oplus b_2 ,\, b_2 \oplus b_3 \rangle}
  \,.
$$

Since the parities agree on both branches of $X_i {\vert \psi_L \rangle}$, this unitary maps

$$
  X_i {\vert \psi_L \rangle} \otimes {\vert 00 \rangle}
  \;\mapsto\;
  X_i {\vert \psi_L \rangle} \otimes {\vert s_1 s_2 \rangle}
  \,.
$$

This being a product state, measuring the ancillas yields the syndrome $(s_1, s_2)$ with certainty and leaves the code qbits in $X_i {\vert \psi_L \rangle}$, uncollapsed. Applying $X_i$ once more, with $i$ read off from the syndrome table [above](#TheClassicalCase), restores ${\vert \psi_L \rangle}$.

This is the *3-qbit bit flip code*. Its full circuit reads as follows: encoding, error (here on the second qbit), syndrome extraction, measurement, correction:

\begin{tikzcd}[row sep=small, column sep=small]
{\vert\psi\rangle} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[d,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[ddd,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X^{s_1 \bar s_2}} \arrow[r,dash] & {} \\
{\vert 0\rangle} \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X} \arrow[r,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & \bullet \arrow[r,dash]\arrow[ddd,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X^{s_1 s_2}} \arrow[r,dash]\arrow[u,equal] & {} \\
{\vert 0\rangle} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & {} \arrow[r,dash] & \boxed{X^{\bar s_1 s_2}} \arrow[r,dash]\arrow[u,equal] & {} \\
{\vert 0\rangle} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{\mathrm{meas}} \arrow[r,equal] & s_1 \arrow[u,equal] & \\
{\vert 0\rangle} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & \oplus \arrow[r,dash] & \boxed{\mathrm{meas}} \arrow[r,equal] & s_2 \arrow[u,equal] &
\end{tikzcd}

Here $\bar s \coloneqq 1 \oplus s$, the exponents are products in $\mathbb{Z}/2$, and $X^0 \coloneqq 1$, $X^1 \coloneqq X$. The final gates are classically controlled (double lines) by the measurement outcomes, so they flip exactly the qbit indicated by the syndrome.

### Refinements
 {#Refinements}

The bit flip code does not protect against *phase flips* $Z_i$ (acting by ${\vert 0 \rangle} \mapsto {\vert 0 \rangle}$, ${\vert 1 \rangle} \mapsto -{\vert 1 \rangle}$ on the $i$th qbit). These send ${\vert \psi_L \rangle}$ to $\alpha {\vert 000 \rangle} - \beta {\vert 111 \rangle}$, which is again a code state and hence has trivial syndrome: the error goes undetected and corrupts the logical state.

But since the Hadamard gate $H$ exchanges bit and phase flips, $H X H = Z$, the same scheme may be run in the Hadamard-transformed basis ${\vert {\pm} \rangle} \coloneqq \frac{1}{\sqrt{2}} \left( {\vert 0 \rangle} \pm {\vert 1 \rangle} \right)$. The encoding

$$
  {\vert 0 \rangle} \;\mapsto\; {\vert {+}{+}{+} \rangle}
  \,,
  \qquad
  {\vert 1 \rangle} \;\mapsto\; {\vert {-}{-}{-} \rangle}
$$

gives the *3-qbit phase flip code*, with syndrome given by the parity observables $X_1 X_2$ and $X_2 X_3$. It corrects any single phase flip, but now not bit flips.

Nesting the two codes, by encoding each of the three qbits of the phase flip code via the bit flip code, yields *Shor's 9-qbit code*:

$$
  {\vert 0 \rangle}
  \;\mapsto\;
  \frac{1}{2\sqrt{2}}
  \left( {\vert 000 \rangle} + {\vert 111 \rangle} \right)^{\otimes 3}
  \,,
  \qquad
  {\vert 1 \rangle}
  \;\mapsto\;
  \frac{1}{2\sqrt{2}}
  \left( {\vert 000 \rangle} - {\vert 111 \rangle} \right)^{\otimes 3}
  \,.
$$

This corrects bit flips, phase flips and their composites $X_i Z_i$ on any single qbit. In fact this suffices to correct *arbitrary* errors on a single qbit. Every operator on a qbit is a linear combination of $1$, $X$, $Z$ and $X Z$, and the syndrome measurement collapses such a superposition of errors onto one of its components, which is then corrected as before.

All of these are examples of *stabilizer codes*: the code space is the joint $(+1)$-eigenspace of a commuting set of products of Pauli operators (for the bit flip code: $Z_1 Z_2$ and $Z_2 Z_3$), whose measurement via ancillas yields the error syndrome.
