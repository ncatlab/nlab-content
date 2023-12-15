

Consider electromagnetism on $\mathbb{R}^{0,1} \times X$ for $X$ a [[Riemannian manifold]]. Then for $A = A_0 + A_X \in \Omega_{dR}^1(\mathbb{R}^{0,1} \times X)$ we have

$$
  \mathrm{d} A
  \;=\;
  \mathrm{d}t \wedge \dot A_X
  +
  \mathrm{d}_X A_0 
  +
  \mathrm{d}_X A_X
$$

and

$$
  \star \mathrm{d}A
  \;=\;
  \star_X \dot A_X
  +
  \star_X \mathrm{d}_X A_0
  +
  \star_X \mathrm{d}_X A_X \wedge \mathrm{d}T
$$

$$
  \begin{array}{l}
    \mathrm{d}A \wedge \star \mathrm{d}A
    \\
    \;=\;
    \big(
      \mathrm{d}t \wedge \dot A_X
      +
      \mathrm{d}_X A_X
    \big)
    \wedge
    \big(
      \star_X \dot A_X
      +
      \star_X \mathrm{d}_X A_X \wedge \mathrm{d}t
    \big)
    \\
    \;=\;
    \big(
      -
      \dot A_X \wedge \star_X \dot A_X
      +
      \mathrm{d}_X A_X \wedge \star_X \mathrm{d}_X A_X
     \big) \wedge \mathrm{d}t
  \end{array}
$$


$D^{\triangledown}$

```coq
CoInductive conat : Set :=
| cozero : conat
| cosuc : conat -> conat.

CoFixpoint omega: conat := cosucc omega.
```

\[
x = y \quad\text{Some text $X$ with math in it}
\]

\[
x = y \quad\hbox{Some text $X$ with math in it}
\]