> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***


\begin{lemma}

For $T \longrightarrow B$ a [[Serre fibration]] of [[pointed topological spaces]], with ([[homotopy fiber|homotopy]]) [[fiber]] $F \to T$, the [[connecting homomorphism]] in the LES

$$
  \pi_2(B) \longrightarrow \pi_1(F)
$$

factors through the [center](center#OfGroupsAndMonoids) of $\pi_1(F)$.

\end{lemma}
\begin{proof}

Textbooks usually state the analogous statement for the LES of relative homotopy groups, where it says that for $(X,A)$ a "[[CW-pair|pair]]", hence a [[subspace]] inclusion $A \hookrightarrow X$ (here: of [[pointed topological spaces]]), there is a [[long exact sequence]] of the form

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

factors through the center.

So we just need to translate: We set

* $A \coloneqq T$

and

* $X \coloneqq Cyl(T \to B)$

the [[mapping cylinder]] of our fibration, which has a canonical comparison map

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