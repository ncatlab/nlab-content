> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***

$\infty$

Denote by 

* $\mathscr{H}$ [[generalized the|the]] countably-infinite-dimensional [[separable Hilbert space|separable]] [[Hilbert space]],

* $\mathcal{B}(\mathscr{H})$ the [[norm topology]]-space of [[bounded operators]],

* $\mathcal{K}(\mathscr{H}) \subset \mathcal{B}(\mathscr{H})$ the [[subset]] of [[compact operators]],

* $GL(\mathscr{H}) \subset \mathcal{B}(\mathscr{H})$ the [[general linear group]],

* $\mathrm{U}(\mathscr{H}) \subset GL(\mathscr{H})$ the [[unitary group]] (cf. at *[[U(ℋ)]]*).

\begin{definition}
  The *Fredholm group* of $\mathscr{H}$ is the [[subgroup]] of the [[general linear group]] of those [[elements]] which differ from the [identity operator](identity+morphism#IdentityOperator) by a [[compact operator]]:

\[
  GL^c(\mathscr{H})
  \coloneqq
  \big\{
    \phi \in GL(\mathscr{H})
    \,\big\vert\,
    \phi - id \in \mathcal{K}(\mathscr{H})
  \big\}
  \,.
\]

(cf. [Atiyah & Singer 1969 pp 10](#AtiyahSinger69), [Swanson 1978 p 191](Swanson1978), [Mukherjea 1970 p. 653](#Mukherjea1970))

Analogously, the *unitary Fredholm group* is the [[subgroup]] of [[U(ℋ)]] of those [[elements]] which differ from the [identity operator](identity+morphism#IdentityOperator) by a [[compact operator]]:

\[
  U^c(\mathscr{H})
  \coloneqq
  \big\{
    U \in \mathrm{U}(\mathscr{H})
    \,\big\vert\,
    U - id \in \mathcal{K}(\mathscr{H})
  \big\}
  \,.
\]

(cf. [Atiyah & Singer 1969 pp 10](#AtiyahSinger69), [Andruchow & Larotonda 2010](#AndruchowLarotonda2010), [DSBW 2023 p. 87, 247](#DSBW2023))

\end{definition}


## References

Mentioning of the Fredholm group:

* {#AtiyahSinger69} [[Michael Atiyah]], [[Isadore Singer]], pp 10 of: *Index theory for skew-adjoint Fredholm operators*,  Publications Mathématiques de l’Institut des Hautes Scientifiques **37** 1 (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf)&rbrack;
  > (not calling these groups by any name other than a symbol)

* {#Mukherjea1970} Kalyan K. Mukherjea: *The Homotopy Type of Fredholm Manifolds*, Transactions of the AMS **149** (1970) 653-663 &lbrack;[doi:10.1090/S0002-9947-1970-0259954-4](https://doi.org/10.1090/S0002-9947-1970-0259954-4), [pdf](https://www.ams.org/journals/tran/1970-149-02/S0002-9947-1970-0259954-4/S0002-9947-1970-0259954-4.pdf)&rbrack;

* {#Swanson1978} R. C Swanson: *Fredholm intersection theory and elliptic boundary deformation problems, I*, Journal of Differential Equations **28** 2 (1978) 189-201 \[<a href="https://doi.org/10.1016/0022-0396(78)90066-9">doi:10.1016/0022-0396(78)90066-9</a>\]

Mentioning of the unitary Fredholm group

* {#AtiyahSinger69} [[Michael Atiyah]], [[Isadore Singer]]: *Index theory for skew-adjoint Fredholm operators*,  Publications Mathématiques de l’Institut des Hautes Scientifiques **37** 1 (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf)&rbrack;

* {#AndruchowLarotonda2010} Esteban Andruchow, Gabriel Larotonda: *The rectifiable distance in the unitary Fredholm group*, Studia Mathematica Volume **196** 2 (2010) 151-178 &lbrack;[arXiv:0812.4475](https://arxiv.org/abs/0812.4475), [eudml:285458](https://eudml.org/doc/285458)&rbrack;


* {#DSBW2023} Nora Doll, [[Hermann Schulz-Baldes]], [[Nils Waterstraat]], Sections 3.7 and 8.1 in: *Spectral Flow --- A Functional Analytic and Index-Theoretic Approach*, Studies in Mathematics **94**, De Gruyter (2023) &lbrack;[doi:10.1515/9783111172477](https://doi.org/10.1515/9783111172477), [hdl:20.500.12657/63798](https://library.oapen.org/handle/20.500.12657/63798), ch8:[[DSBW23-HomotopyFredholmOps.pdf:file]]&rbrack;


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

