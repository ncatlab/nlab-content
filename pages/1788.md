
\begin{proposition}
  For $X \,\in\, TopSp$ a [[topological space]] 
  and $G \,\in\, Grp(TopSp)$ a [[topological group]], 
  if there is a [[concordance]] between a [[pair]] of 
  $G$-[[principal bundles]] over $X$, 
\begin{tikzcd}
  P_0 
  \ar[r]
  \ar[d, "{p_0}"]
  \ar[dr,phantom,"\mbox{\tiny(pb)}"]
  &
  P
  \ar[d, "{p}"]
  \ar[dr,phantom,"\mbox{\tiny(pb)}"]
  &
  P_1
  \ar[l]
  \ar[d, "{p_1}"]
  \\
  X \times \{0\}
  \ar[r, hook]
  &
  X \times [0,1]
  &
  X \times \{1\}
  \ar[l, hook']
\end{tikzcd}
then there is already an [[isomorphism]] between them
\begin{tikzcd}
  P_0
  \ar[dr, "{p_0}"{below}]
  \ar[rr, "{\sim}"]
  &&
  P_1
  \ar[dl, "{p_1}"]
  \\
  & 
  X
\end{tikzcd}
\end{proposition}
\begin{proof}
Recall that isomorphisms between principal bundles $P$ and $P'$ over $X$ are equivalently [[global sections]] of the fiber bundle $(P \times_X P')/G$. In particular, for every $P$ the [[identity morphism]] on it corresponds to a canonical section of $(P \times_X P)/G$. 

In the given situation, this means that we have a canonical local section $\sigma_0$ making the following solid diagram [[commuting square|commute]], exhibiting that the restriction of the bundle $P_0 \times [0,1]$ to $\{0\} \subset [0,1]$ is isomorphic to $P_0$, by construction

\begin{tikzcd}
  X \times \{0\}
  \ar[rr, "\sigma_0"]
  \ar[dd, "\in \mathrm{Cof} \cap \mathrm{W}"]
  &&
  \big(
    P \underset{X \times [0,1]}{\times} (P_0 \times [0,1])
  \big)/G
  \ar[dd, "\in \mathrm{Fib}"]
  \\
  \\
  X \times [0,1]
  \ar[rr,-, shift right=1pt]
  \ar[rr,-, shift left=1pt]
  \ar[uurr, dashed, "\exists"]
  &&
  X \times [0,1]
\end{tikzcd}

Here, with respect to the [[Quillen-Serre model structure on topological spaces]]:

1. the left vertical [[continuous function|map]] is manifestly an [[relative cell complex]] inclusion and a [[weak homotopy equivalence]], hence an [[acyclic cofibration]],

1. the right vertical [[map]] is a [[Serre fibration]], as a special case of the the fact that all [[locally trivial bundle|locally trivial]] [[fiber bundles]] are [[Serre fibrations]] (by [this Prop.](fiber+bundle#RelationToFibrations)).

Therefore a dashed [[lifting]] exists, as shown. But by the resulting [[commuting diagram|commutativity]] of the bottom right triangle, this is a [[global section]] which hence exhibits an [[isomorphism]] of principal bundles (over $X \times [0,1]$) of this form:

$$
  P
  \;\;
  \simeq_X
  \;\;
  P_0 \times [0,1]
  \,.
$$

The [[restriction]] of this isomorphism to $\{1\} \subset [0,1]$ is hence an isomorphism $P_1 \,\simeq_X\, P_0$, as claimed.
\end{proof}
