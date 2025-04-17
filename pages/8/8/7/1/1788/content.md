
Let $G$ be a [[finite group]].

Denote by $Irr(G) \simeq \big\{ [\rho_i] \big\}_{i \in I}$ the [[set]] of [[isomorphism classes]] of its [[irreducible representations]].

For $(n_i)_{i \in I}$ an $I$-partition, $n = \sum_i n_i$, write

$$
  Sym_{(n)}
  \;\coloneqq\;
  \prod_i Sym_{n_i}
  \;\;
  \subset
  \;\;
  Sym_n
$$

There is then an evident representation of $G \wr Sym_{(n)}$ on $  
  \displaystyle{\underset{i \in I}{\bigotimes}}
  \rho_i^{\otimes_{n_i}} 
$

Moreover for $R$ an irrep of $Sym_n$, we may regarded as a rep of $G \wr Sym_n \to Sym_n$.

\begin{theorem}
  Up to isomorphism, the irreducible representations of the [[wreath product group]] $G \wr Sym_n$ are exactly the [[induced representations]] along $G \wr Sym_{(n)} \hookrightarrow G \wr Sym_n$ of the reps of the form
$$
  \Big(
    \displaystyle{\underset{i \in I}{\bigotimes}}
    \rho_i^{\otimes_{n_i}} 
  \Big)
  \otimes
  R
$$
for $(n)$ an $I$-partition as above and $R$ an irrep of $Sym_n$
\end{theorem}
