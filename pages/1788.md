

For 

$$
  \mathcal{X}
  \;\colon\;
  \mathcal{C}^{op}
  \xrightarrow{\;}
  Grpd_\infty
$$

an $\infty$-presheaf and

$$
  \overset{
    c \in \mathcal{C}
  }{\int}
  \mathcal{X}(c)
  \;\;
  \in
  \;\;
  Grpd_\infty
$$
its $\infty$-Grothendieck construction, it ought to be the case that its projection onto the $\infty$-Grothendieck construction of its $n$-truncation is the $\infty$-Grothendieck construction on the system 

$$
  \big(
    c,
    \,
    x \in \mathcal{X}(c)
  \big)
  \;\mapsto\;
  cn_n
  \big(
    \mathcal{X}(c), x
  \big)
$$

of $n$-connected covers:

\begin{tikzcd}
    \overset
      { \mathclap{ c \in \mathcal{C} } }
      { \scalebox{1.6}{$\int$} }    
    \mathcal{X}(c)
    \ar[rr]
    \ar[d, "P_n", start anchor={[yshift=2pt]}, end anchor={[yshift=-10pt]}]
    \ar[drr, phantom, "{\mbox{\tiny(pb)}}"]
    &&
    \widehat{\mathrm{Grpd}_{\infty}}
    \ar[d]
    \\
    \overset
      { \mathclap{ c \in \mathcal{C} } }
      { \scalebox{1.6}{$\int$} }
    \tau_n \mathcal{X}(c)
    \ar[
      rr,
      "{
        (c,x)
        \,\mapsto\,
        \mathrm{cn}_n
        \big(
          \mathcal{X}(c), x
        \big)
      }"{swap}
    ]
    &&
    \mathrm{Grpd}_\infty
\end{tikzcd}


Is this discussed anywhere?


\linebreak

Here some more elaboration:

For $n \in \mathbb{N} \sqcup \{\infty\}$, we write

\begin{tikzcd}
    \widehat{\mathrm{Grpd}_n}
    \mathrlap{
      =: \mathrm{Grpd}_n^{\ast/}
    }
    \ar[d]
    &
    \\
    \mathrm{Grpd}_n
\end{tikzcd}

for the universal fibration of $n$-groupoids.


Via the naturality squares

\begin{tikzcd}
    \widehat{\mathrm{Grpd}_\infty}
    \ar[d]
    \ar[r, "\tau_n"]
    &
    \widehat{\mathrm{Grpd}_n}
    \ar[d]
    \\
    \mathrm{Grpd}_\infty
    \ar[r, "\tau_n"]
    &
    \mathrm{Grpd}_n
\end{tikzcd}

we may canonically regard any pointed $\infty$-groupoid 
$(\mathcal{X}, x) \,\in\, \widehat{\mathrm{Grpd}_\infty}$
as an element in the homotopy pullback of the $n$th universal fibration along
$\tau_n$.

The resulting further homotopy pullback along its classifying map should be the $n$-connected cover 
$\mathrm{cn}_n(\mathcal{X},s)$
of 
$(\mathcal{X},x)$:

\begin{tikzcd}
    \mathrm{cn}_n(\mathcal{X},x)
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    &
    \widehat{\mathrm{Grpd}_\infty}
    \ar[d]
    \\
    \ast
    \ar[
      r,
      "{
        \vdash (\mathcal{X},x)
      }"{swap}
    ]
    &
    {}
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    &
    \widehat{\mathrm{Grpd}_n}
    \ar[d]
    \\
    &
    \mathrm{Grpd}_\infty
    \ar[r, "\tau_n"]
    &
    \mathrm{Grpd}_n
\end{tikzcd}


Then consider the following tower of $\infty$-Grothendieck constructions on the $n$-truncations of an $\infty$-presheaf $\mathcal{X}(-)$, here shown in the first few stages:

\begin{tikzcd}
    \mathrm{cn}_1
    \big(
      \mathcal{X}(c),
      x
    \big)
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    &[+5pt]
    \overset
      { \mathclap{ c \in \mathcal{C} } }
      { \scalebox{1.6}{$\int$} }
    \mathcal{X}(c)
    \ar[r]
    \ar[d, "P_1", start anchor={[yshift=2pt]}, end anchor={[yshift=-10pt]}]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    &
    \widehat{\mathrm{Grpd}_\infty}
    \ar[d]
    \\
    \ast
    \ar[
      r, 
      "{
        \vdash 
        \big(
          \mathcal{X}(c),x
        \big)
      }"{swap}
    ]
    &
    \overset
      { \mathclap{ c \in \mathcal{C} } }
      { \scalebox{1.6}{$\int$} }
    \tau_1 \mathcal{X}(c)
    \ar[d, start anchor={[yshift=+2pt]}, end anchor={[yshift=-12pt]}]
    \ar[r]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    &
    {}
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    &
    \widehat{\mathrm{Grpd}_1}
    \ar[d]
    \\
    &
    \overset
      { \mathclap{ c \in \mathcal{C} } }
      { \scalebox{1.6}{$\int$} }
      \tau_0 \mathcal{X}(c)
    \ar[d, start anchor={[yshift=2pt]}, end anchor={[yshift=-6pt]}]
    \ar[r]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    & 
    {}
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    & 
    {}
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny(pb)}"]
    & 
    \widehat{\mathrm{Set}}
    \ar[d]
    \\
    &
    \mathclap{\phantom{\scalebox{1.6}{$\int$}}}
    \mathcal{C}^{\mathrm{op}}
    \ar[
      r,
      "{
        \mathcal{X}  
      }"{swap}
    ]
    &
    \mathrm{Grpd}_\infty
    \ar[
      r, 
      "{\tau_1}"{swap}
    ]
    &
    \mathrm{Grpd}_1
    \ar[
      r, 
      "{\tau_0}"{swap}
    ]
    &
    \mathrm{Set}
\end{tikzcd}

By the pasting law, and the previous diagram, the top left square ought to be as shown, exhibiting the homotopy fibers of $P_1$ as the 1-connected covers as claimed. The same argument would apply to any $P_n$.



