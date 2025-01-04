
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

\tableofcontents


## Definition

### Mod=$n$ integer Heisenberg group extensions of $\mathbb{Z}^2$
  {#IntegerHeisenbergGroup}

We discuss the restriction of the basic [[Heisenberg group]] $H_3$ (see [there](Heisenberg+group#H3InComponents)) along the inclusion $\mathbb{Z}^2 \hookrightarrow \mathbb{R}^2$ and the mod-$n$ [[quotient groups]] of that.

In the following, we denote [[cyclic groups]], for $n \in \mathbb{N}$, uniformly by
$$
  \mathbb{Z}_{n}
  \;\coloneqq\;
  \left\{
  \begin{array}{lcl}
    \mathbb{Z} &\vert& n = 0
    \\
    \mathbb{Z}/(n) &\vert& \text{otherwise}
    \mathrlap{\,.}
  \end{array}
  \right.
$$

\begin{proposition}
  For $n \in \mathbb{N}$,
  the [[central extension|central]] [[group extensions]] of $\mathbb{Z}^2$ by $\mathbb{Z}_n$ are all integral multiples of the following elementary Heisenberg extension:
\[
  \label{BasicIntegerHeisenbergExtensionOfZ2}
  \Big\{
    \big(a,b,[n]\big)
    \,\in\,
    \mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}_{2\vert k \vert}
    \;,\;
    \big(
      a,b,[n]
    \big)
    \cdot
    \big(
      a',b',[n']
    \big)
    \;=\;
    \big(
      a + a', b+ b', 
      [ 
        n + n' + 
        {\color{purple}
          a \, b'
        }
      ]
    \big)
  \Big\}
  \,.
\]
\end{proposition}

\begin{proof} 
The [[central extensions]] in question
$$
  1 
    \to 
  \mathbb{Z}_n
    \xrightarrow{cntrl}
  H
    \longrightarrow
  \mathbb{Z}^2
    \to
  1
$$
[are classified](group+extension#CentralExtensionClassificationByGroupCohomology) by the degree=2 [[group cohomology]] of $\mathbb{Z}^2$ with [[coefficients]] in $\mathbb{Z}_n$ (equipped with the [[trivial action|trivial]] $\mathbb{Z}^2$-[[group action|action]]).
 
That second [[group cohomology]] is:
\[
  \label{SecondGroupCohomologyOfZPlusZ}
  \begin{array}{ccl}
    H^2_{Grp}(\mathbb{Z}^2;\, \mathbb{Z}_n)
    &\simeq&
    H^2(B \mathbb{Z}^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    H^2(T^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    H^2(S^1_a \vee S^1_b \vee S^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    H^2(S^2;\, \mathbb{Z}_n)    
    \\
    &\simeq&
    \mathbb{Z}_n
    \mathrlap{\,,}
  \end{array}
\]

where we used, in order of the appearance:

1. that [[group cohomology]] is [[ordinary cohomology]] of the domain group's [[classifying space]];

1. that the [[classifying space]] of the [[integers]] is the [[circle]] and that this respects [[Cartesian products]];

1. that the [[stable homotopy type]] of the [[2-torus]] is the [[wedge sum]] of two [[circles]] with a [[2-sphere]] (see [there](torus#AsAHomotopyType)).

The generator of this [[cohomology group]] must be the [[group cohomology|group 2-cocycle]] 

$$
  \alpha \,\in\, H^2_{Grp}\big(
    \mathbb{Z}^2
    ;\,
    \mathbb{Z}_n
  \big)
$$

given by

\[
  \label{IntegerHeisenbergExtension}
  \begin{array}{ccc}
    \mathbb{Z}^2 
    \times
    \mathbb{Z}^2
    &\xrightarrow{\; \alpha \;}&
    \mathbb{Z}_{n}
    \\
    \big(
      (a,b), (a',b')
    \big)
    &\mapsto&
    [a b']
    \mathrlap{\,,}
  \end{array}
\]

(whose cocycle condition
$
  [a b'] + [(a+a')b'']
  =
  [a(b'+b'')] + [a' b'']
$
is evidently satisfied due to the [[distributive law]] in the [[ring]] $\mathbb{Z}$).
\end{proof}

\begin{example}
In the integer Heisenberg group (eq:BasicIntegerHeisenbergExtensionOfZ2)

* the [[inverse elements]] are given by
 
  $$
    \big(a ,\, b ,\, [n]\big)^{-1}
    \;=\;
    \big(
      -a ,\, -b ,\, [-n + a b]
    \big)
  $$

* the basic [[group commutators]] give

  $$
    \begin{array}{ccl}
      \big[
        (1,0,0), (0,1,0)
      \big]
      &\equiv&
      (1,0,0) \cdot (0,1,0) \cdot (1,0,0)^{-1} \cdot (0,1,0)^{-1}
      \\
      &=&
      (1,1,1) \cdot (-1,0,0) \cdot (0,-1,0)
      \\
      &=&
      (0,1,1) \cdot (0,-1,0)
      \\
      &=&
      (0,0,1)
      \mathrlap{\,.}
    \end{array}
  $$

\end{example}

Of particular interest is the second multiple of this basic extension:

\begin{proposition}
\label{TwiceHeisenbergExtensionInSymplecticForm}
  Twice the basic integer Heisenberg extension (eq:IntegerHeisenbergExtension) at $n = 2k$ is [[isomorphism|isomorphic]] to
\[
  \label{TwiceOfBasicIntegerHeisInSymplecticForm}
  \Big\{
    \big(a, b, [n]\big)
    \,\in\,
    \mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}_{2\vert k\vert}
    \,,
    \big(
      a, b, [n]
    \big)
    \cdot
    \big(
      a', b', [n']
    \big)
    \;=\;
    \big(
      a + a'
      ,\,
      b + b'
      ,\,
      [n + n' + {\color{red} a \cdot b' - a' \cdot b}]
    \big)
  \Big\}  
  \mathrlap{\,.}
\]
\end{proposition}
\begin{proof}
  It is sufficient to see that the second red summand is a 2-cocycle cohomologous to the first red summand, which means equivalently that the 2-cocycle
$$
  \big(
    (a, b), (a', b')
  \big)
  \;\mapsto\;
  a \cdot b' + a' \cdot b
$$
has a [[coboundary]]: This coboundary is readily found to be
$$
  (a, b) \;\mapsto\; - a \cdot b
  \,,
$$
since
$$
  - a \cdot b - a' \cdot  b'
  \,+\,
  (a + a') \cdot (b + b')
  \;=\;
  a \cdot b' + a' \cdot b  
  \,.
$$
\end{proof}

## Properties

### Representations

\begin{example}
The non-trivial [[irrep]] of twice the $\mathbb{Z}_{2 {\left\vert k \right\vert}}$-Heisenberg extension of $\mathbb{Z}^2$ (eq:TwiceOfBasicIntegerHeisInSymplecticForm)
\[
  \label{IrrepOfInyegerHeisenbergGroup}
  \begin{array}{ccc}
    \widehat{\mathbb{Z}^2}
    &
    \xrightarrow{\; W \;}
    &
    \mathrm{Aut}\big(
      \mathscr{H}_1
    \big)
  \end{array}
\]
is, up to [[isomorphism]], given by:
$$
  \mathscr{H}_1
  \;\coloneqq\;
  \mathbb{C}\big[\mathbb{Z}_{\vert k \vert}\big]
$$
$$
  \begin{array}{ccccccl}
  W_a  
  & \coloneqq &
  W(1,0,0)
  &\colon&
  \big\vert [n] \big\rangle
  &\mapsto&
  e^{2 \pi \mathrm{i} \tfrac{n}{k}}
  \big\vert [n] \big\rangle
  \\
  W_b  
  &\coloneqq&
  W(0,1,0)
  &\colon&
  \big\vert [n] \big\rangle
  &\mapsto&
  \big\vert [n + 1] \big\rangle
  \\
  \zeta 
  &\coloneqq&
  W(0,0,1)
  &\colon&
  \big\vert [n] \big\rangle
  &\mapsto&
  e^{\pi \mathrm{i} \tfrac{1}{k}}
  \big\vert [n] \big\rangle
  \mathrlap{\,.}
  \end{array}
$$
\end{example}


### Modular automorphisms

\begin{definition}
**(modular action on the integer Heisenberg group)**
\linebreak
Since the colored summand in (eq:TwiceOfBasicIntegerHeisInSymplecticForm) is the canonical [[symplectic form]] on $\mathbb{Z}^2$, the integer [[symplectic group]] in dimension 2, hence the [[modular group]]
$$
  \Big\{
    g \in \mathrm{GL}_2(\mathbb{Z})
    \,\Big\vert\,
    \underset{
      \mathrm{det}(g)
      \cdot
      (a b' - a' b)
    }{
    \underbrace{
    (g_{1 1} a + g_{12} b)
    (g_{2 1} a' + g_{22} b')
    -
    (g_{11} a' + g_{12}b')
    (g_{21} a + g_{22} b)
    }
    }
    =
    a b' - a'b
  \Big\}
  \;\simeq\;
  \mathrm{SL}_2(\mathbb{Z})
$$
(which is generated by 
$
  S
  \;=\;\left[
    \begin{array}{rr}
    0 & 1
    \\
    -1 & 0
  \end{array}
  \right]
$
and
$
  T
  \;=\;
  \left[
  \begin{array}{rr}
    1 & 1
    \\
    0 & 1
  \end{array}
  \right]
$),
acts by evident group [[automorphism]] on (eq:TwiceOfBasicIntegerHeisInSymplecticForm):
\[
  \label{SymplecticActonOnSecondIntegerHeisenberg}
  \begin{array}{ccc}
    \mathrm{SL}_2(\mathbb{Z})
    \times
    \widehat{\mathbb{Z}^2}
    &\xrightarrow{}&
    \widehat{\mathbb{Z}^2}
    \\
    \Big(
      g, \big(a,b,[n]\big)
    \Big)
    &\mapsto&
    \Big(
      g_{11}a + g_{12}b
      ,\,
      g_{21}a + g_{22}b
      ,\,
      [n]
    \Big)
    \mathrlap{\,.}
  \end{array}
\]

\end{definition}

\begin{proposition}
There exists a [[linear representation]]
$$
  \begin{array}{ccc}
    \mathrm{SL}_2(\mathbb{Z})
    \times
    \mathscr{H}_1
    &\xrightarrow{\;}&
    \mathscr{H}_1
    \mathrlap{\,,}
  \end{array}
$$
which [[intertwiner|intertwines]] the action (eq:IrrepOfInyegerHeisenbergGroup)
of $\widehat{\mathbb{Z}^2}$ on $\mathscr{H}_1$, with its automorphic images under $\mathrm{SL}_2(\mathbb{Z})$\eqref{SymplecticActonOnSecondIntegerHeisenberg},
in that 
$$
  m(W) \cdot m\Big(
    \big\vert [n] \big\rangle
  \Big)
  \;=\;
  m\Big(
    W \cdot 
    \big\vert [n] \big\rangle
  \Big)
  \,,
  \;\;\;\;\;
  \forall
  \left\{
    \begin{array}{ccc}
      m &\in& SL_2(\mathbb{Z})
      \\
      W &\in& \widehat{\mathbb{Z}^2}
      \\
      {\left\vert [n] \right\rangle} &\in& \mathscr{H}_1
    \end{array}
  \right.
$$
This representation is just the [[modular functor|modular action]] known from [[abelian Chern-Simons theory]] (cf. [Manoliu 1998a p 67](abelian+Chern-Simons+theory#Manoliu98a)):
$$
  \begin{array}{ccr}
  S\Big(
    {\big\vert [n] \big\rangle}
  \Big)
  &=&
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, n
     }{
       k
     }
  }
  {\big\vert
   [\widehat{n}]
  \big\rangle}
  \\
  T\Big(
    \big\vert [n] \big\rangle
  \Big)
  &=&
  e^{ 
    \pi \mathrm{i}
    \tfrac{ n^2 }{ k }
  }
  {\big\vert
   [ n ]
  \big\rangle}
   \end{array}
$$

\end{proposition}
\begin{proof}
By direct computation:
$$
  \begin{array}{ccl}
    S(W_a)
    \cdot
    S\Big(
      {\big\vert
        [n]
      \big\rangle}
    \Big)
    &\equiv&
    W_b^{-1}
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, n
     }{
       k
     }
  }
  {\big\vert
   [\widehat{n}]
  \big\rangle}
  \\
  &=&
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       (\widehat{n} + 1) \, n
     }{
       k
     }
  }
  {\big\vert
   [\widehat{n}]
  \big\rangle}
  \\
  &=&
  e^{
    2 \pi \mathrm{i} 
    \tfrac{n}{k}
  }
    S\Big(
      \big\vert
        [n]
      \big\rangle
    \Big)  
  \\
  &=&
  S\Big(
    W_a \big\vert [n] \big\rangle
  \Big)
  \end{array}
$$

$$
  \begin{array}{ccl}
    S(W_b)
    \cdot
    S\Big(
      {\big\vert
        [n]
      \big\rangle}
    \Big)
    &\equiv&
    W_a
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, n
     }{
       k
     }
  }
  \big\vert
   [\widehat{n}]
  \big\rangle
  \\
  &=&
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{2 \pi \mathrm{i} \tfrac{n}{k}}
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, n
     }{
       k
     }
  }
  {\big\vert
   [\widehat{n}]
  \big\rangle}
  \\
  &=&
  S\Big(
    W_a 
    {\big|
      [n]
    \big\rangle}
  \Big)
  \end{array}
$$

$$
  \begin{array}{ccl}
    T(W_a) \cdot
    T\Big(
      {\big\vert [n] \big\rangle}
    \Big)
    &\equiv&
    W_a 
    \,
    e^{
      \mathrm{i} \pi
      \tfrac{n^2}{k}
    }
    {\big\vert
      [n]
    \big\rangle}
    \\
    &=&
    e^{2 \pi \mathrm{i} \tfrac{n}{k}}
    e^{
      \mathrm{i} \pi
      \tfrac{n^2}{k}
    }
    {\big\vert
      [n]
    \big\rangle}
    \\
    &=&
    T\Big(
      W_a
      \,
      {\big\vert
        [n]
      \big\rangle}
    \Big)
  \end{array}
$$

$$
  \begin{array}{ccl}
    T(W_b)\cdot
    T\Big(
      {\big\vert
        [n]
      \big\rangle}
    \Big)
    &\equiv&
    W_b \, W_a \, 
    e^{2\pi \mathrm{i} \tfrac{1}{k}}
    e^{\pi \mathrm{i} \tfrac{n^2}{k}}
    {\big\vert
      [n]
    \big\rangle}
    \\
    &=&
    e^{\pi \mathrm{i} 
    \tfrac{
      n^2
      +
      2n
      +
      1
    }{k}}
    {\big\vert
      [n + 1]
    \big\rangle}
    \\
    &=&
    e^{\pi \mathrm{i} 
    \tfrac{
      (n+1)^2
    }{k}}
    {\big\vert
      [n + 1]
    \big\rangle}
    \\
    &=&
    T\Big(
      W_b
      {\big\vert
        [n]
      \big\rangle}
    \Big)
  \end{array}
$$

\end{proof}

## Related entries

* [2-Cohomotopy moduli of surfaces](cohomotopy#CohomotopyModuliOfSurfaces)


## Literature

On the integer Heisenberg $\mathbb{Z}$-extensions of $\mathbb{Z}^{2g}$:

* {#LeePacker96} Soo Teck Lee, Judith A. Packer: *The Cohomology of the Integer Heisenberg Groups*, Journal of Algebra **184** 1 (1996) 230-250 &lbrack;[doi:10.1006/jabr.1996.0258](https://doi.org/10.1006/jabr.1996.0258)&rbrack;
  > (concerning its [[group cohomology]])

* Roman Budylin: *Conjugacy classes in discrete Heisenberg groups*, Sbornik: Mathematics **205** 8 (2014) 1069–1079 &lbrack;[arXiv:1405.5499](https://arxiv.org/abs/1405.5499), [doi:10.1070/SM2014v205n08ABEH004410](https://doi.org/10.1070/SM2014v205n08ABEH004410)&rbrack;

* Jayadev S. Athreya, Ioannis Konstantoulas: *Lattice deformations in the Heisenberg group*, Groups, Geometry and Dynamics **14** 3 (2020) 1007–1022 &lbrack;[arXiv:1510.01433](https://arxiv.org/abs/1510.01433), [doi:10.4171/ggd/572](https://doi.org/10.4171/ggd/572)&rbrack;

* Ruiwen Dong, p 9 of: *Recent advances in algorithmic problems for semigroups*, ACM SIGLOG News **10** 4 (2023) 3-23 &lbrack;[arXiv:2309.10943](https://arxiv.org/abs/2309.10943), [doi:10.1145/3636362.3636365](https://doi.org/10.1145/3636362.3636365)&rbrack;

[[!redirects integer Heisenberg groups]]



