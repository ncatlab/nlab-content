#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The recognition principle for finite relative loop spaces states that, for $1 \leq N \lt \infty$, a pair of pointed topolological spaces is of the homotopy type of a relative $N$-loop space pair of some $(N-1)$-connected topological pair if and only if it is a grouplike algebra over the Swiss-Cheese relative operad $\mathcal{SC}_N$.

The recognition principle for infinite relative loop spaces states that a pair of pointed toplological spaces is of the homotopy type of a relative $\infty$-loop space pair of some 1-shifted morphism of connective spectra if and only if it is a grouplike algebra over $\mathcal{SC}_\infty$.


## Idempotent weak Quillen quasiadjunctions

### Weak Quillen quasiadjunction

The following definition introduced in Vi20 is a generalization of Quillen adjunctions between model categories. The basic idea is that to construct the unit and counit natural transformations of an adjuction between the homotopy categories it suffices to construct a unit natural span and counit natural cospan at the model categories level, plus some additional compatibility conditions.

\begin{definition}\label{QsiAdjQuilFr} Let $\mathcal{T}$ and $\mathcal{A}$ be model categories. A weak Quillen quasiadjunction, or just quasiadjunction, between $\mathcal{T}$ and $\mathcal{A}$, denoted by 
$$
(S \dashv_{\ \mathscr{C},\mathscr{F}}\Lambda):\mathcal{T}\rightleftharpoons \mathcal{A},
$$
is a quadruple of functors
$$
\mathscr{C}:\mathcal{T} \to \mathcal{T}
,\quad
\mathscr{F}:\mathcal{A} \to \mathcal{A}
,\quad
S:\mathcal{T} \to \mathcal{A}
,\quad
\Lambda:\mathcal{A} \to \mathcal{T}
$$
with $S$ the left quasiadjoint and $\Lambda$ the right quasiadjoint, equipped with a natural span in $\mathcal{T}$ and a natural cospan in $\mathcal{A}$
$$
\eta':\mathscr{C}\xRightarrow{\sim} Id_{\mathcal{T}}
,\quad
\eta:\mathscr{C}\Rightarrow \Lambda S
,\qquad
\epsilon:S \Lambda \Rightarrow \mathscr{F},
\quad
\epsilon':Id_{\mathcal{A}}\xRightarrow{\sim}\mathscr{F}
$$

such that

 (i) $S$ is left derivable;
        
 (ii) $\Lambda$ is right derivable;
        
 (iii) $\mathscr{C}$ and $\mathscr{F}$ preserve cofibrant and fibrant objects;
        
 (iv) $\eta'$ and $\epsilon'$ are natural weak equivalences;
        
 (v) If $X\in\mathcal{T}$ is cofibrant then $\epsilon_{SX}S\eta_X\simeq \epsilon'_{SX}S\eta_X'$;
        
 (vi) If $Y\in\mathcal{A}$ is fibrant then $\Lambda\epsilon_Y \eta_{\Lambda Y}\simeq \Lambda\epsilon'_Y\eta'_{\Lambda Y}$.
\end{definition}

\begin{theorem}
    A quasiadjunction induces an adjunction
$$
    (\mathbb{L}S \dashv\mathbb{R}\Lambda):\mathcal{H}o \mathcal{T}\rightleftharpoons \mathcal{H}o \mathcal{A}
$$
between the homotopy categories.
\end{theorem} 




### Idempotent quasi(co)monads

The following generalization of idempotent Quillen monads \cite{BF78} was also introduced following the same principle of only requiring the existence of a unit natural span, and they also induce Bousfield localizations.

\begin{definition}
    Let $\mathcal{T}$ be a right proper model category. A Quillen idempotent quasimonad on $\mathcal{T}$, or simply an \textit{idempotent quasimonad}, is a pair of endofunctors $Q,\overline{\mathscr{C}}:\mathcal{T}\rightarrow\mathcal{T}$ equipped with a natural span 
$$
  \eta':\overline{\mathscr{C}}\xRightarrow{\sim}Id_{\mathcal{T}}
,\qquad 
\eta:\overline{\mathscr{C}}\Rightarrow Q
$$
such that:
    
(i) $\eta'$ is a natural weak equivalence;
        
(ii) $Q$ preserves weak equivalences;
        
(iii) $Q\eta$ and $\eta_{Q}$ are natural weak equivalences;
        
(iv) If $f\in\mathcal{T}(X,B)$, $p\in F(E,B)$ and $\eta_E,\eta_B,Qf\in W$ then $Q(f^\ast p)\in W$;
            
(v) If $\iota\in C(\overline{\mathscr{C}} X,K)$ then $\iota_\ast \eta'\in W$.
\end{definition}


The above definition can be dualized. The resulting idempotent quasicomonads induce right Bousfield localizations and associated coreflective homotopy subcategories.


\begin{theorem}
  An idempotent quasimonad induces a left Bousfield localization $\mathcal{T}_Q=(\mathcal{T};W_Q,C_Q,F_Q)$ with $W_Q=Q^{-1}W$, $C_Q=C$ and $F_Q\subset F$ the subset composed of the fibrations $p\in F$ such that
\begin{center}
\begin{xymatrix@=0.5cm}    E\ar@{->>}[d]_p\ar[r]^(0.25){i_E}&E\sqcup_{\overline{C} E}QE\ar[d]^{(p,Qp)}\\
    B\ar[r]_(0.25){i_B}&B\sqcup_{\overline{C} B}QB
\end{xymatrix}
\end{center}
is a homotopy pullback.

The resulting homotopy category is the reflective subcategory
$$\mathcal{H}o \mathcal{T}_Q:=\{X\in \mathcal{H}o \mathcal{T}\mid (i_X:X\rightarrow X\sqcup_{\overline{\mathscr{C}} X}QX)\in W\}
$$
of $Q$-fibrant objects.

\end{theorem}


### Idempotent quasiadjunctions

A quasiadjunction $(S\dashv_{\ \mathscr{C},\mathscr{F}}\Lambda):\mathcal{T}\rightleftharpoons \mathcal{A}$ induces the following natural span on $\mathcal{T}$ and natural cospan on $\mathcal{A}$
$$
  cof \eta'_{Cof}:\mathscr{C} Cof\xRightarrow{\sim} Id_{\mathcal{T}},
\quad 
(\Lambda fib_S \eta)_{Cof}:\mathscr{C} Cof\Rightarrow \Lambda Fib S Cof
$$
$$
  (\epsilon S cof_{\Lambda})_{Fib}: S Cof \Lambda Fib\Rightarrow \mathscr{F} Fib,
\quad
\epsilon'_{Fib}fib:Id_{\mathcal{A}}\xRightarrow{\sim} \mathscr{F} Fib
$$
\begin{definition}
    An idempotent quasiadjunction is a quasiadjunction such that the induced span and cospan are respectively an idempotent quasimonad and an idempotent quasicomonad.
\end{definition}

\begin{theorem}
An idempotent quasiadjunction induces an equivalence between the associated (co)reflective homotopy subcategories.
$$
(\mathbb{L}S\dashv\mathbb{R}\Lambda):
\mathcal{H}o \mathcal{T}_{\Lambda Fib S Cof} \leftrightharpoons \mathcal{H}o \mathcal{A}_{S Cof \Lambda Fib}.
$$
\end{theorem}


## Finite relative recognition theorem

In this section fix some $1\leq N\lt \infty$. Let $\mathcal{SC}_N$ be the cubical Swiss-Cheese relative operad, a colored operad over the colors $\{c, o\}$, respectively referred to as the closed and open colors. It induces a monad $SC_N$ on the category $Top_*^{\{c, o\}}$ of pairs of pointed topological spaces.  We denote pairs of pointed spaces as $X=(X_{c},X_{o})$. Denote by $\mathcal{SC}_N[Top]$ the category of algebras over $SC_N$, which we equip with the mixed model structure induced by the one on $Top_*^{\{c, o\}}$.

Denote by $Top_*^\rightarrow$ the category of pointed maps, equipped with the mixed projective model structure. We denote maps as $Y=(Y:Y_0\rightarrow Y_1)$.

\begin{definition}
The relative $N$-loop pair functor is
$$
  \Omega^N_2:Top_*^{\rightarrow}\rightarrow Top_*^{\{c,o\}},\qquad \Omega^N_2(Y)\coloneqq(Y_1^{\mathbb{S}^N},(Y_0\times_{Y_1} Y_1^I)^{\mathbb{S}^{N-1}}).
$$

The relative $N$-suspension functor is
$$
\Sigma^N_\to : Top_*^{\{c,o\}}\to Top_*^\to, \qquad
\Sigma^N_\to(X)\coloneqq
(X_{o} \wedge \mathbb{S}^{N-1} \to ((X_o \wedge I) \vee(X_c \wedge \mathbb{S}^1)) \wedge \mathbb{S}^{N-1} ).
$$
\end{definition}


\begin{theorem}
  We have a weak Quillen adjunction
$$
(\Sigma^N_\to \dashv \Omega^N_2):Top_*^{\{c,o\}}\leftrightharpoons Top_*^\to.
$$
\end{theorem}

This adjunction transfers a new model structure on $Top_*^\to$, with weak equivalences the commutative squares $f\in Top_*^\to(X,Y)$ such that $f_{0,*}:\pi_q X_0\to \pi_q Y_0$ are isomorphisms for all $q\geq N$ and $(f_0,f_1^I)_*:\pi_q(X_0\times_{X_1}X_1^I)\to \pi_q(Y_0\times_{Y_1}Y_1^I)$ are isomorphisms for all $q\geq N-1$. All objects of $Top_*^\to$ are fibrant in this model structure. We will say a pointed map $Y\in Top_*^\to$ is $(N-1)$-connected if $Y_0$ is $(N-1)$-connected and $Y_1$ is $N$-connected. The cofibrant objects are the $Y\in Top_*^\to$ that are the $(N-1)$-connected inclusions of relative CW-pairs. We denote the category of pointed maps equipped with this model structure as $Top^\to_{N-1}$.

The images of $\Omega^N_2$ are naturally algebras over $\mathcal{SC}_N$, so we have an induced functor $\Omega^N_2:Top_*^N\rightarrow \mathcal{SC}[Top]$. This functor is not a right adjoint, but it does have a left weak Quillen quasiadjoint induced by the two-sided bar construction.

\begin{definition}
  The relative $N$-delooping functor is
$$
B^N_\to:\mathcal{SC}_N[Top]\to Top_*^\to,\qquad B^N_\to(X)\coloneqq B(\Sigma^N_\to,SC_N,X).
$$
\end{definition}

\begin{definition}
  The resolution of $\mathcal{SC}_N$-spaces functor is
$$
\overline{B}_2^N:\mathcal{SC}_N[Top]\to\mathcal{SC}_N[Top],\qquad \overline{B}_2^N(X)=B(SC_N,SC_N,X).
$$
\end{definition}

\begin{theorem}
  If $N\geq 3$ then we have an idempotent weak Quillen quasiadjunction
$$
  (B^N_\to\dashv_{\ \overline{B}^N_2,Id_{Top_*^\to}}\Omega^N_2):\mathcal{SC}_N[Top]\leftrightharpoons Top^\to_{N-1}
$$
which induces an equivalence 
$$
(\mathbb{L}B^N_\to\dashv\mathbb{R}\Omega^N_2):\mathcal{H}o\mathcal{SC}_N[Top]_{grp}\leftrightharpoons \mathcal{H}oTop^\to_{N-1}
$$
between the homotopy subcategory of grouplike Swiss-Cheese spaces and the homotopy category of $(N-1)$-connected pointed maps.
\end{theorem}



## Infinite relative recognition theorem

  Let $Sp^{\nearrow}$ be the category composed of pairs of spectra $Y_0,Y_1\in Sp$ equipped with a 1-shifted spectra map $Y:Y_0\to Y_1[1]$. Morphisms are pairs of spectra maps that commute with the shifted spectra maps in the appropriate sense. It admits a strict mixed model structure with weak equivalences the level-wise weak homotopy equivalences and with fibrations the level-wise Hurewicz fibrations. The cofibrations are the maps $f:X\to Y$ such that the maps
$$(f_{0\bullet},\sigma_{\bullet-1}):X_{0\bullet}\vee_{X_{0(\bullet-1)}\wedge\mathbb{S}^1}(Y_{0(\bullet-1)}\wedge\mathbb{S}^1)\to Y_{0\bullet}
$$


$$ 
((f_{1\bullet},Y_{\bullet-1}),\sigma_{\bullet-1})
:(X_{1\bullet}\vee_{X_{0(\bullet-2)}}Y_{0(\bullet-2)})\vee_{(X_{1(\bullet-1)}\vee_{X_{0(\bullet-2)}}Y_{0(\bullet-2)})\wedge\mathbb{S}^1} Y_{1(\bullet-1)}\wedge\mathbb{S}^1 \to Y_{1\bullet}
$$
are $m$-cofibrations.

\begin{definition}
The spectrification functor is
$$
\widetilde{\Omega}:Sp\to Sp,\qquad \widetilde{\Omega}(Y)_\bullet\coloneqq \colim_{q\to\infty} \overline Y_{\bullet+q}^{\mathbb{S}^q}
$$

\end{definition}
