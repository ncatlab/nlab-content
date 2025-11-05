> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

***

| this space of such Fredholm operators | classifies |
|---|---|
| complex  |  $K \mathrm{U}^0$ |
| complex self-adjoint | $K \mathrm{U}^1$ |
| real  |  $K \mathrm{O}^0$ |
| real self-adjoint | $K \mathrm{O}^1$ |
| real anti-self-adjoint | $K\mathrm{O}^7$ |
| quaternionic  |  $K \mathrm{O}^4$ |
| quaternionic self-adjoint | $K \mathrm{O}^5$ |
| quaternionic anti-self-adjoint | $K \mathrm{O}^{3}$ |
| complex anti-linear self-adjoint  |  $K \mathrm{O}^2$ |
| complex anti-linear anti-self-adjoint | $K \mathrm{O}^6$ |

or conversely

| this K-theory | is classified by such Fredholm operators |
|---|---|
| $K \mathrm{U}^0$ | complex  |  
| $K \mathrm{U}^1$ | complex self-adjoint | 
| $K \mathrm{O}^0$ | real  |  
| $K \mathrm{O}^1$ | real self-adjoint  |
| $K \mathrm{O}^2$ | complex anti-linear self-adjoint |
| $K \mathrm{O}^3$ | quaternionic anti-self-adjoint |
| $K \mathrm{O}^4$ | quaternionic |
| $K \mathrm{O}^5$ | quaternionic self-adjoint |
| $K \mathrm{O}^6$ | complex anti-linear anti-self-adjoint |
| $K \mathrm{O}^7$ | real anti-self-adjoint |


except that in the cases of $K \mathrm{U}^n$ with $n = 1 mod 2$ and  $K\mathrm{O}^n$ with $n = 1 mod 4$ the given space of Fredholm operators is actually the disjoint union of $K \mathrm{U}^n$/$K\mathrm{O}^n$ with two contractible components.


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

