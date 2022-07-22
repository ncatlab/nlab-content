

[[relation between preorders and (0,1)-categories|here]]



Let 

* $G$ a [[finite group]], with

  * $Orb(G)$ its [[orbit category]]

  * $sPSh\big( Orb(G) \big)_{proj}$ 

    its [[model structure on equivariant simplicial sets]]

    hence the [[projective model structure on simplicial presheaves]] over $Orb(G)$

* $\mathscr{X} \,\in\, \Big(sPSh\big(Orb(G)\big)_{proj}\Big)_{fib}$ an [[equivariant homotopy type]], with

  * $[\mathscr{X}]_0 \,\simeq\, \ast$ (equivariantly connected), hence

  * $[\mathscr{X}]_1 \;\simeq\; \mathbf{B} \pi_1(\mathscr{X})$ (the [[1-truncation]]/[[fundamental groupoid]])


  * $\Pi^G_1 \mathscr{X}
     \;\coloneqq\; Orb(G)_{/[\mathscr{X}]_1}$ (tom Dieck's [[fundamental category]]).

By the assumption that $[\mathscr{X}]_0 \,\simeq\, \ast$ there exists a $G$-fixed point $x \,\colon\, G/G \to \mathscr{X}$. This induces a morphism of sites

\[
  \label{GFixedPointAsFunctorFromGOrbitsToFundamentalCategory}
  \array{
    Orb(G)
    &
    \xrightarrow{\;\;i\;\;}
    &
    \Pi^G_1 \mathscr{X}
    \\
    G/H 
      &\overset{\;\;\;\;}{\mapsto}&
    \big[
      G/H 
        \xrightarrow{\exists !} 
      G/G
        \xrightarrow{x}
      \mathscr{X}
    \big]
  }
\]
and thus the induced [[Kan extension]] of [[simplicial presheaves]]:
\[
  \label{QuillenTransferOfGHomotopyTypesToFundamentalCategory}
    sPSh
    \big(
       \Pi^G_1 \mathscr{X}
    \big)_{proj}
    \underoverset
      {\underset{i^\ast}{\longrightarrow}}
      {\overset{i_!}{\longleftarrow}}
      {\;\;\;\;\; \bot_{\mathrlap{Qu}} \;\;\;\;\;}
    sPSh
    \big(
       Orb(G)
    \big)_{proj}
  \,.
\]

This is a [[Quillen adjunction]] between the corresponding [[projective model structures on simplicial presheaves]] (e.g. since the [[right adjoint]] $i^\ast$, being given by [[precomposition]], evidently preserves all projective [[fibrations]] and even all [[weak equivalences]]).

In fact, since $i$ (eq:GFixedPointAsFunctorFromGOrbitsToFundamentalCategory) is an [[essentially surjective functor]], $i^\ast$ also *detects* fibrations and weak equivalences, in that $f \,\in\, SPSh\big( \Pi_G(X) \big)_{proj}$ is a fibration or weak equivalence precisely of $i^\ast(f)$ is so, respectively.

This means that (eq:QuillenTransferOfGHomotopyTypesToFundamentalCategory) in fact exhibits $sPSh\big(\Pi^G_1 \mathscr{X}\big)_{proj}$ as the right-[[transferred model structure]] of/from $sPSh\big( Orb(G)\big)_{proj}$

\begin{example}
  When $G = 1$ is the [[trivial group]], then $X$ is just a plain topological space. If it is connected, then 
$\Pi_G(X) \,\simeq\, B \pi_1(X)$. In this case (eq:QuillenTransferOfGHomotopyTypesToFundamentalCategory) becomes the $\pi_1(X)$-[[Borel model structure]].
$$
  \pi_1 Act\big(sSet_{Qu}\big)_{proj}
    \underoverset
      {\underset{underlying}{\longrightarrow}}
      {\overset{free}{\longleftarrow}}
      {\;\; \bot_{\mathrlap{Qu}} \;\;}
  sSet_{Qu}
$$
\end{example}

So consider now this diagram of right adjoints:

$$
  \array{
    Func
    \big(
      \Pi_G(X)
      ,\,
      dgcAlg_{\mathbb{Q}}^{\geq 0} 
    \big)
    &&
    sPSh
    \big(
      \Pi_G(X)
    \big)
    \\
    &&
    \big\downarrow
    \\
    Func
    \big(
      Orb(G)
      ,\,
      dgcAlg_{\mathbb{Q}}^{\geq 0} 
    \big)
    &&
    sPSh
    \big(
      Orb(G)
    \big)
  }
$$


