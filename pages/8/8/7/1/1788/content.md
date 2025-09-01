> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***

\begin{proposition}
  **(fundamental crossed module of a fibration)**
  \label{FundamentalCrossedModuleOfAFibration}
\linebreak
  Given a [[Serre fibration]] $p \,\colon\, T \longrightarrow B$ of [[pointed topological spaces]], with [[fiber]] $\iota \,\colon\,F \longrightarrow T$, the induced [[homomorphism]] of [[fundamental groups]]
$$
  \pi_1(F)
  \xrightarrow{\phantom{--}
    \iota_\ast
  \phantom{--}}
  \pi_1(T)
$$
constitutes a [[crossed module]] with respect to the canonical [[group action]] of $\alpha \,\colon\, \pi_1(T) \times \pi_1(F) \longrightarrow \pi_1(F)$.
\end{proposition}
This is discussed in [Brown, Higgins & Sivera 2011, §2.6](#BHS11), there attributed to [[Daniel Quillen]].


\begin{proposition}
Given a [[Serre fibration]] $p \,\colon\, T \longrightarrow B$ of [[pointed topological spaces]], with [[fiber]] $\iota \,\colon\,F \longrightarrow T$, the [[image]] of the first [[connecting homomorphism]] of the corresponding [[long exact sequence of homotopy groups]]
$$
  \pi_2(B) \longrightarrow \pi_1(F)
$$
is in the [[center]] $Z\big(\pi_1(F)\big) \hookrightarrow \pi_1(F)$.
\end{proposition}
\begin{proof}
  By [[exact sequence|exactness]], the image in question is the [[kernel]] of $\pi_1(F) \to \pi_1(T)$, and that is central by Prop. \ref{FundamentalCrossedModuleOfAFibration}.

Usual textbooks usually state instead an analogous statement for the LES of relative homotopy groups: For $(X,A)$ a "[[CW-pair|pair]]", hence a [[subspace]] inclusion $A \hookrightarrow X$ (here: of [[pointed topological spaces]]), there is a [[long exact sequence]] of the form

$$
  \cdots
  \to
  \pi_{n+1}(X,A)
  \longrightarrow
  \pi_n(A)
  \longrightarrow
  \pi_n(X)
  \longrightarrow
  \pi_n(X,A)
$$

such that 

$$
  \pi_2(A) \longrightarrow \pi_2(X,A)
$$

factors through the center ([Whitehead 1978 Cor 3.5 on p. 166](#Whitehead78), [tom Dieck 2008 Cor 6.2.7](#tomDieck08)).

With a little care, this translates to the statement here by specializing $A \coloneqq T$ and taking $X \coloneqq Cyl(T \to B)$ to be the [[mapping cylinder]] of the fibration.
\end{proof}

$$
  Cyl(T \to B) \longrightarrow B
$$

that is a [[weak homotopy equivalence]]. Using this we get a morphism of exact sequences

$$
  \array{
    \pi_2(A)
    &\longrightarrow&
    \pi_2(X)
    &\longrightarrow&
    \pi_2(X,A)
    &\longrightarrow&
    \pi_1(A)
    &\longrightarrow&
    \pi_1(X)
    \\
    \downarrow
    &&
    \downarrow
    &&
    \downarrow
    &&
    \downarrow
    &&
    \downarrow
    \\
    \pi_2(T)
    &\longrightarrow&
    \pi_2(B)
    &\longrightarrow&
    \pi_1(F)
    &\longrightarrow&
    \pi_1(T)
    &\longrightarrow&
    \pi_1(B)
  }
$$ 

where the middle one is the composite

$$
  \pi_2(X,A) 
    \equiv
  \pi_2\big(
    Cyl(T \to B) , T
  \big)
  \to
  \pi_2\big(
    B
  \big)
  \to
  \pi_1(F)
$$


\end{proof}