
#Contents#
* table of contents
{:toc}

## Idea

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://upload.wikimedia.org/wikipedia/commons/5/59/Dynkin_diagram_D4.png" width="100"/>
</div>

The [[Dynkin diagram]]/[[Dynkin quiver]] [[D4]] has an [[symmetric group|S3]]-[[symmetry group]]

   (graphics grabbed from Wikipedia [here](https://upload.wikimedia.org/wikipedia/commons/5/59/Dynkin_diagram_D4.png))

This manifests itself in "triality" symmetries enjoyed by the objects that are labeled by [[D4]] in an [[ADE-classification]].

Specifically for the [[simple Lie group]] [[SO(8)]] corresponding to [[D4]], triality is the statement that the two [[spin representations]] of the corresponding [[spin group]] $Spin(8)$ and the defining vector representations are all [[isomorphism|isomorphic]], and in a nice way.

## Details 

### Triality of subgroups of $Spin(8)$ and $SO(8)$
 {#TrialityOfSubgroupsOfSpin8}

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
**([[G2]] is [[intersection]] of [[Spin(7)]]-[[subgroups]] of [[Spin(8)]])**

The [[intersection]] inside [[Spin(8)]] of any two [[Spin(7)]]-subgroups from distinct [[conjugacy classes of subgroups]] (according to Prop. \ref{Spin7SubgroupsInSpin8})
is the [[exceptional Lie group]] [[G2]], hence we have [[pullback squares]] of the form

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
    \ar@{^{(}->}[d]^{B \iota'}
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

[[SU(2)]] $\hookrightarrow$ [[SU(3)]] $\hookrightarrow$ [[G2]] $\hookrightarrow$ [[Spin(7)]]

and the right vertical inclusion $B \iota'$ is the [[delooping]] of one of the two non-standard inclusions, according to Prop. \ref{Spin7SubgroupsInSpin8}.

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

## References

### General

* {#SpringerVeltkamp00} [[Tonny Springer]], [[Ferdinand Veldkamp]], chapter 3 of _Octonions, Jordan Algebras, and Exceptional Groups_, Springer Monographs in Mathematics, 2000

Discussion of triality of [[subgroups]] of [[Spin(8)]] and [[SO(8)]]:

* {#Varadarajan01} [[Veeravalli Varadarajan]], _Spin(7)-subgroups of SO(8) and Spin(8)_, Expositiones Mathematicae Volume 19, Issue 2, 2001, Pages 163-177 (<a href="https://doi.org/10.1016/S0723-0869(01)80027-X">doi:10.1016/S0723-0869(01)80027-X</a>, [pdf](https://core.ac.uk/download/pdf/81114499.pdf))

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))


* Megan M. Kerr, _New examples of homogeneous Einstein metrics_, Michigan Math. J. Volume 45, Issue 1 (1998), 115-134 ([euclid:1030132086](https://projecteuclid.org/euclid.mmj/1030132086))

* {#Kollross02} Andreas Kollross, Prop. 3.3 of _A Classification of Hyperpolar and Cohomogeneity One Actions_, Transactions of the American Mathematical Society Vol. 354, No. 2 (Feb., 2002), pp. 571-612 ([jstor:2693761](https://www.jstor.org/stable/2693761))

See also

* Wikipedia, _[Triality](http://en.wikipedia.org/wiki/Triality)_

* [[John Baez]], _[Spinors and trialities](http://math.ucr.edu/home/baez/octonions/node7.html)_

### In string theory

Exposition with an eye to application in [[string theory]]:

* {#TongTurner19} [[David Tong]], Carl Turner, _Notes on 8 Majorana Fermions_ ([arXiv:1906.07199](https://arxiv.org/abs/1906.07199))

Discussion in the foundations of [[M-theory]]:

* {#FSS19} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3.3 of _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))



[[!redirects trialities]]

