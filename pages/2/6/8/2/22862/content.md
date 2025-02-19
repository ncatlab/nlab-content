
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


#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[discrete group]] (often taken to be a [[finite group]]) and for $A$ any ([[discrete group|discrete]]) [[abelian group]], there is a [[transgression]] [[homomorphism]] of [[cohomology groups]]

\[
  \label{TransgressionMapOnGroupCohomology}
  \begin{array}{rcl}
  H_{grp}^{\bullet + 1}(G;\,A)
  \;\;=\;\;
  \\
  H^{\bullet + 1}(B G;\, A)
  &
  \xrightarrow{ 
    \;\;\;\;
    \tau 
    \;\;\;\;
  }
  &
  H^n
  \big(
    \Lambda B G,
    \,
    A
  \big)
  \;\simeq
  \\
  &&
  \underset{
    \mathclap{
      \array{
      \phantom{-}
      \\
      [g] \in G^{ad}/G
      }
    }
  }{\oplus}
  \;
  H^n_{grp}\big(C_g;\, A \big)
  \end{array}
\]

from the [[group cohomology]] of $G$ to the [[groupoid cohomology]], in one degree lower, of the [[inertia groupoid]]  $\Lambda B G$ of its [[delooping groupoid]] $B G \simeq (G \rightrightarrows \ast)$.

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
  \begin{array}{l}
  \tau(c)
  \big(
    \gamma, g_{n-1}, \cdots, g_1, g_0
  \big)
  \\
  \;=\;
  \pm
  \underset{
    0 \leq j \leq n
  }{\sum}
  (-1)^j
  \cdot
  c\big( 
    g_{n-1}, 
     \cdots,\, 
    g_{n-j},\, 
    Ad_j(\gamma),\, 
    g_{n-j-1},\, 
    \cdots,\, 
    g_0 
  \big)
  \,,
  \end{array}
\]

where

$$ 
  \gamma
  \xrightarrow{ g_{n-1} }
  Ad_{1}(\gamma)
  \xrightarrow{ g_{n-2} }
  \cdots
  \xrightarrow{\; g_0 \;}
  Ad_{n}(\gamma)
  \;\;\;\;\;
  \in
  \;\;
  \Lambda B G
$$

is any sequence of $n$ composable [[morphisms]] in the [[inertia groupoid]], and where we use a shorthand for the [[adjoint action]] of $G$ on itself:

$$
  \begin{aligned}
    Ad_{j}(\gamma)
    & \;\coloneqq\;
    Ad_{(g_{n-1}\cdots g_{n-j})}(\gamma)
    \\
    & \;\coloneqq\;
    (g_{n-1} \cdots g_{n-j})^{-1} 
      \cdot 
    \gamma \cdot (g_{n-1} \cdots g_{n-j})
    \,,
  \end{aligned}
$$

(which [[restriction|restricts]] to $Ad_j(\gamma) = \gamma$ upon [[corestriction]] to the connected component on the right of (eq:DecompositionOfTheInertiaGroupoid) that is indexed by $[\gamma]$).

In historically influential examples, for the case $n = 4$ and $A = \mathbb{Z}$ or, equivalently, $n = 3$ and $A = $ [[U(1)]], this formula (eq:SumFormulaForTransgressedCocycle):

* implicitly underlies &lbrack;[Dijkgraaf & Witten 1990, p. 14](#DijkgraafWitten90)&rbrack; the discussion of [[Dijkgraaf-Witten theory]]; 

* explains &lbrack;[Willerton 2008](#Willerton08)&rbrack; the nature of the "[[twisted Drinfeld double]]" of the [[group algebra]] of $G$;

* governs &lbrack;[Dove 2019, Sec. 6.4](#Dove19)&rbrack; the expression of 4-[[twisted cohomology|twisted]] [[equivariant elliptic cohomology]] at the [[Tate curve]] in terms of 3-[[twisted equivariant K-theory|twisted equivariant]] [[Tate K-theory]].

Below we mean to spell out a general abstract definition (Def. \ref{Transgression}) of the transgression map (eq:TransgressionMapOnGroupCohomology) and a [full proof](#ProofOfTheComponentFormula) of its component formula (eq:SumFormulaForTransgressedCocycle), amplifying that its form is a direct consequence of -- besides some basic [[homotopy theory]]/[[homological algebra]] which we review [below](#BackgroundAndLemmata)  -- the classical [[Eilenberg-Zilber theorem]], i.e. the [[Eilenberg-Zilber/Alexander-Whitney deformation retraction]] (which was partially re-discovered in [Willerton 2008, Sec. 1](#Willerton08) under the name "Parmesan theorem").


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

* $Ho(Ch_+)$ for the [[homotopy category of a model category|homotopy category of]] the [[model structure on connective chain complexes]].

For $A \in $ [[Ab]], and $n \in \mathbb{N}$ we write

$$
  A[n] 
    \,\in\, 
  Ch_+ 
    \xrightarrow{Loc_{\mathrm{W}}} 
  Ho(Ch_+)
$$

for the [[chain complex]] concentrated on $A$ in degree $n$.

We denote (using the same symbols for [[derived functors]] as for the original [[functors]]):

* the [[derived adjunction]] of the ([[free construction|free]] [[simplicial abelian group]] $\dashv$ [[underlying]] [[simplicial set]])-[[Quillen adjunction]] ([here](model+structure+on+simplicial+abelian+groups#eq:QuillenAdjunctionWithClassicalModelStructureOnSimplicialSets)) by

  \[
    \label{DerivedFreeSimplicialAbelianGroupAdjunction}
    Ho(sAb)
      \underoverset
       {\underset{undrlg}{\longrightarrow}}
       {\overset{\mathbb{Z}(-)}{\longleftarrow}}
       {\;\;\;\;\;\;\bot\;\;\;\;\;\;}
    Ho(sSet)
  \]

* the [[derived adjunction|derived]] [[adjoint equivalence]]  of the [[Dold-Kan correspondence|Dold-Kan]] [[Quillen equivalence]] ([here](Dold-Kan+correspondence#ModelCatVersion)) by

  \[
    \label{DerivedDoldKanAdjunction}
    Ho(Ch_+)
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
    Ho(Ch_+)
      \underoverset
        {\underset{ V_\bullet \mapsto V_{\bullet + 1} }{\longrightarrow}}
        {\overset{ V_\bullet \mapsto V_{\bullet - 1} }{\longleftarrow}}
        {\;\;\;\;\;\;\bot\;\;\;\;\;\;}
    Ho(Ch_+)
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
For notational brevity we will be referring to $\overline{W}G$ in the following, but it may be helpful to keep thinking of this isomorphically as the [[nerve]] of the [[delooping groupoid]], $\overline{W} G \,=\, N (G \rightrightarrows \ast)$. 
From this perspective, an [[n-simplex]] in $\overline{W}G$, which is an [[n-tuple]] of [[group]] [[elements]], is suggestively denoted as a sequence of [[morphisms]]:

$$
  \big(\overline{W}G\big)_{n}
  \;\;
    =
  \;\;
  \Big\{
    \bullet
    \xrightarrow{g_{n-1}}
    \bullet
    \xrightarrow{\phantom{--}}
    \cdots
    \bullet
    \xrightarrow{\phantom{--}}
    \bullet
    \xrightarrow{\; g_1 \;}
    \bullet
    \xrightarrow{\; g_0 \;}
    \bullet
    \;\big\vert\;
    g_i \in G
  \Big\}
  \,.
$$

\end{remark}

We denote the [[image]] of $\overline{W}G$ in the [[classical homotopy category]] by:

$$
  B G
  \;=\;
  \mathbf{B} G
  \;=\;
  Loc_{\mathrm{W}}
  \big(
    \overline{W}G
  \big)
  \;\;\;
  \in
  \;
  Ho(sSet)
$$

(where the first equality reflects that $G$ is assumed to be [[discrete group|discrete]]).



### Group(oid) cohomology

Some relevant basics of [[cohomology]], for the cases of [[ordinary cohomology]] and [[group cohomology]]:

\begin{definition}\label{EilenbergMacLaneSpaces}
**([[Eilenberg-MacLane spaces]])** \linebreak
  For $A \,\in\,$ [[Ab]], and $n \in \mathbb{N}$, we write
  $$
    B^n A \,=\, K(A,n) 
    \,\coloneqq\,
    underlg \circ DK(A[n])
    \;\;\;
    \in
    \;
    sAb 
      \xrightarrow{ Loc_{\mathrm{W}}}
    Ho(sAb)
     \xrightarrow{undrlg}
    Ho(sSet)
  $$
  for (the [[homotopy type]] of) the [[Eilenberg-MacLane space]] with $A$ in degree $n$ -- here constructed as the [[underlying]] [[simplicial set]] of the [[simplicial abelian group]] which is the image under the [[Dold-Kan construction]] of the [[chain complex]] that is concentrated on $A$ in degree $n$.
\end{definition}

\begin{definition}\label{OrdinaryCohomology}
**([[ordinary cohomology]])** \linebreak
  For $X \in Ho(sSet)$,  $A \,\in\, Ab$  and $n \in \mathbb{N}$,
  the degree-$n$ *[[ordinary cohomology]]* of $X$ with [[coefficients]] in $A$ is the following [[hom-set]] in the [[classical homotopy category]]:
  $$
    H^n(X;\, A)
    \;=\;
    Ho(sSet)
    \big(
      X, \, B^n A
    \big)
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
  Ho(Ch_+)
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
  H^n(B G;\, A)
  \,.
$$

\end{proposition}

\begin{proof}

By the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the [above](#HomotopyCategories) [[derived adjunctions]]:

$$
  \begin{aligned}
    H^n_{grp}(G;\, A)
    & \;0\;
    Ho(Ch_+)
    \big(
      N_\bullet \circ \mathbb{Z}(\overline{W}G),
      \,
      A[n]
    \big)
    \\
    & \;\simeq\;
    Ho(sAb)
    \big(
      \mathbb{Z}(\overline{W}G)
      ,\,
      DK(A[n])
    \big)
    \\
    & \;\simeq\;
    Ho(sSet)
    \big(
      \overline{W}G
      ,\,
      undrlng \circ DK(A[n])
    \big)
    \\
    & \;=\;
    Ho(sSet)
    \big(
      B G
      ,\,
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

Some basic facts about [[products of simplicial sets]]:

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

* as [[morphisms]] of [[posets]], they are [[strictly monotone]];

* as [[permutations]] of $(p+q)$ [[elements]] they are $(p,q)$-[[shuffles]];

* as [[morphisms]] of [[finitely generated object|finitely generated]] [[categories]] they take generating morphisms to generating morphisms;

\end{proposition}

Such morphisms may hence be represented by [[paths]]:

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
precisely if, when regarded as a path as above, it contains a [[constant function|constant]] step, i.e. one which moves neither horizontally nor vertically. But then --- by degree reasons, since we are looking at paths of $p + q$ steps in a lattice of side length $p$ and $q$ --- it must be that the path proceeds by $p + q$ unit steps. 
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


\begin{remark}
The [[groupoid convolution algebra]] of the [[inertia groupoid]] of the [[delooping groupoid]] $\mathbf{B}G$ is the [[Drinfeld double]] (see there for more) of the [[group algebra]] of $G$.
\end{remark}



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
\big\downarrow\mathrlap{ \scriptsize{0} }
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



The following proposition holds on general grounds (duscussed at *[[free loop space of classifying space]]*), but the explicit component-based proof we give now is necessary, further below, in order to understand the [[transgression]]-formula for [[cocycles]] in the [[group cohomology]] of $G$ to cocycles on the inertia groupoid.
\begin{proposition}\label{RelationToSimplicialHomComplexIntoClassifyingSpace}
The [[nerve]] of the [[inertia groupoid]] of a [[delooping groupoid]] of a [[finite group]] $G$ is [[isomorphism|isomorphic]] to the [[simplicial hom complex]] out of the [[minimal simplicial circle]] $S$ (Def. \ref{MinimalSimplicialCircle}) into the [[simplicial classifying space]] $\overline{W}G$ (Rem. \ref{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}):

$$
  N\big( \Lambda \mathbf{B}G\big)_\bullet
  \;\simeq\;
  [S,\overline{W}G]_\bullet
  \,.
$$
\end{proposition}
\begin{proof}
This is a specialization of the general fact that the simplicial nerve repects [[mapping objects]] (see [this Prop.](nerve#NerveOfCategoriesPreservesMappingObjects) at *[[nerve]]*). We spell it out for the present case:

We claim that the isomorphism is given by sending, for each $n \in \mathbb{N}$, any [[n-simplex]] $(\gamma;\, g_{n-1}, \cdots, g_1, g_0)$ of $N\big( Func( \mathbf{B}\mathbb{Z}, \, \mathbf{B}G )\big)$, being a sequence of [[natural transformations]] of the form
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
    \big\downarrow\mathrlap{^{  
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
  maps non-degenerate $n+1$-simpleces of $[S,\overline{W}G] \times S$ as follows:

\begin{tikzcd}[
    column sep=30pt,
    row sep=4pt
  ]
  S_{n+1}
  \times
  \mathrm{Hom}
  \big(
    S \times \Delta[n+1]
    ,\,
    \overline{W}G
  \big)
  \ar[
    rr,
    "{ \mathrm{ev} }"
  ]
  &&
  \big(
    \overline{W}G
  \big)_{n+1}
  \\
  \Big(
  s_{(1,\cdots, \widehat{k}, \cdots, n)} \ell
  ,\,
  s_k
  \big(
    \gamma
    ;\,
    g_{n-1}
    ,\,
    \cdots
    ,\,
    g_{0}
  \big)
  \Big)
  &\mapsto&
  \big(
    g_{n-1}
    ,\,
    \cdots,
    g_{n-k}
    ,\,
    \mathrm{Ad}_k(\gamma)
    ,\,
    g_{n - (k+1)}
    ,\,
    \cdots
    ,\,
    g_0
  \big)
\end{tikzcd}

 
\end{proposition}
\begin{proof}
This follows by unwinding the component formula for the [[evaluation map]] on [[simplicial mapping complexes]] ([this Prop.](function+complex#ComponentFormulaForEvaluationMap)):

Recall that we denote by
\[
  \label{CellInNerveOfInertiaGroupoid}
 \big(
  \gamma
  ;\,
  g_{n-1}
  ,\,
  g_{n-2}
  ,\,
  \cdots
  ,\,
  g_{0}
 \big)
 \;\; \in \;\;
 \mathrm{Hom}
 \big(
   S \times \Delta[n]
   ,\,
   \overline{W}G
 \big)
 \;\simeq\;
 \Big(
 N
 \mathrm{Map}
  \big( 
   { \mathbf{B}\mathbb{Z} }
   ,\,
   { \mathbf{B}G }
  \big)
 \Big)_{n}
\]
the $n$-cell in the [[nerve]] of the [[inertia groupoid]] that corresponds to the sequence of natural transformation which start at the functor 
$$
  \gamma 
    \,\in\, 
   G 
    \,\simeq\, 
  \mathrm{Hom}_{\mathrm{Grp}}(\mathbb{Z}, G) 
    \,\simeq\, 
  \mathrm{Hom}\big(
    \mathbf{B}\mathbb{Z}
    ,\, 
    \mathbf{B}G
  \big)
$$
and successively have components $g_{n-\bullet} \in G$. 

> Throughout we are writing "$Hom$" for [[hom-sets]] and "$Map$" for [[hom-objects]], i.e. for [[internal homs]] and we keep tacitly going back and forth through the [[bijections]] in (eq:CellInNerveOfInertiaGroupoid).

If we abbreviate (this follows conventions familiar in discussion of *[[transgression in group cohomology]]*)
$$
  \begin{aligned}
    Ad_{k}(\gamma)
    & \;\coloneqq\;
    Ad_{(g_{n-1}\cdots g_{n-k})}(\gamma)
    \\
    & \;\coloneqq\;
    (g_{n-1} \cdots g_{n-k})^{-1} 
      \cdot 
    \gamma \cdot (g_{n-1} \cdots g_{n-k})
    \,,
  \end{aligned}
$$
then this corresponds to a sequence of composable morphisms in the inertia groupoid of this form:
$$ 
  \gamma
  \xrightarrow{ g_{n-1} }
  Ad_{1}(\gamma)
  \xrightarrow{ g_{n-2} }
  \cdots
  \xrightarrow{\; g_0 \;}
  Ad_{n}(\gamma)
  \;\;\;\;\;
  \in
  \;\;
  \Lambda B G
$$

The simplicial map (eq:CellInNerveOfInertiaGroupoid) maps the non-degenerate $(n+1)$-cells in the [[product of simplicial sets]] (see the discussion [there](product+of+simplices#NonDegenerateCellsInAProductOfSimplices)) of $S$ (eq:MinimalSimplicialCircle) with the [[simplicial simplex|simplicial $n$-simplex]] as follows:

\begin{imagefromfile}
    "file_name": "ActionOfCellInNerveOfIniertiaGroupoid-221205.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


This is not exactly what we need unwinding the [[evaluation map]], but it is close: the image of (eq:CellInNerveOfInertiaGroupoid) under the $k$th [[degeneracy map]] evidently gives the following mapping:

\begin{imagefromfile}
    "file_name": "ActOfDegOfCellInNerveOfInertiaGrpd-221205b.jpg",
    "width": "850",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This is the type of mapping that appears in the component formula for the [[evaluation map]] on [[function complexes]] (from [that Prop.](function+complex#ComponentFormulaForEvaluationMap)), and so the claim follows.
\end{proof}

### Transgression in cohomology

\begin{definition}\label{Transgression}
  **([[transgression]])**
  For $\mathcal{A} \,\in\, sAb$ a [[simplicial abelian group]], hence with [[free loop space of classifying space|free loop space of its classifying space]] given
  (via [this Prop.](free+loop+space+of+classifying+space#FreeLoopSpaceOfClassifyingSpaceOfSimplicialAbelianGroup)) by
  \[
    \label{FreeLoopSpaceOfClassifyingSpaceOfAbelianSimplicialGroup}
    \Lambda \mathbf{B}\mathcal{A}
    \;\simeq\;
    \mathcal{A}
    \times 
    \mathbf{B}\mathcal{A}
  \]
  we say that *[[transgression]]* in $\mathcal{A}$-cohomology
  is 
  $$
    H
    \big( 
      -;\,
      \mathbf{B}\mathcal{A}
    \big)
    \xrightarrow{ [S, -] }
    H
    \big( 
      \Lambda(-);\,
      \mathcal{A} \times \mathbf{B}\mathcal{A}
    \big)
    \xrightarrow{\;\; pr_2 \;\; }
    H
    \big( 
      \Lambda(-);\,
      \mathcal{A}
    \big)    
    \,.
  $$
\end{definition}

\begin{proposition}\label{FreeLoopSpaceOfEMSpaceIdentifiedViaEilenbergZilber}
**([[free loop space of classifying space]] identified via [[Eilenberg-Zilber map]])** \linebreak
For $n \in \mathbb{N}_+$ and
for $A \,\in\, Ab$ the [[integers]] or the [[circle group]],
the following [[composition|composite]] of is a [[simplicial weak equivalence]]
\[
  \label{ComparisonMorphismFromFreeLoopSpaceViaEilenbergZilber}
  \begin{aligned}
    &
    \big[
      S,
      \,
      B^n A
    \big]_\bullet   
    \\
    & \;=\;
    \big[
      S, 
      \,
      undrlng \circ DK(A[n])
    \big]_\bullet
    \\
    &
    \;\simeq\;   
    sSet
    \big(
      S \times \Delta[\bullet],
      \,
      undrlng \circ DK(A[n])
    \big)
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S \times \Delta[\bullet]),
      \,
      A[n]
    \big)    
    \\
    & \;\xrightarrow{EZ_S}\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S) 
      \,\otimes\,
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      A[n]
    \big)    
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      [
        N \circ \mathbb{Z}(S),
        \,
        A[n]
      ]
    \big)    
    \\
    & \;\simeq\;
    \Big(
    undrlng \circ DK
    \big(
      [
        \underset{
          \mathbb{Z} \oplus \mathbb{Z}[1]
        }{
        \underbrace{
          N \circ \mathbb{Z}(S)
        }
        },
        \,
        A[n]
      ]
    \big)
    \Big)_\bullet
    \\
    & \;\simeq\;
    \Big(
    undrlng \circ DK
    \big(
      A[n] \oplus A[n-1]
    \big)
    \Big)_\bullet
    \;=\;
    B^n A \times B^{n-1} A
  \end{aligned}
\]

\end{proposition}
Here all [[isomorphisms]] are [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the [above](#HomotopyCategories) [[adjoint functor|adjunctions]], the step denoted $EZ_S$ is pre-composition with the [[Eilenberg-Zilber map]], and under the brace we are using Prop. \ref{NormalizedChainComplexOfMinimalSimplicialCircle}.

\begin{proof}
  By the fact that the [[Eilenberg-Zilber map]] has a [[left inverse]] given by the [[Alexander-Whitney map]] $AW$ (see at *[[Eilenberg-Zilber/Alexander-Whitney deformation retraction]]*), the analogous composite with $AW_S$ instead of $EZ_S$ yields a left inverse morphism, which hence [[retraction|retracts]] the [[homotopy groups]] of $B^n A \times B^{n-1}A$ onto those of $\big[S, B^n A \big]$. 
But, by (eq:FreeLoopSpaceOfClassifyingSpaceOfAbelianSimplicialGroup), the latter is a product of [[Eilenberg-MacLane spaces]]
with homotopy groups $A$ concentrated in degrees $n$ and $n -1 $. By assumption on $A$ the only retractions of $A$ onto itself is the identity, so that $EZ_S$ must induce the identity morphism of homotopy groups. 
\end{proof}



## Proof of the component formula
 {#ProofOfTheComponentFormula}

We prove that the formula (eq:SumFormulaForTransgressedCocycle) indeed expresses transgression in group cohomology. 

\begin{proof}

Consider the following sequence of [[natural isomorphisms]] of [[hom-sets]] of the above [[homotopy categories]] (Def. \ref{HomotopyCategories}):

\[
  \label{TransgressionDecomposed}
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
      \overline{W}G, \, undrlng \circ DK\big( A[n] \big)
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
      [S,\overline{W}G],\, \, \big[S, undrlng \circ DK\big( A[n] \big)\big]
    \Big)
    \\
    & 
    \;\simeq\;
    Ho(sSet)
    \Big(
      [S,\overline{W}G] \times S,
      \, undrlng \circ DK\big( A[n] \big)  
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
    Ho(Ch_+)
    \Big(
      N_\bullet \circ \mathbb{Z}\big( [S, \overline{W}G] \times S \big),
      \,
      A[n]
    \Big)    
    \\
    &
    \;\overset{EZ}{\simeq}\;
    Ho(Ch_+)
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
    Ho(Ch_+)
    \Big(
      N_\bullet \circ \mathbb{Z}\big([S, \overline{W}G]\big),
      \,
      A[n] \oplus A[n-1]
    \Big)    
    \\
    & 
    \;\overset{pr_2}{\to}\;
    Ho(Ch_+)
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
\]

Here 

* the first three lines recall the identification from Prop. \ref{GroupCohomologyIsOrdinaryCohomologyOfClassifyingSpace};

* the fourth line is the [component function](functor#eq:ComponentFunctionOnHomSets) on [[hom-sets]] of the [[derived functor|derived]] [[internal hom]]/[[simplicial mapping complex]]-[[functor]] out of the [[minimal simplicial circle]] $S$ (Def. \ref{MinimalSimplicialCircle});

* the fifth line is the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the derived [[free abelian group|free]] [[simplicial abelian group]]-adjunction (eq:DerivedFreeSimplicialAbelianGroupAdjunction);

* the sixth line is the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the derived [[Dold-Kan equivalence]] (eq:DerivedDoldKanAdjunction);

* the seventh line is pre-composition with the [[Eilenberg-Zilber map]], using that this is a [[quasi-isomorphism]] (and hence an [[isomorphism]] in the [[homotopy category]] [[model structure on connective chain complexes|on chain complexes]]) by the [[Eilenberg-Zilber theorem]];

  under the brace we are using Prop. \ref{NormalizedChainComplexOfMinimalSimplicialCircle};

* the eighth line is the [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of the derived degree-shift adjunction (eq:DerivedDegreeShiftAdjunction)

  (observing that the [[tensor product of chain complexes|tensor product]] of [[normalized chain complexes]] of [[free simplicial abelian groups]] is a [[cofibrant object|cofibrant]] representative of the correct [[derived functor]]-image -- using that all simplicial sets are [[cofibrant object|cofibrant]], that $\mathbb{Z}(-)$ and $N_\bullet$ are [[left Quillen functors]], and that $(Ch_+, \otimes)$ is a [[monoidal model category]] ([this Prop.](model+structure+on+chain+complexes#ProjectiveModelStructureOnConnectiveChainComplexesIsMonoidal)), so that the [[tensor product of chain complexes|tensor product]] with $\mathbb{Z} \oplus \mathbb{Z}[1]$ is the correct [[left derived functor]]);

* the ninth line is the [[projection]] onto the second [[direct sum|direct summand]];

* the last line is Def. \ref{GroupoidCohomology} of [[groupoid cohomology]].

[[diagram chase|Chasing]] a group cocycle (Def. \ref{GroupCohomology}) through this sequence, and using Prop. \ref{FormOfTheSimplicialEvaluationMap} when it gets sent through the [[Eilenberg-Zilber map]], manifestly outputs the sum formula (eq:SumFormulaForTransgressedCocycle) to be proven. 

Hence it only remains to see that this concrete composite (eq:TransgressionDecomposed) is equal to the abstractly defined transgression map (Def. \ref{Transgression}). 

{#VerifyingTheMapIsCorrect} This follows by Prop. \ref{FreeLoopSpaceOfEMSpaceIdentifiedViaEilenbergZilber}. In detail, since:

1. $A[n] \in Ch_+$ is a [[fibrant object]] (like every object in the projective [[model structure on connective chain complexes]]);

1. $[S,\overline{W}G] \in sSet$ is a [[cofibrant objects]] (like every object in the [[classical model structure on simplicial sets]]);

the chain of hom-isomorphisms of [[derived adjunctions]] in (eq:TransgressionDecomposed) is covered (through the [[quotient]] by [[left homotopy]] that defines the [[homotopy category of a model category]] according to [this Lemma](homotopy+category+of+a+model+category#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)) by "the same" chain of hom-isomorphisms of plain adjunctions. Using here that every simplicial set $X$ is the [[colimit]] over its [[category of elements|elements]] $\Delta[k] \in el(X)$ ([this Prop.](simplicial+set#SimplicialSetIsColimitOfItsSimplices)) and that the [[1-category]]-theoretic [[hom functors]] turn this colimit, in their first argument, into a [[limit]] ([this Prop.](hom-functor+preserves+limits#HomFunctorPreservesLimits)), we find that the composite in (eq:TransgressionDecomposed) is covered by

$$
  \begin{aligned}
    &
    sSet
    \Big(
      \big[S, \overline{W}G \big], 
      \,
      \big[S, undrlng \circ DK(A[n]) \big]
    \Big)
    \\
    & \;\simeq\;
    sSet
    \Big(
      \underset{
        \underset{
          \mathclap{
            {\Delta[k] \in}
            \atop
            {el\big([S,\overline{W}G]\big)}
          }
        }
        {\longrightarrow}
      }{\lim}
      \Delta[k], 
      \,
      \big[S, undrlng \circ DK(A[n]) \big]
    \Big)    
    \\
    & \;\simeq\;
    \underset{
      \underset{
        \mathclap{
          {\Delta[k] \in}
          \atop
          {el\big([S,\overline{W}G]\big)}
        }
      }
      {\longleftarrow}
    }{\lim}
    \,
    sSet
    \Big(
      \Delta[k], 
      \,
      \big[S, undrlng \circ DK(A[n]) \big]
    \Big)    
    \\
    & \;\simeq\;
    \underset{
      \underset{
        \mathclap{
          {\Delta[k] \in}
          \atop
          {el\big([S,\overline{W}G]\big)}
        }
      }
      {\longleftarrow}
    }{\lim}
    \,
    Ch_+
    \Big(
      N_\bullet \circ \mathbb{Z}
      \big(
        S \times \Delta[k] 
      \big), 
      \,
      A[n]
    \Big)    
    \\
    & \;\xrightarrow{EZ_S}\;
    \underset{
      \underset{
        \mathclap{
          {\Delta[k] \in}
          \atop
          {el\big([S,\overline{W}G]\big)}
        }
      }
      {\longleftarrow}
    }{\lim}
    \,
    Ch_+
    \Big(
      N_\bullet \circ \mathbb{Z}(S)
      \,\otimes\,
      N_\bullet \circ \mathbb{Z}(\Delta[k]),
      \,
      A[n]
    \Big)    
    \\
    & \;\simeq\;
    \underset{
      \underset{
        \mathclap{
          {\Delta[k] \in}
          \atop
          {el\big([S,\overline{W}G]\big)}
        }
      }
      {\longleftarrow}
    }{\lim}
    \,
    sSet
    \Big(
      \Delta[k],
      \,
      undrlng \circ DK
      \big(
        A[n] \oplus A[n-1] 
      \big)
    \Big)    
    \\
    & \;\simeq\;
    sSet
    \Big(
    \underset{
      \underset{
        \mathclap{
          {\Delta[k] \in}
          \atop
          {el\big([S,\overline{W}G]\big)}
        }
      }
      {\longrightarrow}
    }{\lim}
      \Delta[k],
      \,
      undrlng \circ DK
      \big(
        A[n] \oplus A[n-1] 
      \big)
    \Big)    
    \\
    & \;\simeq\;
    sSet
    \Big(
      [S,\overline{W}G],
      \,
      undrlng \circ DK
      \big(
        A[n] \oplus A[n-1] 
      \big)
    \Big)    
    \,.
  \end{aligned}
$$

This is manifestly the image under $sSet\big( [S,\overline{W}G], - \big)$ of the correct morphism (eq:ComparisonMorphismFromFreeLoopSpaceViaEilenbergZilber) from Prop. \ref{FreeLoopSpaceOfEMSpaceIdentifiedViaEilenbergZilber}.
\end{proof}

## References

The transgression map is alluded to in 

* {#DijkgraafWitten90} [[Robbert Dijkgraaf]], [[Edward Witten]], p. 14 of: _[[DW.pdf:file]]_, Commun. Math. Phys. __129__ (1990) 393 ([euclid:cmp/1104180750](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-129/issue-2/Topological-gauge-theories-and-group-cohomology/cmp/1104180750.full))

An indication of a proof, implicitly using ingredients of the [[Eilenberg-Zilber map]] (re-discovered under the name "Parmesan map"):

* {#Willerton08} [[Simon Willerton]], Section 1 of: *The twisted Drinfeld double of a finite group via gerbes and finite groupoids*, Algebr. Geom. Topol. 8 (2008) 1419-1457 &lbrack;[arXiv:math/0503266](https://arxiv.org/abs/math/0503266), [doi:10.2140/agt.2008.8.1419](https://doi.org/10.2140/agt.2008.8.1419)&rbrack;

The transgression formula itself (without derivation) is also considered, in a context of [[twisted equivariant K-theory|twisted]] [[orbifold K-theory]], in:

* [[Alejandro Adem]], [[Yongbin Ruan]], [[Bin Zhang]], Section 4 of: _A Stringy Product on Twisted Orbifold K-theory_, Morfismos (10th Anniversary Issue), Vol. 11, No 2 (2007), 33-64.  ([arXiv:math/0605534](https://arxiv.org/abs/math/0605534), [Morfismos pdf](www.morfismos.cinvestav.mx/Portals/morfismos/SiteDocs/Articulos/Volumen11/No2/Zhang/arz.pdf))

* [[Jean-Louis Tu]], [[Ping Xu]], Section 3 of: *The ring structure for equivariant twisted K-theory*, J. Reine Angew. Math. 635 (2009), 97–148 ([arXiv:math/0604160](https://arxiv.org/abs/math/0604160), [doi:10.1515/CRELLE.2009.077](https://doi.org/10.1515/CRELLE.2009.077))

and specifically in the context of equivariant [[Tate K-theory]]:

* {#Dove19} [[Thomas Dove]], _Twisted Equivariant Tate K-Theory_ ([arXiv:1912.02374](https://arxiv.org/abs/1912.02374))


Generalization to Real $\mathbb{Z}/2$-equivariant cohomology (as appropriate for [[twisted cohomology|twists]] of [[KR-theory]]):

* [[Behrang Noohi]], [[Matthew B. Young]], *Twisted loop transgression and higher Jandl gerbes over finite groupoids*, Algebr. Geom. Topol. **22** (2022) 1663-1712 &lbrack;[arXiv:1910.01422](https://arxiv.org/abs/1910.01422), [doi:10.2140/agt.2022.22.1663](https://doi.org/10.2140/agt.2022.22.1663)&rbrack;

The above discussion and proof that transgression is essentially the [[internal hom]] out of the circle into the cocycle-as-a-functor is taken from:

* {#SatiSchreiber22} [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Cyclification of Orbifolds]]*, Comm. Math. Phys. **405** 67 (2024) &lbrack;[doi:10.1007/s00220-023-04929-w](https://doi.org/10.1007/s00220-023-04929-w), [arXiv:2212.13836](https://arxiv.org/abs/2212.13836), [[schreiber:cyclic loop spaces 2022|talk]]&rbrack;



following earlier observations in:

* [[Urs Schreiber]], [[Zoran Škoda]], [§8.2](https://arxiv.org/pdf/1004.2472.pdf#page=37) & [§9.6.2](https://arxiv.org/pdf/1004.2472.pdf#page=47) of: *Categorified symmetries* &lbrack;[arXiv:1004.2472](https://arxiv.org/abs/1004.2472)&rbrack;


[[!redirects transgressions in group cohomology]]

[[!redirects transgression of group cocycles]]
[[!redirects transgressions of group cocycles]]
