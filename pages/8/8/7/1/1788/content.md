> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***



* Nora Doll, [[Hermann Schulz-Baldes]], [[Nils Waterstraat]]:  *Homotopy Theory of Fredholm Operators*, Chapter 8 in: *Spectral Flow --- A Functional Analytic and Index-Theoretic Approach*, Studies in Mathematics **94**, De Gruyter (2023) &lbrack;[doi:10.1515/9783111172477](https://doi.org/10.1515/9783111172477), ch8:[[DSBW23-HomotopyFredholmOps.pdf:file]]&rbrack;


All [[linear operators]] in the following act on a given [[separable Hilbert space|separable]] countably infinite-dimensional [[complex numbers|complex]] [[Hilbert space]].

Consider and denote:

* $\mathcal{B}$ --- the space of [[bounded operators]],

* $\mathcal{K} \subset \mathcal{B}$ --- the subspace of [[compact operators]],

* $\mathcal{C} \coloneqq \mathcal{B}/\mathcal{K}$  --- the [[Calkin algebra]] regarded as a [[C*-algebra|$C^\ast$-algebra]],

* $\mathbf{p} \colon \mathcal{B} \twoheadrightarrow \mathcal{C}$  --- the [[quotient]] [[coprojection]],

* $\mathcal{G} \coloneqq \mathcal{C}^\times = GL(\mathcal{C})$  --- the [[group of units]] of the [[Calkin algebra]],

* $\widehat{\mathcal{G}} \subset \mathcal{G}$  --- the subgroup of [[self-adjoint elements]],

* $\widehat{\mathcal{G}}_{\pm} \subset \widehat{\mathcal{G}}$   --- the subgroup of elements with purely positibe/negative [[essential spectrum]], 

* $\widehat{\mathcal{G}}_{\ast} \subset \widehat{\mathcal{G}}$   --- the remaining subspace, of elements whose essential spectrum is both positive and negative,

* $G \coloneqq \mathrm{U}(\mathcal{C}) \subset GL(\mathcal{C})$ --- the [[unitary group]] of the Calkin algebra, 

* $\widehat{G} \coloneqq \widehat{\mathcal{G}} \cap G$ --- the group of self-adjoint unitary elements of the Calkin algebra

* $\widehat{G}_{\pm} \coloneqq \widehat{\mathcal{G}}_{\pm} \cap G$ --- the group of self-adjoint unitary elements of the Calkin algebra with purely positive/negative essential spectrum,

* $\widehat{G}_{\ast} \coloneqq \widehat{\mathcal{G}}_{\ast} \cap G$ --- the group of self-adjoint unitary elements of the Calkin algebra with both positive and negative essential spectrum,

* $\mathcal{F} \simeq \mathbf{p}^{-1}(\mathcal{G})$  --- the space of [[Fredholm operators]],

* $\widehat{\mathcal{F}} \subset \mathcal{F}$  --- the subspace of self-adjoint Fredholm operators,

* $\widehat{\mathcal{F}}_{\pm} \subset \widehat{\mathcal{F}}$  --- the subspace of operators with purely positive/negative [[essential spectrum]],
  
* $\widehat{\mathcal{F}}_{\ast} \subset \widehat{\mathcal{F}}$  --- the remaining subspace, that of operators with both positive and negative [[essential spectrum]],


\begin{proposition}

We have [[homeomorphisms]]:

\[
  \begin{aligned}
     \widehat{\mathcal{G}} 
     & \;\simeq\; 
     \widehat{\mathcal{G}}_+ 
       \sqcup 
     \widehat{\mathcal{G}}_- 
       \sqcup 
     \widehat{\mathcal{G}}_\ast
     \\
     \widehat{\mathcal{F}} 
     & \;\simeq\; 
     \widehat{\mathcal{F}}_+ 
       \sqcup 
     \widehat{\mathcal{F}}_- 
       \sqcup 
     \widehat{\mathcal{F}}_\ast
     \\
     \widehat{G}_\pm 
     & \;\simeq\; 
     \{ \pm id \}
     \\
     \widehat{G}_\ast
     & \;\simeq\; 
     \big\{
       g \in \mathcal{C}
       \;\Big\vert\;
       g^\ast = g
       ,\;
       g^2 = id
       ,\;
       g \neq \pm id
     \big\}
     \\
     & \;\simeq\; 
     \big\{
       g \in \mathcal{C}
       \;\Big\vert\;
       g^\ast = g
       ,\;
       spec(g) = \{+1, -1\}
     \big\}
     \\
     & \;\simeq\;
     \underset{
       Gr(\mathcal{C})
     }{
     \underbrace{
       \big\{ 
          p \in \mathcal{C} 
       \,\big\vert\, 
          p^2 = p = p^\ast \neq 0, id 
       \big\} 
     }}
  \end{aligned}
\]

and [[homotopy equivalences]]:

\[
  \begin{aligned}
    \widehat{\mathcal{G}}_{\pm} 
     & \;\sim\; 
    \widehat{G}_{\pm} \;\sim\; \ast
    \\
    \widehat{\mathcal{F}}_{\pm} 
    & \;\sim\; 
    \mathbf{p}^{-1}\big(\widehat{\mathcal{G}}_{\pm}\big)
      \;\sim\; 
      \ast
    \\
    \widehat{\mathcal{F}}_{\ast} 
    & \;\sim\; 
    \mathbf{p}^{-1}\big(\widehat{\mathcal{G}}_{\ast}\big)
    \\
    \mathbf{p} 
      \;\colon\; 
    \widehat{\mathcal{F}}_\ast 
     & \;\sim\; 
    \widehat{\mathcal{G}}_\ast  
       \;\sim\;
    \widehat{G}_\ast  
  \end{aligned}
\]

For $j_0 \in \widehat{G}_\ast$ any [[base point]], the [[conjugation action]] map

$$
  \begin{array}{c}
     G 
     &\overset{}{\longrightarrow}&
     \widehat{G}_\ast
     \\
     u &\mapsto& u \circ j_0 \circ u^{-1}
  \end{array}
$$

is a [[fiber bundle]] (in fact a [[principal bundle]]) with [[typical fiber]] $G \times G$.

\end{proposition}

\begin{proposition}
  The [[exponential map]]
  $$
    \exp\big(\pi \mathrm{i} (-) \big)
    \;\colon\;
    \widehat{\mathcal{F}}_\ast
    \longrightarrow
    \Big\{
      U \in \mathrm{U}(\mathscr{H})
      \,\Big\vert\,
      U + id \in \mathcal{K}(\mathscr{H})
    \Big\}
  $$
  is a [[homotopy equivalence]].
\end{proposition}



+-- {: .num_theorem #PullbackLawForACube}
###### Theorem
**(Pasting Law for Pullbacks in a Cube)**
\linebreak
Suppose we have a commutative cube in a category:

\begin{tikzcd}[sep = scriptsize]
{U'} && {V'} \\
& {X'} && {Y'} \\
U && V \\
& X && Y
\arrow[from=1-1, to=1-3]
\arrow[from=1-1, to=2-2]
\arrow[from=1-1, to=3-1]
\arrow[from=1-3, to=2-4]
\arrow[from=1-3, to=3-3]
\arrow[crossing over, from=2-2, to=2-4]
\arrow[from=2-4, to=4-4]
\arrow[from=3-1, to=3-3]
\arrow[from=3-1, to=4-2]
\arrow[from=3-3, to=4-4]
\arrow[from=4-2, to=4-4]
\arrow[crossing over, from=2-2, to=4-2]
\end{tikzcd}
\linebreak

* Assume the front and bottom faces are pullback squares. Then the following are equivalent:
  1.  The total rectangle from $U'\to V'$ to $X\to Y$ is a pullback.

  1.  The top and back faces are pullback squares.

  1.  The top face or the back face is a pullback square.

* Assume the top and back faces are pushout squares. Then the following are equivalent:
  1.  The total rectangle from $U'\to V'$ to $X\to Y$ is a pushout.

  1.  The front and bottom faces are pushout squares.

  1.  The front face or the bottom face is a pushout square.
 =--

\begin{proof}
Bla.
\end{proof}

