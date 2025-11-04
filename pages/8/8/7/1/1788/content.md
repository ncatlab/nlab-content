> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***


[[CechGroupoid-Illustration-251101b.png:file]]

[[EquivariantChechGroupoidIllustration-251101.png:file]]

[[SpindleGluingMorphismIllustration-251101.png:file]]

[[DuggerCofibrantSpindleGroupoid-251101.png:file]]


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

* Assume the front face is a pullback. Then the following are equivalent:
  1.  The total rectangle from $U'\to V'$ to $X\to Y$ is a pullback.

  1.  Each face is a pullback.

  1.  At least one of the other faces apart from the front face is a pullback.

* Assume the back face is a pushout. Then the following are equivalent:
  1.  The total rectangle from $U'\to V'$ to $X\to Y$ is a pushout.

  1.  Each face is a pushout.

  1.  At least one of the other faces apart from the back face is a pullback.
 =--

