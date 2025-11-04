> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

\begin{proposition}
  The space of [[self-adjoint operator|self-adjoint]] [[Fredholm operators]] 
  $$
    Fred^{sa}
    \subset
    \Big\{
      F \in Fred 
      \;\Big\vert\;
      F^\dagger = F
    \Big\}
  $$
  has three [[connected components]]
  $$
    Fred^{sa}
    \simeq
    Fred_+^{sa}
    \sqcup
    Fred_-^{sa}
    \sqcup
    Fred_\ast^{sa}
  $$
  corresponding to the operators $F$ whose [[essential spectrum]] (which is [[real number|real]], by self-adjointness) is, respectively:

  1. $Fred_+^{sa}$: purely [[positive number|positive]]

  1. $Fred_-^{sa}$: purely [[negative number|negative]]

  1. $Fred_{\ast}^{sa}$: both, hence [[inhabited set|nonempty]] both above and below [[zero]].

Moreover, 

1. the first two components are [[contractible topological space|contractible]]

   $$
     Fred^{sa}_{\pm} \simeq \ast
     \,,
   $$

1. the last component is [[homotopy equivalence|homotoppy equivalent]] to the [[stable unitary group]], hence the [[classifying space]] for [[topological K-theory]] in odd degree:

   $$
     Fred^{sa}_{\ast} \simeq U \simeq KU_1
     \,.
   $$

\end{proposition}
Up to some straightforward reidentifications (for instance one may equivalently use *skew* self-adjoint operators whose spectrum is then purely [[imaginery number|imaginary]]) this is the statement of [Atiyah & Singer 1969 Thm. B](#AtiyahSinger1969) and [Karoubi 1970 Lem 1.4 & Prop. 1.5](#Karoubi1970).

## References

* {#AtiyahSinger1969} [[Michael F. Atiyah]], [[Isadore M. Singer]]: *Index theory for skew-adjoint Fredholm operators*, Publications Mathématiques de l'IHÉS **37** (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [numdam:PMIHES_1969__37__5_0](https://www.numdam.org/item/PMIHES_1969__37__5_0), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/askew.pdf)&rbrack;

* {#Karoubi1970} [[Max Karoubi]]: *Espaces Classifiants en K-Théorie*, Trans. Amer. Math. Soc. **147** (1970) 75-115 &lbrack;[doi:10.2307/1995218](https://doi.org/10.2307/1995218), [jstor:1995218](https://www.jstor.org/stable/1995218)&rbrack;


***


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

