
# A heading about [[sets]]

discussed [[étale space#RelationToSheaves|at étale space]] [[étale space#RelationToSheaves]], etc.

* Foo bar

  > A point of terminology: - I have consistently used the word “categorial” where the literature uniformly employs “categorical”. The reason is that while both can serve as adjectival forms of the noun “category”, the second of them already has a different and long established usage in the domain of logic, one that derives from its ordinary-language meaning of “absolute”. Logicians have known since the work of Gödel that set theory has no categorical axiomatisation. One function of this book will be to explain to them why it does have a categorial one.


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
    PSh
    \Big(
      \Pi_G(X)
      ,\,
      \big(dgcAlg_{\mathbb{Q}}^{\geq 0} \big)^{op}
    \Big)_{traScu}
    &
    \overset
      {\;\;\; exp \;\;\;}
      {\longrightarrow}
    &
    PSh
    \big(
      \Pi_G(X)
      \,,
      sSet
    \big)_{proj}
    \\
    \big\downarrow
    &&
    \big\downarrow
    \mathrlap{
      {}^{i^\ast}
    }
    \\
    PSh
    \Big(
      Orb(G)
      ,\,
      \big(dgcAlg_{\mathbb{Q}}^{\geq 0} \big)^{op}
    \Big)_{Scu}
    &
    \overset
      {\;\;\; exp \;\;\;}
      {\longrightarrow}
    &
    PSh
    \big(
      Orb(G)
      \,,
      sSet
    \big)_{proj}
  }
  \,,
$$

where on the bottom we have the [[Quillen adjunction between equivariant simplicial sets and equivariant connective dgc-algebras]].

Notice that *if* the transferred model structure on the top left exists, then the top functor is right Quillen (by the previous comment, it preserves (acyclic) fibrations iff its composite with the right functor does, which is equivalently the case if the left-bottom composite is right Quillen, which is the case by the existence of the transferred structure on the left)



