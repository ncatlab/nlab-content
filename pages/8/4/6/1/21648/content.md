
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

\tableofcontents

## Definition

\begin{definition}
By $SL(2,\mathbb{H})$ one denotes the [[special linear group]] of $2 \times 2$ [[matrices]] with [[coefficients]] in the [[quaternions]], where "special" refers to their [[Dieudonné determinant]] being unity:

$$
  SL(2,\mathbb{H})
  \;\coloneqq\;
  \Big\{\left.
     A 
       \in
     Mat_{2 \times 2}(\mathbb{H})
     \;\right\vert\;
     det_D(A) = 1
  \Big\}
  \mathrlap{\,,}
$$

namely (cf. [Venâncio & Batista 2021 (2.4)](#VenâncioBatista21))

\[
  \label{QuaternonicDeterminant}
    det_D\left(
        \array{
          a & b 
          \\
          c & d 
        }
    \right)
    \;
    =
    \;
    \left\{
    \begin{array}{cl}
      0 
      & 
      \;\text{if}\; a = b = c = d = 0
      \\
      \left\vert
        a d - a c a^{-1} b
      \right\vert
      &
      \;\text{if}\; a \neq 0
      \\
      \left\vert
        d a - d b d^{-1} c
      \right\vert
      & 
      \;\text{if}\; d \neq 0
      \\
      \left\vert
        b d b^{-1} a  - b c
      \right\vert
      & 
      \;\text{if}\; b \neq 0
      \\
      \left\vert
        c a c^{-1} d - c b
      \right\vert
      &
      \;\text{if}\; c \neq 0
    \mathrlap{\,.}
  \end{array}
  \right.
\]

\end{definition}


Here 

\[
  \label{QuaternionNormSquare}
  \left\vert q \right\vert 
    \;\coloneqq\; 
  \textstyle{\sqrt{q q^\ast}}
   \;\in \mathbb{R}
\] 

is the standard [[norm]] on [[quaternions]]. 


\begin{remark}
Since the norm (eq:QuaternionNormSquare) evidently satisfies

$$
  \left\vert q q'\right\vert
  \;=\;
  \left\vert q \right\vert
  \cdot
  \left\vert q' \right\vert
  \mathrlap{\,,}
$$

the formulas (eq:QuaternonicDeterminant) are furthermore equivalent to  

\[
  \label{QuaternonicDeterminantFactored}
    det_D\left(
        \array{
          a & b 
          \\
          c & d 
        }
    \right)
    \;=\;
    \left\{
    \begin{array}{cl}
      0 
      &
      \;\text{if}\; a = b = c = d = 0
      \\
      \left\vert
        a
      \right\vert
      \cdot
      \left\vert
        d - c a^{-1} b
      \right\vert
      & 
      \;\text{if}\; a \neq 0
      \\
      \left\vert
        d
      \right\vert
      \cdot
      \left\vert
        a - b d^{-1} c
      \right\vert
      &
      \;\text{if}\; d \neq 0
      \\
      \left\vert
        b
      \right\vert
        \cdot
      \left\vert
        d b^{-1} a  - c
      \right\vert
      &
      \;\text{if}\; b \neq 0
      \\
      \left\vert
        c
      \right\vert
        \cdot
      \left\vert
        a c^{-1} d - b
      \right\vert
      & 
      \;\text{if}\; c \neq 0
    \mathrlap{\,.}
  \end{array}
  \right.
\]

In this form they appear in [Cohen & De Leo 1999 p. 11](#CohenDeLeo99).

\end{remark}




## Properties

### Relation to $Sp(2)$
 {#RelationToSp2}


\begin{lemma}
\label{BasicPropertiesOfDDeterminant}
The above $det_D$ (eq:QuaternonicDeterminant) satisfies

\[
  \begin{aligned}
    det_D(A) 
    & \in\; \mathbb{R}_{\geq 0}
    \\
    det_D(I_2) 
    & =\; 1
    \\
    det_D(A \cdot B) 
    &=\;
    det_D(A) \cdot det_D(B)
    \\
    det_D\big(
      A^\dagger
    \big)
    &=\;
    det_D(A)
    \mathrlap{\,.}
  \end{aligned}
\]

\end{lemma}
(cf. [Cohen & De Leo 1999 Thm. 5.1(5) & Cor. 6.4](#CohenDeLeo99))

\begin{proposition}\label{UnitarySubgroup}
Every quaternionic [[unitary matrix]] (hence in [[Sp(2)]]) happens to have unit [[Dieudonné determinant]], whence we have a [[subgroup]] inclusion:

$$
  Sp(2)
  \;\equiv\;
  U(2,\mathbb{H})
  \;\subset\;
  SL(2,\mathbb{H})
  \,.
$$

\end{proposition}
([Cohen-De Leo 99, Cor. 6.4](Dieudonne+determinant#CohenDeLeo99))
\begin{proof}
  By definition, $A \in Mat_{2 \times 2}(\mathbb{H})$ is in $Sp(2)$ iff $A \cdot A^\dagger = I_2$. From this, Lemma \ref{BasicPropertiesOfDDeterminant} gives 
$$
  \begin{aligned}
    1 
    & = 
    det_D\big(A \cdot A^\dagger \big)
    \\
    & = 
    det_D(A) \cdot det_D\big(A^\dagger\big)
    \\
    & = 
    \big( det_D(A) \big)^2
    \,.
  \end{aligned}
$$
But the only element $det_D(A) \in \mathbb{R}_{\geq 0}$ satisfying this equation is $det_D(A) = 1$.
\end{proof}


### Relation to $Spin(5,1)$
 {#RelationToSpin51}

Under the [[conjugation action]] on $2 \times 2$ [[Hermitian matrices]] with [[coefficients]] in the [[quaternions]], $SL(2,\mathbb{H})$ is identified with [[Spin(5,1)]] and its canonical [[action]] on [[Minkowski spacetime]] $\mathbb{R}^{5,1}$.

(cf. [Venâncio & Batista 2021](#VenâncioBatista21))

For more on this see at _[[spin representation]]_, _[[supersymmetry and division algebras]]_ and _[[geometry of physics -- supersymmetry]]_.

This [[exceptional isomorphism]] is compatible with that between the [[subgroups]] [[Spin(5)]] and the [[quaternion unitary group]] [[Sp(2)]]:

\begin{tikzcd}
  \mathrm{Spin}(5) 
    \ar[r, hook] 
    \ar[d, "\sim"{sloped}]
  & 
  \mathrm{Spin}(1,5)
    \ar[d, "\sim"{sloped}]
  \\
  \mathrm{U}(2,\mathbb{H}) 
    \ar[r, hook] 
  & 
  \mathrm{SL}(2,\mathbb{H})
\end{tikzcd}

## Related concepts

[[!include exceptional spinors and division algebras -- table]]

## References

* {#CohenDeLeo99} Nir Cohen, Stefano De Leo, Cor. 6.4 in: *The quaternionic determinant*, Electronic Journal of Linear Algebra **7** (2000) 100-111 &lbrack;[arXiv:math-ph/9907015](https://arxiv.org/abs/math-ph/9907015), [doi:10.13001/1081-3810.1050](https://doi.org/10.13001/1081-3810.1050), [eudml:121484](https://eudml.org/doc/121484)&rbrack;

* {#VenâncioBatista21} [[Joás Venâncio]], [[Carlos Batista]], Sections 2,3 of: _Two-Component Spinorial Formalism using Quaternions for Six-dimensional Spacetimes_, Adv. Appl. Clifford Algebras **31** 71 (2021) &lbrack;[arXiv:2007.04296](https://arxiv.org/abs/2007.04296), [doi:10.1007/s00006-021-01172-1](https://doi.org/10.1007/s00006-021-01172-1)&rbrack;

[[!redirects SL2H]]
