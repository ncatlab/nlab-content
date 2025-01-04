
The non-trivial [[irrep]] of the [[integer Heisenberg group]] [[group extension|extension]] $\mathbb{Z}_2 \hookrightarrow \widehat{\mathbb{Z}^2} \twoheadrightarrow \mathbb{Z}^2$ on is on 

$$
  \mathscr{H}_1
  \;\coloneqq\;
  \mathbb{C}\Big(
    \left\vert [n] \right\rangle
    \,\Big\vert\,
    [n] \in \mathbb{Z}_k
  \Big)
$$

given by

$$
  \begin{array}{ccl}
    W_a \, 
    \left\vert [n] \right\rangle
    &=&
    e^{2 \pi \mathrm{i} \tfrac{n}{k}}
    \left\vert [n] \right\rangle
    \\
    W_b \, 
    \left\vert [n] \right\rangle
    &=&
    \left\vert [n + 1] \right\rangle
    \\
    \zeta \,  
    \left\vert [n] \right\rangle
    &=&
    \exp(\pi \mathrm{i}\tfrac{1}{k})
    \left\vert [n] \right\rangle
  \end{array}
$$

Consider the group [[automorphism]] 

$$
  \begin{array}{ccl}
    \widehat{\mathbb{Z}^2}
    &\xrightarrow{ \; S \; }&
    \widehat{\mathbb{Z}^2}
    \\
    W_a &\mapsto& W_b^{-1}
    \\
    W_b &\mapsto& W_a
    \\
    \zeta &\mapsto& \zeta
  \end{array}
$$

We claim that this is compensated by the following linear map 
$$
  \begin{array}{ccl}
    \mathscr{H}_1
    &\xrightarrow{ S }&
    \mathscr{H}_1
    \\
    \left\vert [n] \right\rangle
    &\mapsto&
    \sum_{ [ \widehat{n} ] } 
    \exp\big( 
      2 \pi \mathrm{i}\tfrac{\widehat{n} n}{k}
    \big)
    \left\vert [\widehat{n}] \right\rangle
  \end{array}
$$

\begin{proof}
$$
  \begin{array}{ccl}
    S(W_a) S\big( \left\vert [n] \right\rangle \big)
    &=&
    W_b^{-1} 
    \sum_{[\widehat n]}
    \exp\big(2 \pi \mathrm{i} \tfrac{\widehat{n} n}{k}\big)
    \left\vert [\widehat n] \right\rangle \big)
    \\
    &=&
    \sum_{[\widehat n]}
    \exp\big(2 \pi \mathrm{i} \tfrac{\widehat{n} n}{k}\big)
    \left\vert [\widehat n - 1] \right\rangle \big)
    \\
    &=&
    \sum_{[\widehat n]}
    \exp\big(
      2 \pi \mathrm{i} \tfrac{(\widehat{n}+1) n}{k}
    \big)
    \left\vert [\widehat n] \right\rangle \big)
    \\
    &=&
    \exp\big(
      2 \pi \mathrm{i} \tfrac{n}{k}
    \big)
    \sum_{[\widehat n]}
    \exp\big(
      2 \pi \mathrm{i} \tfrac{\widehat{n} n}{k}
    \big)
    \left\vert [\widehat n] \right\rangle \big)
    \\
    &=&
    S\big(
      W_a \left\vert [n] \right\rangle
    \big)
  \end{array}
$$
and
$$
  \begin{array}{ccl}
    S(W_b)
    S\big( \left\vert [n] \right\rangle \big)
    &=&
    W_a
    \sum_{[\widehat n]}
    \exp\big(2 \pi \mathrm{i} \tfrac{\widehat{n} n}{k}\big)
    \left\vert [\widehat n] \right\rangle \big)
    \\
    &=&
    \sum_{[\widehat n]}
    \exp\big(2 \pi \mathrm{i} \tfrac{\widehat{n} (n+1)}{k}\big)
    \left\vert [\widehat n] \right\rangle \big)
    \\
    &=&
    S\big(
     \left\vert n+1 \right\rangle
    \big)
    \\
    &=&
    S\big(
      W_b\left\vert n \right\rangle
    \big)
  \end{array}
$$
\end{proof}


Similarly
$$
  \begin{array}{ccc}
    \widehat{ \mathbb{Z}^2 }
    &\xrightarrow{ T }&
    \widehat{ \mathbb{Z}^2 }
    \\
    W_a &\mapsto& W_a
    \\
    W_b &\mapsto& W_{a + b}
    \\
    \zeta &\mapsto& \zeta
  \end{array}
$$

is compensated by (?)

$$
  \begin{array}{ccc}
    \mathscr{H}_1
    &\xrightarrow{ T }& 
    \mathscr{H}_1
    \\
    \left\vert [n] \right\rangle
    &\mapsto&
    \exp( 2\pi \mathrm{i} \tfrac{n^2}{k})
    \left\vert [n] \right\rangle
  \end{array}
$$

\begin{proof}
$$
  \begin{array}{ccl}
    T(W_b)T\big( \left\vert [n] \right\rangle \big)
    &=&
    W_a W_b e^{-2\pi \mathrm{i}\tfrac{1}{k}}
    \exp( 2\pi \mathrm{i} \tfrac{n^2}{k} )
    \left\vert [n] \right\rangle
    \\
    &=&
    \exp\big( 2\pi \mathrm{i} 
      \tfrac{(n^2 + 2n + 1)}{k} \big)
    \left\vert [n+1] \right\rangle
    \\
    &=&
    \exp\big( 2\pi \mathrm{i} 
      \tfrac{(n+1)^2}{k} 
    \big)
    \left\vert [n+1] \right\rangle
    \\
    &=&
    \cdots
  \end{array}
$$
\end{proof}

(fix...)

$$
  \begin{array}{l}
    (1,0,0)\cdot(0,1,0) \cdot (-1,0,0) \cdot (0,-1,0)
    \\
    \;=\;
    (1,1,1) \cdot (-1,0,0) \cdot (0,-1,0)
    \\
    \;=\;
    (0,1,2) \cdot (0,-1,0)
    \\
    \;=\;
    (0,0,2)
  \end{array}
$$

$$
  \left[
  \begin{matrix}
   a & b
   \\
   c & d
  \end{matrix}
  \right]
$$


