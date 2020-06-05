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
  }{\phantom{AA}\bot\phantom{AA}}
  DiffeologicalSpaces
$$

between the categories of [[Top|TopologicalSpaces]] and of [[DiffeologicalSpaces]], where

* $Cdfflg$ takes a [[topological space]] $X$ to the **continuous diffeology**, namely the diffeological space on the same underlying set $\flat X$ whose plots $U \to X$ are the [[continuous functions]] (from the underlying [[topological space]] of the domain $U$). 

* $Dtplg$ takes a [[diffeological space]] to the **diffeological topology** ([[D-topology]]), namely the [[topological space]] with the same underlying set $\flat X$ and with the [[final topology]] that makes all its plots $U_{set} \to X_{set}$ into [[continuous functions]]: called the _[[D-topology]]_.

  Hence a [[subset]] $O \subset \flat X$ is an [[open subset]] in the [[D-topology]] precisely if for each plot $f \colon U \to X$ the [[preimage]] $f^{-1}(O) \subset U$ is an [[open subset]] in the [[Cartesian space]] $U$.

Moreover:

1. the [[fixed point of an adjunction|fixed points of this adjunction]] $X \in$[[Top|TopologicalSpaces]] (those for which the [[counit of an adjunction|counit]] is an [[isomorphism]], hence here: a [[homeomorphism]]) are precisely the [[Delta-generated topological spaces]]:

   $$
     X \;\,\text{is}\;\Delta\text{-generated}
     \;\;\;\;\;
     \Leftrightarrow
     \;\;\;\;\;
     Dtplg(Cdffg(X))
     \underoverset{\simeq}{\;\;\epsilon_X\;\;}{\longrightarrow}
     X
   $$

1. this is an [[idempotent adjunction]], which exhibits $\Delta$-generated topological spaces as a [[reflective subcategory]] inside [[diffeological spaces]] and a [[coreflective subcategory]] inside all [[topological spaces]]:

$$
  TopologicalSpaces
  \underoverset
    {
      \underset{
       Cdfflg
      }{\longrightarrow}
    }
    {
      \overset{
      }{\hookleftarrow}
    }
    {\phantom{AA}\bot\phantom{AA}}
  DeltaGeneratedSpaces
  \underoverset
    {
      \underset{
      }{\hookrightarrow}
    }
    {
      \overset{
       Dtplg
      }{\longleftarrow}
    }
    {\phantom{AA}\bot\phantom{AA}}
  DiffeologicalSpaces
$$

=--

This is ([Shimakawa-Yoshida-Haraguchi 10, Prop. 3.1, Prop. 3.2, Lemma 3.3](diffeological+space#SYH10))
