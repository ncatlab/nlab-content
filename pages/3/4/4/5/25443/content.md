#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The recognition principle for finite relative loop spaces states that, for $1 \leq N \lt \infty$, a pair of pointed topolological spaces is of the homotopy type of a relative $N$-loop space pair of some $(N-1)$-connected topological pair if and only if it is a grouplike algebra over the Swiss-Cheese relative operad $\mathcal{SC}_N$.

The recognition principle for infinite relative loop spaces states that a pair of pointed toplological spaces is of the homotopy type of a relative $\infty$-loop space pair of some 1-shifted morphism of connective spectra if and only if it is a grouplike algebra over $\mathcal{SC}_\infty$.


## Idempotent weak Quillen quasiadjunctions

\subsection{Weak Quillen quasiadjunction}

The following definition introduced in \cite{Vi20} is a generalization of Quillen adjunctions between model categories. The basic idea is that to construct the unit and counit natural transformations of an adjuction between the homotopy categories it suffices to construct a unit natural span and counit natural cospan at the model categories level, plus some additional compatibility conditions.

\begin{definition}\label{QsiAdjQuilFr} Let $\mathcal{T}$ and $\mathcal{A}$ be model categories. A weak Quillen quasiadjunction, or just quasiadjunction, between $\mathcal{T}$ and $\mathcal{A}$, denoted by 
$$
(S \dashv_{\ C,F}\Lambda):\mathcal{T}\rightleftharpoons \mathcal{A},
$$
is a quadruple of functors
\begin{center}\begin{xymatrix}
\mathcal{T}\ar@<0.1cm>[r]^{S}\ar@(dl,ul)[]^{C}&\mathcal{A}\ar@<0.1cm>[l]^{\Lambda}\ar@(ur,dr)[]^{F}
\end{xymatrix}\end{center}
with $S$ the left quasiadjoint and $\Lambda$ the right quasiadjoint, equipped with a natural span in $\mathcal{T}$ and a natural cospan in $\mathcal{A}$
\begin{center}
\begin{xymatrix}
Id_{\mathcal{T}}& C \ar@{=>}[l]_{\eta'}^{\sim}\ar@{=>}[r]^{\eta}
& \Lambda S
&&
& S \Lambda \ar@{=>}[r]^{\epsilon}
&F
& Id_{\mathcal{A}} \ar@{=>}[l]_{\epsilon'}^{\sim} 
\end{xymatrix}
\end{center}

such that

 (i) $S$ is left derivable;
        
 (ii) $\Lambda$ is right derivable;
        
 (iii) $\mathscr{C}$ and $\mathscr{F}$ preserve cofibrant and fibrant objects;
        
 (iv) $\eta'$ and $\epsilon'$ are natural weak equivalences;
        
 (v) If $X\in\mathcal{T}$ is cofibrant then $\epsilon_{SX}S\eta_X\simeq \epsilon'_{SX}S\eta_X'$;
        
 (vi) If $Y\in\mathcal{A}$ is fibrant then $\Lambda\epsilon_Y \eta_{\Lambda Y}\simeq \Lambda\epsilon'_Y\eta'_{\Lambda Y}$.



## Finite relative recognition theorem

Let $1\leq N\leq \infty$ and $\mathcal{SC}_N$ be the cubical Swiss Cheese relative operad, a colored operad over the colors $\{c, o\}$, respectively referred to as the closed and open colors. It induces a monad $SC_N$ on the category $Top_*^2$ of pairs of pointed topological spaces. Denote by $\mathcal{SC}_N[Top]$ the category of algebras over $SC_N$, which we equip with the mixed model structure induced by the one on $Top_*^2$. We denote pairs of pointed spaces as $X=(X_{c},X_{o})$.

Denote by $Top_*^\rightarrow$ the category of pointed maps, equipped with the mixed projective model structure. We denote maps as $Y=(Y:Y_d\rightarrow Y_c)$.

\begin{definition}
For $1 \leq N \lt \infty$ the relative $N$-loop space functor is
$$
  \Omega^N_2:Top_*^{\rightarrow}\rightarrow Top_*^2,\qquad \Omega^N_2(Y):=(Y_c^{\mathbb{S}^N},(Y_o\times_{Y_c} Y_c^I)^{\mathbb{S}^{N-1}}).
$$

The $N$-suspension functor is
$$
\Sigma^N_\to : Top_*^2\to Top_*^\to, \qquad
\Sigma^N_\to(X)=
(X_{o} \wedge \mathbb{S}^{N-1} \to ((X_o \wedge I) \vee(X_c \wedge \mathbb{S}^1)) \wedge \mathbb{S}^{N-1} ).
$$
\end{definition}

\begin{theorem}
  We have a weak Quillen adjunction
$$
(\Sigma^N_\to \rvert \Omega^N_2).
$$
\end{theorem}



## Infinite relative recognition theorem