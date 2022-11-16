


$$
  prepare(0) \;\colon\; \ast \xrightarrow{0} Bit \xrightarrow{ \eta^{\lozenge} } \lozenge_B \mathbb{1}
$$

\linebreak


$prepare \equiv return^\lozenge$

$measure \equiv extract^{\Box}$

$save \equiv return^{\triangle}$

\linebreak

$$
  \text{for}\;
  (b_1, b_2, z)
  \;\text{measured in}\;
  (\psi \otimes bell_1)
  \;\text{>}\;
  CNOT
  \;\text{>}\;
  (H \otimes id)
  \;\text{do}\;
  z_{b_1, b_2}
$$

\linebreak

$$
  QBit 
  \xrightarrow{
    BellPrep \otimes  Qbit
  }
  QBit \otimes QBit \otimes QBit
  \xrightarrow{ QBit \otimes Alice }
  Qbit \otimes \bigcirc_{B \times B} \mathbb{C}
  \simeq
  \bigcirc_{B \times B} QBit
  \xrightarrow{ bind \; Bob }
  \bigcirc_{B \times B} QBit
$$

\linebreak

$
  Alice 
    \;\colon\; 
  QBit \otimes Qbit
    \to
  \bigcirc_{B \times B} \mathbb{C}
$

$
  Alice(\psi, bell_2)
  \;=\;
  parallelize(\psi, bell_2)
  \;\text\;
  (psi \otimes bell_2)
  \;\text{>}\;
  CNOT
  \;\text{>}\;
  (H \otimes  B)
$

\linebreak



\linebreak

$
  Alice 
  \;\colon\;
  QBit 
  \to
  \QBit 
  \to 
  \bigcirc_{B^2} \mathbb{C}
$

$$
  Alice(bell_1,\psi)
  \;=\;
  return (bee)
$$


$$
  Bob
  \;\colon\;
  \bigcirc_{B^2} QBit
  \to 
  \bigcirc_{B^2} QBit
$$

$$
  Bob( Data ) =
  \text{for}\;
  \psi \;\text{in}\; Data
  \;\text{do}\;
  \big(ZX(b_1, b_2)(\psi) \big)_{b_1, b_2}
$$




\linebreak

$H \colon \triangle(Bool \times \mathbb{C}) \to QBit$

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
  QBit \otimes QBit
    \to 
  \triangle
  \big(
    Bool \times Bool \times \mathbb{C}
  \big)
$

$
\begin{array}{ll}
Alice(bell_1, \psi) =  
  &\;
  \text{save}
  \big(
    (\psi \otimes bell_1) 
    \;\text{>}\;
    CNOT
    \;\text{>}\;
    (H \otimes id)  
    \;\text{>}\;
    measure
  \big)
  \end{array}
$

\linebreak


$Bob 
  \;\colon\; 
  \QBit
  \times
  \Bool
  \times
  \Bool
  \to 
  \QBit
  \times
  \Bool
  \times
  \Bool
$

$Bob(\phi)(b_1, b_2) 
  \;=\; 
  \Big(
    \phi \;\text{>}\; ZX(b_1, b_2)
    ,\,
    b_1, b_2,  
  \Big)
$

\linebreak

$teleport \;\colon\; QBit \to \triangle(Bool \times Bool \times QBit) $

$
\begin{array}{ll}
  teleport \;\;=
  & \text{for}\;\;\;
  (bell_1 \otimes bell_2) 
  \;\;\; \text{in} \;\;\; 
  \big(prepare(0) \otimes\ prepare(0)\big)
      \;\text{>}\; ( H \otimes id )
      \;\text{>}\; CNOT    
  \\
  &
  \text{do} \;\;\;
  Alice(bell_1) 
    \;\;\text{>}\;\;
  \triangle Bob(bell_2)
\end{array}
$


$
  verification
  \;\colon\;
  \underset{
    \array{
      \psi \colon QBit
    }
  }{\forall}
  \Big(
  teleport(\psi)
  =
  save
  \;
  parallelize_{Bool \times Bool}(\psi)
  \Big)
$

\linebreak

\linebreak


$
  Alice
  \;\colon\;
  QBit \otimes QBit
  \to 
  \bigcirc_{Bool^2} \mathbb{C}
$














