

\begin{prop}
  Let 
  $$
   \array{
    A &\overset{\; i \;}{\longrightarrow}& B
    \\
    {}^{\mathllap{f}}
    \big\downarrow
    &{}^{{}_{(po)}}&
    \big\downarrow {}^{\mathrlap{g}}
    \\
    C &\underset{\; j \;}{\longrightarrow}& D
   }
  $$
  be a [[pushout]] [[commuting diagram|square]] of [[chain maps]] between (unbounded) [[chain complexes]], such that 

* $i$ is a degreewise [[injection]];

* $f$ is a [[quasi-isomorphism]].

Then also $g$ is a [[quasi-isomorphism]].
\end{prop}
\begin{proof}
  The [[pushout]] of chain complexes is degreewise a pushout in the underlying [[abelian category]].
  Since pushout in abelian categories preserves monomorphisms ([this Prop.](abelian+category#PullbackPreservesEpimorphisms)) it follows that also $j_n$ is a monomorphism. Finally, the [[pasting law]] implies that the induced morphism of [[cokernels]] of $i$ and $j$ is an [[isomorphism]]. In summary, this means that we have a [[commuting diagram]] of chain complexes as follows:
  $$
   \array{
    A
    &\overset{\;\;\; i \;\;\;}{\hookrightarrow}& 
    B 
    &\longrightarrow&
    cok(i)
    \\
    {}^{\mathllap{f}}
    \big\downarrow
    &{}^{{}_{(po)}}&
    \big\downarrow {}^{\mathrlap{g}}
    &&
    \big\downarrow {}^{\mathrlap{\simeq}}
    \\
    C
    &\underset{\;\;\; j \;\;\;}{\hookrightarrow}& 
    D
    &\longrightarrow&
    cok(j)
    \,.
   }
  $$

This implies a morphism of the corresponding [[long exact sequences in chain homology]] of the form:

$$
  \array{
    \cdots
    &\to&
    H_{n+1}
    \big(
      cok(i)
    \big)
    &
    \xrightarrow{\; \delta \;}
    &
    H_n(A)
    &
    \xrightarrow{\; i_\ast\;}
    &
    H_n(B)
    &
    \xrightarrow{\;\;\;}
    &
    H_n\big(cok(i)\big)
    &
    \xrightarrow{\;\delta\;}
    &
    H_{n-1}(A)
    &
    \to
    &
    \cdots  
    \\
    &&
    {}^{\mathllap{}}
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{f_\ast}}
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{g_\ast}}
    \big\downarrow
    &&
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{f_\ast}}
    \big\downarrow
    {}^{\mathrlap{\simeq}}
    \\
    \cdots
    &\to&
    H_{n+1}
    \big(
      cok(j)
    \big)
    &
    \xrightarrow{\; \delta \;}
    &
    H_n(C)
    &
    \xrightarrow{\; j_\ast\;}
    &
    H_n(D)
    &
    \xrightarrow{\;\;\;}
    &
    H_n\big(cok(j)\big)
    &
    \xrightarrow{\;\delta\;}
    &
    H_{n-1}(C)
    &
    \to
    &
    \cdots  
  }
$$
From this the [[five lemma]] implies that $g_\ast$ is an isomorphism on [[chain homology]], hence that $g$ is a quasi-isomorphism.
\end{proof}


$$
  H_{\bullet+1}(B) 
  \longrightarrow
  H_\bullet
  \big(
    A \times_B C 
  \big)
  \xrightarrow{ (pr_1, p^\ast(f)) }
  H_\bullet
  (
    A
  )
  \oplus
  H_\bullet(C)
  \xrightarrow{ f - p }
  H_\bullet(B) 
  \longrightarrow
  H_{\bullet-1}
  \big(
    A \times_B C 
  \big)
$$

\begin{prop}
  The [[pullback]] $p^\ast f$ of a [[quasi-isomorphism]] $f$ of [[chain complexes]] along a degreewise [[surjection]] $p$ of chain complexes is itself a quasi-isomorphism:

$$
  \array{   
    A \times_B C 
    &
    \overset{
     p^\ast f \, \in \mathrm{QIso}
    }{\longrightarrow}&
    C
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow {}^{\mathrlap{p \in Surj}}
    \\
    A
    &
    \underset{
      f \in \mathrm{QIso}
    }{\longrightarrow}
    &
    B
  }
$$

\end{prop}

In all of the following, consider a [[pullback]] [[commuting square|square]] of [[chain maps]] between [[chain complexes]]:

$$
  \array{   
    A \times_B C 
    &
    \overset{
     p^\ast f \, \in \mathrm{QIso}
    }{\longrightarrow}&
    C
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow {}^{\mathrlap{p \in Surj}}
    \\
    A
    &
    \underset{
      f \in \mathrm{QIso}
    }{\longrightarrow}
    &
    B
  }
$$


\begin{lemma}
  Let 

  * $n \in \mathbb{Z}$;
  
  * $f \;\colon\; A \to B$ a [[chain map]] which induces an [[isomorphism]] on [[chain homology]] in degree $n$:

    $$
      H_n(f) \;\colon\; H_n(A) \xrightarrow{\;\simeq\;} H_n(B)
    $$ 

  * $p \;\colon\; C \to B$ be a [[chain map]] which is a [[surjection]] in degrees $n+1$ and $n + 2$

    $$
      \array{
        p_{n+1} 
        &\colon\;& 
        C_{n+1} 
        \overset{\;\;\;\;}{\twoheadrightarrow} 
        B_{n+1}
        \\
        p_{n+2} 
        &\colon\;& 
        C_{n+2} 
        \overset{\;\;\;\;}{\twoheadrightarrow} 
        B_{n+2}
      }
    $$

Then the [[pullback]] $p^\ast(f)$ is also an [[isomorphism]] on [[chain homology]] in degree $n$:

$$
  H_n
  \big(
   p^\ast(f)
  \big) 
    \;\colon\; 
  H_n(A) \xrightarrow{\;\simeq\;} H_n(B)
  \,.
$$   
\end{lemma}

\begin{proof}

First to see that 
$  H_n
  \big(
   p^\ast(f)
  \big) 
$
is an [[injection]]: Consider a [[cycle]] $(a_n, c_n) \in A_n \times_{B_n} C_n$ whose image under $p^\ast(f)$ becomes exact:

* $d(a_n,c_n) = 0$,

* $c_n = \partial c_{n+1}$.

We need to show that then also $(a_n, c_n)$ is exact.

By surjectivity if follows that there exists $(a_{n+1}, c_{n+1})$.
By commutativity we have

$f(\partial a_{n+1}) = p(c_n) = f(a_n)$


First, it follows that also $f(a_n)$ is exact, because:

$$
  \begin{array}{lll}
    f(a_n)
    & = 
    p(c_n)
    \\
    & =
    p(\partial c_{n+1})
    \\
    & = 
    \partial p( c_{n+1} )
    \,.
  \end{array}
$$

By assumption on $f$ this means that already $a_n$ is exact

$$
  a_n  = \partial a_{n+1} 
$$

and by assumption on $p$ there is $c'_{n+1}$ with 

$$
  f(a_{n+1}) = p(c'_{n+1})
  \,.
$$

Since 

$$
  \partial p(c_{n+1} - c'_{n+1}) = 0
$$

there is

$$
  f(a_{n+2}) = p(c_{n+1} - c'_{n+1}) + \partial b_{n+2}
$$

now

$$
  f(a_{n+1} + \partial a_{n+2})
  \;=\;
  f(a_{n+1}) + \partial b_{n+2}
  \;=\;
  p(c'_{n+1}) + p(c_{n+1} - c'_{n+1})
  \;=\;
  p(c_{n+1})
$$

So 

$$
  \big(
    a_{n+1} + \partial a_{n+2}
    ,\,
    c_{n+1}
  \big)
  \;\in\;
  A_{n+1} \underset{B_{n+1}}{\times} C_{n+1}
$$

and

$$
  \partial
  \big(
    a_{n+1} + \partial a_{n+2}
    ,\,
    c_{n+1}
  \big)
  \;=\;
  (a_n, c_n)
  \,.
$$


Since, in summary, this implies that 




by assumption 

$ f(a_n) = p(c_n) = p(d c_{n-1}) = d p(c_{n-1})$


Hence $d(a_{n-1},c_{n-1}) = (a_n,c_n)$.



For surjectivity

For $d c_n = 0$

$d p(c_n) = 0$

$ p(c_n) = f(a_n) + d b_{n-1} $

$b_{n-1} = p(c_{n-1})$

$p( c_n ) = f(a_n) + p( d c_{-1}) $

$$
  d( a_n, c_n - d c_{n-1} ) = 0
$$

\end{proof}

\begin{prop}\label{InducedQuilleAdjunctionsOnModelCategoriesOfPointedObjects}
**(induced [[Quillen adjunction]] on [[model categories of pointed objects]])** \linebreak
Given a [[Quillen adjunction]] between [[model categories]]
$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}
  \,,
$$
there is induced a [[Quillen adjunction]] between the corresponding [[model categories of pointed objects]]
$$
  \mathcal{D}^{\ast\!/}
    \underoverset
      {\underset{R^{\ast\!/}}{\longrightarrow}}
      {\overset{L^{\ast\!/}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{\ast\!/}
  \,,
$$
where 

* the [[right adjoint]] acts directly as $R$ on the triangular [[commuting diagrams]] in $\mathcal{C}$ that define the morphisms in $\mathcal{C}^{\ast\!/}$;

* the [[left adjoint]] is the [[composition|composite]] of the corresponding direct application of $L$ followed by [[pushout]] along the [[adjunction counit]] $L(\ast) \simeq L \circ R(\ast) \xrightarrow{ \;\epsilon_\ast \; } \ast$ (using that $R(\ast) \simeq \ast$ since [[right adjoints preserve limits]] and hence [[terminal objects]]):

  $$
    L^{\ast\!/}
    \;\colon\;
    \mathcal{C}^{\ast\!/}
    \xrightarrow{ \;\; L  \;\; }
    \mathcal{D}^{L(\ast)\!/}
    \;\simeq\;
    \mathcal{D}^{L\circ R(\ast)\!/}
    \xrightarrow{ \;\; (-) \sqcup \epsilon_\ast \;\; }
    \mathcal{D}^{\ast\!/}
    \,.
  $$

\end{prop}
\begin{proof}
  It is fairly straightforward to check this directly (e.g. [Hovey 1999, Prop. 1.3.5](#model+structure+on+pointed+objects#Hovey99)), but it is also an example Prop. \ref{slice+model+structure#SlicedQuillenAdjunction}. To make this explicit, notice that passing to [[opposite categories]] with their [[opposite model structures]] turns the original Quillen adjunction into the [[opposite Quillen adjunction]]:

$$
  \mathcal{D}^{op}
    \underoverset
      {\underset{L^{op}}{\longrightarrow}}
      {\overset{R^{op}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{op}
  \,.
$$

Now the passage to [[pointed objects]] corresponds to [[slice category|slicing]] (instead of [[coslice category|co-slicing]]), since

\[
  \label{PointedObjectsIsOppositeOfCopointedObjectsInOpposite}
  \mathcal{C}^{\ast\!/}
  \;\;
  \simeq
  \big(
    \mathcal{C}^{op}_{/\ast}
  \big)^{op}
  \,,
  \;\;\;\;\;\;\;
  \text{similarly}
  \;\;\;
  \mathcal{D}^{\ast\!/}
  \;\;
  \simeq
  \big(
    \mathcal{D}^{op}_{/R(\ast)}
  \big)^{op}
  \,,
\]

whence item (1) in Prop. \ref{SlicedQuillenAdjunction} says that there is a Quillen adjunction of the form

$$
  \mathcal{D}^{op}_{/R(\ast)}
    \underoverset
      {\underset{L^{op}_{/\ast}}{\longrightarrow}}
      {\overset{R^{op}_{/\ast}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{op}_{/\ast}
  \,,
$$

hence with [[opposite Quillen adjunction]] of the required form

$$
  \mathcal{D}^{\ast\!/}  
  \simeq
  \big(\mathcal{D}^{op}_{/R(\ast)}\big)^{p[}
    \underoverset
      {\underset{ 
        L^{\ast\!/} \,\coloneqq\, \big( L^{op}_{/\ast} \big)^{op}
      }{\longrightarrow}}
      {\overset{
        R^{\ast\!/} \,\coloneqq\, \big( R^{op}_{/\ast} \big)^{op}
      }{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \big(\mathcal{C}^{op}_{/\ast}\big)^{op}
  \simeq
  \mathcal{C}^{\ast\!/}
  \,,
$$


with $R^{op}$ acting directly as $R$ on underlying diagrams, and with $L^{op}$ acting as the composite of $L$ following by [[pullback]] -- in $\mathcal{C}^{op}$ -- along the [[adjunction unit]] of $(R^{op} \dashv L^{op})$. Since the component morphism of the [[adjunction unit|unit]] of the [[opposite adjunction]] $(R^{op} \dashv L^{op})$ is that of the adjunction unit of $(L \dashv R)$, and since [[pullback]] in an [[opposite category]] is [[pushout]] in the original category, this implies the claim. 
\end{proof}



\linebreak

$$
  \mathcal{D}^{op}
    \underoverset
      {\underset{L^{op}}{\longrightarrow}}
      {\overset{R^{op}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{op}
$$

\linebreak

$$
  \mathcal{D}^{op}_{/R(\ast)}
    \underoverset
      {\underset{L^{op}_{/\ast}}{\longrightarrow}}
      {\overset{R^{op}_{/\ast}}{\longleftarrow}}
      {\;\;\;\;\;\bot_{\mathrlap{{}_{Qu}}}\;\;\;\;\;}
  \mathcal{C}^{op}_{/\ast}
$$

\linebreak


$$
  L^{op}_{/\ast}
  \;\colon\;
  \mathcal{D}^{op}_{/\ast}
  \xrightarrow{ \; L^{op} \; }
  \mathcal{C}^{op}_{/L^{op} \circ R^{op}(\ast)}
  \xrightarrow{ \; ( \eta^{op}_{\ast} )^\ast  \;  }
  \mathcal{C}^{op}
$$

$$
  \mathcal{D}^{\ast/}
    \underoverset
      {\underset{R^{\ast/}}{\longrightarrow}}
      {\overset{L^{\ast/}}{\longleftarrow}}
      {\;\;\;\;\;\bot\;\;\;\;\;}
  \mathcal{C}^{\ast/}
$$



\linebreak


$$
  r_1 \,\otimes\, r_2
  \;=\;
  \big( r_1 \,\otimes\, 1 \big) \cdot \big( 1 \otimes r_2 \big)
  \;=\;
  1 \,\otimes\, r_1 \cdot 1 \otimes r_2
  \;=\;
  1 \,\otimes\, r_1 \cdot r_2
$$

\begin{prop}
  If $f$ is an [[isomorphism]] with [[inverse morphism]] $f^{-1}$, then any [[left inverse]] or [[right inverse]] is already an actual [[inverse morphism]] and in fact is [[equality|equal]] to $f^{-1}$.
\end{prop}
In particular, [[inverse morphisms]] are unique when they exist.
\begin{proof}
  Let $g$ be a [left inverse]], hence such that $g \circ f \,=\, id$. 
  Write $f^{-1}$ for the actual inverse, hence such that
  $f^{-1} \circ f \,=\, id$ and $f \circ f^{-1} \,=\, id$.  
  Then the following sequence of equalities implies that
  $g = f^{-1}$:
$$
  \begin{aligned}
    g 
    & \;=\;
    g \circ id
    \\
    & \;=\;
    g \circ ( f \circ f^{-1} )
    \\
    & \;=\;
    (g \circ f) \circ f^{-1}
    \\
    & \;=\;
    id \circ f^{-1}
    \\
    & \;=\;
    f^{-1}
    \,.
  \end{aligned}
$$
Here essentially all steps use just the definitions of the various morphisms, except the third, which uses [[associativity]] of [[composition]] in any [[category]].

An analogous argument applies to right inverses; and, of course, either argument applies to actual inverses.
\end{proof}

\begin{remark}
  The sliced adjunction (Prop. \ref{SliceAdjoints}) in the second form (eq:SlicedAdjointFunctorsOverRb) is such that the sliced [[left adjoint]] form [[adjuncts]] of slicing morphisms, in that (again by [this Prop.](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)):

$$
  L_{/d}
  \left(
    \array{
      c
      \\
      \big\downarrow {}^{\mathrlap{\tau}}
      \\
      R(b)
    }
  \right)
  \;\;
  =
  \;\;
  \array{
    L(c)
    \\
    \big\downarrow {}^{\mathrlap{\widetilde{\tau}}}
    \\
    b
  }
$$
\end{remark}


**(1a)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
  c
  \ar[rr, dashed, "f"]
  \ar[dr]
  &&
  R(d)
  \ar[dl]
  \\
  & 
  R(b)
\end{tikzcd}

**(2)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
  L(c)
  \ar[rr, dashed, "L(f)"]
  \ar[dr]
  \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=+8pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 \widetilde{f}
               $}
             } ([yshift=+8pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
  ]
  &&
  L \circ R(d)
  \ar[rr, "\epsilon_d"{above}]
  \ar[dl]
  &&
  d
  \ar[dl]
  \\
  &
  L \circ R(b)
  \ar[rr, "\epsilon_b"{below}]
  &&
  b
\end{tikzcd}

**(1b)**

\begin{tikzcd}[column sep={between origins, 33}, row sep=4]
  c
  \ar[rr, "\eta_c"{above}]
  \ar[dr]
  \ar[
      rrrrrr,
      rounded corners,
      to path={
           -- ([yshift=+12pt]\tikztostart.north)
           --node[above]{
               \scalebox{.7}{$
                 f
               $}
             } ([yshift=+8pt]\tikztotarget.north)
           -- (\tikztotarget.north)}
  ]
  &&
  R \circ L(c)
  \ar[rrrr,"R(\widetilde{f})"]
  \ar[dr]
  &&
  %R \circ L \circ R(d)
  %\ar[rr, "R(\epsilon_d)"{above}]
  %\ar[dl]
  &&
  R(d)
  \ar[dl]
  \\
  &
  R(b)
  \ar[rr, "\eta_{R(b)}"{below}]
    \ar[
      rrrr,
      rounded corners,
      to path={
           -- ([yshift=-8pt]\tikztostart.south)
           --node[below]{
               \scalebox{.7}{$
                 \mathrm{id}
               $}
             } ([yshift=-8pt]\tikztotarget.south)
           -- (\tikztotarget.south)}
    ]
  &&
  R \circ L \circ R(b)
  \ar[rr, "R(\epsilon_b)"{below}]
  &&
  R(b)
\end{tikzcd}

\linebreak





* [[flat connections]] [[Maurer-Cartan forms]]

  $d\, A^i \,=\,  f^i{}_{j k} A^j \wedge A^k$

* flat string 2-connections

  $ d, B_3 \;=\; k_{i j} F^i \wedge F^j $

* cohomotopy classifies

  - cobordism classes of normally framed submanifolds

  - deg 2: moduli of YM monopones
  
* maps into twistor space...

* twisted cohomology is really non-abelian cohomology equipped with a non-abelian cohomology operation called the twist


# Para construction

In [[deep learning]] and [[game theory]], we usually think of neural networks/economic agents as processes taking in an input $A$ and producing an output $B$. However, we additionally want to model that these processes have extra, "hidden" inputs. In neural networks we call these _weights_ (or _parameters_) and in game theory we call these _strategies_.

In other words, we want to form a category where a morphism $A \to B$ contains the data of i) a _parameter space_ $P$ and b) a morphism $f : P \otimes A \to B$. From this description we see that this construction necesissitates a choice of some underlying monoidal category $\mathcal{C}$.

Such a morphism might be visualised using the string diagram language of monoidal categories (left), however, this notation does not emphasize the special role played by $P$, which is part of the data of the morphism itself. Parameters and data in machine learning have different semantics; by separating them on two different axes, we obtain a graphical language which is more closely tied to these semantics (right).

<img src="/nlab/files/standard_vs_para.png" width="500"/>

This lends itself to a intuitive graphical language, where composition with a $Q$-parameterised morphism $B \to C$ can be visualised as follows:

<img src="/nlab/files/para_comp2.gif" width="500"/>

This construction is called $\mathbf{Para}(\mathcal{C})$, originally introduced in (backprop as functor) in a simplified form; then succesively refined in (compDL), (catfoundofgraddesc), (towardscatcybernetics)

[[para construction]]
