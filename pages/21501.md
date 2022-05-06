+-- {: .num_prop #AdjunctionBetweenTopologicalSpacesAndDiffeologicalSpaces}
###### Proposition
**([[adjunction between topological spaces and diffeological spaces]])**


There is a pair of [[adjoint functors]]

$$
  TopologicalSpaces
  \underoverset{
    \underset{
      Cdfflg
    }{\longrightarrow}
  }{
    \overset{
      Dtplg
    }{\longleftarrow}
  }{\bot}
  DiffeologicalSpaces
$$

between the categories of [[Top|TopologicalSpaces]] and of [[DiffeologicalSpaces]], where

* $Cdfflg$ takes a [[topological space]] $X$ to the **continuous diffeology**, namely the diffeological space on the same underlying set $\flat X$ whose plots $U \to X$ are the [[continuous functions]] (from the underlying [[topological space]] of the domain $U$). 

* $Dtplg$ takes a [[diffeological space]] to the **diffeological topology** ([[D-topology]]), namely the [[topological space]] with the same underlying set $\flat X$ and with the [[final topology]] that makes all its plots $U_{set} \to X_{set}$ into [[continuous functions]]: called the _[[D-topology]]_.

  Hence a [[subset]] $O \subset \flat X$ is an [[open subset]] in the [[D-topology]] precisely if for each plot $f \colon U \to X$ the [[preimage]] $f^{-1}(O) \subset U$ is an [[open subset]] in the [[Cartesian space]] $U$.

Moreover, the [[fixed point of an adjunction|fixed points of this adjunction]] $X \in$[[Top|TopologicalSpaces]] (those for which the [[counit of an adjunction|counit]] is an [[isomorphism]], hence here: a [[homeomorphism]]) are precisely the [[Delta-generated topological spaces]]:

$$
  X \; \Delta\text{-generated}
  \;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;
  Dtplg(Cdffg(X))
  \underoverset{\simeq}{\;\;\epsilon_X\;\;}{\longrightarrow}
  X
$$

This exhibits $\Delta$-generated topological spaces as a [[coreflective subcategory]] inside all [[topological spaces]].

=--

This is ([Shimakawa-Yoshida-Haraguchi 10, Prop. 3.1, Prop. 3.2](diffeological+space#SYH10))
