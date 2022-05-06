

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the presence of [[D-branes]], plain [[type II string theory]] in fact has a [[quantum anomaly]] reflected by [[tadpole]] [[Feynman diagrams]] in the [[string perturbation series]] for [[RR-fields]]. This anomaly cancels if the [[D-branes]] are accompanied by a suitable collection of [[O-planes]], hence if one considers [[orientifold]] backgrounds ([Sagnotti 88, pp. 5](#Sagnotti88), [Simon-Polchinski 96, section 3](#SimonPolchinski96)). (For space-filling [[O-planes]] this means to consider [[type I string theory]] instead.)

\begin{center}
<img src="https://ncatlab.org/nlab/files/RRTadpoleCancellation.jpg" width="600">
\end{center}

> graphics grabbed from [Ibanez-Uranga 12](#IbanezUranga12)

Accordingly, tadpole cancellation via [[orientifolds|orientifolding]] is a key consistency condition in the construction of [[intersecting D-brane models]] for [[string phenomenology]].

Traditionally RR-tadpole cancellation is discussed in [[ordinary cohomology]], the common arguments notwithstanding that [[D-brane charge]] should be in [[K-theory]].

Discussion of tadpole cancellation with [[D-brane charge]] regarded in [[K-theory]] was initated in [Uranga 00, Section 5](#Uranga00), see also [Garcia-Uranga 05](#GarciaUranga05), [Marchesano 03, Section 4](#Marchesano03), [Maiden-Shiu-Stefanski 06, Section 5](#MaidenShiuStefanski06).

But the situation seems to remain somewhat inconclusive (see also [Moore 14, p. 21-22](#Moore14)).

## For fractional D-branes at orbifold singularities
 {#ForFractionalDBranes}

More details are understood in the special case of [[fractional D-branes]] stuck at [[orbifold]]/[[orientifold]] singularities, whose [[D-brane charge]] is supposed to be in the [[equivariant K-theory]] of the point, hence the [[representation ring]] of the given [[isotropy group]].

### In terms of equivariant K-theory / the representation ring

In this case tadpole cancellation conditions are given by [[representation theory|representation theoretic]] [[equations]], constraining the [[character of a linear representation|characters]] of the [[linear representations]] corresponding to the [[fractional D-branes]].

Detailed review of this is in [Marchesano 03, Section 4](#Marchesano03), based on [ABIU 99](#ABIU99), [Honecker 02](#Honecker02).

Let $G$ be a [[finite group]]. Let 

$$
  [1]
    \subset 
  [H_1]
    \subset 
  [H_2]
    \subset
    \cdots
    \subset
  [G]
$$ 

be a [[linear extension of a partial order|linear extension]] of its [[partially ordered set|partially ordered]] [[lattice of subgroups|lattice of]] [[conjugacy classes]] of [[subgroups]], with [[subset|sub-]] [[linear order]] of [[cyclic group|cyclic]] [[subgroups]]

$$
  [1]
    \subset 
  \left[
   \left\langle
     g_1
   \right\rangle
  \right]
    \subset 
  \left[
   \left\langle
     g_2
   \right\rangle
  \right]
    \subset
    \cdots
    \subset
  \left[
   \left\langle
     g_{\vert ConjCl(G)\vert}
   \right\rangle
  \right]
  \,.
$$ 

This way every [[virtual representation]] $[V] \in RU(G) = KU_G(\ast)$ (the [[D-brane charge]] of a [[bound state]] of [[fractional D-branes]]/[[anti-branes]]) has a [[character of a linear representation|character]] which is a list of [[complex numbers]] of the form


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\cdots$ |  $\left[\langle g_{\vert ConjCl(G)\vert}\rangle\right]$ |
|--|--|--|--|--|--|
| $\chi_V =$ | $dim(V)$ |  $tr_V\left( g_1\right)$ |  $tr_V\left(g_2\right)$ | $\cdots$ |  $tr_V\left(g_{\vert ConjCl(G)\vert}\right)$ | 
| ${{\text{fractional} \atop \text{D-brane/anti-brane}} \atop \text{bound state}}$ |  ${ {\text{mass} =} \atop {{\text{net number} \atop \text{of branes}}}}$ | ${\text{RR-charge in} \atop {g_1\text{-twisted sector}}}$  | ${\text{RR-charge in} \atop {g_2\text{-twisted sector}}}$  | $\cdots$  | $\cdots$  | 

Here $dim(V) \in \mathbb{Z}$ is the [[mass]], hence the net number of [[fractional D-branes]]/[[anti-branes]] in the [[bound state]], while $tr_V\left(g_k\right)$ is (up to a global [[rational number]]-factor $1/{\vert G \vert}$) supposed to be its  [[charge]] as seen by the [[RR-fields]] in the $g_k$-[[twisted sector]].

Now in terms of this, the tadpole cancellation condition is simply that the RR-charges in all non-trivially twisted sectors vanish:

\[
  \label{VanishingOfCharacterValuesOnNontrivialSubgroups}
  \chi_{V}\left(g_{\geq 1}\right) \;=\; 0
\]

([Marchesano 03 (4.9)](#Marchesano03))

On the other hand, at an [[orientifold]] singularity, the [[O-plane]] itself carries such charge

| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\cdots$ |  $\left[\langle g_{\vert ConjCl(G)\vert}\rangle\right]$ |
|--|--|--|--|--|--|
| $\chi_O =$ | $dim(O)$ |  $tr_O\left( g_1\right)$ |  $tr_O\left(g_2\right)$ | $\cdots$ |  $tr_O\left(g_{\vert ConjCl(G)\vert}\right)$ | 
| $\text{O-plane}$ |   | ${\text{O-plane charge in} \atop {g_1\text{-twisted sector}}}$  | ${\text{O-plane-charge in} \atop {g_2\text{-twisted sector}}}$  | $\cdots$  | $\cdots$  | 

Now the tadpole cancellation condition is that (all representations are real and) this O-plane charge is cancelled, an [[affine space|affine]] version of the previous condition

$$
  \chi_{V}\left(g_{k \geq 1}\right) 
    + 
  \chi_{O}\left( g_{k \geq 1} \right) \;=\; 0
  \,.
$$


([Marchesano 03 (4.15)](#Marchesano03))


### Examples

We discuss the solutions to the homogeneous tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for [[fractional D-branes]] at [[orbifold]] [[singularities]] for [[isotropy group]] one of  the [[nonabelian group|non-abelian]] [[finite subgroups of SU(2)]], 

$$
  G_{DE}
  \;\subset\;
  SU(2)
$$

hence those in the [[ADE-classification|D- and E-series]], hence the [[binary dihedral groups]] $2 D_{2n}$ and the three exceptional cases: [[2T]], [[2O]] and [[2I]].

For these groups, by [BSS 18, Theorem 4.1](#BurtonSatiSchreiber18) the [[virtual representation|virtual]] [[permutation representations]] span precisely the sub charge lattice of integral (non-irrational) characters/RR-charges in the [[orientifold]] charge lattice of the corresponding [[ADE-singularity]], namely of the [[equivariant KO-theory]]=[[representation ring|real representation ring]]

$$
  KO^0_{G_{DE}}(\ast)
  \;=\;
  RO\left( G_{DE} \right)
  \,.
$$

 Since the tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) in particular requires the characters/charges to be integral (specifically: zero) the general solution to the tadpole cancellation condition is indeed in this sub-lattice, and so that is where we may and do solve it, below.

We find that in each case there is precisely a 1-dimensional (i.e. $\simeq \mathbb{Z}$) sublattice of the charge lattice (the [[representation ring]]) which solves the homogenous tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups), hence a sublattice given by the [[integer]]-multiples $n \cdot V_0$ of one single [[fractional D-brane]] [[bound state]] $V_0 \in KO^0_G(\ast)$. There are then necessarily two of these generators $\pm V_0$. We find that in all cases the [[mass]] of these in non-vanishing, and hence one of the two has [[positive number|positive]] [[mass]], the other [[negative number|negative]] [[mass]] (net [[fractional D-brane]] [[anti D-brane]]).  Picking the [[positive number|positive]] [[mass]] generators for definiteness, we find the following result:


| [[singularity]] | [[mass]] |
|----|-----|
| $2 D_4$ | $8$ | 
| $2 D_6$ | $12$ |
| $2 D_{8}$ | $16$ | 
| $2 D_{10}$ | $20$ | 
| $2 D_{12}$ | $24$ | 
| $2 D_{14}$ | $28$ | 
| $2 D_{16}$ | $32$ | 



#### At a $2 D_4$-orientifold singularity
 {#At2d4Singularity}

For $G = 2 D_4 = Q_8$ the [[binary dihedral group]] of [[order of a group|order]] ${\vert 2 D_4\vert}$ (equivalently: the [[quaternion group]]), the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.1](#BurtonSatiSchreiber18)):


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | 
|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $-1$ | $\phantom{-}1$ |  $-1$ |
| $\chi_{V_3} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $-1$ | $-1$ |  $\phantom{-}1$ | 
| $\chi_{V_4} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $-1$ |  $-1$ | 
| $\chi_{V_5} =$ | $\phantom{-}4$ |  $-4$ |  $\phantom{-}0$ | $\phantom{-}0$ |  $\phantom{-}0$ | 

One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G =2 D_4$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1 
      +
    1 \cdot V_2
      + 
    1 \cdot V_3
      + 
    1 \cdot V_4
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$

whose minimal [[positive number|positive]] [[mass]] (net brane number) is


$$
  \begin{aligned}
    M_{2 D_4}
    & =
    dim(V)
    \\
    & = 
    \chi_V\left( [\langle e\rangle]\right) 
    & =
    1 + 1 + 1 + 1 + 4 
    \\
    & = 8
  \end{aligned}
$$



#### At a $2 D_6$-orientifold singularity
  {#At2D6Singularity}

For $G = 2 D_6$ the [[binary dihedral group]] of [[order of a group|order]] ${\vert 2 D_6\vert} = 12$, the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.2](#BurtonSatiSchreiber18)):


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |
|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $-1$ |  $-1$ | $\phantom{-}1$ |
| $\chi_{V_3} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $-1$ | $\phantom{-}0$ |  $\phantom{-}0$ | $-1$ |
| $\chi_{V_4} =$ | $\phantom{-}2$ |  $-2$ |  $\phantom{-}2$ | $\phantom{-}0$ |  $\phantom{-}0$ | $-2$ |
| $\chi_{V_5} =$ | $\phantom{-}4$ |  $-4$ |  $-2$ | $\phantom{-}0$ |  $\phantom{-}0$ | $\phantom{-}2$ |

One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G =2 D_6$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1 
      +
    1 \cdot V_2
      + 
    2 \cdot V_3
      + 
    1 \cdot V_4
      + 
    1 \cdot V_5
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$

whose minimal [[positive number|positive]]  [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2 D_6}
    & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1
        +
      1 \cdot 1
        + 
      2 \cdot 2
        + 
      1 \cdot 2
        + 
      1 \cdot 4
      & 
      \\
      & 
      =
      12
  \end{aligned}
$$


#### At a $2 D_8$-orientifold singularity
  {#At2D8Singularity}

For $G = 2 D_8$ the [[binary dihedral group]] of [[order of a group|order]] ${\vert 2 D_8\vert} = 16$, the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.3](#BurtonSatiSchreiber18)):


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ |
|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |$\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $-1$ |  $\phantom{-}1$ | $-1$ | $-1$ |
| $\chi_{V_3} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $-1$ |  $-1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_4} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $-1$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $-2$ | $\phantom{-}0$ |  $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_6} =$ | $\phantom{-}8$ |  $-8$ |  $\phantom{-}0$ | $\phantom{-}0$ |  $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ |


One sees from immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G =2 D_8$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1 
      +
    1 \cdot V_2
      + 
    1 \cdot V_3
      + 
    1 \cdot V_4
      + 
    2 \cdot V_5
      + 
    1 \cdot V_6
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$

whose minimal [[positive number|positive]]  [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2 D_8}
     & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1 
        +
      1 \cdot 1
        + 
      1 \cdot 1
        + 
      1 \cdot 1
        + 
      2 \cdot 2
        + 
      1 \cdot 8
      & 
      \\
      & 
      =
      16
  \end{aligned}
$$

#### At a $2 D_{10}$-orientifold singularity
  {#At2D10Singularity}

For $G = 2 D_{10}$ the [[binary dihedral group]] of [[order of a group|order]] ${\vert 2 D_{10}\vert} = 20$, the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.4](#BurtonSatiSchreiber18)):


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ |  $\left[\langle g_7\rangle\right]$ |
|--|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $-1$ | $-1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_3} =$ | $\phantom{-}2$ |  $-2$ |  $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}2$ | $\phantom{-}2$ | $-2$ | $-2$ |
| $\chi_{V_4} =$ | $\phantom{-}4$ |  $\phantom{-}4$ |  $\phantom{-}0$ | $\phantom{-}0$ | $-1$ | $-1$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-}8$ |  $-8$ |  $\phantom{-}0$ | $\phantom{-}0$ | $-2$ | $-2$ | $\phantom{-}2$ | $\phantom{-}2$ |




One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G =2 D_{10}$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1 
      +
    1 \cdot V_2
      + 
    1 \cdot V_3
      + 
    2 \cdot V_4
      + 
    1 \cdot V_5
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$

whose minimal [[positive number|positive]]  [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2 D_{10}}
      & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1
        +
      1 \cdot 1
        + 
      1 \cdot 2
        + 
      2 \cdot 4
        + 
      1 \cdot 8
      & 
      \\
      & 
      =
      20
  \end{aligned}
$$

#### At a $2 D_{12}$-orientifold singularity
  {#At2D12Singularity}

For $G = 2 D_{12}$ the [[binary dihedral group]] of [[order of a group|order]] ${\vert 2 D_{12}\vert} = 24$, the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.5](#BurtonSatiSchreiber18)):


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ |  $\left[\langle g_7\rangle\right]$ | $\left[\langle g_8\rangle\right]$ |
|--|--|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $-1$ | $-1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_3} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $-1$ | $\phantom{-}1$ | $-1$ | $\phantom{-}1$ | $-1$ | $-1$ |
| $\chi_{V_4} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ | $-1$ | $-1$ | $\phantom{-}1$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $-1$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}2$ | $-1$ | $-1$ | $-1$ |
| $\chi_{V_6} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $-1$ | $\phantom{-}0$ | $\phantom{-}0$ | $-2$ | $-1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_7} =$ | $\phantom{-}4$ |  $-4$ |  $\phantom{-}4$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $-4$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_8} =$ | $\phantom{-}8$ |  $-8$ |  $-4$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}4$ | $\phantom{-}0$ | $\phantom{-}0$ |





One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G =2 D_{12}$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1 
      +
    1 \cdot V_2
      + 
    1 \cdot V_3
      + 
    1 \cdot V_4
      + 
    2 \cdot V_5
      + 
    2 \cdot V_6
      + 
    1 \cdot V_7
      + 
    1 \cdot V_8
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$

whose minimal [[positive number|positive]]  [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2 D_{12}}
      & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1 
        +
      1 \cdot 1
        + 
      1 \cdot 1
        + 
      1 \cdot 1
        + 
      2 \cdot 2
        + 
      2 \cdot 2
        + 
      1 \cdot 4
        + 
      1 \cdot 8
      & 
      \\
      & 
      =
      24
  \end{aligned}
$$




#### At a $2 D_{14}$-orientifold singularity
  {#At2D14Singularity}

For $G = 2 D_{14}$ the [[binary dihedral group]] of [[order of a group|order]] ${\vert 2 D_{14}\vert} = 28$, the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.6](#BurtonSatiSchreiber18)):


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ |  $\left[\langle g_7\rangle\right]$ | $\left[\langle g_8\rangle\right]$ | $\left[\langle g_9\rangle\right]$ |
|--|--|--|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $-1$ | $-1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_3} =$ | $\phantom{-}2$ |  $-2$ |  $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}2$ | $\phantom{-}2$ | $\phantom{-}2$ | $-2$ | $-2$ | $-2$ |
| $\chi_{V_4} =$ | $\phantom{-}6$ |  $\phantom{-}6$ |  $\phantom{-}0$ | $\phantom{-}0$ | $-1$ | $-1$ | $-1$ | $-1$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-1}\mathllap{12}$ |  $\phantom{-1}\mathllap{-12}$ |  $\phantom{-}0$ | $\phantom{-}0$ | $-2$ | $-2$ | $-2$ | $\phantom{-}2$ | $\phantom{-}2$ | $\phantom{-}2$ |




One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G =2 D_{14}$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1 
      +
    1 \cdot V_2
      + 
    1 \cdot V_3
      + 
    2 \cdot V_4
      + 
    1 \cdot V_5
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$

whose minimal [[positive number|positive]]  [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2 D_{14}}
      & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1
        +
      1 \cdot 1
        + 
      1 \cdot 2
        + 
      2 \cdot 6
        + 
      1 \cdot 12
      \\
      & 
      =
      28
  \end{aligned}
$$



#### At a $2 D_{16}$-orientifold singularity
  {#At2D16Singularity}

For $G = 2 D_{16}$ the [[binary dihedral group]] of [[order of a group|order]] ${\vert 2 D_{16}\vert} = 32$, the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.7](#BurtonSatiSchreiber18)):


| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ |  $\left[\langle g_7\rangle\right]$ | $\left[\langle g_8\rangle\right]$ | $\left[\langle g_9\rangle\right]$ |$\left[\langle g_9\rangle\right]$ |
|--|--|--|--|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $-1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $-1$ | $-1$ | $-1$ | $-1$ |
| $\chi_{V_3} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $-1$ | $-1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_4} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $-1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $-1$ | $-1$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}2$ | $-2$ | $-2$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_6} =$ | $\phantom{-}4$ |  $\phantom{-}4$ |  $\phantom{-}0$ | $\phantom{-}0$ | $-4$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_7} =$ | $\phantom{-1}\mathllap{16}$ |  $\phantom{-1}\mathllap{-16}$ |  $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ | $\phantom{-}0$ |




One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G =2 D_{16}$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1 
      +
    1 \cdot V_2
      + 
    1 \cdot V_3
      + 
    1 \cdot V_4
      + 
    2 \cdot V_5
      + 
    2 \cdot V_6
      + 
    1 \cdot V_7
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$

whose minimal [[positive number|positive]]  [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2 D_{16}}
      & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1   
        +
      1 \cdot 1
        + 
      1 \cdot 1
        + 
      1 \cdot 1
        + 
      2 \cdot 2
        + 
      2 \cdot 4
        + 
      1 \cdot 16
      \\
      & 
      =
      32
  \end{aligned}
$$



#### At a $2 T$-orientifold singularity
  {#At2TSingularity}

For $G = 2 T$ the [[binary tetrahedral group]] (whose [[order of a group|order]] is ${\vert 2T \vert} =24$), the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.8](#BurtonSatiSchreiber18)):

| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ |
|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |$\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $-1$ | $-1$ |  $\phantom{-}2$ | $-1$ | $-1$ |
| $\chi_{V_3} =$ | $\phantom{-}3$ |  $\phantom{-}3$ |  $\phantom{-}0$ | $\phantom{-}0$ |  $-1$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_4} =$ | $\phantom{-}4$ |  $-4$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}0$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-}4$ |  $-4$ |  $-2$ | $-2$ |  $\phantom{-}0$ | $\phantom{-}2$ | $\phantom{-}2$ |


One sees by immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G = 2T$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1
    + 
    1 \cdot V_2
    + 
    3 \cdot V_3
    + 
    2 \cdot V_4
    + 
    1 \cdot V_5 
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$


whose minimal [[positive number|positive]] [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2I}
      & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
        1 \cdot 1
        + 
        1 \cdot 2
        + 
        3 \cdot 3
        + 
        2 \cdot 4
        + 
        1 \cdot 4
      & 
      \\
      & 
      =
      24
  \end{aligned}
$$



#### At a $2 O$-orientifold singularity
  {#At2OSingularity}

For $G = 2 O$ the [[binary octahedral group]] (whose [[order of a group|order]] is ${\vert 2O \vert} = 48$), the [[character of a linear representation|characters]]/[[D-brane charges]] of the elementary [[virtual representation|virtual]] [[permutation representations]]/[[fractional D-branes]] are ([BSS 18, 4.9](#BurtonSatiSchreiber18)):

| $[H] = $ | $\left[\langle e\rangle\right]$ | $\left[\langle g_1\rangle\right]$ |  $\left[\langle g_2\rangle\right]$ | $\left[\langle g_3\rangle\right]$ | $\left[\langle g_4\rangle\right]$ | $\left[\langle g_5\rangle\right]$ |  $\left[\langle g_6\rangle\right]$ | $\left[\langle g_7\rangle\right]$ |
|--|--|--|--|--|--|--|--|--|
| $\chi_{V_1} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_2} =$ | $\phantom{-}1$ |  $\phantom{-}1$ |  $\phantom{-}1$ | $\phantom{-}1$ |  $-1$ | $\phantom{-}1$ | $-1$ | $-1$ |
| $\chi_{V_3} =$ | $\phantom{-}2$ |  $\phantom{-}2$ |  $-1$ | $\phantom{-}2$ |  $\phantom{-}0$ | $-1$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_4} =$ | $\phantom{-}3$ |  $\phantom{-}3$ |  $\phantom{-}0$ | $-1$ |  $\phantom{-}1$ | $\phantom{-}0$ | $-1$ | $-1$ |
| $\chi_{V_5} =$ | $\phantom{-}3$ |  $\phantom{-}3$ |  $\phantom{-}0$ | $-1$ |  $-1$ | $\phantom{-}0$ | $\phantom{-}1$ | $\phantom{-}1$ |
| $\chi_{V_6} =$ | $\phantom{-}8$ |  $-8$ |  $\phantom{-}2$ | $\phantom{-}0$ |  $\phantom{-}0$ | $-2$ | $\phantom{-}0$ | $\phantom{-}0$ |
| $\chi_{V_7} =$ | $\phantom{-}8$ |  $-8$ |  $-4$ | $\phantom{-}0$ |  $\phantom{-}0$ | $\phantom{-}4$ | $\phantom{-}0$ | $\phantom{-}0$ |



One sees by not so immediate inspection, that the general solution to the (homogenous part of the) tadpole cancellation condition (eq:VanishingOfCharacterValuesOnNontrivialSubgroups) for $G = 2O$ is

$$
  V 
  \;=\;
  n
  \Big(
    1 \cdot V_1
    + 
    1 \cdot V_2
    + 
    2 \cdot V_3
    + 
    3 \cdot V_4
    + 
    3 \cdot V_5 
    + 
    2 \cdot V_6 
    + 
    1 \cdot V_7 
  \Big)
  \,,
  \phantom{AAA}
  n \in \mathbb{Z}
$$


whose minimal [[positive number|positive]] [[mass]] (net brane number) is

$$
  \begin{aligned}
    M_{2O}
      & =
    dim(V) 
    \\
      & =
    \chi_V([\langle e\rangle]) 
    \\
      & =
      1 \cdot 1
      + 
      1 \cdot 1
      + 
      2 \cdot 2
      + 
      3 \cdot 3
      + 
      3 \cdot 3
      + 
      2 \cdot 8
      + 
      1 \cdot 8
      & 
      \\
      & 
      =
      48
  \end{aligned}
$$



## References

The issue was first highlighted in

* {#Sagnotti88} [[Augusto Sagnotti]], _Open strings and their symmetry groups_ in G. Mack et. al. (eds.) Cargese ’87, "Non-perturbative Quantum Field Theory,"  (Pergamon Press, 1988) p. 521 ([arXiv:hep-th/0208020](https://arxiv.org/abs/hep-th/0208020))

The argument is recalled in

* {#SimonPolchinski96} Eric G. Gimon, [[Joseph Polchinski]], section 3 of _Consistency Conditions for Orientifolds and D-Manifolds_, Phys.Rev.D54:1667-1676, 1996 ([arXiv:hep-th/9601038](https://arxiv.org/abs/hep-th/9601038))

Details are in 

* {#Witten12} [[Edward Witten]], section 9.3 of _Superstring Perturbation Theory Revisited_ ([arXiv:1209.5461](https://arxiv.org/abs/1209.5461))

Textbook accounts include

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 4.4 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge 2012

* [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], section 9.4 of _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics pp 585-639 Springer 2013


Quick illustrations include:


* [slide 18 here](http://www2.kek.jp/theory-center/project/string2higgsflavor/wp-content/uploads/2016/08/part-2.pdf)

Critical outlook in

* {#Moore14} [[Gregory Moore]] p. 21-22 of _[[Physical Mathematics and the Future]]_, talk at [Strings 2014](http://physics.princeton.edu/strings2014/) ([talk slides](http://physics.princeton.edu/strings2014/slides/Moore.pdf), [companion text pdf](http://www.physics.rutgers.edu/~gmoore/PhysicalMathematicsAndFuture.pdf), [[MooreVisionTalk2014.pdf:file]])



See also

* {#ABIU99} G. Aldazabal, D. Badagnani, [[Luis Ibáñez]], [[Angel Uranga]], _Tadpole versus anomaly cancellation in $D=4,6$ compact IIB orientifolds_, JHEP 9906:031, 1999 ([arXiv:hep-th/9904071](https://arxiv.org/abs/hep-th/9904071))

* {#Uranga00} [[Angel Uranga]], _D-brane probes, RR tadpole cancellation and K-theory charge_, Nucl.Phys.B598:225-246, 2001 ([arXiv:hep-th/0011048](https://arxiv.org/abs/hep-th/0011048))

* {#Honecker02} Gabriele Honecker, _Intersecting brane world models from D8-branes on $(T^2 \times T^4\mathbb{Z}_3)/\Omega\mathcal{R}_1$ type IIA orientifolds_, JHEP 0201 (2002) 025 ([arXiv:hep-th/0201037](https://arxiv.org/abs/hep-th/0201037))

* {#GarciaUranga05} Inaki Garcia-Etxebarria, [[Angel Uranga]], _From F/M-theory to K-theory and back_, JHEP 0602:008, 2006 ([arXiv:hep-th/0510073](https://arxiv.org/abs/hep-th/0510073))

* {#Marchesano03} [[Fernando Marchesano]], section 4 of _Intersecting D-brane Models_ ([arXiv:hep-th/0307252](https://arxiv.org/abs/hep-th/0307252))

* {#MaidenShiuStefanski06} John Maiden, Gary Shiu, [[Bogdan Stefanski]], _D-brane Spectrum and K-theory Constraints of D=4, N=1 Orientifolds_, JHEP0604:052,2006 ([arXiv:hep-th/0602038](https://arxiv.org/abs/hep-th/0602038))

The character tables for [[virtual representation|virtual]] [[permutation representations]] above are taken from

* {#BurtonSatiSchreiber18} [[Simon Burton]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The image of the Burnside ring in the Representation ring|The image of the Burnside ring in the Representation ring -- for binary Platonic groups]]_ ([arXiv:1812.09679](https://arxiv.org/abs/1812.09679), [Python code](https://arxiv.org/src/1812.09679v1/anc))


[[!redirects RR-field tadpole cancellations]]

[[!redirects RR-tadpole cancellation]]
[[!redirects RR-tadpole cancellations]]

[[!redirects tadpole cancellation]]
[[!redirects tadpole cancellations]]


[[!redirects RR-field tadpole]]
[[!redirects RR-field tadpoles]]

[[!redirects RR-tadpole]]
[[!redirects RR-tadpoles]]

[[!redirects tadpole]]
[[!redirects tadpoles]]

[[!redirects RR-field tadpole anomaly]]

