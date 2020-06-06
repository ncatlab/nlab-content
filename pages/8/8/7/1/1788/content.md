
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
         Dtplg
      }{\longleftarrow}
    }
    {\phantom{AA}\bot\phantom{AA}}
  DiffeologicalSpaces
$$

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
  EuclideanGeneratedSpaces
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


First, to see we have an [[adjunction]] $Dtplg \dashv Cdfflg$, we check the hom-isomorphism ([here](adjoint+functor#eq:HomIsomorphismForAdjointFunctors))

Let $X \in DiffeologicalSpaces$ and $Y \in TopologicalSpaces$. Write $(-)_s$ for the underlying sets. Then a morphism ([[continuous function]])

$$
  f \;\colon\; Dtplg(X) \longrightarrow Y
$$

is a [[function]] $f_s \colon X_s \to Y_s$ of the underlying sets such that for every [[open subset]] $A \subset Y_s$ and every [[smooth function]] of the form $\phi \colon \mathbb{R}^n \to X$ the [[preimage]] $(f_s \circ \phi_s)^{-1}(A) \subset \mathbb{R}^n$ is open. But this means equivalently that for every such $\phi$, $f \circ \phi$ is [[continuous function|continuous]].  This, in turn, means equivalently that the same underlying function $f_s$ constitutes a [[smooth function]] $\widetilde f \;\colon\; X \longrightarrow Cdfflg(Y)$.

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

given simply as the [[identity function|identity]] on the underlying [[functions]] of underlying sets. This establishes the [[adjunction]]. This makes it immediate that this hom-isomorphism is [[natural bijection|natural]] in $X$ and $Y$.

Next, to see that the [[Euclidean-generated topological spaces]] are the [[fixed point of an adjunction|fixed points]] of this adjunction, 
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

Therefore $\eta_X$ is an [[isomorphism]], namely a [[homeomorphism]], precisely if the open subsets of $X_s$ with respect to the topology on $X$ are precisely those with respect to the topology on $Dtplg(Cdfflg(X))$, which means equivalently that the open subsets of $X$ coincide with those whose pre-images under all continuous functions $\phi \colon \mathbb{R}^n \to X$ are open. This means equivalently that $X$ is a Euclidean-generated space.

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

is a [[natural isomorphism]]. But, as before for the adjunction counit $\epsilon$, we have that also the [[adjunction unit]] $\eta$ is the [[identity function]] on the underlying sets, so that this being a natural isomorphism is equivalent to stating that the operation of passing to the Euclidean-generated refinement of the topologogy of a topological space is an idempotent operation, which is clearly the case.




