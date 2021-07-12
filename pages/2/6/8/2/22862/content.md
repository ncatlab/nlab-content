
> under construction

#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[discrete group]] (often taken to be a [[finite group]]), and for $A$ any [[abelian group]] there is a [[transgression]] [[homomorphism]]

\[
  \label{TransgressionMapOnGroupCohomology}
  H_{grp}^{\bullet + 1}(G;\,A)
  \;=\;
  H^{\bullet + 1}(B G;\, A)
  \xrightarrow{ \tau }
  H^n
  \big(
    \Lambda B G,
    \,
    A
  \big)
  \;\simeq\;
  \underset{
    [g] \in G^{ad}/G
  }{\oplus}
  H^n_{grp}\big(C_g;\, A \big)
\]

from the [[group cohomology]] of $G$ to the [[groupoid cohomology]], in one degree lower,  of the [[inertia groupoid]]  $\Lambda B G$ of its [[delooping groupoid]] $B G \simeq (G \rightrightarrows G)$.

Since the [[inertia groupoid]] of the [[delooping groupoid]] is [[equivalence of groupoids|equivalent]] to a [[disjoint union]] over [[conjugacy classes]] $[g] \in G^{ad}/G$ of [[delooping groupoids]] of [[centralizer subgroups]] $C_g$ with $C_e = G$

\[
  \label{DecompositionOfTheInertiaGroupoid}
  \Lambda B G
  \;\simeq\;
  \underset{ [g] \in G_{ad}/G }{\coprod}
  B C_g
  \;\simeq\;
  B G \,\sqcup\, 
  \underset{ [g] \neq [e] }{\coprod}
  B C_g
\]

this induces in particular a [[corestriction|corestricted]] transgression map within the [[group cohomology]] of $G$, or, generally, to the [[group cohomology]] of its [[centralizer subgroups]]:

$$
  H_{grp}^{\bullet + 1}(G;\,A)
  \xrightarrow{ \tau_{[e]} }
  H_{grp}^{\bullet}(G;\,A)
  \,,
  \;\;\;\;\;\;\;
  H_{grp}^{\bullet + 1}(G,A)
  \xrightarrow{ \tau_{[g]} }
  H_{grp}^{\bullet}(C_g;\,A)
  \,.
$$

It is a [[folklore]] [[theorem]] that the transgression (eq:TransgressionMapOnGroupCohomology) maps an $(n+1)$-cocycle $c \colon G^{\times_{n+1}} \to A$ to the alternating sum

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

where we use the shorthand

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

(which restricts to $Ad_j(\gamma) = \gamma$ upon [[corestriction]] the connected components on the right of (eq:DecompositionOfTheInertiaGroupoid)).

In historically influential examples, this formula (all for the case $n=4$, $A = \mathbb{Z}$ or, equivalently, $n = 3$, $A = $ [[U(1)]]):

* implicitly underlies ([Dijkgraaf & Witten 1990, p. 24](#DijkgraafWitten90)) the discussion of [[Dijkgraaf-Witten theory]], 

* explains ([Willerton 2008](#Willerton08)) the nature of the "twisted [[Drinfeld double]]" of the [[group algebra]] of $G$;

* governs the expression ([Dove 2019, Sec. 6.4](#Dove19)) of 4-twisted [[equivariant elliptic cohomology]] at the [[Tate curve]] in terms of 3-[[twisted equivariant K-theory|twisted equivariant]] [[Tate K-theory]].

Below we mean to spell out a general abstract definition of the transgression map (eq:TransgressionMapOnGroupCohomology) and a full proof of its component formula (eq:SumFormulaForTransgressedCocycle), amplifying that its form is a direct consequence of -- besides some basic [[homotopy theory]]/[[homological algebra]] -- the classical [[Eilenberg-Zilber theorem]] (which was partially re-discovered in [Willerton 2008, Sec. 1](#Willerton08)).


\linebreak

## Lemmas

### Products of simplices

We have the following fundamental fact about [[products of simplices]] (see there for more):

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

(e.g. [Kerodon 2.5.7.2](#Kerodon): [00RH](https://kerodon.net/tag/00RH))

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
From Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise} 
it is clear (Rem. \ref{DegenerateSimplicesInProductOfSimplicialSets}) that a 
simplex $\sigma$ (eq:GenericSimplexInProductOfSimplices) is degenerate 
precisely if, when regarded as a path as above, it contains a [[constant function|constant]] step, i.e. one which moves neither horizontally nor vertically. But then -- by degree reasons, since we are looking at paths of $p + q$ steps in a lattice of side length $p$ and $q$ -- it must be that the path proceeds by $p + q$ unit steps. 
\end{proof}

### Nerve of the inertia groupoid

We have the following basic facts about the [[inertia groupoid]] (see there for more):

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
For notational brevity we will be referring to $\overline{W}G$ in the following, but it may be helpful to keep thinking of the nerve of the delooping groupoid. 
From that perspective, an [[n-simplex]] in $\overline{W}G$, which is an [[n-tuple]] of group elements, is suggestively denoted as a sequence of composable arrows:

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


\begin{proposition}
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
**(minimal simplicial circle)** \linebreak
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

The following proposition follows on abstract grounds, but the explicit component-based proof we give is necessary in order to understand the [[transgression]]-formula for [[cocycles]] in the [[group cohomology]] of $G$ to cocycles on the inertia groupoid.
\begin{proposition}\label{RelationToSimplicialHomComplexIntoClassifyingSpace}
The [[nerve]] of the inertia groupoid of a delooping groupoid of a [[finite group]] $G$ is [[isomorphism|isomorphic]] to the [[simplicial hom complex]] out of the minimal simplicial circle $S$ (Def. \ref{MinimalSimplicialCircle}) into the [[simplicial classifying space]] $\overline{W}G$ (Rem. \ref{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}):

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


## Proof

We have the following sequence of [[natural isomorphisms]], which are

* [hom-isomorphisms](adjoint+functor#InTermsOfHomIsomorphism) of [[derived adjunctions]] of

  * the [[Dold-Kan correspondence]],

  * the [[free abelian group]]/[[forgetful functor]]-adjunction,

* the [[Eilenberg-Zilber theorem]]:

$$
  \begin{aligned}
    H^n
    \big(
      B G; A
    \big)
    &
    \;=\;
    Ho(sSet)
    \big(
      N \circ \mathbb{Z}(\overline{W}G),
      \,
      A[n]
    \big)
    \\
    &
    \;\simeq\;
    Ho(sSet)
    \big(
      \overline{W}G; \, undrlg \circ DK\big( A[n] \big)
    \big)
    \\
    &
    \;\overset{[S,-]}{\to}\;
    Ho(sSet)
    \big(
      [S,\overline{W}G];\, \, \big[S,undrlg \circ DK\big( A[n] \big)\big]
    \big)
    \\
    & 
    \;\simeq\;
    Ho(sSet)
    \Big(
      [S,\overline{W}G] \times S,
      \, undrlg \circ DK\big( A[n] \big)  
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
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N \circ \mathbb{Z}\big( [S, \overline{W}G] \times S \big),
      \,
      A[n]
    \Big)    
    \\
    &
    \;\overset{EZ}{\simeq}\;
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N\circ \mathbb{Z}\big([S, \overline{W}G]\big) 
        \otimes 
      \underset{\mathbb{Z}[1]}{\underbrace{N \circ \mathbb{Z}(S)}},
      \,
      A[n]
    \Big)    
    \\
    &
    \;\simeq\;
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N\circ \mathbb{Z}\big([S, \overline{W}G]\big),
      \,
      A[n] \oplus A[n-1]
    \Big)    
    \\
    & 
    \;\overset{pr_2}{\to}\;
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N\circ \mathbb{Z}\big([S, \overline{W}G]\big),
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
  \end{aligned}
$$

Chasing a cocycle through this sequence and using Prop. \ref{FormOfTheSimplicialEvaluationMap} when it gets to go through the [[Eilenberg-Zilber map]] yields (eq:SumFormulaForTransgressedCocycle).


## References

* {#DijkgraafWitten90} [[Robbert Dijkgraaf]], [[Edward Witten]], _[[DW.pdf:file]]_, Commun. Math. Phys. __129__ (1990) 393 ([euclid:cmp/1104180750](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-129/issue-2/Topological-gauge-theories-and-group-cohomology/cmp/1104180750.full))


* {#Willerton08} [[Simon Willerton]], Section 1 of: *The twisted Drinfeld double of a finite group via gerbes and finite groupoids*, Algebr. Geom. Topol. 8 (2008) 1419-1457 ([arXiv:math/0503266](https://arxiv.org/abs/math/0503266))

* [[Jean-Louis Tu]], [[Ping Xu]], Section 3 of: *The ring structure for equivariant twisted K-theory*, J. Reine Angew. Math. 635 (2009), 97–148 ([arXiv:math/0604160](https://arxiv.org/abs/math/0604160), [doi:10.1515/CRELLE.2009.077](https://doi.org/10.1515/CRELLE.2009.077))

* [[Alejandro Adem]], [[Yongbin Ruan]], [[Bin Zhang]], Section 4 of: _A Stringy Product on Twisted Orbifold K-theory_, Morfismos (10th Anniversary Issue), Vol. 11, No 2 (2007), 33-64.  ([arXiv:math/0605534](https://arxiv.org/abs/math/0605534), [Morfismos pdf](www.morfismos.cinvestav.mx/Portals/morfismos/SiteDocs/Articulos/Volumen11/No2/Zhang/arz.pdf))

* {#Dove19} [[Thomas Dove]], _Twisted Equivariant Tate K-Theory_ ([arXiv:1912.02374](https://arxiv.org/abs/1912.02374))
