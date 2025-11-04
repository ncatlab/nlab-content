> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***

\begin{example}
  The canonical [[real structure]] on $\mathbb{C}$
  $$
    \begin{array}{ccc}
      \mathbb{C} 
        &\xrightarrow{\; \widehat{T} \;}& 
      \mathbb{C}
      \\
      z &\mapsto& \overline{z}
    \end{array}
  $$
  is self-adjoint (cf. Lem. \ref{SelfAdjointAntiLinearOperator}):
  $$
    \begin{aligned}
      \big\langle
        \widehat{T} z
        ,
        w
      \big\rangle
      & =
      \big\langle
        \overline{z}
        ,
        w
      \big\rangle
      \\
      & =
      \overline{\overline{z}} \, w
      \\
      & =
      z \, w
      \\
      & =
      \overline{
        \overline{z} \, \overline{w}
      }
      \\
      & =
      \overline{
        \big\langle
           z, \overline{w}
        \big\rangle
      }
      \\
      & =
      \overline{
        \big\langle
           z, \widehat{T} w
        \big\rangle
      }
      \mathrlap{\,.}
    \end{aligned}
  $$
\end{example}

\begin{example}
  The canonical [[quaternionic structure]] on $\mathbb{C}^2$
  $$
    \begin{array}{ccc}
      \mathbb{C}^2 
        &\xrightarrow{\; \widehat{T} \;}& 
      \mathbb{C}^2
      \\
      \left(
      \begin{matrix}
        z_1
        \\
        z_2
      \end{matrix} 
      \right)
        &\mapsto& 
      \left(
      \begin{matrix}
        -\overline{z_2}
        \\
        \overline{z_1}
      \end{matrix} 
      \right)
    \end{array}
  $$
  is anti-self-adjoint (cf. Lem. \ref{SelfAdjointAntiLinearOperator}):

$$
  \begin{aligned}
    \Big\langle
      \widehat{T}\vec z
      ,\,
      \vec w
    \Big\rangle
    & =
    \left\langle
    \left(
      \begin{matrix}
        -\overline{z_2}
        \\
        \overline{z_1}
      \end{matrix} 
    \right)
    ,
    \left(
      \begin{matrix}
        w_1
        \\
        w_2
      \end{matrix} 
    \right)
    \right\rangle
    \\
    & =
    - z_2 \, w_1 \;+\; z_1 \, w_2
    \\
    & =
    \overline{
      - \overline{z_2} \, \overline{w_1}
      +
      \overline{z_1} \, \overline{w_2}
    }
    \\
    & =
    \overline{
      \left\langle
      \left(
        \begin{matrix}
          z_1
          \\
          z_2
        \end{matrix} 
      \right)
      ,
      \left(
        \begin{matrix}
          \overline{w_2}
          \\
          -\overline{w_1}
        \end{matrix} 
      \right)
    \right\rangle
    }
    \\
    & = 
    -
    \Big\langle
      \vec z
      ,\,
      \widehat{T} \vec w
    \Big\rangle
    \mathrlap{\,.}
  \end{aligned}
$$
\end{example}

\begin{lemma}
\label{SelfAdjointAntiLinearOperator}
  For a complex [[anti-linear operator]] $A$ on a [[Hilbert space]] $\mathscr{H}$, the following are equivalent:

1. $A^\dagger = A$ with respect to the [[Hermitian inner product]] $\langle -,-\rangle$,

1. $A^\ast = A$ with respect to the underlying real inner product $Re\big(\langle -,-\rangle\big)$.

\end{lemma}
\begin{proof}
  One direction is immediate: 
$$
  \big\langle A v , w \big\rangle 
  =
  \overline{
    \big\langle v , A w \big\rangle 
  }
  \;\;\;\;\;\; 
  \Rightarrow
  \;\;\;\;\;\;
  Re\Big(
    \big\langle A v , w \big\rangle 
  \Big)
  =
  Re\Big(
  \overline{
    \big\langle v , A w \big\rangle 
  }
  \Big)
  =
  Re\Big(
    \big\langle v , A w \big\rangle 
  \Big)
  \mathrlap{\,.}
$$

In the other direction: Assuming that 
$$
  Re\Big(
    \big\langle A v , w \big\rangle 
  \Big)
  =
  Re\Big(
    \big\langle v , A w \big\rangle 
  \Big)
$$
we need to show that then 
$$
  Im\Big(
    \big\langle A v , w \big\rangle 
  \Big)
  =
  -
  Im\Big(
    \big\langle v , A w \big\rangle 
  \Big)
  \mathrlap{\,.}
$$
For that we compute as follows (where we use the convention that $\langle-,-\rangle$ is anti-linear in the first and linear in the second argument, but the same conclusion holds of course with the other convention):
$$
  \begin{array}{lll}
    Im\Big(
      \big\langle A v , w \big\rangle 
    \Big)
    & =
    Re\Big(
      -\mathrm{i}
      \big\langle A v , w \big\rangle 
    \Big)   
    & \text{basic property of complex arithmetic}
    \\
    & =
    Re\Big(
      \big\langle A v , - \mathrm{i} w \big\rangle 
    \Big)   
    & \text{sesqui-linearity of inner product}
    \\
    & =
    Re\Big(
      \big\langle v , A(-\mathrm{i} w) \big\rangle 
    \Big)   
    & \text{assumption of real self-adjointness}
    \\
    & =
    Re\Big(
      \big\langle v , \mathrm{i} A w \big\rangle 
    \Big)   
    & \text{assumption of complex anti-linearity}
    \\
    & =
    Re\Big(
      \mathrm{i}
      \big\langle v , A w \big\rangle 
    \Big)   
    & \text{sesqui-linearity of inner product}
    \\
    & =
    -Im\Big(
      \big\langle v , A w \big\rangle 
    \Big)   
    & \text{basic property of complex arithmetic}
    \mathrlap{\,.}
  \end{array}
$$

\end{proof}

\begin{proposition}
\label{KaroubiModelForKO2}
  The space of [[Fredholm operators]] on the complex Hilbert space $\mathscr{H}$ which are

1. [[anti-linear maps|anti-linear]],

1. [[self-adjoint operator|self-adjoint]] (cf. Lem. \ref{SelfAdjointAntiLinearOperator})

is a classifying space for $K\mathrm{O}^2$.
\end{proposition}
([Karoubi 1970 Prop. 1.9](#Karoubi1970))

It is useful to reformulate Prop. \ref{KaroubiModelForKO2} as follows:

\begin{proposition}
On the complex Hilbert space $\mathscr{H}$ consider a [[real structure]] $\widehat T$, hence 

1. $\widehat{T}$ is [[anti-linear map|anti-linear]],

2. $\widehat{T}^2 = -1$,

3. $\widehat{T}^\dagger = \widehat{T}$ (cf. Lem. \ref{SelfAdjointAntiLinearOperator}).

On the $\mathbb{Z}/2$-graded Hilbert space $\mathscr{H} \oplus \mathscr{H}$ consider 

$$
  \widehat{C}
  \,\coloneqq\,
  \left(
  \begin{matrix}
    0 & \widehat{T} 
    \\
    \widehat{T} & 0
  \end{matrix}
  \right)
  \mathrlap{\,.}
$$

Then the space
 
$$
  \bigg\{
    F \in Fred(\mathscr{H} \oplus \mathscr{H})
    \;\bigg\vert\;
    \substack{
      F\;\text{is odd},
      \\
      F^\dagger = F,
    }
    \;\;
    F \circ \widehat{C} = \widehat{C} \circ F
  \bigg\}
$$

is a classifying space for $K\mathrm{O}^2$.
\end{proposition}
\begin{proof}
  The fact that $F$ in our space is odd and self-adjoint implies that it is of the form
$$
  F 
    = 
  \left(
  \begin{matrix}
    0 & f^\dagger
    \\
    f & 0
  \end{matrix}
  \right)
  \,.
$$
From this, the further condition that it commutes with $\widehat{C}$,
$$
  \left(
  \begin{matrix}
    0 & \widehat{T}
    \\
    \widehat{T} & 0
  \end{matrix}
  \right)
  \cdot
  \left(
  \begin{matrix}
    0 & f^\dagger
    \\
    f & 0
  \end{matrix}
  \right)
  =
  \left(
  \begin{matrix}
    0 & f^\dagger
    \\
    f & 0
  \end{matrix}
  \right)
  \cdot
  \left(
  \begin{matrix}
    0 & \widehat{T}
    \\
    \widehat{T} & 0
  \end{matrix}
  \right)
  \mathrlap{\,,}
$$
means equivalently that
$$
  \widehat{T} \circ f 
    \;=\; 
  f^\dagger \circ \widehat{T}
  \,,
$$
and hence our space is equivalently given by
$$
  \Big\{
    f \in Fred(\mathscr{H})
    \;\Big\vert\;
    \widehat{T} \circ f 
      \;=\; 
    f^\dagger \circ \widehat{T}
  \Big\}
  \,.
$$
For $f$ of this from, notice that $\widehat{T} \circ f$ is (anti-linear and) self-adjoint:
$$
  \big(
    \widehat{T} \circ f
  \big)^\dagger
  \;=\;
  f^\dagger \circ \widehat{T}
  \;=\;
  \widehat{T} \circ f
  \mathrlap{\,.}
$$

Therefore this space is homeomorphic to the space from Prop. \ref{KaroubiModelForKO2}, via the map
$$
  f \;\mapsto\; \widehat{T} \circ f 
  \,,
$$
and hence the claim follows by Prop. \ref{KaroubiModelForKO2}.
\end{proof}

* {#Karoubi1970} [[Max Karoubi]]: *Espaces Classifiants en K-Théorie*, Trans. Amer. Math. Soc. **147** (1970) 75-115 &lbrack;[doi:10.2307/1995218](https://doi.org/10.2307/1995218), [jstor:1995218](https://www.jstor.org/stable/1995218)&rbrack;



+-- {: .num_theorem #PullbackLawForACube}
###### Theorem
**(Pasting Law for Pullbacks in a Cube)**
\linebreak
Suppose we have a commutative cube in a category:

\begin{tikzcd}[sep = scriptsize]
{U'} && {V'} \\
& {X'} && {Y'} \\
U && V \\
& X && Y
\arrow[from=1-1, to=1-3]
\arrow[from=1-1, to=2-2]
\arrow[from=1-1, to=3-1]
\arrow[from=1-3, to=2-4]
\arrow[from=1-3, to=3-3]
\arrow[crossing over, from=2-2, to=2-4]
\arrow[from=2-4, to=4-4]
\arrow[from=3-1, to=3-3]
\arrow[from=3-1, to=4-2]
\arrow[from=3-3, to=4-4]
\arrow[from=4-2, to=4-4]
\arrow[crossing over, from=2-2, to=4-2]
\end{tikzcd}
\linebreak

* Assume the front and bottom faces are pullback squares. Then the following are equivalent:
  1.  The total rectangle from $U'\to V'$ to $X\to Y$ is a pullback.

  1.  The top and back faces are pullback squares.

  1.  The top face or the back face is a pullback square.

* Assume the top and back faces are pushout squares. Then the following are equivalent:
  1.  The total rectangle from $U'\to V'$ to $X\to Y$ is a pushout.

  1.  The front and bottom faces are pushout squares.

  1.  The front face or the bottom face is a pushout square.
 =--

\begin{proof}
Bla.
\end{proof}

