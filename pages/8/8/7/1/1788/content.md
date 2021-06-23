
\begin{example}
  Let 

  * $G \in Groups(Sets)$ 

    be a [[discrete group]],

  * $X \in G Actions(Sets)$ 

    be a $G$-[[group action|action]],

  * $\mathcal{X} \;\coloneqq\; X \sslash G \;\coloneqq\; N( X \times G \rightrightarrows X ) \,=\, X \times G^{\times^\bullet} \in sSet$ 
 
    the [[simplicial set]] which is the [[nerve]] of its [[action groupoid]] (a model for its [[homotopy quotient]]),

  * $\mathcal{G} \,\coloneqq\, \mathbf{B}\mathbb{Z} \,\coloneqq\, N(\mathbb{Z} \rightrightarrows \ast)  \,\coloneqq\, \mathbb{Z}^{\times^\bullet} \,\in\, Groups(sSet)$ 

    the [[simplicial group]] which is the [[nerve]] of the [[2-group]] that is the [[delooping groupoid]] of the additive group of [[integers]].

Then the [[functor groupoid]]

\[
  \label{InertiaGroupoidAsFunctorGroupoidOutOfBZ}
  \begin{aligned}
    \Lambda(X \!\sslash\! G)
    & \;\coloneqq\;
    \big[
      \mathbf{B}\mathbb{Z}, X \!\sslash\! G
    \big]
    \\
    &
    \;\simeq\;
    Func
    \big(  
      (\mathbb{Z} \rightrightarrows \ast),
      \,
      (X \times G \rightrightarrows X)
    \big)
    \\
    & \;\underset{\in \mathrm{W}}{\leftarrow}\;
    \underset{
      [g] \in ConjCl(G)
    }{\coprod}
    \Big(
      X^{g} \!\sslash\! C_g
    \Big)
  \end{aligned}
\]

is known as the *[[inertia groupoid]]* of $X \!\sslash\! G$. Here

$$
  ConjCla(G)
  \;\coloneqq\;
  G/_{ad} G
  \,,
  \;\;\;\;\;\;\;\;\;\;\;
  C_g 
  \;\coloneqq\;
  \big\{
    h \in G
    \,\left\vert\,
    h \cdot g = g \cdot h
    \right.
  \big\}
$$

denotes, respectively, the set of [[conjugacy classes]] of elements of $G$, and the [[centralizer]] of $\{g\} \subset G$ -- this data serves to express the [[equivalence of categories|equivalent]] [[skeleton]] of the inertia groupoid in the last line of (eq:InertiaGroupoidAsFunctorGroupoidOutOfBZ).

Now, by Prop. \ref{CofreeAction} the inertia groupoid (eq:InertiaGroupoidAsFunctorGroupoidOutOfBZ) carries a canonical [[infinity-action|2-action]] of the [[2-group]] $\mathbf{B}\mathbb{Z}$:

By the formula (eq:CofreeSimplicialActionInComponents), for $n \in \mathbb{Z}$ the 2-group element in degree 1

$$
  {\color{purple}n}
  \;\colon\;
  \Delta[1]
  \longrightarrow
  \mathbf{B}G
$$

acts on the morphisms 

$$
  (x,g) \overset{h}{\longrightarrow} (h\cdot x, g)
  \;\;\;
  \in
  \;
  \Lambda(X \!\sslash\! G)
$$

of the inertia groupoid as follows:

<img src="https://ncatlab.org/nlab/files/BZActionOnInertiaGroupoid20210623.jpg" width="800" />

\end{example}

$$
  \big(
    (1,0),
    [0,0,1]
  \big)
  \mapsto
  \big(
    (1,0),
    [0,0,1],
    [0,0,1]
  \big)
  \mapsto
  \big(
    (1,0),
    (0,n),
    [0,0,1]
  \big)
  \mapsto
  \big(
    (1,n),
    [0,0,1]
  \big)
$$


$$
  \big(
    (0,1),
    [0,1,1]
  \big)
  \mapsto
  \big(
    (0,1),
    [0,1,1],
    [0,1,1]
  \big)
  \mapsto
  \big(
    (0,1),
    (n,0),
    [0,1,1]
  \big)
  \mapsto
  \big(
    (n,1),
    [0,1,1]
  \big)
$$



\begin{tikzcd}[column sep=60pt, row sep=60pt]
  (
    \bullet
    ,
    [0]
  )
  \ar[
    r,
    "{
      (
        0
        ,
        [0,1]
      )
    }"{above}
  ]
  \ar[
    d,
    "{
      (
        1
        ,
        [0,0]
      )
    }"{left}
  ]
  \ar[
    dr,
    "{
      (
        1
        ,
        [0,1]
      )
    }"{description, sloped}
  ]
  &
  (
    \bullet
    ,
    [1]
  )
  \ar[
    d,
    "{
      (
        1
        ,
        [1,1]
      )
    }"{right}
  ]
  \ar[
    dl,
    phantom,
    "{
      (
        (1,0)
        ,
        [0,0,1]
      )
    }"{near end, scale=.7}
  ]
  \ar[
    dl,
    phantom,
    "{
      (
        (0,1)
        ,
        [0,1,1]
      )
    }"{near start, scale=.7}
  ]
  \\
  (
    \bullet
    ,
    [0]
  )
  \ar[
    r,
    "{
      (
        0
        ,
        [0,1]
      )
    }"{below}
  ]
  &
  (
    \bullet
    ,
    [1]
  )
\end{tikzcd}




Now the action

$$
  \array{
    \mathbb{Z}^{\times^\bullet}
    \times
    X^g \times (C_g)^{\times^\bullet}
    &\longrightarrow&
    X^g \times (C_g)^{\times^\bullet}
    \\
    \mathbb{Z} \times X^g \times C_g
    &\longrightarrow&
    X^g \times C_g 
    \\
    \big\downarrow \big\downarrow
    &&
    \big\downarrow \big\downarrow
    \\
    X^g 
    &\longrightarrow&
    X^g
  }
$$




$\gg$

For $\mathcal{G} \,\in\, Groups(sSets)$ a [[simplicial group]], write $\mathcal{G}Actions(sSets)$ for the [[category]] of $\mathcal{G}$-[[actions]] on [[simplicial sets]].

\begin{proposition}
  The [[forgetful functor]] $undrl$ from $\mathcal{G}Actions$ to underlying simplicial sets has a [[right adjoint]]

$$
  sSet
  \underoverset
    {\underset{ \;\;\; [\mathcal{G},-] \;\;\; }{\longrightarrow}}
    {\overset{ \;\;\; undrl \;\;\; }{\longleftarrow}}
    {\bot}
  \mathcal{G}Actions(sSet)
$$

which sends $X \in sSet$ to 

* the simplicial set 

  $$
    [\mathcal{G},X] 
    \;\coloneqq\;
    Hom_{sSet}\big( \mathcal{G} \times \Delta[\bullet], X\big) 
    \;\;\;
    \in
    sSet
  $$

* equipped with the $\mathcal{G}$-action

  $$
    \mathcal{G} \times [\mathcal{G},X]
    \longrightarrow 
    \mathcal{G}
  $$

  which in degree $n \in \mathbb{N}$ is the [[function]] 

  $$
    Hom(\Delta[n], \mathcal{G})
    \,\times\,
    Hom
    \big(
      \mathcal{G} \times \Delta[n],
      \,
      X
    \big)
    \longrightarrow
    Hom
    \big(
      \mathcal{G} \times \Delta[n],
      \,
      X
    \big)    
  $$

  that sends

  \[
  \label{CofreeSimplicialActionInComponents}
  \begin{aligned}
  &
  \Big(
    \mathcal{G}\times \Delta[n]
    \overset{\phi}{\to}
    X,
    \;
    \Delta[n] \overset{g_n}{\to} \mathcal{G}
  \Big)
  \\
  \;\;\mapsto\;\;
  &
  \Big(
  \mathcal{G} \times \Delta[n]
  \overset{id \times diag}{\longrightarrow}
  \mathcal{G} \times \Delta[n] \times \Delta[n]
  \overset{ id \times g_n \times id }{\longrightarrow}
  \mathcal{G} \times \mathcal{G} \times \Delta[n]
  \overset{(-)\cdot(-) \times id}{\to}
  \mathcal{G} \times \Delta[n]
  \overset{\phi}{\to}
   X
  \Big)
  \end{aligned}
  \]

\end{proposition} 

\begin{proof}

For $P \in \mathcal{G}Actions(sSet)$, and $X \in sSet$, we check the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism)

$$
  \big\{
    P \overset{\;\;\phi_{(-)}\;\;}{\longrightarrow} [G,X]
  \big\}
  \;\;\;\overset{ \;\; \widetilde{(-)} \;\; }{\leftrightarrow}\;\;\;
  \big\{
    undrl(P) \overset{\;\; {\widetilde \phi}_{(-)} \;\; }{\longrightarrow} X
  \big\}
  \,.
$$

Given

$$
  \phi_{(-)}
  \;\colon\;
  p_n 
  \mapsto 
  \big(
    \phi_{p_n}
    \;\colon\;
    \mathcal{G} \times \Delta[n] \to X
  \big)
$$

define

\[
  \label{AdjunctOfHomomorphismToCofreeSimplicialAction}
  \widetilde \phi_{(-)}
  \;\colon\;
  p_n 
  \mapsto
  \phi_{p_n}(e_n, \sigma_n)
  \,,
\]

where $e_n \in \mathcal{G}_n$ denotes the [[neutral element]] in degree $n \in \mathbb{N}$ and where $\sigma_n \in (\Delta[n])_n$ denotes the unique non-degenerate element $n$-cell in the [[n-simplex]].

We need to show that ${\widetilde \phi}_{(-)} \colon undrl(P) \to X$ already determines all of $\phi_{(-)}$.

Write $\sigma_n \in (\Delta[n])_n$ for the unique non-degenerate simplex in that degree, and observe that $\phi_{p_n}$ is uniquely fixed by its values  $\phi_{p_n}( -, \sigma_n )$ on this simplex. Now for any $g_n \in \mathcal{G}_n$ observe the following sequence of identifications:

$$
  \begin{aligned} 
    \phi_{p_n}(g_n, \sigma_n)
    & \;=\;
    \phi_{p_n}( e_n \cdot g_n, \sigma_n )
    \\
    & \;=\;
    \big(
      g_n \cdot \phi_{p_n}
    \big)
    ( e_n, \sigma_n )
    \\
    & \;=\;
    \phi_{ g_n \cdot p_n }
    (e_n, \sigma_n)
    \\
    & \;=\;
    {\widetilde \phi}_{g_n \cdot p_n}
  \end{aligned}
$$

Here

* the first step is the unit law in the component group $\mathcal{G}_n$;

* the second step uses the definition (eq:CofreeSimplicialActionInComponents) of the cofree action;

* the third step is the assumption that $\phi_{(-)}$ is a homomorphism of $\mathcal{G}$-actions ([[equivariant function|equivariance]]);

* the fourth step is the definition (eq:AdjunctOfHomomorphismToCofreeSimplicialAction).


\linebreak

$$
  \phi_{p_n}( e_n \cdot g_n, \sigma_n )
  \;=\;
  \phi_{ g_n \cdot p_n }( e_n, \sigma_n )
$$

\end{proof}


$$
  Hom_{sSet}
  \big(
    P, X
  \big)
  \;\longrightarrow\;
  Hom_{\mathcal{G}Acts}
  \big(
    P, [\mathcal{G}, X]
  \big)
$$

\begin{lemma}

Cofibrant resolution of 

$$
  \varnothing
  \xrightarrow{\;\;}
  N
  \big(
    (C_g \times \mathbb{R}) \times \mathbb{Z}
    \rightrightarrows
    (C_g \times \mathbb{R})
  \big)
  \xrightarrow{ \;\simeq\; }
  \Lambda_g
$$  

\end{lemma}

$$
  \big(
    X^g 
      \times 
    W
    \big( 
      (C_g \times \mathbb{R}) \sslash \mathbb{Z}
    \big)
  \big)
  \big/
  \big(
    (C_g \times \mathbb{R}) \sslash \mathbb{Z}
  \big)
  \xrightarrow{\;\;\;}
  \big(
    [B\mathbb{Z}, X \sslash G]
    \times
    W( B\mathbb{Z} )
  \big)
  \big/
  B \mathbb{Z}
$$

degree 0:

$$
  \big(
    X^g 
      \times 
    (C_g \times \mathbb{R}) 
  \big)
  \big/
  \big(
    (C_g \times \mathbb{R})
  \big)
  \xrightarrow{\;\; x \mapsto \big( (\ast \overset{1}{\to} \ast) \mapsto (x \overset{g}{\to} g) \big) \;\;}
  Hom(B\mathbb{Z}, X \sslash G)
$$


degree 1:

$$
  \big(
    X^g 
      \times 
    (C_g \times \mathbb{R})
  \xrightarrow{\;\;
    (x,h) \mapsto conjugation
  \;\;}
  Hom(B\mathbb{Z}\times \Delta[1], X \sslash G)
$$

degree 2:

$$
  \big(
    X^g 
      \times 
    \mathbb{Z}
      \times
    (C_g \times \mathbb{R})
  \xrightarrow{\;\;\;\;}
  \big(
    Hom(B\mathbb{Z} \times \Delta[2], X \sslash G)
    \times
    W( B\mathbb{Z} )
  \big)
  \big/
  B \mathbb{Z}
$$


Identify

$$
  S^1 \;\simeq\; \mathbb{R} / \mathbb{Z}
$$

consider

$$
  \mathbb{R}
  \xrightarrow{\;q\;}
  S^1
$$

$$
  \mathbb{Z}
  \times 
  \mathbb{R}
  \xrightarrow{
    \;\;
    (n,r) \mapsto (r, r + n)
    \;\;
  }
  \mathbb{R}
  \times_{S^1}
  \mathbb{R}  
$$

$$
  \mathbb{Z} \times \mathbb{Z} \times \mathbb{R}
  \xrightarrow{ \;\; (n_1, n_2, r) \mapsto (r, r + n_1, r + n_1 + n_2)  \;\; }
  \mathbb{R}
    \times_{S^1}
  \mathbb{R}
    \times_{S^1}
  \mathbb{R}
$$

$$
  &#643; S^1 
  \xrightarrow{ \sim }
  B \mathbb{Z}
$$

\linebreak

$$
  W(B \mathbb{Z})_n
  \;=\;
  \mathbb{Z}^n
    \times
  \cdots
    \times
  \mathbb{Z}^2
    \times
  \mathbb{Z}
$$

\linebreak

$$
  \big(
  Hom
  \big(
    B \mathbb{Z} \times \Delta[1],
    \,
    X \sslash G
  \big)
  \times
  W(B \mathbb{Z})_1
  \big)
  /
  (B \mathbb{Z})_1
  \;\;\;
  \simeq
  \;\;\;
  \underset{ [g] }{\coprod}
  X^g \sslash C_g
$$


$$
  \big(
  Hom
  \big(
    B \mathbb{Z} \times \Delta[2],
    \,
    X \sslash G
  \big)
  \times
  W(B \mathbb{Z})_2
  \big)
  /
  (B \mathbb{Z})_2
  \;\;\;
  \simeq
  \;\;\;
$$

 
\linebreak

$$
  \langle g, 1 \rangle
  \xhookrightarrow{\;\;}
  { C_g \times \mathbb{R} }
  \xrightarrow{\;\;}
  \Lambda_g
$$

$$
  \mathbb{Z} \times C_g \times \mathbb{R}
  \xrightarrow
    {\;\;   
      (n, h, r) \mapsto \big( (h,r), ( g^n g, n + r  )  \big)
    \;\;}
  (C_g \times \mathbb{R})
  \times_{\Lambda_g}
  (C_g \times \mathbb{R})
$$

$$
  \big(
    X^g
    \times
    W( X^g \sslash \Lambda_g )
  \big)
  /
  (\Lanbda)
$$

$$
  \big(
    X^g
    \times
    W( X^g \sslash \Lambda_g )
  \big)
  /
  (X^g \sslash \Lambda_g)
$$


\linebreak

***

\linebreak

$$
  (S^1)\hat{_I}
$$

$$
  Ext
  \Big(
    \big(
      \mathcal{L}^{const} X 
    \big) \!\sslash\! S^1
  \Big)
  \longrightarrow
  A
$$

$$
  \big(
    \mathcal{L}^{const} X 
  \big) \!\sslash\! S^1
  \longrightarrow
  Cyc(A)
$$

\linebreak

\linebreak

Let $\mathcal{C}$ be a [[small category]]. We write

\[
  \label{YonedaEmbedding}
  \mathcal{C}^{op} 
  \xhookrightarrow{\;\;\; y \;\;\;}
  Funct(\mathcal{C}, Sets)
\]

for the [[Yoneda embedding]] of its [[opposite category]], which we will often regard through its [[opposite functor]]

\[
  \label{OppositeYonedaEmbedding}
  \mathcal{C}
  \xhookrightarrow{\;\;\; y^{op} \;\;\;}
  Funct(\mathcal{C}, Sets)^{op} 
  \,.
\]

This is still a [[full subcategory]]-inclusion, now of $\mathcal{C}$ itself.

\begin{definition}\label{CategoryOfProObjects}
**(category of pro-objects)** \linebreak

The the *category of pro-objects in $\mathcal{C}$*, according to [Grothendieck 1960, Section 2](#Grothendieck1960), is the [[full subcategory]] of $Funct(\mathcal{C}, Sets)^{op}$ (eq:OppositeYonedaEmbedding)

\[
  \label{ProCAsFullSubcategoryOfOppositeOfCategoryOfPresheaves}
  Pro(\mathcal{C})
  \xhookrightarrow{\;\;}
  Funct(\mathcal{C}, Sets)^{op}   
\]

on those functors which are [[cofiltered limits]] of [[representable functors]] under the opposite Yoneda embedding (eq:OppositeYonedaEmbedding), hence of the form

\[
  \label{FilteredLimitOfRepresentablesInOppositeOfPresheafCategory}
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)
  \;\;
  \coloneqq
  \;\;
  \underset{\longleftarrow}{\lim}
  \big(
    \mathcal{I}
    \xrightarrow{\;X_\bullet\;}
    \mathcal{C}
    \xrightarrow{\;y^{op}\;}
    Funct(\mathcal{C}, Sets)^{op}
  \big)
  \,,
\]

for $\mathcal{I}$ a [[cofiltered category]]. These objects of $Pro(\mathcal{C})$ are also called the *pro-objects of $\mathcal{C}$*.
\end{definition}

\begin{remark}
Notice that $Funct(\mathcal{C}, Sets)^{op}$ (eq:OppositeYonedaEmbedding) is the [[free completion]] of $\mathcal{C}$, so $Pro(\mathcal{C})$ is the *free completion of $\mathal{C}$ under [[cofiltered limits]].* See also at [[pro-representable functor]].
\end{remark}

\begin{remark}\label{BetweenFilteredLimitsAndFilteredColimits}
Under the identification of the [[objects]] of a category with its [[opposite category]], the  objects (eq:FilteredLimitOfRepresentablesInOppositeOfPresheafCategory) are [[filtered colimits]] of [[presheaves]]:

$$
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  y(X^{op}_i)
  \;\;
  \coloneqq
  \;\;
  \underset{\longrightarrow}{\lim}
  \big(
    \mathcal{I}^{op}
    \xrightarrow{\;X^{op}_\bullet\;}
    \mathcal{C}^{op}
    \xrightarrow{\;y\;}
    Funct(\mathcal{C}, Sets)
  \big)
  \,.
$$
\end{remark}

\begin{lemma}\label{ProObjectsAsFunctors}
  The pro-objects regarded as functors (eq:FilteredLimitOfRepresentablesInOppositeOfPresheafCategory)
  are objectwise on $c \in \mathcal{C}$ given by 
  $$
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
    y^{op}(X_i)  
    \;\;
    \colon
    \;\;
    c 
    \;\mapsto\;
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
    \mathcal{C}(X_i, c)
    \,.
  $$
  because [[limit]] over an [[opposite functor]] is the [[colimit]] of the functor itself.
\end{lemma}
\begin{proof}
This is the composite of the following sequence of [[natural isomorphisms]]
$$
  \begin{aligned}
  \Big(
  \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{\lim}  
  y^{op}(X_i)  
  \Big)
  (c) 
  &
  \;\simeq\;
  \Big(
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  y(X^{op}_i)  
  \Big)
  (c) 
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}  
  \Big(
    \big(y(X^{op}_i)\big)
    (c)
  \Big)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \;
  Func(\mathcal{C},Sets)
  \big(
    y(c), \, y(X_i)
  \big)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \mathcal{C}^{op}(c, X_i)
  \\
  &
  \;\simeq\;
  \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{\lim}   
  \mathcal{C}(X_i, c)
  \mathrlap{\,,}
  \end{aligned}
$$
where

* the first step is Remark \ref{BetweenFilteredLimitsAndFilteredColimits};

* the second step uses that [[colimits of presheaves are computed objectwise]];

* the third step is the [[Yoneda lemma]];

* the fourth step is the [[Yoneda embedding]] (eq:YonedaEmbedding);

* the fifth step is the definition of the [[opposite category]].

\end{proof}

\begin{lemma}

The [[hom-sets]] in $Pro(\mathcal{C})$ (Def. \ref{CategoryOfProObjects})
are in [[natural bijection]] with [[limits]] of [[colimits]] of [[hom-sets]] in $\mathcal{C}$ as follows:

$$
  Pro(\mathcal{C})
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
$$

\end{lemma}

\begin{proof}
This is the composite of the following sequence of [[natural bijections]]:
$$
  \begin{aligned}
  Pro(\mathcal{C})
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
  &
  \;\simeq\;
  Func(\mathcal{C},Sets)^{op}
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longleftarrow}}{lim}
    y^{op}(X_i),
    \,
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
    y^{op}(Y_j),    
  \Big)
  \\
  & 
  \;\simeq\;
  Func(\mathcal{C},Sets)
  \Big(
    \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{lim}
    y(Y^{op}_j),    
    \,
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    y(X^{op}_i),
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \;
  Func(\mathcal{C},Sets)
  \Big(
    y(Y^{op}_j),    
    \,
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    y(X^{op}_i),
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \Big(
    \big(
      \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
      y(X^{op}_i)
    \big)
    \big(
      y(Y^{op}_j)
    \big)    
  \Big)
  \\
  & \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{lim}
  \Big(
    \underset{\underset{i \in \mathcal{I}}{\longrightarrow}}{lim}
    \mathcal{C}
    \big(
      X_i,
      \,
      Y_j
    \big)
  \Big)
  \end{aligned}
$$

Here

* the first step is the [[fully faithful functor|fully faithfulness]] of the defining [[full subcategory]]-inclusion (eq:ProCAsFullSubcategoryOfOppositeOfCategoryOfPresheaves);

* the second step is the definition of the [[opposite category]], using Remark \ref{BetweenFilteredLimitsAndFilteredColimits};

* the third step is the [[hom-functor preserves limits]] in the first argument, which means that in the first argument, $\mathcal{K}^{op} \times \mathcal{K} \xrightarrow{Hom} Sets$ takes *[[colimits]] in $\mathcal{K}$* to *limits in $\mathcal{K}$*, here for $\mathcal{K} = Func(\mathcal{C},Sets)$;

* the fourth step is the [[Yoneda lemma]];

* the fifth step is Lemma \ref{ProObjectsAsFunctors}.

\end{proof}

\linebreak

\linebreak

$$
\begin{aligned}
    \tau_0
    \,
    \mathbf{H}
    \big(
      X, \, B \mathcal{G}
    \big)
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    \big[
      X, \, B \mathcal{G}
    \big]
    \\
    &
    \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    \big[
      X,
      \,
      &#643;
      \, 
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    &#643;
    \,
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    Pnts
    \,
    Disc
    \,
    \mathrm{Sing}
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    \mathrm{Sing}
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \Big(
    \big[
      X,
      \,
      \mathbf{B}\mathcal{G}
    \big]
    (\Delta^\bullet_{\mathrm{smth}})
    \Big)
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \Big(
    \mathbf{H}
    \big(
      X
      \times
      \Delta^\bullet_{\mathrm{smth}}
      \,
      \mathbf{B}\mathcal{G}
    \big)
    \Big)
    \\
    & \;\simeq\;
    \tau_0
    \,
    \underset{\longrightarrow}{\mathrm{lim}}
    \big(
      {\mathcal{G}}PrinBund_{X \times \Delta^\bullet_{\mathrm{smth}}}
    \big)
    \\
    & \;\simeq\;
    \underset{\longrightarrow}{\mathrm{lim}}
    \,
    \tau_0
    \big(
    {\mathcal{G}}PrinBund_{X \times \Delta^\bullet_{\mathrm{smth}}}
    \big)
    \\
    & \;\simeq\;
    \Big(
      \tau_0
      \big(
        {\mathcal{G}}PrinBund_{ X }
      \big)
    \Big)
    \big/
    \Big(
      \tau_0
      \big(
      {\mathcal{G}}PrinBund_{X \times \Delta^1_{\mathrm{smth}}}
      \big)
    \Big)
    \\
    & \;\simeq\;
    \big(
      {\mathcal{G}}PrinBund_X
    \big)_{\sim_{\mathrm{conc}}}
  \end{aligned}
$$


$\leftrightarrows$

$\ldots$

$$
  \begin{aligned}
  & 
  2Loc_{QuillenEquivs}
  \big(
    CombinatorialModelCategories
  )
  \\
  &
  \;
  \overset{\color{purple}?}{\simeq}
  \;
  2Ho
  \big(
    Presentable \infty Categories
  \big)
  \end{aligned}
$$

\linebreak

***

\linebreak

For $\mathbf{H}$ an $\infty$-topos
and $G \in Groups(\mathbf{H})$,
one would expect that 

(1)
group objects 
$\Gamma /\!\!/ G \,\in\, \mathrm{Groups}\big( \mathbf{H}_{/\mathbf{B}G} \big)$
in the slice over the delooping of $G$

are equivalent to 

(2) group objects $\Gamma \,\in\, \mathrm{Groups}(\mathbf{H})$
equipped with an action of $G$ by group automorphisms.

A construction $(2)\Rightarrow (1)$ is in Prop. 2.102 on [p. 35](https://ncatlab.org/schreiber/files/orbi210607.pdf#page=35) of *[[schreiber:Proper Orbifold Cohomology|Proper Orbifold Cohomology]]*.

The following are some thoughts on how to go about $(1) \Rightarrow (2)$, but not conclusive yet.

The following pasting diagram shows something slightly weaker:

  \begin{tikzcd}
    &
    G 
    \ar[r]
    \ar[
      d,
      "{(e,\mathrm{id})}"{left}
    ]
    \ar[
      dr,
      phantom,
      "\mbox{\tiny\rm(d)}"
    ]
    &
    \ast
    \ar[d]
    \\
    G
    \ar[r]
    \ar[d]
    \ar[
      dr,
      phantom,
      "\mbox{\tiny\rm(d)}"
    ]
    &
    \Gamma \times G
    \ar[
      r,
      "\mathrm{pr}_1"{description}
    ]
    \ar[
      d,
      "\rho"{description}
    ]
    \ar[
      dr,
      phantom,
      "{\mbox{\tiny (c)}}"
    ]
    & 
    \Gamma
    \ar[d]
    \ar[rr]
    \ar[
      drr,
      phantom,
      "{\mbox{\tiny (b)}}"
    ]
    &&
    \ast
    \ar[d]
    \\
    \ast
    \ar[r]
    &
    \Gamma
    \ar[d]
    \ar[r]
    \ar[
      dr,
      phantom,
      "{\mbox{\tiny (b)}}"
    ]
    &
    \Gamma /\!\!/ G
    \ar[rr]
    \ar[d]
    \ar[
      drr,
      phantom,
      "\mbox{\tiny\rm(a)}"
    ]
    &&
    \mathbf{B}G
    \mathrlap{
      \;
      \simeq
      \Gamma /\!\!/ (\Gamma \rtimes G)
    }
    \ar[d]
    \\
    &
    \ast
    \ar[r]
    &
    \mathbf{B}G
    \ar[rr]
    &&
    \underset{\mathbf{B}G}{\sum} \mathbf{B} (\Gamma /\!\!/ G)
    \mathrlap{
      \;
      \simeq
      \mathbf{B}(\Gamma \rtimes G)
    }
    \ar[d]
    \\ 
    &&&&
    \mathbf{B}G
    &
    {\phantom{AAAAAAAAAA}}
  \end{tikzcd}

Here:

(a) is the homotopy pullback that exhibits $\Gamma /\!\!/ G$
as a group object in the slice over $\mathbf{B}G$;

(b) is the homotopy pullback that exhibits $\Gamma /\!\!/ G$
as the homotopy quotient of a $G$-action on $\Gamma$;

(c) is the homotopy fiber product which exhibits
the shear map equivalence of 
$\Gamma$ as a principal $G$-bundle over $\Gamma /\!\!/ G$;

(d) is a homotopy pullback implied from this by the pasting law.

While we can't seem to conclude group structure on $\Gamma$ directly, 
we see that $\Gamma \times G$ carries a group structure,
to be denoted $\Gamma \rtimes G$, whose delooping is 
the bottom right object.


Moreover, 
$G \xrightarrow{(e,\mathrm{id})} \Gamma \times G$ is
exhibited as a homomorphism of group objects.


Also, we see that 
$G \xrightarrow{(e,\mathrm{id})} \Gamma \times G \xrightarrow{\rho} \Gamma$
are $G$-equivariant maps for $G$ acting by right multiplication on itself.
This implies that $\rho$ is the given $G$-action, 

So we are beginning to see that $\Gamma \!\sslash\! G \in Groups\big( \Gamma \rtimes G\big)$ is equivalent to a  "semidirect product $\infty$-group"
$\Gamma \rtimes G$. 

But can we make explicit that the action of $G$ on $\Gamma$ is by group automorphisms? This would require constructing a homotopy fiber sequence of the form

$$
  \array{
    \mathbf{B}\Gamma
    &\longrightarrow&
    \mathbf{B}(\Gamma \rtimes G)
    \\
    && \big\downarrow
    \\
    && \mathbf{B}G
  }
$$

How to see this homotopy fiber from the above diagram (or from some other consideration)?


\linebreak
\linebreak







