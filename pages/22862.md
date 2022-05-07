
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


> under construction

#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[discrete group]] (often taken to be a [[finite group]]) and for $A$ any [[abelian group]], there is a [[transgression]] [[homomorphism]] of [[cohomology groups]]

\[
  \label{TransgressionMapOnGroupCohomology}
  H_{grp}^{\bullet + 1}(G;\,A)
  \;\;=\;\;
  H^{\bullet + 1}(B G;\, A)
  \xrightarrow{ 
    \;\;\;
    \tau 
    \;\;\;
  }
  H^n
  \big(
    \Lambda B G,
    \,
    A
  \big)
  \;\;\;
    \simeq
  \;
  \underset{
    [g] \in G^{ad}/G
  }{\oplus}
  H^n_{grp}\big(C_g;\, A \big)
\]

from the [[group cohomology]] of $G$ to the [[groupoid cohomology]], in one degree lower,  of the [[inertia groupoid]]  $\Lambda B G$ of its [[delooping groupoid]] $B G \simeq (G \rightrightarrows \ast)$.

Since the [[inertia groupoid]] of the [[delooping groupoid]] is [[equivalence of groupoids|equivalent]] to a [[disjoint union]] over [[conjugacy classes]] $[g] \in G^{ad}/G$ of [[delooping groupoids]] of [[centralizer subgroups]] $C_g$, with $C_e = G$,

\[
  \label{DecompositionOfTheInertiaGroupoid}
  \Lambda B G
  \;\simeq\;
  \underset{ [g] \in G_{ad}/G }{\coprod}
  B C_g
  \;\;\;\simeq\;\;\;
  B G \,\sqcup\, 
  \underset{ [g] \neq [e] }{\coprod}
  B C_g
  \,,
\]

this induces a [[corestriction|corestricted]] transgression map within the [[group cohomology]] of $G$, and, more generally, to the [[group cohomology]] of any of its [[centralizer subgroups]]:

$$
  H_{grp}^{\bullet + 1}(G;\,A)
  \xrightarrow{ 
    \;\;\;
    \tau_{[e]} 
    \;\;\;
  }
  H_{grp}^{\bullet}(G;\,A)
  \,,
  \;\;\;\;\;\;\;
  H_{grp}^{\bullet + 1}(G,A)
  \xrightarrow{ 
    \;\;\;
    \tau_{[g]} 
    \;\;\;
  }
  H_{grp}^{\bullet}(C_g;\,A)
  \,.
$$

It is a [[folklore]] [[theorem]] that the transgression (eq:TransgressionMapOnGroupCohomology) maps an $(n+1)$-cocycle $c \colon G^{\times_{n+1}} \to A$ to the alternating [[sum]] (of [[functions]] with values in the [[abelian group]] $A$ with group operation denoted "$+$")

\[
  \label{SumFormulaForTransgressedCocycle}
  \tau(c)(\gamma, g_{n-1}, \cdots, g_1, g_0)
  \;=\;
  \pm
  \underset{
    0 \leq j \ln n
  }{\sum}
  (-1)^j
  \cdot
  c( g_{n-1}, \cdots, g_{n-j}, Ad_j(\gamma), g_{n-j-1}, \cdots, g_0 )
  \,,
\]

where

$$ 
  \gamma
  \xrightarrow{ g_{n-1} }
  Ad_{n-1}(\gamma)
  \xrightarrow{ g_{n-2} }
  \cdots
  \xrightarrow{ g_0 }
  Ad_{0}(\gamma)
  \;\;\;\;\;
  \in
  \;\;
  \Lambda B G
$$

is any sequence of $n$ composable [[morphisms]] in the [[inertia groupoid]], and where we use a shorthand for the [[adjoint action]] of $G$ on itself:

$$
  \begin{aligned}
    Ad_j(\gamma)
    & \;\coloneqq\;
    Ad_{(g_{n-1}\cdots g_j)}(\gamma)
    \\
    & \;\coloneqq\;
    (g_{n-1} \cdots g_j)^{-1} \cdot \gamma \cdot (g_{n-1} \cdots g_j)
    \,,
  \end{aligned}
$$

(which [[restriction|restricts]] to $Ad_j(\gamma) = \gamma$ upon [[corestriction]] to the connected component on the right of (eq:DecompositionOfTheInertiaGroupoid) that is indexed by $[\gamma]$).

In historically influential examples, for the case $n = 4$ and $A = \mathbb{Z}$ or, equivalently, $n = 3$ and $A = $ [[U(1)]], this formula (eq:SumFormulaForTransgressedCocycle):

* implicitly underlies ([Dijkgraaf & Witten 1990, p. 24](#DijkgraafWitten90)) the discussion of [[Dijkgraaf-Witten theory]]; 

* explains ([Willerton 2008](#Willerton08)) the nature of the "[[twisted Drinfeld double]]" of the [[group algebra]] of $G$;

* governs ([Dove 2019, Sec. 6.4](#Dove19)) the expression of 4-[[twisted cohomology|twisted]] [[equivariant elliptic cohomology]] at the [[Tate curve]] in terms of 3-[[twisted equivariant K-theory|twisted equivariant]] [[Tate K-theory]].

Below we mean to spell out a general abstract definition of the transgression map (eq:TransgressionMapOnGroupCohomology) and a [full proof](#ProofOfTheComponentFormula) of its component formula (eq:SumFormulaForTransgressedCocycle), amplifying that its form is a direct consequence of -- besides some basic [[homotopy theory]]/[[homological algebra]] which we review [below](#BackgroundAndLemmata)  -- the classical [[Eilenberg-Zilber theorem]] (which was partially re-discovered in [Willerton 2008, Sec. 1](#Willerton08)).


\linebreak


## Background and Lemmata
 {#BackgroundAndLemmata}

### Homotopy and homological algebra

Some relevant basics of [[homotopy theory]] in relation to [[homological algebra]]:

\begin{definition}\label{HomotopyCategories}
**([[homotopy categories]])**

We write:

* $Ho(sSet)$ for the [[classical homotopy category]], realized as the [[homotopy category of a model category|homotopy category of]] the [[classical model structure on simplicial sets]];

* $Ho(sAb)$ for the [[homotopy category of a model category|homotopy category of]] the [[model structure on simplicial abelian groups]];

* $Ho(Ch^+)$ for the [[homotopy category of a model category|homotopy category of]] the [[model structure on connective chain complexes]].

For $A \in $ [[Ab]], and $n \in \mathbb{N}$ we write

$$
  A[n] 
    \,\in\, 
  Ch^+_\bullet 
    \xrightarrow{Loc_{\mathrm{W}}} 
  Ho(Ch^+_\bullet)
$$

for the [[chain complex]] concentrated on $A$ in degree $n$.

We denote (using the same symbols for [[derived functors]] as for the original [[functors]]):

* the [[derived adjunction]] of the ([[free construction|free]] [[simplicial abelian group]] $\dashv$ [[underlying]] [[simplicial set]])-[[Quillen adjunction]] ([here](model+structure+on+simplicial+abelian+groups#eq:QuillenAdjunctionWithClassicalModelStructureOnSimplicialSets)) by

  \[
    \label{DerivedFreeSimplicialAbelianGroupAdjunction}
    Ho(sAb)
      \underoverset
       {\underset{frgt}{\longrightarrow}}
       {\overset{\mathbb{Z}(-)}{\longleftarrow}}
       {\;\;\;\;\;\;\bot\;\;\;\;\;\;}
    Ho(sSet)
  \]

* the [[derived adjunction|derived]] [[adjoint equivalence]]  of the [[Dold-Kan correspondence|Dold-Kan]] [[Quillen equivalence]] ([here](Dold-Kan+correspondence#ModelCatVersion)) by

  \[
    \label{DerivedDoldKanAdjunction}
    Ho(Ch^+_\bullet)
      \underoverset
        {\underset{DK}{\longrightarrow}}
        {\overset{N_\bullet}{\longleftarrow}}
        {\;\;\;\;\;\;\bot_{\mathrlap{\simeq}}\;\;\;\;\;\;}
    Ho(sAb)
  \]

* the [[derived adjunction|derived]] [[internal-hom]]-[[Quillen adjunction]] ([here](monoidal+model+category#InternalHomQuillenAdjunction)), for any $X \in $ [[SimplicialSets]], by

  \[
    \label{DerivedInternalHomAdjunction}
    Ho(sSet)
      \underoverset
        {\underset{[X,-]}{\longrightarrow}}
        {\overset{X \times (-)}{\longleftarrow}}
        {\;\;\;\;\;\;\bot\;\;\;\;\;\;}
    Ho(sSet)
    \,,
  \]

  (whose underived [[right adjoint]] is the [[simplicial mapping complex]]-construction);

* the [[derived adjunction|derived]] [[internal-hom]]-[[Quillen adjunction]] ([here](monoidal+model+category#InternalHomQuillenAdjunction)) for $\mathbb{Z}[1] \,\in\,$ [[ConnectiveChainComplexes]]:

  \[
    \label{DerivedDegreeShiftAdjunction}
    Ho(Ch^+_\bullet)
      \underoverset
        {\underset{ V_\bullet \mapsto V_{\bullet + 1} }{\longrightarrow}}
        {\overset{ V_\bullet \mapsto V_{\bullet - 1} }{\longleftarrow}}
        {\;\;\;\;\;\;\bot\;\;\;\;\;\;}
    Ho(Ch^+_\bullet)
  \]

\end{definition}


### Simplicial classifying spaces

\begin{remark}\label{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}
**([[delooping groupoid]] and [[simplicial classifying space]] of [[finite group]])** \linebreak
The [[nerve]] of the [[delooping groupoid]] of a [[discrete group]] $G$ is [[isomorphism|isomorphic]] to the [[simplicial classifying space]] of $G$ (see [this Example](simplicial+classifying+space#SimplicialClassifyingSpaceOfAnOrdinaryGroup)): 
$$
  N
  \big(
    G \rightrightarrows \ast
  \big)
  \;\simeq\;
  \overline{W} G
  \;\;\;
  \in
  \;
  sSet
  \,.
$$
For notational brevity we will be referring to $\overline{W}G$ in the following, but it may be helpful to keep thinking of the [[nerve]] of the [[delooping groupoid]]. 
From that perspective, an [[n-simplex]] in $\overline{W}G$, which is an [[n-tuple]] of [[group]] [[elements]], is suggestively denoted as a sequence of [[morphisms]]:

$$
  \big(\overline{W}G\big)_{n}
  \;\;
    =
  \;\;
  \Big\{
    \bullet
    \xrightarrow{g_{n-1}}
    \bullet
    \xrightarrow{\;}
    \cdots
    \bullet
    \xrightarrow{\;}
    \bullet
    \xrightarrow{g_1}
    \bullet
    \xrightarrow{g_0}
    \bullet
    \;\big\vert\;
    g_i \in G
  \Big\}
  \,.
$$

\end{remark}

We denote the [[image]] of $\overline{W}G$ in the [[classical homotopy category]] by

$$
  B G
  \;=\;
  \mathbf{B} G
  \;=\;
  Loc_{\mathrm{W}}(\overline{W}G)
  \;\;\;
  \in
  \;
  Ho(sSet)
  \,.
$$



### Group(oid) cohomology

Some relevant basics of [[cohomology]], for the cases of [[ordinary cohomology]] and [[group cohomology]]:

\begin{definition}\label{EilenbergMacLaneSpaces}
**([[Eilenberg-MacLane spaces]])** \linebreak
  For $A \,\in\,$ [[Ab]], and $n \in \mathbb{N}$, we write
  $$
    B^n A \,=\, K(A,n) 
    \,\coloneqq\,
    frgt \circ DK(A[n])
    \;\;\;
    \in
    \;
    sAb 
      \xrightarrow{ Loc_{\mathrm{W}}}
    Ho(sAb)
     \xrightarrow{frgt}
    Ho(sSet)
  $$
  for (the [[homotopy type]] of) the [[Eilenberg-MacLane space]]
  with $A$ in degree $n$.
\end{definition}

\begin{definition}\label{OrdinaryCohomology}
**([[ordinary cohomology]])** \linebreak
  For $X \in Ho(sSet)$,  $A \,\in\, Ab$  and $n \in \mathbb{N}$,
  the degree-$n$ *[[ordinary cohomology]]* of $X$ with [[coefficients]] in $A$ is
  $$
    H^n(X;\, A)
    \;=\;
    Ho(sSet)(X, \, B^n A)
    \,,
  $$
  where on the right we have the [[Eilenberg-MacLane space]] from Def. \ref{EilenbergMacLaneSpaces}.
\end{definition}


The following is an immediate re-casting of the traditional definition of [[group cohomology]]:

\begin{definition}\label{GroupCohomology}
**([[group cohomology]])** \linebreak
 For $G \,\in\, $ [[Groups]] and $A \,\in\,$ [[AbelianGroups]], 
the [[group cohomology]] of $G$ with [[coefficients]] in $A$ is, in degree $n \in \mathbb{N}$, the [[hom-group]]

$$
  H^n_{grp}(G;\,A)
  \;=\;
  Ho(Ch^+_\bullet)
  \big(
    N_\bullet 
     \circ
    \mathbb{Z}(\overline{W}G),
    \,
    A[n]
  \big)
  \,.
$$

\end{definition}

\begin{proposition}
\label{GroupCohomologyIsOrdinaryCohomologyOfClassifyingSpace}
**([[group cohomology]] is [[ordinary cohomology]] of [[classifying space]])** \linebreak
 For $G \,\in\, $ [[Groups]] and $A \,\in\,$ [[AbelianGroups]], 
 the [[group cohomology]] (Def. \ref{GroupCohomology}) of $G$ with coefficient in $A$ is [[natural isomorphism|naturally isomorphic]] to the [[ordinary cohomology]] of the [[simplicial classifying space]] of $G$ with [[coefficients]] in $B^n A$:

$$
  H^n_{grp}(G;\, A)
  \;\simeq\;
  H^n(B G,\, B^A)
  \,.
$$

\end{proposition}

\begin{proof}

By the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the [above](#HomotopyCategories) [[derived adjunctions]]:

$$
  \begin{aligned}
    H^n_{grp}(G;\, A)
    & \;0\;
    Ho(Ch^+_\bullet)
    \big(
      N_\bullet \circ \mathbb{Z}(\overline{W}G),
      \,
      A[n]
    \big)
    \\
    & \;\simeq\;
    Ho(sAb)
    \big(
      \mathbb{Z}(\overline{W}G),
      \,
      DK(A[n])
    \big)
    \\
    & \;\simeq\;
    Ho(sSet)
    \big(
      \overline{W}G
      \,
      frgt \circ DK(A[n])
    \big)
    \\
    & \;=\;
    Ho(sSet)
    \big(
      B G
      \,
      B^n A
    \big)
    \\
    & \;=\;
    H^n(B G;\, A)  
    \,.
  \end{aligned}
$$

\end{proof}

This Prop. \ref{GroupCohomologyIsOrdinaryCohomologyOfClassifyingSpace}, in view of Rem. \ref{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}  justifies the following definition:

\begin{definition}\label{GroupoidCohomology}
**([[groupoid cohomology]])** \linebreak
For $\mathcal{G} \,=\, (\mathcal{G}_1 \rightrightarrows \mathcal{G}_0) \,\in\,$ [[Groupoids]] and $A \,\in\,$ [[Ab]], $n \,\in\, \mathbb{N}$, the degree-$n$ *[[groupoid cohomology]]* of $\mathcal{G}$ with [[coefficients]] in $A$ is the [[ordinary cohomology]] (Def. \ref{OrdinaryCohomology}) of the [[homotopy type]] of the [[nerve]] of $\mathcal{G}$, regarded in the [[classical homotopy category]]: 

$$
  H^n
  \big(
    \mathcal{G};\,
    A
  \big)
  \;\coloneqq\;
  Ho(sSet)
  \big(
    N(\mathcal{G}),
    \,
    B^n A
  \big)
  \,.
$$
\end{definition}


### Products of simplices

Some fundamental fact about [[products of simplicial sets]]:

\begin{proposition}\label{NonDegenerateSimplicesInProductOfSimplices}
**(non-degenerate $(p+q)$-simplices in $\Delta[p] \times \Delta[q]$)**
\linebreak
For $p,q \,\in\, \mathbb{N}$
the non-degenerate simplices in the [[Cartesian product]] (Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise})

$$
  \Delta[p] \times \Delta[q]
$$ 

of standard [[simplices]] in [[sSet]] correspond, under the [[Yoneda lemma]], to precisely those morphisms of [[simplicial sets]]

\[
  \label{GenericSimplexInProductOfSimplices}
  \Delta[p+q]
  \xrightarrow{\;\; \sigma \;\;}
  \Delta[p] \times \Delta[q]
\]

which satisfy the following equivalent conditions:

* as morphisms of [[posets]], they are [[strictly monotone]];

* as [[permutations]] of $(p+q)$ elements they are $(p,q)$-[[shuffles]];

* as morphisms of [[finitely generated object|finitely generated]] [[categories]] they take generating morphisms to generating morphisms;

\end{proposition}

Such morphisms may hence be represented by [[paths]]

* on a $(p+1)\times(q+1)$-lattice,

* from one corner to its opposite corner,

* consisting of $p+q$ unit steps, 

* each either horizontally or vertially:

\begin{tikzcd}
  [
    row sep=large
  ]
    {(0,0)}
    \ar[r]
    \ar[d]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    %
    {(1,0)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,0)}
    \ar[rr,dotted]
    \ar[d]
    &
    &
    {(p,0)}
    \ar[d]
    \\
    {(0,1)}
    \ar[r]
    \ar[d]
    &
    {(1,1)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,1)}
    \ar[rr, dotted]
    \ar[d]
    &
    \cdots
    &
    {(p,1)}    
    \ar[d]
    \\
    {(0,2)}
    \ar[r]
    \ar[dd, dotted]
    &
    {(1,2)}
    \ar[r]
    \ar[dd, dotted]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,2)}
    \ar[rr, dotted]
    \ar[dd, dotted]
    \ar[ddrr, dotted]
    \ar[
      ddrr,-,
      color=blue,
      opacity=.25,
      line width=6pt,
      dotted
    ]
    &
    &
    {(p,2)}
    \ar[dd, dotted]
    \\
    &
    &
    &&
    \\
    {(0,q)}
    \ar[r]
    &
    {(1,q)}
    \ar[r]
    &
    {(2,q)}
    \ar[rr, dotted]
    &
    &
    {(p,q)}
\end{tikzcd}

\begin{proof}
From [this Prop.](product+of+simplices#CartesianProductOfSimplicialSetsIsComponentwise) 
it is clear (see [this Remark](product+of+simplices#DegenerateSimplicesInProductOfSimplicialSets)) that a 
simplex $\sigma \,\colon\, \Delta[p+q] \xrightarrow{\;} \Delta[p] \times \Delta[q]$  is degenerate 
precisely if, when regarded as a path as above, it contains a [[constant function|constant]] step, i.e. one which moves neither horizontally nor vertically. But then -- by degree reasons, since we are looking at paths of $p + q$ steps in a lattice of side length $p$ and $q$ -- it must be that the path proceeds by $p + q$ unit steps. 
\end{proof}

### Nerve of the inertia groupoid

Some basic facts about the [[nerve]] of an [[inertia groupoid]]:

\begin{proposition}
\label{InertiaGroupoidOfDeloopingGroupoidIsAdjointActionGroupoid}
**([[inertia groupoid]] of [[delooping groupoid]] is [[adjoint action|adjoint]] [[action groupoid]])** \linebreak
The inertia groupoid $\Lambda \mathbf{B} G$ is [[isomorphism|isomorphic]] to the [[action groupoid]] of the [[adjoint action]] of $G$ on itself:
$$
  \Lambda \mathbf{B}G
  \;\simeq\;
  G_{ad} \sslash G
  \;=\;
  \left(
    G \times G
    \underoverset
      {Ad_{(-)}(-)}
      {pr_2}
      {\rightrightarrows}
      G
  \right)
$$
\end{proposition}
This follows by immediate inspection. For more discussion see at *[[free loop space of a classifying space]]* the section *[Examples -- For finite groups](free+loop+space+of+classifying+space#ExampleDiscreteGroups)*.


\begin{proposition}
The [[groupoid convolution algebra]] of the inertia groupoid of the [[delooping groupoid]] $\mathbf{B}G$ is the [[Drinfeld double]] of the [[group convolution algebra]] of $G$.
\end{proposition}



\begin{definition}\label{MinimalSimplicialCircle}
**([[minimal simplicial circle]])** \linebreak
  Write 
  $$
    S 
    \;\coloneqq\;
    \Delta[1]/\partial\Delta[1]
    \;\;\;
    \in
    \;
    sSet
  $$
  for the [[simplicial set]] with exactly two non-degenerate cells, 

* one of which in degree 0, which we denote by $[0] = [1]$,

* and one in degree 1, which we denote by $\big[ [0], [1] \big]$.

\end{definition}

\begin{proposition}\label{NormalizedChainComplexOfMinimalSimplicialCircle}
**([[normalized chain complex]] of [[minimal simplicial circle]])**
\linebreak
  The [[normalized chain complex]] of the [[free simplicial abelian group]] of the [[minimal simplicial circle]] $S$ (Def. \ref{MinimalSimplicialCircle}) has the group of [[integers]] in degrees 0 and 1, and all [[differentials]] are [[zero morphism|zero]]:
$$
  N_\bullet \circ \mathbb{Z}(S)
  \;\simeq\;
  \left[
  \array{
    \vdots
    \\
    \big\downarrow
    \\
    0
    \\
    \big\downarrow
    \\
    \mathbb{Z}
    \\
    \big\downarrow {}^{\mathrlap{ 0 }}
    \\
    \mathbb{Z}
  }
  \;\;
  \right]
  \;\simeq\;
  \mathbb{Z}[1] \,\oplus\, \mathbb{Z} 
  \,.
$$
\end{proposition}



The following proposition follows on abstract grounds, but the explicit component-based proof we give is necessary in order to understand the [[transgression]]-formula for [[cocycles]] in the [[group cohomology]] of $G$ to cocycles on the inertia groupoid.
\begin{proposition}\label{RelationToSimplicialHomComplexIntoClassifyingSpace}
The [[nerve]] of the inertia groupoid of a delooping groupoid of a [[finite group]] $G$ is [[isomorphism|isomorphic]] to the [[simplicial hom complex]] out of the [[minimal simplicial circle]] $S$ (Def. \ref{MinimalSimplicialCircle}) into the [[simplicial classifying space]] $\overline{W}G$ (Rem. \ref{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}):

$$
  N\big( \Lambda \mathbf{B}G\big)_\bullet
  \;\simeq\;
  [S,\overline{W}G]_\bullet
  \,.
$$
\end{proposition}
\begin{proof}
We claim that the isomorphism is given by sending, for each $n \in \mathbb{N}$, any [[n-simplex]] $(\gamma, g_{n-1}, \cdots, g_1, g_0)$ of $N\big( Func( \mathbf{B}\mathbb{Z}, \, \mathbf{B}G )\big)$, being a sequence of [[natural transformations]] of the form
$$
  \array{
    \bullet
    &\xrightarrow{g_{n-1}}&
    \bullet
    &\xrightarrow{g_{n-2}}&
    \cdots
    &\xrightarrow{g_{n-j-1}}&
    \bullet
    &\xrightarrow{g_{n-j-2}}&
    \bullet
    &\xrightarrow{g_{n-j-3}}&
    \cdots
    &\xrightarrow{g_{0}}&
    \bullet
    \\
    \big\downarrow
    {}^{\mathrlap{  
      \gamma 
    }}
    && 
    \big\downarrow
    {}^{\mathrlap{  
      g_{n-1}^{-1} \cdot \gamma \cdot g_{n-1}
    }}
    && 
    && 
    \big\downarrow
    &&
    \big\downarrow
    && &&
    \big\downarrow 
    {}^{\mathrlap{  
      ( g_{n-1} \cdots g_{0} )^{-1} 
      \cdot
      \gamma 
      \cdot
      ( g_{n-1} \cdots g_{0} )
    }}
    \\
    \bullet
    &\xrightarrow{g_{n-1}}&
    \bullet
    &\xrightarrow{g_{n-2}}&
    \cdots
    &\xrightarrow{g_{n-j-1}}&
    \bullet
    &\xrightarrow{g_{n-j-2}}&
    \bullet
    &\xrightarrow{g_{n-j-3}}&
    \cdots
    &\xrightarrow{g_{0}}&
    \bullet
    \mathrlap{\,,}
  }
$$


to the homomorphism of simplicial sets

$$
  \Delta[n] \times S \xrightarrow{\;\;} \overline{W}G
  \,,
$$

which, in turn, sends a non-degenerate $(n+1)$-simplex in $\Delta[n] \times S$ of the form (in the path notation discussed at *[[product of simplices]]*)

$$
  \array{
    (0,[0])
    &\to&
    (1,[0])
    &\to&
    \cdots
    &\to&
    (j,[0])
    \\
    && && && \big\downarrow
    \\
    && && && 
    (j,[1])
    &\to&
    (j+1,[1])
    &\to&
    \cdots
    &\to&
    (n,[1])
  }
$$

to the $n+1$-simplex in $\overline{W}G$ (Rem. \ref{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}) of the form
 
$$
  \array{
    \bullet
    &\xrightarrow{g_{n-1}}&
    \bullet
    &\xrightarrow{g_{n-2}}&
    \cdots
    &\xrightarrow{g_{n-j}}&
    \bullet
    \\
    && && && 
    \big\downarrow 
    {}^{\mathrlap{  
      ( g_{n-1} \cdots g_{n-j} )^{-1} 
      \cdot
      \gamma 
      \cdot
      ( g_{n-1} \cdots g_{n-j} )
    }}
    \\
    && && && 
    \bullet
    &\xrightarrow{g_{n-j}}&
    \bullet
    &\xrightarrow{g_{n-j-1}}&
    \cdots
    &\xrightarrow{g_{0}}&
    \bullet
  }
$$

\end{proof}


As a consequence:

\begin{proposition}\label{FormOfTheSimplicialEvaluationMap}
  The [[evaluation map]]
  $$
    [S,\overline{W}G] \times S
    \xrightarrow{\;\;}
    \overline{W}G
  $$
  (out of the [[product of simplicial sets|product]] of the [[simplicial hom complex]] out of $S$ with $S$)
  takes any non-degenerate $n+1$-simplex of $[S,\overline{W}G] \times S$ of the form (still in the path notation discussed at *[[product of simplices]]*)
  $$
    \array{
      (\gamma, [0]) 
      &\xrightarrow{ (g_{n-1}, id) }&
      ( Ad_{n-1}(\gamma), [0]  )
      &\xrightarrow{ (g_{n-2}, id) }&
      \cdots
      &\xrightarrow{ (g_{j}, id) }&
      \big( Ad_{j}(\gamma), [0]  \big)      
      \\
      && && &&
      \big\downarrow {}^{\mathrlap{ (e, [ [0],[1] ]) }}
      \\
      && && &&
      (Ad_j(\gamma), [1])
      &\xrightarrow{ (g_{n-j},id)  }
      &
      \cdots
      &\xrightarrow{ (g_0,id) }&      
      (Ad_0(\gamma), [1])
      \mathrlap{\,,}
    }
  $$
  where we are abbreviating
  $$  
    \begin{aligned}
    Ad_j(\gamma) 
      &
      \;\coloneqq\;
    Ad_{(g_{n-1} \cdots g_j)}(\gamma)
    \\
    &
    \;\coloneqq\;
    (g_{n-1} \cdots g_j)^{-1} 
      \cdot 
    \gamma
      \cdot
    (g_{n-1} \cdots g_j)
    \,,
    \end{aligned}
  $$
  to the following $n+1$ simplex of $\overline{W}G$:
  $$
    \array{
      \bullet
      &\xrightarrow{ g_{n-1} }&
      \bullet
      &\xrightarrow{ g_{n-2} }&
      \cdots
      &\xrightarrow{ g_{j} }&
      \bullet
      \\
      && && &&
      \big\downarrow {}^{\mathrlap{ 
        Ad_j(\gamma)
      }}
      \\
      && && &&
      \bullet
      &\xrightarrow{ g_{n-j} }
      &
      \cdots
      &
      \xrightarrow{ g_0 } 
      &      
      \bullet
      \mathrlap{\,.}
    }
  $$
\end{proposition}


## Proof of the component formula
 {#ProofOfTheComponentFormula}

We prove that the formula (eq:SumFormulaForTransgressedCocycle) indeed expresses transgression in group cohomology. 

Consider the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
    H^n_{grp}
    \big(
      G;\, A
    \big)
    &
    \;=\;
    Ho(sSet)
    \big(
      N_\bullet \circ \mathbb{Z}(\overline{W}G),
      \,
      A[n]
    \big)
    \\
    &
    \;\simeq\;
    Ho(sSet)
    \big(
      \overline{W}G; \, frgt \circ DK\big( A[n] \big)
    \big)
    \\
    =
    H^n
    \big(
      B G;\, A
    \big)
    &
    \;\overset{[S,-]}{\to}\;
    Ho(sSet)
    \Big(
      [S,\overline{W}G];\, \, \big[S, frgt \circ DK\big( A[n] \big)\big]
    \Big)
    \\
    & 
    \;\simeq\;
    Ho(sSet)
    \Big(
      [S,\overline{W}G] \times S,
      \, frgt \circ DK\big( A[n] \big)  
    \Big)
    \\
    &
    \;\simeq\;
    Ho(sAbGrp)
    \Big(
      \mathbb{Z}\big( [S, \overline{W}G] \times S \big),
      \,
      DK\big(A[n]\big)
    \Big)
    \\
    &
    \;\simeq\;
    Ho(Ch^+_\bullet)
    \Big(
      N_\bullet \circ \mathbb{Z}\big( [S, \overline{W}G] \times S \big),
      \,
      A[n]
    \Big)    
    \\
    &
    \;\overset{EZ}{\simeq}\;
    Ho(Ch^+_\bullet)
    \Big(
      N_\bullet \circ \mathbb{Z}\big([S, \overline{W}G]\big) 
        \otimes 
      \underset{
        \mathbb{Z}[1]
        \oplus 
        \mathbb{Z}
      }{
        \underbrace{N_\bullet \circ \mathbb{Z}(S)}
      },
      \,
      A[n]
    \Big)    
    \\
    &
    \;\simeq\;
    Ho(Ch^+_\bullet)
    \Big(
      N_\bullet \circ \mathbb{Z}\big([S, \overline{W}G]\big),
      \,
      A[n] \oplus A[n-1]
    \Big)    
    \\
    & 
    \;\overset{pr_2}{\to}\;
    Ho(Ch^+_\bullet)
    \Big(
      N_\bullet \circ \mathbb{Z}\big([S, \overline{W}G]\big),
      \,
      A[n-1]
    \Big)    
    \\
    & \;=\;
    H^{n-1}
    \big(
      \Lambda B G;
      \,
      A
    \big)        
    \,.
  \end{aligned}
$$

Here 

* the first three lines recall the identification from Prop. \ref{GroupCohomologyIsOrdinaryCohomologyOfClassifyingSpace};

* the fourth line is the [component function](functor#eq:ComponentFunctionOnHomSets) on [[hom-sets]] of the [[derived functor|derived]] [[internal hom]]/[[simplicial mapping complex]]-[[functor]] out of the [[minimal simplicial circle]] $S$ (Def. \ref{MinimalSimplicialCircle});

* the fifth line is the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the derived [[free abelian group|free]] [[simplicial abelian group]]-adjunction (eq:DerivedFreeSimplicialAbelianGroupAdjunction);

* the sixth line is the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the derived [[Dold-Kan equivalence]] (eq:DerivedDoldKanAdjunction);

* the seventh line is pre-composition with the [[Eilenberg-Zilber map]], using that this is a [[quasi-isomorphism]] (and hence an [[isomorphism]] in the [[homotopy category]] [[model structure on connective chain complexes|on chain complexes]]) by the [[Eilenberg-Zilber theorem]];

  under the brace we are using Prop. \ref{NormalizedChainComplexOfMinimalSimplicialCircle};

* the eighth line is the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the derived degree-shift adjunction (eq:DerivedDegreeShiftAdjunction)

  (observing that the [[tensor product of chain complexes|tensor product]] of [[normalized chain complexes]] of [[free simplicial abelian groups]] is a [[cofibrant object|cofibrant]] representative of the correct [[derived functor]]-image -- using that all simplicial sets are [[cofibrant object|cofibrant]], that $\mathbb{Z}(-)$ and $N_\bullet$ are [[left Quillen functors]], and that $(Ch^+_\bullet, \otimes)$ is a [[monoidal model category]] ([this Prop.](model+structure+on+chain+complexes#ProjectiveModelStructureOnConnectiveChainComplexesIsMonoidal)), so that the [[tensor product of chain complexes|tensor product]] with $\mathbb{Z} \oplus \mathbb{Z}[1]$ is the correct [[left derived functor]]);

* the ninth line is the [[projection]] onto the second [[direct sum|direct summand]];

* the last line is Def. \ref{GroupoidCohomology} of [[groupoid cohomology]].

Chasing a cocycle through this sequence, and using Prop. \ref{FormOfTheSimplicialEvaluationMap} when it gets sent through the [[Eilenberg-Zilber map]], yields (eq:SumFormulaForTransgressedCocycle). (...)


## References

The transgression map is alluded to in 

* {#DijkgraafWitten90} [[Robbert Dijkgraaf]], [[Edward Witten]], p. 24 of: _[[DW.pdf:file]]_, Commun. Math. Phys. __129__ (1990) 393 ([euclid:cmp/1104180750](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-129/issue-2/Topological-gauge-theories-and-group-cohomology/cmp/1104180750.full))

An indication of a proof, implicitly using ingredients of the [[Eilenberg-Zilber map]] (re-discovered under the name "Parmesan map"):

* {#Willerton08} [[Simon Willerton]], Section 1 of: *The twisted Drinfeld double of a finite group via gerbes and finite groupoids*, Algebr. Geom. Topol. 8 (2008) 1419-1457 ([arXiv:math/0503266](https://arxiv.org/abs/math/0503266))

The transgression formula itself (without derivation) is also considered, in a context of [[twisted equivariant K-theory|twisted]] [[orbifold K-theory]], in:

* [[Alejandro Adem]], [[Yongbin Ruan]], [[Bin Zhang]], Section 4 of: _A Stringy Product on Twisted Orbifold K-theory_, Morfismos (10th Anniversary Issue), Vol. 11, No 2 (2007), 33-64.  ([arXiv:math/0605534](https://arxiv.org/abs/math/0605534), [Morfismos pdf](www.morfismos.cinvestav.mx/Portals/morfismos/SiteDocs/Articulos/Volumen11/No2/Zhang/arz.pdf))

* [[Jean-Louis Tu]], [[Ping Xu]], Section 3 of: *The ring structure for equivariant twisted K-theory*, J. Reine Angew. Math. 635 (2009), 97–148 ([arXiv:math/0604160](https://arxiv.org/abs/math/0604160), [doi:10.1515/CRELLE.2009.077](https://doi.org/10.1515/CRELLE.2009.077))

and specifically in the context of equivariant [[Tate K-theory]]:

* {#Dove19} [[Thomas Dove]], _Twisted Equivariant Tate K-Theory_ ([arXiv:1912.02374](https://arxiv.org/abs/1912.02374))


[[!redirects transgressions in group cohomology]]

[[!redirects transgression of group cocycles]]
[[!redirects transgressions of group cocycles]]
