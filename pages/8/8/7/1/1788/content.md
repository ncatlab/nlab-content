

$$
  \array{
    J 
    &\colon&
    Type 
    &\longrightarrow&
    LType
    \\
    &&
    X 
    &\mapsto&
    p_X^\ast \mathbb{1}
  }
$$

\begin{example}
**([[linear span]])**
\linebreak
For $\mathbb{K}$ any [[ground field]], consider:

1. $\mathbf{J} \coloneqq $ [[Set]];

1. $\mathbf{C} \coloneqq \int_{B \colon Set} Vect_B$ the category of [[indexed sets]] of [[vector spaces]] -- hence of [[vector bundles]] over [[sets]] (i.e. over [[discrete topological spaces]])

   $$
     \array{
       \mathscr{H}
       \\
       \big\downarrow
       \\
       B
     }
   $$


   with possibly base-changing vector bundle [[maps]] between them: 


   $$
     \array{
       \mathscr{H}
       &\longrightarrow&
       \mathscr{H}'
       \\
       \big\downarrow
       &&
       \big\downarrow
       \\
       B
       &\underset{f}{\longrightarrow}&
       B'
     }
   $$



1. the relativization functor given by sending a set to the [[trivial bundle|trivial]] [[tensor unit]]-bundle over it:

   \[
     \label{FormingTrivialTensorUnitBundle}
     \array{
       J 
       &\colon&
       Set
       &\longrightarrow&
       \int_{S \colon S} Vect_S
       \\
       &&
       B
       &\mapsto&
       B \times \mathbb{K}
     }
   \]

Notice that for each [[map]] $f \;\colon\; B \to B'$ of base sets, there is a [[base change]] [[adjoint triple]] of functors 

$$
  f_! \dashv f^\ast \dashv f_\ast
  \;\;\colon\;\;
  Vect_{B}
  \leftrightarrow
  Vect_{B'}
  \,.
$$

In particular, for $S' = \ast$ the [[terminal object|terminal]] [[singleton set]], the left base change along the unique $p_X \colon S \to \ast$ is the operation which forms the [[direct sum]] of the ([[fiber]]-)vector spaces in the bundle, and regards the resulting [[vector space]] as a bundle over the point:

$$
  (p_B)_! 
  \;\colon\;
  Vect_B 
    \longrightarrow 
  Vect_\ast \,=\, Vect
  \,.
$$

In view of this, we claim that the functor   

$$
  \array{
    Q
    &\colon&
    Set
    &\longrightarrow&
    \int_{B \colon Set} Vect_{B}
    \\
    &&
    S
    &\mapsto&
    (p_B)_!\big( B \times \mathbb{K} \big)
    \mathrlap{
      \;\simeq\;
      \underset{b \colon B}{\bigoplus} \mathbb{K}
    }
  }
$$

which may be understood as sending a [[set]] to its $\mathbb{K}$-[[linear span]],

carries the structure of a monad relative to the functor $J$ from (eq:FormingTrivialTensorUnitBundle) with

1. [[unit of a monad|unit]] given by

   $$
     \array{
       \eta_{B}
       &\colon&
       B \times \mathbb{K}
       &\longrightarrow&
       \underset{b \colon B}{\bigoplus} \mathbb{K}
       \\
       &&
       (b,k) &\mapsto& (k)_b
     }
   $$

1. [[extension system|Kleisli extension]] given by

   $$
     \Big(
       B \times \mathbb{K} 
         \xrightarrow{f}
       \underset{
         \mathclap{b' \colon B'}
       }{\oplus} \mathbb{K}
     \Big)
     \;\;\;\;\mapsto\;\;\;\;
     \Big(
       \underset{b \colon B}{\oplus} \mathbb{K}     
       \xrightarrow{
         \big( 
           f(b,-) 
         \big)_{b \colon B}
       }
       \underset{b' \colon B}{\oplus} \mathbb{K}     
     \Big)
   $$



\end{example}



$$
  \array{
    (p_X)^\ast \mathbb{1}  
    \to
    \mathscr{H}
    \\
    \hline
    \\
    (p_X)_! 
    (p_X)^\ast
    \mathbb{1}
    \to
    \mathscr{H}
  }
$$


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














