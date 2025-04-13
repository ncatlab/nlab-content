
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



## Idea 

The *integer Heisenberg groups* or *discrete Heisenberg groups* are [[non-abelian group|non-abelian]] [[discrete group|discrete]] [[central extensions]] of the [[integer]] [[product groups]] $\mathbb{Z}^{2g}$, $g \in \mathbb{N}$, analogous to how the ordinary [[Heisenberg groups]] are [[non-abelian group|non-abelian]] [[central extensions]] of $\mathbb{R}^{2g}$. Generally there are analogous *$R$-Heisenberg groups* for any [[commutative ring]] $R$.

In fact, for even multiples of the basic such extension, integer Heisenberg groups are [[discrete group|discrete]] [[subgroups]] of ordinary $\mathbb{R}$-[[Heisenberg groups]] covering a [[lattice (discrete subgroup)|lattice]] inclusion $\mathbb{Z}^{2g} \hookrightarrow \mathbb{R}^{2g}$ (cf. Prop. \ref{TwiceHeisenbergExtensionInSymplecticForm} below).

In [[physics]], specifically in [[quantum field theory]], these even-weight integer Heisenberg groups are closely related to [[quantization of D=3 Chern-Simons theory|quantum]] [[abelian Chern-Simons theory]] (spelled out [below](#ModularAutomorphisms), following [SS25](#SS25), see also at *[2-Cohomotopy moduli of surfaces](cohomotopy#CohomotopyModuliOfSurfaces)*).


## Definition
 {#Definition}

### Integer Heisenberg group extensions of $\mathbb{Z}^2$
  {#IntegerHeisenbergGroup}

We discuss the restriction of the basic $\mathbb{R}$-[[Heisenberg group]] $H_3$ (see [there](Heisenberg+group#H3InComponents)) along the inclusion $\mathbb{Z}^2 \hookrightarrow \mathbb{R}^2$ and the mod-$n$ [[quotient groups]] of that.

In the following, we denote [[cyclic groups]], for $n \in \mathbb{N}$, uniformly by
$$
  \mathbb{Z}_{k}
  \;\coloneqq\;
  \left\{
  \begin{array}{lcl}
    \mathbb{Z} &\vert& k = 0
    \\
    \mathbb{Z}/(k) &\vert& \text{otherwise}
    \mathrlap{\,.}
  \end{array}
  \right.
$$

Recall (see [there](group+extension#CentralExtensionClassificationByGroupCohomology)) the equivalence of [[central extensions]] of a [[discrete group|discrete]] [[group]] $G$ by an [[abelian group]] $A$ (for the present case equipped with the [[trivial action|trivial]] $G$-[[action]]) with the degree=2 [[group cohomology]] $H^2(G;A)$.

\begin{proposition}
  For $k \in \mathbb{N}$,
  the [[central extension|central]] [[group extensions]] of $\mathbb{Z}^2$ by $\mathbb{Z}_k$ are all integral multiples of the following elementary Heisenberg extension:
\[
  \label{BasicIntegerHeisenbergExtensionOfZ2}
  \left\{
    \begin{array}{l}
    \big(a,b,[n]\big)
    \,\in\,
    \mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}_{k}
    \,,
    \\
    \big(
      a,b,[n]
    \big)
    \cdot
    \big(
      a',b',[n']
    \big)
    \;=\;
    \big(
      a + a', 
      b + b', 
      [ 
        n + n' + 
        {\color{red}
          a \, b'
        }
      ]
    \big)
    \end{array}
  \right\}
  \,.
\]
\end{proposition}
\begin{proof} 
The [[central extensions]] in question
$$
  1 
    \to 
  \mathbb{Z}_k
    \xrightarrow{cntrl}
  H
    \longrightarrow
  \mathbb{Z}^2
    \to
  1
$$
[are classified](group+extension#CentralExtensionClassificationByGroupCohomology) by the degree=2 [[group cohomology]] of $\mathbb{Z}^2$ with [[coefficients]] in $\mathbb{Z}_k$ (equipped with the [[trivial action|trivial]] $\mathbb{Z}^2$-[[group action|action]]).
 
That second [[group cohomology]] is:
\[
  \label{SecondGroupCohomologyOfZPlusZ}
  \begin{array}{ccl}
    H^2_{Grp}(\mathbb{Z}^2;\, \mathbb{Z}_k)
    &\simeq&
    H^2(B \mathbb{Z}^2;\, \mathbb{Z}_k)    
    \\
    &\simeq&
    H^2(T^2;\, \mathbb{Z}_k)    
    \\
    &\simeq&
    H^2(S^1_a \vee S^1_b \vee S^2;\, \mathbb{Z}_k)    
    \\
    &\simeq&
    H^2(S^2;\, \mathbb{Z}_k)    
    \\
    &\simeq&
    \mathbb{Z}_k
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
    \mathbb{Z}_k
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
    [ a b']
    \mathrlap{\,,}
  \end{array}
\]

whose cocycle condition
$
  [a b'] + [(a+a')b'']
  =
  [a(b'+b'')] + [a' b'']
$
is evidently satisfied due to the [[distributive law]] in the [[ring]] $\mathbb{Z}$ and which is clearly not divisible.
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

  \[
    \label{BasicGroupCommutator}
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
  \]

\end{example}

\begin{remark}
\label{BasicIntHeisenbergAsUpperTriangularMatrices}
  The basic integer Heisenberg group extension (eq:BasicIntegerHeisenbergExtensionOfZ2), at $k = 0$, is [[isomorphism|isomorphic]] to the [[matrix group]] of $3 \times 3$ [[upper triangular matrices]] with [[integer]] entries and all "1"s on their diagonal, since [[matrix multiplication]] gives:

$$
  \left[
  \begin{matrix}
    1 & a & c
    \\
    0 & 1 & b
    \\
    0 & 0 & 1
  \end{matrix}
  \right]
  \cdot
  \left[
  \begin{matrix}
    1 & a' & c'
    \\
    0 & 1 & b'
    \\
    0 & 0 & 1
  \end{matrix}
  \right]
  \;=\;
  \left[
  \begin{matrix}
    1 & a + a' & c + c' + a b'
    \\
    0 & 1 & b + b'
    \\
    0 & 0 & 1
  \end{matrix}
  \right]
$$

In this matrix form the basic integer Heisenberg group $H_3(\mathbb{Z})$ is commonly known in the pure [[group theory]]-literature (e.g. [Dummit & Foote 2006 p 35](#DummitFoote06), [Budylin 2014](#Budylin14)) where the higher level extensions typically do not find attention.
\end{remark}

But the relation to the *real* [[Heisenberg group]] (in both senses of "real") is made by the second multiple of this basic extension (cf. [Gelca & Uribe 2010 p. 7](#GelcaUribe10), [Gelca & Hamilton 2012 Def 2.4](#GelcaHamilton12), [Gelca & Hamilton 2015 Def 2.3](#GelcaHamilton15)):

\begin{proposition}
\label{TwiceHeisenbergExtensionInSymplecticForm}
  Twice the basic integer Heisenberg extension (eq:IntegerHeisenbergExtension)  is [[isomorphism|isomorphic]] to
\[
  \label{TwiceOfBasicIntegerHeisInSymplecticForm}
  \left\{
    \begin{array}{l}
    \big(a, b, [n]\big)
    \,\in\,
    \mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}_{k}
    \,,
    \\
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
    \end{array}
  \right\}  
  \mathrlap{\,.}
\]
\end{proposition}
\begin{proof}
  It is sufficient to see that the second red summand in (eq:TwiceOfBasicIntegerHeisInSymplecticForm) is a [[group cohomology|group 2-cocycle]] cohomologous to the first red summand, which means equivalently that the 2-cocycle
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

### Basic properties

\begin{prop}
  The multiple=2 discrete Heisenberg group $\mathbb{Z}_{k} \to \widehat{\mathbb{Z}^{2}} \to \mathbb{Z}^2$ (eq:TwiceOfBasicIntegerHeisInSymplecticForm) is the following [[quotient group]] of the [[product group]] $F(a,b) \times \mathbb{Z}_{k}$ with the [[free group]] $F(a,b)$ on two generators:
\[
  \label{HeisenbergAsQuotientOfFreeGroup}
  \widehat{\mathbb{Z}^2}
  \,\simeq\,
  \big(
    F(a,b) \times \mathbb{Z}_{k}
  \big) 
    \big/ 
  \big( a \cdot b = [2] \cdot b \cdot a \big)
  \,.
\]
\end{prop}

\begin{proof}
  The map
  $$
    \begin{array}{ccc}
     \frac{
       F(a,b) 
       \times 
       \mathbb{Z}_{k}
     }{
       a \cdot b = [2] \cdot b \cdot a     
     }
     &\xrightarrow{\;}&
     \widehat{\mathbb{Z}^2}
     \\
     [a] &\mapsto& (1,0,0)
     \\
     [b] &\mapsto& (0,1,0)
     \\ 
     [n] &\mapsto& (0,0,[n])
    \end{array}
  $$
  is clearly a [[bijection]] on [[underlying]] [[sets]], and is a [[group homomorphism]] since the quotient relation (eq:HeisenbergAsQuotientOfFreeGroup) is respected in $\widehat{\mathbb{Z}^2}$, by (eq:BasicGroupCommutator).
\end{proof}

(cf. also [arXiv:2203.08030](https://arxiv.org/abs/2203.08030), [p 21](https://arxiv.org/pdf/2203.08030#page=21))


### Linear representations
 {#LinearRepresentations}

\begin{example}
For $k \in \mathbb{Z}$,  [[linear representations]] of twice the $\mathbb{Z}_{2k}$-Heisenberg extension of $\mathbb{Z}^2$ (eq:TwiceOfBasicIntegerHeisInSymplecticForm)
\[
  \label{IrrepOfIntegerHeisenbergGroup}
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
are given by:
$$
  \mathscr{H}_1
  \;\coloneqq\;
  Span_{\mathbb{C}}\Big(
    {\vert 0 \rangle}
    ,\, 
    {\vert 1 \rangle}
    ,\,
    \cdots
    ,\,
    {\vert k-1 \rangle},
  \Big)
$$
$$
  \begin{array}{ccccccl}
  W_a  
  & \coloneqq &
  W(1,0,0)
  &\colon&
  {\big\vert n \big\rangle}
  &\mapsto&
  \zeta^{2n}
  {\big\vert n \big\rangle}
  \\
  W_b  
  &\coloneqq&
  W(0,1,0)
  &\colon&
  {\big\vert n \big\rangle}
  &\mapsto&
  {\big\vert (n + 1) \,mod\, k \big\rangle}
  \\
  \zeta 
  &\coloneqq&
  W(0,0,1)
  &\colon&
  {\big\vert n \big\rangle}
  &\mapsto&
  \zeta
  {\big\vert n \big\rangle}
  \mathrlap{\,,}
  \end{array}
$$
for $\zeta$ a $2k$th [[root of unity]].

For instance:
\[
  \label{W11InTermsOfWab}
  W_a \cdot W_b \cdot \zeta^{-1}
  \;=\;
  W(1,1,0)
  \;=\;
  W_b \cdot W_a \cdot \zeta^{+1}
  \,.
\]
\end{example}
**Notation:** In the following we write "$[n]$" for "$n \,mod\, k$" and "$\sum_{[n]}$" for "$\sum_{n =0}^{k-1}$".
\begin{proof}
  To see that this is a [[linear representation]],
  by (eq:HeisenbergAsQuotientOfFreeGroup) it is sufficient to check that the basic [[group commutator]] is represented, in that
\[
  \label{RepresentationOfBasicGroupCommutator}
  W_a \cdot W_b \,=\,
  \zeta^2
  \, 
  W_b \cdot W_a
  \mathrlap{\,,}
\]
which is evidently the case, since
$$
  \begin{array}{ccl}
    W_a \cdot W_b {\big\vert [n] \big\rangle}
    &=&
    W_a \cdot {\big\vert [n+1] \big\rangle}
    \\
    &=&
    \zeta^{2(n+1)}
    \,
    {\big\vert [n+1] \big\rangle}
    \mathrlap{\,,}
  \end{array}
$$
while
$$
  \begin{array}{ccl}
    W_b \cdot W_a {\big\vert [n] \big\rangle}
    &=&
    \zeta^{2n}
    \,
    W_b {\big\vert [n] \big\rangle}
    \\
    &=&
    \zeta^{2n}
    \,
    {\big\vert [n + 1] \big\rangle}
    \mathrlap{\,.}
  \end{array}
$$
\end{proof}

For more on linear representations of the level$=1$ integer Heisenberg group, see [Floratos & Tsohantjis 2022](#FloratosTsohantjis22).

\begin{remark}\label{RelationToChernSimonsStates}
**(relation to [[quantum states]] and [[quantum observables]] of [[abelian Chern-Simons theory]])**
\linebreak
The [[complex numbers|complex]] [[dimension of a vector space|dimension]] of the representation $\mathscr{H}_1$ (eq:IrrepOfIntegerHeisenbergGroup) is that expected for the [[space of quantum states]] of [[abelian Chern-Simons theory]] on a [[2-torus]] (cf. [Manoliu 1998a p 40](abelian+Chern-Simons+theory#Manoliu98a), [Gelca & Uribe 2010 Prop. 2.2](#GelcaUribe10))
\[
  \label{CSLevel}
  dim(\mathscr{H}_1) \;=\; K
  \,,
\]
and the [[group commutator]]-relation (eq:RepresentationOfBasicGroupCommutator)
$$
  W_a \cdot W_b 
  =
  \zeta^2
  \,
  W_b \cdot W_a
$$
of [[linear operators]] acting on this irrep (eq:IrrepOfIntegerHeisenbergGroup) reflects the characteristic [[commutator]]-relation of [[Wilson loop]]-[[quantum observables]] in [[abelian Chern-Simons theory]] on a [[2-torus]] (cf. [Tong 2016 (5.28)](quantum+Hall+effect#Tong16), [p 166](https://ncatlab.org/nlab/files/Tong-QuantumHallEffect.pdf#page=168)).
\end{remark}



### Modular automorphisms
 {#ModularAutomorphisms}


Moreover, the integer Heisenberg group at leve 2 knows about the [[modular group]] acting on its irrep (eq:IrrepOfIntegerHeisenbergGroup), hence on the  [[space of quantum states]] $\mathscr{H}_{T^2}$ from Rem. \ref{RelationToChernSimonsStates}, hence about the "[[modular functor]]" of [[abelian Chern-Simons theory]]:


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
  \,,
$$
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

\begin{remark}
\label{GenerationOfModularGroup}
Recall (from [there](SL2Z#SandTgenerateSL2Z)) that the [[modular group]] [[SL(2,Z)|$SL_2(\mathbb{Z})$]] is the [[subgroup]] of the [[general linear group]] generated by the two elements
\[
  \label{ModularGenerators}
  S
  \;\coloneqq\;
  \left[
    \begin{array}{rr}
    0 & 1
    \\
    -1 & 0
  \end{array}
  \right]
  \;\;\;\;\;
  \text{and}
  \;\;\;\;\;
  T
  \;\coloneqq\;
  \left[
  \begin{array}{rr}
    1 & 1
    \\
    0 & 1
  \end{array}
  \right]
  \mathrlap{\,.}
\]
and *[[finitely presented group|presented]]* via these generators subject to the following relations:
\[
  \label{PresentationOfSL2Z}
  SL_2(\mathbb{Z})
  \;\simeq\;
  \big\langle
    S, T
    \,\big\vert\,
    S^4 = \mathrm{e}
    ,\,
    (T S)^3 = \mathrm{e}
    ,\,
    S^2 (T S) = (T S)S^2
  \big\rangle
  \,.
\]
\end{remark}

\begin{proposition}
\label{ModularEquivariantHeisenbergRepresentation}
For [[even number|even]] $k$ (eq:CSLevel)
there exists a [[linear representation]]
\[
  \label{ModularActionOnH1}
  \begin{array}{ccc}
    \mathrm{SL}_2(\mathbb{Z})
    \times
    \mathscr{H}_1
    &\xrightarrow{\;}&
    \mathscr{H}_1
    \mathrlap{\,,}
  \end{array}
\]
of the [[modular group]] on the [[underlying]] [[complex vector space]] of (eq:IrrepOfIntegerHeisenbergGroup),
which [[intertwiner|intertwines]] the action (eq:IrrepOfIntegerHeisenbergGroup)
of $\widehat{\mathbb{Z}^2}$ on $\mathscr{H}_1$, with its [[automorphism|automorphic]] [[images]] under the modular group action \eqref{SymplecticActonOnSecondIntegerHeisenberg} on the Heisenberg group, in that: 
\[
  \label{SemidirectProductRelations}
  m(W) \cdot m\Big(
    {\big\vert [n] \big\rangle}
  \Big)
  \;=\;
  m\Big(
    W \cdot 
    {\big\vert [n] \big\rangle}
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
      \mathrlap{\,.}
    \end{array}
  \right.
\]
{#SemidirectProductAction} In other words, (eq:ModularActionOnH1) enhances $\mathscr{H}_1$ to a representation of the [[semidirect product group]]  $\widehat{\mathbb{Z}^2} \rtimes \mathrm{SL}_2(\mathbb{Z})$ with [[binary operation|operation]]

$$
  (W,m)\cdot (W',m') 
    \;\coloneqq\; 
  \big(
    W \cdot m(W'),\, m \cdot m'  
  \big) 
  \,.
$$

This representation (eq:ModularActionOnH1) is just the [[modular functor|modular action]] known from [[abelian Chern-Simons theory]] at [[even number|even]] [[level (Chern-Simons theory)|level]] $k$ (cf. [Wen 1990 (5.3)](abelian+Chern-Simons+theory#Wen90Rigid), [Manoliu 1998a p 67](abelian+Chern-Simons+theory#Manoliu98a), [Gannon 2005 (3.1b)](SL2Z#Gannon05)):
\[
  \label{RepresentationOfModularGenerators}
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
    {\big\vert [n] \big\rangle}
  \Big)
  &=&
  \underset{
    \eqqcolon 1/c_k 
  }{
  \underbrace{
    e^{
      -
      \pi \mathrm{i}/12
    }
  }
  }
  \,
  e^{ 
    \tfrac{\pi \mathrm{i}}{k}
    n^2
  }
  {\big\vert
   [ n ]
  \big\rangle}
  \end{array}
\]
\end{proposition}
\begin{proof}
To see that (eq:RepresentationOfModularGenerators) is indeed a representation of the modular group, we need to check that the relations (eq:PresentationOfSL2Z) are satisfied:

First we find
$$
  \begin{array}{rcl}
  S^2
  \Big({\big\vert [n] \big\rangle}\Big)
  &=&
  S
  \Big(
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
  {\big\vert[\widehat{n}]\big\rangle}
  \Big)
  \\
  &=&
  \sum_{
      [\widehat{\widehat n}] 
  }
  \,
  \underset{
    \delta_0\big(
       [ n + \widehat{\widehat{n}} ]
   \big)
  }{
  \underbrace{
  \tfrac{1}{k}
  \sum_{
      [\widehat n] 
  }
  \,
  e^{
    2 \pi \mathrm{i}
     \tfrac{
       \widehat{n} \, 
       (n + \widehat{\widehat{n}})
     }{
       k
     }
  }
  }
  }
  \,
  {\big\vert[\widehat{\widehat{n}}]\big\rangle}
  \\
  &=&
  {\big\vert[-n]\big\rangle}
  \end{array}
$$
(where under the brace we evaluated the [sum of roots of unity](root+of+unity#SumOfRootsOfUnity)),
which immediately implies the relation $S^4 = \mathrm{id}$ and thereby, with 
$$
  T \circ S
  \Big(
    {\big\vert [n] \big\rangle}
  \Big)
  \;=\;
  \tfrac{1}{\sqrt{\vert k \vert} c_k}
  \displaystyle{
    \sum_{
        [\widehat n] 
    }
  }
  \,
  e^{
     \tfrac{
       \pi \mathrm{i}
     }{k}
     (
       \widehat{n}^2
       +
       2\widehat{n} \, n
     )
  }
  {\big\vert[\widehat{n}]\big\rangle}
  \,,
$$
also the relation $S^2 (T S) = (T S) S^2$. It just remains to show that $(T S)^3 = \mathrm{e}$ or equivalently that $S T S \,=\, T^{-1} S^{-1} T^{-1}$. Direct computation yields:

$$
  \begin{array}{l}
    T^{-1} S^{-1} T^{-1}
    {\vert n \rangle}
    \;=\;
    T^{-1} S^{-1}
    e^{ - \tfrac{\pi \mathrm{i}}{k} n^2 }
    {\vert n \rangle}
    \\
    \;=\;
    T^{-1}
    \tfrac{1}{\sqrt{k}}
    \sum_{\widehat{n}}
    e^{ 
      \tfrac{\pi \mathrm{i}}{k} 
      (
        - n^2 - 2 \widehat{n} n 
      )   
    }
    {\vert \widehat{n} \rangle}
    \\
    \;=\;
    \tfrac{1}{\sqrt{k}}
    \sum_{\widehat{n}}
    e^{ 
      \tfrac{\pi \mathrm{i}}{k} 
      (
        - n^2 - 2 \widehat{n} n - \widehat{n}^2
      )   
    }
    {\vert \widehat{n} \rangle}
    \\
    \;=\;
    \tfrac{1}{\sqrt{k}}
    \sum_{\widehat{n}}
    e^{
      - 
      \tfrac{\pi \mathrm{i}}{k} 
      (\widehat{n} + n)^2
    }
    {\vert \widehat{n} \rangle}
  \end{array}
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \begin{array}{l}
  S T S
    {\big\vert n \big\rangle}
  \;=\;
  S T 
  \frac{1}{\sqrt{\vert k \vert}}
  \sum_{
      \widehat n
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
  {\big\vert \widehat{n} \big\rangle}
  \\
  \;=\;
  S
  \tfrac{1}{\sqrt{k}}
  \sum_{
      \widehat n
  }
  \,
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    (
      2 \widehat{n} \, n
      +
      \widehat{n}^2
    )
  }
  {\big\vert \widehat{n} \big\rangle}
  \\
  \;=\;
  \frac{1}{k}
  \sum_{
    \widehat n
    ,\,
    \widehat{\widehat{n}}
  }
  \,
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    (
      2 \widehat{n} \, n
      +
      \widehat{n}^2
      +
      2 \widehat{\widehat{n}} \widehat{n}
    )
  }
  {\big\vert \widehat{\widehat{n}} \big\rangle}
  \\
  \;=\;
  \frac{1}{\sqrt{k}}
  \sum_{ \widehat{\widehat{n}} }
  \underbrace{
  \tfrac{1}{\sqrt{k}}
  \sum_{ \widehat n }
  \,
  e^{
    \tfrac{\pi \mathrm{i}}{k}
      (\widehat{n} + (n + \widehat{\widehat{n}}))^2
  }
  }
  e^{
    -
    \tfrac{\pi \mathrm{i}}{k}
      (n + \widehat{\widehat{n}})^2
  }
  {\big\vert \widehat{\widehat{n}} \big\rangle}
  \,,
\end{array}
$$
where the term over the brace is in fact constant in $n$ and $\widehat{\widehat{n}}$ by the assumption that $k$ is even, because this implies that the summands are $k$-periodic:
\[
  \label{PeriodicityOfSummands}
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    (n + k)^2
  }
  \;=\;
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    (n^2 + 2 n k + k^2)
  }
  \;=\;
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    n^2
  }
  \underset{
    1\;if\;k\;even
  }{
  \underbrace{
    e^{
      \pi \mathrm{i}(2n + k)
    }
  }
  }
  \;=\;
  e^{
    \tfrac{\pi \mathrm{i}}{k}
    n^2
  }
  \,.
\]


This means that the last relation holds if the normalization factor $c_k$ is indeed fixed, as shown in (eq:RepresentationOfModularGenerators), to this [[quadratic Gauss sum]], which evaluated to (see [there](Gauss+sum#EvaluationOfQuadraticGaussSumWithHalvedExponents))
\[
  \label{NormalizationFactorForTOperator}
  c_k
  \;=\;
  \Big(
    \tfrac{1}{\sqrt{k}}
    \textstyle{
      \sum_{
        \widehat n
      }
    }
    \,
    e^{
       \tfrac{
         \pi \mathrm{i}
       }{k}
       \widehat{n}^2
    }
  \Big)^{1/3}
  \;=\;
  \big(\sqrt{\mathrm{i}}\big)^{1/3}
  \;=\;
  e^{ \pi \mathrm{i}/12 }
  \,.
\]


Finally to see that also the semidirect product of these two groups is represented in that (eq:SemidirectProductRelations) holds: 

We may explicitly check this for $m \in \{S,T\}$ any one of the modular generators (eq:ModularGenerators) by unwinding the above definitions:
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
  \,
    S\Big(
      {\big\vert
        [n]
      \big\rangle}
    \Big)  
  \\
  &=&
  S\Big(
    W_a 
    {\big\vert [n] \big\rangle}
  \Big)
  \mathrlap{\,,}
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
  e^{2 \pi \mathrm{i} \tfrac{\widehat{n}}{k}}
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
    W_b 
    {\big|
      [n]
    \big\rangle}
  \Big)
  \mathrlap{\,,}
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
    \mathrlap{\,,}
  \end{array}
$$
and finally, using (eq:W11InTermsOfWab):
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
    e^{\pi \mathrm{i} \tfrac{1}{k}}
    \,
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
    \mathrlap{\,.}
  \end{array}
$$

This completes the proof.
\end{proof}


\linebreak


## Related entries

* [[Heisenberg group]]

* [2-Cohomotopy moduli of surfaces](cohomotopy#CohomotopyModuliOfSurfaces)



## Literature

### In group theory

Generally on the integer/discrete Heisenberg group in the [[algebra]] and [[group theory]] literature

* {#LeePacker96} Soo Teck Lee, Judith A. Packer: *The Cohomology of the Integer Heisenberg Groups*, Journal of Algebra **184** 1 (1996) 230-250 &lbrack;[doi:10.1006/jabr.1996.0258](https://doi.org/10.1006/jabr.1996.0258)&rbrack;
  > (concerning its [[group cohomology]])

* {#DummitFoote06} David S. Dummit, Richard M. Foote Ex. 11 on p. 35: *Abstract Algebra*, Wiley (2003) &lbrack;[ISBN:978-0-471-43334-7](https://www.wiley.com/en-us/Abstract+Algebra%2C+3rd+Edition-p-9780471433347), [pdf](https://rksmvv.ac.in/wp-content/uploads/2021/04/David_S_Dummit_Richard_M_Foote_Abstract_Algeb_230928_225848.pdf)&rbrack;


* {#Budylin14} Roman Budylin: *Conjugacy classes in discrete Heisenberg groups*, Sbornik: Mathematics **205** 8 (2014) 1069–1079 &lbrack;[arXiv:1405.5499](https://arxiv.org/abs/1405.5499), [doi:10.1070/SM2014v205n08ABEH004410](https://doi.org/10.1070/SM2014v205n08ABEH004410)&rbrack;

* [[Daniel Bump]], Persi Diaconis, Angela Hicks, Laurent Miclo, Harold Widom: *An Exercise (?) in Fourier Analysis on the Heisenberg Group*, Annales de la Faculté des sciences de Toulouse: Mathématiques, Serie 6, Volume 26 (2017) no. 2, pp. 263-288 &lbrack;[arXiv:1502.04160](https://arxiv.org/abs/1502.04160), [numdam:AFST_2017_6_26_2_263_0](http://www.numdam.org/item/AFST_2017_6_26_2_263_0)&rbrack;

* {#DruţuKapovich18} [[Cornelia Druţu]], [[Michael Kapovich]] (appendix by [[Bogdan Nica]]): *Geometric group theory*, Colloquium Publications **63**, AMS (2018) &lbrack;[ISBN:978-1-4704-1104-6](https://bookstore.ams.org/coll-63/), [pdf](https://courses.maths.ox.ac.uk/node/view_material/35649)&rbrack;


* Jayadev S. Athreya, Ioannis Konstantoulas: *Lattice deformations in the Heisenberg group*, Groups, Geometry and Dynamics **14** 3 (2020) 1007–1022 &lbrack;[arXiv:1510.01433](https://arxiv.org/abs/1510.01433), [doi:10.4171/ggd/572](https://doi.org/10.4171/ggd/572)&rbrack;

* Uri Bader, Vladimir Finkelshtein, §5 of: *On the horofunction boundary of discrete Heisenberg group*, Geom Dedicata **208** (2020) 113–127 &lbrack;[arXiv:1904.11234](https://arxiv.org/abs/1904.11234), [doi:10.1007/s10711-020-00513-x](https://doi.org/10.1007/s10711-020-00513-x)&rbrack;

* Ruiwen Dong, p 9 of: *Recent advances in algorithmic problems for semigroups*, ACM SIGLOG News **10** 4 (2023) 3-23 &lbrack;[arXiv:2309.10943](https://arxiv.org/abs/2309.10943), [doi:10.1145/3636362.3636365](https://doi.org/10.1145/3636362.3636365)&rbrack;

On (invertibility in) the [[group algebra]]:

* Martin Göll, Klaus Schmidt, Evgeny Verbitskiy: *A Wiener Lemma for the discrete Heisenberg group: Invertibility criteria and applications to algebraic dynamics*, Monatsh Math **180** (2016) 485–525 &lbrack;[doi:10.1007/s00605-016-0894-0](https://doi.org/10.1007/s00605-016-0894-0), [arXiv:1603.08225](https://arxiv.org/abs/1603.08225)&rbrack;

On the [[representation theory]] with an eye towards [[quantum information theory]]:

* {#FloratosTsohantjis22} E. Floratos, I. Tsohantjis: *Complete set of unitary irreps of Discrete Heisenberg Group $H W_{2^s}$* &lbrack;[arXiv:2210.04263](https://arxiv.org/abs/2210.04263)&rbrack;

On the [[automorphism group]]:

* D.V. Osipov: *Discrete Heisenberg group and its automorphism group*, Mathematical Notes **98** 1 (2015) 185-188 &lbrack;[arXiv:1505.00348](https://arxiv.org/abs/1505.00348), [doi:10.1134/S0001434615070160](https://doi.org/10.1134/S0001434615070160)&rbrack;


See also:

* Yves Benoist: *Positive Harmonic Functions on the Heisenberg group I*, in: Proceedings of *European Congress of Mathematics 2021*, EMS Press (2023) 181-198  &lbrack;[arXiv:1907.05041](https://arxiv.org/abs/1907.05041), [doi:10.4171/8ecm/17](https://doi.org/10.4171/8ecm/17)&rbrack;

* Yves Benoist: *Positive harmonic functions on the Heisenberg group II*, Journal de l’École polytechnique - Mathématiques **8** (2021) 973-1003 &lbrack;[doi:10.5802/jep.163](https://doi.org/10.5802/jep.163), [numdam:10.5802/jep.163](https://www.numdam.org/articles/10.5802/jep.163), [hal:02400005](https://hal.science/hal-02400005)&rbrack;


### In modular/Chern-Simons theory

In relation to $U(1)$-[[current algebra]] ([[WZW-model]]):

* [[Ludwig D. Fadeev]]: *Discrete Heisenberg-Weyl Group and modular group*, Lett Math Phys **34** (1995) 249–254 &lbrack;[doi:10.1007/BF01872779](https://doi.org/10.1007/BF01872779)&rbrack;

As describing the [[phase space]] of [[abelian Chern-Simons theory]] on [[closed manifold|closed]] [[Riemann surfaces]] (and its relation to [[skein relations]] and [[theta functions]]):

* {#GelcaUribe10} [[Răzvan Gelca]], [[Alejandro Uribe]]: *From classical theta functions to topological quantum field theory*, in: *The Influence of Solomon Lefschetz in Geometry and Topology: 50 Years of Mathematics at CINVESTAV*, Contemporary Mathematics **621**, AMS (2014) 35-68 &lbrack;[arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [doi;10.1090/conm/621](https://doi.org/10.1090/conm/621), [ams:conm-621](https://bookstore.ams.org/conm-621), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf), [[GelcaUribe-ThetaFunctionsTQFT.pdf:file]]&rbrack;

* {#GelcaHamilton12} [[Răzvan Gelca]], [[Alastair Hamilton]]: *Classical theta functions from a quantum group perspective*, New York J. Math. **21** (2015) 93–127 &lbrack;[arXiv:1209.1135](http://arxiv.org/abs/1209.1135), [nyjm:j/2015/21-4](https://nyjm.albany.edu/j/2015/21-4.html)&rbrack;

* {#GelcaHamilton15} [[Răzvan Gelca]], [[Alastair Hamilton]]: *The topological quantum field theory of Riemann’s theta functions*, Journal of Geometry and Physics **98** (2015) 242-261 &lbrack;[doi:10.1016/j.geomphys.2015.08.008](https://doi.org/10.1016/j.geomphys.2015.08.008), [arXiv:1406.4269](https://arxiv.org/abs/1406.4269)&rbrack;


On [[group actions]] of the [[mapping class group]] of closed oriented [[surfaces]] on integer Heisenberg groups:

* [[Awais Shaukat]], [[Christian Blanchet]]: *Weakly framed surface configurations, Heisenberg homology and Mapping Class Group action*, Arch. Math. **120** (2023) 99–109 &lbrack;[arXiv:2206.11475](https://arxiv.org/abs/2206.11475), [doi:10.1007/s00013-022-01793-3](https://doi.org/10.1007/s00013-022-01793-3)&rbrack;

* [[Christian Blanchet]], [[Martin Palmer]], [[Awais Shaukat]]: *Action of subgroups of the mapping class group on Heisenberg homologies*, Contemporary Mathematics &lbrack;[arXiv:2306.08614](https://arxiv.org/abs/2306.08614)&rbrack;

* [[Martin Palmer]]: *Representations of the Torelli group via the Heisenberg group*, talk at *Workshop for Young Researchers in Mathematics – 10th ed.* (2021) &lbrack;[pdf](https://mdp.ac/files/2105-talk-notes-WYRM.pdf), [[Palmer-Anghel-TorelliHeisenberg.pdf:file]]&rbrack;

*  [[Christian Blanchet]]: *Heisenberg homologies of surface configurations*, [talk at](CQTS#BlanchetMar2023) *[Geometric/Topological Quantum Field Theories Workshop](Center+for+Quantum+and+Topological+Systems#ConferencesMar2023)* @ [[CQTS]] NYUAD (2023) &lbrack;slides: [[Blanchet-at-QFTAndCobordism2023.pdf:file]], video:[YT](https://www.youtube.com/watch?v=prcU4v7LFZQ)&rbrack;


The above discussion of irreps and modular automorphisms related to abelian Chern-Simons theory follows:

* {#SS25} [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Engineering of Anyons on M5-Probes via Flux-Quantization]]*, Lecture Notes (2025)


[[!redirects integer Heisenberg groups]]

[[!redirects discrete Heisenberg group]]
[[!redirects discrete Heisenberg groups]]



