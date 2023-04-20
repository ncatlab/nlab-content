
Hence it remains to see the claim about the colimit. For that it is sufficient to observe that whenever have a [[commuting diagram]] in [[simplex category|$\Delta$]] of the form

\begin{tikzcd}[sep=20pt]
    & 
    {[r]}
    \ar[dl,->>, "{p}"{swap}]
    \ar[dr,->>, "{p'}"]
    \\
    {[s]} 
    \ar[dr,->>, "{q}"{swap}]
    &
    & 
    {[s']}
    \ar[dl,->>, "{q'}"]
    \\
    &
    {[t]}
\end{tikzcd}

we may equivalently factor it as a [[zig-zag]] of diagrams 

\begin{tikzcd}[sep=20pt]
    & 
    {[r]}
    \ar[dl,->>, "{p}"{swap}]
    \ar[dr,->>, "{p'}"]
    \ar[d, ->>]
    \\
    {[s]} 
    \ar[dr,->>, "{q}"{swap}]
    &
    {[t]}
    \ar[d, equals]
    \ar[from=r, ->>]
    \ar[from=l, ->>]
    & 
    {[s']}
    \ar[dl,->>, "{q'}"]
    \\
    &
    {[t]}
\end{tikzcd}

Now the right half of this commuting diagram

\begin{tikzcd}[sep=20pt]
    & 
    {[r]}
    \ar[dl,->>, "{ p  }"{swap}]
    \ar[dr,->>, "{ q' \,\circ\, p' }"]
    \\
    {[s]} 
    \ar[dr,->>, "{q}"{swap}]
    \ar[rr, ->>, "{q}"]
    &
    & 
    {[t]}
    \ar[dl,->>, "{\mathrm{id}}"]
    \\
    &
    {[t]}
\end{tikzcd}


This [[zig-zag]] of diagrams means that in the colimit the left pair of maps will be identified with the right pair of maps.


\begin{proposition}
  Let $\mathcal{A}$ be an [[additive category]] in which all [[retractions]] exhibit [[direct sums]] (such as in an [[abelian category]]).

Then for any [[simplicial object]] $X_\bullet \in s\mathcal{A} \coloneqq \mathcal{A}^{\Delta^{op}}$ and all $n \in \mathbb{N}$, the comparison morphism from the $n$th latching object of $X_\bullet$ is a ([[split monomorphism|split]]) [[monomorphism]]:

$$
  L_n X \xhookrightarrow{\phantom{---}} X_n
  \,.
$$
\end{proposition}
\begin{proof}
  Under the given assumption on $\mathcal{A}$ the [[Dold-Kan correspondence]] applies (see [there](Dold-Kan+correspondence#StatementAdditiveACase)) to [[simplicial objects]] in $\mathcal{A}$ and says that, up to [[isomorphism]], $X_\bullet$ is of the form $X_\bullet \simeq \Gamma(V_\bullet)$ for some [[connective chain complex]] $V_\bullet$ (in fact $V_\bullet \simeq N X_\bullet$ is the [[normalized chain complex]] of $X_\bullet$, but we don't even need this), in that each $X_r$ is the [[direct sum]] of one copy of $V_s$ for each [[surjection]] $[r] \twoheadrightarrow [s]$ in [[simplex category|$\Delta$]] (by [this Prop.](Dold-Kan+correspondence#ExplicitFormOfGamma)):

$$
  X_r 
  \;\simeq\;
  \underset
    {[r] \twoheadrightarrow [s]}
    {\bigoplus}
  V_s
  \;\simeq\;
  \left(
  \underset
    {
      {[r] \overset{p}{\twoheadrightarrow} [s]}
      \atop
      p \neq id_{[r]}
    }
    {\bigoplus}
  V_s
  \right)
  \,\oplus\,
  V_r
  \,.
$$
(On the right we have split off the summand corresponding to the [[identity morphisms]], just for emphasis, since this is what matters in a moment).

Moreover (still by [this Prop.](Dold-Kan+correspondence#ExplicitFormOfGamma)), under this identification the [[degeneracy maps]] $X_{[r'] \overset{p}{\twoheadrightarrow} [r]}$ of $X_\bullet$ are simply given on these [[direct sum|direct summands]] by precomposition of their labels with $p$.

$$
  \array{
    X_{r} 
    &
    \overset{X_{[r'] \overset{p}{\twoheadrightarrow} [r]} }{\longrightarrow}
    &
    X_{r'}
    \\
    \big(
      [r] \overset{\sigma}{\twoheadrightarrow} [s]
      ,\,
      v \in V_s
    \big)
    &\mapsto&
    \big(
      [r'] \overset{\sigma \circ p}{\twoheadrightarrow} [s]
      ,\,
      v \in V_s
    \big)
  }
$$

This implies that the colimit defining $L_r X$ consists of [[equivalence classes]] of triples of the form 
$
\Big(  
    [r] 
      \overset{p}{\twoheadrightarrow} 
    [r'] 
      \overset{q}{\twoheadrightarrow}
    [s]
   ,\,
  v \in V_s 
  \Big)
$
for non-identity $p$,
under the [[equivalence relation]] which identifies $(p,q,v)$ with $(p'q',v')$ iff $p \circ q \,=\, p' \circ q'$. But this evidently means that the equivalence classes are simply labeled by pairs $\big([r] {\twoheadrightrightarrw} [s] ,\,  v \in V_s\big)$ where the surjection is non-identity. 

Hence the colimit is

$$
  L_r X
  \;\coloneqq\;
  \underset{
    \underset
      {
        { p \colon [r] \twoheadrightarrow [s] }
        \atop
        { p \neq id }
      }
      {\longrightarrow}
  }{\lim}
  X_s
  \;\simeq\;
  \underset{
      {
        { p \colon [r] \twoheadrightarrow [s] }
        \atop
        { p \neq id }
      }
  }{\bigoplus}
  V_s
$$

and the comparison map $L_r X \to X_r$ is the canonical inclusion of all the non-identity [[direct summands]]:

$$
  L_r X 
  \xhookrightarrow{\phantom{--}}
  L_r X \,\oplus\, V_r
  \;\simeq\;
  X_\bullet
  \,.  
$$
\end{proof}