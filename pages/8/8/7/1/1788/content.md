

\begin{example}
**([[evaluation map]] on [[function complexes]] which are [[nerves]] of [[inertia groupoids]])**
\linebreak

Consider a [[discrete group]] $G$. 

We write $\mathbf{B}G$ for its [[delooping groupoid]], here specifically for its [[strict category|strict]] version $\mathbf{B}G \,\coloneqq\,\big(G \rightrightarrows \ast \big)$. The [[nerve]] of this groupoid is the canonical model for the [[simplicial classifying space]]:
$
  N \mathbf{B}G \,=\, \overline{W}G
  \,.
$

The [[functor groupoid]]
$$
  \Lambda \mathbf{B}G
  \;\coloneqq\;
  Maps\big(
    \mathbf{B}\mathbb{Z}    
    ,\,
    \mathbf{B}G
  \big)
$$
is also known as the *[[inertia groupoid]]* of $\mathbf{B}G$. 

The [[simplicial nerve]] of this functor groupoid is the following [[function complex]] of [[simplicial sets]] (using [this Prop.](nerve#NerveOfCategoriesPreservesMappingObjects)):
$$
  N \Lambda \mathbf{B}G
  \;\coloneqq\;
  Maps\big(
    N \mathbf{B}\mathbb{Z}    
    ,\,
    N \mathbf{B}G
  \big)
  \;\simeq\;
  Maps\big(
    S
    ,\,
    N \mathbf{B}G
  \big)
  \,.
$$
Here in the second step we introduced the simplicial set
\[
  \label{MinimalSimplicialCircle}
  S 
  \;\coloneqq\;
  \Delta[1]/\partial \Delta[1]
  \;\;\;
  \in
  \;
  sSet
  \,,
\]
which is the [[minimal model]] for $\mathbf{B}\mathbb{Z}$, whose unique non-degenerate 1-cell we will denote by
$$
  \ell \;\coloneqq\; [0,1] \in \Delta[1]_1 \twoheadrightarrow S_1
$$

We now describe in detail the [[evaluation map]] on the simplicial [[function complex]]
$  
  Maps\big(
    S
    ,\,
    N \mathbf{B}G
  \big)
  \,.
$

To that end, we denote by
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

The simplicial map (eq:CellInNerveOfInertiaGroupoid) maps the non-degenerate $(n+1)$-cells in the [[product of simplicial sets]] (see the discussion there) of $S$ (eq:MinimalSimplicialCircle) with the [[simplicial simplex|simplicial $n$-simplex]] as follows:

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
    "file_name": "ActOfDegOfCellInNerveOfInertiaGrpd-221205.jpg",
    "width": "900",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This is the mapping that appears in the component formula for the [[evaluation map]] on [[function complexes]] (via Prop. \ref{ComponentFormulaForEvaluationMap}). Hence we find that this evaluation map is given on non-degenerate $(n+1)$-simplices in the product (see again [there](product+of+simplices#NonDegenerateCellsInAProductOfSimplices)) as follows:

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

The expressions on the right happen to be those that appear in the formula for [[transgression in group cohomology]], see [there](transgression+in+group+cohomology#eq:SumFormulaForTransgressedCocycle).
\end{example}