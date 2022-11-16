

$$
  prepare(0) \;\colon\; \ast \xrightarrow{0} Bit \xrightarrow{ \eta^{\lozenge} } \lozenge_B \mathbb{1}
$$

\linebreak

$prepare \equiv return^\lozenge$

$measure \equiv extract^{\Box}$

\linebreak

$H \colon \lozenge(Bool \times \mathbb{C}) \to QBit$

$
  \begin{array}{ll}
    H(\psi) = & do  \; (b, q) \;\lt\; \psi 
    \\
    & 
    q
    \big(
      \vert 0 \rangle + (-1)^b \vert 1 \rangle
    \big)
  \end{array}
$

better wording:

$
  \begin{array}{ll}
    H(\psi) = & for  \; q\cdot \vert b \rangle \; in \; \psi 
    \\
    & 
    do
    \;
    q\cdot
    \big(
      \vert 0 \rangle + (-1)^b \vert 1 \rangle
    \big)
  \end{array}
$


\linebreak

$Alice 
  \;\colon\; 
  QBit \to 
  \lozenge
  \big(
    Bool \times Bool \times QBit
  \big)
$

$
\begin{array}{ll}
Alice(\psi) =  
& 
  prepare
  \Big(
  measure
  \Big(
  (\psi \otimes bell_1) 
  \;\gt\;
  CNOT
  \;\gt\;
  (H \otimes id)  
  \Big)
  , 
  bell_2
  \Big)
\\
& \text{where}\;\;\;
(bell_1 \otimes bell_2) \;=\; 
\big(prepare(0) \otimes\ prepare(0)\big)
    \gt \; ( H \otimes id )
    \gt \; CNOT    
\end{array}
$

\linebreak

$Bob \;\colon\; 
  \Bool \times Bool \times QBit 
  \to 
  \lozenge(\Bool \times \Bool \times \QBit)$

$Bob(b_1, b_2, q) 
  \;=\; 
  prepare
  \Big(b_1, b_2,  q \gt ZX(b_1, b_2) \Big)$

\linebreak

$teleport \;\colon\; QBit \to \lozenge(Bool \times Bool \times QBit) $

$teleport \;\;=\;\; Alice \gt\!\!\!\!\gt\!\!\!= Bob$

