
consider

$$
  \flat X 
    \overset{ \phantom{A} \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
  &#643; X
$$

hence

$$
  Disc \Gamma X 
    \overset{ \phantom{A} \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
  Disc \Pi X
$$


form the $(Disc \dashv \Gamma)$-adjoint:

$$
  \underset{
    = id_{\Gamma X}
  }{
  \underbrace{
    \Gamma X
      \underoverset{iso}{ \phantom{A} \eta^{\flat}_{\Gamma X} \phantom{A} }{ \longrightarrow }
    \Gamma Disc \Gamma X 
      \underoverset{iso}{ \phantom{A} \Gamma \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
    \Gamma X
  }}
      \overset{ \phantom{A} \Gamma \eta^{&#643;}_X \phantom{A}  }{\longrightarrow}
    \Gamma Disc \Pi X
$$

and postcompose

$$
    \Gamma X
      \overset{ \phantom{A} \Gamma \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
    \Gamma Disc \Pi X
      \underoverset{iso}{ \phantom{A} \left(\eta^{ \flat }_{\Pi X}\right)^{-1} \phantom{A} }{ \longrightarrow }
    \Pi X
$$

alternatively, form the $(\Pi \dashv Disc)$-adjoint


$$
  \Pi Disc \Gamma X 
    \overset{ \phantom{A} \Pi \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
  \underset{ = id_{\Pi X} }{
    \underbrace{
      \Pi X
        \underoverset{iso}{ \phantom{A} \Pi \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
      \Pi Disc \Pi X
        \underoverset{iso}{ \phantom{A} \epsilon^{&#643;}_{\Pi X} \phantom{A}}{\longrightarrow}
      \Pi X
    }
  }
$$

and precompose

$$
  \Gamma X
    \overset{ \phantom{A} \left(\eta^{&#643;}_{\Gamma X}\right)^{-1} \phantom{A} }{\longrightarrow}
  \Pi Disc \Gamma X 
    \overset{ \phantom{A} \Pi \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
 \Pi X
$$

and more

$$
  \array{
    \Pi Disc \Gamma X 
      &\overset{ 
         \phantom{A} \Pi \epsilon^{\flat}_X \phantom{A} 
       }{\longrightarrow}
     &
   \Pi X
   \\
   {}^{ \mathllap{ \Pi Disc \Gamma \eta^\flat_X } }
   \big\downarrow^{ \mathrlap{\simeq} }
     && 
   {}^{\mathllap{\simeq}}\big\downarrow^{\mathrlap{ \Pi \eta^\flat_X }}
   \\
   \Pi Disc \Gamma Disc \Gamma X
    & \underset{ \Pi \epsilon^{\flat}_{Disc \Gamma X} }{\longrightarrow}&
   \Pi Disc \Gamma X
  }
$$

now consider

$$
  Disc X
    \overset{ \phantom{A} \eta^{\sharp}_{Disc X} \phantom{A} }{\longrightarrow}
  \sharp Disc X
$$

hence 

$$
  Disc X
    \overset{ \phantom{A} \eta^{\sharp}_{Disc X} \phantom{A} }{\longrightarrow}
  coDisc \Gamma  Disc X
$$

and postcompose

$$
  Disc X
    \overset{ \phantom{A} \eta^{\sharp}_{Disc X} \phantom{A} }{\longrightarrow}
  coDisc \Gamma  Disc X
    \overset{ coDisc \left( \eta^{\flat}_{X} \right)^{-1} }{ \longrightarrow}
  coDisc X
$$

+-- {: .num_lemma}
###### Lemma

Consider an [[adjoint triple]]

$$
  Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AA} Disc \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\longleftarrow}
    }
  \mathbf{B}
$$

Then application of the [[functor]] $\Gamma$ on any [[morphism]] $\mathbf{X} \overset{f}{\to} \mathbf{Y} \;\;\in \mathbf{H}$ is equal to the operations of

1. [[composition|pre-composition]] with the $(Disc \dashv \Gamma)$-[[adjunction counit]] $\epsilon^\flat_{\mathbf{X}}$, followed by passing to the  $(Disc \dashv \Gamma)$-[[adjunct]];

1. [[composition|post-composition]] with the $(\Gamma \dashv coDisc)$-[[adjunction unit]] $\eta^{ \sharp }_{\mathbf{Y}}$, followed by passing to the $(\Gamma \dashv coDisc)$-[[adjunct]]:

\[
  \label{PostcompositionWithEtaAsGamma}
  \Gamma_{\mathbf{X}, \mathbf{Y}} \;=\;  \widetilde{\eta^\sharp_{\mathbf{Y}} \circ (-)}
  \;=\;
  \widetilde{ (-) \circ \epsilon^\flat_{\mathbf{X}} }
  \,.
\]

=--

+-- {: .proof}
###### Proof

For the first equality, consider the following [[naturality square]] for the adjunction hom-isomorphism ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)):

$$
  \array{
    Hom_{\mathbf{B}}( \Gamma \mathbf{Y} , \Gamma \mathbf{Y} )
    &\overset{\widetilde {(-)}}{\longrightarrow}&
    Hom_{\mathbf{H}}( \mathbf{Y}, coDisc \Gamma \mathbf{Y} )
    \\
    {}^{\mathllap{ Hom_{\mathbf{B}}(\Gamma(f), \Gamma \mathbf{Y}) }}
    \big\downarrow
    &&
    \!\!\!\!\!
    \big\downarrow^{\mathrlap{ Hom_{\mathbf{H}}( f, coDisc \Gamma \mathbf{Y} ) }}
    \\
    Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma \mathbf{Y} )
    &\overset{\widetilde{ (-) }}{\longleftarrow}&
    Hom_{\mathbf{H}}( \mathbf{X}, coDisc \Gamma \mathbf{Y} )
  }
  \phantom{AAAAA}
  \array{
    \{ \Gamma \mathbf{Y} \overset{id_{\Gamma \mathbf{Y}}}{\to} \Gamma \mathbf{Y}\}
    &\longrightarrow&
    \{ \mathbf{Y} \overset{\eta^\sharp_{\mathbf{Y}}}{\to} coDisc \Gamma \mathbf{Y} \}
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    \{ \Gamma \mathbf{X} \overset{\Gamma(f)}{\to} \Gamma \mathbf{Y} \}
    &\longleftarrow&
    \{ \mathbf{X} \overset{\eta^\sharp_{\mathbf{Y}} \circ f}{\longrightarrow} coDisc \Gamma \mathbf{Y} \}    
  }
$$

Chasing the [[identity morphism]] $id_{\Gamma \mathbf{Y}}$ through this diagram, yields the claimed equality, as shown on the right. Here we use that the right [[adjunct]] of the [[identity morphism]] is the [[adjunction unit]], as shown.

The second equality is [[formal duality|fomally dual]]:

$$
  \array{
    Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma \mathbf{X})
    &\overset{\widetilde { (-) }}{\longrightarrow}&
    Hom_{\mathbf{H}}( Disc \Gamma \mathbf{X}  , \mathbf{X})
    \\
    {}^{\mathllap{ Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma(f) )  }}
    \big\downarrow
    &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathbf{X}}( Disc \Gamma \mathbf{X}, f ) 
} }
    \\
    Hom_{\mathbf{B}}( \Gamma \mathbf{X}, \Gamma \mathbf{Y} )
    &\overset{ \widetilde{ (-) } }{\longleftarrow}&
    Hom_{\mathbf{H}}( Disc \Gamma \mathbf{X}, \mathbf{Y} )
  }
  \phantom{AAAAA}
  \array{
     \{ \Gamma \mathbf{X} \overset{id_{\Gamma \mathbf{X}}}{\to} \Gamma \mathbf{X} \}
     &\longrightarrow&
     \{ Disc \Gamma \mathbf{X} \overset{\epsilon^{\flat}_X}{\to} \mathbf{X} \}
     \\
     \big\downarrow 
       &&
     \big\downarrow
     \\
     \{ \Gamma \mathbf{X} \overset{\Gamma(f)}{\to} \Gamma(\mathbf{Y}) \}
     &\longleftarrow& \{ Disc \Gamma \mathbf{X} \overset{f\circ \epsilon^\flat_{\mathbf{X}}  }{\longrightarrow} \mathbf{Y}\}
  }
$$



=--

