
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The [[spin group]] in [[dimension]] $n = 7$.

\linebreak

## Properties

### Subgroups and Supgroups

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

([Varadarajan 01, Theorem 5 on p. 6](#Varadarajan01))


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

and the right vertical inclusion $\iota'$ is the one of the two non-standard inclusions, according to Prop. \ref{Spin7SubgroupsInSpin8}.

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



\linebreak


### Coset spaces

+-- {: .num_prop #QuotientOfSpin7ByG2IsS7}
###### Proposition
**([[coset space]] of [[Spin(7)]] by [[G₂]] is [[7-sphere]])**

Consider the canonical [[action]] of [[Spin(7)]] on the [[unit sphere]] in $\mathbb{R}^8$ (the [[7-sphere]]),

1. This action is is [[transitive action|transitive]];

1. the [[stabilizer group]] of any point on $S^7$ is [[G₂]];

1. all [[G₂]]-subgroups of [[Spin(7)]] arise this way, and are all [[conjugate subgroup|conjugate]] to each other.

Hence the [[coset space]] of [[Spin(7)]] by [[G₂]] is the [[7-sphere]]

$$
  Spin(7)/G_2 \;\simeq\; S^7
  \,.
$$

=--

(e.g [Varadarajan 01, Theorem 3](#Varadarajan01))


[[!include coset space structure on n-spheres -- table]]

\linebreak

### $G$-Structure and exceptional geometry

[[!include Spin(8)-subgroups and reductions -- table]]

### Homotopy groups

$\pi_1$ | $\pi_2$ | $\pi_3$ | $\pi_4$ | $\pi_5$ | $\pi_6$ | $\pi_7$ | $\pi_8$ | $\pi_9$ | $\pi_10$ | $\pi_11$ | $\pi_12$ | $\pi_13$ | $\pi_14$ | $\pi_15$ | $\pi_16$ | $\pi_17$ |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $0$ | $0$ | $\mathbb{Z}$ | $0$ | $0$ | $0$ | $\mathbb{Z}$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_8$ | $\mathbb{Z}\oplus\mathbb{Z}_2$ | $0$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2560\oplus\mathbb{Z}_8\oplus\mathbb{Z}_2$ | $\mathbb{Z}_2^4$ | $\mathbb{Z}_2^7$ | $\mathbb{Z}_8^2\oplus\mathbb{Z}_2^2$

$\pi_18$ | $\pi_19$ | $\pi_20$ | $\pi_21$ | $\pi_22$ |
|--|--|--|--|--|
$\mathbb{Z}_945\oplus\mathbb{Z}_16\oplus\mathbb{Z}_8\oplus\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_24\oplus\mathbb{Z}_4$ | $\mathbb{Z}_10395\oplus\mathbb{Z}_8^2\oplus\mathbb{Z}_2^4$

([Mimura 67](#Mimura67))

## Related concepts

[[!include low dimensional rotation groups -- table]]

[[!include special holonomy table]]

## References

* {#Mimura67} [[Mamoru Mimura]], _The Homotopy groups of Lie groups of low rank_, Math. Kyoto Univ. Volume 6, Number 2 (1967), 131-176. ([Euclid](http://projecteuclid.org/euclid.kjm/1250524375))

* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993

* {#Varadarajan01} [[Veeravalli Varadarajan]], _Spin(7)-subgroups of SO(8) and Spin(8)_, Expositiones Mathematicae Volume 19, Issue 2, 2001, Pages 163-177 (<a href="https://doi.org/10.1016/S0723-0869(01)80027-X">doi:10.1016/S0723-0869(01)80027-X</a>, [pdf](https://core.ac.uk/download/pdf/81114499.pdf))

[[!redirects Spin7]]