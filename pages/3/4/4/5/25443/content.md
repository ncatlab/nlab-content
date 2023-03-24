#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The recognition principle for finite relative loop spaces states that, for $1 \leq N \lt \infty$, a pair of [[pointed topological space]]s is of the [[homotopy type]] of a relative $N$-loop space pair of some $(N-1)$-connected inclusion map if and only if it is a grouplike algebra over the [[Swiss cheese operad]] $\mathcal{SC}_N$, in the sense of an [[algebra over an operad]].

The recognition principle for infinite relative loop spaces states that a pair of pointed topological spaces is of the homotopy type of a relative $\infty$-loop space pair of some 1-shifted morphism of connective spectra if and only if it is a grouplike algebra over $\mathcal{SC}_\infty\coloneqq \colim_{N\to\infty}\mathcal{SC}_N$.

These are relative versions of [[May recognition theorem]] ([May 72](#May72), [May 74](#May74)) of loop spaces.

The recognition principle for relative $N$-loop spaces was proved in ([Vieira 2020](#VVieira2020)) for $3\leq N\leq \infty$. The proof there works in the cases $N=1,2$ if we assume the spaces connected. The general case for $N=1$ was proved in ([Hoefel, Livernet, Stasheff 2016](#HLS16)). The unconnected case for $N=2$ remains open.

Notoriously the loop space functors that appear in these recognition theorems are not right adjoint, thus they cannot be proved as an equivalence of homotopy categories induced by a [[Quillen equivalence]]. May's original strategy is to define what essentially constitutes adjunction units up to resolutions induced by the [[two-sided bar construction]]. The strategy of ([Vieira 2020](#VVieira2020)) is to define a generalization of [[Quillen adjunction]] that allow for the units and counits to exist only up to functorially determined resolutions, providing a natural model theoretical axiomatization of the essential elements of May’s original proof. For the full proof, homotopical versions of the concepts of [[idempotent monad]] and [[idempotent adjunction]] require similar generalizations. This is because we are interested in the homotopy subcategories of grouplike algebras and $(N-1)$-connected spaces/connective spectra. 

Bellow the proof of the relative recognition of $N$-loop spaces for $3\leq N\leq \infty$ using the machinery of idempotent quasiadjunctions in ([Vieira 2020](#VVieira2020)) is sketched.


## Idempotent weak Quillen quasiadjunctions

### Weak Quillen quasiadjunction

To construct the unit and counit natural transformations of an adjuction between homotopy categories of model categories it suffices to construct a unit natural span and counit natural cospan at the model categories level, plus some additional compatibility conditions.

\begin{definition}\label{QsiAdjQuilFr} ([Vieira 2020, Definition 2.1.1](#VVieira2020)) Let $\mathcal{T}$ and $\mathcal{A}$ be model categories. A weak Quillen quasiadjunction, or just quasiadjunction, between $\mathcal{T}$ and $\mathcal{A}$, denoted by 
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

If $\mathscr{C}$, $\mathscr{F}$, $\eta'$ and $\epsilon'$ are all identities and the homotopy equivalences in (v) and (vi) are equalities we recover the notion of a weak Quillen adjunction. If we further require $S$ to preserve cofibrations and $\Lambda$ to preserve fibrations we get a Quillen adjunction. Though the above information is weaker than that of a Quillen adjunction it suffices to construct an adjunction at the homotopy categories level. 


\begin{theorem} ([Vieira 2020, Theorem 2.1.2](#VVieira2020))
    A quasiadjunction induces an adjunction
$$
    (\mathbb{L}S \dashv\mathbb{R}\Lambda):\mathcal{H}o \mathcal{T}\rightleftharpoons \mathcal{H}o \mathcal{A}
$$
between the homotopy categories.
\end{theorem} 


### Idempotent quasi(co)monads

The following generalization of Quillen idempotent monads (see [[Bousfield-Friedlander theorem]]) was also introduced following the same principle of only requiring the existence of a unit natural span, and they also induce [[Bousfield localization]]s.

\begin{definition}([Vieira 2020, Definition 2.3.1](#VVieira2020))
    Let $\mathcal{T}$ be a right proper model category. A Quillen idempotent quasimonad on $\mathcal{T}$, or simply an idempotent quasimonad, is a pair of endofunctors $Q,\overline{\mathscr{C}}:\mathcal{T}\rightarrow\mathcal{T}$ equipped with a natural span 
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


\begin{theorem}([Vieira 2020, Theorem 2.3.5 / Proposition 2.3.6](#VVieira2020))
  An idempotent quasimonad induces a left Bousfield localization $\mathcal{T}_Q=(\mathcal{T};W_Q,C_Q,F_Q)$ with $W_Q=Q^{-1}W$, $C_Q=C$ and $F_Q\subset F$ the subset composed of the fibrations $(p:E\twoheadrightarrow B)\in F$ such that
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


The above definition can be dualized. The resulting idempotent quasicomonads induce right Bousfield localizations and associated coreflective homotopy subcategories.

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
where $cof : Cof \xRightarrow{\sim} Id$ and $fib : Id \xRightarrow{\sim} Fib$ are the functorial (co)fibrant resolutions of the model structures. 


\begin{definition}([Vieira 2020, Definition 2.3.7](#VVieira2020))
    An idempotent quasiadjunction is a quasiadjunction such that the induced span and cospan are respectively an idempotent quasimonad and an idempotent quasicomonad.
\end{definition}

\begin{theorem}([Vieira 2020, Theorem 2.3.8](#VVieira2020))
An idempotent quasiadjunction induces an equivalence between the associated (co)reflective homotopy subcategories.
$$
(\mathbb{L}S\dashv\mathbb{R}\Lambda):
\mathcal{H}o \mathcal{T}_{\Lambda Fib S Cof} \leftrightharpoons \mathcal{H}o \mathcal{A}_{S Cof \Lambda Fib}.
$$
\end{theorem}


## Finite relative recognition theorem

In this section fix some $1\leq N\lt \infty$. Let $\mathcal{SC}_N$ be the cubical Swiss cheese relative operad, a colored operad over the colors $\{c, o\}$, respectively referred to as the closed and open colors. It induces a monad $SC_N$ on the category $Top_*^{\{c, o\}}$ of pairs of pointed topological spaces (see [[algebra over an operad]]).  We denote pairs of pointed spaces as $X=(X_{c},X_{o})$. Denote by $\mathcal{SC}_N[Top]$ the category of algebras over $SC_N$, which we equip with the [[mixed model structure]] transferred from the one on $Top_*^{\{c, o\}}$.

Denote by $Top_*^\rightarrow$ the category of pointed maps, equipped with the mixed [[projective model structure]]. We denote maps as $Y=(Y:Y_0\rightarrow Y_1)$.

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


\begin{theorem} ([Vieira 2020, Proposition 2.2.3](#VVieira2020))
  We have a weak Quillen adjunction
$$
(\Sigma^N_\to \dashv \Omega^N_2):Top_*^{\{c,o\}}\leftrightharpoons Top_*^\to.
$$
\end{theorem}

This adjunction transfers a new model structure on $Top_*^\to$, with weak equivalences the commutative squares $f\in Top_*^\to(X,Y)$ such that $f_{0,*}:\pi_q X_0\to \pi_q Y_0$ are isomorphisms for all $q\geq N$ and $(f_0,f_1^I)_*:\pi_q(X_0\times_{X_1}X_1^I)\to \pi_q(Y_0\times_{Y_1}Y_1^I)$ are isomorphisms for all $q\geq N-1$. All objects of $Top_*^\to$ are fibrant in this model structure. We will say a pointed map $Y\in Top_*^\to$ is $(N-1)$-connected if $Y_0$ is $(N-2)$-connected and $Y_1$ is $(N-1)$-connected. The cofibrant objects are the $Y\in Top_*^\to$ that are homotopy equivalent to $(N-1)$-connected inclusions of relative CW-pairs. We denote the category of pointed maps equipped with this model structure as $Top^\to_{N-1}$.

The images of $\Omega^N_2$ are naturally algebras over $\mathcal{SC}_N$, so we have an induced functor $\Omega^N_2:Top_*^\to\rightarrow \mathcal{SC}_N[Top]$. This functor is not a right adjoint, but it does have a left weak Quillen quasiadjoint induced by the [[two-sided bar construction]].

\begin{definition}
  The relative $N$-delooping functor is
$$
B^N_\to:\mathcal{SC}_N[Top]\to Top_*^\to,\qquad B^N_\to(X)\coloneqq B(\Sigma^N_\to,SC_N,X).
$$
\end{definition}

\begin{definition}
  The resolution of $\mathcal{SC}_N$-spaces functor is
$$
\overline{B}_2:\mathcal{SC}_N[Top]\to\mathcal{SC}_N[Top],\qquad \overline{B}_2(X)=B(SC_N,SC_N,X).
$$
\end{definition}

\begin{theorem} ([Vieira 2020, Theorem 4.3.5, Theorem 4.3.8](#VVieira2020))
  We have an idempotent weak Quillen quasiadjunction
$$
  (B^N_\to\dashv_{\ \overline{B}_2,Id_{Top_*^\to}}\Omega^N_2):\mathcal{SC}_N[Top]\leftrightharpoons Top^\to_{N-1}.
$$
If $N\geq 3$ then this quasiadjunction induces an equivalence 
$$
(\mathbb{L}B^N_\to\dashv\mathbb{R}\Omega^N_2):\mathcal{H}o\mathcal{SC}_N[Top]_{grp}\leftrightharpoons \mathcal{H}o Top^\to_{N-1}
$$
between the homotopy subcategory of grouplike Swiss cheese algebras and the homotopy category of $(N-1)$-connected pointed maps.
\end{theorem}

\begin{remark}
In the reference [Vieira 2020](#VVieira2020) a cofibrant resolution of $\mathcal{SC}_N$ is used. The fact that $\mathcal{SC}_N$ is a $\Sigma$-cofibrant operad (see [[model structure on operads]]) when we consider the mixed model structure of collections means this assumption is not necessary. 
\end{remark}

\begin{remark}
The reason the proof of the above theorem doesn't extend to the cases $N=1,2$ is due to the fact that the constructed unit of the quasiadjunction is induced by a natural map $\alpha:SC_N\Rightarrow \Omega^N_2\Sigma^N_\to$ which is a natural pair of [[group completion]]s if and only if $N\geq 3$.
\end{remark}

## Infinite relative recognition theorem

  Let $Sp$ be the category of [[sequential spectra]], and $Sp^{\nearrow}$ the category composed of pairs of spectra $Y_0,Y_1\in Sp$ equipped with a 1-shifted spectra map $Y:Y_0\to Y_1[1]$. Morphisms are pairs of spectra maps that commute with the shifted spectra maps in the appropriate sense. It admits a strict mixed model structure with weak equivalences the level-wise weak homotopy equivalences and with fibrations the level-wise Hurewicz fibrations.

\begin{definition}
The spectrification functor is
$$
\widetilde{\Omega}:Sp\to Sp,\qquad \widetilde{\Omega}(Y)_\bullet\coloneqq \colim_{q\to\infty} \widetilde Y_{\bullet+q}^{\mathbb{S}^q}
$$
where $\widetilde{Y}$ is a certain inclusion prespectrum constructed from $Y$, equipped with a quotient map $Y\to \widetilde{Y}$ ([LMS 86, Appendix 1](#LewisMaySteinberger86)). If $Y$ is already an inclusion spectrum then $\widetilde Y=Y$. 

This functor induces a spectrification functor 
$$
\widetilde{\Omega}_{\nearrow}:Sp^{\nearrow}\to Sp^{\nearrow}
,\qquad \widetilde{\Omega}_{\nearrow}(Y)\coloneqq(\widetilde{\Omega}(Y):\widetilde{\Omega}(Y_0)\to \widetilde{\Omega}(Y_1)[1]).
$$
\end{definition}

We have a natural [[stable weak homotopy equivalence]] $\epsilon':Id_{Sp^{\nearrow}}\Rightarrow\widetilde{\Omega}_{\nearrow}$ which gives a Quillen idempotent monad structure on $\widetilde{\Omega}_{\nearrow}$. The stable mixed model structure on $Sp^{\nearrow}$ is the one induced by this idempotent monad, which is the left Bousfield localization of the strict mixed model structure on the pairs of stable weak homotopy equivalences.

\begin{definition}
  The relative base pair of spaces functor is
$$
\Lambda^\infty_2:Sp^{\nearrow}\to Top_*^{\{c,o\}},
\qquad \Lambda^\infty_2(Y)\coloneqq (Y_{10},Y_{00}\times_{Y_{11}}Y_{11}^I).
$$
The relative $\infty$-loop pair of spaces functor is 
$$\Omega^\infty_2:=\Lambda^\infty_2\widetilde{\Omega}_{\nearrow}:Sp^{\nearrow}\to Top_*^{\{c,o\}}.
$$
\end{definition}

The images of $\Omega^\infty_2$ are naturally algebras over $\mathcal{SC}_\infty$, so we have an induced functor $\Omega^\infty_2:Sp^{\nearrow}\rightarrow \mathcal{SC}_\infty[Top]$. 

\begin{definition}
The relative $\infty$-delooping functor is
$$
B^\infty_\nearrow:\mathcal{SC}_\infty[Top]\to Sp_\nearrow,
\qquad 
B^\infty_\nearrow(X)_\bullet\coloneqq B(\Sigma^{\bullet+1}_\to,SC_{\bullet+1},X).
$$
\end{definition}

\begin{definition}
  The resolution of $\mathcal{SC}_\infty$-spaces functor is
$$
\overline{B}_2:\mathcal{SC}_\infty[Top]\to\mathcal{SC}_\infty[Top],\qquad \overline{B}_2(X)=B(SC_\infty,SC_\infty,X).
$$
\end{definition}

\begin{theorem}([Vieira 2020, Theorem 4.3.5, Theorem 4.3.8](#VVieira2020))
  We have an idempotent weak Quillen quasiadjunction
$$
  (B^\infty_\nearrow\dashv_{\ \overline{B}_2,\widetilde{\Omega}_\nearrow}\Omega^\infty_2):\mathcal{SC}_\infty[Top]\leftrightharpoons Sp^\nearrow
$$
which induces an equivalence 
$$
(\mathbb{L}B^\infty_\nearrow\dashv\mathbb{R}\Omega^\infty_2):\mathcal{H}o\mathcal{SC}_\infty[Top]_{grp}\leftrightharpoons \mathcal{H}o Sp^\nearrow_{con}
$$
between the homotopy category of grouplike Swiss cheese algebras and the homotopy category of shifted spectra maps between connective spectra.
\end{theorem}


## References

* {#HLS16} [[Eduardo Hoefel]], [[Muriel Livernet]], [[Jim Stasheff]], _$A_\infty$-actions and recognition of relative loop spaces_, Topology and its Applications,
Vol. 206, 2016, Pages 126-147 ([arXiv:1312.7155](https://arxiv.org/abs/1312.7155),[doi:10.1016/j.topol.2016.03.023](https://doi.org/10.1016/j.topol.2016.03.023))

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], [[Mark Steinberger]] (with contributions by [[James McClure|J.E. McClure]]), _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics  **1213** (1986) &lbrack;[pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf), [doi:10.1007/BFb0075778](https://link.springer.com/book/10.1007/BFb0075778)&rbrack;

* {#May72} [[Peter May]], _The geometry of iterated loop spaces_, Lecture Notes in Mathematics, Springer 1972 ([doi:10.1007/BFb0067491](https://link.springer.com/book/10.1007/BFb0067491), [pdf](http://www.math.uchicago.edu/~may/BOOKS/gils.pdf))

* {#May74} [[Peter May]], _$E_\infty$-Spaces, group completions, and permutative categories_, New Developments in Topology, London Math. Soc. Lecture Note Series 11 (1974) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/13.pdf))

* {#VVieira2020} [[Renato Vasconcellos Vieira]], _Relative recognition principle_, Algebr. Geom. Topol. 20(3): 1431-1486 (2020) ([arXiv:1802.01530](https://arxiv.org/abs/1802.01530), [doi:10.2140/agt.2020.20.1431](https://doi.org/10.2140/agt.2020.20.1431))