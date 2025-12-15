

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Among all [[special orthogonal groups]] $SO(n)$, the case of $SO(8)$ is special, since in the [[ADE classification]] of [[simple Lie groups]] it corresponds to [[D4]], which makes its [[representation theory]] enjoy _[[triality]]_.

## Properties

### Subgroup lattice
 {#SubgroupLattice}

+-- {: .num_prop #Spin7SubgroupsInSpin8}
###### Proposition
**([[Spin(7)]]-[[subgroups]] in [[Spin(8)]])

There are precisely 3 [[conjugacy classes of subgroups|conjugacy classes]] of [[Spin(7)]]-[[subgroups]] inside [[Spin(8)]], and the [[triality]] group $Out(Spin(8))$ [[action|acts]] [[transitive action|transitively]] on these three classes. 

\begin{center}
  \begin{xymatrix}
      \mathrm{Spin}(7)
      \ar@{^{(}->}[dr]^{\iota'}
      \\
      & \mathrm{Spin}(8)
      & 
      \mathrm{Spin}(7)
      \ar@{_{(}->}[l]^-{\iota}
      \\
      \mathrm{Spin}(7)
      \ar@{^{(}->}[ur]_-{ \iota'' }
  \end{xymatrix}
\end{center}


=--

([Varadarajan 01, Theorem 5 on p. 6](#Varadarajan01), see also [Kollross 02, Prop. 3.3 (1)](#Kollross02))


+-- {: .num_prop #G2IsIntersectionOfSpin7SubgroupsInSpin8}
###### Proposition
**([[G₂]] is [[intersection]] of [[Spin(7)]]-[[subgroups]] of [[Spin(8)]])**

The [[intersection]] inside [[Spin(8)]] of any two [[Spin(7)]]-subgroups from distinct [[conjugacy classes of subgroups]] (according to Prop. \ref{Spin7SubgroupsInSpin8})
is the [[exceptional Lie group]] [[G₂]], hence we have [[pullback squares]] of the form

\begin{center}
\begin{xymatrix}
  G_2 
   \ar@{^{(}->}[r]
   \ar@{^{(}->}[d]
  & 
  \mathrm{Spin}(7)
  \ar@{^{(}->}[d]^-{\iota^\prime}
  \\
  \mathrm{Spin}(7)
   \ar@{^{(}->}[r]_-{\iota}
  & 
  \mathrm{Spin}(8)
 \end{xymatrix}
\end{center}

=--

([Varadarajan 01, Theorem 5 on p. 13](#Varadarajan01))

+-- {: .num_prop }
###### Proposition

We have the following [[commuting diagram]] of [[subgroup]] inclusions, where each [[square]] exhibits a [[pullback]]/[[fiber product]], hence an [[intersection]] of subgroups:

\begin{center}
\begin{xymatrix}
    \mathrm{SU}(2)
    \ar@{^{(}->}[r]
    \ar@{^{(}->}[d]
    \ar@{}[dr]|-{
      \mbox{
        \tiny
        (pb)
      }
    }
    &
    \mathrm{SU}(3)
    \ar@{^{(}->}[r]
    \ar@{^{(}->}[d]
    \ar@{}[dr]|-{
      \mbox{
        \tiny
        (pb)
      }
    }
    &
    \mathrm{G}_2
    \ar@{^{(}->}[r]
    \ar@{^{(}->}[d]
    \ar@{}[dr]|-{
      \mbox{
        \tiny
        (pb)
      }
    }
    &
    \mathrm{Spin}(7)
    \ar@{^{(}->}[d]^{\iota'}
    \\
    \mathrm{Spin}(5)
    \ar@{^{(}->}[r]
    &
    \mathrm{Spin}(6)
    \ar@{^{(}->}[r]
    &
    \mathrm{Spin}(7)
    \ar@{^{(}->}[r]_-{\iota}
    &
    \mathrm{Spin}(8)
\end{xymatrix}
\end{center}

Here in the bottom row we have the [[Lie groups]]

[[Spin(5)]] $\hookrightarrow$ [[Spin(6)]] $\hookrightarrow$ [[Spin(7)]] $\hookrightarrow$ [[Spin(8)]] 

with their canonical [[subgroup]]-inclusions, while in the top row we have 

[[SU(2)]] $\hookrightarrow$ [[SU(3)]] $\hookrightarrow$ [[G₂]] $\hookrightarrow$ [[Spin(7)]]

and the right vertical inclusion $\iota'$ is one of the two non-standard inclusions, according to Prop. \ref{Spin7SubgroupsInSpin8}.

=--


+-- {: .proof}
###### Proof

The square on the right is that from Prop. \ref{G2IsIntersectionOfSpin7SubgroupsInSpin8}.

The square in the middle is [Varadarajan 01, Lemma 9 on p. 10](#Varadarajan01).

The statement also follows with
[Onishchik 93, Table 2, p. 144](#Onishchik93):

\begin{center}
\begin{imagefromfile}
  "file_name": "SO8SubgroupIntersection.jpg",
  "width": 690
\end{imagefromfile}
\end{center}

=--


+-- {: .num_prop #Spin3DotSpin5SubgroupsInSO8}
###### Proposition
**([[Spin(5).Spin(3)]]-[[subgroups]] in [[SO(8)]])

The [[direct product group]] [[SO(3)]] $\times$ [[SO(5)]] together with the groups [[Sp(2).Sp(1)]] and $Sp(1) \cdot Sp(2)$, with their canonical inclusions into [[SO(8)]], form 3 [[conjugacy classes of subgroups|conjugacy classes]] of [[subgroups]] inside [[SO(8)]], and the [[triality]] group $Out(Spin(8))$ [[action|acts]] [[transitive action|transitively]] on these three classes. 

\begin{center}
  \begin{xymatrix}
      Sp(2)\cdot Sp(1)
      \ar@{^{(}->}[dr]^{\iota'}
      \\
      & 
      SO(8)
      & 
      SO(3) \times SO(5)
      \ar@{_{(}->}[l]^-{\iota}
      \\
      Sp(1) \cdot Sp(2)
      \ar@{^{(}->}[ur]_-{ \iota'' }
  \end{xymatrix}
\end{center}


=--

([Kollross 02, Prop. 3.3 (3)](#Kollross02))

Similarly:

+-- {: .num_prop #Spin3DotSpin5SubgroupsInSpin8}
###### Proposition
**([[Spin(5).Spin(3)]]-[[subgroups]] in [[Spin(8)]])

The groups [[Spin(5).Spin(3)]], [[Sp(2).Sp(1)]] and $Sp(1) \cdot Sp(2)$, with their canonical inclusions into [[Spin(8)]], form 3 [[conjugacy classes of subgroups|conjugacy classes]] of [[subgroups]] inside [[Spin(8)]], and the [[triality]] group $Out(Spin(8))$ [[action|acts]] [[transitive action|transitively]] on these three classes. 

\begin{center}
  \begin{xymatrix}
      Sp(2)\cdot Sp(1)
      \ar@{^{(}->}[dr]^{\iota'}
      \\
      & 
      Spin(8)
      & 
      Spin(3) \cdot Spin(5)
      \ar@{_{(}->}[l]^-{\iota}
      \\
      Sp(1) \cdot Sp(2)
      \ar@{^{(}->}[ur]_-{ \iota'' }
  \end{xymatrix}
\end{center}


=--

([Čadek-Vanžura 97, Sec. 2](#CadekVanzura97))

{#Sp2DotSp1SubgroupInclusionsInSummary} In summary we have these subgroup inclusions

\begin{xymatrix}
    \mathrm{Sp}(1) {\cdot} \mathrm{Sp}(2)
    \ar@{=}[dddddr]
    \ar@{_{(}->}[ddrr]|-{ \iota' }
    \\
    \\
    &&
    \mathrm{Spin}(8)
    \ar@{->>}[dddddr]
    &&
    \mathrm{Spin}(3) {\cdot} \mathrm{Spin}(5)
    \ar@{->>}[dddddr]
    \ar@{_{(}->}[ll]|-{\iota}
    \\
    \\
    \mathrm{Sp}(2) {\cdot} \mathrm{Sp}(1)
     \ar@{=}[dddddr]
     \ar@{^{(}->}[uurr]
       |<<<<<<<<<<<<<<<<<<<<<<<<<<{ \phantom{AA \atop AA} }
       |>>>>>>>>>>>>>>>>>>>>>>>{ \iota'' }
    \\
    &
    \mathrm{Sp}(1) {\cdot} \mathrm{Sp}(2)
    \ar@{_{(}->}[ddrr]|-{ \iota' }
    \\
    \\
    &&& 
    \mathrm{SO}(8)
    &&
    \mathrm{SO}(3) \times \mathrm{SO}(5)
    \ar@{_{(}->}[ll]|-{\iota}
    \\
    \\
    &
    \mathrm{Sp}(2) {\cdot} \mathrm{Sp}(1)
    \ar@{^{(}->}[uurr]|-{ \iota'' }
\end{xymatrix}

permuted by triality:


\begin{center}
\begin{imagefromfile}
  "file_name": "TrialityOnSp2Sp1.jpg",
  "width": 680
\end{imagefromfile}
\end{center}

> graphics grabbed from [FSS 19, Sec. 3.3](#FSS19)

\linebreak


### Homotopy groups


The [[homotopy groups]] of $SO(8)$ in [[low-dimensional topology|low degrees]]:

| $G$ | $\pi_1$ | $\pi_2$ | $\pi_3$ | $\pi_4$ | $\pi_5$ | $\pi_6$ | $\pi_7$ | $\pi_8$ | $\pi_9$ | $\pi_10$ | $\pi_11$ | $\pi_12$ | $\pi_13$ | $\pi_14$ | $\pi_15$ |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $SO(8)$ | $\mathbb{Z}_2$ | $0$ | $\mathbb{Z}$ | $0$ | $0$ | $0$ | $\mathbb{Z}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 3}$ | $\mathbb{Z}_{2}^{\oplus 3}$ | $\mathbb{Z}_{8} \oplus \mathbb{Z}_{24}$ | $\mathbb{Z}_2 \oplus \mathbb{Z}$ | 0 | $\mathbb{Z}^{\oplus 2}$ | $\mathbb{Z}_2\oplus\mathbb{Z}_8\oplus\mathbb{Z}_{120}\oplus\mathbb{Z}_{2520}$ | $\mathbb{Z}_2^{\oplus 7}$ |

\linebreak

### Cohomology of classifying spaces

+-- {: .num_prop #CohomologyRingOfSpin8}
###### Proposition

The [[ordinary cohomology|ordinary]] [[cohomology ring]] of the [[classifying space]] $B Spin(8)$ is:

**1)** with [[coefficients]] in the [[cyclic group of order 2]]:

$$
  H^\bullet
  \big(
    B Spin(8), \mathbb{Z}_2
  \big)
  \;\simeq\;
  \mathbb{Z}
  \big[
    w_4, w_6, w_7, w_8, 
    \;
    \rho_2
    \left(
    \tfrac{1}{4}
    \left(
      p_2
      -
      \big(\tfrac{1}{2}p_1\big)^2
      -
      2 \chi
    \right)
    \right)
  \big]
$$

where $w_i$ are the [[universal characteristic class|universal]] [[Stiefel-Whitney classes]], 

and where 

$$
  \rho_2 \;\colon\; H^\bullet(B Spin(8), \mathbb{Z}) \to H^\bullet(B Spin(8), \mathbb{Z}_2)
$$ 

is [[cyclic group|mod 2 reduction]]

**2)** with [[coefficients]] in the [[integers]]:

$$
  H^\bullet
  \big(
    B Spin(8), \mathbb{Z}
  \big)
  \;\simeq\;
  \mathbb{Z}
  \Big[
    \tfrac{1}{2}p_1,
    \;
    \tfrac{1}{4}
    \left(
      p_2
      -
      \big(\tfrac{1}{2}p_1\big)^2
    \right)
    -
    \tfrac{1}{2}\chi
    ,
    \;
    \chi,
    \;
    \beta(w_6)
  \Big]
  /
  \big\langle 2 \beta(w_6)\big\rangle
  \,,
$$

where $p_1$ is the [[first fractional Pontryagin class]], $p_2$ is the [[second Pontryagin class]], $\chi$ is the [[Euler class]], and

$$
  \beta
  \;\colon\;
  H^\bullet
  \big(
    B Spin(8),
    \mathbb{Z}_2
  \big)
  \longrightarrow
  H^{\bullet + 1}
  \big(
    B Spin(8),
    \mathbb{Z}
  \big)
$$

is the [[Bockstein homomorphism]].

Moreover, we have the following relations:

$$
  \begin{aligned}
    \rho_2\left(
      \tfrac{1}{2}p_1
    \right)  
    & = 
    w_4
    \\
    \rho_2\big( \chi\big) 
    & =
    w_8
  \end{aligned}
$$

=--

This is due to [Quillen 71](#Quillen71), [Čadek-Vanžura 95](#CadekVanzura95), see [Čadek-Vanžura 97, Lemma 4.1](#CadekVanzura97).



+-- {: .num_prop}
###### Proposition

Consider the [[looping and delooping|delooping]] of the [[triality]] automorphism relating [[Sp(2).Sp(1)]] with [[Spin(5).Spin(3)]] (Prop. \ref{Spin3DotSpin5SubgroupsInSpin8}) on [[classifying spaces]]

$$
  \array{
    B 
    \big(
      Spin(5) \cdot Spin(3)
    \big)
    &\hookrightarrow&
    B Spin(8)
    \\
    \big\downarrow
    &&
    \big\downarrow^{ B \mathrlap{tri} }
    \\
    B 
    \big(
      Sp(2) \cdot Sp(1)
    \big)
    &\hookrightarrow&
    B Spin(8)    
  }
$$

Then the pullback of the [[universal characteristic classes]] of $B Spin(8)$ (from Prop. \ref{CohomologyRingOfSpin8}) along $B tri$ is as follows:

$$
  \big(
    B tri
  \big)^\ast
  \;\colon\;
  \begin{aligned}
    \tfrac{1}{2} p_1 & \mapsto \tfrac{1}{2} p_1
    \\
    \chi 
      & \mapsto 
      -
      \tfrac{1}{4}
      \big(
        p_2 
        - \big(\tfrac{1}{2}p_1\big)^2
      \big)
      + 
      \tfrac{1}{2}\chi
    \\
      \tfrac{1}{4}
      \big(
        p_2 
        - 
        \big(\tfrac{1}{2}p_1\big)^2
      \big)
      - 
      \tfrac{1}{2}\chi
    & \mapsto 
      -
      \chi
  \end{aligned}
$$

=--

([Čadek-Vanžura 97, Lemma 4.2](#CadekVanzura97))

In fact $tri^{-1} = tri$.


Hence, in rational cohomology:

$$
  \begin{aligned}
    \big(
      B tri
    \big)^\ast
    \big(
      \tfrac{1}{4}p_2
    \big) 
    & =
    \big(
      B tri
    \big)^\ast
    \Big(
      \big(
        \tfrac{1}{4}p_2 
        - \big(\tfrac{1}{4}p_1\big)^2
        - \tfrac{1}{2}\chi
      \big)
      + \big(\tfrac{1}{4}p_1\big)^2
      + \tfrac{1}{2}\chi
    \Big) 
    \\
    & =
    -\chi
    + 
    \big(\tfrac{1}{4}p_1\big)^2
    -
    \tfrac{1}{2}
    \big(
      \tfrac{1}{4}p_2 
      - \big(\tfrac{1}{4}p_1\big)^2
      - \tfrac{1}{2}\chi
    \big)
  \end{aligned}
$$

\linebreak

### $G$-Structure and exceptional geometry

[[!include Spin(8)-subgroups and reductions -- table]]

\linebreak

### Octonionic construction of representations

The group $Spin(8)$ has three 8-dimensional irreducible real representations: the right- and left-handed spinor representations $S_+$ and $S_-$, and the vector representation $V$, which factors through $SO(8)$.   ([Bryant 20](#Bryant20)) gives a unified construction of all three representations using [[octonions]], as follows.   

For $x \in \mathbb{O}$ define a linear map $m_x \colon \mathbb{O}^2 \to \mathbb{O}^2$ as follows:

$$ m_x = \left( \begin{array}{cc} 0 & C R_x \\ -C L_x & 0  \end{array}   \right) $$

where $L_x, R_x, C \colon \mathbb{O} \to \mathbb{O}$ are left multiplication by $x$, right multiplication by $x$ and octonionic conjugation, respectively.  Since $m_x^2 = -{|x|}^2$ this map induces an action of the Clifford algebra $Cliff(\mathbb{O})$ on $\mathbb{O}^2$.  (To be precise, this is Clifford algebra generated by 8 anticommuting square roots of *minus* 1).  One can show that this action gives an isomorphism of real associative algebras

$$ Cliff(\mathbb{O}) \cong End(\mathbb{O}^2) $$

where $End(\mathbb{O}^2)$, the algebra of all real-linear transformations of $\mathbb{O}^2$, is isomorphic to the algebra of $16 \times 16$ real matrices.

The group $Spin(8)$ is isomorphic to the group of linear transformations generated by products $m_x m_y$ where $x, y \in \mathbb{O}$ have ${|x|} = {|y|} = 1$.  This group is also generated by elements

$$  \left( \begin{array}{cc} L_u & 0 \\ 0 & R_u \end{array}   \right) $$

where $u \in \mathbb{O}$ has ${|u|} = 1$.  In this sense we may say $Spin(8)$ is generated by unit octonions $u$, though octonion multiplication is not itself associative.

It follows that $\mathbb{O}^2$ splits, as a representation of $Spin(8)$, into two summands isomorphic to $\mathbb{O}$.  These are the two spinor representations of $Spin(8)$.  To match standard conventions Bryant calls the first summand, on which $u$ acts as $L_u$, the spinor representation $S_-$, and the second, on which $u$ acts as $R_u$, the spinor representation $S_+$.  The vector representation of $Spin(8)$ can also be identified with $\mathbb{O}$, with $u$ acting as $L_u R_u$.

Bryant also describes the intertwiners $V \otimes S_{\pm} \to S_{\mp}$ and the triality automorphisms of $Spin(8)$ in these terms.

## Related concepts

* [[principal SO(8)-bundle]]

[[!include low dimensional rotation groups -- table]]

\linebreak

## References

### General

* {#Bryant20} [[Robert Bryant]], Notes on spinors in low dimension.   ([arXiv:2011.05568](https://arxiv.org/abs/2011.05568))

See also

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/SO(8)">SO(8)</a>_

### Subgroup lattice

On the [[subgroup lattice]] of [[Spin(8)]]

* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993

* {#Varadarajan01} [[Veeravalli Varadarajan]], _Spin(7)-subgroups of SO(8) and Spin(8)_, Expositiones Mathematicae Volume 19, Issue 2, 2001, Pages 163-177 (<a href="https://doi.org/10.1016/S0723-0869(01)80027-X">doi:10.1016/S0723-0869(01)80027-X</a>, [pdf](https://core.ac.uk/download/pdf/81114499.pdf))

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))


* Megan M. Kerr, _New examples of homogeneous Einstein metrics_, Michigan Math. J. Volume 45, Issue 1 (1998), 115-134 ([euclid:1030132086](https://projecteuclid.org/euclid.mmj/1030132086))

* {#Kollross02} Andreas Kollross, Prop. 3.3 of _A Classification of Hyperpolar and Cohomogeneity One Actions_, Transactions of the American Mathematical Society Vol. 354, No. 2 (Feb., 2002), pp. 571-612 ([jstor:2693761](https://www.jstor.org/stable/2693761))

Discussion with an eye towards foundations of [[M-theory]]:

* {#FSS19} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))


### Cohomology

The [[integral cohomology]] of the [[classifying spaces]] [[BSO(n)|$B SO(8)$]] and $B Spin(8)$ and the [[action]] of [[triality]] on these is discussed in


* {#GrayGreen70} [[Alfred Gray]], Paul S. Green, _Sphere transitive structures and the triality automorphism_, Pacific J. Math. Volume 34, Number 1 (1970), 83-96 ([euclid:1102976640](https://projecteuclid.org/euclid.pjm/1102976640))

* {#Quillen71} [[Daniel Quillen]], _The mod 2 cohomology rings of extra-special 2-groups and the spinor groups_, Math. Ann . 194 (1971), 19

* {#CadekVanzura95} [[Martin Čadek]], [[Jiří Vanžura]], _On the existence of 2-fields in 8-dimensional vector bundles over 8-complexes_, Commentationes Mathematicae Universitatis Carolinae, vol. 36 (1995), issue 2, pp. 377-394 ([dml-cz:118764](https://dml.cz/handle/10338.dmlcz/118764))

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], Section 2 of _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))


[[!redirects Spin(8)]]

[[!redirects SO8]]

[[!redirects Spin8]]
