
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

$$
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
$$
and thus the induced [[Kan extension]] of [[simplicial presheaves]]:
$$
    sPSh
    \big(
       \Pi^G_1 \mathscr{X}
    \big)
    \underoverset
      {\underset{i_\ast}{\longleftarrow}}
      {\overset{i^\ast}{\longrightarrow}}
      {\;\; \bot \;\;}
    sPSh
    \big(
       Orb(G)
    \big)
$$

\begin{proposition}
  The [left](transferred+model+structure#LeftTransfer)-[[transferred model structure]] along
  $$
    sPSh
    \big(
       \Pi^G_1 \mathscr{X}
    \big)
    \underoverset
      {\underset{i_\ast}{\longleftarrow}}
      {\overset{i^\ast}{\longrightarrow}}
      {\;\; \bot \;\;}
    sPSh
    \big(
       Orb(G)
    \big)_{proj}
  $$
  exists.
\end{proposition}
\begin{proof}
  Since both categories are [[cofibrantly generated model category|cofibrantly generated]] and the [[model structure on simplicial presheaves]] is in addition [[cofibrantly generated model category|cofibrantly generated]], [this Prop.](transferred+model+structure#RecognitionOfLeftTransferUnderCofibrantlyGeneration) reduces us to checking that co-anodyne maps are weak equivalences: 
$$
  \begin{array}{ll}
    (i^\ast)^{-1}(Cof)
    \;&solb;\;
    f
    \\
    \;\Rightarrow\;
    i_!(Cof) \;&solb;\; f    
    \\
    \;\Leftrightarrow\;
    Cof \;&solb;\; i^\ast(f)    
    \\
    \;\Rightarrow\;
    i^\ast(f) \;\in\; W
    \\
    \;\Leftrightarrow\;
    f \;\in\; (i^\ast)^{-1}(W)
  \end{array}
$$
Here the first step is by Lemma \ref{LeftCaseChangeOfCofibrationsAreTransferredCofibrations}.
\end{proof}


\begin{lemma}
\label{LeftPushPullIsProductWithFundamentalGroup}
$$
  i^\ast \circ i_! (-)
  \;\simeq\;
  \pi_1(\mathscr{X}) \times (-)
  \,.
$$
\end{lemma}
\begin{proof}
On the level of presheaves on 1-sites:
$$
  i^\ast i_! (G/H)
  \;\simeq\;
  i^\ast
  \big[
    G/H \to G/G \xrightarrow{x} \mathscr{X}
  \big]
  \;\simeq\;
  \big(
    G/K
    \mapsto
    Hom(G/K, G/H)
    \times
    \pi^K_1(\mathscr{X})
  \big)
$$
Alternatively, via slicing of 2-sites:
$$
  \array{
    \pi_1(\mathscr{X})
      \times
    \mathscr{A}
    &\longrightarrow&
    \mathscr{A}
    \\
    \big\downarrow
    &(pb)&
    \big\downarrow
    \\
    \pi_1(\mathscr{X})
    &\longrightarrow&
    \ast
    \\ 
    \big\downarrow
    &(pb)&
    \big\downarrow
    \\
    \ast
    &\longrightarrow&
    [\mathscr{X}]_1   
  }
$$
\end{proof}

\begin{lemma}
  \label{LeftCaseChangeOfCofibrationsAreTransferredCofibrations}
  $$
    i_!(Cof)
    \;\subset\;
    (i^\ast)^{-1}(Cof)
  $$
\end{lemma}
\begin{proof}
  By Lemma \ref{LeftPushPullIsProductWithFundamentalGroup} 
  we have
  $$
    i^\ast \circ i_! (Cof)
    \;=\;
    \pi_1(\mathscr{X}) \times Cof
    \,.
  $$
  Hence ... hm, so it only works if $\pi_1(\mathscr{X})$ is cofibrant, which is rarely the case...
\end{proof}




