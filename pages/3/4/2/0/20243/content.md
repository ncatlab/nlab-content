
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

The [[Lie group]] denoted $Sp(n).Sp(1)$ 
([Alekseevskii 68](#Alekseevskii68), [Gray 69](#Gray69))
or just $Sp(n)Sp(1)$ is the [[quotient group]] of the [[direct product group]] of the given [[quaternion unitary groups]] by their [[diagonal]] [[center]] [[cyclic group of order 2]]. 


A [[smooth manifold]] of [[dimension]] $4n$ with [[G-structure]] for this group $G = Sp(n).Sp(1)$ is a [[quaternion-Kähler manifold]].

Similarly, for $Spin(n_1)$, $Spin(n_2)$ [[spin groups]] in some dimension, the group denoted $Spin(n_1) \cdot Spin(n_2)$ or just $Spin(n_1)Spin(n_2)$ is the [[quotient group]] of the [[direct product group]] $Spin(n_1) \times Spin(n_2)$ by the [[diagonal]] [[center]] [[cyclic group of order 2]].

These products $G_1 \cdot G_2$ are examples of [[central products of groups]].

\linebreak


## Definition


+-- {: .num_defn #SpnSp1}
###### Definition

For $n \in \mathbb{N}$ with $n \geq 2$, the [[Lie group]] denoted $Sp(n).Sp(1)$ or just $Sp(n)Sp(1)$ is the [[quotient group]] of the [[direct product group]] $Sp(n) \times Sp(1)$ of [[quaternion unitary groups]] $Sp(n)$ (in particular $Sp(1) \simeq$ [[Spin(3)]]) by the [[diagonal]] [[center]] [[cyclic group of order 2]] $\mathbb{Z}_2$:

$$
  Sp(n).Sp(1)
  \;\coloneqq\;
  \big(
    Sp(n)
     \times
    Sp(1)
  \big)/_{diag}\mathbb{Z}_2
$$

hence the [[quotient group]] by the [[subgroup]]

\[
  \label{DiagonalCenter}
  \mathbb{Z}_2
  \;\simeq\;
  \big\{ 
    (1,1), (-1,-1)
  \big\}
  \hookrightarrow
  Sp(n) \times Sp(1)
  \,.
\]

=--

(e.g. [Čadek-Vanžura 97, Sec. 2](#CadekVanzura97))

A similar definition yields 

+-- {: .num_defn #Spinn1Spinn2}
###### Definition

Write

$$
  Spin(n_1) \cdot Spin(n_2)
  \;\coloneqq\;
  \big(
    Spin(n_1)
    \times 
    Spin(n_2)
  \big)/\mathbb{Z}_2
$$

for the [[quotient group]] of the [[direct product group]] of [[spin groups]] by their [[diagonal]] [[subgroup]]

$$
  \mathbb{Z}_2
  \;\simeq\;
  \big\{
    (1,1), (-1,-1)
  \big\}
  \;\hookrightarrow\;
  Spin(n_1) \times Spin(n_1)
  \,.
$$

=--

([McInnes 99a, p. 9](#McInnes99a), [Hilgert-Neeb 12, Prop. 17.3.1](#HilgertNeeb12))

Sometimes one sees the notation further generalized to include cases such as

* $Spin(n) \cdot U(1) \simeq Spin(n)\cdot Spin(2) \simeq$ [[Spin^c]],

see Example \ref{SpinnSpin2IsSpinc} below.

\linebreak

## Properties

### As the effective quotient of $Sp(n)\times Sp(1)$ acting on $\mathbb{H}^n$ 

The [[direct product group]] $Sp(n) \times Sp(1)$ has a canonical [[action]] on the [[quaternion]] [[vector space]] $\mathbb{H}^n$, where the factor [[Sp(n)]] acts as $2 \times 2$ [[quaternion unitary group|quaternion unitary]] [[matrix multiplication]] from the left, and $Sp(1)$ acts by [[diagonal]] $1 \times 1$ matrix action on each $\mathbb{H}$-summand from the right.

For instance for $n = 2$ this action controls the [[quaternionic Hopf fibration]] and its $Sp(2)$ [[equivariant function|equivariance]] (see [there](quaternionic+Hopf+fibration#EquivariantStructure)).

But this action is not an [[effective group action]]: Precisely the diagonal center (eq:DiagonalCenter) acts trivially.

There is then a [[commuting diagram]] of [[Lie groups]]

\[
  \label{CompatibilityDiagram}
  \array{
    Sp(2) \times Sp(1)
    &\longrightarrow&
    Spin(8)
    \\
    \big\downarrow && \big\downarrow
    \\
    Sp(2) \cdot Sp(1)    
    &\longrightarrow&
    SO(8)
  }
\]
with the horizontal maps being [[group homomorphisms]] to [[Spin(8)]] and [[SO(8)]], respectively, the left morphism being the defining [[quotient]] projection and the right morphism the [[double cover]] morphism that defines the [[spin group]].

(e.g. [Čadek-Vanžura 97, p. 4](#CadekVanzura97))

### Lift to $Sp(n) \times Sp(1)$

([Marchiafava-Romani 76](#MarchiafavaRomani76), [Salamon 82, around Def. 2.1](#Salamon82))

(...)

\linebreak



## Examples


### $Sp(1)\cdot Sp(1)$ is $SO(4)$
 {#SO4}

The case of $Sp(n)\cdot Sp(1)$ for $n = 1$ is special, as in this case the canonical inclusion $Sp(n)\cdot Sp(1) \hookrightarrow SO(4n)$ becomes an [[isomorphism]]

$$
  Sp(1)\cdot Sp(1)
  \;\simeq\;
  SO(4)
$$

with the [[special orthogonal group]] [[SO(4)]],
and hence the compatibility diagram (eq:CompatibilityDiagram) now exhibits at the top the [[exceptional isomorphism]] $Sp(1) \times Sp(1) \simeq $ [[Spin(4)]] (see [there](Spin4#ExceptionalIsomorphisms))

In summary:


+-- {: .num_prop }
###### Proposition

There is a [[commuting diagram]] of [[Lie groups]] of the form

$$
  \array{
    ( q_1, q_2 )
    &\mapsto&
    (x \mapsto q_1 \cdot x \cdot \overline{q}_2) 
    \\
    Sp(1) \times Sp(1) 
    &\overset{\simeq}{\longrightarrow}&
    Spin(4)
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    Sp(1)\cdot Sp(1)
    &\overset{\simeq}{\longrightarrow}&
    SO(4)
  }
$$

where

1. in the top left we have [[Sp(1)]] = [[Spin(3)]],

1. in the top right we have [[Spin(4)]],

1. in the bottom left we have [[Sp(n).Sp(1)|Sp(1).Sp(1)]]

1. in the bottom right we have [[SO(4)]]

1. the horizontal morphism assigns the [[conjugation action]] of unit [[quaternions]], as indicated,

1. the right vertical morphism is the defining [[double cover]],

1. the left vertical morphism is the defining [[quotient group]]-projection.

=--

\linebreak


### $Spin(n)\cdot Spin(2)$ is $Spin^c(n)$
  {#Spinc}

+-- {: .num_example #SpinnSpin2IsSpinc}
###### Example

For $n \in \mathbb{N}$,  group $Sp(n) \cdot Sp(2)$ in Def. \ref{Spinn1Spinn2} is the group otherwise known as [[spin^c|spin^c(n)]]:

$$
  Spin(n)\cdot Spin(2)
  \;\simeq\;
  Spin^c(n)
  \,.
$$

This is due to the identification of the [[double cover]] by [[Spin(2)]] of [[SO(2)]] with the [[real Hopf fibration]] ([this Prop](Spin2#Spin2OverSO2IsRealHopfFibration)), which identifies $Spin(2) \simeq U(1)$ compatible with the subgroupinclusion of $\mathbb{Z}_2$.


=--

(See also e.g. [Gompf 97, p. 2](#Gompf97))



### Triality
 {#Triality}

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

In summary:

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


### $Sp(1)Sp(1)Sp(1) = Spin(4)\cdot Spin(3)$
 {#Sp1Sp1Sp1}


+-- {: .num_example #Spin4Spin3}
###### Example
**([[Spin(4).Spin(3)]])**

The group

$$
  Spin(4)\cdot Spin(3)
  \;\coloneqq\;
  \big(  
    Spin(4) \times Spin(3)
  \big)/\mathbb{Z}_2
$$

is the [[quotient group]] of the [[direct product group]] of [[Spin(4)]] with [[Spin(3)]] by the [[subgroup]]

\[
  \label{Spin4Spin3DiagonalCenter}
  \mathbb{Z}_2
  \;\simeq\;
  \big\{ 
    (1,1), (-1,-1)
  \big\}
  \hookrightarrow
  Spin(4) \times Spin(3)
  \,.
\]

Due to the exception [[isomorphism]] [[Spin(4)]] $\simeq$ [[Spin(3)]] $\times$ [[Spin(3)]] ([this Prop.](Spin4#ExceptionalIsoWithSpin3TimesSpin3)) this is [[isomorphism|isomorphic]] to the [[quotient group]] of the [[direct product group|direct product]] of 3 copies of [[Sp(1)]] $\simeq$ [[Spin(3)]] with itself

$$
  Spin(4)\cdot Spin(3)
  \;\simeq\;
  Sp(1)Sp(1)Sp(1)
  \;\coloneqq\;
  \big( Spin(3) \times Spin(3) \times Spin(3)\big)/_{diag} \mathbb{Z}_2
$$

by the triple diagonal center

\[
  \label{Spin3Spin3Spin3DiagonalCenter}
  \mathbb{Z}_2
  \;\simeq\;
  \big\{ 
    (1,1,1), (-1,-1,-1)
  \big\}
  \hookrightarrow
  Spin(3) \times Spin(3) \times Spin(3)
  \,.
\]


=--

See the references [below](#ReferencesSpin4Spin3).

+-- {: .num_example}
###### Example

The [[coset space]] of [[Sp(2).Sp(1)]] (Def. \ref{SpnSp1}) by [[Sp(1)Sp(1)Sp(1)]] (Def. \ref{Spin4Spin3}) is the [[4-sphere]]:

$$
  \frac{
    Sp(2)\cdot Sp(1)
  }
  {
    Sp(1)Sp(1)Sp(1)
  }
  \;\simeq\;
  S^4
  \,.
$$

This follows essentially from the [[quaternionic Hopf fibration]] and its $Sp(2)$-[[equivariant function|equivariance]]...

=--

(e.g. [Bettiol-Mendes 15, (3.1), (3.2), (3.3)](#BettiolMendes15))


### Spin-Grassmannians
 {#SpinGrassmannians}

We have the following [[coset spaces]] of [[spin groups]] by dot-products of Spin groups as above:

$$
  Spin(7)/ \big(  Spin(4)\cdot Spin(3) \big)
  \;\simeq\;
  SO(7) / \big( SO(4) \times SO(3)  \big)
  \;\simeq\;
  Gr(4, 7)
$$

is the space of [[Cayley 4-planes]] ([[Cayley 4-form]]-[[calibrated submanifolds]] in 8d [[Euclidean space]]). This happens to also be [[homeomorphism|homeomorphic]] to just the plain [[Grassmannian]] of 4-planes in 7d (recalled e.g. in [Ornea-Piccini 00, p. 1](#OrneaPiccini00)).

Similarly,

$$
  Spin(6)/ \big(  Spin(3)\cdot Spin(3) \big)
  \;\simeq\;
  SU(6)/ SO(4) 
$$

is the Grassmannian of those [[Cayley 4-planes]] that are also [[special Lagrangian submanifolds]] ([BBMOOY 96, p. 7 (8 of 17)](Cayley+form#BBMOOY96)).


Moreover, 

$$
  Spin(8)/ \big(  Spin(5)\cdot Spin(3) \big)
  \;\simeq\;
  Gr(3, 8)
$$

is the [[Grassmannian]] of 3-planes in 8d. ([Cadek-Vanzura 97, Lemma 2.6](#CadekVanzura97)).




\linebreak




## Related concepts

[[!include low dimensional rotation groups -- table]]

 
## References
 {#References}


### $Sp(n)\cdot Sp(1)$

Very early appearances of the notation $Sp(n)\cdot Sp(1)$ are mostly in discussions of [[Berger's theorem]] for exceptional [[holonomy]]:

* {#Gray69} [[Alfred Gray]], [_A Note on Manifolds Whose Holonomy Group is a Subgroup of Sp(n) $\cdot$ Sp(1)_](https://projecteuclid.org/euclid.mmj/1029000212), Michigan Math. J. Volume 16, Issue 2 (1969), 125-128.

* {#Alekseevskii68} [[Dmitri Alekseevskii]], [_Riemannian spaces with exceptional holonomy groups_](https://link.springer.com/article/10.1007%2FBF01075943), Functional Analalysis and its Applications (1968) 2: 97.

However, the even earlier paper:

* Joseph Wolff, _Complex homogeneous contact manifolds and quaternionic symmetric spaces_, Journal of Mathematics and Mechanics, vol. 14 (1965), pp. 1033-1048.

describes this construction as a "local [[direct product]]" of [[topological groups]] and applies it to the classification of [[quaternionic manifolds]]. The notation in the classical paper of [Bonan](#) for this group is $V_{4n} [Sp(n) \otimes_\mathbf{H} Sp(1)]$. 

Of early algebraic interest is the structure theory article:

* Stefano Marchiafava, Giuliano Romani, _Sul classificante del gruppo $Sp(n) \cdot Sp(1)$_, Annali di Matematica Pura ed Applicata December 1976, Volume 110, Issue 1, pp 295–319 ([doi:10.1007/BF02418010](https://doi.org/10.1007/BF02418010))

More on the [[cohomology]] of $Sp(n)\cdot Sp(1)$ and its [[classifying space]]:

* Stefano Marchiafava, Giuliano Romani, _Alcune osservazioni sui sottogruppi abeliani del gruppo $Sp(n)\cdot Sp(1)$_, Annali di Matematica 1977 ([doi:10.1007/BF02413792](https://doi.org/10.1007/BF02413792))

* [[Paolo Piccinni]], Giuliano Romani, _A generalization of symplectic Pontrjagin classes to vector bundles with structure group $Sp(n)\cdot Sp(1)$_,  Annali di Matematica pura ed applicata (1983) 133: 1 ([doi:10.1007/BF01766008](https://doi.org/10.1007/BF01766008))


* [[Paolo Piccinni]], _Vector fields and characteristic numbers on hyperkàhler and quaternion Kâhler manifolds_, Atti della Accademia Nazionale dei Lincei. Classe di Scienze Fisiche, Matematiche e Naturali. Rendiconti Lincei. Matematica e Applicazioni (1992) Volume: 3, Issue: 4, page 295-298 ([dml:244204](https://eudml.org/doc/244204))

* [[Dmitri Alekseevskii]] S. Marchiafava, _Quaternionic structures on a manifold and subordinated structures_, Annali di Matematica pura ed applicata (1996) 171: 205 ([doi:10.1007/BF01759388](https://doi.org/10.1007/BF01759388))

Discussion of the lift to $Sp(n) \times Sp(1)$ appears in 

* {#MarchiafavaRomani76} S. Marchiafava, G. Romani, _Sui fibrati con struttura quaternionale generalizzata_, Ann. Mat. Pura Appl. (IV) CVII, 131-157 (1976) ([doi:10.1007/BF02416470](https://doi.org/10.1007/BF02416470))

* {#Salamon82} [[Simon Salamon]], around Def. 2.1 in _Quaternionic Kähler manifolds_, Invent Math (1982) 67: 143. ([doi:10.1007/BF01393378](https://doi.org/10.1007/BF01393378))

### $Sp(2)\cdot Sp(1)$
 {#ReferencesSp2Sp1}

Articles dealing specifically with the group $Sp(2)\cdot Sp(1)$:

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], Section 2 of _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))

* {#CadekVanzura98b} [[Martin Čadek]], [[Jiří Vanžura]], _Almost quaternionic structures on eight-manifolds_, Osaka J. Math. Volume 35, Number 1 (1998), 165-190 ([euclid:1200787905](https://projecteuclid.org/euclid.ojm/1200787905))

* {#Kollross02} Andreas Kollross, Prop. 3.3 of _A Classification of Hyperpolar and Cohomogeneity One Actions_, Transactions of the American Mathematical Society Vol. 354, No. 2 (Feb., 2002), pp. 571-612 ([jstor:2693761](https://www.jstor.org/stable/2693761))


See also the references at _[[quaternion-Kähler manifold]]_.

### $Spin(n_1)\cdot Spin(n_2)$

A textbook occurrence of dot notation for general spin groups, $Spin(n_1)\cdot Spin(n_2)$, appears in

* {#HilgertNeeb12} Joachim Hilgert, [[Karl-Hermann Neeb]], Prop. 17.3.1 _Structure and Geometry of Lie Groups_, Springer Monographs in Mathematics, Springer-Verlag New York, 2012 ([doi:10.1007/978-0-387-84794-8](https://link.springer.com/book/10.1007/978-0-387-84794-8))


The identification of $Spin \dot Spin(2)$ with [[Spin^c]] appears for instance in

* {#Gompf97} [[Robert Gompf]], _$Spin^c$ structures and homotopy equivalences_, Geom. Topol. 1 (1997) 41-50 ([arXiv:math/9705218](https://arxiv.org/abs/math/9705218))

Discussion of central product spin groups as [[subgroups]] of [[semi-spin groups]] (motivated by analysis of the [[gauge groups]] and [[Green-Schwarz anomaly cancellation]] of [[heterotic string theory]]) is in

* {#McInnes99a} [[Brett McInnes]], p. 9 of _The Semispin Groups in String Theory_, J. Math. Phys. 40:4699-4712, 1999 ([arXiv:hep-th/9906059](https://arxiv.org/abs/hep-th/9906059))

* {#McInnes99b} [[Brett McInnes]], _Gauge Spinors and String Duality_,  Nucl. Phys. B577:439-460, 2000 ([arXiv:hep-th/9910100](https://arxiv.org/abs/hep-th/9910100))

As such these also appear as [[U-duality groups]] and their [[subgroups]], e.g.

* [[Arjan Keurentjes]], p. 10 of _The topology of U-duality (sub-)groups_, Class.Quant.Grav. 21 (2004) 1695-1708 ([arXiv:hep-th/0309106](https://arxiv.org/abs/hep-th/0309106))


### $Sp(1)Sp(1)Sp(1) \simeq Spin(4)\cdot Spin(3) $
 {#ReferencesSpin4Spin3}

The group $Spin(4)\cdot Spin(3) \simeq (Spin(3))^3/_{diag} \mathbb{Z}_2$ (Example \ref{Spin4Spin3}) is discussed in the following, largely in describing the Grassmannian of [[Cayley 4-planes]], see [there](Cayley+form#GrassmannianOfCayley4Planes):

* Wu-Chung Hsiang, Wu-Yi Hsiang, Tables A of _Differentiable Actions of Compact Connected Classical Groups: II_, Annals of Mathematics
Second Series, Vol. 92, No. 2 (1970), pp. 189-223 ([jstor:1970834](https://www.jstor.org/stable/1970834))

* {#HarveyLawson82} [[Reese Harvey]], [[H. Blaine Lawson]], theorem 1.38 of _Calibrated geometries_, Acta Math. Volume 148 (1982), 47-157 ([Euclid:1485890157](https://projecteuclid.org/euclid.acta/1485890157))

* {#BryantHarvey89} [[Robert Bryant]], [[Reese Harvey]], (3.19) in _Submanifolds in Hyper-Kähler Geometry_, Journal of the American Mathematical Society Vol. 2, No. 1 (Jan., 1989), pp. 1-31 ([jstor:1990911](https://www.jstor.org/stable/1990911))

* {#GluckMackenzieMorgan95} Herman Gluck, Dana Mackenzie, Frank Morgan, (5.20) in _Volume-minimizing cycles in Grassmann manifolds_, Duke Math. J. Volume 79, Number 2 (1995), 335-404 ([euclid:1077285156](https://projecteuclid.org/euclid.dmj/1077285156))

* {#Kerr96} Megan M. Kerr, Lemma 6.2 of _Some New Homogeneous Einstein Metrics on Symmetric Spaces_, Transactions of the American Mathematical Society, Vol. 348, No. 1 (1996), pp. 153-171 ([jstor:2155169](https://www.jstor.org/stable/2155169))

* {#BBMOOY96} [[Katrin Becker]], [[Melanie Becker]], [[David Morrison]], [[Hirosi Ooguri]], Y. Oz, Z. Yin, (3.5) of _Supersymmetric Cycles in Exceptional Holonomy Manifolds and Calabi-Yau 4-Folds_, Nucl. Phys. B480:225-238, 1996 ([arXiv:hep-th/9608116](https://arxiv.org/abs/hep-th/9608116))


* {#KacSmilga00} [[Victor Kac]], A.V. Smilga, around (1.10) in _Vacuum structure in supersymmetric Yang-Mills theories with any gauge group_, in _[[The Many Faces of the Superworld]], pp. 185-234 World Scientific (2000)_ ([arXiv:hep-th/9902029](https://arxiv.org/abs/hep-th/9902029), [doi:10.1142/9789812793850_0014](https://doi.org/10.1142/9789812793850_0014))

* {#OrneaPiccini00} Liviu Ornea, [[Paolo Piccinni]], _Cayley 4-frames and a quaternion-Kähler reduction related to Spin(7)_, Proceedings of the International Congress of Differential Geometry in the memory of A. Gray, held in Bilbao, Sept. 2000 ([arXiv:math/0106116](https://arxiv.org/abs/math/0106116))

* {#GroveWilkingZiller} Karsten Grove, Burkhard Wilking, Wolfgang Ziller, p. 30 of _Positively Curved Cohomogeneity One Manifolds and 3-Sasakian Geometry_ ([arXiv:math/0511464](https://arxiv.org/abs/math/0511464))

* {#BettiolMendes15} Renato G. Bettiol, Ricardo A. E. Mendes, _Flag manifolds with strongly positive curvature_, Math. Z. 280 (2015), no. 3-4, 1031-1046 ([arXiv:1412.0039](https://arxiv.org/abs/1412.0039))

* Maurizio Parton, Paolo Piccinni, Victor Vuletescu, Prop. 2.2 in _Clifford systems in octonionic geometry_ ([arXiv:1511.06239](https://arxiv.org/abs/1511.06239))

Discussion of $Sp(1)\cdot Sp(1) \cdot Sp(1)$ in the context of [[super Lie algebras]] and [[superconformal geometry|superconformal symmetry]] is in:

* {#Freund78} [[Peter Freund]], p. 634 of _World topology and gauged internal symmetries_, Proc. 19th Int. Conf. High Energy Physics, Tokyo 1978 ([spire:137780](http://inspirehep.net/record/137780/), [pdf](https://cds.cern.ch/record/870701/files/c78-08-23-p617.pdf))

and possibly with the $\mathbb{Z}_2$-quotient not made explicit:

* [[Peter Goddard]] (auth.), [[Peter Freund]], K. T. Mahanthappa, p. 128 of _Superstrings_, NATO ASI Series 175, Springer 1988

* Kazuo Hosomichi, Sangmin Lee, Sungjay Lee, [[Jaemo Park]], slide 13 of _New  Superconformal Chern-Simons Theories_ ([pdf](http://www3.ic.ac.uk/pls/portallive/docs/1/46083696.PDF))

[[!redirects Sp(2).Sp(1)]]
[[!redirects Spin(5).Spin(3)]]

[[!redirects Spn.Sp1]]

[[!redirects SpnSp1]]

[[!redirects Sp(1)Sp(1)Sp(1)]]
[[!redirects Sp(1).Sp(1).Sp(1)]]

[[!redirects central product spin group]]
[[!redirects central product spin groups]]

[[!redirects Spin(n).Spin(m)]]

[[!redirects Spin(n1).Spin(n2)]]

[[!redirects Spin(3)Spin(3)Spin(3)]]
[[!redirects Spin(3).Spin(3).Spin(3)]]

[[!redirects Spin(4).Spin(3)]]
