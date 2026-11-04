

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", there is no harm in breaking the lock, as it is just caused by bot traffic. When the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\tableofcontents

## The 3Qbit code

### The classical case
 {#TheClassicalCase}

We regard [[bit]] values as elements of the [[cyclic group]] $\mathbb{Z}_{/2} = \{0,1\}$ of integers modulo 2. Their addition is the *exclusive or* (xor) of bits, denoted

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
    \mathbb{Z}_{/2} &\longrightarrow& (\mathbb{Z}_{/2})^3
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

Flipping the indicated bit back (equivalently: taking the majority vote) recovers the logical bit. This fails only if two or more of the bits were flipped. Assuming that the bits flip independently of each other, this happens with probability

$$
  \underset{
    \text{two flips}
  }{
  \underbrace{
    3 p^2 (1-p)
  }}
  \;+\;
  \underset{
    \text{three flips}
  }{
  \underbrace{
    p^3
  }}
  \;=\;
  3 p^2 - 2 p^3
  \,,
$$

where the factor of 3 counts the choices of the pair of flipped bits. Since $p - (3p^2 - 2p^3) = p(1-p)(1-2p)$, this is smaller than the error probability $p$ of an unprotected bit as long as $p \lt 1/2$.

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

A flip of the $i$th qbit now acts by the Pauli operator $X_i$, which is

$$
  X
  \;\coloneqq\;
  \left(
    \array{
      0 & 1
      \\
      1 & 0
    }
  \right)
  \,,
  \qquad
  X {\vert b \rangle} \,=\, {\vert b \oplus 1 \rangle}
$$

on the $i$th tensor factor and the identity on the others (with $X_0 \coloneqq 1$ for the error-free case). For example:

$$
  X_2 {\vert \psi_L \rangle}
  \;=\;
  \alpha {\vert 010 \rangle} + \beta {\vert 101 \rangle}
  \,.
$$

Applying the classical strategy verbatim means measuring the three qbits in the computational basis. This does reveal the syndrome, but already the first measurement collapses the state onto one of its two branches (here ${\vert 010 \rangle}$ or ${\vert 101 \rangle}$, with probability ${\vert \alpha \vert}^2$ or ${\vert \beta \vert}^2$, respectively). The error is diagnosed, but the amplitudes $\alpha, \beta$ (the very data to be protected) are lost.

Notice, however, that the syndrome takes the same value on both branches (here $(s_1, s_2) = (1,1)$ for ${\vert 010 \rangle}$ as well as for ${\vert 101 \rangle}$). In terms of the Pauli operator

$$
  Z
  \;\coloneqq\;
  \left(
    \array{
      1 & 0
      \\
      0 & -1
    }
  \right)
  \,,
  \qquad
  Z {\vert b \rangle} \,=\, (-1)^b {\vert b \rangle}
  \,,
$$

under which $Z_1 Z_2 {\vert b_1 b_2 b_3 \rangle} = (-1)^{b_1 \oplus b_2} {\vert b_1 b_2 b_3 \rangle}$ (and similarly for $Z_2 Z_3$), this means that each $X_i {\vert \psi_L \rangle}$ is a joint eigenstate of the parity observables $Z_1 Z_2$ and $Z_2 Z_3$, with eigenvalues $(-1)^{s_1}$ and $(-1)^{s_2}$. The individual bits must not be measured, but their parities may.

This motivates adjoining auxiliary *ancilla* qbits onto which the parities are imprinted by unitary gates. A [[quantum measurement]] of just the ancillas is then a measurement on the total system which reveals the syndrome without collapsing the encoded state.

### The proper quantum case
 {#TheProperQuantumCase}

Concretely, adjoin two ancilla qbits and consider the unitary operator

$$
  I
  \;\colon\;
  {\vert b_1 b_2 b_3 \rangle} \otimes {\vert a_1 a_2 \rangle}
  \;\mapsto\;
  {\vert b_1 b_2 b_3 \rangle} \otimes {\vert a_1 \oplus b_1 \oplus b_2 ,\, a_2 \oplus b_2 \oplus b_3 \rangle}
$$

(a permutation of the computational basis, implemented by four CNOT gates), which imprints the parities of the code qbits onto ancillas initialized in ${\vert 00 \rangle}$.

Suppose that the code state has suffered at most one bit flip, so that it is $X_i {\vert \psi_L \rangle}$ for some *unknown* $i \in \{0,1,2,3\}$. Since the parities agree on both branches of $X_i {\vert \psi_L \rangle}$, we have

$$
  I\left( X_i {\vert \psi_L \rangle} \otimes {\vert 00 \rangle} \right)
  \;=\;
  X_i {\vert \psi_L \rangle} \otimes {\vert s_1 s_2 \rangle}
  \,,
$$

where $(s_1, s_2)$ is the syndrome of the error $X_i$. Error correction now proceeds in three steps:

1. *Syndrome measurement:* Since the above is a product state, measuring only the ancillas yields the syndrome $(s_1, s_2)$ with certainty, and leaves the code qbits in $X_i {\vert \psi_L \rangle}$, uncollapsed.

1. *Decoding:* From the syndrome, a classical algorithm, the *decoder*, determines $i$ (here simply via the syndrome table [above](#TheClassicalCase)) and thereby *chooses* the correcting gate $X_i$.

1. *Correction:* Applying the chosen gate restores the code state: $X_i X_i {\vert \psi_L \rangle} = {\vert \psi_L \rangle}$, since $X X = 1$.

The decoder's choice involves the assumption of at most one bit flip: the syndrome $(1,1)$ of $X_2$ is also that of the double flip $X_1 X_3$. Choosing $X_2$ as the more likely of the two, the decoder turns the latter into the logical error $X_1 X_2 X_3 \colon {\vert \psi_L \rangle} \mapsto \alpha {\vert 111 \rangle} + \beta {\vert 000 \rangle}$. This is the quantum counterpart of the failure of the majority vote [above](#TheClassicalCase).

This is the *3-qbit bit flip code*. Its full circuit reads as follows: encoding, error (here on the second qbit), syndrome extraction by $I$, measurement, decoding and correction:

\begin{tikzcd}[row sep=small, column sep=small]
{\vert\psi\rangle} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[d,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[ddd,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X^{s_1 \bar s_2}} \arrow[r,dash] & {} \\
{\vert 0\rangle} \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X} \arrow[r,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & \bullet \arrow[r,dash]\arrow[ddd,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{X^{s_1 s_2}} \arrow[r,dash]\arrow[u,equal] & {} \\
{\vert 0\rangle} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \bullet \arrow[r,dash]\arrow[dd,dash] & {} \arrow[r,dash] & \boxed{X^{\bar s_1 s_2}} \arrow[r,dash]\arrow[u,equal] & {} \\
{\vert 0\rangle} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & \oplus \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \boxed{\mathrm{meas}} \arrow[r,equal] & s_1 \arrow[u,equal] & \\
{\vert 0\rangle} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & {} \arrow[r,dash] & \oplus \arrow[r,dash] & \oplus \arrow[r,dash] & \boxed{\mathrm{meas}} \arrow[r,equal] & s_2 \arrow[u,equal] &
\end{tikzcd}

Here $\bar s \coloneqq 1 \oplus s$, the exponents are products in $\mathbb{Z}_{/2}$, and $X^0 \coloneqq 1$, $X^1 \coloneqq X$. The final gates are classically controlled (double lines) by the measurement outcomes: they implement decoding and correction in one go, flipping exactly the qbit indicated by the syndrome.

### Refinements
 {#Refinements}

The bit flip code does not protect against *phase flips* $Z_i$. These send ${\vert \psi_L \rangle}$ to $\alpha {\vert 000 \rangle} - \beta {\vert 111 \rangle}$, which is again a code state and hence has trivial syndrome: the error goes undetected and corrupts the logical state.

But since the Hadamard gate

$$
  H
  \;\coloneqq\;
  \frac{1}{\sqrt{2}}
  \left(
    \array{
      1 & 1
      \\
      1 & -1
    }
  \right)
$$

exchanges bit and phase flips, $H X H = Z$, the same scheme may be run in the Hadamard-transformed basis ${\vert {\pm} \rangle} \coloneqq H {\vert 0/1 \rangle} = \frac{1}{\sqrt{2}} \left( {\vert 0 \rangle} \pm {\vert 1 \rangle} \right)$. The encoding

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