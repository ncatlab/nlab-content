
## Idea

For $G$ a [[discrete group]] (often taken to be a [[finite group]]), and for $A$ any [[abelian group]] there is a [[transgression]] [[homomorphism]]

\[
  \label{TransgressionMapOnGroupCohomology}
  H_{grp}^{\bullet + 1}(G,A)
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
  H^n_{grp}\big(C_g, A \big)
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

this induces in particular a [[corestriction|corestricted]] transgression map withing the [[group cohomology]] of $G$:

$$
  H_{grp}^{\bullet + 1}(G,A)
  \longrightarrow
  H_{grp}^{\bullet}(G,A)
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

The historically influential example of this formula is the case $n=4$, $A = \mathbb{Z}$ or, equivalently, $n = 3$, $A = $ [[U(1)]], which:

* implicitly underlies ([Dijkgraaf & Witten 1990, p. 24](#DijkgraafWitten90)) the discussion of [[Dijkgraaf-Witten theory]], 

* explains ([Willerton 2008](#Willerton08)) the nature of the "twisted [[Drinfeld double]]" of the [[group algebra]] of $G$;

* governs the expression ([Dove 2019, Sec. 6.4](#Dove19)) of 4-twisted [[equivariant elliptic cohomology]] at the [[Tate curve]] in terms of 3-[[twisted equivariant K-theory|twisted equivariant]] [[Tate K-theory]].

Below we mean to spell out a general abstract definition of the transgression map (eq:TransgressionMapOnGroupCohomology) and a full proof of its component formula (eq:SumFormulaForTransgressedCocycle), amplifying that its form is a direct consequence of -- besides some basic [[homotopy theory]]/[[homological algebra]] -- the classical [[Eilenberg-Zilber theorem]] (which was partially re-discovered in [Willerton 2008, Sec. 1](#Willerton08)).


\linebreak

and for $[c] \in H^{n+1}_{grp}(G, A) \;\simeq\; H^n(B G, A)$ an $(n+1)$-[[cocycle]] in the [[group cohomology]] of $G$


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



$$
  \Delta[n+1]
  \longrightarrow
  [S,\overline{W}] \times S
$$

$$
  (\phi,j)
  \;\in\;
  Hom(\Delta[n+1] \times S, \overline{W}) 
  \times
  Hom(\Delta[n+1], S)
$$


\begin{proposition}
  The [[evaluation map]]
  $$
    [S,\overline{W}G] \times S
    \xrightarrow{\;\;}
    \overline{W}G
  $$
  (out of the [[product of simplicial sets|product]] of the [[simplicial hom complex]] out of $S$ with $S$)
  takes any non-degenerate $n+1$-simplex of $[S,\overline{W}G] \times S$
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
    }
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


  \begin{tikzcd}
    \scalebox{.8}{$
      \left( {[0]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[0,0]}
        \atop
        {[0,1]}
        \right)
      }"{above, scale=.8}
    ]
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[0,0]}
        \right)
      }"{left, scale=.8}
    ]
    \ar[
      ddrr,
      "{
        \left(
        { [0,1] }
        \atop
        { [0,1] }
        \right)
      }"{description, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[0]} \atop {[1]} \right)
    $}
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[1,1]}
        \right)
      }"{right, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,0,1] }
        \atop
        { [0,1,1] }
        \right)
      }"{pos=.15, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,1,1] }
        \atop
        { [0,0,1] }
        \right)
      }"{pos=.85, scale=.8}
    ]
    \\
    \\
    \scalebox{.8}{$
      \left( {[1]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[1,1]}
        \atop
        {[0,1]}
        \right)
      }"{below, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[1]} \atop {[1]} \right)    
    $}
  \end{tikzcd}


The non-degenerate (n+1)-simplices of 
$\begin{aligned} & \Delta[1] \\ \times & \Delta[n] \end{aligned}$ are

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$


$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$



$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 0 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 3 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$



$$
  \array{
    Hom(\Delta[1] \times \Delta[n], \overline{W}G)
    \times
    Hom(\Delta[n],\Delta[1])
    &&
    Hom(\Delta[n],\overline{W}G)  
    \\
    (\gamma, g_{n-1}, \cdots, g_0), 
    (0,\cdots, 0, 1, \cdots, 1)
    &&
  }
$$

$$
  \array{
    (\gamma, g_{n-1}, \cdots, g_1, g_0)
    \;\colon\;
    &
    \Delta[1] \times \Delta[n]
    &\longrightarrow&
    \overline{W}G
    \\
    &
    \big(
       [0, \cdots, 0, 1, \cdots, 1], ([0,1,\cdots, n])
    \big)
    &\mapsto&
    ( )
  }
$$
   

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

## References

* {#DijkgraafWitten90} [[Robbert Dijkgraaf]], [[Edward Witten]], _[[DW.pdf:file]]_, Commun. Math. Phys. __129__ (1990) 393 ([euclid:cmp/1104180750](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-129/issue-2/Topological-gauge-theories-and-group-cohomology/cmp/1104180750.full))


* {#Willerton08} [[Simon Willerton]], Section 1 of: *The twisted Drinfeld double of a finite group via gerbes and finite groupoids*, Algebr. Geom. Topol. 8 (2008) 1419-1457 ([arXiv:math/0503266](https://arxiv.org/abs/math/0503266))

* [[Jean-Louis Tu]], [[Ping Xu]], Section 3 of: *The ring structure for equivariant twisted K-theory*, J. Reine Angew. Math. 635 (2009), 97–148 ([arXiv:math/0604160](https://arxiv.org/abs/math/0604160), [doi:10.1515/CRELLE.2009.077](https://doi.org/10.1515/CRELLE.2009.077))

* [[Alejandro Adem]], [[Yongbin Ruan]], [[Bin Zhang]], Section 4 of: _A Stringy Product on Twisted Orbifold K-theory_, Morfismos (10th Anniversary Issue), Vol. 11, No 2 (2007), 33-64.  ([arXiv:math/0605534](https://arxiv.org/abs/math/0605534), [Morfismos pdf](www.morfismos.cinvestav.mx/Portals/morfismos/SiteDocs/Articulos/Volumen11/No2/Zhang/arz.pdf))

* {#Dove19} [[Thomas Dove]], _Twisted Equivariant Tate K-Theory_ ([arXiv:1912.02374](https://arxiv.org/abs/1912.02374))
