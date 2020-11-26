
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

between the [[categories]] of [[Top|TopologicalSpaces]] and of [[DiffeologicalSpaces]], where

* $Cdfflg$ takes a [[topological space]] $X$ to the **continuous diffeology**, namely the diffeological space on the same underlying set $X_s$ whose plots $U_s \to X_s$ are the [[continuous functions]] (from the underlying [[topological space]] of the [[domain]] $U$). 

* $Dtplg$ takes a [[diffeological space]] to the **diffeological topology** ([[D-topology]]), namely the [[topological space]] with the same underlying set $X_s$ and with the [[final topology]] that makes all its plots $U_{s} \to X_{s}$ into [[continuous functions]]: called the _[[D-topology]]_.

  Hence a [[subset]] $O \subset \flat X$ is an [[open subset]] in the [[D-topology]] precisely if for each plot $f \colon U \to X$ the [[preimage]] $f^{-1}(O) \subset U$ is an [[open subset]] in the [[Cartesian space]] $U$.

Moreover:

1. the [[fixed point of an adjunction|fixed points of this adjunction]] $X \in$[[Top|TopologicalSpaces]] (those for which the [[counit of an adjunction|counit]] is an [[isomorphism]], hence here: a [[homeomorphism]]) are precisely the [[Delta-generated topological spaces]] ([i.e.](Delta-generated+topological+space#AsDTopologicalSpaces) [[D-topological spaces]]):

   $$
     X \;\,\text{is}\;\Delta\text{-generated}
     \;\;\;\;\;
     \Leftrightarrow
     \;\;\;\;\;
     Dtplg(Cdffg(X))
     \underoverset{\simeq}{\;\;\epsilon_X\;\;}{\longrightarrow}
     X
   $$

1. this is an [[idempotent adjunction]], which exhibits $\Delta$-generated/[[D-topological spaces]] as a [[reflective subcategory]] inside [[diffeological spaces]] and a [[coreflective subcategory]] inside all [[topological spaces]]:

\[
  \label{DeltaGeneratedSpacesInIdempotentAdjunction}
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
  DTopologicalSpaces
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
\]

Finally, these adjunctions are a sequence of [[Quillen equivalences]] with respect to the:

|  |  |  |
|--|--|--|
| [[classical model structure on topological spaces]] | [[model structure on D-topological spaces]] | [[model structure on diffeological spaces]] |

> Caution: There was a gap in the original proof that $DTopologicalSpaces \simeq_{Quillen} DiffeologicalSpaces$. The gap is claimed to be filled now, see the commented references [here](model+structure+on+diffeological+spaces#References).

=--

These adjunctions and their properties are observed in [Shimakawa-Yoshida-Haraguchi 10, Prop. 3.1, Prop. 3.2, Lemma 3.3](diffeological+space#SYH10). The model structures and Quillen equivalences are due to [Haraguchi 13, Thm. 3.3](#model+structure+on+Delta-generated+topological+spaces#Haraguchi13) (on the left) and [Haraguchi-Shimakawa 13, Sec. 7](model+structure+on+diffeological+spaces#HaraguchiShimakawa13) (on the right, but this may have a gap).

+-- {: .proof}
###### Proof

We spell out the existence of the [[idempotent adjunction]] (eq:DeltaGeneratedSpacesInIdempotentAdjunction):

First, to see we have an [[adjunction]] $Dtplg \dashv Cdfflg$, we check the hom-isomorphism ([here](adjoint+functor#eq:HomIsomorphismForAdjointFunctors)).

Let $X \in DiffeologicalSpaces$ and $Y \in TopologicalSpaces$. Write $(-)_s$ for the underlying sets. Then a [[morphism]], hence a [[continuous function]] of the form

$$
  f \;\colon\; Dtplg(X) \longrightarrow Y
  \,,
$$

is a [[function]] $f_s \colon X_s \to Y_s$ of the underlying [[sets]] such that for every [[open subset]] $A \subset Y_s$ and every [[smooth function]] of the form $\phi \colon \mathbb{R}^n \to X$ the [[preimage]] $(f_s \circ \phi_s)^{-1}(A) \subset \mathbb{R}^n$ is open. But this means equivalently that for every such $\phi$, $f \circ \phi$ is [[continuous function|continuous]].  This, in turn, means equivalently that the same underlying function $f_s$ constitutes a [[smooth function]] $\widetilde f \;\colon\; X \longrightarrow Cdfflg(Y)$.

In summary, we thus have a [[bijection]] of [[hom-sets]]

$$
  \array{
    Hom( Dtplg(X), Y )
    &\simeq&
    Hom(X, Cdfflg(Y))
    \\
    f_s &\mapsto& (\widetilde f)_s = f_s
  }
$$

given simply as the [[identity function|identity]] on the underlying [[functions]] of underlying sets.  This makes it immediate that this hom-isomorphism is [[natural bijection|natural]] in $X$ and $Y$ and this establishes the [[adjunction]]. 

Next, to see that the [[D-topological spaces]] are the [[fixed point of an adjunction|fixed points]] of this adjunction, 
we apply the above [[natural bijection]] on hom-sets to the case

$$
  \array{
    Hom( Dtplg(Cdfflg(Z)), Y )
    &\simeq&
    Hom(Cdfflg(Z), Cdfflg(Y))
    \\
    (\epsilon_Z)_s &\mapsto& (\mathrm{id})_s
  }
$$

to find that the [[counit of the adjunction]]

$$
  Dtplg(Cdfflg(X))
  \overset{\epsilon_X}{\longrightarrow}
  X
$$

is given by the [[identity function]] on the underlying sets $(\epsilon_X)_s = id_{(X_s)}$.

Therefore $\eta_X$ is an [[isomorphism]], namely a [[homeomorphism]], precisely if the open subsets of $X_s$ with respect to the topology on $X$ are precisely those with respect to the topology on $Dtplg(Cdfflg(X))$, which means equivalently that the open subsets of $X$ coincide with those whose pre-images under all continuous functions $\phi \colon \mathbb{R}^n \to X$ are open. This means equivalently that $X$ is a D-topological space.

Finally, to see that we have an [[idempotent adjunction]], we check that the [[comonad]]

$$
  Dtplg \circ Cdfflg \;\colon\; TopologicalSpaces \to TopologicalSpaces
$$

is an [[idempotent comonad]], hence that

$$
  Dtplg \circ Cdfflg
  \overset{
    Dtplg \cdot \eta \cdot Cdfflg
  }{\longrightarrow}
  Dtplg \circ Cdfflg \circ Dtplg \circ Cdfflg
$$

is a [[natural isomorphism]]. But, as before for the adjunction counit $\epsilon$, we have that also the [[adjunction unit]] $\eta$ is the [[identity function]] on the underlying sets. Therefore, this being a natural isomorphism is equivalent to the operation of passing to the D-topological refinement of the topology of a topological space being an idempotent operation, which is clearly the case.

=--



