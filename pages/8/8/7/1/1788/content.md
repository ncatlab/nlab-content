
$\multimap$

Every [[pair]] of [[adjoint functors]] $(F \dashv U) \;\colon\; \mathbf{C}' \leftrightarrow \mathbf{C}$ (with [[unit of an adjunction|unit]] $\eta^{U F}$ and [[counit of an adjunction|counit]] $\epsilon^{F U}$) between [[categories]] $\mathbf{C}$, $\mathbf{C}'$ fits into a [[commuting diagram]] in [[Cat]] of the following form:

\begin{imagefromfile}
    "file_name": "AdjunctionsAndMonadicity-221106.jpg",
    "width": "540",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}





Here:

* $\mathcal{E} \;\coloneqq\; U F \;\coloneqq\; U \circ F$ denotes the induced [[endofunctor]] on $\mathbf{C}$

  which carries the [[structure]] of a [[monad]] with 

  * [[unit of a monad|unit]] given by 

    $$
      \eta^{\mathcal{E}}
      \;\;
      \colon
      \;\;
      id_{\mathbf{C}}
      \xrightarrow{\;\;
        \eta^{U F}
      \;\;}
      U F
      \;=\;
      \mathcal{E}
    $$ 

  * product given by

    $$
      \mu^{\mathcal{E}}
      \;\;
      \colon
      \;\;
      \mathcal{E} \mathcal{E}
      \;=\;
      U F U F
      \xrightarrow{\;\; 
        U ( \epsilon^{F U} ) F  
      \;\;}
      U F
      \;=\;
      \mathcal{E}
    $$

* $\mathcal{E}\text{-}\mathbf{C}$ denotes the ("[[Eilenberg-Moore category|Eilenberg-Moore]]"-)[[category]] of $\mathcal{E}$-[[algebras over a monad|algebras]] in $\mathbf{C}$ 

  $$
    A 
    \;=\;
    \Big(
      \mathcal{E}
      U^{\mathcal{E}}(A)
      \xrightarrow{\;\; \rho_A  \;\;}
      U^{\mathcal{E}}(A)
    \Big) 
  $$

   in $\mathbf{C}$ with [[homomorphisms]] between them,

* $K^{U F}$ denotes the "[[comparison functor]]" given by

  $$
    \array{
      \mathbf{C}'
      &
      \xrightarrow{\;\;\;\;\;\;\;\;\;\;
         K^{U F}
      \;\;\;\;\;\;\;\;\;\;}
      &
      \!\!\!\!\!\!\!\!\!\!\!\!\!\!
      \mathcal{E}\text{-}\mathbf{C}
      \\
      C' 
      &\mapsto&
      {
        \Big(
          \mathcal{E}
          U(C')
          \,=\,
          U F U (C')
          \xrightarrow{\; 
            U \epsilon^{F U}_{C'}  
          \;}
          U (C')
        \Big)
      }
    }
  $$

* $\big(\mathcal{E}\text{-}\mathbf{C}\big)^{fr}$ denotes the ("[[Kleisli category|Kleisli]]"-)[[category]] of *[free](algebra+over+a+monad#FreeAlgebras)* $\mathcal{E}$-[[algebras over a monad|algebras]]

  $$
    \begin{array}{rl}
    F^{\mathcal{E}}(C)
    &
    \;=\;
    \Big(
      \mathcal{E}
      \mathcal{E}
      (C)
      \xrightarrow{\;\; 
        \mu^{\mathcal{E}}_C  
      \;\;}
      \mathcal{E}(C)
    \Big) 
    \\
    \;=\;
    K^{U F} F(C)
    &
    \;=\;
    \Big(
      \mathcal{E}
      U
      F 
      (C)
      \xrightarrow{\;\; 
        U \epsilon^{ F U }_{F(C)}
      \;\;}
      U
      F 
      (C)
    \Big) 
    \,.
    \end{array}
  $$

* Here the last line makes explicit that

  $$
    U^{\mathcal{E}} F^{\mathcal{E}}
    \;=\;
    U F
    \;=\;
    \mathcal{E}
    \,.
  $$ 

  In fact, $F^{\mathcal{E}} \dashv U^{\mathcal{E}}$ and this realizes the [[monadic adjunction]] whose induced monad is $\mathcal{E}$.

  Hence the original $F \dashv U$ is [[monadic adjunction|monadic]] iff the [[comparison functor]] $K^{U F}$ is an [[equivalence of categories]].


