

\begin{example}
The [[bit-flip quantum channel]] for flip-[[probability]] $p \,\colon\, [0,1]$
$$
  \begin{aligned}
    flip
    &\colon\;
    States(QBit)
    \longrightarrow
    States(QBit)
    \\
    flip(\rho) 
    &\equiv\;
    (1-p) \, \rho \,+\, p \cdot (X \cdot \rho \cdot X)
  \end{aligned}
$$
(where $X$ denotes the corresponding [[Pauli gate]])
is exhibited as a [[unistochastic quantum channel]] by taking another [[QBit]] as the environment and considering the following [[unitary operator]] on the coupled system of two [[qbits]]:


$$
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & 1
    \\
    -1 & 1
  }
  \right]
  \cdot
  \left[
  \array{
    0 & 1
    \\
    1 & 0
  }
  \right]
  \cdot
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & -1
    \\
    1 & 1
  }
  \right]
$$

$$
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & 1
    \\
    -1 & 1
  }
  \right]
  \cdot
  \left(
  (1-\rho)
  \,
  \left[
  \array{
    1 & 0 
    \\
    0 & 1
  }
  \right]
  \;+\;
  \rho
  \,
  \left[
  \array{
    0 & 1 
    \\
    1 & 0
  }
  \right]
  \,
  \right)
  \cdot
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & -1
    \\
    1 & 1
  }
  \right]
  \;=\;
  \left(
  (1-\rho)
  \,
  \left[
  \array{
    1 & 0 
    \\
    0 & 1
  }
  \right]
  \;+\;
  \rho
  \,
  \left[
  \array{
    1 & 0 
    \\
    0 & -1
  }
  \right]
  \,
  \right)
$$


\end{example}