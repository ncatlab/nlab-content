

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a ([[topological field|topological]]) [[ground field]] $\mathbb{K}$ (or more generally a [[topological ring|topological]] [[ground ring]]), its [[projective spaces]] $\mathbb{K}P^n$ canonical form a [[sequence]] of [[subspaces]]

\[
  \label{SequenceOfInclusionsOfFiniteProjectiveSpaces}
  \begin{array}{ccc}
    \mathbb{K}P^n 
      &\xhookrightarrow{\phantom{--}}&
    \mathbb{K}P^{n+1} 
    \\
    [x_1 \colon \cdots \colon x_{n+1}]
    &\mapsto&
    [x_1 \colon \cdots \colon x_{n+1} \colon 0]
    \mathrlap{\,.}
  \end{array}
\]


\begin{definition}
The *infinite projective space* $\mathbb{K}P^\infty$ over $\mathbb{K}$ is the [[union]] of the $\mathbb{K}P^n$, hence the [[colimit]] over the above sequence (eq:SequenceOfInclusionsOfFiniteProjectiveSpaces):

$$
  \mathbb{K}P^\infty
  \;\coloneqq\;
  \underset{\underset{n \to \infty}{\longrightarrow}}{\lim}
  \, 
  \mathbb{K}P^n
  \,.
$$

\end{definition}


## Examples

\begin{example}
 The infinite projective space over the [[real numbers]], $\mathbb{K} \coloneqq \mathbb{R}$, is a model for (the [[homotopy type]] of) the [[classifying space]] of the [[cyclic group of order 2]]:

$$
  \mathbb{R}P^\infty \;\simeq\; B C_2
  \,.
$$
\end{example}


\begin{example}
 The infinite projective space over the [[complex numbers]], $\mathbb{K} \coloneqq \mathbb{C}$, is a model for (the [[homotopy type]] of) the [[classifying space]] of the [[circle group]] [[U(1)]]:

$$
  \mathbb{C}P^\infty \;\simeq\; B \mathrm{U}(1)
  \,.
$$
\end{example}

\begin{example}
The infinite projective space over the [[quaternions]], $\mathbb{K} \coloneqq \mathbb{H}$, is a model for (the [[homotopy type]] of) the [[classifying space]] of the [[quaternion unitary group]] [[Sp(1)]]:

$$
  \mathbb{H}P^\infty \;\simeq\; B \mathrm{Sp}(1)
  \,.
$$
\end{example}


## Related entries

* [[projective line]]

* [[projective plane]]



