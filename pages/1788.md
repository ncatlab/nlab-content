
+-- {: .num_prop #PointsToPiecesTransform}
###### Proposition
**([[points-to-pieces transform]])**

Consider an [[adjoint quadruple]] of the form 

$$
  \Pi \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AA} \Pi \phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  \mathbf{B}
$$

(for instance a [[cohesive topos]] over some [[base topos]] $\mathbf{B}$).

Then for all $X \in \mathbf{X}$ the following two [[natural transformations]], constructed from the [[adjunction units]]/[[adjunction counit|counits]] and their [[inverse morphisms]] (using [[idempotent monad|idempotency]]), are equal:

\[
  \label{PointsToPiecesInTheBase}
  ptp_{\mathbf{B}}
  \;\;\coloneqq\;\;
  \left(
    \Pi \epsilon^\flat_X
  \right)
  \circ
  \left(
    \eta^{&#643;}_{\Gamma X}
  \right)^{-1}
  \;\;=\;\;
  \left(
    \eta^\flat_{\Pi X}
  \right)^{-1}
  \circ
  \left(
    \Gamma \eta^{&#643;}_X
  \right)
  \phantom{AAAAAAA}
  \array{
    \Gamma X 
    & \overset{
       \Gamma \eta^{&#643;}_X
   }{\longrightarrow} & 
   \Gamma Disc \Pi X
   \\
   {}^{ \mathllap{
      \left(
       \eta^{&#643;}_{\Gamma X}
     \right)^{-1}    
   } }\big\downarrow 
     & \searrow^{ \mathrlap{ ptp_{\mathbf{B}} }  } & 
   \big\downarrow^{ \mathrlap{  
     \left(
       \eta^\flat_{\Pi X}
     \right)^{-1}
   } }
   \\ 
   \Pi Disc \Gamma X
   &\underset{ 
    \Pi \epsilon^\flat_X
    }{\longrightarrow}&
   \Pi X
  }
\]

Moreover, the image of these morphisms under $Disc$ equals the following composite:

\[
  \label{PointsToPieces}
  ptp_{\mathbf{H}}
  \;\colon\;
  \flat X 
    \overset{ \phantom{A} \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
  &#643; X
  \,,
\]

hence

\[
  \label{PiecesToPointsFromBase}
  ptp_{\mathbf{H}} \;=\; Disc(ptp_{\mathbf{B}})
  \,.
\]

Either of these morphisms we call the _[[points-to-pieces transform]]_.

=--

+-- {: .proof}
###### Proof

For the second statement, notice that the $(Disc \dashv \Gamma)$-[[adjunct]] of

$$
  ptp_{\mathbf{H}}
  \;\colon\;
  Disc \Gamma X 
    \overset{ \phantom{A} \epsilon^{\flat}_X \phantom{A} }{\longrightarrow}
  X
    \overset{ \phantom{A} \eta^{&#643;}_X \phantom{A} }{\longrightarrow}
  Disc \Pi X
$$

is

\[
  \label{AdjunctOfptpH}
  \widetilde{ ptp_{\mathbf{H}} }
  \;\;=\;\;
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
  \,,
\]

where under the braces we uses the [[zig-zag identity]]. 

(As a side remark, for later usage, we observe that the morphisms on the left in (eq:AdjunctOfptpH) are [[isomorphisms]], as shown, by [[idempotent monad|idempotency]] of the adjunctions.)  

From this we obtain the following [[commuting diagram]]:

$$
  \array{
    Disc \Gamma X
      &\overset{ \phantom{A} Disc \Gamma \eta^{&#643;}_X \phantom{A} }{\longrightarrow}&
    Disc \Gamma Disc \Pi X
      &\underoverset{iso}{ \phantom{A} Disc \left(\eta^{ \flat }_{\Pi X}\right)^{-1} \phantom{A} }{ \longrightarrow }&
    Disc \Pi X
    \\
    &{}_{\mathllap{ ptp_{\mathbf{H}} }}\searrow&
    {}^{ \mathllap{ \epsilon^{\flat}_{Disc \Pi X} } }
    \big\downarrow^{\mathrlap{\simeq}}
     & 
    \nearrow_{\mathrlap{id_{\Pi X}}}
    \\
    && Disc \Pi X
  }
$$

Here:

1. on the left we identified $\widetilde {\widetilde {ptp_{\mathbf{H}}}} \;=\;  ptp_{\mathbf{\mathbf{H}}}$ by applying the formula for $(Disc \dashv \Gamma)$-[[adjuncts]] to $\widetilde {ptp_{\mathbf{H}}} = \Gamma \eta^{&#643;}_X$ (eq:AdjunctOfptpH);

1. on the right we used the [[zig-zag identity]] for $(Disc \dashv \Gamma)$.

This proves the second statement.

=--




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

+-- {: .num_lemma #ReExpressingMiddleFunctorInAdjointTriple}
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

+-- {: .num_prop}
###### Proposition


Consider an [[adjoint quadruple]] of the form 

$$
  \Pi \dashv Disc \dashv \Gamma \dashv coDisc
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{\phantom{AA} \Pi \phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} Disc \phantom{AA} }{\hookleftarrow}
      \\
      \overset{\phantom{AAA} \Gamma \phantom{AAA} }{\longrightarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookleftarrow}
    }
  \mathbf{B}
$$

(for instance a [[cohesive topos]] over some [[base topos]] $\mathbf{B}$).

Then the following are equivalent:

1. [[pieces have points]]: 

   1. as seen in $\mathbf{B}$: For every [[object]] $X \in \mathbf{X}$ the [[points-to-pieces transform]] (Prop. \ref{PointsToPiecesTransform}) in $\mathbf{B}$ (eq:PointsToPiecesInTheBase) is an [[epimorphism]]:

   $$
     ptp_{\mathbf{B}}
     \;\colon\;
     \Gamma X \overset{ epi }{\longrightarrow} \Pi X
   $$

   1. equivalently, as seen in $\mathbf{H}$: For every [[object]] $X \in \mathbf{X}$ the [[points-to-pieces transform]] (Prop. \ref{PointsToPiecesTransform}) in $\mathbf{H}$ (eq:PointsToPieces) is an [[epimorphism]]:

   $$
     ptp_{\mathbf{H}}
     \;\colon\;
     \flat X \overset{ epi }{\longrightarrow} &#643; X
   $$

1. [[discrete objects are concrete]]: For every [[object]] $S \in \mathbf{B}$ the [[discrete object]] $Disc(S)$ is a [[concrete object]], in that the [[sharp modality|sharp]] [[adjunction counit]] on $Disc(S)$ is a [[monomorphism]]:

   $$
     \eta^\sharp_{Disc(S)}
     \;\colon\;
     Disc S
       \overset{ mono }{\longrightarrow}
     \sharp Disc S
   $$
   
=--

+-- {: .proof}
###### Proof

First observe the equivalence of the first two statements:

$$
  ptp_{\mathbf{H}} \;\; \text{is epi}
  \phantom{AAA}
  \text{iff}
  \phantom{AAA}
  ptp_{\mathbf{B}} \;\; \test{is epi}
  \,.
$$

In one direction, assume that $ptp_{\mathbf{B}}$ is an epimorphism. By (eq:PiecesToPointsFromBase) we have $ptp_{\mathbf{H}} = Disc(ptp_{\mathbf{B}})$, but $Disc$ is a [[left adjoint]] and left adjoints preserve monomorphisms.

In the other direction, assume that $ptp_{\mathbf{H}}$ is an epimorphism. By (eq:PointsToPiecesInTheBase) and (eq:AdjunctOfptpH) we see that $ptp_{\mathbf{B}}$ is re-obtained from this by applying $\Gamma$ and then composition with isomorphisms. But $\Gamma$ is again a left adjoint, and hence preserves epimorphism, as does composition with isomorphisms.

By applying (eq:PointsToPiecesInTheBase) again, we find in particular that _[[pieces have points]]_ is also equivalent to $\Pi \epsilon^\flat_{Disc S}$ being an epimorphism, for all $S \in \mathbf{B}$. But this is equivalent to

$$
  Hom_{\mathbf{B}}(\Pi \epsilon^\flat_{\mathbf{X}}, S)
  =
  Hom_{\mathbf{\mathbf{H}}}(\epsilon^\flat_{\mathbf{X}}, Disc(S))  
$$

being a [[monomorphism]] for all $S$ (by adjunction isomorphism and definition of [[epimorphism]]).

Now by Lemma \ref{ReExpressingMiddleFunctorInAdjointTriple}, this is equivalent to

$$
  Hom_{\mathbf{H}}( \mathbf{X}, \eta^\sharp_{Disc(S)} )
$$

being a monomorphism, which is equivalent to $\eta^\sharp_{Disc(S)}$ being a monomorphism, hence to _[[discrete objects are concrete]]_.


=--

