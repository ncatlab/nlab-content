> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak


***

{#Discussion} Consider:

* $\mathbf{H}$ an $\infty$-topos,

* $G \in Grp(\mathbf{H})$ an $\infty$-group,

* $G \curvearrowright P \in G Act(\mathbf{H})$ an $\infty$-action,

* $X \coloneqq P \sslash G$ its [[homotopy quotient]].

Note that the quotient coprojection is a $G$-principal $\infty$-bundle:

\begin{tikzcd}
  G 
  \ar[r]
  &
  P
  \ar[d]
  \\
  {}
  &
  X
\end{tikzcd}

and every $G$-principal $\infty$-bundle is of this form (cf. [[schreiber:EPB]]v2 Prop. 1.2.1, [p. 15](https://ncatlab.org/schreiber/files/EquivariantInfinityBundles_251013.pdf#page=15)).



Further consider:

* $\mathcal{A} \in \mathbf{H}$ any object,

  to be thought of as a moduli stack for some kind of structure, for instance for differential forms or differential cohomology,

* $G \curvearrowright \mathcal{A} \coloneqq G \curvearrowright \ast \times \mathcal{A} \in G Act(\mathbf{H})$ its incarnation as a trivial $G$-action,

* $G \curvearrowright [P, \mathcal{A}] \coloneqq  \big[G \curvearrowright P,\, G \curvearrowright \mathcal{A} \big] \in G Act(\mathbf{H})$ the internal hom of $G$-actions, being the mapping space $[P,\mathcal{A}]$ equipped with the induced conjugation action,

* $[P, \mathcal{G}]^G$ its $G$-fixed locus

(cf. [[schreiber:DCCT]]v1, Def. 3.6.232; [p. 339](https://arxiv.org/pdf/1310.7930v1#page=339);  [[schreiber:DCCT]]v2 Def. 5.1.278, [p. 443](https://ncatlab.org/schreiber/files/dcct170811.pdf#page=443)).

**Claim:** We have a natural equivalence:

$$
  [P, \mathcal{A}]^G
  \;\simeq\;
  [X, \mathcal{A}]
  \,.
$$

In words: "$G$-Invariant $\mathcal{A}$-cocycles on the total space $P$ of a $G$-principle bundle are equivalently plain $\mathcal{A}$-cocyles on the base space $X$."

\begin{proof}

Recall the equivalence ([[schreiber:EPB]]v2 Prop. 1.2.1, [p. 15](https://ncatlab.org/schreiber/files/EquivariantInfinityBundles_251013.pdf#page=15)):

\begin{tikzcd}
  G \mathrm{Act}(\mathbf{H})
  \ar[r, "{ \sim }"]
  &
  \mathbf{H}_{/\mathbf{B}G}
  \\[-40pt]
  G \curvearrowright X
  \ar[r, |->, shorten=4pt]
  &
  \big(
    p_{X} \colon X /\!\!/ G \to \mathbf{B}G
  \big)
  \mathrlap{\,,}
\end{tikzcd}

under which forming fixed loci is right base change to the point: $(-)^G \leftrightarrow \prod_{\mathbf{B}G}$.

Hence in our case:
$$
  [P,\mathcal{A}]^G
  \;\;\leftrightarrow\;\;
  \big[P \sslash G, \mathcal{A}\sslash G\big]_{\mathbf{B}G}
  \,\coloneqq\,
  \prod_{\mathbf{B}G}
  \big[
    p_P, p_{\mathcal{A}}
  \big]
  \mathrlap{\,.}
$$


Now observe that have have a pullback square of this form ([[schreiber:EPB]]v2 Lem. 4.2.69 with Def. 4.2.66, [p. 121](https://ncatlab.org/schreiber/files/EquivariantInfinityBundles_251013.pdf#page=121)):

\begin{tikzcd}
  \big[
    P /\!\!/ G
    ,\,
   \mathcal{A} \times \mathbf{B}G
  \big]_{ \mathbf{B}G }
  \ar[r]
  \ar[d]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  \big[
    P /\!\!/ G
    ,\,
    \mathcal{A}\times \mathbf{B}G
  \big]
  \ar[
    d,
    "{ (\mathrm{pr}_2)_\ast }"
  ]
  \\
  \ast
  \ar[
    r,
    "{ \vdash \, p_{{}_P} }"
  ]
  &
  \big[
    P /\!\!/ G
    ,\,
   \mathbf{B}G
  \big]
  \mathrlap{\,,}
\end{tikzcd}

where we used in the top row that the $G$-action on $\mathcal{A}$ being trivial (by assumption) means equivalently that:

\begin{tikzcd}
  \mathcal{A} /\!\!/ G
  \ar[rr, "{ \sim }"]
  \ar[dr, "{ p_{\mathcal{A}} }"{swap}]
  &[-40pt]&[-40pt]
  \mathcal{A} \times \mathbf{B}G
  \ar[dl, "{ \mathrm{pr}_2 }"]
  \\[-10pt]
  & 
  \mathbf{B}G
  \mathrlap{\,.}
\end{tikzcd}

But the internal hom $\big[-,-\big]$ preserves limits in its second argument, whence

$$
  \big[
    P \sslash G 
    ,\,
    \mathcal{A} \times \mathbf{B}G
  \big]
  \,\simeq\,
  \big[
    P \sslash G 
    ,\,
    \mathcal{A}
  \big]
    \times
  \big[
    P \sslash G 
    ,\,
    \mathbf{B}G
  \big]  
  \,,
$$

and since pullbacks commute with products, the above pullback square is seen to be equivalent to:


\begin{tikzcd}
  \big[
    P /\!\!/ G
    ,\,
   \mathcal{A}
  \big]
  \times
  \ast
  \ar[r]
  \ar[
    d,
    "{ p \,\times\, \mathrm{id} }"
  ]
  \ar[dr, phantom, "{ \lrcorner }"{pos=.1}]
  &
  \big[
    P /\!\!/ G
    ,\,
   \mathcal{A}
  \big]
  \times
  \big[
    P /\!\!/ G
    ,\,
   \mathbf{B}G
  \big]
  \ar[
    d,
    "{ p \,\times\, \mathrm{id} }"
  ]
  \\
  \ast
  \times \ast
  \ar[
    r,
    "{ \mathrm{id} \,\times\, \vdash \, p_{{}_P} }"
  ]
  &
  \ast 
  \times
  \big[
    P /\!\!/ G
    ,\,
   \mathbf{B}G
  \big]
  \mathrlap{\,.}
\end{tikzcd}

Finally, since $P \sslash G \,\simeq\, X$, this proves the claim.
\end{proof}
