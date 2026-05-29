> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\linebreak


$\mathbb{R}$

\begin{proposition}
Consider:

* $X, \mathcal{A}$ be a [[pair]] of [[connected topological space|connected]] [[nilpotent topological space]] [[CW-complexes]] of [[rational cohomology|rational]] [[finite type]]
 
  with $X$ a [[finite CW complex]] or $Y$ having a finite [[Postnikov tower]],

* $\phi \colon X \to \mathcal{A}$ a [[continuous map]]

Then [[dg-Lie algebra]] model for the [[rational homotopy type]] of the [[mapping space]] $Map\big(X; \mathcal{A}\big)$ in the [[connected component]] of $\phi$ is given by the twisted [[tensor product]]

$$
  \big(
    \Omega^\bullet_{PL}(X) 
      \textstyle{
        \otimes_{\mathbb{Q}}
      }
    \mathfrak{l} \mathcal{A}
  \big)^{\mathfrak{l}\phi}
  \langle 0 \rangle
$$ 

where :

* $\Omega^\bullet_{PL}(-)$ denotes the [[PL de Rham complex|PL de Rham]] [[dgc-algebra]],

* $\mathfrak{l}(-)$ denotes the [[dg-Lie algebra]] model.

* $\xi_\phi \in MC\big( \Omega^\bullet_{PL}(X) \otimes \mathfrak{l}\mathcal{A}\big)$ is the [[Maurer-Cartan element]] corresponding to the [[pullback of differential forms]]

  $$
    \phi^\ast 
      \,\colon\,
    CE(\mathfrak{l}\mathcal{A})
      \longrightarrow
    \Omega^\bullet_{PL}(X) 
    \mathrlap{\,,}
  $$

* $(-)^{\xi_\phi}$ means that the [[differential]] of the tensor [[dg-Lie algebra]] is twisted as

  $$
    d^{\mathfrak{l}\phi}(-)
    \coloneqq
    \mathrm{d}(-)
    +
    \big[\xi_\phi, -\big]
    \mathrlap{\,,}
  $$

* $(-)\langle-\rangle$ denotes the [[connective cover]] (discarding negative degrees and restricting to [[cycles]] in degree=0).

\end{proposition}

(cf. [Lazarev 2013 Thm. 8.1](#Lazarev2013))

\linebreak

***


$$
  \frac{\Gamma \vdash t:\Box A}{\Gamma \vdash \mathsf{extract}(t):A}
  \qquad
  \frac{\Gamma \vdash t : \Box A \qquad x : A \vdash u : B}{\Gamma \vdash \mathsf{let\ box}\ x = t\ \mathsf{in}\ u : B}
$$

---


$\esh$



$$
  J 
    \;=\;
    \sum_i f_i \theta_i 
      + 
    \sum_j g_j d \theta_j 
    f_i, g_j \in C^\infty(X)
  \,.
$$


\begin{xymatrix}
Q B \ar[d] \ar[r] & Q A \sqcup Q B \ar[d] \ar[r] & A \sqcup Q B \ar[d]\cr
  B        \ar[r] & Q A \sqcup   B        \ar[r] & A \sqcup   B       \cr
\end{xymatrix}