$F:\: \mathcal{C} \to \mathcal{D}$



\begin{definition}[Set of trivializations of the d-invariant]
  \label{SetOfTrivializationsOfTheDInvariant}
  For $E$ a [[multiplicative cohomology theory]] 
  and $n, d \in \mathbb{N}$,
  write
  \begin{equation}
    \label{SetOfTrivializationsOfdInvariant}
    \begin{aligned}
    H_{n-1}\!Fluxes^E\!\big( S^{n+d-1} \big)
    &
    \;\coloneqq\;
    \underset{
      [c] \in \mathbb{S}_{d-1}
    }{\sqcup}
    \pi_0
    \mathrm{Paths}_0^{c^\ast (1^E)}
    \Big(
    \mathrm{Maps}^{\ast/}\!
      \big(
        S^{n+d-1}
        \,,\,
        E^{n}
      \big)
    \Big)
    \end{aligned}
  \end{equation}
  for the [[set]] of [[tuples]] consisting of the 
  [[stable Cohomotopy]] class 
  $\big[ G^{\mathbb{S}}_{n}\!(c) \big]$ 
  of a [[map]] $S^{n+d-1} \xrightarrow{\;c\;}S^{n}$
  and the [[2-homotopy]] class 
  $\big[ H^E_{n-1}\!(c) \big]$
  of a trivialization (if any) of its
  [[d-invariant]] $c^\ast(1^E)$ in $E$-cohomology.    

So an element of $H_{n-1}\!Fluxes^E\!\big( S^{n+d-1} \big)$ (eq:SetOfTrivializationsOfdInvariant) is the [[2-homotopy]] class relative the boundary of a [[homotopy coherent diagram]]of the following form:

\begin{xymatrix@C=75pt@R=36pt}
      S^{n+d-1}
      \ar[rr]_>>{\ }="s"
      \ar[d]
        |-{
          \mathclap{\phantom{\vert^{\vert}}}
          c
          \mathclap{\phantom{\vert_{\vert}}}
        }
      \ar[dr]|-{
        G^{\mathbb{S}}_{n}\!(c)
      }
      ^>>>>>{\ }="t"
      &&
      \ast
      \ar[d]
        |-{
          \mathclap{\phantom{\vert^{\vert}}}
          0
          \mathclap{\phantom{\vert_{\vert}}}
        }
      \\
      S^{n}
      \ar@/_1.3pc/[rr]|-{ \;\Sigma^{n}(1^E)\; }
      \ar[r]|-{
        \;
        \Sigma^{n}
        (1^{\mathbb{S}})
        \;
      }
      &
      \mathbb{S}^{n}
      \ar[r]|-{
        \;
        (e^E)^{n}
        \;
      }
      &
      E^{n}
      %
      \ar@{==>}
        |-{
          \;
          \color{orange}
          H^E_{n-1}\!(c)
          \;
        }
        "s"; "t"
\end{xymatrix}

\end{definition}

\begin{definition}[Unit cofiber cohomology theory]
  \label{UnitCofiberCohomologyTheory}

For $E$ a [[multiplicative cohomology theory]] with unit map $\mathbb{S} \overset{ e^E }{\longrightarrow} E$ we denote the corresponding [[homotopy cofiber]]-theory as follows:

\begin{xymatrix@C=50pt@R=12pt}

    \mathbb{S}
    \ar[dd]
      ^>>{\ }="t"
    \ar[rr]
      ^-{
        \;1^E\;
      }
      _>>{\ }="s"
    &&
    \overset{
      \mathclap{
      \raisebox{4pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          $E$-cohomology
        \end{tabular}
      }
      }
    }{
      E
    }
    \ar[dd]
      _-{
        \mathclap{\phantom{\vert^{\vert^{\vert}}}}
        i^E
        \mathclap{\phantom{\vert_{\vert}}}
      }
      ^>>{\ }="t2"
    \ar[rr]
      ^-{
      }
      _>>{\ }="s2"
    &&
    \ast
    \ar[dd]
    \\
    {\phantom{A}}
    \\
    \ast
    \ar[rr]
    &&
    \underset{
      \mathclap{
      \raisebox{-4pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          $E$-cofiber
          \\
          cohomology
          \\
          theory
        \end{tabular}
      }
      }
    }{
      E/\mathbb{S}
    }
    \ar[rr]
      |-{ \;\partial^E\; }
      _-{
        \mbox{
          \tiny
          \color{green}
          \bf
          \begin{tabular}{c}
            \phantom{-}
            \\
            boundary
            \\
            operation
          \end{tabular}
        }
      }
    &&
    \underset{
      \mathclap{
      \raisebox{-6pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          shifted stable
          \\
          Cohomotopy
        \end{tabular}
      }
      }
    }{
      \Sigma \mathbb{S}
    }
    \,,
    &
    {\phantom{AAA}}
    %
    \ar@{=>}^-{ \mbox{\tiny\rm(po)} }
      "s"; "t"
    \ar@{=>}^-{ \mbox{\tiny\rm(po)} }
      "s2"; "t2"


\end{xymatrix}


\end{definition}



\begin{proposition}[Trivializations of d-invariant are classes in cofiber theory]
  \label{EFluxesAreCocycleInCofiberTheory}
  There is a [[bijection]] between the set
  (eq:SetOfTrivializationsOfdInvariant)
  of trivializations of the d-invariant
  and the [[cohomology group]] of the unit cofiber theory
  $E\!/\mathbb{S}$ (Def. \ref{UnitCofiberCohomologyTheory}):
  
\begin{xymatrix@=18pt}    
     \Big(
       \big[
         G^{\mathbb{S}}_n\!(c)
       \big]
       \,,\,
       \big[
         H^E_{n-1}\!(c)
       \big]
      \Big)
    \ar@{|->}[dd]
    &
     \overset{ \mathllap{
        \mbox{
          \tiny
          \bf
          \begin{tabular}{c}
          \end{tabular}
        }
      }}{
      H_{n-1}\mbox{\rm{Fluxes}}^E\!
      \big(
        S^{n + d - 1}
      \big)
      }
      \ar[rr]^-{ \simeq }
      \ar[dd]
      &&
      \big(
        E \!/\mathbb{S}
      \big)_{d}
      \ar[dd]^{\partial}
      \\
      \\
        \big[
          G^{\mathbb{S}}_n\!(c)
        \big]
      &
      \widetilde {\mathbb{S}}{}^{n}
      \big(
        S^{n+d-1}
      \big)
      \ar@{=}[rr]
      &&
      \mathbb{S}_{d-1}
\end{xymatrix}
  compatible with the fibrations
  of both over the underlying stable Cohomotopy classes
  $
    \widetilde {\mathbb{S}}{}^d
    \big( S^{n + d - 1}\big)
    \,\simeq\, 
    \mathbb{S}_{d-1}
  $.
\end{proposition}

We give two proofs: A quick abstract one and a more explicit one. The latter is closer to the old argument of [Conner-Floyd 66, Thm. 16.2](MUFr#ConnerFloyd66) (there for $E/\mathbb{S} = $ [[MUFr]], see there for more)

\begin{proof}[quick abstract]

By Definition \ref{SetOfTrivializationsOfTheDInvariant}, an element in $H_{n-1}Fluxes^E\big( S^{n+d-1} \big)$ is equivalently the class of a homotopy [[cone]] with tip $\Sigma^{n+d-1} \mathbb{S}$ over the [[cospan]] formed by the ring spectrum unit $e^E$ and the [[zero morphism]]. By the [[universal property]] of [[homotopy fibers]] this is equivalently the class of a map from $\Sigma^{n+d-1}\mathbb{S}$ to 
$fib\big( \Sigma^{n} e^E \big) \,\simeq\, \Sigma^{n-1} E/\mathbb{S}$. This implies the claim, by 

$$
  \pi_0
  Maps
  \Big(
    \Sigma^{n+d - 1}\mathbb{S}
    \,,\,
    \Sigma^{n-1} (E/\mathbb{S})
  \Big)
  \;\simeq\;
  (E/\mathbb{S})_{d}
  \,.
$$


\end{proof}

\begin{proof}[more explicit, Conner-Floyd-style]

Let
$\big[ S^{n + d - 1} \overset{c}{\longrightarrow} S^{n} \big] \;\in\; \pi^n\big(S^{n+d-1}\big)$ be a given class in Cohomotopy.
We need to produce a map of the form

\begin{xymatrix@R=10pt}
    {
      \color{orange}
      H^E_{n-1}\!(c)
    }
    \ar@{}[rr]|-{\longmapsto}
    &&
    M^d
    \\
    H_{n-1}\mbox{Fluxes}(X)_c
    \ar[rr]
    \ar[dd]
    &&
    \big(
      E\!/\mathbb{S}
    \big)_d
    \ar[dd]^-{ \partial }
    \\
    {\phantom{A}}
    \\
    \big\{
      [
        \Sigma^\infty c
      ]
    \big\}
    \;
    \ar@{^{(}->}[rr]
    &&
    \;
    \mathbb{S}_{d-1}
\end{xymatrix}

and show that it is a bijection onto this fiber, hence that the square is [[cartesian square|cartesian]]. To this end, we discuss the following [[homotopy coherent diagram|homotopy]] [[pasting diagram]], all of whose cells are homotopy cartesian:

\begin{xymatrix@R=15pt@C=60pt}
    \Sigma^\infty S^{n + d - 1}
    \ar[dd]_-{
      \Sigma^\infty
      {\color{green}
        c
      }
    }
    \ar[rr]
    &&
    \ast
    \ar[dd]
    \\
    \\
    \Sigma^\infty S^{n}
    \ar[dd]
    \ar[rr]|-{ 
      %\;\Sigma^\infty q_c\; 
    }
    \ar@/_1.4pc/[rrr]
      |<<<<<<<<<<<<<<<<<<<{
        \; \Sigma^{n}(e^{E}) \;
      }
    &&
    \Sigma^\infty C_c
    \ar[dd]|<<<<{ \phantom{A} }
    \ar@{-->}[r]
    \ar@{}[r]
    |-{
      \scalebox{.7}{$
        \begin{array}{c}
          \vdash
          {\color{orange}
            H^E_{n-1}\!(c)
          }
          \\
          {\phantom{a}}
        \end{array}
      $}
    }
    \ar@/^2pc/[rr]
    &
    \Sigma^n E
    \ar[r]
    \ar[dd]
    &
    \ast
    \ar[dd]
    \\
    \\
    \ast
    \ar[rr]
    &&
    \Sigma^{\infty\scalebox{.6}{$+1$}} S^{n + d - 1}
    \ar[r]^-{
      \color{magenta}
      M^{d}
    }
    \ar@/_1.2pc/[rr]|-{
      \;
      \Sigma^{\infty\scalebox{.5}{$+1$}}
      {\color{green}
        c
      }
      \;
    }
    &
    \Sigma^{n}(E\!/\mathbb{S})
    \ar[r]^{ \partial }
    &
    \Sigma^{\infty\scalebox{.6}{$+1$}} S^{n}
\end{xymatrix}

For given $H^E_{n-1}\!(c)$, this diagram is constructed as follows
(where we say "square" for any {\it single} cell and "rectangle" for the pasting composite of any adjacent {\it pair} of them):

* The two squares on the left are the stabilization of the homotopy pushout squares defining the cofiber space $C_c$ and the suspension of $S^{n + d - 1}$

* The bottom left rectangle (with $\Sigma^n(e^E)$ at its top)
is the homotopy pushout defining $\Sigma^n(E\!/\mathbb{S})$.

* The classifying map for the given $(n-1)$-flux, shown as a dashed arrow,
completes a co-cone under the bottom left square. Thus the map ${\color{magenta}M^d}$ forming the bottom middle square is uniquely implied by the homotopy pushout property of the bottom left square.
Moreover, the [[pasting law]] implies that this bottom middle square is itself homotopy cartesian.

* The bottom right square is the homotopy pushout defining $\partial$.

* By the [[pasting law]] it follows that also the bottom right rectangle is homotopy cartesian, hence that, after the two squares on the left, it exhibits the third step in the long homotopy cofiber sequence of $\Sigma^\infty c$. This means that its total bottom morphism is $\Sigma^{\infty + 1} c$, and hence that $\partial \big[ M^d \big] = [c]$.


In conclusion, these construction steps yield a map map $H^E_{n-1}\!(c) \mapsto M^d$ which is as required in (eq:TheMapFromEFluxes).

It only remains to see that this map is bijective over any $\Sigma^\infty c$: So assume conversely that $M^d$ is given, and with it the above diagram  except for the dashed arrow. But since the bottom right square is homotopy cartesian, a dashed morphism is uniquely implied. By its uniqueness, this reverse assignment $M^{2d} \mapsto H^E_{n-1}\!(c)$ must be the inverse of the previous construction.

\end{proof}

























\begin{xymatrix@=17pt}
    S^{2(n + d)-1}
    \ar@/^1.7pc/[drr]_-{\ }="s"
    \ar@/_1.7pc/[drr]^-{\ }="t"
    \\
    &&
    \;
    \big(
      (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}
    \big)^{2n}
    %
    \ar@{=>}
      %_{ {\color{magenta} e_{\mathbb{C}}(c)} }
      ^-{
        \!\!
        \mathrm{Td}
        [
          {\color{magenta}M^{2d}}
        ]
      }
    "s"; "t"
\end{xymatrix}



\begin{xymatrix@C=12pt}
    0
    \ar[r]
    &
    \big(
      \widetilde {H^{\mathrm{ev}}\mathbb{Q}}
    \big)
    {}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar@{=}[d]
    &&
    \big(
      \widetilde {(H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}}
    \big)
    {}^{2n}
    \big(
      S^{2(n+d)}
    \big)
    \ar[rr]
    \ar[d]|-{
      \hspace{2.7pt}
      \scalebox{.7}{
        \rotatebox{-90}{$
          \,
          \simeq
          \,
        $}
      }
    }
    &&
    \widetilde {\mathbb{S}}
    {}^{2n+1}
    \big(
      S^{2(n+d)}
    \big)
    \ar[r]
    \ar@{=}[d]
    &
    0
    \\
    0
    \ar[r]
    &
    \mathbb{Q}
    \;
    \ar@{^{(}->}[rr]
    &&
    \mathbb{Q}
    \oplus
    \mathbb{S}_{2d-1}
    \ar@{->>}@[red][rr]
    &&
    \mathbb{S}_{2d-1}
    \ar[r]
    &
    0
\end{xymatrix}

\begin{xymatrix@C=1.5em}
    S^{2(n + d)-1}
    \ar@/^1.7pc/[drr]_-{\ }="s"
    \ar@/_1.7pc/[drr]^-{\ }="t"
    \\
    &&
    \;
    \big(
      (H^{\mathrm{ev}}\mathbb{Q})/\mathbb{S}
    \big)^{2n}
    %
    \ar@{=>}
      %_{ {e_{\mathbb{C}}(c)} }
      ^-{
        \!\!
        \mathrm{Td}
        [
          {M^{2d}}
        ]
      }
    "s"; "t"
\end{xymatrix}
