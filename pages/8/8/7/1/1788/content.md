

Consider $\mathfrak{g}$-[[Yang-Mills theory]] on a [[globally hyperbolic spacetime]] $\mathbb{R}^{0,1} \times X$ for $X$ a [[Riemannian manifold|Riemmannian]] [[2-manifold]]. Then for $A = A_0 + A_X \in \Omega_{dR}^1(\mathbb{R}^{0,1} \times X; \mathfrak{g}_P)$ we have

$$
  \begin{array}{l}
    L
    \;\coloneqq\;
    \tfrac{1}{2}
    \langle F, F \rangle
    \\
    \;=\;
    \tfrac{1}{2}
    \big\langle 
       \mathrm{d}A + \tfrac{1}{2}[A, A]
       ,\,
       \mathrm{d}A + \tfrac{1}{2}[A, A]
    \big\rangle
    \\
    \;=\;
    \big\langle
      \partial_0 A_\nu 
      ,\,
      F_{0 \nu}
    \big\rangle
    +
    \cdots
  \end{array}
$$

The [[canonical momentum]] is 

$$
  \pi_\mu
  \;\equiv\;
  \frac{\delta L}{
    \delta \partial_0 A_\mu 
  }
  \;=\;
  F_{0\mu}
$$

If we spatially Hodge-dualize the spatial component of the canonical momentum to

$$
  E \,\equiv\, \star_X \pi_X 
  \,\in\,
  \Omega^2_{dR}(X; \mathfrak{g}_P)
$$

Then the [[Gauss law]]-constraint

$$
  \pi_0 = 0
  ,\;\;\;
  [\pi_0, H] = 
$$



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