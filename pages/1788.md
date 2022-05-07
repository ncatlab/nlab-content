Please do not delete the following example for the moment!

An article by \cite{vandenBergGarner2011} and another by \cite{MarraReggio2020}.

\section{References}

\bibitem{MarraReggio2020}

\bibitem{vandenBergGarner2011}


\linebreak

\linebreak

\begin{xymatrix@C=20pt}
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        framed Cobordism
      \end{tabular}
    }
    }
  }{
  \mathrm{Cob}^{n}_{\mathrm{Fr}}
    \big(
      M^d
    \big)
  }
  \ar@{}[r]
  |-{:=}
  &
  \mathrm{NFramedSubMflds}_{d-n}
  \big(
    M^d
  \big)_{\!\!\big/\mathrm{brdsm}}
  \ar@<+10pt>[rr]
    ^-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        \begin{tabular}{c}
          asymptotic directed distance
        \end{tabular}
      }
    }
  \ar@{}[rr]
    |-{ \simeq }
  \ar@<-10pt>@{<-}[rr]
    _-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        pre-image of regular value
      }
    }
  &
  {\phantom{AAAAA}}
  &
  \mathrm{Maps}
  \big(
    M^d
    \,,\,
    S^n
  \big)_{\!\!\big/ \mathrm{hmpty}}
  \ar@{}[r]
    |-{ =: }
  &
  \overset{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        Cohomotopy
      \end{tabular}
    }
  }{
    \pi^n
    \big(
      M^d
    \big)
  }
\end{xymatrix}



\begin{xymatrix@C=20pt}
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        framed Cobordism
      \end{tabular}
    }
    }
  }{
  \mathrm{Cob}^{n}_{\mathrm{Fr}}
    \big(
      M^d
    \big)
  }
  \ar@{}[r]
  |-{:=}
  &
  \mathrm{NFramedSubMflds}_{d-n}
  \big(
    M^d
  \big)_{\!\!\big/\mathrm{brdsm}}
  \ar@<+10pt>[rr]
    ^-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        \begin{tabular}{c}
          asymptotic directed distance
        \end{tabular}
      }
    }
  \ar@{}[rr]
    |-{ \simeq }
  \ar@<-10pt>@{<-}[rr]
    _-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        pre-image of regular value
      }
    }
  &
  {\phantom{AAAAA}}
  &
  \pi_0
  \mathrm{Maps}^{\ast/\!}
  \Big(
    \big(
      M^d
    \big)^{\mathrm{cpt}}
    \,,\,
    S^n
  \Big)
  \ar@{}[r]
    |-{ =: }
  &
  \overset{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        reduced Cohomotopy
      \end{tabular}
    }
  }{
    {\widetilde \pi}{}^n
    \Big(
      \big(
        M^d
      \big)^{\mathrm{cpt}}
    \Big)
  }
\end{xymatrix}



\begin{xymatrix@C=20pt}
  {\phantom{AA}}
  \overset{
    \mathclap{
    \raisebox{3pt}{
      \tiny
      \color{blue}
      \bf
      \begin{tabular}{c}
        unstable
        \\
        oriented Cobordism
      \end{tabular}
    }
    }
  }{
  \mathrm{Cob}^{n}_{\mathrm{SO}}
    \big(
      M^d
    \big)
  }
  \ar@{}[r]
  |-{:=}
  &
  \mathrm{NOrientedSubMflds}_{d-n}
  \big(
    M^d
  \big)_{\!\!\big/\mathrm{brdsm}}
  \ar@<+10pt>[rr]
    ^-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        \begin{tabular}{c}
          asymptotic directed distance
        \end{tabular}
      }
    }
  \ar@{}[rr]
    |-{ \simeq }
  \ar@<-10pt>@{<-}[rr]
    _-{
      \mbox{
        \tiny
        \color{olive}
        \bf
        pre-image of $B \mathrm{SO}(n)$
      }
    }
  &
  {\phantom{AAAAA}}
  &
  \pi_0
  \mathrm{Maps}^{\ast/\!}
  \Big(
    \big(
      M^d
    \big)^{\mathrm{cpt}}
    \,,\,
    M \mathrm{SO}(n)
  \Big)
  {\phantom{AAAAAAAA}}
\end{xymatrix}

\begin{prop}
  For $n \geq 1$ a [[positive number|positive]] [[natural number]] and $(X,x)$ a [[pointed topological space]]/[[pointed homotopy type]], the canonical [[morphism]] from reduced to unreduced Cohomotopy of $X$ in degree $n$ is an [[isomorphism]]:

$$
  {\widetilde \pi}^{n \geq 1}(X,x)
    \overset{\;\;\simeq\;\;}{\longrightarrow}
  {\pi}^{n \geq 1}(X)
  \,.
$$
\end{prop}
\begin{proof}
  For $Maps(-,-)$ denoting [[compact-open topology|mapping space]] for [[topological spaces]] and $Maps^{\ast/}(-,-)$ the subspace for [[pointed topological spaces]], observe that 

$$
  Maps^{\ast/}\big((X,x),(S^n,\ast) \big)
    \overset{fib(ev_x)}{\longrightarrow}
  Maps\big(X,S^n \big)
    \overset{ev_x}{\longrightarrow}
  S^n
$$

(where $ev_x$ is the [[evaluation map]] at $x \in X$) is a [[homotopy fiber sequence]] as soon as $X$ is represented by a [[cell complex]] (e.g. [[CW-complex]]). 

(This follows either from the [pullback-power axiom](enriched+model+category#PullbackPowerAxiom) in the [[classical model structure on topological spaces]], or, more abstractly from the characterization of [[derived hom-spaces]] in [[slice (infinity,1)-category|coslice (infinity,1)-categories]] [here](slice+infinity-category#HamSpacesInASlice)).

Therefore we have the corresponding [[long exact sequence of homotopy groups]], which starts out as

\begin{xymatrix@C=20pt}
  \pi_1\big( S^n \big)
  \ar[r]
  \ar@{=}[d]
  & 
  \pi_0 \mathrm{Maps}^{\ast/}\big((X,x),(S^n,\ast) \big)
  \ar[r]^{  }
  \ar@{=}[d]
  &
  \pi_0 \mathrm{Maps}\big(X,S^n \big)
  \ar[r]
  \ar@{=}[d]
  &
  \pi_0(S^n)
  \ar@{=}[d]
  \\
  {\overbrace{
  \begin{array}{ccc}
    \mathbb{Z} &\!\!\vert\!\!& n = 1
    \\
    \ast &\!\!\vert\!\!& n \geq 2
  \end{array}
  }}
  \ar[r]
  &
  {\widetilde \pi}{}^n(X,x)    
  \ar[r]
  &
  {\pi}{}^n(X)
  \ar[r]
  &
  \ast
  \,.
\end{xymatrix}

By exactness, this yields the claim for $n \geq 2$; while for $n = 1$ it gives the desired isomorphism only up to a possibly non-trivial [[quotient set|quotient]] by an [[action]] of $\mathbb{Z} \simeq \pi_1(S^1)$:

$$
  {\widetilde \pi}{}^1(X,x)/\pi_1(S^1)
  \simeq
  \pi^1(X)
  \,.
$$

Hence it is now sufficient to see that the $\pi_1(S^1)$-[[action]] on reduced 1-Cohomotopy is always trivial:

The action of $n \in \pi_1(S^1)$ takes $\big[ (X,x) \overset{ \;c\; }{\longrightarrow} (S^1,\ast) \big]$ to any $\big[ (X,x) \overset{ \;c'\; }{\longrightarrow} (S^1,\ast) \big]$ such that $[X \overset{c}{\longrightarrow} S^1] \overset{\eta}{\Rightarrow} [X \overset{c'}{\longrightarrow} S^1]$ in $\pi^1(X)$, with $[\eta(x,-)] = n \in \pi_1(S^1)$. 

But using the [[group]]-structure on $S^1 = \mathbb{R}/\mathbb{Z}$  we have that one such $\eta$ is given by $\eta(x,t) \coloneqq c(x) + n t \,mod\, \mathbb{Z}$, which yields $c'(x) = c(x) + n \,mod\, \mathbb{Z}$ and hence $c' = c$.

\end{proof}


