
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mapping spaces
+--{: .hide}
[[!include mapping space - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In [[categories]] of [[simplicial objects]], like [[SimplicialSets]], the [[sSet]]-valued [[hom-object]] between two [[objects]] is often called the _function complex_ (“[[simplicial complex]] of [[functions]] from $X$ to $Y$”).

The *[[function complex]]* of two [[simplicial sets]] is the collection of [[maps]], [[left homotopies]] and [[higher homotopies]] between them, all itself organized into a simplicial set.

More formally, [[SimplicialSets]] is a [[Cartesian monoidal category]] and the corresponding [[internal hom]] is what is traditionally known as the function complex.


## Definition

### General
 {#GeneralDefinition}

Suppose $\mathcal{C}$ is a [[category]] that admits small [[coproducts]].

Given [[simplicial objects]] $X,A\in \mathcal{C}^{\Delta^{op}}$,
their __function complex__ is the [[simplicial set]]

$$
  Hom_{\Delta}(X,A)
  \;\;
  \in
  \;\;
  sSet
$$

whose set of $n$-simplices is the set of maps
$\Delta^n\otimes A\to B$

$$
  \big(
    Hom_{\Delta}(X,A)  
  \big)_n
  \;\;
  =
  \;\;
  Hom_{\mathcal{C}}
  \big(
    \Delta^n \otimes X 
    ,\,
    A
  \big)
  \,,
$$

where $\otimes$ denotes the [[copowering]] of [[simplicial objects]] over [[simplicial sets]] given by

$$
  (S \otimes X)_n 
  \,=\,
  \coprod_{i \in S_n}
  X_n
  \,.
$$

### In simplicial sets
 {#InSimplicialSets}

Specializing the general definition above to $\mathcal{C} = $ [[sSet]] itself, the required tensoring is just the [[product of simplicial sets]] and so

\begin{definition}\label{FunctionComplexOfSimplicialSets}
\linebreak
The function complex between [[simplicial sets]] $X, A$ is the [[cartesian closed category|cartesian]] [[internal hom]] given by

$$
  X, A \,\in\, sSet
  \;\;\;\;
  \vdash
  \;\;\;\;
  \left\{
  \,
  \begin{array}{l}
    Maps(X,A)
    \;\; \in \;\; 
    sSet
    \\
    Maps(X,A)_\bullet
    \;\; = \;\; 
    Hom_{sSet}\big(
      \Delta[\bullet] \times X 
      ,\,
      A
    \big)
  \end{array}
  \right.
$$
\end{definition}
(e.g. [Goerss & Jardine (2009), I.5](#GoerssJardine09))


## Properties
 {#Properties}

### In simplicial sets


\begin{proposition}\label{ComponentFormulaForEvaluationMap}
**(component formula for [[evaluation map]] on [[function complexes]])**
\linebreak
In [[SimplicialSets]], the [[evaluation map]] of the function complex (from Def. \ref{FunctionComplexOfSimplicialSets}) --- defined as the [[counit of an adjunction|counit]] of the $\big(X \times (-)\big)\dashv Maps(X,-)$-[[adjoint functor|adjunction]] ---  is given by:

$$
  \begin{array}{cc}
    X \times Maps(X,A) 
    &\xrightarrow{\;\; ev^X_A  \;\;}&
    A
    \\
    \phantom{A}
    \\
    X_n 
      \times 
    \overset{
      \mathclap{
        Hom(X \times \Delta[n], A)
      }
    }{
      \overbrace{
        Maps(X,A)_n
      }
    }
    &\xrightarrow{\; \big(ev^X_A\big)_n  \;}&
    A_n
    \\
    \big(
      x 
      ,\, 
      f 
    \big)    
    &\mapsto&
    f(x, \iota_n)
    \,,
  \end{array}
$$

where 

$$
  \iota_n 
     \;\coloneqq\; 
  id_{\Delta[n]}
  \;\in\;
  Hom_{sSet}\big( \Delta[n],\, \Delta[n] \big)
  \;\simeq\;
  (\Delta[n])_n
$$

denotes the unique non-degenerate $n$-cell inside $\Delta[n]$.
\end{proposition}
(e.g. [Goerss & Jardine (2009), p. 20](#GoerssJardine09))

\begin{proposition}\label{NerveOfCategoriesPreservesMappingObjects}
**(simplicial nerve intertwines function complexes with functor categories)**
\linebreak

Let $\mathcal{X}, \mathcal{A}$ be [[small categories|small]] [[strict category|strict]] [[categories]] and write $Maps(\mathcal{X}, \mathcal{A})$ for their [[functor category]]. Then under the [[simplicial nerve]]
$
  N \;\colon\; Cat^{sm} \longrightarrow sSet
$
this is [[isomorphic]] to the function complex (Def. \ref{FunctionComplexOfSimplicialSets}) between their separate [[simplicial nerves]]:

$$
  N 
  \big(
    Maps(\mathcal{X},\,\mathcal{A})
  \big)
  \;\simeq\;
  Maps
  \big(
    N(\mathcal{X})
    ,\,
    N(\mathcal{A})
  \big)
  \,.
$$

\end{proposition}
(For the proof see [here](nerve#NerveOfCategoriesPreservesMappingObjects) at *[[nerve]]*.)

## Examples

### General

\begin{example}\label{MappingComplexBetweenNervesOfGroupoids}
**([[simplicial mapping complex]] between [[nerves]] of [[groupoids]])**
For $N(\mathcal{G}_i)$ the [[nerves]] of [[groupoids]], their simplicial mapping complex is [[isomorphism|isomorphic]] to the [[nerve]] of the [[functor groupoid]] from $\mathcal{G}_1$ to $\mathcal{G}_2$:

$$
  \big[
    N(\mathcal{G}_1),
    \,
    N(\mathcal{G}_2)
  \big]
  \;\;
  \simeq
  \;\;
  N
  \big(
    Func(\mathcal{G}_1, \, \mathcal{G}_2)
  \big)
  \;\;\;
  \in
  \;
  SimplicialSets
$$
\end{example}


### Nerves of inertia groupoids

\begin{example}\label{EvaluationMapOnNervesOfInertiaGroupoids}
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

The [[simplicial nerve]] of this functor groupoid is the following [[function complex]] of [[simplicial sets]] (using Prop. \ref{NerveOfCategoriesPreservesMappingObjects}):
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


This is the type of mapping that appears in the component formula for the [[evaluation map]] on [[function complexes]] (from Prop. \ref{ComponentFormulaForEvaluationMap}). Hence we find that this evaluation map is given on non-degenerate $(n+1)$-simplices in the product (see again [there](product+of+simplices#NonDegenerateCellsInAProductOfSimplices)) as follows:

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


## Related concepts

* [[internal hom]]

* [[simplicial object]]

* [[simplicial set]]

## Related concepts

* [[mapping space]], [[mapping complex]]

* [[derived mapping space]]

## References

The original definition of a function complex in the generality stated above:

* [[Daniel M. Kan]], _On c.s.s. categories_, Boletín de la Sociedad Matemática Mexicana 2 (1957), 82–94.  [PDF](https://dmitripavlov.org/scans/kan-on-css-categories.pdf).

In function complxes in the generality of [[simplicial presheaves]]

* [[William Dwyer]], [[Daniel Kan]], *Function complexes for diagrams of simplicial sets*, Indagationes Mathematicae (Proceedings) **86** 2 (1983) 139-147 &lbrack;<a href="https://doi.org/10.1016/1385-7258(83)90051-3">doi:10.1016/1385-7258(83)90051-3</a>, [pdf](https://core.ac.uk/download/pdf/82652265.pdf)&rbrack;


Textbook account in [[simplicial homotopy theory]]:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section I.5 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack;

Introduction with an eye towards [[quasicategories]]:

* {#Rezk22} [[Charles Rezk]], Section 15 of: *Introduction to quasicategories* (2022) &lbrack;[pdf](https://faculty.math.illinois.edu/~rezk/quasicats.pdf), [[Rezk-IntroToQuasicategories.pdf:file]]&rbrack;


[[!redirects function complexes]]


[[!redirects simplicial mapping complex]]
[[!redirects simplicial mapping complexes]]

[[!redirects simplicial hom complex]]
[[!redirects simplicial hom complexes]]

[[!redirects simplicial hom-complex]]
[[!redirects simplicial hom-complexes]]

